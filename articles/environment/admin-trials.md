---
title: Registrer deg for Project Operations-prøveversjoner
description: Dette emnet gir informasjon om hvordan du distribuerer en prøveversjon av Dynamics 365 Project Operations.
author: ruhercul
ms.date: 12/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e40b4ac23241730f5c2db89f0dc674083f9e7abe
ms.sourcegitcommit: 8f970b46d0303dafaa75fc7d00567d232e1e600b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901629"
---
# <a name="sign-up-for-project-operations-trials"></a>Registrer deg for Project Operations-prøveversjoner 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering, og Project Operations for lagerførte/produksjonsbaserte scenarioer_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet forklarer hvordan du abonnerer på forhåndsversjonspartnertilbudet og distribuerer et Dynamics 365 Project Operations-miljø.

Med den nye prøveversjonen av Project Operations kan du automatisk distribuere et av de tre støttede distribusjonsscenarioene ved å fylle ut et spørreskjema som anbefaler den beste distribusjonsmåten. Dette emnet gir informasjon om hvordan du:

- løser inn prøveversjonstilbudet
- iverksetter klargjøring
- konfigurerer dobbel skriving
- finner ut mer om Project Operations 

Tabellen nedenfor viser detaljene for det nye prøveversjonstilbudet.

| **Tilbudselement**               | **Detaljer**                                  |
|------------------------------|----------------------------------------------|
| Tilbudstype                   | Denne tilbudstypen er administratorkundeemne, slik at en leieradministrator er nødvendig for å få tilgang til tilbudet. |
| Bruk av tilbud                    | Én gang per leier                          |
| Tilbudsvarighet               | 30 kalenderdager                             |
| Innløsning per leietaker       | 1                                            |
| Antall brukere              | 25                                           |
| Internnummer                    | 1 utvidelse, 30 kalenderdager               |
| Antall prøveversjonsmiljøer | 3                                            |


## <a name="admin-trial-details"></a>Detaljer om administratorprøveversjon
Tabellen nedenfor viser prøveversjonsdetaljene og hvordan de gjelder for hver distribusjonstype.

| **Vare**                      | **Lite**                                     | **Ikke lagerført beholdning** | **Lagerført beholdning** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Konfigurasjonsdata gitt           | Ja                                          | Ja                       | Ja (USSI)            |
| Transaksjonsdata            | No                                           | No                        | No                    |
| Klargjøringstid i minutter  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Forutsetninger
Forutsetningene nedenfor kreves for å distribuere en prøveversjon av Dynamics 365 Project Operations.

- Registrer deg for [Dynamics 365 Project Operations – forhåndsversjon](https://www.aka.ms/try-po).
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.

> [!IMPORTANT]
> Bare én person i en organisasjon, leieradministratoren, må utføre denne oppgaven. Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations – forhåndsversjon 

Før du begynner logger du på en nettleser med brukerkontoen i leieren der du vil ha forhåndsversjonen av Project Operations.

1. Løs inn den første tilbudskoden **Dynamics 365 Project Operations – forhåndsversjon** ved å lime den inn i nettadressen i nettleseren.

    ![Løs inn tilbud](./media/16RedeemFirstOfferNew.png)

2. Bekreft ordren.

    ![Bekreft ordren](./media/17ConfirmOrderNew.png)

  Du ser bekreftelsen på at tilbudet er innløst.

   ![Bekreftelse](./media/18OrderConfirmationNew.png)

  Du blir omdirigert til [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Spørreskjema og klargjøring

1.  Gå til [Power Platform-administrasjonssenteret](https://admin.powerplatform.com/projectoperationstrial) og fullfør spørreskjemaet.  
2.  Se gjennom den anbefalte distribusjonstypen, og velg **Start installasjonsprogrammet** for å starte klargjøringen.
3.  Se gjennom vilkårene, og velg deretter **Start**.

   Når klargjøringen har startet, blir du omdirigert til miljølisten i Power Platform-administrasjonssenteret. Når klargjøring pågår, er tilstanden for miljøet **PreparingInstance**.
 
  Når klargjøringen er fullført, er tilstanden for miljøet **klar**. Klargjøring av miljøet inkluderer distribusjon av demonstrasjonsdata.
 
4.  Velg den respektive Microsoft Dataverse-nettadressen og nettadressene for Finance and Operations-apper for å validere distribusjonen.

## <a name="configuring-dual-write"></a>Konfigurasjon av dobbel skriving
- Hvis du vil konfigurere sikkerhetsroller for dobbeltskriving, kan du se [Oppdatere sikkerhetsinnstillinger for Project Operations i Dataverse](resource-provision-new-environment.md).
- Hvis du vil konfigurere tilordninger for dobbeltskriving, kan du se [Kjøre Project Operations med tilordninger for dobbel skriving](resource-provision-new-environment.md#run-project-operations-dual-write-maps).

## <a name="assign-licenses"></a>Tilordne lisenser

Du må ha administrativ tilgang til organisasjonens Microsoft 365-portal for å kunne utføre følgende trinn.

1. Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisensene til brukerne.

   ![Startsiden for administrasjonssenteret](./media/14AdminPortal.png)

2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.

   ![Tilordne lisenser](./media/15AssignLicenses.png)

3. Kontroller at lisensen for **Dynamics 365 Project Operations-forhåndsversjonen** er valgt, og velg **Lagre endringer**.

## <a name="additional-resources"></a>Ytterligere ressurser

Følgende ressurser gir nyttig veiledning når du begynner arbeidet med Project Operations:

- [Videoserie – Oversikt over Project Operations, fordypning i funksjoner og veikart](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Fastslå distribusjonstypen](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Hva skjer hvis jeg trenger ALM eller ELM for Finance and Operations-appmiljøet?

- Partnere som trenger fullstendige funksjoner for administrasjon av miljølivssyklusen, kan du se [Lisensforespørselen for partnersandkassen](https://experience.dynamics.com/requestlicense) for å se gjennom det nye partnertilbudet. 
- For partnere som ønsker mer informasjon om interne bruksrettigheter, kan du se [Skyen for interne bruksrettigheter og programvarefordeler (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kan jeg forlenge prøveversjonen utover 30 dager?
Fullfør trinnene nedenfor for å forlenge prøveversjonen.

1. Gå til **Fakturering** > **Dine produkter** i **administrasjonssenteret for Microsoft 365**.
2. Velg **Dynamics 365 Project Operations (CE) – forhåndsversjon**.
3. Velg **Forleng dato** under **Utløpsdato**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kan jeg oppgradere fra Lite-distribusjonen til ressursbaserte/ikke-lagerbaserte scenarioer?
Det er for øyeblikket ingen støtte for oppgradering av et miljø fra Lite til en ikke-lagerbasert distribusjon.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Får jeg tilgang til LCS (Lifecycle Services) for Finance-miljøene mine?  
Nei. Distribusjonen håndteres via Power Platform-administrasjonssenteret for disse prøveversjonene. Tilgang til Finance-miljøet er begrenset.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kan jeg installere prøveversjonen i et eksisterende miljø?
Hvis du har et eksisterende miljø, kan du installere Lite-distribusjonen i et eksisterende Dataverse-salgsmiljø fra Power Platform-administrasjonssenteret.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
