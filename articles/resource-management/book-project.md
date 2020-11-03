---
title: Bestille til et prosjekt
description: Dette emnet gir informasjon om bestilling av en ressurs til et prosjekt.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081472"
---
# <a name="book-to-a-project"></a><span data-ttu-id="371ec-103">Bestille til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="371ec-103">Book to a project</span></span>

<span data-ttu-id="371ec-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="371ec-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="371ec-105">Det er tilfeller der en prosjektleder eller ressursleder må tildele en ressurs til et prosjekt uten at et bestemt krav er definert fra et generelt teammedlem.</span><span class="sxs-lookup"><span data-stu-id="371ec-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="371ec-106">Dette kan oppnås på én av tre måter.</span><span class="sxs-lookup"><span data-stu-id="371ec-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="371ec-107">Bestille fra teammedlemsrutenettet</span><span class="sxs-lookup"><span data-stu-id="371ec-107">Book from the team member grid</span></span>
- <span data-ttu-id="371ec-108">Bestille fra planleggingstavlen</span><span class="sxs-lookup"><span data-stu-id="371ec-108">Book from the schedule board</span></span>
- <span data-ttu-id="371ec-109">Bestille fra **Prosjekt** -skjemaet</span><span class="sxs-lookup"><span data-stu-id="371ec-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="371ec-110">Bestille fra teammedlemsrutenettet</span><span class="sxs-lookup"><span data-stu-id="371ec-110">Book from the team member grid</span></span>

<span data-ttu-id="371ec-111">Hvis organisasjonen din opererer i hybrid ressursallokeringsmodus, kan prosjektlederen reservere en ressurs direkte i prosjektet ved å utføre følgende trinn.</span><span class="sxs-lookup"><span data-stu-id="371ec-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="371ec-112">Fra prosjektet går du til teammedlemsrutenettet og velger **Ny**.</span><span class="sxs-lookup"><span data-stu-id="371ec-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="371ec-113">Definer stillingsnavnet og rollen for ressursen.</span><span class="sxs-lookup"><span data-stu-id="371ec-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="371ec-114">Velg den bestillbare ressursen fra det tilgjengelige oppslaget.</span><span class="sxs-lookup"><span data-stu-id="371ec-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="371ec-115">Etter at du har valgt ressursen, definerer du følgende feltinformasjon for å bestille ressursen:</span><span class="sxs-lookup"><span data-stu-id="371ec-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="371ec-116">Startdato</span><span class="sxs-lookup"><span data-stu-id="371ec-116">Start date</span></span>
    - <span data-ttu-id="371ec-117">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="371ec-117">Finish date</span></span>
    - <span data-ttu-id="371ec-118">Tilordningsmetode</span><span class="sxs-lookup"><span data-stu-id="371ec-118">Allocation method</span></span>
    - <span data-ttu-id="371ec-119">Eventuelle timer</span><span class="sxs-lookup"><span data-stu-id="371ec-119">Hours, if applicable</span></span>
    - <span data-ttu-id="371ec-120">Prosjektgodkjenner</span><span class="sxs-lookup"><span data-stu-id="371ec-120">Project approver</span></span>

6. <span data-ttu-id="371ec-121">Velg **Lagre og lukk**</span><span class="sxs-lookup"><span data-stu-id="371ec-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="371ec-122">Bestille fra planleggingstavlen</span><span class="sxs-lookup"><span data-stu-id="371ec-122">Book from the schedule board</span></span>

<span data-ttu-id="371ec-123">Når en ressursleder må reservere en ressurs direkte til et prosjekt, kan de bruke planleggingstavlen og prosjektkravet.</span><span class="sxs-lookup"><span data-stu-id="371ec-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="371ec-124">Prosjektkravet er et ressurskrav som alltid er tilgjengelig for bestilling.</span><span class="sxs-lookup"><span data-stu-id="371ec-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="371ec-125">Fullfør fremgangsmåten nedenfor for å bestille direkte til et prosjekt fra planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="371ec-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="371ec-126">Naviger til planleggingstavlen og filtrer etter ressursene du vurderer for kravet, på venstre side.</span><span class="sxs-lookup"><span data-stu-id="371ec-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="371ec-127">Velg **Prosjekt** -fanen i den nederste ruten for å vise en liste over prosjektkrav.</span><span class="sxs-lookup"><span data-stu-id="371ec-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="371ec-128">Dra kravet til en ressurs, og definer følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="371ec-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="371ec-129">Startdato</span><span class="sxs-lookup"><span data-stu-id="371ec-129">Start date</span></span>
    - <span data-ttu-id="371ec-130">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="371ec-130">Finish date</span></span>
    - <span data-ttu-id="371ec-131">Bestillingsstatus</span><span class="sxs-lookup"><span data-stu-id="371ec-131">Booking status</span></span>
    - <span data-ttu-id="371ec-132">Bestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="371ec-132">Booking method</span></span>
    - <span data-ttu-id="371ec-133">Varighet</span><span class="sxs-lookup"><span data-stu-id="371ec-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="371ec-134">Bestille fra Prosjekt-skjemaet</span><span class="sxs-lookup"><span data-stu-id="371ec-134">Book from the Project form</span></span>

<span data-ttu-id="371ec-135">Som prosjektleder må du kanskje reservere en ressurs til et prosjekt, men du kjenner bare til vilkårene i stedet for navnet på ressursen.</span><span class="sxs-lookup"><span data-stu-id="371ec-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="371ec-136">Fullfør fremgangsmåten nedenfor for å bruke planleggingsassistenten til å finne en ressurs basert på eventuelle tilgjengelige attributter for ressursen.</span><span class="sxs-lookup"><span data-stu-id="371ec-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="371ec-137">Naviger til prosjektet, og velg **Bestill** for å åpne planleggingsassistenten.</span><span class="sxs-lookup"><span data-stu-id="371ec-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="371ec-138">Bruk filtrene på venstre side av planleggingsveiviseren til å begrense vilkårene, og velg **Søk.**</span><span class="sxs-lookup"><span data-stu-id="371ec-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="371ec-139">Basert på ressurser som returneres i resultatet, kan du reservere en ressurs.</span><span class="sxs-lookup"><span data-stu-id="371ec-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="371ec-140">Denne metoden oppretter ingen bestillinger for ressursen.</span><span class="sxs-lookup"><span data-stu-id="371ec-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="371ec-141">I stedet legges ressursen til for teamet.</span><span class="sxs-lookup"><span data-stu-id="371ec-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="371ec-142">Når teammedlemmene er lagt til i prosjektet, kan prosjektlederen bruke vedlikehold av bestillinger eller utvide bestillinger til å legge til de nødvendige bestillingerne i ressursen.</span><span class="sxs-lookup"><span data-stu-id="371ec-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
