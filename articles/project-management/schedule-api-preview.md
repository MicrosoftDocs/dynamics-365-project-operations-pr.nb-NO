---
title: Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter
description: Denne artikkelen inneholder informasjon om og eksempler for bruk av API-er for prosjektplan.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ada06186121d41edddaa06f747b3e1687c303928
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929226"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_



## <a name="scheduling-entities"></a>Planleggingsenheter

API-er for prosjektplan gir mulighet til å utføre operasjoner for oppretting, oppdatering og sletting med **planleggingsenheter**. Disse enhetene administreres via planleggingsmotoren i Project for the web. Oppretting, oppdatering og sletting med **planleggingsenheter** var begrenser i tidligere versjoner av Dynamics 365 Project Operations.

Tabellen nedenfor viser en fullstendig liste over prosjekttidsplanens enheter.

| Enhetsnavn  | Logisk navn for enhet |
| --- | --- |
| Project | msdyn_project |
| Prosjektoppgave  | msdyn_projecttask  |
| Avhengighet for prosjektoppgaver  | msdyn_projecttaskdependency  |
| Ressurstilordning | msdyn_resourceassignment |
| Prosjektsamling  | msdyn_projectbucket |
| Prosjektteammedlem | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet er et enhetsarbeidsmønster som kan brukes når flere forespørsler som påvirker tidsplanen, må behandles i en transaksjon.

## <a name="project-schedule-apis"></a>API-er for prosjektplan

Nedenfor vises en liste over gjeldende API-er for prosjektplan.

- **msdyn_CreateProjectV1:** Denne API-en kan brukes til å opprette et prosjekt. Prosjektet og standard prosjektsamling opprettes umiddelbart.
- **msdyn_CreateTeamMemberV1:** Denne API-en kan brukes til å opprette et prosjektteammedlem. Teammedlemsoppføringen opprettes umiddelbart.
- **msdyn_CreateOperationSetV1**: Denne API-en kan brukes til å planlegge flere forespørsler som må utføres i en transaksjon.
- **msdyn_PSSCreateV1**: Denne API-en kan brukes til å opprette en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter opprettingsoperasjonen.
- **msdyn_PSSUpdateV1**: Denne API-en kan brukes til å oppdatere en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter oppdateringsoperasjonen.
- **msdyn_PSSDeleteV1**: Denne API-en kan brukes til å slette en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter sletteoperasjonen.
- **msdyn_ExecuteOperationSetV1**: Denne API-en brukes til å kjøre alle operasjonene i det angitte operasjonssettet.

## <a name="using-project-schedule-apis-with-operationset"></a>Bruk av API-er for prosjektplan med OperationSet

Ettersom oppføringer med både **CreateProjectV1** og **CreateTeamMemberV1** opprettes umiddelbart, kan ikke disse API-ene brukes direkte i **OperationSet**. Du kan imidlertid bruke API-en til å opprette nødvendige oppføringer, opprette et **OperationSet** og deretter bruke disse forhåndsopprettede oppføringene i **OperationSet**.

## <a name="supported-operations"></a>Støttede operasjoner

| Planleggingsenhet | Opprette | Oppdater | Delete | Viktige hensyn |
| --- | --- | --- | --- | --- |
Prosjektoppgave | Ja | Ja | Ja | Feltene **Progress**, **EffortCompleted** og **EffortRemaining** kan redigeres i Project for the Web, men de kan ikke redigeres i Project Operations.  |
| Avhengighet for prosjektoppgaver | Ja |  | Ja | Oppføringer for prosjektoppgaveavhengighet oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes. |
| Ressurstilordning | Ja | Ja | | Operasjoner med følgende felter støttes ikke: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**. Ressurstilordningsoppføringer oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes. |
| Prosjektsamling | Ja | Ja | Ja | Standardsamlingen opprettes ved hjelp av API-en **CreateProjectV1**. Støtte for oppretting og sletting av prosjektsamlinger ble lagt til i oppdateringsversjon 16. |
| Prosjektteammedlem | Ja | Ja | Ja | For oppretting bruker du API-en **CreateTeamMemberV1**. |
| Project | Ja | Ja |  | Operasjoner med følgende felter støttes ikke: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** og **Duration**. |

