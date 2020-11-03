---
title: Bruk demonstrasjonsoppsett og konfigurasjonsdata
description: Dette emnet gir informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081485"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="07267-103">Bruk demonstrasjonsoppsett og konfigurasjonsdata for Lite-distribusjon i Project Operations – avtale til proformafakturering</span><span class="sxs-lookup"><span data-stu-id="07267-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="07267-104">_\*\*Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="07267-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="07267-105">Last ned [Master data-pakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="07267-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="07267-106">Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integrert CMT* , og kjør den kjørbare filen *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="07267-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="07267-107">På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.</span><span class="sxs-lookup"><span data-stu-id="07267-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="07267-109">På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.</span><span class="sxs-lookup"><span data-stu-id="07267-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="07267-110">Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.</span><span class="sxs-lookup"><span data-stu-id="07267-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="07267-111">Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="07267-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="07267-113">På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="07267-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="07267-114">På side 4 velger du zip-filen *MasterAndSetupData* fra den utpakkede mappen, *ProjOpsDemoDataSetupAndMaster - Integrert CMT*.</span><span class="sxs-lookup"><span data-stu-id="07267-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. <span data-ttu-id="07267-117">Når du har valgt zip-filen, velger du **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="07267-117">After the zip file is selected, select **Import Data**.</span></span>

![Importer data](./media/5ImportData.png)

10. <span data-ttu-id="07267-119">Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten.</span><span class="sxs-lookup"><span data-stu-id="07267-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="07267-120">Når den er fullført, avslutter du CMT-veiviseren.</span><span class="sxs-lookup"><span data-stu-id="07267-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="07267-121">Kontroller organisasjonen for data i følgende 20 enheter:</span><span class="sxs-lookup"><span data-stu-id="07267-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="07267-122">Valuta</span><span class="sxs-lookup"><span data-stu-id="07267-122">Currency</span></span>
- <span data-ttu-id="07267-123">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="07267-123">Organizational Unit</span></span>
- <span data-ttu-id="07267-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="07267-124">Contact</span></span>
- <span data-ttu-id="07267-125">Avgiftsgruppe</span><span class="sxs-lookup"><span data-stu-id="07267-125">Tax Group</span></span>
- <span data-ttu-id="07267-126">Kundegruppe</span><span class="sxs-lookup"><span data-stu-id="07267-126">Customer Group</span></span>
- <span data-ttu-id="07267-127">Enhet</span><span class="sxs-lookup"><span data-stu-id="07267-127">Unit</span></span>
- <span data-ttu-id="07267-128">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="07267-128">Unit Group</span></span>
- <span data-ttu-id="07267-129">Prisliste</span><span class="sxs-lookup"><span data-stu-id="07267-129">Price List</span></span>
- <span data-ttu-id="07267-130">Prisliste for prosjektparameter</span><span class="sxs-lookup"><span data-stu-id="07267-130">Project Parameter Price List</span></span>
- <span data-ttu-id="07267-131">Fakturafrekvens</span><span class="sxs-lookup"><span data-stu-id="07267-131">Invoice Frequency</span></span>
- <span data-ttu-id="07267-132">Fakturafrekvensdetalj</span><span class="sxs-lookup"><span data-stu-id="07267-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="07267-133">Kategori for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="07267-133">Bookable Resource Category</span></span>
- <span data-ttu-id="07267-134">Transaksjonskategori</span><span class="sxs-lookup"><span data-stu-id="07267-134">Transaction Category</span></span>
- <span data-ttu-id="07267-135">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="07267-135">Expense Category</span></span>
- <span data-ttu-id="07267-136">Rollepris</span><span class="sxs-lookup"><span data-stu-id="07267-136">Role Price</span></span>
- <span data-ttu-id="07267-137">Pris for transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="07267-137">Transaction Category Price</span></span>
- <span data-ttu-id="07267-138">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="07267-138">Characteristic</span></span>
- <span data-ttu-id="07267-139">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="07267-139">Bookable Resource</span></span>
- <span data-ttu-id="07267-140">Kategoritilknytning for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="07267-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="07267-141">Kjennetegn for ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="07267-141">Bookable Resource Characteristic</span></span>

![Fullført import](./media/6CompleteImport.png)
