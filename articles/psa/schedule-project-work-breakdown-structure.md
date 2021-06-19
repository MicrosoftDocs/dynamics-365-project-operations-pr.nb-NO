---
title: Planlegge et prosjekt med en arbeidsnedbrytningsstruktur
description: Slik planlegger du et prosjekt med en arbeidsnedbrytningsstruktur i Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008593"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="13553-103">Planlegge et prosjekt med en arbeidsnedbrytningsstruktur (Project Service)</span><span class="sxs-lookup"><span data-stu-id="13553-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="13553-104">En prosjektplan kommuniserer hvilke oppgaver som må utføres, hvilke ressurser som skal utføre arbeidet, og tidsrammen som arbeidet må fullføres i.</span><span class="sxs-lookup"><span data-stu-id="13553-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="13553-105">Prosjektplanen gjenspeiler alt arbeidet som er forbundet med å levere prosjektet i tide.</span><span class="sxs-lookup"><span data-stu-id="13553-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="13553-106">Et av de første trinnene i startfasen av prosjektet er å komme opp med en prosjektplan.</span><span class="sxs-lookup"><span data-stu-id="13553-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="13553-107">Hvis du vil opprette en prosjektplan, må du opprette en arbeidsnedbrytningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="13553-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="13553-108">Opprett en prosjektstruktur med en arbeidsnedbrytningsstruktur, som hjelper deg å:</span><span class="sxs-lookup"><span data-stu-id="13553-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="13553-109">Dele opp arbeidet i håndterbare oppgaver</span><span class="sxs-lookup"><span data-stu-id="13553-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="13553-110">Beregne tiden som kreves for å fullføre en oppgave</span><span class="sxs-lookup"><span data-stu-id="13553-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="13553-111">Angi oppgaveavhengigheter og oppgavevarighet</span><span class="sxs-lookup"><span data-stu-id="13553-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="13553-112">Fastslå rollene som kreves for å fullføre hver oppgave</span><span class="sxs-lookup"><span data-stu-id="13553-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="13553-113">Prosjektplanen i arbeidsnedbrytningsstrukturen har et velkjent utseende, komplett med et interaktivt Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="13553-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="13553-114">Opprette en arbeidsnedbrytningsstruktur for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="13553-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="13553-115">Opprett en arbeidsnedbrytningsstruktur for å representere sekvensen av oppgavene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="13553-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="13553-116">Arbeidsnedbrytningsstrukturen omfatter oppgaver, krav for hver oppgave og informasjon om inntekter og kostnader.</span><span class="sxs-lookup"><span data-stu-id="13553-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="13553-117">I en arbeidsnedbrytningsstruktur kan du legge til:</span><span class="sxs-lookup"><span data-stu-id="13553-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="13553-118">Rekkefølgen for oppgvaer i et hierarki</span><span class="sxs-lookup"><span data-stu-id="13553-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="13553-119">Andre oppgaver, om noen, som må fullføres før du kan starte en oppgave</span><span class="sxs-lookup"><span data-stu-id="13553-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="13553-120">Startdato, sluttdato og varighet for en oppave</span><span class="sxs-lookup"><span data-stu-id="13553-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="13553-121">Antall timer som kreves for en oppgave</span><span class="sxs-lookup"><span data-stu-id="13553-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="13553-122">Eventuelle nødvendige arbeiderferdigheter og -utdanning</span><span class="sxs-lookup"><span data-stu-id="13553-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="13553-123">Arbeiderne som er tildelt en oppgave</span><span class="sxs-lookup"><span data-stu-id="13553-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="13553-124">Beregnet omsetning og kostnader</span><span class="sxs-lookup"><span data-stu-id="13553-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="13553-125">Oppgavetyper</span><span class="sxs-lookup"><span data-stu-id="13553-125">Task types</span></span>  
<span data-ttu-id="13553-126">Når du oppretter en arbeidsnedbrytningsstruktur, skal du bruke følgende typer oppgaver:</span><span class="sxs-lookup"><span data-stu-id="13553-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="13553-127">**Rotnode for prosjektet**</span><span class="sxs-lookup"><span data-stu-id="13553-127">**Project root node**</span></span> | <span data-ttu-id="13553-128">Hovedaktiviteten på øverste nivå for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="13553-128">The top-level summary task for the project.</span></span> <span data-ttu-id="13553-129">Alle andre prosjektoppgaver opprettes under den.</span><span class="sxs-lookup"><span data-stu-id="13553-129">All other project tasks are created under it.</span></span> <span data-ttu-id="13553-130">Navnet på rotoppgaven er navnet på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="13553-130">The name of the root task is the project name.</span></span> <span data-ttu-id="13553-131">Innsats, datoer og varighet for rotnoden er basert på verdiene i hierarkiet under den.</span><span class="sxs-lookup"><span data-stu-id="13553-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="13553-132">Du kan ikke redigere egenskaper for rotnoden eller slette rotnoden.</span><span class="sxs-lookup"><span data-stu-id="13553-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="13553-133">**Hovedaktiviteter eller beholderoppgaver**</span><span class="sxs-lookup"><span data-stu-id="13553-133">**Summary or container tasks**</span></span> | <span data-ttu-id="13553-134">En hovedaktivitet er en oppgave som har deloppgaver under seg.</span><span class="sxs-lookup"><span data-stu-id="13553-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="13553-135">En hovedaktivitet har ikke arbeidsinnsats eller kostnader selv.</span><span class="sxs-lookup"><span data-stu-id="13553-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="13553-136">Arbeidsinnsatsen og kostnadene er en beregnet verdi av deloppgavene.</span><span class="sxs-lookup"><span data-stu-id="13553-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="13553-137">Du kan endre navnet på en hovedaktivitet, men du kan ikke endre innsats, datoer eller varighet, fordi de blir automatisk beregnet.</span><span class="sxs-lookup"><span data-stu-id="13553-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="13553-138">Hvis du sletter en hovedaktivitet, slettes oppgaven og alle deloppgavene.</span><span class="sxs-lookup"><span data-stu-id="13553-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="13553-139">**Bladnodeoppgaver**</span><span class="sxs-lookup"><span data-stu-id="13553-139">**Leaf node tasks**</span></span> | <span data-ttu-id="13553-140">En bladnodeoppgave representerer det mest detaljerte arbeidet på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="13553-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="13553-141">Den har en beregnet arbeidsinnsats, et planlagt antall ressurser, planlagte start- og sluttdatoer og en varighet.</span><span class="sxs-lookup"><span data-stu-id="13553-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="13553-142">Oppgavehierarki</span><span class="sxs-lookup"><span data-stu-id="13553-142">Task hierarchy</span></span>  
 <span data-ttu-id="13553-143">Du har følgende alternativer når du oppretter et oppgavehierarki:</span><span class="sxs-lookup"><span data-stu-id="13553-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="13553-144">**Legg til oppgave**.</span><span class="sxs-lookup"><span data-stu-id="13553-144">**Add task**.</span></span>   <span data-ttu-id="13553-145">Du kan legge til en oppgave i en posisjon du velger i oppgavehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="13553-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="13553-146">Hvis du ikke velger en posisjon, vises den nye oppgaven på slutten.</span><span class="sxs-lookup"><span data-stu-id="13553-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="13553-147">**Rykk inn aktivitet**.</span><span class="sxs-lookup"><span data-stu-id="13553-147">**Indent task**.</span></span>   <span data-ttu-id="13553-148">Rykke inn en aktivitet for å gjøre den til en underordnet aktivitet direkte ovenfor.</span><span class="sxs-lookup"><span data-stu-id="13553-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="13553-149">**Reduser innrykk for aktivitet**.</span><span class="sxs-lookup"><span data-stu-id="13553-149">**Outdent task**.</span></span>   <span data-ttu-id="13553-150">Reduser innrykk for en aktivitet, slik at den ikke lenger en underordnet aktivitet for den opprinnelige overordnede aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="13553-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="13553-151">**Flytt opp og Flytt ned**.</span><span class="sxs-lookup"><span data-stu-id="13553-151">**Move up and Move down**.</span></span>   <span data-ttu-id="13553-152">Flytt aktiviteter opp eller ned i hierarkiet for den overordnede aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="13553-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="13553-153">Hvis du flytter en aktivitet opp eller ned, har dette ingen innvirkning på arbeid, kostnader, datoer eller varighet.</span><span class="sxs-lookup"><span data-stu-id="13553-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="13553-154">Oppgaveattributter</span><span class="sxs-lookup"><span data-stu-id="13553-154">Task attributes</span></span>  
 <span data-ttu-id="13553-155">Et oppgavenavn beskriver arbeidet som må fullføres.</span><span class="sxs-lookup"><span data-stu-id="13553-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="13553-156">Du kan bruke forskjellige oppgaveattributter til å beskrive tidsplanen og bemanningsbehovene for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="13553-157">Planlegge attributter</span><span class="sxs-lookup"><span data-stu-id="13553-157">Schedule attributes</span></span>

 - <span data-ttu-id="13553-158">Tilordne verdier til **Innsatstimer**, **Antall ressurser**, **Startdato**, **Sluttdato** og **Varighet** for å bestemme tidsplanen for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="13553-159">**Innsats** er et estimat for timene det tar å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="13553-160">**Antall ressurser** er et estimat som prosjektlederen legger inn i oppgaven, for å komme opp med den beste mulige tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="13553-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="13553-161">**Varighet** (i dager) angir hvor mange arbeidsdager det vil ta å fullføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="13553-162">Bemanningsattributter</span><span class="sxs-lookup"><span data-stu-id="13553-162">Staffing attributes</span></span>

 - <span data-ttu-id="13553-163">**Rolle**, **Organisasjonsenhet for ressurs**, **Antall ressurser** og **Ressurser** beskriver bemanningsbehovene for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="13553-164">**Rolle** beskriver hvilken type ressurs som kreves for å utføre oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="13553-165">**Organisasjonsenhet for ressurs** angir organisasjonsenheten der ressursene skal bemannes for denne oppgaven. Dette også påvirker kostnader og salgsestimat for oppgaven, siden dette er gjort rede for når det skal avgjøres enhetssalgspris for ressursen.</span><span class="sxs-lookup"><span data-stu-id="13553-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="13553-166">**Ressurser** inneholder en generell ressurs eller en navngitt ressurs når noe blir funnet.</span><span class="sxs-lookup"><span data-stu-id="13553-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="13553-167">Oppgaveavhengigheter</span><span class="sxs-lookup"><span data-stu-id="13553-167">Task dependencies</span></span>  
 <span data-ttu-id="13553-168">Du kan opprette avhengigheter mellom én eller flere oppgaver for foregående oppgave i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="13553-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="13553-169">Du kan angi én eller flere verdier for feltet for foregående oppgaver for å angi hvilke oppgaver det skal være avhengig av.</span><span class="sxs-lookup"><span data-stu-id="13553-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="13553-170">Når du tilordner en verdi for foregående oppgave til en oppgave, kan oppgaven bare starte når alle de foregående oppgavene er fullført.</span><span class="sxs-lookup"><span data-stu-id="13553-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="13553-171">Sette denne avhengigheten på en oppgave fører til ny beregning av den planlagte startdatoen for oppgaven som siste slutten av alle de foregående oppgavene.</span><span class="sxs-lookup"><span data-stu-id="13553-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="13553-172">Foregåenderelaterte innvirkninger på en tidsplan er ikke begrenset til oppgavemodus definert på oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="13553-173">Oppgavemodus</span><span class="sxs-lookup"><span data-stu-id="13553-173">Task mode</span></span>  
 <span data-ttu-id="13553-174">Oppgavemodus er en av de viktige faktorene som bestemmer planlegging av bladnodeoppgaver.</span><span class="sxs-lookup"><span data-stu-id="13553-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="13553-175">Det finnes to oppgavemoduser for hver oppgave: automatisk planleggingsmodus og manuell planleggingsmodus.</span><span class="sxs-lookup"><span data-stu-id="13553-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="13553-176">**Automatisk planlegging**.</span><span class="sxs-lookup"><span data-stu-id="13553-176">**Auto scheduling**.</span></span>   <span data-ttu-id="13553-177">Når du angir oppgavemodusen til automatisk planlagt, bruker oppgaveplanleggingsmotoren planleggingsreglene på følgende oppgaveattributter for å bestemme tidsplanen for oppgaven:</span><span class="sxs-lookup"><span data-stu-id="13553-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="13553-178">Foregående oppgaver</span><span class="sxs-lookup"><span data-stu-id="13553-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="13553-179">Innsats</span><span class="sxs-lookup"><span data-stu-id="13553-179">Effort</span></span>  
  
    -   <span data-ttu-id="13553-180">Antall ressurser</span><span class="sxs-lookup"><span data-stu-id="13553-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="13553-181">Start- og sluttdatoer</span><span class="sxs-lookup"><span data-stu-id="13553-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="13553-182">**Planleggingsregler**.</span><span class="sxs-lookup"><span data-stu-id="13553-182">**Scheduling rules**.</span></span>   <span data-ttu-id="13553-183">Startdatoen for en bladnodeoppgave som ikke har standard foregående oppgaver, settes som standard til planlagt startdato for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="13553-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="13553-184">Varigheten av en bladnodeoppgave er alltid beregnet som antall arbeidsdager mellom start- og sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="13553-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="13553-185">Når en oppgave planlegges automatisk, vil planleggingsmotoren følge reglene nedenfor:</span><span class="sxs-lookup"><span data-stu-id="13553-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="13553-186">Start- og sluttdatoer for en oppgave må alltid være virkedager i henhold til prosjektets planleggingskalender</span><span class="sxs-lookup"><span data-stu-id="13553-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="13553-187">Startdatoen for en oppgave som har foregående oppgaver, settes som standard til den seneste sluttdatoen for foregående oppgaver</span><span class="sxs-lookup"><span data-stu-id="13553-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="13553-188">Innsats = antall personer \* varighet \* timer i en standard arbeidsdag i prosjektkalenderen</span><span class="sxs-lookup"><span data-stu-id="13553-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="13553-189">**Manuell planlegging**.</span><span class="sxs-lookup"><span data-stu-id="13553-189">**Manual scheduling**.</span></span>   <span data-ttu-id="13553-190">I noen tilfeller vil du kanskje avvike fra disse reglene.</span><span class="sxs-lookup"><span data-stu-id="13553-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="13553-191">I slike tilfeller kan du angi oppgavemodusen for oppgaven som skal planlegges manuelt.</span><span class="sxs-lookup"><span data-stu-id="13553-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="13553-192">Dette stopper planleggingsmotoren fra å beregne verdier for andre planleggingsattributter.</span><span class="sxs-lookup"><span data-stu-id="13553-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="13553-193">Angi foregående oppgaver påvirker alltid startdatoen for den avhengige oppgaven.</span><span class="sxs-lookup"><span data-stu-id="13553-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="13553-194">Opprette en arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="13553-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="13553-195">Gå til **Project Service > Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="13553-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="13553-196">Klikk prosjektet du vil arbeide på.</span><span class="sxs-lookup"><span data-stu-id="13553-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="13553-197">Velg pil ned ved siden av prosjektnavnet i feltet øverst på skjermen, og klikk deretter Arbeidsnedbrytningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="13553-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="13553-198">Hvis du vil legge til en oppgave, klikker du **Legg til oppgave**.</span><span class="sxs-lookup"><span data-stu-id="13553-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="13553-199">Fyll ut feltene for oppgaven, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="13553-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="13553-200">Fortsett å legge til oppgaver til arbeidsnedbrytningsstrukturen er fullført.</span><span class="sxs-lookup"><span data-stu-id="13553-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="13553-201">Når du oppretter en arbeidsnedbrytningsstruktur, kan du gjøre følgende for å organisere oppgavene:</span><span class="sxs-lookup"><span data-stu-id="13553-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="13553-202">Velg en oppgave, og klikk **Innrykk** for å flytte den under en annen oppgave, eller klikk Reduser innrykk for å flytte den ut et nivå.</span><span class="sxs-lookup"><span data-stu-id="13553-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="13553-203">Velg en oppgave, og klikk **Flytt opp** eller **Flytt ned** for å flytte den opp eller ned i listen.</span><span class="sxs-lookup"><span data-stu-id="13553-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="13553-204">Klikk **Skjul Gantt-diagram** for å skjule Gantt-diagrammet, og klikk **Vis Gantt-diagram** for å vise det på nytt.</span><span class="sxs-lookup"><span data-stu-id="13553-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="13553-205">Velg en annen tidsperiode for Gantt-diagrammet i **Tidsskala**.</span><span class="sxs-lookup"><span data-stu-id="13553-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="13553-206">Hvis du vil legge til roller som du har angitt i arbeidsnedbrytningsstrukturen, for teammedlemmer i prosjektet, klikker du **Generer prosjektteam**.</span><span class="sxs-lookup"><span data-stu-id="13553-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="13553-207">Klikk **Lagre** nederst til høyre på skjermen når du er ferdig med endringene.</span><span class="sxs-lookup"><span data-stu-id="13553-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="13553-208">Se også</span><span class="sxs-lookup"><span data-stu-id="13553-208">See Also</span></span>  
 [<span data-ttu-id="13553-209">Prosjektlederveiledning</span><span class="sxs-lookup"><span data-stu-id="13553-209">Project manager guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]