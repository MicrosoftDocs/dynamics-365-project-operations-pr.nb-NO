---
title: Oversikt over prisdimensjoner
description: Dette emnet gir informasjon om prisdimensjonene i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650215"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="1465d-103">Oversikt over prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1465d-103">Pricing dimensions overview</span></span>

<span data-ttu-id="1465d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="1465d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1465d-105">Dimensjonene som brukes i personalet til å definere priser og kostnader, kan deles inn i to kategorier:</span><span class="sxs-lookup"><span data-stu-id="1465d-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="1465d-106">Personer</span><span class="sxs-lookup"><span data-stu-id="1465d-106">People</span></span>
- <span data-ttu-id="1465d-107">Planlagt arbeid</span><span class="sxs-lookup"><span data-stu-id="1465d-107">Planned work</span></span>

<span data-ttu-id="1465d-108">På grunn av dette er to typer prisdimensjonsverdier tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="1465d-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="1465d-109">**Alternativsett**: Dimensjoner som er faste opplistinger for et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="1465d-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1465d-110">**Enhetsbaserte verdier**: Dimensjoner som kan være et variert sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="1465d-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1465d-111">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1465d-111">Pricing dimensions</span></span>

<span data-ttu-id="1465d-112">Dynamics 365 Project Operations leveres med et standardsett med prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1465d-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1465d-113">Du kan vise disse prisdimensjonene ved å gå til **Project Operations** > **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="1465d-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="1465d-114">i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1465d-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1465d-115">Når disse feltene er aktivert, kan du konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="1465d-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Skjermbilde av Project Service-parametere med "Gjelder salg" uthevet](media/PS-OOB-parameters.png)

<span data-ttu-id="1465d-117">Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1465d-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="1465d-118">Hvis du vil ha mer informasjon, kan du se følgende emner.</span><span class="sxs-lookup"><span data-stu-id="1465d-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="1465d-119">Prosedyrene må fullføres i den rekkefølgen de vises.</span><span class="sxs-lookup"><span data-stu-id="1465d-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="1465d-120">Opprette en løsning for egendefinerte prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1465d-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="1465d-121">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="1465d-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="1465d-122">Legge til egendefinerte felt i prisoppsett og transaksjonsenheter </span><span class="sxs-lookup"><span data-stu-id="1465d-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="1465d-123">Konfigurere egendefinerte felt som prisdimensjoner </span><span class="sxs-lookup"><span data-stu-id="1465d-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="1465d-124">Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1465d-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="1465d-125">Prising av personaltid</span><span class="sxs-lookup"><span data-stu-id="1465d-125">Pricing human resource time</span></span>
<span data-ttu-id="1465d-126">Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="1465d-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1465d-127">Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.</span><span class="sxs-lookup"><span data-stu-id="1465d-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1465d-128">Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="1465d-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1465d-129">Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1465d-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1465d-130">Vurder om prisdimensjonen skal være en tabell eller et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="1465d-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1465d-131">Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="1465d-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="1465d-132">Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.</span><span class="sxs-lookup"><span data-stu-id="1465d-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="1465d-133">Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører.</span><span class="sxs-lookup"><span data-stu-id="1465d-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1465d-134">Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører.</span><span class="sxs-lookup"><span data-stu-id="1465d-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1465d-135">I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:</span><span class="sxs-lookup"><span data-stu-id="1465d-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1465d-136">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="1465d-136">**Sample bill rates**</span></span>

| <span data-ttu-id="1465d-137">Rolle</span><span class="sxs-lookup"><span data-stu-id="1465d-137">Role</span></span>        | <span data-ttu-id="1465d-138">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="1465d-138">Org Unit</span></span>    |<span data-ttu-id="1465d-139">Enhet</span><span class="sxs-lookup"><span data-stu-id="1465d-139">Unit</span></span>      |<span data-ttu-id="1465d-140">Pris</span><span class="sxs-lookup"><span data-stu-id="1465d-140">Price</span></span>      |<span data-ttu-id="1465d-141">Valuta</span><span class="sxs-lookup"><span data-stu-id="1465d-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1465d-142">Utvikler</span><span class="sxs-lookup"><span data-stu-id="1465d-142">Developer</span></span>   | <span data-ttu-id="1465d-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1465d-143">Contoso US</span></span>  |<span data-ttu-id="1465d-144">Hour</span><span class="sxs-lookup"><span data-stu-id="1465d-144">Hour</span></span> | <span data-ttu-id="1465d-145">200</span><span class="sxs-lookup"><span data-stu-id="1465d-145">200</span></span>|<span data-ttu-id="1465d-146">USD</span><span class="sxs-lookup"><span data-stu-id="1465d-146">USD</span></span>     |
| <span data-ttu-id="1465d-147">Utvikler</span><span class="sxs-lookup"><span data-stu-id="1465d-147">Developer</span></span>   | <span data-ttu-id="1465d-148">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="1465d-148">Contoso India</span></span> |<span data-ttu-id="1465d-149">Hour</span><span class="sxs-lookup"><span data-stu-id="1465d-149">Hour</span></span>|   <span data-ttu-id="1465d-150">112</span><span class="sxs-lookup"><span data-stu-id="1465d-150">112</span></span>|<span data-ttu-id="1465d-151">USD</span><span class="sxs-lookup"><span data-stu-id="1465d-151">USD</span></span>     |


<span data-ttu-id="1465d-152">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="1465d-152">**Sample cost rates**</span></span>

| <span data-ttu-id="1465d-153">Lønnssats</span><span class="sxs-lookup"><span data-stu-id="1465d-153">Salary Band</span></span>     | <span data-ttu-id="1465d-154">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="1465d-154">Org Unit</span></span>    |<span data-ttu-id="1465d-155">Enhet</span><span class="sxs-lookup"><span data-stu-id="1465d-155">Unit</span></span>      |<span data-ttu-id="1465d-156">Pris</span><span class="sxs-lookup"><span data-stu-id="1465d-156">Price</span></span>      |<span data-ttu-id="1465d-157">Valuta</span><span class="sxs-lookup"><span data-stu-id="1465d-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1465d-158">Mitt firma_Band1</span><span class="sxs-lookup"><span data-stu-id="1465d-158">My company_Band1</span></span> | <span data-ttu-id="1465d-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1465d-159">Contoso US</span></span>  |<span data-ttu-id="1465d-160">Hour</span><span class="sxs-lookup"><span data-stu-id="1465d-160">Hour</span></span> | <span data-ttu-id="1465d-161">145</span><span class="sxs-lookup"><span data-stu-id="1465d-161">145</span></span>|<span data-ttu-id="1465d-162">USD</span><span class="sxs-lookup"><span data-stu-id="1465d-162">USD</span></span>     |
| <span data-ttu-id="1465d-163">Mitt firma_Band2</span><span class="sxs-lookup"><span data-stu-id="1465d-163">My company_Band2</span></span> | <span data-ttu-id="1465d-164">Ekeli India</span><span class="sxs-lookup"><span data-stu-id="1465d-164">Contoso India</span></span> |<span data-ttu-id="1465d-165">Hour</span><span class="sxs-lookup"><span data-stu-id="1465d-165">Hour</span></span>|   <span data-ttu-id="1465d-166">67</span><span class="sxs-lookup"><span data-stu-id="1465d-166">67</span></span>|<span data-ttu-id="1465d-167">USD</span><span class="sxs-lookup"><span data-stu-id="1465d-167">USD</span></span>     |
