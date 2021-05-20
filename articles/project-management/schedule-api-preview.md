---
title: Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter
description: Dette emnet inneholder informasjon og eksempler for bruk av API-er for tidsplan.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950816"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="84635-103">Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter</span><span class="sxs-lookup"><span data-stu-id="84635-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="84635-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="84635-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="84635-105">Noen av eller alle funksjonene som er angitt i dette emnet, er tilgjengelig som en del av en forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="84635-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="84635-106">Innholdet i og funksjonaliteten kan endres.</span><span class="sxs-lookup"><span data-stu-id="84635-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="84635-107">Planleggingsenheter</span><span class="sxs-lookup"><span data-stu-id="84635-107">Scheduling entities</span></span>

<span data-ttu-id="84635-108">API-er for planlegging gjør det mulig å utføre operasjoner for oppretting, oppdatering og sletting med **planleggingsenheter**.</span><span class="sxs-lookup"><span data-stu-id="84635-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="84635-109">Disse enhetene administreres via planleggingsmotoren i Project for the web.</span><span class="sxs-lookup"><span data-stu-id="84635-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="84635-110">Oppretting, oppdatering og sletting med **planleggingsenheter** var begrenser i tidligere versjoner av Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="84635-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="84635-111">Tabellen nedenfor viser en fullstendig liste over **planleggingsenhetene**.</span><span class="sxs-lookup"><span data-stu-id="84635-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="84635-112">Enhetsnavn</span><span class="sxs-lookup"><span data-stu-id="84635-112">Entity name</span></span>  | <span data-ttu-id="84635-113">Logisk navn for enhet</span><span class="sxs-lookup"><span data-stu-id="84635-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="84635-114">Project</span><span class="sxs-lookup"><span data-stu-id="84635-114">Project</span></span> | <span data-ttu-id="84635-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="84635-115">msdyn_project</span></span> |
| <span data-ttu-id="84635-116">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="84635-116">Project Task</span></span>  | <span data-ttu-id="84635-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="84635-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="84635-118">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="84635-118">Project Task Dependency</span></span>  | <span data-ttu-id="84635-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="84635-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="84635-120">Ressurstilordning</span><span class="sxs-lookup"><span data-stu-id="84635-120">Resource Assignment</span></span> | <span data-ttu-id="84635-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="84635-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="84635-122">Prosjektsamling</span><span class="sxs-lookup"><span data-stu-id="84635-122">Project Bucket</span></span>  | <span data-ttu-id="84635-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="84635-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="84635-124">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="84635-124">Project Team Member</span></span> | <span data-ttu-id="84635-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="84635-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="84635-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="84635-126">OperationSet</span></span>

<span data-ttu-id="84635-127">OperationSet er et enhetsarbeidsmønster som kan brukes når flere forespørsler som påvirker tidsplanen, må behandles i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="84635-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="84635-128">API-er for planlegging</span><span class="sxs-lookup"><span data-stu-id="84635-128">Schedule APIs</span></span>

<span data-ttu-id="84635-129">Nedenfor vises en liste over gjeldende API-er for planlegging.</span><span class="sxs-lookup"><span data-stu-id="84635-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="84635-130">**msdyn_CreateProjectV1:** Denne API-en kan brukes til å opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="84635-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="84635-131">Prosjektet og standard prosjektsamling opprettes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="84635-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="84635-132">**msdyn_CreateTeamMemberV1:** Denne API-en kan brukes til å opprette et prosjektteammedlem.</span><span class="sxs-lookup"><span data-stu-id="84635-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="84635-133">Teammedlemsoppføringen opprettes umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="84635-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="84635-134">**msdyn_CreateOperationSetV1**: Denne API-en kan brukes til å planlegge flere forespørsler som må utføres i en transaksjon.</span><span class="sxs-lookup"><span data-stu-id="84635-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="84635-135">**msdyn_PSSCreateV1**: Denne API-en kan brukes til å opprette en enhet.</span><span class="sxs-lookup"><span data-stu-id="84635-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="84635-136">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter opprettingsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="84635-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="84635-137">**msdyn_PSSUpdateV1**: Denne API-en kan brukes til å oppdatere en enhet.</span><span class="sxs-lookup"><span data-stu-id="84635-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="84635-138">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter oppdateringsoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="84635-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="84635-139">**msdyn_PSSDeleteV1**: Denne API-en kan brukes til å slette en enhet.</span><span class="sxs-lookup"><span data-stu-id="84635-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="84635-140">Enheten kan være en hvilken som helst av planleggingsenhetene som støtter sletteoperasjonen.</span><span class="sxs-lookup"><span data-stu-id="84635-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="84635-141">**msdyn_ExecuteOperationSetV1**: Denne API-en brukes til å kjøre alle operasjonene i det angitte operasjonssettet.</span><span class="sxs-lookup"><span data-stu-id="84635-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="84635-142">Bruke API-er for tidsplan med OperationSet</span><span class="sxs-lookup"><span data-stu-id="84635-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="84635-143">Ettersom oppføringer med både **CreateProjectV1** og **CreateTeamMemberV1** opprettes umiddelbart, kan ikke disse API-ene brukes direkte i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="84635-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="84635-144">Du kan imidlertid bruke API-en til å opprette nødvendige oppføringer, opprette et **OperationSet** og deretter bruke disse forhåndsopprettede oppføringene i **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="84635-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="84635-145">Støttede operasjoner</span><span class="sxs-lookup"><span data-stu-id="84635-145">Supported operations</span></span>

| <span data-ttu-id="84635-146">Planleggingsenhet</span><span class="sxs-lookup"><span data-stu-id="84635-146">Scheduling entity</span></span> | <span data-ttu-id="84635-147">Opprette</span><span class="sxs-lookup"><span data-stu-id="84635-147">Create</span></span> | <span data-ttu-id="84635-148">Oppdatering</span><span class="sxs-lookup"><span data-stu-id="84635-148">Update</span></span> | <span data-ttu-id="84635-149">Delete</span><span class="sxs-lookup"><span data-stu-id="84635-149">Delete</span></span> | <span data-ttu-id="84635-150">Viktige hensyn</span><span class="sxs-lookup"><span data-stu-id="84635-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="84635-151">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="84635-151">Project task</span></span> | <span data-ttu-id="84635-152">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-152">Yes</span></span> | <span data-ttu-id="84635-153">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-153">Yes</span></span> | <span data-ttu-id="84635-154">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-154">Yes</span></span> | <span data-ttu-id="84635-155">Ingen</span><span class="sxs-lookup"><span data-stu-id="84635-155">None</span></span> |
| <span data-ttu-id="84635-156">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="84635-156">Project task dependency</span></span> | <span data-ttu-id="84635-157">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-157">Yes</span></span> | <span data-ttu-id="84635-158">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-158">Yes</span></span> | | <span data-ttu-id="84635-159">Oppføringer for prosjektoppgaveavhengighet oppdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="84635-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="84635-160">I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="84635-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="84635-161">Ressurstilordning</span><span class="sxs-lookup"><span data-stu-id="84635-161">Resource assignment</span></span> | <span data-ttu-id="84635-162">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-162">Yes</span></span> | <span data-ttu-id="84635-163">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-163">Yes</span></span> | | <span data-ttu-id="84635-164">Operasjoner med følgende felter støttes ikke: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="84635-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="84635-165">Ressurstilordningsoppføringer oppdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="84635-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="84635-166">I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes.</span><span class="sxs-lookup"><span data-stu-id="84635-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="84635-167">Prosjektsamling</span><span class="sxs-lookup"><span data-stu-id="84635-167">Project bucket</span></span> | <span data-ttu-id="84635-168">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84635-168">N/A</span></span> | <span data-ttu-id="84635-169">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84635-169">N/A</span></span> | <span data-ttu-id="84635-170">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84635-170">N/A</span></span> | <span data-ttu-id="84635-171">Standardsamlingen opprettes ved hjelp av API-en **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="84635-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="84635-172">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="84635-172">Project team member</span></span> | <span data-ttu-id="84635-173">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-173">Yes</span></span> | <span data-ttu-id="84635-174">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-174">Yes</span></span> | <span data-ttu-id="84635-175">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-175">Yes</span></span> | <span data-ttu-id="84635-176">For oppretting bruker du API-en **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="84635-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="84635-177">Project</span><span class="sxs-lookup"><span data-stu-id="84635-177">Project</span></span> | <span data-ttu-id="84635-178">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-178">Yes</span></span> | <span data-ttu-id="84635-179">Ja</span><span class="sxs-lookup"><span data-stu-id="84635-179">Yes</span></span> | <span data-ttu-id="84635-180">Ikke tilgjengelig</span><span class="sxs-lookup"><span data-stu-id="84635-180">N/A</span></span> | <span data-ttu-id="84635-181">Operasjoner med følgende felter støttes ikke: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** og **Duration**.</span><span class="sxs-lookup"><span data-stu-id="84635-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="84635-182">Disse API-ene kan kalles med enhetsobjekter som inneholder egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="84635-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="84635-183">ID-egenskapen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="84635-183">The ID property is optional.</span></span> <span data-ttu-id="84635-184">Hvis den er angitt, prøver systemet å bruke den, og dette fører til et unntak hvis den ikke kan brukes.</span><span class="sxs-lookup"><span data-stu-id="84635-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="84635-185">Hvis den ikke er angitt, genererer systemet den.</span><span class="sxs-lookup"><span data-stu-id="84635-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="84635-186">Begrensede felt</span><span class="sxs-lookup"><span data-stu-id="84635-186">Restricted fields</span></span>