Disse API-ene kan kalles med enhetsobjekter som inneholder egendefinerte felt.

ID-egenskapen er valgfri. Hvis den er angitt, prøver systemet å bruke den, og dette fører til et unntak hvis den ikke kan brukes. Hvis den ikke er angitt, genererer systemet den.

## <a name="restricted-fields"></a>Begrensede felt

Tabellene nedenfor definerer feltene som er begrenset fra **Opprett** og **Rediger**.

### <a name="project-task"></a>Prosjektoppgave

| Logisk navn                           | Kan opprette     | Kan redigere         |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | No             | No               |
| msdyn_actualcost_base                  | No             | No               |
| msdyn_actualend                        | No             | No               |
| msdyn_actualsales                      | No             | No               |
| msdyn_actualsales_base                 | No             | No               |
| msdyn_actualstart                      | No             | No               |
| msdyn_costatcompleteestimate           | No             | No               |
| msdyn_costatcompleteestimate_base      | No             | No               |
| msdyn_costconsumptionpercentage        | No             | No               |
| msdyn_effortcompleted                  | Nei (ja for Prosjekt)             | Nei (ja for Prosjekt)               |
| msdyn_effortremaining                  | Nei (ja for Prosjekt)              | Nei (ja for Prosjekt)                |
| msdyn_effortestimateatcomplete         | No             | No               |
| msdyn_iscritical                       | No             | No               |
| msdyn_iscriticalname                   | No             | No               |
| msdyn_ismanual                         | No             | No               |
| msdyn_ismanualname                     | No             | No               |
| msdyn_ismilestone                      | No             | No               |
| msdyn_ismilestonename                  | No             | No               |
| msdyn_LinkStatus                       | No             | No               |
| msdyn_linkstatusname                   | No             | No               |
| msdyn_msprojectclientid                | No             | No               |
| msdyn_plannedcost                      | No             | No               |
| msdyn_plannedcost_base                 | No             | No               |
| msdyn_plannedsales                     | No             | No               |
| msdyn_plannedsales_base                | No             | No               |
| msdyn_pluginprocessingdata             | No             | No               |
| msdyn_progress                         | Nei (ja for Prosjekt)             | Nei (ja for Prosjekt) |
| msdyn_remainingcost                    | No             | No               |
| msdyn_remainingcost_base               | No             | No               |
| msdyn_remainingsales                   | No             | No               |
| msdyn_remainingsales_base              | No             | No               |
| msdyn_requestedhours                   | No             | No               |
| msdyn_resourcecategory                 | No             | No               |
| msdyn_resourcecategoryname             | No             | No               |
| msdyn_resourceorganizationalunitid     | No             | No               |
| msdyn_resourceorganizationalunitidname | No             | No               |
| msdyn_salesconsumptionpercentage       | No             | No               |
| msdyn_salesestimateatcomplete          | No             | No               |
| msdyn_salesestimateatcomplete_base     | No             | No               |
| msdyn_salesvariance                    | No             | No               |
| msdyn_salesvariance_base               | No             | No               |
| msdyn_scheduleddurationminutes         | No             | No               |
| msdyn_scheduledend                     | No             | No               |
| msdyn_scheduledstart                   | No             | No               |
| msdyn_schedulevariance                 | No             | No               |
| msdyn_skipupdateestimateline           | No             | No               |
| msdyn_skipupdateestimatelinename       | No             | No               |
| msdyn_summary                          | No             | No               |
| msdyn_varianceofcost                   | No             | No               |
| msdyn_varianceofcost_base              | No             | No               |

### <a name="project-task-dependency"></a>Avhengighet for prosjektoppgaver

