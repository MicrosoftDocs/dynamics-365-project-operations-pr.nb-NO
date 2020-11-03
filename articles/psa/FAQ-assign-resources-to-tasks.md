---
title: Tilordne en ressurs til en oppgave
description: Dette emnet gir informasjon om hvordan du tilordner ressurser til oppgaver.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081809"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="9c85b-103">Tilordne en ressurs til en oppgave</span><span class="sxs-lookup"><span data-stu-id="9c85b-103">Assign a resource to a task</span></span>

<span data-ttu-id="9c85b-104">Det er tre måter å tilordne en ressurs til en oppgave på i Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9c85b-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="9c85b-105">Reserver en ressurs som et teammedlem og tilordne deretter ressursen til en oppgave</span><span class="sxs-lookup"><span data-stu-id="9c85b-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="9c85b-106">Du kan legge til en ressurs i prosjektteamet og deretter tilordne ressursen til oppgaver i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="9c85b-107">Legg til et nytt teammedlem ved å velge **Ny** i kategorien **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="9c85b-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="9c85b-108">Panelet for **hurtigoppretting av teammedlem** åpnes, der du kan velge navnet på ressursen som kan bestilles, og angi en rolle.</span><span class="sxs-lookup"><span data-stu-id="9c85b-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="9c85b-109">Velg én av følgende tildelingsmetoder for bestilling av ressursen:</span><span class="sxs-lookup"><span data-stu-id="9c85b-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="9c85b-110">**Full kapasitet** bestiller ressursens fulle kapasitet for de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="9c85b-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9c85b-111">**Kapasitet i prosent** bestiller ressursen med en prosent av ressursens kapasitet for de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="9c85b-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="9c85b-112">**Etter timer - distribuer jevnt** bestiller ressursen for et bestemt antall timer og distribuerer dem jevnt per dag over de angitte fra-/til-datoene.</span><span class="sxs-lookup"><span data-stu-id="9c85b-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="9c85b-113">**Etter timer - frontbelast** bestiller ressursen for et bestemt antall timer og frontbelaster timene per dag over de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="9c85b-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="9c85b-114">**Ingen** legger til ressursen i teamet, men oppretter ikke en bestilling som absorberer kapasiteten deres.</span><span class="sxs-lookup"><span data-stu-id="9c85b-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="9c85b-115">I rutenettet **Planlegg** for en oppgave velger du **Ressurs** -ikonet i ressurscellen, og velger deretter teammedlemmet du akkurat la til, under **Teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="9c85b-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="9c85b-116">I kategorien **Teammedlem** og **Avstemming** viser ressursen bestilte timer og tilordnede timer.</span><span class="sxs-lookup"><span data-stu-id="9c85b-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="9c85b-117">Timene børl være like, men behøver ikke være det ettersom bestillinger og tilordninger ikke er tett sammenknyttet.</span><span class="sxs-lookup"><span data-stu-id="9c85b-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="9c85b-118">Kategorien **Avstemming** gir informasjon når de er forskjellige, for eksempel når du tilordner en ressurs flere timer enn du har bestilt.</span><span class="sxs-lookup"><span data-stu-id="9c85b-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="9c85b-119">Om nødvendig kan du korrigere informasjonen ved å utvide ressursens bestillinger eller endre tilordningen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="9c85b-120">Opprette et generelt teammedlem gjennom oppgavetilordning</span><span class="sxs-lookup"><span data-stu-id="9c85b-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="9c85b-121">Når du oppretter et generelt teammedlem via oppgavetildeling, oppretter du en plassholder eller en generell ressurs som beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene.</span><span class="sxs-lookup"><span data-stu-id="9c85b-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="9c85b-122">Deretter genererer du et krav (eller sender en forespørsel ved hjelp av kravet) som brukes til å søke etter og reservere den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="9c85b-123">I rutenettet **Planlegg** for en oppgave velger du **ressursikonet** i ressurscellen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="9c85b-124">Skriv inn et navn som fungerer som plassholder for ressursens navn.</span><span class="sxs-lookup"><span data-stu-id="9c85b-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="9c85b-125">For eksempel "Programleder".</span><span class="sxs-lookup"><span data-stu-id="9c85b-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="9c85b-126">Velg **Opprett** , og angi rollen for den generelle ressursen i feltet for **hurtigoppretting av prosjektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="9c85b-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="9c85b-127">Du kan fortsette å tilordne oppgaver til denne plassholderessursen ved å velge ressursen i **ressursvelgeren** for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="9c85b-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="9c85b-128">De er oppført under **Teammedlemmer**.</span><span class="sxs-lookup"><span data-stu-id="9c85b-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="9c85b-129">Når du er ferdig med å tilordne den generelle ressursen, velger du den generelle ressursen i kategorien **Team** og velger deretter **Generer krav** for å opprette et ressurskrav for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="9c85b-130">Velg **Bestill** for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="9c85b-131">Du kan deretter bruke planleggingstavlen for å finne og bestille en virkelig ressurs.</span><span class="sxs-lookup"><span data-stu-id="9c85b-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="9c85b-132">Du kan også sende kravet for fullføring av en ressursleder.</span><span class="sxs-lookup"><span data-stu-id="9c85b-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="9c85b-133">Når den generelle ressursen er fullført med en navngitt ressurs, fjernes den generelle ressursen fra teamet og oppgavetilordningene for den generelle ressursen tilordnes til den navngitte ressursen som fullførte ressurskravet for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="9c85b-134">Tilordne en navngitt ressurs fra listen over alle ressurser som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="9c85b-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="9c85b-135">Du kan bruke søkeboksen i **ressursvelgeren** for å søke i alle ressursene som kan reserveres, og tilordne dem til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="9c85b-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="9c85b-136">Ressurser som er tilordnet på denne måten, blir lagt til i teamet uten bestillinger.</span><span class="sxs-lookup"><span data-stu-id="9c85b-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="9c85b-137">Dette ligner på å legge til et teammedlem og velge Ingen som tildelingsmetode.</span><span class="sxs-lookup"><span data-stu-id="9c85b-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="9c85b-138">Ressursen vises i kategorien **Team** og kategorien **Avstemming** som ressurser med bare tilordninger og et bestillingsunderskudd.</span><span class="sxs-lookup"><span data-stu-id="9c85b-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="9c85b-139">Reserver dem hvis du vil bruke tilgjengeligheten deres.</span><span class="sxs-lookup"><span data-stu-id="9c85b-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="9c85b-140">I rutenettet **Planlegg** for en oppgave velger du **ressursikonet** i ressurscellen.</span><span class="sxs-lookup"><span data-stu-id="9c85b-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="9c85b-141">Begynn å skrive inn et navn.</span><span class="sxs-lookup"><span data-stu-id="9c85b-141">Start typing a name.</span></span> <span data-ttu-id="9c85b-142">Søkeresultater for navnet vises i **ressursvelgeren** under **Andre ressurser**.</span><span class="sxs-lookup"><span data-stu-id="9c85b-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="9c85b-143">Velg ressursen som du vil tilordne til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="9c85b-143">Select the resource that you want to assign to the task.</span></span>

