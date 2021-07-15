---
title: Hjemmeside for pris- og kostnadsdimensjoner
description: Dette emnet gir en oversikt over prisdimensjoner.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5c8c28839f5e7b3259afbea4ab400d0c4fca95fd
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368893"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="1b988-103">Hjemmeside for pris- og kostnadsdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1b988-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1b988-104">Dimensjonene som brukes til å angi pris og kostnad for arbeid i prosjektbaserte organisasjoner, er påvirket av følgende attributter:</span><span class="sxs-lookup"><span data-stu-id="1b988-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="1b988-105">Personer som utfører arbeid som ligner på deres erfaring, rolle eller geografi</span><span class="sxs-lookup"><span data-stu-id="1b988-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="1b988-106">Arbeid som skal utføres på samme måte som kompleksiteten eller tiden på dagen</span><span class="sxs-lookup"><span data-stu-id="1b988-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="1b988-107">Gitt den vanlige typen av disse attributtene for arbeidet og personene som kreves for å utføre arbeidet, er de to typer prisdimensjonsverdier tilgjengelige i Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="1b988-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="1b988-108">**Alternativsett** – attributter som er faste opplistinger for et sett med verdier.</span><span class="sxs-lookup"><span data-stu-id="1b988-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1b988-109">**Enhetsbaserte verdier** – attributter som kan ha et variert sett med verdier som er begrensede, men som kan endre seg over tid.</span><span class="sxs-lookup"><span data-stu-id="1b988-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1b988-110">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1b988-110">Pricing dimensions</span></span>

