---
title: Økonomiske estimater for materialer på prosjekter
description: Dette emnet inneholder informasjon om hvordan du definerer eller beregner prosjektbasert materiell.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788881"
---
# <a name="financial-estimates-for-materials-on-projects"></a><span data-ttu-id="17590-103">Økonomiske estimater for materialer på prosjekter</span><span class="sxs-lookup"><span data-stu-id="17590-103">Financial estimates for materials on projects</span></span>

<span data-ttu-id="17590-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="17590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17590-105">Dynamics 365 Project Operations gjør det mulig for prosjektledere å definere prosjektbaserte materialekostnader for hvert prosjekt eller hver oppgave.</span><span class="sxs-lookup"><span data-stu-id="17590-105">Dynamics 365 Project Operations allows Project managers to define project-based material costs for each project or task.</span></span> <span data-ttu-id="17590-106">Hvert materialestimat kan knyttes til en bestemt prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="17590-106">Each material estimate can be associated with a specific project task.</span></span> <span data-ttu-id="17590-107">Utgifter kategoriseres i ulike utgiftskategorier, som defineres på organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="17590-107">Expenses are categorized into different expense categories, which are defined at the organizational level.</span></span> <span data-ttu-id="17590-108">Priser og kostnader for hver utgiftskategori defineres i prislisten.</span><span class="sxs-lookup"><span data-stu-id="17590-108">Pricing and costing for each expense category is defined in the price list.</span></span> 

<span data-ttu-id="17590-109">Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette et estimat for prosjektmateriell.</span><span class="sxs-lookup"><span data-stu-id="17590-109">Complete the following steps to view, add, or delete a project material estimate.</span></span>

1. <span data-ttu-id="17590-110">Gå til **Prosjekter**, og velg prosjektet du vil oppdatere.</span><span class="sxs-lookup"><span data-stu-id="17590-110">Go to **Projects**, and select the project you want to update.</span></span>
2. <span data-ttu-id="17590-111">I kategorien **Materialestimater** viser du listen over prosjektmaterialestimater.</span><span class="sxs-lookup"><span data-stu-id="17590-111">On the **Material Estimates** tab, view the list of project material estimates.</span></span>
3. <span data-ttu-id="17590-112">Velg **Nytt materialestimat** for å opprette et nytt materialestimat.</span><span class="sxs-lookup"><span data-stu-id="17590-112">Select **New Material estimate** to create a new material estimate.</span></span> <span data-ttu-id="17590-113">Du kan også velge et materialestimat som skal slettes, og deretter velge **Slett materialestimat**.</span><span class="sxs-lookup"><span data-stu-id="17590-113">Or, select a material estimate to delete, and then select **Delete Material Estimate**.</span></span>

<span data-ttu-id="17590-114">Tabellen nedenfor inneholder informasjon om feltene på **materialestimatlinjen** for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17590-114">The following table provides information about the fields on the **Material Estimate line** on a project.</span></span> 

