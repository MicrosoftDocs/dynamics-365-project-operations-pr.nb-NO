---
title: Oversikt over prisdimensjoner
description: Dette emnet gir information om prisdimensjonene i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081727"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="8542d-103">Oversikt over prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="8542d-103">Pricing dimensions overview</span></span>

<span data-ttu-id="8542d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="8542d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8542d-105">Dimensjonene som brukes i personalet til å definere priser og kostnader, kan deles inn i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="8542d-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="8542d-106">Personer</span><span class="sxs-lookup"><span data-stu-id="8542d-106">People</span></span>
- <span data-ttu-id="8542d-107">Planlagt arbeid</span><span class="sxs-lookup"><span data-stu-id="8542d-107">Planned work</span></span>

<span data-ttu-id="8542d-108">På grunn av dette er to typer prisdimensjonsverdier tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="8542d-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="8542d-109">**Alternativsett** : Dimensjoner som er faste opplistinger for et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="8542d-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="8542d-110">**Enhetsbaserte verdier** : Dimensjoner som kan være et variert sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="8542d-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="8542d-111">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="8542d-111">Pricing dimensions</span></span>

<span data-ttu-id="8542d-112">Dynamics 365 Project Operations leveres med et standardsett med prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8542d-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="8542d-113">Du kan vise disse prisdimensjonene ved å gå til **Project Operations** > **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="8542d-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="8542d-114">i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8542d-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="8542d-115">Når disse feltene er aktivert, kan du konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="8542d-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="8542d-116">Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8542d-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="8542d-117">Prising av personaltid</span><span class="sxs-lookup"><span data-stu-id="8542d-117">Pricing human resource time</span></span>
<span data-ttu-id="8542d-118">Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="8542d-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="8542d-119">Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.</span><span class="sxs-lookup"><span data-stu-id="8542d-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="8542d-120">Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="8542d-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="8542d-121">Felt som **Transaksjonskategori** ( **msdyn_transactioncategory** ) og **Bestillbar ressurs** ( **bookableresource** ) er eksempler på kandidatdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8542d-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="8542d-122">Vurder om prisdimensjonen skal være en tabell eller et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="8542d-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="8542d-123">Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="8542d-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="8542d-124">Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.</span><span class="sxs-lookup"><span data-stu-id="8542d-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="8542d-125">Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører.</span><span class="sxs-lookup"><span data-stu-id="8542d-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="8542d-126">Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører.</span><span class="sxs-lookup"><span data-stu-id="8542d-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="8542d-127">I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:</span><span class="sxs-lookup"><span data-stu-id="8542d-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="8542d-128">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="8542d-128">**Sample bill rates**</span></span>

| <span data-ttu-id="8542d-129">Rolle</span><span class="sxs-lookup"><span data-stu-id="8542d-129">Role</span></span>        | <span data-ttu-id="8542d-130">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="8542d-130">Org Unit</span></span>    |<span data-ttu-id="8542d-131">Enhet</span><span class="sxs-lookup"><span data-stu-id="8542d-131">Unit</span></span>      |<span data-ttu-id="8542d-132">Pris</span><span class="sxs-lookup"><span data-stu-id="8542d-132">Price</span></span>      |<span data-ttu-id="8542d-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="8542d-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8542d-134">Utvikler</span><span class="sxs-lookup"><span data-stu-id="8542d-134">Developer</span></span>   | <span data-ttu-id="8542d-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8542d-135">Contoso US</span></span>  |<span data-ttu-id="8542d-136">Hour</span><span class="sxs-lookup"><span data-stu-id="8542d-136">Hour</span></span> | <span data-ttu-id="8542d-137">200</span><span class="sxs-lookup"><span data-stu-id="8542d-137">200</span></span>|<span data-ttu-id="8542d-138">USD</span><span class="sxs-lookup"><span data-stu-id="8542d-138">USD</span></span>     |
| <span data-ttu-id="8542d-139">Utvikler</span><span class="sxs-lookup"><span data-stu-id="8542d-139">Developer</span></span>   | <span data-ttu-id="8542d-140">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="8542d-140">Contoso India</span></span> |<span data-ttu-id="8542d-141">Hour</span><span class="sxs-lookup"><span data-stu-id="8542d-141">Hour</span></span>|   <span data-ttu-id="8542d-142">112</span><span class="sxs-lookup"><span data-stu-id="8542d-142">112</span></span>|<span data-ttu-id="8542d-143">USD</span><span class="sxs-lookup"><span data-stu-id="8542d-143">USD</span></span>     |


<span data-ttu-id="8542d-144">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="8542d-144">**Sample cost rates**</span></span>

| <span data-ttu-id="8542d-145">Lønnssats</span><span class="sxs-lookup"><span data-stu-id="8542d-145">Salary Band</span></span>     | <span data-ttu-id="8542d-146">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="8542d-146">Org Unit</span></span>    |<span data-ttu-id="8542d-147">Enhet</span><span class="sxs-lookup"><span data-stu-id="8542d-147">Unit</span></span>      |<span data-ttu-id="8542d-148">Pris</span><span class="sxs-lookup"><span data-stu-id="8542d-148">Price</span></span>      |<span data-ttu-id="8542d-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="8542d-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="8542d-150">Mitt firma_Band1</span><span class="sxs-lookup"><span data-stu-id="8542d-150">My company_Band1</span></span> | <span data-ttu-id="8542d-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="8542d-151">Contoso US</span></span>  |<span data-ttu-id="8542d-152">Hour</span><span class="sxs-lookup"><span data-stu-id="8542d-152">Hour</span></span> | <span data-ttu-id="8542d-153">145</span><span class="sxs-lookup"><span data-stu-id="8542d-153">145</span></span>|<span data-ttu-id="8542d-154">USD</span><span class="sxs-lookup"><span data-stu-id="8542d-154">USD</span></span>     |
| <span data-ttu-id="8542d-155">Mitt firma_Band2</span><span class="sxs-lookup"><span data-stu-id="8542d-155">My company_Band2</span></span> | <span data-ttu-id="8542d-156">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="8542d-156">Contoso India</span></span> |<span data-ttu-id="8542d-157">Hour</span><span class="sxs-lookup"><span data-stu-id="8542d-157">Hour</span></span>|   <span data-ttu-id="8542d-158">67</span><span class="sxs-lookup"><span data-stu-id="8542d-158">67</span></span>|<span data-ttu-id="8542d-159">USD</span><span class="sxs-lookup"><span data-stu-id="8542d-159">USD</span></span>     |
