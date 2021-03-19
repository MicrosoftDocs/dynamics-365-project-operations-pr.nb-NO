---
title: Endringer i ressursbehandling (Project Service Automation 3.x)
description: Dette emnet inneholder informasjon om endringene i ressursbehandling.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5f88d7309a5e1171629a72e749bfc01abb64c62a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284775"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="4d5ca-103">Endringer i ressursbehandling (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="4d5ca-104">Delene i dette emnet gir informasjon om endringene som er gjort i ressursbehandling i Dynamics 365 Project Service Automation versjon 3.x.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="4d5ca-105">Prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="4d5ca-105">Project estimates</span></span>

<span data-ttu-id="4d5ca-106">I stedet for å være basert på enheten **msdyn\_projecttask** (**Prosjektoppgave**) er prosjektestimater basert på enheten **msdyn\_resourceassignment** (**Ressurstilordning**).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="4d5ca-107">Ressurstilordningene har blitt "kilden til sannheten" for oppgaveplanlegging og prising.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="4d5ca-108">Linjeoppgaver</span><span class="sxs-lookup"><span data-stu-id="4d5ca-108">Line tasks</span></span>

<span data-ttu-id="4d5ca-109">I PSA 3.x er linjeoppgaver foreldede (avskrevet).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="4d5ca-110">Tilordninger peker nå på hele oppgaven i stedet for linjeoppgavene.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="4d5ca-111">Følgende eksempel viser hvordan en oppgave med navnet "Testoppgave" er tilordnet til teammedlemmer A og B i tidligere versjoner av PSA og i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="4d5ca-112">**Før PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="4d5ca-113">Testoppgave</span><span class="sxs-lookup"><span data-stu-id="4d5ca-113">Test task</span></span>

        - <span data-ttu-id="4d5ca-114">Testoppgave – linjeoppgave 1</span><span class="sxs-lookup"><span data-stu-id="4d5ca-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="4d5ca-115">Tilordning til A</span><span class="sxs-lookup"><span data-stu-id="4d5ca-115">Assignment to A</span></span>

        - <span data-ttu-id="4d5ca-116">Testoppgave – linjeoppgave 2</span><span class="sxs-lookup"><span data-stu-id="4d5ca-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="4d5ca-117">Tilordning til B</span><span class="sxs-lookup"><span data-stu-id="4d5ca-117">Assignment to B</span></span>

- <span data-ttu-id="4d5ca-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="4d5ca-119">Testoppgave</span><span class="sxs-lookup"><span data-stu-id="4d5ca-119">Test task</span></span>

        - <span data-ttu-id="4d5ca-120">Tilordning til A</span><span class="sxs-lookup"><span data-stu-id="4d5ca-120">Assignment to A</span></span>
        - <span data-ttu-id="4d5ca-121">Tilordning til B</span><span class="sxs-lookup"><span data-stu-id="4d5ca-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="4d5ca-122">Ikke-tilordnet tilordning</span><span class="sxs-lookup"><span data-stu-id="4d5ca-122">Unassigned assignment</span></span>

<span data-ttu-id="4d5ca-123">I PSA 3.x er en ikke-tilordnet tilordning en tilordning som er tilordnet til et **NULLl**-teammedlem og en **NULL**-ressurs.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="4d5ca-124">Ikke-tilordnede tilordninger kan forekomme i noen scenarioer:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="4d5ca-125">Hvis en oppgave er opprettet, men ennå ikke er tilordnet til noen teammedlemmer, opprettes det alltid en tilordning som ikke er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="4d5ca-126">Hvis alle tilordnede ressurser i en oppgave blir fjernet, blir en ikke-tilordnet tilordning opprettet på nytt for den oppgaven.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="4d5ca-127">Planlegge felt i Prosjektoppgave-enheten</span><span class="sxs-lookup"><span data-stu-id="4d5ca-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="4d5ca-128">Feltene i enheten **msdyn\_projecttask** er avskrevet eller flyttet til enheten **msdyn\_resourceassignment**, eller de blir referert til fra enheten **msdyn\_projectteam** (**Prosjektteammedlem**).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="4d5ca-129">Avskrevet felt i msdyn\_projecttask (Prosjektoppgave)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4d5ca-130">Nytt felt i msdyn\_resourceassignment (Ressurstilordning)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="4d5ca-131">Kommentar</span><span class="sxs-lookup"><span data-stu-id="4d5ca-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="4d5ca-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="4d5ca-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="4d5ca-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d5ca-133">None</span></span> | |
| <span data-ttu-id="4d5ca-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="4d5ca-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="4d5ca-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d5ca-135">None</span></span> | |
| <span data-ttu-id="4d5ca-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="4d5ca-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="4d5ca-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d5ca-137">None</span></span> | |
| <span data-ttu-id="4d5ca-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="4d5ca-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="4d5ca-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="4d5ca-139">None</span></span> | |
| <span data-ttu-id="4d5ca-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="4d5ca-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="4d5ca-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="4d5ca-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="4d5ca-142">Formatet på JSON-datastrukturen (JavaScript Object Notation) som er lagret i feltet, er endret.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="4d5ca-143">Tidsplankontur</span><span class="sxs-lookup"><span data-stu-id="4d5ca-143">Schedule contour</span></span>