| <span data-ttu-id="17590-115">**Felt**</span><span class="sxs-lookup"><span data-stu-id="17590-115">**Field**</span></span> | <span data-ttu-id="17590-116">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="17590-116">**Description**</span></span> | <span data-ttu-id="17590-117">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="17590-117">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="17590-118">Oppgave</span><span class="sxs-lookup"><span data-stu-id="17590-118">Task</span></span> | <span data-ttu-id="17590-119">En liste over oppgavene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-119">A list of tasks in the project.</span></span> <span data-ttu-id="17590-120">Dette inkluderer sammendrags- og bladnodeoppgaver.</span><span class="sxs-lookup"><span data-stu-id="17590-120">This includes summary and leaf node tasks.</span></span> | <span data-ttu-id="17590-121">Når du velger en oppgave for en materialestimatlinje, påvirkes den estimerte materialkostnaden og det estimert materialsalget for en oppgave.</span><span class="sxs-lookup"><span data-stu-id="17590-121">When you select a task for a material estimate line, the estimated material cost and estimated material sales for a task are impacted.</span></span> <span data-ttu-id="17590-122">Hvis dette feltet står tomt, spores materialestimatet og oppsummeres bare på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="17590-122">If this field is empty, the material estimate is tracked and summarized only at the project level.</span></span> |
| <span data-ttu-id="17590-123">Velg produkt</span><span class="sxs-lookup"><span data-stu-id="17590-123">Select Product</span></span> |  <span data-ttu-id="17590-124">Du kan angi om estimatlinjen gjelder et eksisterende produkt (i produktkatalogen) eller et produkt som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="17590-124">You can specify whether the estimate line is for an existing (catalog) or write-in product.</span></span> | <span data-ttu-id="17590-125">Dette feltet avgjør om du velger et produkt fra katalogen eller et produkt som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="17590-125">This field determines if you select a product from the catalog or a write in product.</span></span> |
| <span data-ttu-id="17590-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="17590-126">Product</span></span> | <span data-ttu-id="17590-127">ID-en for produktet fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="17590-127">The ID of the product from the product catalog.</span></span> <span data-ttu-id="17590-128">Når du velger en produkt-ID, oppdateres verdien i feltet **Velg produkt** automatisk til **Eksisterende produkt**.</span><span class="sxs-lookup"><span data-stu-id="17590-128">When you select a product ID, the value in the **Select Product** field is automatically updated to **Existing product**.</span></span> <span data-ttu-id="17590-129">ID-en brukes til å hente kost- og salgsprisene fra prislisten.</span><span class="sxs-lookup"><span data-stu-id="17590-129">The ID is used to retrieve the cost and sales prices from the price list.</span></span> | <span data-ttu-id="17590-130">Dette feltet har ingen nedstrøms påvirkning.</span><span class="sxs-lookup"><span data-stu-id="17590-130">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="17590-131">Beskrivelse av produkt ikke i produktkatalog</span><span class="sxs-lookup"><span data-stu-id="17590-131">Write In Product Description</span></span> | <span data-ttu-id="17590-132">Et tekstfelt for å skrive inn navnet på produktet.</span><span class="sxs-lookup"><span data-stu-id="17590-132">A text field to write in the name of the product.</span></span> <span data-ttu-id="17590-133">Dette feltet skal brukes når **Ikke i produktkatalog** er valgt i **Velg produkt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="17590-133">This field should be used when **Write In** is selected in the **Select Product** field.</span></span>| <span data-ttu-id="17590-134">Dette feltet har ingen nedstrøms påvirkning.</span><span class="sxs-lookup"><span data-stu-id="17590-134">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="17590-135">Startdato</span><span class="sxs-lookup"><span data-stu-id="17590-135">Start date</span></span> | <span data-ttu-id="17590-136">Den forventede datoen for bruk av materialet.</span><span class="sxs-lookup"><span data-stu-id="17590-136">The forecasted date on which the material is expected to be used.</span></span> | <span data-ttu-id="17590-137">Dette feltet har ingen nedstrøms påvirkning.</span><span class="sxs-lookup"><span data-stu-id="17590-137">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="17590-138">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="17590-138">Unit group</span></span> | <span data-ttu-id="17590-139">Standardverdien i dette feltet kommer fra standard enhetsgruppe for katalogproduktet.</span><span class="sxs-lookup"><span data-stu-id="17590-139">The default value in this field comes from the default unit group on the catalog product.</span></span> <span data-ttu-id="17590-140">Du kan oppdatere dette feltet for å velge en annen enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="17590-140">You can update this field to select another unit group.</span></span> | <span data-ttu-id="17590-141">Dette feltet har ingen nedstrøms påvirkning.</span><span class="sxs-lookup"><span data-stu-id="17590-141">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="17590-142">Enhet</span><span class="sxs-lookup"><span data-stu-id="17590-142">Unit</span></span> | <span data-ttu-id="17590-143">Verdien i dette feltet kommer fra standardenheten for det valgte produktet.</span><span class="sxs-lookup"><span data-stu-id="17590-143">The value in this field comes from the default unit of the selected product.</span></span> <span data-ttu-id="17590-144">Du kan oppdatere dette feltet for å velge en annen enhet.</span><span class="sxs-lookup"><span data-stu-id="17590-144">You can update this field to select another unit.</span></span> | <span data-ttu-id="17590-145">Endring av enheten fører til en annen standard enhetspris og -kostnad.</span><span class="sxs-lookup"><span data-stu-id="17590-145">Changing the unit results in a different default unit price and cost.</span></span> |
| <span data-ttu-id="17590-146">Antall</span><span class="sxs-lookup"><span data-stu-id="17590-146">Quantity</span></span> | <span data-ttu-id="17590-147">Det estimerte antallet av produktet som skal brukes på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-147">The estimated quantity of the product that will be used on the project.</span></span> | <span data-ttu-id="17590-148">Dette feltet har ingen nedstrøms påvirkning.</span><span class="sxs-lookup"><span data-stu-id="17590-148">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="17590-149">Enhetskost</span><span class="sxs-lookup"><span data-stu-id="17590-149">Unit Cost</span></span> | <span data-ttu-id="17590-150">Enhetskostnaden for det valgte produktet og enhetskombinasjonen som angitt i den aktuelle kostnadsprislisten.</span><span class="sxs-lookup"><span data-stu-id="17590-150">The unit cost of the selected product and unit combination as set up in the applicable cost price list.</span></span> | <span data-ttu-id="17590-151">Enhetskostnaden vises alltid i kostnadsvalutaen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-151">The unit cost is always shown in the project's cost currency.</span></span> <span data-ttu-id="17590-152">Hvis det ikke er definert noen enhetskostnad for kombinasjonen av produktet og enhetsoppsettet i prislisten, settes enhetskostnaden til 0,00 som standard.</span><span class="sxs-lookup"><span data-stu-id="17590-152">If there is no set up of unit cost for the combination of the product and unit setup in the price list, the unit cost will default to 0.00.</span></span> |
| <span data-ttu-id="17590-153">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="17590-153">Unit Price</span></span> | <span data-ttu-id="17590-154">Prisen for det valgte produktet og enhetskombinasjonen som satt opp i den aktuelle salgsprislisten.</span><span class="sxs-lookup"><span data-stu-id="17590-154">The price of the selected product and unit combination as set up in the applicable sales price list.</span></span> | <span data-ttu-id="17590-155">Enhetsprisen vises alltid i salgsvalutaen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-155">The unit price is always shown in the project's sales currency.</span></span> <span data-ttu-id="17590-156">Hvis det ikke er satt opp en enhetspris for kombinasjonen av produktet og enhetsoppsettet i prislisten, settes enhetsprisen til 0,00 som standard.</span><span class="sxs-lookup"><span data-stu-id="17590-156">If there is no setup of unit price  for the combination of the product and unit setup in the price list, then unit price will default to 0.00.</span></span>|
| <span data-ttu-id="17590-157">Totale kostnader</span><span class="sxs-lookup"><span data-stu-id="17590-157">Total Cost</span></span> | <span data-ttu-id="17590-158">Kostnadsbeløpet som beregnes som antall \* enhetskostnad.</span><span class="sxs-lookup"><span data-stu-id="17590-158">The cost amount that is calculated as quantity \* unit cost.</span></span>| <span data-ttu-id="17590-159">Kostnadsbeløpet vises alltid i kostnadsvalutaen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-159">The cost amount is always shown in the project's cost currency.</span></span> |
| <span data-ttu-id="17590-160">Totalt salg</span><span class="sxs-lookup"><span data-stu-id="17590-160">Total Sales</span></span> | <span data-ttu-id="17590-161">Salgsbeløpet som beregnes som antall \* enhetspris.</span><span class="sxs-lookup"><span data-stu-id="17590-161">The sales amount that is calculated as quantity \* unit price.</span></span> | <span data-ttu-id="17590-162">Salgsbeløpet vises alltid i salgsvalutaen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="17590-162">The sales amount is always shown in the project's sales currency.</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]