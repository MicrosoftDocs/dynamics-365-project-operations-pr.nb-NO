---
title: Opprette en prosjektbestilling fra planleggingstavlen
description: Dette emnet gir informasjon om hvordan du oppretter en prosjektestilling fra planleggingstavlen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122310"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="d2646-103">Opprette en prosjektbestilling fra planleggingstavlen</span><span class="sxs-lookup"><span data-stu-id="d2646-103">Create a project booking from the Schedule board</span></span>

<span data-ttu-id="d2646-104">Du kan reservere en ressurs til et prosjekt direkte fra kategorien **Team** i prosjektet eller ved å generere et ressurskrav fra en generell teammedlemstilordning og deretter oppfylle det genererte kravet med et prosjektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="d2646-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="d2646-105">Du kan også bestille en ressurs til et prosjekt direkte fra planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="d2646-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="d2646-106">Du kan gjøre dette på tre måter:</span><span class="sxs-lookup"><span data-stu-id="d2646-106">There are three ways to do this:</span></span>

- <span data-ttu-id="d2646-107">**Bestille fra et generert ressurskrav:** Du kan generere et ressurskrav etter at du har opprettet en generisk ressurs og tilordnet oppgaver i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d2646-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="d2646-108">**Bestille fra det primære kravet:** De primære kravene vises på planleggingstavlen i kategorien **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="d2646-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="d2646-109">**Bestille fra et nytt ressurskrav:** Du kan opprette et ressurskrav fra grunnen av og knytte det til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d2646-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="d2646-110">På planleggingstavlen vises ressurskravet i **Åpne krav**-kategorien.</span><span class="sxs-lookup"><span data-stu-id="d2646-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="d2646-111">Bestille fra et generert ressurskrav</span><span class="sxs-lookup"><span data-stu-id="d2646-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="d2646-112">Du kan opprette en generell ressurs og tilordne den til én oppgave eller flere oppgaver i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d2646-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="d2646-113">Deretter kan du generere et ressurskrav fra det generelle teammedlemmet.</span><span class="sxs-lookup"><span data-stu-id="d2646-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="d2646-114">På planleggingstavlen vises denne ressursen i **Åpne krav**-kategorien. Du må kanskje bruke kolonnefiltre i rutenettet hvis du har mange åpne krav.</span><span class="sxs-lookup"><span data-stu-id="d2646-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="d2646-115">![Kategorien Åpne krav på planleggingstavlen](media/FAQ-Project-Booking-Schedule-Board-1.png "Skjermbilde av tabell med bestillinger og tilordninger")</span><span class="sxs-lookup"><span data-stu-id="d2646-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="d2646-116">Velg kravet.</span><span class="sxs-lookup"><span data-stu-id="d2646-116">Select the requirement.</span></span> <span data-ttu-id="d2646-117">**Søk etter tilgjengelighet**-kategorien vises øverst i den valgte raden.</span><span class="sxs-lookup"><span data-stu-id="d2646-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="d2646-118">Når du velger kategorien, åpnes modusen Planleggingsassistent på planleggingstavlen og filtrerer de tilgjengelige ressursene som oppfyller ressurskravet.</span><span class="sxs-lookup"><span data-stu-id="d2646-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="d2646-119">Deretter kan du bestille en ressurs.</span><span class="sxs-lookup"><span data-stu-id="d2646-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="d2646-120">Du kan også dra og slippe valgt rad fra bunnen av planleggingstavlen til en ressurscelle i rutenettet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="d2646-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="d2646-121">Når du slipper det, åpner **Opprett ressursbestilling**-panelet til høyre.</span><span class="sxs-lookup"><span data-stu-id="d2646-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="d2646-122">Valg av **Bestill** bestiller ressursen til prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="d2646-122">Selecting **Book** books the resource onto the project team.</span></span>

![Panel for å opprette ressursbestilling](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="d2646-124">Bestille fra det primære kravet</span><span class="sxs-lookup"><span data-stu-id="d2646-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="d2646-125">Når du oppretter et prosjekt i Project Service, opprettes automatisk et ressurskrav kalt primærkrav.</span><span class="sxs-lookup"><span data-stu-id="d2646-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="d2646-126">Dette er et tomt krav som brukes til å bestille raskt en ressurs med planleggingstavlen uten å generere et krav eller opprette ett helt forfra.</span><span class="sxs-lookup"><span data-stu-id="d2646-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="d2646-127">Fordi kravet er tomt, må du angi datoer samt tildelingsmetode og timer hvis det er aktuelt.</span><span class="sxs-lookup"><span data-stu-id="d2646-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="d2646-128">Hvis du vil bestille en ressurs med primærkravet, velger du **Prosjekt**-kategorien på planleggingstavlen. Det kan hende du må bruke kolonnefilteret i **Prosjekt**-kolonnen hvis du har mange prosjekter.</span><span class="sxs-lookup"><span data-stu-id="d2646-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="d2646-129">![Kolonnefiltre på planleggingstavlen](media/FAQ-Project-Booking-Schedule-Board-2.png "Skjermbilde av tabell med bestillinger og tilordninger")</span><span class="sxs-lookup"><span data-stu-id="d2646-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="d2646-130">Velg kravet som bare har prosjektnavnet som navn, og som har en varighet på null (0).</span><span class="sxs-lookup"><span data-stu-id="d2646-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="d2646-131">Velg **Søk etter tilgjengelighet**-kategorien som vises i raden.</span><span class="sxs-lookup"><span data-stu-id="d2646-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="d2646-132">Dette setter planleggingstavlen i modusen Planleggingsassistent og viser tilgjengelige ressurser som kan bestilles på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d2646-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="d2646-133">Siden et **primærkrav** er et tomt krav med null (0) varighet, må du angi varigheten i **Opprett ressursbestilling**-panelet når du velger og bestiller en ressurs.</span><span class="sxs-lookup"><span data-stu-id="d2646-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="d2646-134">Du kan også velge **primærkravet for prosjektet** nederst på planleggingstavlen og dra og slippe det på en ressurs for å bestille den.</span><span class="sxs-lookup"><span data-stu-id="d2646-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="d2646-135">Siden **primærkravet** er et tomt krav med null (0) varighet, må du angi varigheten i **Opprett ressursbestilling**-panelet når du velger og bestiller en ressurs.</span><span class="sxs-lookup"><span data-stu-id="d2646-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="d2646-136">Når du bestiller en ressurs gjennom **primærkravet på planleggingstavlen**, kan du legge den til prosjektteamet uten tilordninger.</span><span class="sxs-lookup"><span data-stu-id="d2646-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="d2646-137">Bestille fra et nytt ressurskrav</span><span class="sxs-lookup"><span data-stu-id="d2646-137">Book from a new resource requirement</span></span>
<span data-ttu-id="d2646-138">Fullfør fremgangsmåten nedenfor for å bestille fra et nytt ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="d2646-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="d2646-139">Gå til **Ressurskrav** og velg deretter **Ny** for å opprette et nytt ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="d2646-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="d2646-140">Velg et prosjekt i kategorien **Prosjekt** for å knytte behovet til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d2646-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="d2646-141">På planleggingstavlen vises dette nylig opprettede kravet som et **åpent krav** som du kan fullføre.</span><span class="sxs-lookup"><span data-stu-id="d2646-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="d2646-142">Bestill ressursen for å legge den til i prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="d2646-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="d2646-143">Nå som ressursen er bestilt, må du tilordne oppgaver manuelt.</span><span class="sxs-lookup"><span data-stu-id="d2646-143">Now that the resource is booked, you must assign tasks manually.</span></span>