<span data-ttu-id="84635-187">Tabellene nedenfor definerer feltene som er begrenset fra **Opprett** og **Rediger.**</span><span class="sxs-lookup"><span data-stu-id="84635-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="84635-188">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="84635-188">Project task</span></span>

| <span data-ttu-id="84635-189">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="84635-189">**Logical name**</span></span>                       | <span data-ttu-id="84635-190">**Kan opprette**</span><span class="sxs-lookup"><span data-stu-id="84635-190">**Can create**</span></span> | <span data-ttu-id="84635-191">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="84635-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="84635-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="84635-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="84635-193">nei</span><span class="sxs-lookup"><span data-stu-id="84635-193">no</span></span>             | <span data-ttu-id="84635-194">nei</span><span class="sxs-lookup"><span data-stu-id="84635-194">no</span></span>               |
| <span data-ttu-id="84635-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="84635-196">nei</span><span class="sxs-lookup"><span data-stu-id="84635-196">no</span></span>             | <span data-ttu-id="84635-197">nei</span><span class="sxs-lookup"><span data-stu-id="84635-197">no</span></span>               |
| <span data-ttu-id="84635-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="84635-198">msdyn_actualend</span></span>                        | <span data-ttu-id="84635-199">nei</span><span class="sxs-lookup"><span data-stu-id="84635-199">no</span></span>             | <span data-ttu-id="84635-200">nei</span><span class="sxs-lookup"><span data-stu-id="84635-200">no</span></span>               |
| <span data-ttu-id="84635-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="84635-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="84635-202">nei</span><span class="sxs-lookup"><span data-stu-id="84635-202">no</span></span>             | <span data-ttu-id="84635-203">nei</span><span class="sxs-lookup"><span data-stu-id="84635-203">no</span></span>               |
| <span data-ttu-id="84635-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="84635-205">nei</span><span class="sxs-lookup"><span data-stu-id="84635-205">no</span></span>             | <span data-ttu-id="84635-206">nei</span><span class="sxs-lookup"><span data-stu-id="84635-206">no</span></span>               |
| <span data-ttu-id="84635-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="84635-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="84635-208">nei</span><span class="sxs-lookup"><span data-stu-id="84635-208">no</span></span>             | <span data-ttu-id="84635-209">nei</span><span class="sxs-lookup"><span data-stu-id="84635-209">no</span></span>               |
| <span data-ttu-id="84635-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="84635-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="84635-211">nei</span><span class="sxs-lookup"><span data-stu-id="84635-211">no</span></span>             | <span data-ttu-id="84635-212">nei</span><span class="sxs-lookup"><span data-stu-id="84635-212">no</span></span>               |
| <span data-ttu-id="84635-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="84635-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="84635-214">nei</span><span class="sxs-lookup"><span data-stu-id="84635-214">no</span></span>             | <span data-ttu-id="84635-215">nei</span><span class="sxs-lookup"><span data-stu-id="84635-215">no</span></span>               |
| <span data-ttu-id="84635-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="84635-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="84635-217">nei</span><span class="sxs-lookup"><span data-stu-id="84635-217">no</span></span>             | <span data-ttu-id="84635-218">nei</span><span class="sxs-lookup"><span data-stu-id="84635-218">no</span></span>               |
| <span data-ttu-id="84635-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="84635-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="84635-220">nei</span><span class="sxs-lookup"><span data-stu-id="84635-220">no</span></span>             | <span data-ttu-id="84635-221">nei</span><span class="sxs-lookup"><span data-stu-id="84635-221">no</span></span>               |
| <span data-ttu-id="84635-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="84635-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="84635-223">nei</span><span class="sxs-lookup"><span data-stu-id="84635-223">no</span></span>             | <span data-ttu-id="84635-224">nei</span><span class="sxs-lookup"><span data-stu-id="84635-224">no</span></span>               |
| <span data-ttu-id="84635-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="84635-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="84635-226">nei</span><span class="sxs-lookup"><span data-stu-id="84635-226">no</span></span>             | <span data-ttu-id="84635-227">nei</span><span class="sxs-lookup"><span data-stu-id="84635-227">no</span></span>               |
| <span data-ttu-id="84635-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="84635-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="84635-229">nei</span><span class="sxs-lookup"><span data-stu-id="84635-229">no</span></span>             | <span data-ttu-id="84635-230">nei</span><span class="sxs-lookup"><span data-stu-id="84635-230">no</span></span>               |
| <span data-ttu-id="84635-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="84635-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="84635-232">nei</span><span class="sxs-lookup"><span data-stu-id="84635-232">no</span></span>             | <span data-ttu-id="84635-233">nei</span><span class="sxs-lookup"><span data-stu-id="84635-233">no</span></span>               |
| <span data-ttu-id="84635-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="84635-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="84635-235">nei</span><span class="sxs-lookup"><span data-stu-id="84635-235">no</span></span>             | <span data-ttu-id="84635-236">nei</span><span class="sxs-lookup"><span data-stu-id="84635-236">no</span></span>               |
| <span data-ttu-id="84635-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="84635-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="84635-238">nei</span><span class="sxs-lookup"><span data-stu-id="84635-238">no</span></span>             | <span data-ttu-id="84635-239">nei</span><span class="sxs-lookup"><span data-stu-id="84635-239">no</span></span>               |
| <span data-ttu-id="84635-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="84635-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="84635-241">nei</span><span class="sxs-lookup"><span data-stu-id="84635-241">no</span></span>             | <span data-ttu-id="84635-242">nei</span><span class="sxs-lookup"><span data-stu-id="84635-242">no</span></span>               |
| <span data-ttu-id="84635-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="84635-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="84635-244">nei</span><span class="sxs-lookup"><span data-stu-id="84635-244">no</span></span>             | <span data-ttu-id="84635-245">nei</span><span class="sxs-lookup"><span data-stu-id="84635-245">no</span></span>               |
| <span data-ttu-id="84635-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="84635-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="84635-247">nei</span><span class="sxs-lookup"><span data-stu-id="84635-247">no</span></span>             | <span data-ttu-id="84635-248">nei</span><span class="sxs-lookup"><span data-stu-id="84635-248">no</span></span>               |
| <span data-ttu-id="84635-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="84635-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="84635-250">nei</span><span class="sxs-lookup"><span data-stu-id="84635-250">no</span></span>             | <span data-ttu-id="84635-251">nei</span><span class="sxs-lookup"><span data-stu-id="84635-251">no</span></span>               |
| <span data-ttu-id="84635-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="84635-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="84635-253">nei</span><span class="sxs-lookup"><span data-stu-id="84635-253">no</span></span>             | <span data-ttu-id="84635-254">nei</span><span class="sxs-lookup"><span data-stu-id="84635-254">no</span></span>               |
| <span data-ttu-id="84635-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="84635-256">nei</span><span class="sxs-lookup"><span data-stu-id="84635-256">no</span></span>             | <span data-ttu-id="84635-257">nei</span><span class="sxs-lookup"><span data-stu-id="84635-257">no</span></span>               |
| <span data-ttu-id="84635-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="84635-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="84635-259">nei</span><span class="sxs-lookup"><span data-stu-id="84635-259">no</span></span>             | <span data-ttu-id="84635-260">nei</span><span class="sxs-lookup"><span data-stu-id="84635-260">no</span></span>               |
| <span data-ttu-id="84635-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="84635-262">nei</span><span class="sxs-lookup"><span data-stu-id="84635-262">no</span></span>             | <span data-ttu-id="84635-263">nei</span><span class="sxs-lookup"><span data-stu-id="84635-263">no</span></span>               |
| <span data-ttu-id="84635-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="84635-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="84635-265">nei</span><span class="sxs-lookup"><span data-stu-id="84635-265">no</span></span>             | <span data-ttu-id="84635-266">nei</span><span class="sxs-lookup"><span data-stu-id="84635-266">no</span></span>               |
| <span data-ttu-id="84635-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="84635-267">msdyn_progress</span></span>                         | <span data-ttu-id="84635-268">nei</span><span class="sxs-lookup"><span data-stu-id="84635-268">no</span></span>             | <span data-ttu-id="84635-269">nei (ja for P4W)</span><span class="sxs-lookup"><span data-stu-id="84635-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="84635-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="84635-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="84635-271">nei</span><span class="sxs-lookup"><span data-stu-id="84635-271">no</span></span>             | <span data-ttu-id="84635-272">nei</span><span class="sxs-lookup"><span data-stu-id="84635-272">no</span></span>               |
| <span data-ttu-id="84635-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="84635-274">nei</span><span class="sxs-lookup"><span data-stu-id="84635-274">no</span></span>             | <span data-ttu-id="84635-275">nei</span><span class="sxs-lookup"><span data-stu-id="84635-275">no</span></span>               |
| <span data-ttu-id="84635-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="84635-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="84635-277">nei</span><span class="sxs-lookup"><span data-stu-id="84635-277">no</span></span>             | <span data-ttu-id="84635-278">nei</span><span class="sxs-lookup"><span data-stu-id="84635-278">no</span></span>               |
| <span data-ttu-id="84635-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="84635-280">nei</span><span class="sxs-lookup"><span data-stu-id="84635-280">no</span></span>             | <span data-ttu-id="84635-281">nei</span><span class="sxs-lookup"><span data-stu-id="84635-281">no</span></span>               |
| <span data-ttu-id="84635-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="84635-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="84635-283">nei</span><span class="sxs-lookup"><span data-stu-id="84635-283">no</span></span>             | <span data-ttu-id="84635-284">nei</span><span class="sxs-lookup"><span data-stu-id="84635-284">no</span></span>               |
| <span data-ttu-id="84635-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="84635-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="84635-286">nei</span><span class="sxs-lookup"><span data-stu-id="84635-286">no</span></span>             | <span data-ttu-id="84635-287">nei</span><span class="sxs-lookup"><span data-stu-id="84635-287">no</span></span>               |
| <span data-ttu-id="84635-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="84635-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="84635-289">nei</span><span class="sxs-lookup"><span data-stu-id="84635-289">no</span></span>             | <span data-ttu-id="84635-290">nei</span><span class="sxs-lookup"><span data-stu-id="84635-290">no</span></span>               |
| <span data-ttu-id="84635-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="84635-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="84635-292">nei</span><span class="sxs-lookup"><span data-stu-id="84635-292">no</span></span>             | <span data-ttu-id="84635-293">nei</span><span class="sxs-lookup"><span data-stu-id="84635-293">no</span></span>               |
| <span data-ttu-id="84635-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="84635-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="84635-295">nei</span><span class="sxs-lookup"><span data-stu-id="84635-295">no</span></span>             | <span data-ttu-id="84635-296">nei</span><span class="sxs-lookup"><span data-stu-id="84635-296">no</span></span>               |
| <span data-ttu-id="84635-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="84635-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="84635-298">nei</span><span class="sxs-lookup"><span data-stu-id="84635-298">no</span></span>             | <span data-ttu-id="84635-299">nei</span><span class="sxs-lookup"><span data-stu-id="84635-299">no</span></span>               |
| <span data-ttu-id="84635-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="84635-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="84635-301">nei</span><span class="sxs-lookup"><span data-stu-id="84635-301">no</span></span>             | <span data-ttu-id="84635-302">nei</span><span class="sxs-lookup"><span data-stu-id="84635-302">no</span></span>               |
| <span data-ttu-id="84635-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="84635-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="84635-304">nei</span><span class="sxs-lookup"><span data-stu-id="84635-304">no</span></span>             | <span data-ttu-id="84635-305">nei</span><span class="sxs-lookup"><span data-stu-id="84635-305">no</span></span>               |
| <span data-ttu-id="84635-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="84635-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="84635-307">nei</span><span class="sxs-lookup"><span data-stu-id="84635-307">no</span></span>             | <span data-ttu-id="84635-308">nei</span><span class="sxs-lookup"><span data-stu-id="84635-308">no</span></span>               |
| <span data-ttu-id="84635-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="84635-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="84635-310">nei</span><span class="sxs-lookup"><span data-stu-id="84635-310">no</span></span>             | <span data-ttu-id="84635-311">nei</span><span class="sxs-lookup"><span data-stu-id="84635-311">no</span></span>               |
| <span data-ttu-id="84635-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="84635-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="84635-313">nei</span><span class="sxs-lookup"><span data-stu-id="84635-313">no</span></span>             | <span data-ttu-id="84635-314">nei</span><span class="sxs-lookup"><span data-stu-id="84635-314">no</span></span>               |
| <span data-ttu-id="84635-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="84635-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="84635-316">nei</span><span class="sxs-lookup"><span data-stu-id="84635-316">no</span></span>             | <span data-ttu-id="84635-317">nei</span><span class="sxs-lookup"><span data-stu-id="84635-317">no</span></span>               |
| <span data-ttu-id="84635-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="84635-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="84635-319">nei</span><span class="sxs-lookup"><span data-stu-id="84635-319">no</span></span>             | <span data-ttu-id="84635-320">nei</span><span class="sxs-lookup"><span data-stu-id="84635-320">no</span></span>               |
| <span data-ttu-id="84635-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="84635-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="84635-322">nei</span><span class="sxs-lookup"><span data-stu-id="84635-322">no</span></span>             | <span data-ttu-id="84635-323">nei</span><span class="sxs-lookup"><span data-stu-id="84635-323">no</span></span>               |
| <span data-ttu-id="84635-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="84635-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="84635-325">nei</span><span class="sxs-lookup"><span data-stu-id="84635-325">no</span></span>             | <span data-ttu-id="84635-326">nei</span><span class="sxs-lookup"><span data-stu-id="84635-326">no</span></span>               |
| <span data-ttu-id="84635-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="84635-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="84635-328">nei</span><span class="sxs-lookup"><span data-stu-id="84635-328">no</span></span>             | <span data-ttu-id="84635-329">nei</span><span class="sxs-lookup"><span data-stu-id="84635-329">no</span></span>               |
| <span data-ttu-id="84635-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="84635-330">msdyn_summary</span></span>                          | <span data-ttu-id="84635-331">nei</span><span class="sxs-lookup"><span data-stu-id="84635-331">no</span></span>             | <span data-ttu-id="84635-332">nei</span><span class="sxs-lookup"><span data-stu-id="84635-332">no</span></span>               |
| <span data-ttu-id="84635-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="84635-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="84635-334">nei</span><span class="sxs-lookup"><span data-stu-id="84635-334">no</span></span>             | <span data-ttu-id="84635-335">nei</span><span class="sxs-lookup"><span data-stu-id="84635-335">no</span></span>               |
| <span data-ttu-id="84635-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="84635-337">nei</span><span class="sxs-lookup"><span data-stu-id="84635-337">no</span></span>             | <span data-ttu-id="84635-338">nei</span><span class="sxs-lookup"><span data-stu-id="84635-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="84635-339">Avhengighet for prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="84635-339">Project task dependency</span></span>

