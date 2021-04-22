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
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

> [!IMPORTANT] 
> Noen av eller alle funksjonene som er angitt i dette emnet, er tilgjengelig som en del av en forhåndsversjon. Innholdet i og funksjonaliteten kan endres. 

## <a name="scheduling-entities"></a>Planleggingsenheter

API-er for planlegging gjør det mulig å utføre operasjoner for oppretting, oppdatering og sletting med **planleggingsenheter**. Disse enhetene administreres via planleggingsmotoren i Project for the web. Oppretting, oppdatering og sletting med **planleggingsenheter** var begrenser i tidligere versjoner av Dynamics 365 Project Operations.

Tabellen nedenfor viser en fullstendig liste over **planleggingsenhetene**.

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

## <a name="schedule-apis"></a>API-er for planlegging

Nedenfor vises en liste over gjeldende API-er for planlegging.

- **msdyn_CreateProjectV1:** Denne API-en kan brukes til å opprette et prosjekt. Prosjektet og standard prosjektsamling opprettes umiddelbart.
- **msdyn_CreateTeamMemberV1:** Denne API-en kan brukes til å opprette et prosjektteammedlem. Teammedlemsoppføringen opprettes umiddelbart.
- **msdyn_CreateOperationSetV1**: Denne API-en kan brukes til å planlegge flere forespørsler som må utføres i en transaksjon.
- **msdyn_PSSCreateV1**: Denne API-en kan brukes til å opprette en enhet. Enheten kan være en hvilken som helst av planleggingsenhetene som støtter opprettingsoperasjonen.
- **msdyn_PSSUpdateV1**: Denne API-en kan brukes til å oppdatere en enhet. Enheten kan være en hvilken som helst av planleggingsenhetene som støtter oppdateringsoperasjonen.
- **msdyn_PSSDeleteV1**: Denne API-en kan brukes til å slette en enhet. Enheten kan være en hvilken som helst av planleggingsenhetene som støtter sletteoperasjonen.
- **msdyn_ExecuteOperationSetV1**: Denne API-en brukes til å kjøre alle operasjonene i det angitte operasjonssettet.

## <a name="using-schedule-apis-with-operationset"></a>Bruke API-er for tidsplan med OperationSet

Ettersom oppføringer med både **CreateProjectV1** og **CreateTeamMemberV1** opprettes umiddelbart, kan ikke disse API-ene brukes direkte i **OperationSet**. Du kan imidlertid bruke API-en til å opprette nødvendige oppføringer, opprette et **OperationSet** og deretter bruke disse forhåndsopprettede oppføringene i **OperationSet**.

## <a name="supported-operations"></a>Støttede operasjoner

| Planleggingsenhet | Opprette | Oppdatering | Delete | Viktige hensyn |
| --- | --- | --- | --- | --- |
Prosjektoppgave | Ja | Ja | Ja | Ingen |
| Avhengighet for prosjektoppgaver | Ja | Ja | | Oppføringer for prosjektoppgaveavhengighet oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes. |
| Ressurstilordning | Ja | Ja | | Operasjoner med følgende felter støttes ikke: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**. Ressurstilordningsoppføringer oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes. |
| Prosjektsamling | Ikke tilgjengelig | Ikke tilgjengelig | Ikke tilgjengelig | Standardsamlingen opprettes ved hjelp av API-en **CreateProjectV1**. |
| Prosjektteammedlem | Ja | Ja | Ja | For oppretting bruker du API-en **CreateTeamMemberV1**. |
| Project | Ja | Ja | Ikke tilgjengelig | Operasjoner med følgende felter støttes ikke: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** og **Duration**. |

Disse API-ene kan kalles med enhetsobjekter som inneholder egendefinerte felt.

ID-egenskapen er valgfri. Hvis den er angitt, prøver systemet å bruke den, og dette fører til et unntak hvis den ikke kan brukes. Hvis den ikke er angitt, genererer systemet den.

## <a name="limitations-and-known-issues"></a>Begrensninger og kjente problemer
Nedenfor vises en liste over begrensninger og kjente problemer:

- API-er for planlegging bare brukes av **brukere med Microsoft Project-lisens.** De kan ikke brukes av følgende:
    - Applikasjonsbrukere
    - Systembrukere
    - Integreringsbrukere
    - Andre brukere som ikke har den nødvendige lisensen
- Hvert **OperationSet** kan bare ha maksimalt 100 operasjoner.
- Hver bruker kan bare ha maksimalt 10 åpne **OperationSets**.
- Project Operations støtter for øyeblikket maksimalt 500 oppgaver på et prosjekt.
- **OperationSet**-feilstatus og -feillogger er ikke tilgjengelige for øyeblikket.
- API-er for planlegging er i offentlig forhåndsversjon. Bruk av disse API-ene i et produksjonsmiljø støttes ikke av Microsoft.

## <a name="sample-scenario"></a>Eksempelscenario

I dette scenarioet skal du opprette et prosjekt, et teammedlem, fire oppgaver og to ressurstilordninger. Deretter skal du oppdatere én oppgave, oppdatere prosjektet, slette én oppgave, slette én ressurstilordning og opprette en aktivitetsavhengighet.

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

## <a name="additional-samples"></a>Flere eksempler

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
