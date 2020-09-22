---
title: Opprette egendefinerte felt og enheter
description: Dette emnet forklarer hvordan du oppretter alternativsett og enheter i din egen løsning på Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754181"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="31993-103">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="31993-103">Create custom fields and entities</span></span> 

<span data-ttu-id="31993-104">Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet på Power Apps-plattformen.</span><span class="sxs-lookup"><span data-stu-id="31993-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="31993-105">Fremgangsmåtene i dette emnet bør fullføres ved hjelp av nettgrensesnittet i PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="31993-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="31993-106">Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="31993-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="31993-107">Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst.</span><span class="sxs-lookup"><span data-stu-id="31993-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="31993-108">Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.</span><span class="sxs-lookup"><span data-stu-id="31993-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="31993-109">Opprette en egendefinert løsning for prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="31993-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="31993-110">I PSA klikker du **Innstillinger** > **Løsninger**, og deretter klikker du **Ny** for å opprette en ny løsning.</span><span class="sxs-lookup"><span data-stu-id="31993-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="31993-111">Gi løsningen navnet **\<organisasjonsnavn> prisdimensjoner**, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31993-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Opprette en egendefinert løsning for prisdimensjoner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="31993-113">Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="31993-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="31993-114">En prisdimensjon kan være et alternativsett eller en enhet.</span><span class="sxs-lookup"><span data-stu-id="31993-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="31993-115">Begge må opprettes i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="31993-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="31993-116">Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="31993-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="31993-117">Enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="31993-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="31993-118">I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="31993-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="31993-119">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="31993-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="31993-120">Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="31993-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="31993-121">Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31993-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standard enhetsdefinisjon for tittel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="31993-123">Alternativsettbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="31993-123">Option set-based dimensions</span></span> 
<span data-ttu-id="31993-124">Du kan opprette to alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="31993-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="31993-125">Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet**, og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.</span><span class="sxs-lookup"><span data-stu-id="31993-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="31993-126">I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="31993-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="31993-127">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**.</span><span class="sxs-lookup"><span data-stu-id="31993-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="31993-128">Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31993-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="31993-129">Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs</span><span class="sxs-lookup"><span data-stu-id="31993-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="31993-130">Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs</span><span class="sxs-lookup"><span data-stu-id="31993-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="31993-131">Opprette data for enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="31993-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="31993-132">Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="31993-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="31993-133">Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="31993-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="31993-134">Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.</span><span class="sxs-lookup"><span data-stu-id="31993-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="31993-135">Klikk **Avansert søk** i PSA.</span><span class="sxs-lookup"><span data-stu-id="31993-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="31993-136">Velg enheten **Standardtittel**, og klikk deretter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="31993-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="31993-137">Alle radene i enheten **Standardtittel** vises.</span><span class="sxs-lookup"><span data-stu-id="31993-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="31993-138">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="31993-138">Click **New**.</span></span> <span data-ttu-id="31993-139">I **Navn**-feltet angir du "Systemingeniør" og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="31993-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="31993-140">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="31993-140">Close the form.</span></span> 
4. <span data-ttu-id="31993-141">Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".</span><span class="sxs-lookup"><span data-stu-id="31993-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="31993-142">Eksempeldata for enheten Standardtittel</span><span class="sxs-lookup"><span data-stu-id="31993-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="31993-143">Legg til alle nødvendige PSA-enheter og relaterte komponenter i prisdimensjonsløsningen</span><span class="sxs-lookup"><span data-stu-id="31993-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="31993-144">Du må legge til følgende Project Service-enheter i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="31993-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="31993-145">Følg trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="31993-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="31993-146">I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="31993-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="31993-147">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="31993-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="31993-148">I dialogboksen **Løsningskomponenter** velger du følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="31993-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="31993-149">Faktisk</span><span class="sxs-lookup"><span data-stu-id="31993-149">Actual</span></span>
- <span data-ttu-id="31993-150">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="31993-150">Bookable Resource</span></span>
- <span data-ttu-id="31993-151">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="31993-151">Estimate Line</span></span>
- <span data-ttu-id="31993-152">Fakturalinjedetalj</span><span class="sxs-lookup"><span data-stu-id="31993-152">Invoice Line Detail</span></span>
- <span data-ttu-id="31993-153">Journallinje</span><span class="sxs-lookup"><span data-stu-id="31993-153">Journal Line</span></span>
- <span data-ttu-id="31993-154">Detalj for prosjektkontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="31993-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="31993-155">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="31993-155">Project Team Member</span></span>
- <span data-ttu-id="31993-156">Tilbudslinjedetalj</span><span class="sxs-lookup"><span data-stu-id="31993-156">Quote Line Detail</span></span>
- <span data-ttu-id="31993-157">Rolleprispåslag</span><span class="sxs-lookup"><span data-stu-id="31993-157">Role Price Markup</span></span>
- <span data-ttu-id="31993-158">Rollepris</span><span class="sxs-lookup"><span data-stu-id="31993-158">Role Price</span></span> 
- <span data-ttu-id="31993-159">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="31993-159">Time Entry</span></span> 

> ![Legg til eksisterende enheter i prisdimensjonsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Velg løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="31993-162">Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.</span><span class="sxs-lookup"><span data-stu-id="31993-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="31993-163">Når du blir bedt om å inkludere avhengige enheter for enhetene som er valgt ovenfor, klikker du **Nei**.</span><span class="sxs-lookup"><span data-stu-id="31993-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Ikke ta med alle relaterte komponenter](media/Do-not-include-required.png)