| <span data-ttu-id="84635-340">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="84635-340">**Logical name**</span></span>              | <span data-ttu-id="84635-341">**Kan opprette**</span><span class="sxs-lookup"><span data-stu-id="84635-341">**Can create**</span></span> | <span data-ttu-id="84635-342">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="84635-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="84635-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="84635-343">msdyn_linktype</span></span>                | <span data-ttu-id="84635-344">nei</span><span class="sxs-lookup"><span data-stu-id="84635-344">no</span></span>             | <span data-ttu-id="84635-345">nei</span><span class="sxs-lookup"><span data-stu-id="84635-345">no</span></span>           |
| <span data-ttu-id="84635-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="84635-346">msdyn_linktypename</span></span>            | <span data-ttu-id="84635-347">nei</span><span class="sxs-lookup"><span data-stu-id="84635-347">no</span></span>             | <span data-ttu-id="84635-348">nei</span><span class="sxs-lookup"><span data-stu-id="84635-348">no</span></span>           |
| <span data-ttu-id="84635-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="84635-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="84635-350">ja</span><span class="sxs-lookup"><span data-stu-id="84635-350">yes</span></span>            | <span data-ttu-id="84635-351">nei</span><span class="sxs-lookup"><span data-stu-id="84635-351">no</span></span>           |
| <span data-ttu-id="84635-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="84635-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="84635-353">ja</span><span class="sxs-lookup"><span data-stu-id="84635-353">yes</span></span>            | <span data-ttu-id="84635-354">nei</span><span class="sxs-lookup"><span data-stu-id="84635-354">no</span></span>           |
| <span data-ttu-id="84635-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="84635-355">msdyn_project</span></span>                 | <span data-ttu-id="84635-356">ja</span><span class="sxs-lookup"><span data-stu-id="84635-356">yes</span></span>            | <span data-ttu-id="84635-357">nei</span><span class="sxs-lookup"><span data-stu-id="84635-357">no</span></span>           |
| <span data-ttu-id="84635-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="84635-358">msdyn_projectname</span></span>             | <span data-ttu-id="84635-359">ja</span><span class="sxs-lookup"><span data-stu-id="84635-359">yes</span></span>            | <span data-ttu-id="84635-360">nei</span><span class="sxs-lookup"><span data-stu-id="84635-360">no</span></span>           |
| <span data-ttu-id="84635-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="84635-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="84635-362">ja</span><span class="sxs-lookup"><span data-stu-id="84635-362">yes</span></span>            | <span data-ttu-id="84635-363">nei</span><span class="sxs-lookup"><span data-stu-id="84635-363">no</span></span>           |
| <span data-ttu-id="84635-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="84635-364">msdyn_successortask</span></span>           | <span data-ttu-id="84635-365">ja</span><span class="sxs-lookup"><span data-stu-id="84635-365">yes</span></span>            | <span data-ttu-id="84635-366">nei</span><span class="sxs-lookup"><span data-stu-id="84635-366">no</span></span>           |
| <span data-ttu-id="84635-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="84635-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="84635-368">ja</span><span class="sxs-lookup"><span data-stu-id="84635-368">yes</span></span>            | <span data-ttu-id="84635-369">nei</span><span class="sxs-lookup"><span data-stu-id="84635-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="84635-370">Ressurstilordning</span><span class="sxs-lookup"><span data-stu-id="84635-370">Resource assignment</span></span>

