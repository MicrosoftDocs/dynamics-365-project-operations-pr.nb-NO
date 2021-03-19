---
title: Konfigurere og bruke konfigurasjonsdata i Common Data Service
description: Dette emnet gir informasjon om hvordan du konfigurerer og bruker konfigurasjonsdata i Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289831"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="7f76a-103">Konfigurere og bruke konfigurasjonsdata i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="7f76a-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="7f76a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="7f76a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="7f76a-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="7f76a-105">Prerequisites</span></span>

<span data-ttu-id="7f76a-106">Før du begynner å konfigurere data i Common Data Service (CDS), må følgende forhåndskrav være oppfylt:</span><span class="sxs-lookup"><span data-stu-id="7f76a-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="7f76a-107">Klargjør et CDS-miljø og et Dynamics 365 Finance-miljø for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="7f76a-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="7f76a-108">Informasjon om juridisk enhet fra Dynamics 365 Finance deles til CDS-miljøet.</span><span class="sxs-lookup"><span data-stu-id="7f76a-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="7f76a-109">Dette betyr at **Firma**-enheten i CDS har følgende firmaoppføringer:</span><span class="sxs-lookup"><span data-stu-id="7f76a-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="7f76a-110">THPM</span><span class="sxs-lookup"><span data-stu-id="7f76a-110">THPM</span></span>
  - <span data-ttu-id="7f76a-111">USPM</span><span class="sxs-lookup"><span data-stu-id="7f76a-111">USPM</span></span>
  - <span data-ttu-id="7f76a-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="7f76a-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="7f76a-113">Installer oppsett og konfigurasjonsdata</span><span class="sxs-lookup"><span data-stu-id="7f76a-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="7f76a-114">Last ned, fjern blokkeringen og pakk ut [pakken med installasjons- og konfigurasjonsdata](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="7f76a-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="7f76a-115">Naviger til den utpakkede mappen, og kjør den kjørbare filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="7f76a-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="7f76a-116">På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="7f76a-118">På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="7f76a-119">Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="7f76a-120">Velg området for leieren din, skriv inn legitimasjonen din, og velg **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="7f76a-122">På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="7f76a-123">På side 4 velger du zip-filen *SampleSetupAndConfigData* fra den utpakkede mappen.</span><span class="sxs-lookup"><span data-stu-id="7f76a-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Valg av zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="7f76a-126">Når du har valgt zip-filen, velger du **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-126">After the zip file is selected, select **Import Data**.</span></span>

![Importdata](./media/5ImportData.png)

10. <span data-ttu-id="7f76a-128">Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten.</span><span class="sxs-lookup"><span data-stu-id="7f76a-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="7f76a-129">Når importen er fullført, avslutter du CMT-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="7f76a-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="7f76a-130">Kontroller organisasjonen for data i følgende 19 enheter:</span><span class="sxs-lookup"><span data-stu-id="7f76a-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="7f76a-131">Valuta</span><span class="sxs-lookup"><span data-stu-id="7f76a-131">Currency</span></span>
  - <span data-ttu-id="7f76a-132">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="7f76a-132">Organizational Unit</span></span>
  - <span data-ttu-id="7f76a-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="7f76a-133">Contact</span></span>
  - <span data-ttu-id="7f76a-134">Avgiftsgruppe</span><span class="sxs-lookup"><span data-stu-id="7f76a-134">Tax Group</span></span>
  - <span data-ttu-id="7f76a-135">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="7f76a-135">Customer Group</span></span>
  - <span data-ttu-id="7f76a-136">Enhet</span><span class="sxs-lookup"><span data-stu-id="7f76a-136">Unit</span></span>
  - <span data-ttu-id="7f76a-137">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="7f76a-137">Unit Group</span></span>
  - <span data-ttu-id="7f76a-138">Prisliste</span><span class="sxs-lookup"><span data-stu-id="7f76a-138">Price List</span></span>
  - <span data-ttu-id="7f76a-139">Prisliste for prosjektparameter</span><span class="sxs-lookup"><span data-stu-id="7f76a-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="7f76a-140">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="7f76a-140">Invoice Frequency</span></span>
  - <span data-ttu-id="7f76a-141">Kategori for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="7f76a-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="7f76a-142">Transaksjonskategori</span><span class="sxs-lookup"><span data-stu-id="7f76a-142">Transaction Category</span></span>
  - <span data-ttu-id="7f76a-143">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="7f76a-143">Expense Category</span></span>
  - <span data-ttu-id="7f76a-144">Rollepris</span><span class="sxs-lookup"><span data-stu-id="7f76a-144">Role Price</span></span>
  - <span data-ttu-id="7f76a-145">Pris for transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="7f76a-145">Transaction Category Price</span></span>
  - <span data-ttu-id="7f76a-146">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="7f76a-146">Characteristic</span></span>
  - <span data-ttu-id="7f76a-147">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="7f76a-147">Bookable Resource</span></span>
  - <span data-ttu-id="7f76a-148">Kategoritilknytning for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="7f76a-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="7f76a-149">Kjennetegn for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="7f76a-149">Bookable Resource Characteristic</span></span>

