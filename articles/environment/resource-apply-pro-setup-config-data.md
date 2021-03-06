---
title: Konfigurer og bruk konfigurasjonsdata i Common Data Service for Project Operations
description: Dette emnet gir informasjon om hvordan du konfigurerer og bruker konfigurasjonsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949000"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a>Konfigurer og bruk konfigurasjonsdata i Common Data Service for Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

## <a name="install-setup-and-configuration-data"></a>Installer oppsett og konfigurasjonsdata

1. Last ned, fjern blokkeringen og pakk ut [pakken med installasjons- og konfigurasjonsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Naviger til den utpakkede mappen, og kjør den kjørbare filen *DataMigrationUtility*.
3. På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-veiviseren velger du **Office 365** som **Distribusjonstype**.
5. Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.
6. Velg området for leieren din, skriv inn legitimasjonen din, og velg **Logg på**.

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.
8. På side 4 velger du zip-filen *SampleSetupAndConfigData* fra den utpakkede mappen.

![Valg av zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. Når du har valgt zip-filen, velger du **Importer data**.

![Importdata](./media/5ImportData.png)

10. Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten. Når importen er fullført, avslutter du CMT-veiviseren. 
11. Kontroller organisasjonen for data i følgende 19 enheter:

  - Valuta
  - Organisasjonsenhet
  - Kontakt
  - Avgiftsgruppe
  - Kundegruppe
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

![Fullført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Oppdater Project Operations-konfigurasjoner

1. Naviger til CE-miljøet. Du kan finne det ved å åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), velge miljøet og deretter velge **Åpne miljø**. 

![Åpne miljø](./media/7OpenEnvironment.png)

2. Gå til **Prosjekter** > **Ressurser**, og velg deretter **Ny** for å opprette en bestillbar ressurs for brukeren.

![Ressurser som kan reserveres](./media/8BookableResources.png)

3. På **Generelt**-fanen velger du administratorbrukeren. Kontroller at tidssonen samsvarer med den som du befinner deg i. 

![Ny ressurs som kan reserveres](./media/9NewBookableResource.png)

4. På **Planlegging**-fanen i **Firma**-feltet velger du **USPM**-firmaet og deretter **Lagre**. 

![Planlegging-fanen](./media/10SchedulingTab.png)

5. Velg **Arbeidstimer**-fanen.  

![Arbeidstimer](./media/11WorkHours.png)

6. Dobbeltklikk en hvilken som helst verdi i kalenderen, og velg **Rediger** > **Alle hendelser i serien**. 

![Arbeidskalender](./media/12WorkCalendar.png)

7. Endre arbeidstimer til en arbeidsdag på åtte (8) timer, merk helger som ikke-arbeidsdager, og sørg for at tidssonen samsvarer med din egen. 
8. Velg **Lagre og lukk**.

![Oppdater kalender](./media/13UpdateCalendar.png)

9. Gå til **Innstillinger** > **Kalendermaler**, og velg **Ny**.
 
 ![Kalendermaler](./media/14CalendarTemplates.png)
 
 10. Skriv inn et navn, velg malressursen du opprettet, og velg deretter **Lagre**. 
 
 ![Lagre kalendermal](./media/15SaveCalendarTemplate.png)
 
 11. Gå til **Parametere**, og dobbeltklikk oppføringen. 
 
 ![Prosjektparametere](./media/16ProjectParameters.png)
 
12. Oppdater følgende felter:

 - **Standardfirma**: USPM
 - **Standard organisasjonsenhet**: Contoso Robotics Global
 - **Fakturafrekvens**: Sjuende og siste dag
 - **Arbeidstimemal**: Bytt til malen du opprettet.

13. Velg **Lagre**. 

![Oppdaterte prosjektparametere](./media/17UpdatedProjectParameters.png)