| <span data-ttu-id="84635-371">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="84635-371">**Logical name**</span></span>             | <span data-ttu-id="84635-372">**Kan opprette**</span><span class="sxs-lookup"><span data-stu-id="84635-372">**Can create**</span></span> | <span data-ttu-id="84635-373">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="84635-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="84635-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="84635-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="84635-375">ja</span><span class="sxs-lookup"><span data-stu-id="84635-375">yes</span></span>            | <span data-ttu-id="84635-376">nei</span><span class="sxs-lookup"><span data-stu-id="84635-376">no</span></span>           |
| <span data-ttu-id="84635-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="84635-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="84635-378">ja</span><span class="sxs-lookup"><span data-stu-id="84635-378">yes</span></span>            | <span data-ttu-id="84635-379">nei</span><span class="sxs-lookup"><span data-stu-id="84635-379">no</span></span>           |
| <span data-ttu-id="84635-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="84635-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="84635-381">nei</span><span class="sxs-lookup"><span data-stu-id="84635-381">no</span></span>             | <span data-ttu-id="84635-382">nei</span><span class="sxs-lookup"><span data-stu-id="84635-382">no</span></span>           |
| <span data-ttu-id="84635-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="84635-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="84635-384">nei</span><span class="sxs-lookup"><span data-stu-id="84635-384">no</span></span>             | <span data-ttu-id="84635-385">nei</span><span class="sxs-lookup"><span data-stu-id="84635-385">no</span></span>           |
| <span data-ttu-id="84635-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="84635-386">msdyn_committype</span></span>             | <span data-ttu-id="84635-387">nei</span><span class="sxs-lookup"><span data-stu-id="84635-387">no</span></span>             | <span data-ttu-id="84635-388">nei</span><span class="sxs-lookup"><span data-stu-id="84635-388">no</span></span>           |
| <span data-ttu-id="84635-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="84635-389">msdyn_committypename</span></span>         | <span data-ttu-id="84635-390">nei</span><span class="sxs-lookup"><span data-stu-id="84635-390">no</span></span>             | <span data-ttu-id="84635-391">nei</span><span class="sxs-lookup"><span data-stu-id="84635-391">no</span></span>           |
| <span data-ttu-id="84635-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="84635-392">msdyn_effort</span></span>                 | <span data-ttu-id="84635-393">nei</span><span class="sxs-lookup"><span data-stu-id="84635-393">no</span></span>             | <span data-ttu-id="84635-394">nei</span><span class="sxs-lookup"><span data-stu-id="84635-394">no</span></span>           |
| <span data-ttu-id="84635-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="84635-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="84635-396">nei</span><span class="sxs-lookup"><span data-stu-id="84635-396">no</span></span>             | <span data-ttu-id="84635-397">nei</span><span class="sxs-lookup"><span data-stu-id="84635-397">no</span></span>           |
| <span data-ttu-id="84635-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="84635-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="84635-399">nei</span><span class="sxs-lookup"><span data-stu-id="84635-399">no</span></span>             | <span data-ttu-id="84635-400">nei</span><span class="sxs-lookup"><span data-stu-id="84635-400">no</span></span>           |
| <span data-ttu-id="84635-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="84635-401">msdyn_finish</span></span>                 | <span data-ttu-id="84635-402">nei</span><span class="sxs-lookup"><span data-stu-id="84635-402">no</span></span>             | <span data-ttu-id="84635-403">nei</span><span class="sxs-lookup"><span data-stu-id="84635-403">no</span></span>           |
| <span data-ttu-id="84635-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="84635-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="84635-405">nei</span><span class="sxs-lookup"><span data-stu-id="84635-405">no</span></span>             | <span data-ttu-id="84635-406">nei</span><span class="sxs-lookup"><span data-stu-id="84635-406">no</span></span>           |
| <span data-ttu-id="84635-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="84635-408">nei</span><span class="sxs-lookup"><span data-stu-id="84635-408">no</span></span>             | <span data-ttu-id="84635-409">nei</span><span class="sxs-lookup"><span data-stu-id="84635-409">no</span></span>           |
| <span data-ttu-id="84635-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="84635-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="84635-411">nei</span><span class="sxs-lookup"><span data-stu-id="84635-411">no</span></span>             | <span data-ttu-id="84635-412">nei</span><span class="sxs-lookup"><span data-stu-id="84635-412">no</span></span>           |
| <span data-ttu-id="84635-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="84635-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="84635-414">nei</span><span class="sxs-lookup"><span data-stu-id="84635-414">no</span></span>             | <span data-ttu-id="84635-415">nei</span><span class="sxs-lookup"><span data-stu-id="84635-415">no</span></span>           |
| <span data-ttu-id="84635-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="84635-417">nei</span><span class="sxs-lookup"><span data-stu-id="84635-417">no</span></span>             | <span data-ttu-id="84635-418">nei</span><span class="sxs-lookup"><span data-stu-id="84635-418">no</span></span>           |
| <span data-ttu-id="84635-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="84635-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="84635-420">nei</span><span class="sxs-lookup"><span data-stu-id="84635-420">no</span></span>             | <span data-ttu-id="84635-421">nei</span><span class="sxs-lookup"><span data-stu-id="84635-421">no</span></span>           |
| <span data-ttu-id="84635-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="84635-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="84635-423">nei</span><span class="sxs-lookup"><span data-stu-id="84635-423">no</span></span>             | <span data-ttu-id="84635-424">nei</span><span class="sxs-lookup"><span data-stu-id="84635-424">no</span></span>           |
| <span data-ttu-id="84635-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="84635-425">msdyn_projectid</span></span>              | <span data-ttu-id="84635-426">ja</span><span class="sxs-lookup"><span data-stu-id="84635-426">yes</span></span>            | <span data-ttu-id="84635-427">nei</span><span class="sxs-lookup"><span data-stu-id="84635-427">no</span></span>           |
| <span data-ttu-id="84635-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="84635-428">msdyn_projectidname</span></span>          | <span data-ttu-id="84635-429">nei</span><span class="sxs-lookup"><span data-stu-id="84635-429">no</span></span>             | <span data-ttu-id="84635-430">nei</span><span class="sxs-lookup"><span data-stu-id="84635-430">no</span></span>           |
| <span data-ttu-id="84635-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="84635-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="84635-432">nei</span><span class="sxs-lookup"><span data-stu-id="84635-432">no</span></span>             | <span data-ttu-id="84635-433">nei</span><span class="sxs-lookup"><span data-stu-id="84635-433">no</span></span>           |
| <span data-ttu-id="84635-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="84635-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="84635-435">nei</span><span class="sxs-lookup"><span data-stu-id="84635-435">no</span></span>             | <span data-ttu-id="84635-436">nei</span><span class="sxs-lookup"><span data-stu-id="84635-436">no</span></span>           |
| <span data-ttu-id="84635-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="84635-437">msdyn_start</span></span>                  | <span data-ttu-id="84635-438">nei</span><span class="sxs-lookup"><span data-stu-id="84635-438">no</span></span>             | <span data-ttu-id="84635-439">nei</span><span class="sxs-lookup"><span data-stu-id="84635-439">no</span></span>           |
| <span data-ttu-id="84635-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="84635-440">msdyn_taskid</span></span>                 | <span data-ttu-id="84635-441">nei</span><span class="sxs-lookup"><span data-stu-id="84635-441">no</span></span>             | <span data-ttu-id="84635-442">nei</span><span class="sxs-lookup"><span data-stu-id="84635-442">no</span></span>           |
| <span data-ttu-id="84635-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="84635-443">msdyn_taskidname</span></span>             | <span data-ttu-id="84635-444">nei</span><span class="sxs-lookup"><span data-stu-id="84635-444">no</span></span>             | <span data-ttu-id="84635-445">nei</span><span class="sxs-lookup"><span data-stu-id="84635-445">no</span></span>           |
| <span data-ttu-id="84635-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="84635-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="84635-447">nei</span><span class="sxs-lookup"><span data-stu-id="84635-447">no</span></span>             | <span data-ttu-id="84635-448">nei</span><span class="sxs-lookup"><span data-stu-id="84635-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="84635-449">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="84635-449">Project team member</span></span>