<span data-ttu-id="4d5ca-144">Tidsplankonturen er lagret i feltet **Planlagt arbeid** (**msdyn\_plannedwork**) i hver **Ressurstilordning**-enhet (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="4d5ca-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="4d5ca-145">Structure</span></span>

<span data-ttu-id="4d5ca-146">Den nye strukturen i planleggingskonturen består av fleksible tidsdeler som er definert for hver dag i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="4d5ca-147">Hver tidssektor har følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="4d5ca-148">**Start** – starten på arbeidstiden for dagen i henhold til prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="4d5ca-149">**Slutt** – slutten på arbeidstiden for dagen i henhold til prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="4d5ca-150">**Timer** – antall timer som er tilordnet på dagen.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="4d5ca-151">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-151">**Example**</span></span>

<span data-ttu-id="4d5ca-152">Dette eksemplet bruker en prosjektkalender der arbeidsdagen er fra 9 til 17 i UTC-8-tidssonen.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="4d5ca-153">Automatisk planlegging og manuell planlegging</span><span class="sxs-lookup"><span data-stu-id="4d5ca-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="4d5ca-154">Hvis en oppgave er automatisk planlagt, lastes timene inn, og oppgavevarigheten kan bli redusert.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="4d5ca-155">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-155">**Example**</span></span>

<span data-ttu-id="4d5ca-156">Følgende oppgave planlegges automatisk til 18 timer i løpet av tre dager (3. desember 2018 til 5. desember 2018).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="4d5ca-157">Hvis en oppgave planlegges manuelt, distribueres timene jevnt til alle datoene.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="4d5ca-158">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-158">**Example**</span></span>

<span data-ttu-id="4d5ca-159">Følgende oppgave planlegges manuelt til 18 timer i løpet av tre dager (3. desember 2018 til 5. desember 2018).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="4d5ca-160">Tilordningsenhet</span><span class="sxs-lookup"><span data-stu-id="4d5ca-160">Assignment unit</span></span>

<span data-ttu-id="4d5ca-161">Tilordningsenheten er avskrevet i PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="4d5ca-162">Oppgaveinnsatstimene er nå likt delt per dag, blant alle de tildelte ressursene.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="4d5ca-163">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="4d5ca-163">**Example**</span></span>

<span data-ttu-id="4d5ca-164">I dette eksemplet er oppgaven tilordnet to ressurser og planlagt automatisk i 36 timer over tre dager (3. desember 2018 til 5. desember 2018).</span><span class="sxs-lookup"><span data-stu-id="4d5ca-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="4d5ca-165">Tilordning 1:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="4d5ca-166">Tilordning 2:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="4d5ca-167">Prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="4d5ca-167">Pricing dimensions</span></span>

<span data-ttu-id="4d5ca-168">I PSA 3.x er ressursspesifikke prisdimensjonsfelt (for eksempel **Rolle** og **Organisasjonsenhet**) fjernet fra enheten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="4d5ca-169">Disse feltene kan nå hentes fra det tilsvarende prosjektteammedlemmet (**msdyn\_projectteam**) til ressurstilordningen (**msdyn\_resourceassignment**) når prosjektestimater genereres.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="4d5ca-170">Et nytt felt, **msdyn\_organizationalunit**, er lagt til i enheten **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="4d5ca-171">Avskrevet felt i msdyn\_projecttask (Prosjektoppgave)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4d5ca-172">Felt fra msdyn\_projectteam (Prosjektteammedlem) som brukes i stedet</span><span class="sxs-lookup"><span data-stu-id="4d5ca-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="4d5ca-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4d5ca-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="4d5ca-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="4d5ca-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="4d5ca-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="4d5ca-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="4d5ca-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="4d5ca-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="4d5ca-177">Profiler</span><span class="sxs-lookup"><span data-stu-id="4d5ca-177">Contours</span></span>

<span data-ttu-id="4d5ca-178">Feltene for prising og estimeringsprofil er avskrevet i enheten **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="4d5ca-179">De er flyttet til enheten **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="4d5ca-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="4d5ca-180">Avskrevet felt i msdyn\_projecttask (Prosjektoppgave)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="4d5ca-181">Nytt felt i msdyn\_resourceassignment (Ressurstilordning)</span><span class="sxs-lookup"><span data-stu-id="4d5ca-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="4d5ca-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="4d5ca-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="4d5ca-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="4d5ca-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="4d5ca-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="4d5ca-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="4d5ca-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="4d5ca-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="4d5ca-186">Følgende felt er lagt til i enheten **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="4d5ca-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4d5ca-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="4d5ca-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4d5ca-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="4d5ca-189">Følgende felt for planlagt, faktisk og gjenstående kostnad og salg er uendret i enheten **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="4d5ca-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="4d5ca-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="4d5ca-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="4d5ca-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="4d5ca-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="4d5ca-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="4d5ca-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="4d5ca-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="4d5ca-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="4d5ca-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="4d5ca-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="4d5ca-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="4d5ca-195">msdyn\_remainingsales</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]