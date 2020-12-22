---
title: Klargjør et nytt miljø
description: Dette emnet gir informasjon om hvordan du klargjør et nytt Project Operations-miljø.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642995"
---
# <a name="provision-a-new-environment"></a>Klargjør et nytt miljø

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet gir informasjon om hvordan du klargjør et nytt Dynamics 365 Project Operations-miljø for ressursbaserte/ikke-lagerbaserte scenarioer.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Aktiver automatisk klargjøring av Project Operations i et LCS-prosjekt

Bruk fremgangsmåten nedenfor for å aktivere den automatiserte klargjøringsflyten for Project Operations for LCS-prosjektet.

1. Gå til [LCS](https://lcs.dynamics.com/v2), og velg flisen **Behandling av evalueringsfunksjonalitet**.
2. I listen **Evalueringsfunksjonalitet** velger du **Project Operations-funksjonen** og deretter **Evalueringsfunksjonalitet aktivert** for å aktivere Project Operations.

> [!NOTE]
> Dette trinnet utføres bare én gang per LCS-prosjekt.

## <a name="provision-a-project-operations-environment"></a>Klargjør et Project Operations-miljø

1. Åpne en ny Dynamics 365 Finance-distribusjon med et [demonstrasjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) eller et [sandkasse-/produksjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Gå gjennom veiviseren for **klargjøring av miljø**. 

> [!IMPORTANT]
> Kontroller at den valgte programversjon er 10.0.13 eller høyere.

3. Du klargjør Project Operations ved å gå til **Avanserte innstillinger** og velge **Common Data Service**. 
4. Aktiver **Common Data Service-innstillingen** ved å velge **Ja**, og skriv deretter inn informasjon i de obligatoriske feltene:

  - Navn
  - Område
  - Language
  - Valuta
 
5. I feltet **Common Data Service-mal** velger du **Project Operations** 

6. Velg miljøtypen for distribusjonen din. En abonnementsbasert prøveversjon gjør det mulig å distribuere et CDS-miljø i 30 dager. 

![Distribusjonsinnstillinger](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Velg **Godtar** for å bekrefte vilkårene for bruk, og velg deretter **Ferdig** for å gå tilbake til distribusjonsinnstillingene.

![Distribusjonssamtykke](./media/2DeploymentConsent.png)

7. Fyll ut de gjenstående nødvendige feltene i veiviseren, og bekreft distribusjonen. Tiden det tar å klargjøre miljøet, varierer avhengig av miljøtypen. Klargjøring kan ta opptil seks timer.

  Når distribusjonen er fullført, viser miljøet som **Distribuert**.

8. For å bekrefte at miljøet er distribuert velger du **Logg på** og logger deg på miljøet for å bekrefte.

![-miljødetaljer](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Bruk Project Operations Finance-demodata (valgfritt trinn)

Bruk Project Operations Finance-demodata for det skydriftede miljøet i versjon 10.0.13, som beskrevet i [denne artikkelen](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Bruk oppdateringer i Finance-miljøet

Project Operations krever et Finance-miljø med programversjon **10.0.13 (10.0.569.20009)** eller høyere.

Det kan hende du må bruke kvalitetsoppdateringer i Finance-miljøet for å få denne versjonen.

1. I LCS, på siden **Miljødetaljer**, i delen **Tilgjengelige oppdateringer**, velger du **Vis oppdatering**.

![Vis oppdateringer](./media/5ViewUpdates.png)

2. På siden **Binære oppdateringer** velger du **Lagre pakke.**

![Lagre pakke](./media/6SavePackage.png)

3. Klikk **Velg alle**, og velg deretter **Lagre pakke**.

![Se gjennom og lagre oppdateringer](./media/7ReviewAndSaveUpdates.png)

4. Skriv inn et navn og en beskrivelse av pakken, og velg deretter **Lagre**. Denne prosessen kan ta tid, avhengig av Internett-tilkoblingen.

![Last opp pakke til aktivabibliotek](./media/8UploadPackageToAssetsLibrary.png)

5. Etter at pakken er lagret, velger du **Fullført** og lagrer denne pakken i aktivabiblioteket i LCS-prosjektet.

Lagring og validering av pakken kan ta omtrent 15 minutter.

6. For å bruke oppdateringen går du til siden **Miljødetaljer** i LCS og velger **Vedlikehold** > **Bruk oppdateringer**.

![Vedlikeholde miljøer](./media/9MaintainEnvironment.png)

7. I listen over oppdateringer velger du pakken du opprettet, og deretter velger du **Bruk**.

![Bruke oppdateringer](./media/10ApplyUpdates.png)

Behandling av miljøet kan ta litt tid. Når det er ferdig, går miljøet tilbake til en distribuert tilstand.

![Miljø distribuert](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Opprett en tilkobling for dobbel skriving 

1. I LCS-prosjektet går du til siden **Miljødetaljer**.
2. Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps**.
3. Når koblingen er fullført, velger du **Koble til CDS for Apps** på nytt. Du vil bli videresendt til dobbel skriving i Finance.

![Kobling til CDS](./media/12LinktoCDS.png)

4. Velg **Bruk løsning** for å få tilgang til enhetene som skal tilordnes i integrasjonen.

![Bruk løsninger](./media/13ApplySolutions.png)

5. Velg begge løsningene, **Dynamics 365 Finance and Operations Enhetstilordning for dobbel skriving** og **Dynamics 365 Project Operations Enhetstilordning for dobbel skriving**, og velg deretter **Bruk**.

![Bekreft løsninger](./media/14ConfirmSolutions.png)

Når løsningene er tatt i bruk, brukes enhetene for dobbel skriving i miljøet.

![Bruke løsninger](./media/15ApplyingSolutions.png)

Når enhetene er brukt, vises alle tilgjengelige tilordninger i miljøet.

![Tilordninger for dobbel skriving](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Oppdater dataenhetene etter oppdateringen

1. I Finance går du til arbeidsområdet **Dataadministrasjon**.

![Arbeidsområde for dataadministrasjon](./media/16DataManagement.png)

2. Velg flisen **Parametere for rammeverk**.

![Parametere for rammeverk](./media/17FrameworkParameters.png)

3. På siden **Enhetsinnstillinger** velger du **Oppdater enhetsliste**.

![Oppdater enhetsliste](./media/18RefreshEntityList.png)

Oppdateringen tar ca. 20 minutter. Du mottar et varsel når den er fullført.

![Bekreftelse på oppdatering](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Kjøre tilordninger med dobbel skriving for Project Operations

1. I LCS-prosjektet går du til siden **Miljødetaljer**.
2. Under **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps.** Når du har valgt koblingen, blir du omdirigert til listen over enheter i tilordningene.
3. Start tilordningene slik det er beskrevet i tabellen nedenfor. Pass på at du følger rekkefølgen slik den er oppført.

| **Enhetstilordning** | **Oppdater enhet** | **Første synkronisering** | **Hovedoppføring for første synkronisering** | **Forhåndskrav for kjøring** | **Forhåndskrav for innledende synkronisering** |
| --- | --- | --- | --- | --- | --- |
| **Prosjektressursroller for alle selskaper (bookableresourcecategories)** | No | Ja | Common Data Service | No | Ikke tilgjengelig |
| **Juridiske enheter (cdm\_selskaper)** | No | Ja | Finance and Operations-apper | No | Ikke tilgjengelig |
| **Finans (msdyn_ledgers)** | No | Ja | Finance and Operations-apper | Ja | Ja, Finance and Operations-apper |
| **Faktiske verdier for Project Operations-integrering (msdyn\_faktiske verdier)** | No | No | Ikke tilgjengelig | Ja | No |
| **Prosjektkontraktlinjer (salgsordredetaljer)** | No | No | Ikke tilgjengelig | No | No |
| **Integreringsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections)** | No | No | Ikke tilgjengelig | No | Ikke tilgjengelig |
| **Kontraktlinjemilepæler for Project Operations-integrering (msdyn\_contractlinesscheduleofvalues)** | No | No | Ikke tilgjengelig | No | Ikke tilgjengelig |
| **Enhet for utgiftsestimater for Project Operations-integrering (msdyn\_estimateslines)** | No | No | Ikke tilgjengelig | No | Ikke tilgjengelig |
| **Eksportenhet for prosjektutgiftskategorier for Project Operations-integrering (msdyn\_expensecategories)** | No | No | Ikke tilgjengelig | No | Ikke tilgjengelig |
| **Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn\_utgifter)** | Ja | No | Ikke tilgjengelig | No | Ikke tilgjengelig |
| **Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments)** | Ja | No | Ikke tilgjengelig | No | Ikke tilgjengelig |


4. Hvis du vil oppdatere enheten, velger du tilordningsnavnet, og deretter velger du **Oppdater enhteter**. 


![Oppdater tilordning](./media/20RefreshMapping.png)

5. Kjør tilordningen etter at oppdateringen er fullført. Før du aktiverer den neste tilordningen, må du kontrollere at tilordningen i tabellen er tilstanden **Kjører**. Det kan ta litt tid å kjøre tilordninger med et større antall forhånds krav.

Hvis du vil kjøre en tilordning med forhåndskrav, aktiverer du **Vis relaterte enhetstilordninger**. Hvis tabellen angir at **Forhåndskrav for innledende synkronisering** er **Nei**, må du kontrollere at flagget **Innledende synkronisering** er **Av** i alle tilordninger med forhåndskrav før kjøring.

![Kjør tilordning](./media/21RunMap.png)

6. Valider alle prosjektrelaterte tilordninger er i tilstanden Kjører.

![Alle tilordninger kjører](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Bruk konfigurasjonsdata i CDS for Project Operations (valgfritt)

Hvis du har brukt demonstrasjonsdata i Finance-miljøet, kan du se [Konfigurere og bruke konfigurasjonsdata i Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) for å bruke demonstrasjonsdata i CDS-miljø.


Project Operations-miljøet ditt er nå klargjort og konfigurert. 
