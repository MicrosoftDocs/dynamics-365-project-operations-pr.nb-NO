---
title: Bruke demodata i et skybasert Finance-miljø
description: Dette emnet forklarer hvordan du bruker demonstrasjonsdata fra Project Operations i et skydriftet Dynamics 365 Finance-miljø.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c04aab6ffb332a3095ca2a7890deb73f15a8b5e3713021c60eec02eb13dbd0cb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009678"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Bruke demodata i et skybasert Finance-miljø

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

> [!IMPORTANT]
> Dette emnet bare gjelder bare for Microsoft Dynamics 365 Finance versjon 10.0.13, og kan bare utføres i et skybasert miljø. Fullfør trinnene i dette emnet **FØR** du bruker kvalitetsoppdateringer i miljøet.

1. I LCS-prosjektet åpner du siden **Miljødetaljer**. Legg merke til at den inneholder detaljene som kreves for å koble til miljøet ved hjelp av RDP (Remote Desktop Protocol).

![Miljødetaljer.](./media/1EnvironmentDetails.png)

Det første settet med uthevede legitimasjoner er legitimasjonen for den lokale forretningsforbindelsen og inneholder en hyperkobling til tilkoblingen til eksternt skrivebord. Legitimasjonen inkluderer brukernavn og passord for miljøadministratoren. Det andre settet med legitimasjon brukes til å logge på SQL Server i dette miljøet.

2. Koble til miljøet ved hjelp av hyperkoblingen i **Lokale forretningsforbindelser**, og bruk **legitimasjonen for den lokale forretningsforbindelsen** til å godkjenne.
3. Gå til **Internet Information Services** > **Applikasjonsutvalg** > **AOSService**, og stopp tjenesten. Du stopper tjenesten på dette tidspunktet, slik at du kan fortsette å erstatte SQL-databasen.

![Stopp AOS.](./media/2StopAOS.png)

4. Gå til **Tjenester**, og stopp følgende to elementer:

- Microsoft Dynamics 365 Unified Operations: Tjenesten for partiadministrasjon
- Microsoft Dynamics 365 Unified Operations: Rammeverket for import/eksport av data

![Stopp tjenester.](./media/3StopServices.png)

5. Åpne Microsoft SQL Server Management Studio. Logg på med legitimasjonen for SQL-serveren, og bruk axdbadmin-brukeren og passordet fra LCS-siden **Miljødetaljer**.

![SQL Server Management Studio.](./media/4SSMS.png)

6. I Object Explorer velger du **Databaser**, og finn **AXDB**. Du skal erstatte databasen med en ny database som er plassert i [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Kopier zip-filen til den virtuelle maskinen du er koblet eksternt til, og pakk ut zip-innholdet.
8. I SQL Server Management Studio høyreklikker du på **AxDB**, og deretter velger du **Oppgaver** > **Gjenopprett** > **Database**.

![Gjenopprett database.](./media/5RestoreDatabase.png)

9. Velg **Kildeenhet**, og naviger til filen som ble pakket ut fra zip-filen du kopierte.

![Kildeenheter.](./media/6SourceDevice.png)

10. Velg **Alternativer**, og velg deretter **Overskriv den eksisterende databasen** og **Lukk eksisterende tilkoblinger til måldatabase**. 
11. Velg **OK**.

![Gjenopprett innstillinger.](./media/7RestoreSetting.png)

Du vil motta en bekreftelse på at AXDB-gjenopprettingen var vellykket. Når du har mottatt denne bekreftelsen, kan du lukke SQL Services Management Studio.

12. Gå tilbake til **Internet Information Services** > **Applikasjonsutvalg** > **AOSService**, og start AOSService.
13. Gå til **Tjenester**, og start de to tjenestene du stoppet tidligere.

14. Finn AdminUserProvisioning-verktøyet på denne virtuelle maskinen. Se under K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Kjør .ext-filen ved å bruke brukeradressen din i feltet **E-postadresse**. 
16. Velg **Send inn**.

![Klargjøring av administratorbruker.](./media/8AdminUserProvisioning.png)

Dette tar noen minutter å fullføre. Du skal få en bekreftelsesmelding om at administratorbrukeren er oppdatert.

17. Til slutt kjører du ledeteksten som administrator og utfører iisreset

![IIS-tilbakestilling.](./media/9IISReset.png)

18. Lukk den eksterne skrivebordsøkten, og bruk LCS-siden **Miljødetaljer** til å logge deg på miljøet for å bekrefte at det fungerer som forventet.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]