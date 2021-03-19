---
title: Opprette egendefinerte felt og enheter som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte alternativsett eller enheter.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275640"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="44acd-103">Opprette egendefinerte felt og enheter som prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="44acd-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="44acd-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="44acd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="44acd-105">Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet for å bruke det/den som en prisdimensjon.</span><span class="sxs-lookup"><span data-stu-id="44acd-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="44acd-106">Hvis du vil ha mer informasjon, kan du se [Overskikt over prisdimensjoner](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="44acd-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="44acd-107">Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="44acd-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="44acd-108">Denne anbefalte fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov.</span><span class="sxs-lookup"><span data-stu-id="44acd-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="44acd-109">Dette hjelper deg også med å bruke arbeidet på nytt og gjør det enklere å overføre disse endringene til en annen forekomst etter at du har gjort alle de nødvendige endringene, eksportere denne løsningen som en **Administrert løsning** og importere den til andre forekomster for å bruke prisoppsettet på nytt.</span><span class="sxs-lookup"><span data-stu-id="44acd-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="44acd-110">Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="44acd-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="44acd-111">En prisdimensjon kan være et alternativsett eller en enhet.</span><span class="sxs-lookup"><span data-stu-id="44acd-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="44acd-112">Begge må opprettes i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="44acd-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="44acd-113">Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="44acd-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="44acd-114">Enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="44acd-114">Entity-based dimensions</span></span>
<span data-ttu-id="44acd-115">Følg denne fremgangsmåten for å opprette enhetsbaserte dimensjoner:</span><span class="sxs-lookup"><span data-stu-id="44acd-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="44acd-116">Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="44acd-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="44acd-117">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="44acd-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="44acd-118">Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="44acd-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="44acd-119">Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="44acd-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Standard enhetsdefinisjon for tittel](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="44acd-121">Alternativsettbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="44acd-121">Option set-based dimensions</span></span> 
<span data-ttu-id="44acd-122">Du kan opprette to alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="44acd-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="44acd-123">Bruk **Arbeidssted for ressurs** til å spore prisen på **Hjem**-lokasjonsarbeid og **På stedet**-arbeid.</span><span class="sxs-lookup"><span data-stu-id="44acd-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="44acd-124">Bruke **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** for å bruke et påslag når arbeidet er ferdig.</span><span class="sxs-lookup"><span data-stu-id="44acd-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="44acd-125">Følgende grafikk gir en visning av **Arbeidssted for ressurs**-dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="44acd-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="44acd-127">Følgende grafikk gir en visning av **Arbeidstimer for ressurs**-dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="44acd-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="44acd-129">Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="44acd-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="44acd-130">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**.</span><span class="sxs-lookup"><span data-stu-id="44acd-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="44acd-131">Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="44acd-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="44acd-132">Opprette data for enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="44acd-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="44acd-133">Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="44acd-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="44acd-134">Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="44acd-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="44acd-135">Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.</span><span class="sxs-lookup"><span data-stu-id="44acd-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="44acd-136">Velg **Avansert søk**.</span><span class="sxs-lookup"><span data-stu-id="44acd-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="44acd-137">Velg enheten **Standardtittel**, og velg deretter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="44acd-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="44acd-138">Alle radene i enheten **Standardtittel** vises.</span><span class="sxs-lookup"><span data-stu-id="44acd-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="44acd-139">Velg **Ny**, angi "Systemingeniør" i **Navn**-feltet og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="44acd-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="44acd-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="44acd-140">Close the page.</span></span> 
5. <span data-ttu-id="44acd-141">Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".</span><span class="sxs-lookup"><span data-stu-id="44acd-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Eksempeldata for enheten Standardtittel](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]