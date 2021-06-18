---
title: Bruke demonstrasjonsoppsett og konfigurasjonsdata – Lite
description: Dette emnet gir informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997163"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="4c6c8-103">Bruke demonstrasjonsoppsett og konfigurasjonsdata for Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="4c6c8-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="4c6c8-104">_\*\*Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4c6c8-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="4c6c8-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="4c6c8-105">Prerequisites</span></span>

<span data-ttu-id="4c6c8-106">Før du begynner å konfigurere, må du ha et Common Data Service (CDS)-miljø klargjort for Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="4c6c8-107">Instruksjoner</span><span class="sxs-lookup"><span data-stu-id="4c6c8-107">Instructions</span></span>

1. <span data-ttu-id="4c6c8-108">Last ned [Master data-pakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="4c6c8-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="4c6c8-109">Naviger til mappen *ProjOpsSampleSetupData - CE only CMT*, og kjør den kjørbare filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="4c6c8-110">På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="4c6c8-112">På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="4c6c8-113">Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="4c6c8-114">Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="4c6c8-116">På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="4c6c8-117">På side 4 velger du ZIP-filen, *SampleSetupAndConfigData* fra mappen som er pakket ut, *ProjOpsSampleSetupData – CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Zip-fil](./media/3ZipFile.png)

   ![Velg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="4c6c8-120">Når du har valgt zip-filen, velger du **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importer data](./media/5ImportData.png)

10. <span data-ttu-id="4c6c8-122">Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="4c6c8-123">Når den er fullført, avslutter du CMT-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="4c6c8-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="4c6c8-124">Kontroller organisasjonen for data i følgende 18 enheter:</span><span class="sxs-lookup"><span data-stu-id="4c6c8-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="4c6c8-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="4c6c8-125">Currency</span></span>
    -   <span data-ttu-id="4c6c8-126">Konto</span><span class="sxs-lookup"><span data-stu-id="4c6c8-126">Account</span></span>
    -   <span data-ttu-id="4c6c8-127">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="4c6c8-127">Organizational Unit</span></span>
    -   <span data-ttu-id="4c6c8-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="4c6c8-128">Contact</span></span>
    -   <span data-ttu-id="4c6c8-129">Enhet</span><span class="sxs-lookup"><span data-stu-id="4c6c8-129">Unit</span></span>
    -   <span data-ttu-id="4c6c8-130">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="4c6c8-130">Unit Group</span></span>
    -   <span data-ttu-id="4c6c8-131">Prisliste</span><span class="sxs-lookup"><span data-stu-id="4c6c8-131">Price List</span></span>
    -   <span data-ttu-id="4c6c8-132">Prisliste for prosjektparameter</span><span class="sxs-lookup"><span data-stu-id="4c6c8-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="4c6c8-133">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="4c6c8-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="4c6c8-134">Kategori for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="4c6c8-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="4c6c8-135">Transaksjonskategori</span><span class="sxs-lookup"><span data-stu-id="4c6c8-135">Transaction Category</span></span>
    -   <span data-ttu-id="4c6c8-136">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="4c6c8-136">Expense Category</span></span>
    -   <span data-ttu-id="4c6c8-137">Rollepris</span><span class="sxs-lookup"><span data-stu-id="4c6c8-137">Role Price</span></span>
    -   <span data-ttu-id="4c6c8-138">Pris for transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="4c6c8-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="4c6c8-139">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="4c6c8-139">Characteristic</span></span>
    -   <span data-ttu-id="4c6c8-140">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="4c6c8-140">Bookable Resource</span></span>
    -   <span data-ttu-id="4c6c8-141">Kategoritilknytning for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="4c6c8-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="4c6c8-142">Kjennetegn for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="4c6c8-142">Bookable Resource Characteristic</span></span>

    ![Fullført import](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
