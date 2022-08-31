---
title: Konfigurere og bruke konfigurasjonsdata i Microsoft Dataverse
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer og bruker konfigurasjonsdata i Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b09d3ea7348082a0467fd7b47918c9e00d1f1e8c
ms.sourcegitcommit: 8edd24201cded2672cec16cd5dc84c6a3516b6c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9230264"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigurere og bruke konfigurasjonsdata i Common Data Service 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_



## <a name="prerequisites"></a>Forutsetning

Før du begynner å konfigurere data i Microsoft Dataverse må følgende forhåndskrav oppfylles:

1.  Klargjør et Dataverse-miljø og et Dynamics 365 Finance-miljø for Project Operations.
2.  Informasjon om juridisk enhet fra Dynamics 365 Finance deles med Dataverse-miljøet. Dette betyr at **Firma**-enheten i Dataverse har følgende firmaoppføringer:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Installer oppsett og konfigurasjonsdata

1. Last ned, fjern blokkeringen og pakk ut [pakken med installasjons- og konfigurasjonsdata](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Naviger til den utpakkede mappen, og kjør den kjørbare filen *DataMigrationUtility*.
3. På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.

![Konfigurasjonsoverføring.](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.
5. Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.
6. Velg området for leieren din, skriv inn legitimasjonen din, og velg **Logg på**.

![Logg på konfigurasjon.](./media/2ConfigurationSignin.png)

7. På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.
8. På side 4 velger du zip-filen *SampleSetupAndConfigData* fra den utpakkede mappen.

![Valg av zip-fil.](./media/3ZipFile.png)

![Velg en fil.](./media/4SelectAFile.png)

9. Når du har valgt zip-filen, velger du **Importer data**.

![Importer data.](./media/5ImportData.png)

10. Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten. Når importen er fullført, avslutter du CMT-veiviseren. 
11. Kontroller organisasjonen for data i følgende 26 enheter:

  - Valuta
  - Plan over kontoer
  - Regnskapskalender
  - Valutakurstyper
  - Betalingsdag
  - Betalingsplan
  - Betalingsbetingelse
  - Organisasjonsenhet
  - Kontakt
  - Avgiftsgruppe
  - Kundegruppe
  - Leverandørgruppe
  - Enhet
  - Enhetsgruppe
  - Prisliste
  - Prisliste for prosjektparameter
  - Fakturafrekvens
  - Kategori for ressurs som kan reserveres
  - Transaksjonskategori
  - Utgiftskategori
  - Rollepris
  - Pris for transaksjonskategorier
  - Kjennetegn
  - Ressurs som kan reserveres
  - Kategoritilknytning for ressurs som kan reserveres
  - Kjennetegn for ressurs som kan reserveres

![Fullført import.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Oppdater Project Operations-konfigurasjoner

1. Naviger til CE-miljøet. Du kan finne det ved å åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), velge miljøet og deretter velge **Åpne miljø**. 

![Åpne miljø.](./media/7OpenEnvironment.png)

2. Gå til **Prosjekter** > **Ressurser**, og velg deretter **Ny** for å opprette en bestillbar ressurs for brukeren.

![Ressurser som kan reserveres.](./media/8BookableResources.png)

3. På **Generelt**-fanen velger du administratorbrukeren. Kontroller at tidssonen samsvarer med den som du befinner deg i. 

![Ny ressurs som kan reserveres.](./media/9NewBookableResource.png)

4. På **Planlegging**-fanen i **Firma**-feltet velger du **USPM**-firmaet og deretter **Lagre**. 

![Planlegging-fanen.](./media/10SchedulingTab.png)

5. Velg **Arbeidstimer**-fanen.  

![Arbeidstimer.](./media/11WorkHours.png)

6. Dobbeltklikk en hvilken som helst verdi i kalenderen, og velg **Rediger** > **Alle hendelser i serien**. 

![Arbeidskalender.](./media/12WorkCalendar.png)

7. Endre arbeidstimer til en arbeidsdag på åtte (8) timer, merk helger som ikke-arbeidsdager, og sørg for at tidssonen samsvarer med din egen. 
8. Velg **Lagre og lukk**.

![Oppdater kalender.](./media/13UpdateCalendar.png)

9. Gå til **Innstillinger** > **Kalendermaler**, og velg **Ny**.
 
 ![Kalendermaler.](./media/14CalendarTemplates.png)
 
 10. Skriv inn et navn, velg malressursen du opprettet, og velg deretter **Lagre**. 
 
 ![Lagre kalendermal.](./media/15SaveCalendarTemplate.png)
 
 11. Gå til **Parametere**, og dobbeltklikk oppføringen. 
 
 ![Prosjektparametere.](./media/16ProjectParameters.png)
 
12. Oppdater følgende felter:

 - **Standardfirma**: USPM
 - **Standard organisasjonsenhet**: Contoso Robotics Global
 - **Fakturafrekvens**: Sjuende og siste dag
 - **Arbeidstimemal**: Bytt til malen du opprettet.

13. Velg **Lagre**. 

![Oppdaterte prosjektparametere.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