<span data-ttu-id="1b988-111">PSA leveres med et standardsett med prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b988-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1b988-112">Du kan vise disse ved å gå til **Project Service** > **Parametere**.</span><span class="sxs-lookup"><span data-stu-id="1b988-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="1b988-113">i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1b988-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1b988-114">Dette gjør det mulig å konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="1b988-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Skjermbilde av Project Service-parametere med "Gjelder salg" uthevet](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="1b988-116">Hvis du har brukt de medfølgende feltene for rolle og organisasjonsenhet som prisdimensjoner før versjon 3 av PSA, vil det ikke være noen observerbar endring.</span><span class="sxs-lookup"><span data-stu-id="1b988-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="1b988-117">Du kan fortsette å bruke Project Service på vanlig måte.</span><span class="sxs-lookup"><span data-stu-id="1b988-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="1b988-118">Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b988-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="1b988-119">Hvis du vil ha mer informasjon, kan du se følgende emner, men vær oppmerksom på at du må fullføre prosedyrene i rekkefølgen angitt nedenfor:</span><span class="sxs-lookup"><span data-stu-id="1b988-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="1b988-120">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="1b988-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="1b988-121">Legge til egendefinerte felt i prisoppsett og transaksjonsenheter</span><span class="sxs-lookup"><span data-stu-id="1b988-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="1b988-122">Konfigurere egendefinerte felt som prisdimensjoner </span><span class="sxs-lookup"><span data-stu-id="1b988-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="1b988-123">Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="1b988-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="1b988-124">Prising av personaltid</span><span class="sxs-lookup"><span data-stu-id="1b988-124">Pricing human resource time</span></span>
<span data-ttu-id="1b988-125">Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="1b988-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1b988-126">Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.</span><span class="sxs-lookup"><span data-stu-id="1b988-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1b988-127">Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt.</span><span class="sxs-lookup"><span data-stu-id="1b988-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1b988-128">Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="1b988-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1b988-129">Vurder om prisdimensjonen skal være en tabell eller et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="1b988-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1b988-130">Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett.</span><span class="sxs-lookup"><span data-stu-id="1b988-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="1b988-131">Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste bedriftsbrukere.</span><span class="sxs-lookup"><span data-stu-id="1b988-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="1b988-132">Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører.</span><span class="sxs-lookup"><span data-stu-id="1b988-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1b988-133">Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører.</span><span class="sxs-lookup"><span data-stu-id="1b988-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1b988-134">I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:</span><span class="sxs-lookup"><span data-stu-id="1b988-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1b988-135">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="1b988-135">**Sample bill rates**</span></span>

| <span data-ttu-id="1b988-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="1b988-136">Role</span></span>        | <span data-ttu-id="1b988-137">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="1b988-137">Org Unit</span></span>    |<span data-ttu-id="1b988-138">Enhet</span><span class="sxs-lookup"><span data-stu-id="1b988-138">Unit</span></span>      |<span data-ttu-id="1b988-139">Pris</span><span class="sxs-lookup"><span data-stu-id="1b988-139">Price</span></span>      |<span data-ttu-id="1b988-140">Valuta</span><span class="sxs-lookup"><span data-stu-id="1b988-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1b988-141">Utvikler</span><span class="sxs-lookup"><span data-stu-id="1b988-141">Developer</span></span>   | <span data-ttu-id="1b988-142">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="1b988-142">Contoso US</span></span>  |<span data-ttu-id="1b988-143">Time</span><span class="sxs-lookup"><span data-stu-id="1b988-143">Hour</span></span> | <span data-ttu-id="1b988-144">200</span><span class="sxs-lookup"><span data-stu-id="1b988-144">200</span></span>|<span data-ttu-id="1b988-145">USD</span><span class="sxs-lookup"><span data-stu-id="1b988-145">USD</span></span>     |
| <span data-ttu-id="1b988-146">Utvikler</span><span class="sxs-lookup"><span data-stu-id="1b988-146">Developer</span></span>   | <span data-ttu-id="1b988-147">Contoso India</span><span class="sxs-lookup"><span data-stu-id="1b988-147">Contoso India</span></span> |<span data-ttu-id="1b988-148">Time</span><span class="sxs-lookup"><span data-stu-id="1b988-148">Hour</span></span>|   <span data-ttu-id="1b988-149">112</span><span class="sxs-lookup"><span data-stu-id="1b988-149">112</span></span>|<span data-ttu-id="1b988-150">USD</span><span class="sxs-lookup"><span data-stu-id="1b988-150">USD</span></span>     |


<span data-ttu-id="1b988-151">**Eksempel på kostnadssatser**</span><span class="sxs-lookup"><span data-stu-id="1b988-151">**Sample cost rates**</span></span>

| <span data-ttu-id="1b988-152">Lønnssats</span><span class="sxs-lookup"><span data-stu-id="1b988-152">Salary Band</span></span>     | <span data-ttu-id="1b988-153">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="1b988-153">Org Unit</span></span>    |<span data-ttu-id="1b988-154">Enhet</span><span class="sxs-lookup"><span data-stu-id="1b988-154">Unit</span></span>      |<span data-ttu-id="1b988-155">Pris</span><span class="sxs-lookup"><span data-stu-id="1b988-155">Price</span></span>      |<span data-ttu-id="1b988-156">Valuta</span><span class="sxs-lookup"><span data-stu-id="1b988-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1b988-157">Mitt firma_Band1</span><span class="sxs-lookup"><span data-stu-id="1b988-157">My company_Band1</span></span> | <span data-ttu-id="1b988-158">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="1b988-158">Contoso US</span></span>  |<span data-ttu-id="1b988-159">Time</span><span class="sxs-lookup"><span data-stu-id="1b988-159">Hour</span></span> | <span data-ttu-id="1b988-160">145</span><span class="sxs-lookup"><span data-stu-id="1b988-160">145</span></span>|<span data-ttu-id="1b988-161">USD</span><span class="sxs-lookup"><span data-stu-id="1b988-161">USD</span></span>     |
| <span data-ttu-id="1b988-162">Mitt firma_Band2</span><span class="sxs-lookup"><span data-stu-id="1b988-162">My company_Band2</span></span> | <span data-ttu-id="1b988-163">Contoso India</span><span class="sxs-lookup"><span data-stu-id="1b988-163">Contoso India</span></span> |<span data-ttu-id="1b988-164">Time</span><span class="sxs-lookup"><span data-stu-id="1b988-164">Hour</span></span>|   <span data-ttu-id="1b988-165">67</span><span class="sxs-lookup"><span data-stu-id="1b988-165">67</span></span>|<span data-ttu-id="1b988-166">USD</span><span class="sxs-lookup"><span data-stu-id="1b988-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]