---
title: Opprette egendefinerte felt og enheter som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte alternativsett eller enheter.
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
ms.openlocfilehash: 616bcd5758b434b45bd06aa1a026f32efc8b7f99
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130905"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="9fb6c-103">Opprette egendefinerte felt og enheter som prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="9fb6c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="9fb6c-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9fb6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9fb6c-105">Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fb6c-106">Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="9fb6c-107">Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="9fb6c-108">Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="9fb6c-109">Opprette en egendefinert løsning for prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="9fb6c-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="9fb6c-110">Gå til **Innstillinger** > **Løsninger**, og velg deretter du **Ny** for å opprette en ny løsning.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="9fb6c-111">Gi løsningen navnet **\<your organization name>-prisdimensjoner**, angi den gjenstående nødvendige informasjonen, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="9fb6c-112">Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="9fb6c-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="9fb6c-113">En prisdimensjon kan være et alternativsett eller en enhet.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="9fb6c-114">Begge må opprettes i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="9fb6c-115">Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="9fb6c-116">Enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="9fb6c-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="9fb6c-117">Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="9fb6c-118">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="9fb6c-119">Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="9fb6c-120">Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="9fb6c-121">Alternativsettbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="9fb6c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="9fb6c-122">Du kan opprette to alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="9fb6c-123">Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet**, og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="9fb6c-124">Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9fb6c-125">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="9fb6c-126">Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="9fb6c-127">Opprette data for enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="9fb6c-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="9fb6c-128">Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="9fb6c-129">Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="9fb6c-130">Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="9fb6c-131">Velg **Avansert søk**, velg enheten **Standardtittel**, og velg deretter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="9fb6c-132">Alle radene i enheten **Standardtittel** vises.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="9fb6c-133">Velg **Ny**, angi "Systemingeniør" i **Navn**-feltet og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="9fb6c-134">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-134">Close the form.</span></span> 
4. <span data-ttu-id="9fb6c-135">Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".</span><span class="sxs-lookup"><span data-stu-id="9fb6c-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="9fb6c-136">Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen</span><span class="sxs-lookup"><span data-stu-id="9fb6c-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="9fb6c-137">Du må legge til følgende enheter i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="9fb6c-138">Følg trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="9fb6c-139">Velg **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="9fb6c-140">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="9fb6c-141">I dialogboksen **Løsningskomponenter** velger du følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="9fb6c-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="9fb6c-142">Faktisk</span><span class="sxs-lookup"><span data-stu-id="9fb6c-142">Actual</span></span>
  - <span data-ttu-id="9fb6c-143">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="9fb6c-143">Bookable Resource</span></span>
  - <span data-ttu-id="9fb6c-144">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="9fb6c-144">Estimate Line</span></span>
  - <span data-ttu-id="9fb6c-145">Fakturalinjedetalj</span><span class="sxs-lookup"><span data-stu-id="9fb6c-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="9fb6c-146">Journallinje</span><span class="sxs-lookup"><span data-stu-id="9fb6c-146">Journal Line</span></span>
  - <span data-ttu-id="9fb6c-147">Detalj for prosjektkontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="9fb6c-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="9fb6c-148">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="9fb6c-148">Project Team Member</span></span>
  - <span data-ttu-id="9fb6c-149">Tilbudslinjedetalj</span><span class="sxs-lookup"><span data-stu-id="9fb6c-149">Quote Line Detail</span></span>
  - <span data-ttu-id="9fb6c-150">Rolleprispåslag</span><span class="sxs-lookup"><span data-stu-id="9fb6c-150">Role Price Markup</span></span>
  - <span data-ttu-id="9fb6c-151">Rollepris</span><span class="sxs-lookup"><span data-stu-id="9fb6c-151">Role Price</span></span> 
  - <span data-ttu-id="9fb6c-152">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="9fb6c-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="9fb6c-153">Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="9fb6c-154">Når du blir bedt om å inkludere avhengige enheter for enhetene som er valgt ovenfor, klikker du **Nei**.</span><span class="sxs-lookup"><span data-stu-id="9fb6c-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

