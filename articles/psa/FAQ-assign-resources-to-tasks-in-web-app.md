---
title: Hvordan tilordner jeg en ressurs som kan reserveres, til en oppgave i nettappen
description: En oversikt over måtene du kan tilordne bestillbare ressurser på.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286305"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="52bec-103">Hvordan tilordner jeg en ressurs som kan reserveres, til en oppgave i webappen (Project Service-appen v2.x)?</span><span class="sxs-lookup"><span data-stu-id="52bec-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="52bec-104">Det er to måter å tilordne en ressurs til en oppgave på i Project Service.</span><span class="sxs-lookup"><span data-stu-id="52bec-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="52bec-105">Du kan reservere en ressurs som et teammedlem og deretter tilordne den til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="52bec-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="52bec-106">Eller du kan opprette et generelt teammedlem gjennom rolletilordning i oppgaver, generere et team, og deretter oppfylle reservekravene med en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="52bec-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="52bec-107">Vær oppmerksom på at hvis du vil tilordne en ressurs som kan bestilles, til en oppgave, må ressursteammedlemmet som kan bestilles, ha nok tilgjengelige bestillinger.</span><span class="sxs-lookup"><span data-stu-id="52bec-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="52bec-108">Statusen for bestillingen må være utførelsestypen Forpliktende bestilling og status Dedikert.</span><span class="sxs-lookup"><span data-stu-id="52bec-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="52bec-109">Hvis det ikke er nok bestillinger for ressursen, fjerner Project Service tilordningen og viser følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="52bec-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="52bec-110">*Kan ikke tilordne ressurs til oppgave - Følgende ressurs(er) har ikke tilstrekkelig antall timer reservert for dette prosjektet*</span><span class="sxs-lookup"><span data-stu-id="52bec-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="52bec-111">Reserver en ressurs som et teammedlem og tilordne deretter ressursen til en oppgave</span><span class="sxs-lookup"><span data-stu-id="52bec-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="52bec-112">Med denne metoden kan du legge til en ressurs i prosjektteamet og deretter tilordne oppgaver til ressursen i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="52bec-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="52bec-113">Slik gjør du dette:</span><span class="sxs-lookup"><span data-stu-id="52bec-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="52bec-114">Legg til et nytt teammedlem ved å velge **Ny** i teammedlemsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="52bec-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="52bec-115">Velg navnet på ressursen som kan bestilles, og angi en rolle i skjermbildet for hurtigoppretting av teammedlem.</span><span class="sxs-lookup"><span data-stu-id="52bec-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="52bec-116">Velg **Fra**- og **Til**-datoer.</span><span class="sxs-lookup"><span data-stu-id="52bec-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="52bec-117">![Skjermbilde av å legge til teammedlem](media/FAQ-Resources-to-Tasks2-1.png "Skjermbilde av å legge til teammedlem")</span><span class="sxs-lookup"><span data-stu-id="52bec-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="52bec-118">Velg én av følgende tildelingsmetoder for bestilling av ressursen:</span><span class="sxs-lookup"><span data-stu-id="52bec-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="52bec-119">**Full kapasitet** bestiller ressursens fulle kapasitet for de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="52bec-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="52bec-120">**Kapasitet i prosent** bestiller ressursen med en prosent av ressursens kapasitet for de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="52bec-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="52bec-121">**Etter timer - distribuer jevnt** bestiller ressursen for et bestemt antall timer og distribuerer dem jevnt per dag over de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="52bec-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="52bec-122">**Etter timer - frontbelast** bestiller ressursen for et bestemt antall timer og frontbelaster timene per dag over de angitte fra- og til-datoene.</span><span class="sxs-lookup"><span data-stu-id="52bec-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="52bec-123">Ikke velg **Ingen** fordi den legger til ressursen i teamet, men oppretter ikke en bestilling som absorberer ressursens kapasitet.</span><span class="sxs-lookup"><span data-stu-id="52bec-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="52bec-124">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="52bec-124">Select **Save**.</span></span>

    <span data-ttu-id="52bec-125">Vær oppmerksom på at timene i bestillingen må være nok til å dekke innsatstimene og datoområdene til oppgavene som du tilordner denne ressursen til.</span><span class="sxs-lookup"><span data-stu-id="52bec-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="52bec-126">Hvis de ikke står i forhold til hverandre, kan du ikke tilordne ressursen til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="52bec-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="52bec-127">I arbeidsnedbrytningsstrukturen (WBS) for oppgaven klikker du rullegardinlisten for ressurscellen.</span><span class="sxs-lookup"><span data-stu-id="52bec-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="52bec-128">Deretter:</span><span class="sxs-lookup"><span data-stu-id="52bec-128">Then:</span></span> 

    1. <span data-ttu-id="52bec-129">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="52bec-129">Select **Add**.</span></span>
    2. <span data-ttu-id="52bec-130">Velg rullegardinlisten under **Ressurser**, og velg teammedlemmet du la til ovenfor.</span><span class="sxs-lookup"><span data-stu-id="52bec-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="52bec-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="52bec-131">Select **OK**.</span></span> <span data-ttu-id="52bec-132">Teammedlemmet tilordnes nå til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="52bec-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="52bec-133">![Skjermbilde av å legge til ressurser med WBS](media/FAQ-Resources-to-Tasks2-2.png "Skjermbilde av å legge til ressurser med WBS")</span><span class="sxs-lookup"><span data-stu-id="52bec-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="52bec-134">Du kan se aggregatet av ressursens tilordnede timer under Tilordnede timer i teammedlemsrutenettet</span><span class="sxs-lookup"><span data-stu-id="52bec-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="52bec-135">Det blir mindre enn eller lik de bestilte timene for ressursen.</span><span class="sxs-lookup"><span data-stu-id="52bec-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="52bec-136">![Skjermbilde av tilordnede timer for en ressurs](media/FAQ-Resources-to-Tasks2-3.png "Skjermbilde av tilordnede timer for en ressurs")</span><span class="sxs-lookup"><span data-stu-id="52bec-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="52bec-137">Hvis oppgaven du prøver å tilordne til ressursen, starter etter sluttdatoen for ressursbestillingene, vises ikke ressursen i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="52bec-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="52bec-138">Vær oppmerksom på at du kan tilordne en ressurs til flere timer enn de bestilte timene hvis ressursen har igjen noe ikke-tilordnet kapasitet.</span><span class="sxs-lookup"><span data-stu-id="52bec-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="52bec-139">I dette tilfellet blir ressursen bare delvis tilordnet opptil bestillingene.</span><span class="sxs-lookup"><span data-stu-id="52bec-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="52bec-140">Du kan se disse gjenværende ikke-tilordnede oppgavetimene ved å legge til kolonnen Timer uten bemanning i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="52bec-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="52bec-141">Hvis ressurser tilordnes til deres bestilte timer (bestilte timer er lik tilordnede timer), ser du følgende feilmelding når du prøver å tilordne dem ytterligere oppgaver:</span><span class="sxs-lookup"><span data-stu-id="52bec-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="52bec-142">*Kan ikke tilordne ressurs til oppgave - Følgende ressurs(er) har ikke tilstrekkelig antall timer reservert for dette prosjektet.*</span><span class="sxs-lookup"><span data-stu-id="52bec-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="52bec-143">I tillegg legges standard teammedlem for prosjektleder som legges til teamet når du oppretter prosjektet, til uten noen bestillinger og kan ikke tilordnes til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="52bec-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="52bec-144">De vises ikke i ressursrullegardinlisten for oppgaver.</span><span class="sxs-lookup"><span data-stu-id="52bec-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="52bec-145">Hvis du vil tilordne denne ressursen, må du fjerne dem fra teamet, og deretter legge dem til på nytt med en annen tildelingsmetode enn Ingen.</span><span class="sxs-lookup"><span data-stu-id="52bec-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="52bec-146">Årsaken til at de legges til teamet når prosjektet opprettes, er at et prosjekt har minst én prosjektgodkjenner som standard.</span><span class="sxs-lookup"><span data-stu-id="52bec-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="52bec-147">Opprette et generelt teammedlem gjennom rolletilordning på oppgaver</span><span class="sxs-lookup"><span data-stu-id="52bec-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="52bec-148">Denne metoden sikrer at ressursene har nok bestillinger for oppgaver.</span><span class="sxs-lookup"><span data-stu-id="52bec-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="52bec-149">Først oppretter du en plassholder eller en generell ressurs som beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene, ved å generere et team etter at rollene er tilordnet til oppgavene.</span><span class="sxs-lookup"><span data-stu-id="52bec-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="52bec-150">Slik gjør du dette:</span><span class="sxs-lookup"><span data-stu-id="52bec-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="52bec-151">Velg en oppgave i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="52bec-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="52bec-152">Velg **Tilordnet rolle**-rullegardinlisteikonet i ressurscellen.</span><span class="sxs-lookup"><span data-stu-id="52bec-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="52bec-153">Velg **Rolle**-rullegardinlisten, og velg rollen for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="52bec-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="52bec-154">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="52bec-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="52bec-155">![Skjermbilde av å bruke WBS for å legge til ressurs](media/FAQ-Resources-to-Tasks2-4.png "Skjermbilde av å bruke WBS for å legge til ressurs")</span><span class="sxs-lookup"><span data-stu-id="52bec-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="52bec-156">Når du er ferdig med å tilordne roller til oppgavene i WBS, velger du **Generer prosjektteam**.</span><span class="sxs-lookup"><span data-stu-id="52bec-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="52bec-157">Project Service oppretter minimum antall generelle teammedlemmer basert på rollene, ressursorganisasjonsenhetene og prosjektkalenderen ved å aggregere oppgavetilordningene.</span><span class="sxs-lookup"><span data-stu-id="52bec-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="52bec-158">![Skjermbilde av å generere prosjektteam](media/FAQ-Resources-to-Tasks2-5.png "Skjermbilde av å generere prosjektteam")</span><span class="sxs-lookup"><span data-stu-id="52bec-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="52bec-159">Du kan se ressurser av typen generell ressurs med rolle og stillingsnavn i Teammedlem-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="52bec-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="52bec-160">Hvis to ressurser kreves for en rolle for å fullføre arbeidet, oppretter funksjonen Generer team to teammedlemmer og bruker stillingsnavnet for å skille dem.</span><span class="sxs-lookup"><span data-stu-id="52bec-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="52bec-161">![Skjermbilde av å legge til to generelle ressurser](media/FAQ-Resources-to-Tasks2-6.png "Skjermbilde av å legge til to generelle ressurser")</span><span class="sxs-lookup"><span data-stu-id="52bec-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="52bec-162">Du kan åpne støtteressurskravet for det generelle teammedlemmet ved å velge koblingen under Ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="52bec-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="52bec-163">![Skjermbilde av å åpne støtteressurskrav](media/FAQ-Resources-to-Tasks2-7.png "Skjermbilde av å åpne støtteressurskrav")</span><span class="sxs-lookup"><span data-stu-id="52bec-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="52bec-164">Velg **Bestill** for den generelle ressursen, og deretter kan du bruke planleggingstavlen for å finne og bestille en virkelige ressurs.</span><span class="sxs-lookup"><span data-stu-id="52bec-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="52bec-165">Du kan også sende kravet for fullføring av en ressursleder ved å velge **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="52bec-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="52bec-166">Når den generelle ressursen er fullført med en navngitt ressurs, fjernes den generelle ressursen fra teamet og oppgavetilordningene for den generelle ressursen tilordnes til den navngitte ressursen som fullførte ressurskravet for den generelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="52bec-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]