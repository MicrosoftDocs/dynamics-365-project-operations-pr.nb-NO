---
title: Oppdatere Project Operations i Økonomi-miljøet
description: Dette emnet gir informasjon om hvordan du oppdaterer Project Operations i Dynamics 365 Finance-miljøet.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291991"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Oppdatere Project Operations i Økonomi-miljøet

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Dette emnet gir informasjon om hvordan du oppdaterer Dynamics 365 Project Operations i Dynamics 365 Finance-miljøet. Det er tre prosedyrer som kreves for å oppdatere Project Operations til Update 5 (UR5):

- [Importere pakken til forhåndsvisningsprosjektet](#import)
- [Ta i bruk oppdateringen](#apply)
- [Oppdatere Dataverse-miljøet](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importere pakken til LCS-prosjektet

1. Logg på [Lifecycle Services (LCS)](https://lcs.dynamics.com/) som prosjekteier eller miljøleder.
2. Fra listen over prosjekter velger du LCS-prosjektet.
3. På siden **Prosjekt** i gruppen **Miljøer** åpner du miljøet du vil oppdatere.
4. Bekreft at miljøet kjører. Hvis det ikke er startet, starter du miljøet.
5. I delen **Ny versjon** under **Tilgjengelige oppdateringer** velger du **Vis oppdatering** for 10.0.15.

![Vis oppdatering, knapp](media/view-update.png)

6. På siden **Binære oppdateringer** velger du **Lagre pakke**.
7. På siden **Se gjennom og lagre oppdateringer** velger du **Lagre pakke**.
8. I ruten **Lagre pakke i aktivabibliotek** som åpnes, angir du pakkenavnet og velger deretter **Lagre pakke**.
9. Når LCS er ferdig med å lagre pakken, aktiveres **Ferdig**-knappen. Velg **Ferdig**. LCS verifiserer pakken. Verifisering kan ta noen minutter eller opptil én time.


## <a name="apply-the-package-update"></a><a name="apply"></a>Ta i bruke pakkeoppdateringen

1. På siden **Miljødetaljer** i LCS velger du **Oppretthold** > **Bruk oppdateringer**.
2. Velg pakken du lagret tidligere, fra listen, og velg deretter **Bruk**.
3. Velg **Ja** for å bekrefte at du vil distribuere pakken.

![Dialogboksen Bekreft distribusjon av pakke](media/confirm-package-deployment.png)

4. Velg **Ja** for å bekrefte at du vil oppdatere appen.

![Dialogboksen Bekreft oppdatering av app](media/confirm-application-update.png)

Distribusjonen og appoppdateringen starter. 

På siden **Miljødetaljer** blir miljøstatusen oppdatert til **Betjener** i hjørnet øverst til høyre. Oppdateringen blir fullført på ca. to timer. Informasjonen om apputgivelsen oppdateres til **Microsoft Dynamics 365 for Finance and Operations 10.0.15)**, og miljøstatusen oppdateres til **Distribuert**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Oppdatere Dataverse-miljøet

1. Logg på [Power Platform-administrasjonssenteret](https://admin.powerplatform.com/).
2. I listen finner og åpner du miljøet du brukte til å installere Project Operations.
3. På siden **Miljøer** velger du **Ressurs** > **Dynamics 365-apper**.
4. I listen finner du **Microsoft Dynamics 365 Project Operations**, og i kolonnen **Status** velger du **Oppdatering er tilgjengelig**.
5. Merk av for **Jeg godtar servicebetingelsene**, og velg deretter **Oppdater**. Den nyeste versjonen av løsningen blir installert.

Når installasjonen er fullført, har du versjonsnummeret 4.5.0.134 installert.

## <a name="configure-new-features"></a>Konfigurere nye funksjoner

### <a name="enable-dual-write-mapping"></a>Aktivere tilordning for dobbel skriving

Når du har fullført oppdateringen av Økonomi- og Dataverse-miljøene, kan du aktivere de nødvendige tilordningene for dobbel skriving. Fullfør følgende prosedyrer for å aktivere tilordninger for dobbel skriving.

- [Oppdatere sikkerhetsinnstillinger i Customer Engagement-miljøet](#security)
- [Oppdatere dataenheter](#refresh)
- [Oppdatere og kjøre tilordninger for dobbel skriving](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Oppdatere sikkerhetsinnstillinger i Dataverse-miljøet

Følgende oppdateringer av sikkerhetsrettighetene for enheter nedenfor kreves som en del av oppdateringen til UR5.

1. I Dataverse-miljøet går du til **Innstillinger**, og i gruppen **System** velger du **Sikkerhet**.

![Innstillinger for Dataverse-miljø](media/Picture21.png)

2. Velg **Sikkerhetsroller**.
3. Fra listen over roller velger du **appbruker med dobbeltskriving** og velger kategorien **Egendefinerte enheter**. 
4. Kontroller at rollen har tillatelsene **Lese** og **Tilføye i** for følgende:

      - **Valutakurstype**
      - **Plan over kontoer** 
      - **Regnskapskalender** 
      - **Finans**

5. Etter at sikkerhetsrollen er oppdatert, går du til **Innstillinger** > **Sikkerhet** > **Team**. Kontroller at rollen **appbruker med dobbeltskriving** er brukt på teamet. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Oppdatere dataenheter fra oppdateringen

1. I økonomimiljøet åpner du arbeidsområdet **Databehandling**, og deretter åpner du siden **Rammeverkparametre**.
2. I kategorien **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.
3. Velg **Lukk** for å bekrefte oppdatering av enheten.

 > [!NOTE]
 > Det tar omtrent 20 minutter å fullføre denne prosessen. Du blir varslet når oppdateringen er fullført.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Oppdatere tilordninger for dobbel skriving

1. I arbeidsområdet **Databehandling** velger du **Dobbel skriving**.
2. Velg **Bruk løsninger**, velg begge løsningene fra listen, og velg deretter **Bruk**.
3. På siden **Dobbel skriving** velger du følgende tabelltilordninger, og deretter velger du **Stopp**.

    - **Faktiske verdier for Project Operations-integrering (msdyn_actuals)**
    - **Prosjektutgiftskategorier for Project Operations-integrering (msdyn_expensecategories)**
    - **Faktiske verdier for enhet for prosjektutgiftsrapport for Project Operations-integrering (msdyn_expenses)**

4. På siden **Tabelltilordningsversjon** bruker du en ny versjon av tilordningen for hver av de tre enhetene.
5. På siden **Dobbel skriving** velger du Kjør for å starte tilordningene på nytt.
6. Fra listen over tilordninger velger du tilordningen **Finans (msdyn_ledgers)** med alle dens krav, og deretter merker du av for **Første synkronisering**. 
7. I feltet **Hovedoppføring for første synkronisering** velger du **Finance and Operations-apper** og velger deretter **Kjør**.
 
 ![Synkronisering av finanstilordning](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]