| Logisk navn                  | Kan opprette     | Kan redigere     |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | No             | No           |
| msdyn_linktypename            | No             | No           |
| msdyn_predecessortask         | Ja            | No           |
| msdyn_predecessortaskname     | Ja            | No           |
| msdyn_project                 | Ja            | No           |
| msdyn_projectname             | Ja            | No           |
| msdyn_projecttaskdependencyid | Ja            | No           |
| msdyn_successortask           | Ja            | No           |
| msdyn_successortaskname       | Ja            | No           |

### <a name="resource-assignment"></a>Ressurstilordning

| Logisk navn                 | Kan opprette     | Kan redigere     |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | Ja            | No           |
| msdyn_bookableresourceidname | Ja            | No           |
| msdyn_bookingstatusid        | No             | No           |
| msdyn_bookingstatusidname    | No             | No           |
| msdyn_committype             | No             | No           |
| msdyn_committypename         | No             | No           |
| msdyn_effort                 | No             | No           |
| msdyn_effortcompleted        | No             | No           |
| msdyn_effortremaining        | No             | No           |
| msdyn_finish                 | No             | No           |
| msdyn_plannedcost            | No             | No           |
| msdyn_plannedcost_base       | No             | No           |
| msdyn_plannedcostcontour     | No             | No           |
| msdyn_plannedsales           | No             | No           |
| msdyn_plannedsales_base      | No             | No           |
| msdyn_plannedsalescontour    | No             | No           |
| msdyn_plannedwork            | No             | No           |
| msdyn_projectid              | Ja            | No           |
| msdyn_projectidname          | No             | No           |
| msdyn_projectteamid          | No             | No           |
| msdyn_projectteamidname      | No             | No           |
| msdyn_start                  | No             | No           |
| msdyn_taskid                 | No             | No           |
| msdyn_taskidname             | No             | No           |
| msdyn_userresourceid         | No             | No           |

### <a name="project-team-member"></a>Prosjektteammedlem

| Logisk navn                                     | Kan opprette     | Kan redigere     |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | No             | No           |
| msdyn_creategenericteammemberwithrequirementname | No             | No           |
| msdyn_deletestatus                               | No             | No           |
| msdyn_deletestatusname                           | No             | No           |
| msdyn_effort                                     | No             | No           |
| msdyn_effortcompleted                            | No             | No           |
| msdyn_effortremaining                            | No             | No           |
| msdyn_finish                                     | No             | No           |
| msdyn_hardbookedhours                            | No             | No           |
| msdyn_hours                                      | No             | No           |
| msdyn_markedfordeletiontimer                     | No             | No           |
| msdyn_markedfordeletiontimestamp                 | No             | No           |
| msdyn_msprojectclientid                          | No             | No           |
| msdyn_percentage                                 | No             | No           |
| msdyn_requiredhours                              | No             | No           |
| msdyn_softbookedhours                            | No             | No           |
| msdyn_start                                      | No             | No           |

### <a name="project"></a>Project

