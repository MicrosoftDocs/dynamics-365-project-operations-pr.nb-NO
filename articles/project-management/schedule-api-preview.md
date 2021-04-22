---
title: Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter
description: Dette emnet inneholder informasjon og eksempler for bruk av API-er for tidsplan.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868141"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="dc6ee-103">Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter</span><span class="sxs-lookup"><span data-stu-id="dc6ee-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="dc6ee-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="dc6ee-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="dc6ee-105">Noen av eller alle funksjonene som er angitt i dette emnet, er tilgjengelig som en del av en forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="dc6ee-106">Innholdet i og funksjonaliteten kan endres.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="dc6ee-107">Planleggingsenheter</span><span class="sxs-lookup"><span data-stu-id="dc6ee-107">Scheduling entities</span></span>

<span data-ttu-id="dc6ee-108">API-er for planlegging gjør det mulig å utføre operasjoner for oppretting, oppdatering og sletting med **planleggingsenheter**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="dc6ee-109">Disse enhetene administreres via planleggingsmotoren i Project for the web.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="dc6ee-110">Oppretting, oppdatering og sletting med **planleggingsenheter** var begrenser i tidligere versjoner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="dc6ee-111">Tabellen nedenfor viser en fullstendig liste over **planleggingsenhetene**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="dc6ee-112">Enhetsnavn</span><span class="sxs-lookup"><span data-stu-id="dc6ee-112">Entity name</span></span>  | <span data-ttu-id="dc6ee-113">Logisk navn for enhet</span><span class="sxs-lookup"><span data-stu-id="dc6ee-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="dc6ee-114">Project</span><span class="sxs-lookup"><span data-stu-id="dc6ee-114">Project</span></span> | <span data-ttu-id="dc6ee-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="dc6ee-115">msdyn_project</span></span> |
| <span data-ttu-id="dc6ee-116">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="dc6ee-116">Project Task</span></span>  | <span data-ttu-id="dc6ee-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="dc6ee-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="dc6ee-118">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="dc6ee-118">Project Task Dependency</span></span>  | <span data-ttu-id="dc6ee-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="dc6ee-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="dc6ee-120">Ressurstilordning</span><span class="sxs-lookup"><span data-stu-id="dc6ee-120">Resource Assignment</span></span> | <span data-ttu-id="dc6ee-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="dc6ee-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="dc6ee-122">Prosjektsamling</span><span class="sxs-lookup"><span data-stu-id="dc6ee-122">Project Bucket</span></span>  | <span data-ttu-id="dc6ee-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="dc6ee-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="dc6ee-124">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="dc6ee-124">Project Team Member</span></span> | <span data-ttu-id="dc6ee-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="dc6ee-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="dc6ee-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="dc6ee-126">OperationSet</span></span>

<span data-ttu-id="dc6ee-127">OperationSet er et enhetsarbeidsmønster som kan brukes når flere forespørsler som påvirker tidsplanen, må behandles i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="dc6ee-128">API-er for planlegging</span><span class="sxs-lookup"><span data-stu-id="dc6ee-128">Schedule APIs</span></span>

<span data-ttu-id="dc6ee-129">Nedenfor vises en liste over gjeldende API-er for planlegging.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="dc6ee-130">**msdyn_CreateProjectV1:** Denne API-en kan brukes til å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="dc6ee-131">Prosjektet og standard prosjektsamling opprettes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="dc6ee-132">**msdyn_CreateTeamMemberV1:** Denne API-en kan brukes til å opprette et prosjektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="dc6ee-133">Teammedlemsoppføringen opprettes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="dc6ee-134">**msdyn_CreateOperationSetV1**: Denne API-en kan brukes til å planlegge flere forespørsler som må utføres i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="dc6ee-135">**msdyn_PSSCreateV1**: Denne API-en kan brukes til å opprette en enhet.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="dc6ee-136">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter opprettingsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="dc6ee-137">**msdyn_PSSUpdateV1**: Denne API-en kan brukes til å oppdatere en enhet.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="dc6ee-138">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter oppdateringsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="dc6ee-139">**msdyn_PSSDeleteV1**: Denne API-en kan brukes til å slette en enhet.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="dc6ee-140">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter sletteoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="dc6ee-141">**msdyn_ExecuteOperationSetV1**: Denne API-en brukes til å kjøre alle operasjonene i det angitte operasjonssettet.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="dc6ee-142">Bruke API-er for tidsplan med OperationSet</span><span class="sxs-lookup"><span data-stu-id="dc6ee-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="dc6ee-143">Ettersom oppføringer med både **CreateProjectV1** og **CreateTeamMemberV1** opprettes umiddelbart, kan ikke disse API-ene brukes direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="dc6ee-144">Du kan imidlertid bruke API-en til å opprette nødvendige oppføringer, opprette et **OperationSet** og deretter bruke disse forhåndsopprettede oppføringene i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="dc6ee-145">Støttede operasjoner</span><span class="sxs-lookup"><span data-stu-id="dc6ee-145">Supported operations</span></span>