| <span data-ttu-id="84635-450">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="84635-450">**Logical name**</span></span>                                 | <span data-ttu-id="84635-451">**Kan opprette**</span><span class="sxs-lookup"><span data-stu-id="84635-451">**Can create**</span></span> | <span data-ttu-id="84635-452">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="84635-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="84635-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="84635-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="84635-454">nei</span><span class="sxs-lookup"><span data-stu-id="84635-454">no</span></span>             | <span data-ttu-id="84635-455">nei</span><span class="sxs-lookup"><span data-stu-id="84635-455">no</span></span>           |
| <span data-ttu-id="84635-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="84635-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="84635-457">nei</span><span class="sxs-lookup"><span data-stu-id="84635-457">no</span></span>             | <span data-ttu-id="84635-458">nei</span><span class="sxs-lookup"><span data-stu-id="84635-458">no</span></span>           |
| <span data-ttu-id="84635-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="84635-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="84635-460">nei</span><span class="sxs-lookup"><span data-stu-id="84635-460">no</span></span>             | <span data-ttu-id="84635-461">nei</span><span class="sxs-lookup"><span data-stu-id="84635-461">no</span></span>           |
| <span data-ttu-id="84635-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="84635-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="84635-463">nei</span><span class="sxs-lookup"><span data-stu-id="84635-463">no</span></span>             | <span data-ttu-id="84635-464">nei</span><span class="sxs-lookup"><span data-stu-id="84635-464">no</span></span>           |
| <span data-ttu-id="84635-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="84635-465">msdyn_effort</span></span>                                     | <span data-ttu-id="84635-466">nei</span><span class="sxs-lookup"><span data-stu-id="84635-466">no</span></span>             | <span data-ttu-id="84635-467">nei</span><span class="sxs-lookup"><span data-stu-id="84635-467">no</span></span>           |
| <span data-ttu-id="84635-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="84635-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="84635-469">nei</span><span class="sxs-lookup"><span data-stu-id="84635-469">no</span></span>             | <span data-ttu-id="84635-470">nei</span><span class="sxs-lookup"><span data-stu-id="84635-470">no</span></span>           |
| <span data-ttu-id="84635-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="84635-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="84635-472">nei</span><span class="sxs-lookup"><span data-stu-id="84635-472">no</span></span>             | <span data-ttu-id="84635-473">nei</span><span class="sxs-lookup"><span data-stu-id="84635-473">no</span></span>           |
| <span data-ttu-id="84635-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="84635-474">msdyn_finish</span></span>                                     | <span data-ttu-id="84635-475">nei</span><span class="sxs-lookup"><span data-stu-id="84635-475">no</span></span>             | <span data-ttu-id="84635-476">nei</span><span class="sxs-lookup"><span data-stu-id="84635-476">no</span></span>           |
| <span data-ttu-id="84635-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="84635-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="84635-478">nei</span><span class="sxs-lookup"><span data-stu-id="84635-478">no</span></span>             | <span data-ttu-id="84635-479">nei</span><span class="sxs-lookup"><span data-stu-id="84635-479">no</span></span>           |
| <span data-ttu-id="84635-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="84635-480">msdyn_hours</span></span>                                      | <span data-ttu-id="84635-481">nei</span><span class="sxs-lookup"><span data-stu-id="84635-481">no</span></span>             | <span data-ttu-id="84635-482">nei</span><span class="sxs-lookup"><span data-stu-id="84635-482">no</span></span>           |
| <span data-ttu-id="84635-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="84635-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="84635-484">nei</span><span class="sxs-lookup"><span data-stu-id="84635-484">no</span></span>             | <span data-ttu-id="84635-485">nei</span><span class="sxs-lookup"><span data-stu-id="84635-485">no</span></span>           |
| <span data-ttu-id="84635-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="84635-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="84635-487">nei</span><span class="sxs-lookup"><span data-stu-id="84635-487">no</span></span>             | <span data-ttu-id="84635-488">nei</span><span class="sxs-lookup"><span data-stu-id="84635-488">no</span></span>           |
| <span data-ttu-id="84635-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="84635-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="84635-490">nei</span><span class="sxs-lookup"><span data-stu-id="84635-490">no</span></span>             | <span data-ttu-id="84635-491">nei</span><span class="sxs-lookup"><span data-stu-id="84635-491">no</span></span>           |
| <span data-ttu-id="84635-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="84635-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="84635-493">nei</span><span class="sxs-lookup"><span data-stu-id="84635-493">no</span></span>             | <span data-ttu-id="84635-494">nei</span><span class="sxs-lookup"><span data-stu-id="84635-494">no</span></span>           |
| <span data-ttu-id="84635-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="84635-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="84635-496">nei</span><span class="sxs-lookup"><span data-stu-id="84635-496">no</span></span>             | <span data-ttu-id="84635-497">nei</span><span class="sxs-lookup"><span data-stu-id="84635-497">no</span></span>           |
| <span data-ttu-id="84635-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="84635-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="84635-499">nei</span><span class="sxs-lookup"><span data-stu-id="84635-499">no</span></span>             | <span data-ttu-id="84635-500">nei</span><span class="sxs-lookup"><span data-stu-id="84635-500">no</span></span>           |
| <span data-ttu-id="84635-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="84635-501">msdyn_start</span></span>                                      | <span data-ttu-id="84635-502">nei</span><span class="sxs-lookup"><span data-stu-id="84635-502">no</span></span>             | <span data-ttu-id="84635-503">nei</span><span class="sxs-lookup"><span data-stu-id="84635-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="84635-504">Project</span><span class="sxs-lookup"><span data-stu-id="84635-504">Project</span></span>