![Fullført import](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="7f76a-151">Oppdater Project Operations-konfigurasjoner</span><span class="sxs-lookup"><span data-stu-id="7f76a-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="7f76a-152">Naviger til CE-miljøet.</span><span class="sxs-lookup"><span data-stu-id="7f76a-152">Navigate to the CE environment.</span></span> <span data-ttu-id="7f76a-153">Du kan finne det ved å åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.microsoft.com/environments), velge miljøet og deretter velge **Åpne miljø**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Åpne miljø](./media/7OpenEnvironment.png)

2. <span data-ttu-id="7f76a-155">Gå til **Prosjekter** > **Ressurser**, og velg deretter **Ny** for å opprette en bestillbar ressurs for brukeren.</span><span class="sxs-lookup"><span data-stu-id="7f76a-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Ressurser som kan reserveres](./media/8BookableResources.png)

3. <span data-ttu-id="7f76a-157">På **Generelt**-fanen velger du administratorbrukeren.</span><span class="sxs-lookup"><span data-stu-id="7f76a-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="7f76a-158">Kontroller at tidssonen samsvarer med den som du befinner deg i.</span><span class="sxs-lookup"><span data-stu-id="7f76a-158">Verify that the time zone matches the one you are in.</span></span> 

![Ny ressurs som kan reserveres](./media/9NewBookableResource.png)

4. <span data-ttu-id="7f76a-160">På **Planlegging**-fanen i **Firma**-feltet velger du **USPM**-firmaet og deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planlegging-fanen](./media/10SchedulingTab.png)

5. <span data-ttu-id="7f76a-162">Velg **Arbeidstimer**-fanen.</span><span class="sxs-lookup"><span data-stu-id="7f76a-162">Select the **Work hours** tab.</span></span>  

![Arbeidstimer](./media/11WorkHours.png)

6. <span data-ttu-id="7f76a-164">Dobbeltklikk en hvilken som helst verdi i kalenderen, og velg **Rediger** > **Alle hendelser i serien**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Arbeidskalender](./media/12WorkCalendar.png)

7. <span data-ttu-id="7f76a-166">Endre arbeidstimer til en arbeidsdag på åtte (8) timer, merk helger som ikke-arbeidsdager, og sørg for at tidssonen samsvarer med din egen.</span><span class="sxs-lookup"><span data-stu-id="7f76a-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="7f76a-167">Velg **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-167">Select **Save and close**.</span></span>

![Oppdater kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="7f76a-169">Gå til **Innstillinger** > **Kalendermaler**, og velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendermaler](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="7f76a-171">Skriv inn et navn, velg malressursen du opprettet, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Lagre kalendermal](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="7f76a-173">Gå til **Parametere**, og dobbeltklikk oppføringen.</span><span class="sxs-lookup"><span data-stu-id="7f76a-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Prosjektparametere](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="7f76a-175">Oppdater følgende felter:</span><span class="sxs-lookup"><span data-stu-id="7f76a-175">Update the following fields:</span></span>

 - <span data-ttu-id="7f76a-176">**Standardfirma**: USPM</span><span class="sxs-lookup"><span data-stu-id="7f76a-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="7f76a-177">**Standard organisasjonsenhet**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="7f76a-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="7f76a-178">**Fakturafrekvens**: Sjuende og siste dag</span><span class="sxs-lookup"><span data-stu-id="7f76a-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="7f76a-179">**Arbeidstimemal**: Bytt til malen du opprettet.</span><span class="sxs-lookup"><span data-stu-id="7f76a-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="7f76a-180">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7f76a-180">Select **Save**.</span></span> 

![Oppdaterte prosjektparametere](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]