| <span data-ttu-id="dc6ee-146">Planleggingsenhet</span><span class="sxs-lookup"><span data-stu-id="dc6ee-146">Scheduling entity</span></span> | <span data-ttu-id="dc6ee-147">Opprette</span><span class="sxs-lookup"><span data-stu-id="dc6ee-147">Create</span></span> | <span data-ttu-id="dc6ee-148">Oppdatering</span><span class="sxs-lookup"><span data-stu-id="dc6ee-148">Update</span></span> | <span data-ttu-id="dc6ee-149">Delete</span><span class="sxs-lookup"><span data-stu-id="dc6ee-149">Delete</span></span> | <span data-ttu-id="dc6ee-150">Viktige hensyn</span><span class="sxs-lookup"><span data-stu-id="dc6ee-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="dc6ee-151">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="dc6ee-151">Project task</span></span> | <span data-ttu-id="dc6ee-152">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-152">Yes</span></span> | <span data-ttu-id="dc6ee-153">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-153">Yes</span></span> | <span data-ttu-id="dc6ee-154">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-154">Yes</span></span> | <span data-ttu-id="dc6ee-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="dc6ee-155">None</span></span> |
| <span data-ttu-id="dc6ee-156">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="dc6ee-156">Project task dependency</span></span> | <span data-ttu-id="dc6ee-157">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-157">Yes</span></span> | <span data-ttu-id="dc6ee-158">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-158">Yes</span></span> | | <span data-ttu-id="dc6ee-159">Oppføringer for prosjektoppgaveavhengighet oppdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="dc6ee-160">I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="dc6ee-161">Ressurstilordning</span><span class="sxs-lookup"><span data-stu-id="dc6ee-161">Resource assignment</span></span> | <span data-ttu-id="dc6ee-162">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-162">Yes</span></span> | <span data-ttu-id="dc6ee-163">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-163">Yes</span></span> | | <span data-ttu-id="dc6ee-164">Operasjoner med følgende felter støttes ikke: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="dc6ee-165">Ressurstilordningsoppføringer oppdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="dc6ee-166">I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="dc6ee-167">Prosjektsamling</span><span class="sxs-lookup"><span data-stu-id="dc6ee-167">Project bucket</span></span> | <span data-ttu-id="dc6ee-168">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="dc6ee-168">N/A</span></span> | <span data-ttu-id="dc6ee-169">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="dc6ee-169">N/A</span></span> | <span data-ttu-id="dc6ee-170">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="dc6ee-170">N/A</span></span> | <span data-ttu-id="dc6ee-171">Standardsamlingen opprettes ved hjelp av API-en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="dc6ee-172">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="dc6ee-172">Project team member</span></span> | <span data-ttu-id="dc6ee-173">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-173">Yes</span></span> | <span data-ttu-id="dc6ee-174">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-174">Yes</span></span> | <span data-ttu-id="dc6ee-175">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-175">Yes</span></span> | <span data-ttu-id="dc6ee-176">For oppretting bruker du API-en **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="dc6ee-177">Project</span><span class="sxs-lookup"><span data-stu-id="dc6ee-177">Project</span></span> | <span data-ttu-id="dc6ee-178">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-178">Yes</span></span> | <span data-ttu-id="dc6ee-179">Ja</span><span class="sxs-lookup"><span data-stu-id="dc6ee-179">Yes</span></span> | <span data-ttu-id="dc6ee-180">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="dc6ee-180">N/A</span></span> | <span data-ttu-id="dc6ee-181">Operasjoner med følgende felter støttes ikke: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** og **Duration**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="dc6ee-182">Disse API-ene kan kalles med enhetsobjekter som inneholder egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="dc6ee-183">ID-egenskapen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-183">The ID property is optional.</span></span> <span data-ttu-id="dc6ee-184">Hvis den er angitt, prøver systemet å bruke den, og dette fører til et unntak hvis den ikke kan brukes.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="dc6ee-185">Hvis den ikke er angitt, genererer systemet den.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="dc6ee-186">Begrensninger og kjente problemer</span><span class="sxs-lookup"><span data-stu-id="dc6ee-186">Limitations and known issues</span></span>
<span data-ttu-id="dc6ee-187">Nedenfor vises en liste over begrensninger og kjente problemer:</span><span class="sxs-lookup"><span data-stu-id="dc6ee-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="dc6ee-188">API-er for planlegging bare brukes av **brukere med Microsoft Project-lisens.**</span><span class="sxs-lookup"><span data-stu-id="dc6ee-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="dc6ee-189">De kan ikke brukes av følgende:</span><span class="sxs-lookup"><span data-stu-id="dc6ee-189">They can't be used by:</span></span>
    - <span data-ttu-id="dc6ee-190">Applikasjonsbrukere</span><span class="sxs-lookup"><span data-stu-id="dc6ee-190">Application users</span></span>
    - <span data-ttu-id="dc6ee-191">Systembrukere</span><span class="sxs-lookup"><span data-stu-id="dc6ee-191">System users</span></span>
    - <span data-ttu-id="dc6ee-192">Integreringsbrukere</span><span class="sxs-lookup"><span data-stu-id="dc6ee-192">Integration users</span></span>
    - <span data-ttu-id="dc6ee-193">Andre brukere som ikke har den nødvendige lisensen</span><span class="sxs-lookup"><span data-stu-id="dc6ee-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="dc6ee-194">Hvert **OperationSet** kan bare ha maksimalt 100 operasjoner.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="dc6ee-195">Hver bruker kan bare ha maksimalt 10 åpne **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="dc6ee-196">Project Operations støtter for øyeblikket maksimalt 500 oppgaver på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="dc6ee-197">**OperationSet**-feilstatus og -feillogger er ikke tilgjengelige for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="dc6ee-198">API-er for planlegging er i offentlig forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="dc6ee-199">Bruk av disse API-ene i et produksjonsmiljø støttes ikke av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="dc6ee-200">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="dc6ee-200">Sample scenario</span></span>

<span data-ttu-id="dc6ee-201">I dette scenarioet skal du opprette et prosjekt, et teammedlem, fire oppgaver og to ressurstilordninger.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="dc6ee-202">Deretter skal du oppdatere én oppgave, oppdatere prosjektet, slette én oppgave, slette én ressurstilordning og opprette en aktivitetsavhengighet.</span><span class="sxs-lookup"><span data-stu-id="dc6ee-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="dc6ee-203">Flere eksempler</span><span class="sxs-lookup"><span data-stu-id="dc6ee-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
