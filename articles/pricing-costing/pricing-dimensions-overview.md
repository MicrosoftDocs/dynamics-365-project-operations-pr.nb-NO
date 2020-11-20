---
title: Oversikt over prisdimensjoner
description: Dette emnet gir information om prisdimensjonene i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128475"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="f612c-103">Oversikt over prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="f612c-103">Pricing dimensions overview</span></span>

<span data-ttu-id="f612c-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f612c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f612c-105">Dimensjonene som brukes i personalet til å definere priser og kostnader, kan deles inn i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="f612c-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="f612c-106">Personer</span><span class="sxs-lookup"><span data-stu-id="f612c-106">People</span></span>
- <span data-ttu-id="f612c-107">Planlagt arbeid</span><span class="sxs-lookup"><span data-stu-id="f612c-107">Planned work</span></span>

<span data-ttu-id="f612c-108">På grunn av dette er to typer prisdimensjonsverdier tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="f612c-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="f612c-109">**Alternativsett**: Dimensjoner som er faste opplistinger for et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="f612c-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="f612c-110">**Enhetsbaserte verdier**: Dimensjoner som kan være et variert sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="f612c-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="f612c-111">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="f612c-111">Pricing dimensions</span></span>

<span data-ttu-id="f612c-112">Dynamics 365 Project Operations leveres med et standardsett med prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f612c-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="f612c-113">Du kan vise disse prisdimensjonene ved å gå til **Project Operations** > **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="f612c-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="f612c-114">i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f612c-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="f612c-115">Når disse feltene er aktivert, kan du konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="f612c-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="f612c-116">Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f612c-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="f612c-117">Prising av personaltid</span><span class="sxs-lookup"><span data-stu-id="f612c-117">Pricing human resource time</span></span>
<span data-ttu-id="f612c-118">Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="f612c-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="f612c-119">Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.</span><span class="sxs-lookup"><span data-stu-id="f612c-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="f612c-120">Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="f612c-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="f612c-121">Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f612c-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="f612c-122">Vurder om prisdimensjonen skal være en tabell eller et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="f612c-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="f612c-123">Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="f612c-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="f612c-124">Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.</span><span class="sxs-lookup"><span data-stu-id="f612c-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="f612c-125">Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører.</span><span class="sxs-lookup"><span data-stu-id="f612c-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="f612c-126">Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører.</span><span class="sxs-lookup"><span data-stu-id="f612c-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="f612c-127">I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:</span><span class="sxs-lookup"><span data-stu-id="f612c-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="f612c-128">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="f612c-128">**Sample bill rates**</span></span>

| <span data-ttu-id="f612c-129">Rolle</span><span class="sxs-lookup"><span data-stu-id="f612c-129">Role</span></span>        | <span data-ttu-id="f612c-130">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="f612c-130">Org Unit</span></span>    |<span data-ttu-id="f612c-131">Enhet</span><span class="sxs-lookup"><span data-stu-id="f612c-131">Unit</span></span>      |<span data-ttu-id="f612c-132">Pris</span><span class="sxs-lookup"><span data-stu-id="f612c-132">Price</span></span>      |<span data-ttu-id="f612c-133">Valuta</span><span class="sxs-lookup"><span data-stu-id="f612c-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f612c-134">Utvikler</span><span class="sxs-lookup"><span data-stu-id="f612c-134">Developer</span></span>   | <span data-ttu-id="f612c-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f612c-135">Contoso US</span></span>  |<span data-ttu-id="f612c-136">Hour</span><span class="sxs-lookup"><span data-stu-id="f612c-136">Hour</span></span> | <span data-ttu-id="f612c-137">200</span><span class="sxs-lookup"><span data-stu-id="f612c-137">200</span></span>|<span data-ttu-id="f612c-138">USD</span><span class="sxs-lookup"><span data-stu-id="f612c-138">USD</span></span>     |
| <span data-ttu-id="f612c-139">Utvikler</span><span class="sxs-lookup"><span data-stu-id="f612c-139">Developer</span></span>   | <span data-ttu-id="f612c-140">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="f612c-140">Contoso India</span></span> |<span data-ttu-id="f612c-141">Hour</span><span class="sxs-lookup"><span data-stu-id="f612c-141">Hour</span></span>|   <span data-ttu-id="f612c-142">112</span><span class="sxs-lookup"><span data-stu-id="f612c-142">112</span></span>|<span data-ttu-id="f612c-143">USD</span><span class="sxs-lookup"><span data-stu-id="f612c-143">USD</span></span>     |


<span data-ttu-id="f612c-144">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="f612c-144">**Sample cost rates**</span></span>

| <span data-ttu-id="f612c-145">Lønnssats</span><span class="sxs-lookup"><span data-stu-id="f612c-145">Salary Band</span></span>     | <span data-ttu-id="f612c-146">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="f612c-146">Org Unit</span></span>    |<span data-ttu-id="f612c-147">Enhet</span><span class="sxs-lookup"><span data-stu-id="f612c-147">Unit</span></span>      |<span data-ttu-id="f612c-148">Pris</span><span class="sxs-lookup"><span data-stu-id="f612c-148">Price</span></span>      |<span data-ttu-id="f612c-149">Valuta</span><span class="sxs-lookup"><span data-stu-id="f612c-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="f612c-150">Mitt firma_Band1</span><span class="sxs-lookup"><span data-stu-id="f612c-150">My company_Band1</span></span> | <span data-ttu-id="f612c-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f612c-151">Contoso US</span></span>  |<span data-ttu-id="f612c-152">Hour</span><span class="sxs-lookup"><span data-stu-id="f612c-152">Hour</span></span> | <span data-ttu-id="f612c-153">145</span><span class="sxs-lookup"><span data-stu-id="f612c-153">145</span></span>|<span data-ttu-id="f612c-154">USD</span><span class="sxs-lookup"><span data-stu-id="f612c-154">USD</span></span>     |
| <span data-ttu-id="f612c-155">Mitt firma_Band2</span><span class="sxs-lookup"><span data-stu-id="f612c-155">My company_Band2</span></span> | <span data-ttu-id="f612c-156">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="f612c-156">Contoso India</span></span> |<span data-ttu-id="f612c-157">Hour</span><span class="sxs-lookup"><span data-stu-id="f612c-157">Hour</span></span>|   <span data-ttu-id="f612c-158">67</span><span class="sxs-lookup"><span data-stu-id="f612c-158">67</span></span>|<span data-ttu-id="f612c-159">USD</span><span class="sxs-lookup"><span data-stu-id="f612c-159">USD</span></span>     |