| Logisk navn                           | Kan opprette     | Kan redigere     |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | No             | No           |
| msdyn_actualexpensecost_base           | No             | No           |
| msdyn_actuallaborcost                  | No             | No           |
| msdyn_actuallaborcost_base             | No             | No           |
| msdyn_actualsales                      | No             | No           |
| msdyn_actualsales_base                 | No             | No           |
| msdyn_contractlineproject              | Ja            | No           |
| msdyn_contractorganizationalunitid     | Ja            | No           |
| msdyn_contractorganizationalunitidname | Ja            | No           |
| msdyn_costconsumption                  | No             | No           |
| msdyn_costestimateatcomplete           | No             | No           |
| msdyn_costestimateatcomplete_base      | No             | No           |
| msdyn_costvariance                     | No             | No           |
| msdyn_costvariance_base                | No             | No           |
| msdyn_duration                         | No             | No           |
| msdyn_effort                           | No             | No           |
| msdyn_effortcompleted                  | No             | No           |
| msdyn_effortestimateatcompleteeac      | No             | No           |
| msdyn_effortremaining                  | No             | No           |
| msdyn_finish                           | Ja            | Ja          |
| msdyn_globalrevisiontoken              | No             | No           |
| msdyn_islinkedtomsprojectclient        | No             | No           |
| msdyn_islinkedtomsprojectclientname    | No             | No           |
| msdyn_linkeddocumenturl                | No             | No           |
| msdyn_msprojectdocument                | No             | No           |
| msdyn_msprojectdocumentname            | No             | No           |
| msdyn_plannedexpensecost               | No             | No           |
| msdyn_plannedexpensecost_base          | No             | No           |
| msdyn_plannedlaborcost                 | No             | No           |
| msdyn_plannedlaborcost_base            | No             | No           |
| msdyn_plannedsales                     | No             | No           |
| msdyn_plannedsales_base                | No             | No           |
| msdyn_progress                         | No             | No           |
| msdyn_remainingcost                    | No             | No           |
| msdyn_remainingcost_base               | No             | No           |
| msdyn_remainingsales                   | No             | No           |
| msdyn_remainingsales_base              | No             | No           |
| msdyn_replaylogheader                  | No             | No           |
| msdyn_salesconsumption                 | No             | No           |
| msdyn_salesestimateatcompleteeac       | No             | No           |
| msdyn_salesestimateatcompleteeac_base  | No             | No           |
| msdyn_salesvariance                    | No             | No           |
| msdyn_salesvariance_base               | No             | No           |
| msdyn_scheduleperformance              | No             | No           |
| msdyn_scheduleperformancename          | No             | No           |
| msdyn_schedulevariance                 | No             | No           |
| msdyn_taskearlieststart                | No             | No           |
| msdyn_teamsize                         | No             | No           |
| msdyn_teamsize_date                    | No             | No           |
| msdyn_teamsize_state                   | No             | No           |
| msdyn_totalactualcost                  | No             | No           |
| msdyn_totalactualcost_base             | No             | No           |
| msdyn_totalplannedcost                 | No             | No           |
| msdyn_totalplannedcost_base            | No             | No           |

### <a name="project-bucket"></a>Prosjektsamling

| Logisk navn          | Kan opprette      | Kan redigere     |
|-----------------------|-----------------|--------------|
| msdyn_displayorder    | Ja             | No           |
| msdyn_name            | Ja             | Ja          |
| msdyn_project         | Ja             | No           |
| msdyn_projectbucketid | Ja             | No           |

## <a name="limitations-and-known-issues"></a>Begrensninger og kjente problemer
Nedenfor vises en liste over begrensninger og kjente problemer:

- API-er for prosjektplan kan bare brukes av **brukere med Microsoft Project-lisens**. De kan ikke brukes av følgende:

    - Applikasjonsbrukere
    - Systembrukere
    - Integreringsbrukere
    - Andre brukere som ikke har den nødvendige lisensen

- Hvert **OperationSet** kan bare ha maksimalt 100 operasjoner.
- Hver bruker kan bare ha maksimalt 10 åpne **OperationSets**.
- Project Operations støtter for øyeblikket maksimalt 500 oppgaver på et prosjekt.
- **OperationSet**-feilstatus og -feillogger er ikke tilgjengelige for øyeblikket.
- [Begrensninger og grenser for prosjekter og oppgaver](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Feilbehandling

- Hvis du vil se gjennom feil som genereres fra operasjonssettene, går du til **Innstillinger** \> **Planlegg integrasjon** \> **Operasjonssett**.
- Hvis du vil se gjennom feil som genereres fra prosjektplantjenesten, går du til **Innstilling** \> **Planlegg integrering** \> **PSS-feillogger**.

## <a name="sample-scenario"></a>Eksempelscenario

I dette scenarioet skal du opprette et prosjekt, et teammedlem, fire oppgaver og to ressurstilordninger. Deretter skal du oppdatere én oppgave, oppdatere prosjektet, slette én oppgave, slette én ressurstilordning og opprette en aktivitetsavhengighet.

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

## <a name="additional-samples"></a>Flere eksempler

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
