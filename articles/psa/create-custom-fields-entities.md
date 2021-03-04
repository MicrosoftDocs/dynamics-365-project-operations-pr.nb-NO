---
title: Opprette egendefinerte felt og enheter
description: Dette emnet forklarer hvordan du oppretter alternativsett og enheter i din egen løsning på Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b9e32c8871a8986ba827f742baf4e4d5cd9dd235
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144875"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="bd9d7-103">Opprette egendefinerte felt og enheter</span><span class="sxs-lookup"><span data-stu-id="bd9d7-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bd9d7-104">Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet på Power Apps-plattformen.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="bd9d7-105">Fremgangsmåtene i dette emnet bør fullføres ved hjelp av nettgrensesnittet i PSA (Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="bd9d7-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd9d7-106">Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="bd9d7-107">Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="bd9d7-108">Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="bd9d7-109">Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="bd9d7-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="bd9d7-110">En prisdimensjon kan være et alternativsett eller en enhet.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="bd9d7-111">Begge må opprettes i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="bd9d7-112">Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="bd9d7-113">Enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="bd9d7-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="bd9d7-114">I PSA klikker du på **Innstillinger** > **Løsninger** og dobbeltklikker deretter på **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="bd9d7-115">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="bd9d7-116">Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="bd9d7-117">Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standard enhetsdefinisjon for tittel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="bd9d7-119">Alternativsettbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="bd9d7-119">Option set-based dimensions</span></span> 
<span data-ttu-id="bd9d7-120">Du kan opprette to alternativsettbaserte dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="bd9d7-121">Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet**, og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="bd9d7-122">I PSA klikker du på **Innstillinger** > **Løsninger** og dobbeltklikker deretter på **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="bd9d7-123">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="bd9d7-124">Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="bd9d7-125">Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs</span><span class="sxs-lookup"><span data-stu-id="bd9d7-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="bd9d7-126">Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs</span><span class="sxs-lookup"><span data-stu-id="bd9d7-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="bd9d7-127">Opprette data for enhetsbaserte dimensjoner</span><span class="sxs-lookup"><span data-stu-id="bd9d7-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="bd9d7-128">Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="bd9d7-129">Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="bd9d7-130">Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="bd9d7-131">Klikk **Avansert søk** i PSA.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="bd9d7-132">Velg enheten **Standardtittel**, og klikk deretter **Resultater**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="bd9d7-133">Alle radene i enheten **Standardtittel** vises.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="bd9d7-134">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-134">Click **New**.</span></span> <span data-ttu-id="bd9d7-135">I **Navn**-feltet angir du "Systemingeniør" og klikker deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="bd9d7-136">Lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="bd9d7-136">Close the form.</span></span> 
4. <span data-ttu-id="bd9d7-137">Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".</span><span class="sxs-lookup"><span data-stu-id="bd9d7-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="bd9d7-138">Eksempeldata for enheten Standardtittel</span><span class="sxs-lookup"><span data-stu-id="bd9d7-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


