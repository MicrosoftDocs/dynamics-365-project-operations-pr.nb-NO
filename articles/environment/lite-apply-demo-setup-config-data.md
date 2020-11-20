---
title: Bruke demonstrasjonsoppsett og konfigurasjonsdata – Lite
description: Dette emnet gir informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401275"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="78e72-103">Bruke demonstrasjonsoppsett og konfigurasjonsdata for Project Operations – Lite</span><span class="sxs-lookup"><span data-stu-id="78e72-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="78e72-104">_\*\*Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="78e72-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="78e72-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="78e72-105">Prerequisites</span></span>

<span data-ttu-id="78e72-106">Før du begynner å konfigurere, må du ha et Common Data Service (CDS)-miljø klargjort for Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="78e72-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="78e72-107">Instruksjoner</span><span class="sxs-lookup"><span data-stu-id="78e72-107">Instructions</span></span>

1. <span data-ttu-id="78e72-108">Last ned [Master data-pakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="78e72-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="78e72-109">Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integrert CMT*, og kjør den kjørbare filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="78e72-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="78e72-110">På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="78e72-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="78e72-112">På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.</span><span class="sxs-lookup"><span data-stu-id="78e72-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="78e72-113">Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="78e72-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="78e72-114">Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="78e72-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="78e72-116">På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="78e72-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="78e72-117">På side 4 velger du zip-filen *MasterAndSetupData* fra den utpakkede mappen, *ProjOpsDemoDataSetupAndMaster - Integrert CMT*.</span><span class="sxs-lookup"><span data-stu-id="78e72-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="78e72-120">Når du har valgt zip-filen, velger du **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="78e72-120">After the zip file is selected, select **Import Data**.</span></span>

![Importer data](./media/5ImportData.png)

10. <span data-ttu-id="78e72-122">Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten.</span><span class="sxs-lookup"><span data-stu-id="78e72-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="78e72-123">Når den er fullført, avslutter du CMT-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="78e72-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="78e72-124">Kontroller organisasjonen for data i følgende 20 enheter:</span><span class="sxs-lookup"><span data-stu-id="78e72-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="78e72-125">Valuta</span><span class="sxs-lookup"><span data-stu-id="78e72-125">Currency</span></span>
-   <span data-ttu-id="78e72-126">Konto</span><span class="sxs-lookup"><span data-stu-id="78e72-126">Account</span></span>
-   <span data-ttu-id="78e72-127">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="78e72-127">Organizational Unit</span></span>
-   <span data-ttu-id="78e72-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="78e72-128">Contact</span></span>
-   <span data-ttu-id="78e72-129">Avgiftsgruppe</span><span class="sxs-lookup"><span data-stu-id="78e72-129">Tax Group</span></span>
-   <span data-ttu-id="78e72-130">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="78e72-130">Customer Group</span></span>
-   <span data-ttu-id="78e72-131">Enhet</span><span class="sxs-lookup"><span data-stu-id="78e72-131">Unit</span></span>
-   <span data-ttu-id="78e72-132">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="78e72-132">Unit Group</span></span>
-   <span data-ttu-id="78e72-133">Prisliste</span><span class="sxs-lookup"><span data-stu-id="78e72-133">Price List</span></span>
-   <span data-ttu-id="78e72-134">Prisliste for prosjektparameter</span><span class="sxs-lookup"><span data-stu-id="78e72-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="78e72-135">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="78e72-135">Invoice Frequency</span></span>
-   <span data-ttu-id="78e72-136">Kategori for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="78e72-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="78e72-137">Transaksjonskategori</span><span class="sxs-lookup"><span data-stu-id="78e72-137">Transaction Category</span></span>
-   <span data-ttu-id="78e72-138">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="78e72-138">Expense Category</span></span>
-   <span data-ttu-id="78e72-139">Rollepris</span><span class="sxs-lookup"><span data-stu-id="78e72-139">Role Price</span></span>
-   <span data-ttu-id="78e72-140">Pris for transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="78e72-140">Transaction Category Price</span></span>
-   <span data-ttu-id="78e72-141">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="78e72-141">Characteristic</span></span>
-   <span data-ttu-id="78e72-142">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="78e72-142">Bookable Resource</span></span>
-   <span data-ttu-id="78e72-143">Kategoritilknytning for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="78e72-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="78e72-144">Kjennetegn for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="78e72-144">Bookable Resource Characteristic</span></span>

![Fullført import](./media/6CompleteImport.png)
