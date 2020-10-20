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
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="f700d-103">Konfigurer og bruk konfigurasjonsdata i Common Data Service for Project Operations</span><span class="sxs-lookup"><span data-stu-id="f700d-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="f700d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="f700d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="f700d-105">Installer oppsett og konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="f700d-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="f700d-106">Last ned, fjern blokkeringen og pakk ut [pakken med installasjons- og konfigurasjonsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="f700d-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="f700d-107">Naviger til den utpakkede mappen, og kjør den kjørbare filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f700d-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f700d-108">På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="f700d-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f700d-110">På side 2 i CMT-veiviseren velger du **Office 365** som **Distribusjonstype**.</span><span class="sxs-lookup"><span data-stu-id="f700d-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f700d-111">Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="f700d-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f700d-112">Velg området for leieren din, skriv inn legitimasjonen din, og velg **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="f700d-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f700d-114">På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="f700d-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="f700d-115">På side 4 velger du zip-filen *SampleSetupAndConfigData* fra den utpakkede mappen.</span><span class="sxs-lookup"><span data-stu-id="f700d-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Valg av zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="f700d-118">Når du har valgt zip-filen, velger du **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="f700d-118">After the zip file is selected, select **Import Data**.</span></span>

![Importdata](./media/5ImportData.png)

10. <span data-ttu-id="f700d-120">Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten.</span><span class="sxs-lookup"><span data-stu-id="f700d-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f700d-121">Når importen er fullført, avslutter du CMT-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="f700d-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f700d-122">Kontroller organisasjonen for data i følgende 19 enheter:</span><span class="sxs-lookup"><span data-stu-id="f700d-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="f700d-123">Valuta</span><span class="sxs-lookup"><span data-stu-id="f700d-123">Currency</span></span>
  - <span data-ttu-id="f700d-124">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="f700d-124">Organizational Unit</span></span>
  - <span data-ttu-id="f700d-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="f700d-125">Contact</span></span>
  - <span data-ttu-id="f700d-126">Avgiftsgruppe</span><span class="sxs-lookup"><span data-stu-id="f700d-126">Tax Group</span></span>
  - <span data-ttu-id="f700d-127">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="f700d-127">Customer Group</span></span>
  - <span data-ttu-id="f700d-128">Enhet</span><span class="sxs-lookup"><span data-stu-id="f700d-128">Unit</span></span>
  - <span data-ttu-id="f700d-129">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="f700d-129">Unit Group</span></span>
  - <span data-ttu-id="f700d-130">Prisliste</span><span class="sxs-lookup"><span data-stu-id="f700d-130">Price List</span></span>
  - <span data-ttu-id="f700d-131">Prisliste for prosjektparameter</span><span class="sxs-lookup"><span data-stu-id="f700d-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="f700d-132">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="f700d-132">Invoice Frequency</span></span>
  - <span data-ttu-id="f700d-133">Kategori for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="f700d-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="f700d-134">Transaksjonskategori</span><span class="sxs-lookup"><span data-stu-id="f700d-134">Transaction Category</span></span>
  - <span data-ttu-id="f700d-135">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="f700d-135">Expense Category</span></span>
  - <span data-ttu-id="f700d-136">Rollepris</span><span class="sxs-lookup"><span data-stu-id="f700d-136">Role Price</span></span>
  - <span data-ttu-id="f700d-137">Pris for transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="f700d-137">Transaction Category Price</span></span>
  - <span data-ttu-id="f700d-138">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="f700d-138">Characteristic</span></span>
  - <span data-ttu-id="f700d-139">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="f700d-139">Bookable Resource</span></span>
  - <span data-ttu-id="f700d-140">Kategoritilknytning for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="f700d-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="f700d-141">Kjennetegn for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="f700d-141">Bookable Resource Characteristic</span></span>

![Fullført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="f700d-143">Oppdater Project Operations-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="f700d-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="f700d-144">Naviger til CE-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f700d-144">Navigate to the CE environment.</span></span> <span data-ttu-id="f700d-145">Du kan finne det ved å åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), velge miljøet og deretter velge **Åpne miljø**.</span><span class="sxs-lookup"><span data-stu-id="f700d-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Åpne miljø](./media/7OpenEnvironment.png)

2. <span data-ttu-id="f700d-147">Gå til **Prosjekter** > **Ressurser**, og velg deretter **Ny** for å opprette en bestillbar ressurs for brukeren.</span><span class="sxs-lookup"><span data-stu-id="f700d-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ressurser som kan reserveres](./media/8BookableResources.png)

3. <span data-ttu-id="f700d-149">På **Generelt**-fanen velger du administratorbrukeren.</span><span class="sxs-lookup"><span data-stu-id="f700d-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="f700d-150">Kontroller at tidssonen samsvarer med den som du befinner deg i.</span><span class="sxs-lookup"><span data-stu-id="f700d-150">Verify that the time zone matches the one you are in.</span></span> 

![Ny ressurs som kan reserveres](./media/9NewBookableResource.png)

4. <span data-ttu-id="f700d-152">På **Planlegging**-fanen i **Firma**-feltet velger du **USPM**-firmaet og deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f700d-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planlegging-fanen](./media/10SchedulingTab.png)

5. <span data-ttu-id="f700d-154">Velg **Arbeidstimer**-fanen.</span><span class="sxs-lookup"><span data-stu-id="f700d-154">Select the **Work hours** tab.</span></span>  

![Arbeidstimer](./media/11WorkHours.png)

6. <span data-ttu-id="f700d-156">Dobbeltklikk en hvilken som helst verdi i kalenderen, og velg **Rediger** > **Alle hendelser i serien**.</span><span class="sxs-lookup"><span data-stu-id="f700d-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbeidskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="f700d-158">Endre arbeidstimer til en arbeidsdag på åtte (8) timer, merk helger som ikke-arbeidsdager, og sørg for at tidssonen samsvarer med din egen.</span><span class="sxs-lookup"><span data-stu-id="f700d-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="f700d-159">Velg **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="f700d-159">Select **Save and close**.</span></span>

![Oppdater kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="f700d-161">Gå til **Innstillinger** > **Kalendermaler**, og velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f700d-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendermaler](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="f700d-163">Skriv inn et navn, velg malressursen du opprettet, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f700d-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Lagre kalendermal](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="f700d-165">Gå til **Parametere**, og dobbeltklikk oppføringen.</span><span class="sxs-lookup"><span data-stu-id="f700d-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Prosjektparametere](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="f700d-167">Oppdater følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f700d-167">Update the following fields:</span></span>

 - <span data-ttu-id="f700d-168">**Standardfirma**: USPM</span><span class="sxs-lookup"><span data-stu-id="f700d-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="f700d-169">**Standard organisasjonsenhet**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="f700d-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="f700d-170">**Fakturafrekvens**: Sjuende og siste dag</span><span class="sxs-lookup"><span data-stu-id="f700d-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="f700d-171">**Arbeidstimemal**: Bytt til malen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="f700d-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="f700d-172">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f700d-172">Select **Save**.</span></span> 

![Oppdaterte prosjektparametere](./media/17UpdatedProjectParameters.png)
