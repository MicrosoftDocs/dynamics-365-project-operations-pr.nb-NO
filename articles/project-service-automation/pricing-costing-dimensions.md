---
title: Hjemmeside for pris- og kostnadsdimensjoner
description: Dette emnet gir en oversikt over prisdimensjoner.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754097"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="e36de-103">Hjemmeside for pris- og kostnadsdimensjoner</span><span class="sxs-lookup"><span data-stu-id="e36de-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="e36de-104">Dimensjonene som brukes i personalet til å definere priser og kostnader, kan deles inn i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="e36de-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="e36de-105">Personer</span><span class="sxs-lookup"><span data-stu-id="e36de-105">People</span></span>
- <span data-ttu-id="e36de-106">Planlagt arbeid</span><span class="sxs-lookup"><span data-stu-id="e36de-106">Planned work</span></span>

<span data-ttu-id="e36de-107">På grunn av dette er to typer prisdimensjonsverdier tilgjengelige i PSA (Project Service Automation):</span><span class="sxs-lookup"><span data-stu-id="e36de-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="e36de-108">**Alternativsett** – dimensjoner som er faste opplistinger for et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="e36de-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e36de-109">**Enhetsbaserte verdier** – dimensjoner som kan være et variert sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="e36de-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e36de-110">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="e36de-110">Pricing dimensions</span></span>

<span data-ttu-id="e36de-111">PSA leveres med et standardsett med prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e36de-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e36de-112">Du kan vise disse ved å gå til **Project Service** > **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="e36de-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="e36de-113">i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e36de-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e36de-114">Dette gjør det mulig å konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="e36de-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skjermbilde av Project Service-parametere med "Gjelder salg" uthevet](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="e36de-116">Hvis du har brukt de medfølgende feltene for rolle og organisasjonsenhet som prisdimensjoner før versjon 3 av PSA, vil det ikke være noen observerbar endring.</span><span class="sxs-lookup"><span data-stu-id="e36de-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="e36de-117">Du kan fortsette å bruke Project Service på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="e36de-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="e36de-118">Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e36de-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="e36de-119">Hvis du vil ha mer informasjon, kan du se følgende emner, men vær oppmerksom på at du må fullføre prosedyrene i rekkefølgen angitt nedenfor:</span><span class="sxs-lookup"><span data-stu-id="e36de-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="e36de-120">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="e36de-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="e36de-121">Legge til egendefinerte felt i prisoppsett og transaksjonsenheter</span><span class="sxs-lookup"><span data-stu-id="e36de-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="e36de-122">Konfigurere egendefinerte felt som prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="e36de-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="e36de-123">Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="e36de-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e36de-124">Prising av personaltid</span><span class="sxs-lookup"><span data-stu-id="e36de-124">Pricing human resource time</span></span>
<span data-ttu-id="e36de-125">Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="e36de-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e36de-126">Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.</span><span class="sxs-lookup"><span data-stu-id="e36de-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e36de-127">Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="e36de-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e36de-128">Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="e36de-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e36de-129">Du bør også vurdere om prisdimensjonen skal være en tabell eller et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="e36de-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e36de-130">Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="e36de-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="e36de-131">Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.</span><span class="sxs-lookup"><span data-stu-id="e36de-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="e36de-132">Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører.</span><span class="sxs-lookup"><span data-stu-id="e36de-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e36de-133">Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører.</span><span class="sxs-lookup"><span data-stu-id="e36de-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e36de-134">I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:</span><span class="sxs-lookup"><span data-stu-id="e36de-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e36de-135">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="e36de-135">**Sample bill rates**</span></span>

| <span data-ttu-id="e36de-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="e36de-136">Role</span></span>        | <span data-ttu-id="e36de-137">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="e36de-137">Org Unit</span></span>    |<span data-ttu-id="e36de-138">Enhet</span><span class="sxs-lookup"><span data-stu-id="e36de-138">Unit</span></span>      |<span data-ttu-id="e36de-139">Pris</span><span class="sxs-lookup"><span data-stu-id="e36de-139">Price</span></span>      |<span data-ttu-id="e36de-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="e36de-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e36de-141">Utvikler</span><span class="sxs-lookup"><span data-stu-id="e36de-141">Developer</span></span>   | <span data-ttu-id="e36de-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e36de-142">Contoso US</span></span>  |<span data-ttu-id="e36de-143">Hour</span><span class="sxs-lookup"><span data-stu-id="e36de-143">Hour</span></span> | <span data-ttu-id="e36de-144">200</span><span class="sxs-lookup"><span data-stu-id="e36de-144">200</span></span>|<span data-ttu-id="e36de-145">USD</span><span class="sxs-lookup"><span data-stu-id="e36de-145">USD</span></span>     |
| <span data-ttu-id="e36de-146">Utvikler</span><span class="sxs-lookup"><span data-stu-id="e36de-146">Developer</span></span>   | <span data-ttu-id="e36de-147">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="e36de-147">Contoso India</span></span> |<span data-ttu-id="e36de-148">Hour</span><span class="sxs-lookup"><span data-stu-id="e36de-148">Hour</span></span>|   <span data-ttu-id="e36de-149">112</span><span class="sxs-lookup"><span data-stu-id="e36de-149">112</span></span>|<span data-ttu-id="e36de-150">USD</span><span class="sxs-lookup"><span data-stu-id="e36de-150">USD</span></span>     |


<span data-ttu-id="e36de-151">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="e36de-151">**Sample cost rates**</span></span>

| <span data-ttu-id="e36de-152">Lønnssats</span><span class="sxs-lookup"><span data-stu-id="e36de-152">Salary Band</span></span>     | <span data-ttu-id="e36de-153">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="e36de-153">Org Unit</span></span>    |<span data-ttu-id="e36de-154">Enhet</span><span class="sxs-lookup"><span data-stu-id="e36de-154">Unit</span></span>      |<span data-ttu-id="e36de-155">Pris</span><span class="sxs-lookup"><span data-stu-id="e36de-155">Price</span></span>      |<span data-ttu-id="e36de-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="e36de-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e36de-157">Mitt firma_Band1</span><span class="sxs-lookup"><span data-stu-id="e36de-157">My company_Band1</span></span> | <span data-ttu-id="e36de-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="e36de-158">Contoso US</span></span>  |<span data-ttu-id="e36de-159">Hour</span><span class="sxs-lookup"><span data-stu-id="e36de-159">Hour</span></span> | <span data-ttu-id="e36de-160">145</span><span class="sxs-lookup"><span data-stu-id="e36de-160">145</span></span>|<span data-ttu-id="e36de-161">USD</span><span class="sxs-lookup"><span data-stu-id="e36de-161">USD</span></span>     |
| <span data-ttu-id="e36de-162">Mitt firma_Band2</span><span class="sxs-lookup"><span data-stu-id="e36de-162">My company_Band2</span></span> | <span data-ttu-id="e36de-163">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="e36de-163">Contoso India</span></span> |<span data-ttu-id="e36de-164">Hour</span><span class="sxs-lookup"><span data-stu-id="e36de-164">Hour</span></span>|   <span data-ttu-id="e36de-165">67</span><span class="sxs-lookup"><span data-stu-id="e36de-165">67</span></span>|<span data-ttu-id="e36de-166">USD</span><span class="sxs-lookup"><span data-stu-id="e36de-166">USD</span></span>     |