| <span data-ttu-id="84635-505">**Logisk navn**</span><span class="sxs-lookup"><span data-stu-id="84635-505">**Logical name**</span></span>                       | <span data-ttu-id="84635-506">**Kan opprette**</span><span class="sxs-lookup"><span data-stu-id="84635-506">**Can create**</span></span> | <span data-ttu-id="84635-507">**Kan redigere**</span><span class="sxs-lookup"><span data-stu-id="84635-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="84635-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="84635-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="84635-509">nei</span><span class="sxs-lookup"><span data-stu-id="84635-509">no</span></span>             | <span data-ttu-id="84635-510">nei</span><span class="sxs-lookup"><span data-stu-id="84635-510">no</span></span>           |
| <span data-ttu-id="84635-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="84635-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="84635-512">nei</span><span class="sxs-lookup"><span data-stu-id="84635-512">no</span></span>             | <span data-ttu-id="84635-513">nei</span><span class="sxs-lookup"><span data-stu-id="84635-513">no</span></span>           |
| <span data-ttu-id="84635-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="84635-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="84635-515">nei</span><span class="sxs-lookup"><span data-stu-id="84635-515">no</span></span>             | <span data-ttu-id="84635-516">nei</span><span class="sxs-lookup"><span data-stu-id="84635-516">no</span></span>           |
| <span data-ttu-id="84635-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="84635-518">nei</span><span class="sxs-lookup"><span data-stu-id="84635-518">no</span></span>             | <span data-ttu-id="84635-519">nei</span><span class="sxs-lookup"><span data-stu-id="84635-519">no</span></span>           |
| <span data-ttu-id="84635-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="84635-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="84635-521">nei</span><span class="sxs-lookup"><span data-stu-id="84635-521">no</span></span>             | <span data-ttu-id="84635-522">nei</span><span class="sxs-lookup"><span data-stu-id="84635-522">no</span></span>           |
| <span data-ttu-id="84635-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="84635-524">nei</span><span class="sxs-lookup"><span data-stu-id="84635-524">no</span></span>             | <span data-ttu-id="84635-525">nei</span><span class="sxs-lookup"><span data-stu-id="84635-525">no</span></span>           |
| <span data-ttu-id="84635-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="84635-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="84635-527">ja</span><span class="sxs-lookup"><span data-stu-id="84635-527">yes</span></span>            | <span data-ttu-id="84635-528">nei</span><span class="sxs-lookup"><span data-stu-id="84635-528">no</span></span>           |
| <span data-ttu-id="84635-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="84635-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="84635-530">ja</span><span class="sxs-lookup"><span data-stu-id="84635-530">yes</span></span>            | <span data-ttu-id="84635-531">nei</span><span class="sxs-lookup"><span data-stu-id="84635-531">no</span></span>           |
| <span data-ttu-id="84635-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="84635-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="84635-533">ja</span><span class="sxs-lookup"><span data-stu-id="84635-533">yes</span></span>            | <span data-ttu-id="84635-534">nei</span><span class="sxs-lookup"><span data-stu-id="84635-534">no</span></span>           |
| <span data-ttu-id="84635-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="84635-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="84635-536">nei</span><span class="sxs-lookup"><span data-stu-id="84635-536">no</span></span>             | <span data-ttu-id="84635-537">nei</span><span class="sxs-lookup"><span data-stu-id="84635-537">no</span></span>           |
| <span data-ttu-id="84635-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="84635-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="84635-539">nei</span><span class="sxs-lookup"><span data-stu-id="84635-539">no</span></span>             | <span data-ttu-id="84635-540">nei</span><span class="sxs-lookup"><span data-stu-id="84635-540">no</span></span>           |
| <span data-ttu-id="84635-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="84635-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="84635-542">nei</span><span class="sxs-lookup"><span data-stu-id="84635-542">no</span></span>             | <span data-ttu-id="84635-543">nei</span><span class="sxs-lookup"><span data-stu-id="84635-543">no</span></span>           |
| <span data-ttu-id="84635-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="84635-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="84635-545">nei</span><span class="sxs-lookup"><span data-stu-id="84635-545">no</span></span>             | <span data-ttu-id="84635-546">nei</span><span class="sxs-lookup"><span data-stu-id="84635-546">no</span></span>           |
| <span data-ttu-id="84635-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="84635-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="84635-548">nei</span><span class="sxs-lookup"><span data-stu-id="84635-548">no</span></span>             | <span data-ttu-id="84635-549">nei</span><span class="sxs-lookup"><span data-stu-id="84635-549">no</span></span>           |
| <span data-ttu-id="84635-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="84635-550">msdyn_duration</span></span>                         | <span data-ttu-id="84635-551">nei</span><span class="sxs-lookup"><span data-stu-id="84635-551">no</span></span>             | <span data-ttu-id="84635-552">nei</span><span class="sxs-lookup"><span data-stu-id="84635-552">no</span></span>           |
| <span data-ttu-id="84635-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="84635-553">msdyn_effort</span></span>                           | <span data-ttu-id="84635-554">nei</span><span class="sxs-lookup"><span data-stu-id="84635-554">no</span></span>             | <span data-ttu-id="84635-555">nei</span><span class="sxs-lookup"><span data-stu-id="84635-555">no</span></span>           |
| <span data-ttu-id="84635-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="84635-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="84635-557">nei</span><span class="sxs-lookup"><span data-stu-id="84635-557">no</span></span>             | <span data-ttu-id="84635-558">nei</span><span class="sxs-lookup"><span data-stu-id="84635-558">no</span></span>           |
| <span data-ttu-id="84635-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="84635-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="84635-560">nei</span><span class="sxs-lookup"><span data-stu-id="84635-560">no</span></span>             | <span data-ttu-id="84635-561">nei</span><span class="sxs-lookup"><span data-stu-id="84635-561">no</span></span>           |
| <span data-ttu-id="84635-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="84635-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="84635-563">nei</span><span class="sxs-lookup"><span data-stu-id="84635-563">no</span></span>             | <span data-ttu-id="84635-564">nei</span><span class="sxs-lookup"><span data-stu-id="84635-564">no</span></span>           |
| <span data-ttu-id="84635-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="84635-565">msdyn_finish</span></span>                           | <span data-ttu-id="84635-566">ja</span><span class="sxs-lookup"><span data-stu-id="84635-566">yes</span></span>            | <span data-ttu-id="84635-567">ja</span><span class="sxs-lookup"><span data-stu-id="84635-567">yes</span></span>          |
| <span data-ttu-id="84635-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="84635-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="84635-569">nei</span><span class="sxs-lookup"><span data-stu-id="84635-569">no</span></span>             | <span data-ttu-id="84635-570">nei</span><span class="sxs-lookup"><span data-stu-id="84635-570">no</span></span>           |
| <span data-ttu-id="84635-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="84635-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="84635-572">nei</span><span class="sxs-lookup"><span data-stu-id="84635-572">no</span></span>             | <span data-ttu-id="84635-573">nei</span><span class="sxs-lookup"><span data-stu-id="84635-573">no</span></span>           |
| <span data-ttu-id="84635-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="84635-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="84635-575">nei</span><span class="sxs-lookup"><span data-stu-id="84635-575">no</span></span>             | <span data-ttu-id="84635-576">nei</span><span class="sxs-lookup"><span data-stu-id="84635-576">no</span></span>           |
| <span data-ttu-id="84635-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="84635-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="84635-578">nei</span><span class="sxs-lookup"><span data-stu-id="84635-578">no</span></span>             | <span data-ttu-id="84635-579">nei</span><span class="sxs-lookup"><span data-stu-id="84635-579">no</span></span>           |
| <span data-ttu-id="84635-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="84635-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="84635-581">nei</span><span class="sxs-lookup"><span data-stu-id="84635-581">no</span></span>             | <span data-ttu-id="84635-582">nei</span><span class="sxs-lookup"><span data-stu-id="84635-582">no</span></span>           |
| <span data-ttu-id="84635-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="84635-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="84635-584">nei</span><span class="sxs-lookup"><span data-stu-id="84635-584">no</span></span>             | <span data-ttu-id="84635-585">nei</span><span class="sxs-lookup"><span data-stu-id="84635-585">no</span></span>           |
| <span data-ttu-id="84635-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="84635-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="84635-587">nei</span><span class="sxs-lookup"><span data-stu-id="84635-587">no</span></span>             | <span data-ttu-id="84635-588">nei</span><span class="sxs-lookup"><span data-stu-id="84635-588">no</span></span>           |
| <span data-ttu-id="84635-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="84635-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="84635-590">nei</span><span class="sxs-lookup"><span data-stu-id="84635-590">no</span></span>             | <span data-ttu-id="84635-591">nei</span><span class="sxs-lookup"><span data-stu-id="84635-591">no</span></span>           |
| <span data-ttu-id="84635-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="84635-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="84635-593">nei</span><span class="sxs-lookup"><span data-stu-id="84635-593">no</span></span>             | <span data-ttu-id="84635-594">nei</span><span class="sxs-lookup"><span data-stu-id="84635-594">no</span></span>           |
| <span data-ttu-id="84635-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="84635-596">nei</span><span class="sxs-lookup"><span data-stu-id="84635-596">no</span></span>             | <span data-ttu-id="84635-597">nei</span><span class="sxs-lookup"><span data-stu-id="84635-597">no</span></span>           |
| <span data-ttu-id="84635-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="84635-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="84635-599">nei</span><span class="sxs-lookup"><span data-stu-id="84635-599">no</span></span>             | <span data-ttu-id="84635-600">nei</span><span class="sxs-lookup"><span data-stu-id="84635-600">no</span></span>           |
| <span data-ttu-id="84635-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="84635-602">nei</span><span class="sxs-lookup"><span data-stu-id="84635-602">no</span></span>             | <span data-ttu-id="84635-603">nei</span><span class="sxs-lookup"><span data-stu-id="84635-603">no</span></span>           |
| <span data-ttu-id="84635-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="84635-604">msdyn_progress</span></span>                         | <span data-ttu-id="84635-605">nei</span><span class="sxs-lookup"><span data-stu-id="84635-605">no</span></span>             | <span data-ttu-id="84635-606">nei</span><span class="sxs-lookup"><span data-stu-id="84635-606">no</span></span>           |
| <span data-ttu-id="84635-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="84635-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="84635-608">nei</span><span class="sxs-lookup"><span data-stu-id="84635-608">no</span></span>             | <span data-ttu-id="84635-609">nei</span><span class="sxs-lookup"><span data-stu-id="84635-609">no</span></span>           |
| <span data-ttu-id="84635-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="84635-611">nei</span><span class="sxs-lookup"><span data-stu-id="84635-611">no</span></span>             | <span data-ttu-id="84635-612">nei</span><span class="sxs-lookup"><span data-stu-id="84635-612">no</span></span>           |
| <span data-ttu-id="84635-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="84635-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="84635-614">nei</span><span class="sxs-lookup"><span data-stu-id="84635-614">no</span></span>             | <span data-ttu-id="84635-615">nei</span><span class="sxs-lookup"><span data-stu-id="84635-615">no</span></span>           |
| <span data-ttu-id="84635-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="84635-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="84635-617">nei</span><span class="sxs-lookup"><span data-stu-id="84635-617">no</span></span>             | <span data-ttu-id="84635-618">nei</span><span class="sxs-lookup"><span data-stu-id="84635-618">no</span></span>           |
| <span data-ttu-id="84635-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="84635-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="84635-620">nei</span><span class="sxs-lookup"><span data-stu-id="84635-620">no</span></span>             | <span data-ttu-id="84635-621">nei</span><span class="sxs-lookup"><span data-stu-id="84635-621">no</span></span>           |
| <span data-ttu-id="84635-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="84635-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="84635-623">nei</span><span class="sxs-lookup"><span data-stu-id="84635-623">no</span></span>             | <span data-ttu-id="84635-624">nei</span><span class="sxs-lookup"><span data-stu-id="84635-624">no</span></span>           |
| <span data-ttu-id="84635-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="84635-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="84635-626">nei</span><span class="sxs-lookup"><span data-stu-id="84635-626">no</span></span>             | <span data-ttu-id="84635-627">nei</span><span class="sxs-lookup"><span data-stu-id="84635-627">no</span></span>           |
| <span data-ttu-id="84635-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="84635-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="84635-629">nei</span><span class="sxs-lookup"><span data-stu-id="84635-629">no</span></span>             | <span data-ttu-id="84635-630">nei</span><span class="sxs-lookup"><span data-stu-id="84635-630">no</span></span>           |
| <span data-ttu-id="84635-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="84635-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="84635-632">nei</span><span class="sxs-lookup"><span data-stu-id="84635-632">no</span></span>             | <span data-ttu-id="84635-633">nei</span><span class="sxs-lookup"><span data-stu-id="84635-633">no</span></span>           |
| <span data-ttu-id="84635-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="84635-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="84635-635">nei</span><span class="sxs-lookup"><span data-stu-id="84635-635">no</span></span>             | <span data-ttu-id="84635-636">nei</span><span class="sxs-lookup"><span data-stu-id="84635-636">no</span></span>           |
| <span data-ttu-id="84635-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="84635-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="84635-638">nei</span><span class="sxs-lookup"><span data-stu-id="84635-638">no</span></span>             | <span data-ttu-id="84635-639">nei</span><span class="sxs-lookup"><span data-stu-id="84635-639">no</span></span>           |
| <span data-ttu-id="84635-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="84635-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="84635-641">nei</span><span class="sxs-lookup"><span data-stu-id="84635-641">no</span></span>             | <span data-ttu-id="84635-642">nei</span><span class="sxs-lookup"><span data-stu-id="84635-642">no</span></span>           |
| <span data-ttu-id="84635-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="84635-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="84635-644">nei</span><span class="sxs-lookup"><span data-stu-id="84635-644">no</span></span>             | <span data-ttu-id="84635-645">nei</span><span class="sxs-lookup"><span data-stu-id="84635-645">no</span></span>           |
| <span data-ttu-id="84635-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="84635-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="84635-647">nei</span><span class="sxs-lookup"><span data-stu-id="84635-647">no</span></span>             | <span data-ttu-id="84635-648">nei</span><span class="sxs-lookup"><span data-stu-id="84635-648">no</span></span>           |
| <span data-ttu-id="84635-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="84635-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="84635-650">nei</span><span class="sxs-lookup"><span data-stu-id="84635-650">no</span></span>             | <span data-ttu-id="84635-651">nei</span><span class="sxs-lookup"><span data-stu-id="84635-651">no</span></span>           |
| <span data-ttu-id="84635-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="84635-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="84635-653">nei</span><span class="sxs-lookup"><span data-stu-id="84635-653">no</span></span>             | <span data-ttu-id="84635-654">nei</span><span class="sxs-lookup"><span data-stu-id="84635-654">no</span></span>           |
| <span data-ttu-id="84635-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="84635-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="84635-656">nei</span><span class="sxs-lookup"><span data-stu-id="84635-656">no</span></span>             | <span data-ttu-id="84635-657">nei</span><span class="sxs-lookup"><span data-stu-id="84635-657">no</span></span>           |
| <span data-ttu-id="84635-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="84635-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="84635-659">nei</span><span class="sxs-lookup"><span data-stu-id="84635-659">no</span></span>             | <span data-ttu-id="84635-660">nei</span><span class="sxs-lookup"><span data-stu-id="84635-660">no</span></span>           |
| <span data-ttu-id="84635-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="84635-662">nei</span><span class="sxs-lookup"><span data-stu-id="84635-662">no</span></span>             | <span data-ttu-id="84635-663">nei</span><span class="sxs-lookup"><span data-stu-id="84635-663">no</span></span>           |
| <span data-ttu-id="84635-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="84635-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="84635-665">nei</span><span class="sxs-lookup"><span data-stu-id="84635-665">no</span></span>             | <span data-ttu-id="84635-666">nei</span><span class="sxs-lookup"><span data-stu-id="84635-666">no</span></span>           |
| <span data-ttu-id="84635-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="84635-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="84635-668">nei</span><span class="sxs-lookup"><span data-stu-id="84635-668">no</span></span>             | <span data-ttu-id="84635-669">nei</span><span class="sxs-lookup"><span data-stu-id="84635-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="84635-670">Begrensninger og kjente problemer</span><span class="sxs-lookup"><span data-stu-id="84635-670">Limitations and known issues</span></span>
<span data-ttu-id="84635-671">Nedenfor vises en liste over begrensninger og kjente problemer:</span><span class="sxs-lookup"><span data-stu-id="84635-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="84635-672">API-er for planlegging bare brukes av **brukere med Microsoft Project-lisens.**</span><span class="sxs-lookup"><span data-stu-id="84635-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="84635-673">De kan ikke brukes av følgende:</span><span class="sxs-lookup"><span data-stu-id="84635-673">They can't be used by:</span></span>
    - <span data-ttu-id="84635-674">Applikasjonsbrukere</span><span class="sxs-lookup"><span data-stu-id="84635-674">Application users</span></span>
    - <span data-ttu-id="84635-675">Systembrukere</span><span class="sxs-lookup"><span data-stu-id="84635-675">System users</span></span>
    - <span data-ttu-id="84635-676">Integreringsbrukere</span><span class="sxs-lookup"><span data-stu-id="84635-676">Integration users</span></span>
    - <span data-ttu-id="84635-677">Andre brukere som ikke har den nødvendige lisensen</span><span class="sxs-lookup"><span data-stu-id="84635-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="84635-678">Hvert **OperationSet** kan bare ha maksimalt 100 operasjoner.</span><span class="sxs-lookup"><span data-stu-id="84635-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="84635-679">Hver bruker kan bare ha maksimalt 10 åpne **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="84635-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="84635-680">Project Operations støtter for øyeblikket maksimalt 500 oppgaver på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="84635-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="84635-681">**OperationSet**-feilstatus og -feillogger er ikke tilgjengelige for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="84635-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="84635-682">API-er for planlegging er i offentlig forhåndsversjon.</span><span class="sxs-lookup"><span data-stu-id="84635-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="84635-683">Bruk av disse API-ene i et produksjonsmiljø støttes ikke av Microsoft.</span><span class="sxs-lookup"><span data-stu-id="84635-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="84635-684">Begrensninger og grenser for prosjekter og oppgaver</span><span class="sxs-lookup"><span data-stu-id="84635-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="84635-685">Feilbehandling</span><span class="sxs-lookup"><span data-stu-id="84635-685">Error handling</span></span>

   - <span data-ttu-id="84635-686">Hvis du vil se gjennom feil som genereres fra operasjonssettene, går du til **Innstillinger** \> **Planlegg integrasjon** \> **Operasjonssett**.</span><span class="sxs-lookup"><span data-stu-id="84635-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="84635-687">Hvis du vil se gjennom feil som genereres fra prosjektplanleggingstjenesten, går du til **Innstillinger** \> **Planlegg integrasjon** \> **PSS-feillogger**.</span><span class="sxs-lookup"><span data-stu-id="84635-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="84635-688">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="84635-688">Sample scenario</span></span>

<span data-ttu-id="84635-689">I dette scenarioet skal du opprette et prosjekt, et teammedlem, fire oppgaver og to ressurstilordninger.</span><span class="sxs-lookup"><span data-stu-id="84635-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="84635-690">Deretter skal du oppdatere én oppgave, oppdatere prosjektet, slette én oppgave, slette én ressurstilordning og opprette en aktivitetsavhengighet.</span><span class="sxs-lookup"><span data-stu-id="84635-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="84635-691">Flere eksempler</span><span class="sxs-lookup"><span data-stu-id="84635-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
