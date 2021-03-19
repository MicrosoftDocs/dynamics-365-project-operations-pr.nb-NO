---
title: Oppgraderingshensyn for arbeidsnedbrytningsstruktur
description: Dette emnet gir informasjon om oppgradering av arbeidsnedbrytningsstrukturen fra Project Service Automation 2.x til 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281760"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="2c5d4-103">Oppgraderingshensyn for arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="2c5d4-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2c5d4-104">Dette emnet gir informasjon om oppgradering av arbeidsnedbrytningsstrukturen fra Project Service Automation 2.x til 3.x.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="2c5d4-105">Dette emnet definerer om statusen for et prosjekt er ok i Project Service Automation (PSA), slik at en vellykket oppgradering kan utføres.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="2c5d4-106">Det finnes også informasjon om vanlige blokkeringstilstander som vil føre til at oppgraderingen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="2c5d4-107">Hvis du vil ha mer informasjon om hvordan du definerer prosjektpppgaver og deres funksjoner i en prosjekttidsplan, kan du se [Prosjektplaner](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="2c5d4-108">Viktige enheter</span><span class="sxs-lookup"><span data-stu-id="2c5d4-108">Key entities</span></span>
<span data-ttu-id="2c5d4-109">For en presis arbeidsnedbrytningsstruktur som allerede er lastet inn med ressurser, kreves følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="2c5d4-110">Prosjekt</span><span class="sxs-lookup"><span data-stu-id="2c5d4-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="2c5d4-111">Prosjektteam</span><span class="sxs-lookup"><span data-stu-id="2c5d4-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="2c5d4-112">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="2c5d4-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="2c5d4-113">Ressurstilordninger</span><span class="sxs-lookup"><span data-stu-id="2c5d4-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="2c5d4-114">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="2c5d4-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="2c5d4-115">Ressurser som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="2c5d4-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="2c5d4-116">For å definere en ressursbelastet arbeidsnedbrytingsstruktur må du utføre følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="2c5d4-117">Opprett et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-117">Create a new project.</span></span> <span data-ttu-id="2c5d4-118">Hvis du vil ha mer informasjon om hvordan du oppretter et nytt prosjekt, se [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="2c5d4-119">Opprett én eller flere oppgaver.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-119">Create one or more tasks.</span></span> <span data-ttu-id="2c5d4-120">Hvis du vil ha mer informasjon om hvordan du oppretter en oppgave, se [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="2c5d4-121">Definer aktivitetsavhengighetene.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-121">Define the task dependencies.</span></span> <span data-ttu-id="2c5d4-122">Hvis du vil ha mer informasjon, se [Avhengighet for prosjektoppgaver](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="2c5d4-123">Tilordne prosjektteammedlemmer til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-123">Assign project team members to the project.</span></span> <span data-ttu-id="2c5d4-124">Hvis du vil ha mer informasjon, kan du se [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="2c5d4-125">Tilordne prosjektteammedlemmer til oppgavene.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="2c5d4-126">Hvis du vil ha mer informasjon, kan du se [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="2c5d4-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="2c5d4-127">Prosjektteamrelasjoner</span><span class="sxs-lookup"><span data-stu-id="2c5d4-127">Project team relationships</span></span>

<span data-ttu-id="2c5d4-128">For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="2c5d4-129">Alle prosjektteammedlemmer må tilknyttes en ressurs som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="2c5d4-130">Alle prosjektteammedlemmer må tilknyttes samme prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="2c5d4-131">Prosjektoppgaverelasjoner</span><span class="sxs-lookup"><span data-stu-id="2c5d4-131">Project task relationships</span></span>
<span data-ttu-id="2c5d4-132">For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2c5d4-133">Alle relaterte oppgaver må tilknyttes samme prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="2c5d4-134">Hver linjeoppgave må ha en overordnet oppgave.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="2c5d4-135">Hver oppgave må ha et overordnet prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="2c5d4-136">Gyldige betingelser</span><span class="sxs-lookup"><span data-stu-id="2c5d4-136">Valid conditions</span></span>

- <span data-ttu-id="2c5d4-137">Alle oppgavevarigheter må være større enn eller lik (> =) én time og mindre enn 1 800 000 minutter (1 250 dager). \*</span><span class="sxs-lookup"><span data-stu-id="2c5d4-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="2c5d4-138">Alle oppgaver må ha en startdato som ikke er tidligere enn 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="2c5d4-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="2c5d4-139">Alle oppgaver må ha en startdato som ikke er senere enn 17 år fra den gjeldende dagen.\*</span><span class="sxs-lookup"><span data-stu-id="2c5d4-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="2c5d4-140">Alle oppgaver må ha en startdato som er tidligere enn eller lik sluttdatoen.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="2c5d4-141">Alle transaksjonstyper på klassifiseringer (utgift, material, avgift og tid) må ha verdier for **Standardenhet** og **Enhetsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="2c5d4-142">Datoformater med bokstaver bør unngås.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="2c5d4-143">Potensielle løsningstrinn</span><span class="sxs-lookup"><span data-stu-id="2c5d4-143">Potential mitigation steps</span></span>
- <span data-ttu-id="2c5d4-144">Bruk Avansert søk til å identifisere prosjektoppgaver som ikke inneholder en prosjekt-ID.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="2c5d4-145">Bruk Avansert søk til å identifisere prosjektoppgaver der planlagt varighet er større enn > 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="2c5d4-146">Før du gjør endringer i dataene må du undersøke alle tilpassinger som er knyttet til enheten, og som kan ha fått dataene i en ugyldig tilstand.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="2c5d4-147">Disse tilpassingene bør adresseres før du fortsetter med datarelaterte oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="2c5d4-148">For de identifiserte oppgavene som har vært isolerte, bør du vurdere å slette disse oppgavene hvis de ikke er nødvendige, eller hvis de skal knyttes til det riktige overordnede prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="2c5d4-149">For alle oppgaver der varigheten er større enn 1 250 dager, bør du vurdere å legge til flere oppgaver for å representere den totale varigheten hvis det er mulig.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="2c5d4-150">Elementer som er angitt med en stjerne (\*), har grenser som skyldes at kunderelasjonsstyring (CRM) bare støtter 7 320 regelmessighetsutvidelser.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="2c5d4-151">Du må være under denne grensen.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="2c5d4-152">Ressurstilordningsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="2c5d4-152">Resource Assignment relationships</span></span>
<span data-ttu-id="2c5d4-153">For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2c5d4-154">Alle ressurstilordninger i en arbeidsnedbrytningsstruktur må være relatert til samme prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="2c5d4-155">Alle ressurstilordninger i en arbeidsnedbrytningsstruktur må være tilknyttet prosjekteammedlemmene i samme prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="2c5d4-156">Potensielle løsningstrinn</span><span class="sxs-lookup"><span data-stu-id="2c5d4-156">Potential mitigation steps</span></span>
- <span data-ttu-id="2c5d4-157">Identifiser alle oppgaver som faller utenfor vilkårene som er beskrevet ovenfor.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="2c5d4-158">Eventuelle ressurstilordninger som ikke er gyldige lenger, må slettes.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="2c5d4-159">Relasjoner for prosjektoppgaveavhengighet</span><span class="sxs-lookup"><span data-stu-id="2c5d4-159">Project task dependency relationships</span></span>
<span data-ttu-id="2c5d4-160">For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:</span><span class="sxs-lookup"><span data-stu-id="2c5d4-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="2c5d4-161">Alle avhengigheter for prosjektoppgaver må være relatert til samme prosjekt.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="2c5d4-162">En oppgave kan ikke referere til samme avhengighet mer enn én gang.</span><span class="sxs-lookup"><span data-stu-id="2c5d4-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]