---
title: Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter
description: Denne artikkelen inneholder informasjon om og eksempler for bruk av API-er for prosjektplan.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541137"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


**Planleggingsenheter**

API-er for prosjektplan gir mulighet til å utføre operasjoner for oppretting, oppdatering og sletting med **planleggingsenheter**. Disse enhetene administreres via planleggingsmotoren i Project for the web. Oppretting, oppdatering og sletting med **planleggingsenheter** var begrenser i tidligere versjoner av Dynamics 365 Project Operations.

Tabellen nedenfor viser en fullstendig liste over prosjekttidsplanens enheter.

| **Enhetsnavn**         | **Logisk navn for enhet**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Prosjektoppgave            | msdyn_projecttask           |
| Avhengighet for prosjektoppgaver | msdyn_projecttaskdependency |
| Ressurstilordning     | msdyn_resourceassignment    |
| Prosjektsamling          | msdyn_projectbucket         |
| Prosjektteammedlem     | msdyn_projectteam           |
| Prosjektsjekklister      | msdyn_projectchecklist      |
| Prosjektetikett           | msdyn_projectlabel          |
| Prosjektoppgave til etikett   | msdyn_projecttasktolabel    |
| Prosjektsprint          | msdyn_projectsprint         |

**OperationSet**

OperationSet er et enhetsarbeidsmønster som kan brukes når flere forespørsler som påvirker tidsplanen, må behandles i en transaksjon.

**API-er for prosjektplan**

Nedenfor vises en liste over gjeldende API-er for prosjektplan.

| **API**                                 | Bekrivelse                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Denne API-en brukes til å opprette et prosjekt. Prosjektet og standard prosjektsamling opprettes umiddelbart.                         |
| **msdyn_CreateTeamMemberV1**            | Denne API-en brukes til å opprette et prosjektteammedlem. Teammedlemsoppføringen opprettes umiddelbart.                                  |
| **msdyn_CreateOperationSetV1**          | Denne API-en brukes til å planlegge flere forespørsler som må utføres i en transaksjon.                                        |
| **msdyn_PssCreateV1**                   | Denne API-en brukes til å opprette en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter opprettingsoperasjonen. |
| **msdyn_PssUpdateV1**                   | Denne API-en brukes til å oppdatere en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter oppdateringsoperasjonen  |
| **msdyn_PssDeleteV1**                   | Denne API-en brukes til å slette en enhet. Enheten kan være en hvilken som helst av prosjektplanleggingsenhetene som støtter sletteoperasjonen. |
| **msdyn_ExecuteOperationSetV1**         | Denne API-en brukes til å kjøre alle operasjonene i det angitte operasjonssettet.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Denne API-en brukes til å oppdatere omfanget for planlagt arbeid med ressurstilordning.                                                        |



**Bruk av API-er for prosjektplan med OperationSet**

Ettersom oppføringer med både **CreateProjectV1** og **CreateTeamMemberV1** opprettes umiddelbart, kan ikke disse API-ene brukes direkte i **OperationSet**. Du kan imidlertid bruke API-en til å opprette nødvendige oppføringer, opprette et **OperationSet** og deretter bruke disse forhåndsopprettede oppføringene i **OperationSet**.

**Støttede operasjoner**

| **Planleggingsenhet**   | **Opprette** | **Update** | **Delete** | **Viktige hensyn**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prosjektoppgave            | Ja        | Ja        | Ja        | Feltene **Progress**, **EffortCompleted** og **EffortRemaining** kan redigeres i Project for the Web, men de kan ikke redigeres i Project Operations.                                                                                                                                                                                             |
| Avhengighet for prosjektoppgaver | Ja        | Nei         | Ja        | Oppføringer for prosjektoppgaveavhengighet oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes.                                                                                                                                                                                                                                 |
| Ressurstilordning     | Ja        | Ja\*      | Ja        | Operasjoner med følgende felter støttes ikke: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** og **PlannedWork**. Ressurstilordningsoppføringer oppdateres ikke. I stedet kan en gammel oppføring slettes, og en ny oppføring kan opprettes. En separat API er oppgitt for å oppdatere omganget av ressurstilordningen. |
| Prosjektsamling          | Ja        | Ja        | Ja        | Standardsamlingen opprettes ved hjelp av API-en **CreateProjectV1**. Støtte for oppretting og sletting av prosjektsamlinger ble lagt til i oppdateringsversjon 16.                                                                                                                                                                                                   |
| Prosjektteammedlem     | Ja        | Ja        | Ja        | For oppretting bruker du API-en **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Ja        | Ja        |            | Operasjoner med følgende felter støttes ikke: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** og **Duration**.                                                                                       |
| Prosjektsjekklister      | Ja        | Ja        | Ja        |                                                                                                                                                                                                                                                                                                                                                         |
| Prosjektetikett           | Nei         | Ja        | Nei         | Etikettnavn kan endres. Denne funksjonen er bare tilgjengelig for Project for the Web                                                                                                                                                                                                                                                                      |
| Prosjektoppgave til etikett   | Ja        | Nei         | Ja        | Denne funksjonen er bare tilgjengelig for Project for the Web                                                                                                                                                                                                                                                                                                  |
| Prosjektsprint          | Ja        | Ja        | Ja        | **Start**-feltet må ha en dato som er før **Fullfør**-feltet. Sprinter for samme prosjekt kan ikke overlappe med hverandre. Denne funksjonen er bare tilgjengelig for Project for the Web                                                                                                                                                                    |




ID-egenskapen er valgfri. Hvis den er angitt, prøver systemet å bruke den, og dette fører til et unntak hvis den ikke kan brukes. Hvis den ikke er angitt, genererer systemet den.

**Begrensninger og kjente problemer**

Nedenfor vises en liste over begrensninger og kjente problemer:

-   API-er for prosjektplan kan bare brukes av **brukere med Microsoft Project-lisens**. De kan ikke brukes av følgende:
    -   Applikasjonsbrukere
    -   Systembrukere
    -   Integreringsbrukere
    -   Andre brukere som ikke har den nødvendige lisensen
-   Hvert **OperationSet** kan bare ha maksimalt 100 operasjoner.
-   Hver bruker kan bare ha maksimalt 10 åpne **OperationSets**.
-   Project Operations støtter for øyeblikket maksimalt 500 oppgaver på et prosjekt.
-   Hver oppdateringsoperasjon for omfanget av ressurstilordningen teller som én enkelt operasjon.
-   Hver liste over oppdaterte omfang kan inneholde maksimalt 100 tidssektorer.
-   **OperationSet**-feilstatus og -feillogger er ikke tilgjengelige for øyeblikket.
-   Det er en maksimumsgrense på 400 sprinter per prosjekt.
-   [Begrensninger og grenser for prosjekter og oppgaver](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Etiketter er for øyeblikket bare tilgjengelig for Project for the Web.

**Feilbehandling**

-   Hvis du vil se gjennom feil som genereres fra operasjonssettene, går du til **Innstillinger** \> **Planlegg integrasjon** \> **Operasjonssett**.
-   Hvis du vil se gjennom feil som genereres fra prosjektplantjenesten, går du til **Innstilling** \> **Planlegg integrering** \> **PSS-feillogger**.

**Redigering av ressurstilordningsomfang**

I motsetning til alle andre API-er for prosjektplanlegging som oppdaterer en enhet, er API-en for ressurstilordningsomfang kun ansvarlig for oppdateringer for ett enkelt felt, msdyn_plannedwork, på én enhet, msydn_resourceassignment.

Den gitte tidsplanmodusen er:

-   **faste enheter**
-   prosjektkalender er 9-5p er 9-5pst, man, tir, tor, fre (IKKE ARBEID PÅ ONSDAGER)
-   og ressurskalenderen er 9-1p PST man til fre

Denne tilordningen er for én uke, fire timer om dagen. Dette er fordi ressurskalenderen er fra 9 til 1 PST, eller fire timer om dagen.

| &nbsp;     | Oppgave | Startdato | Sluttdato  | Antall | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 arbeider |  T1  | 13.06.2022  | 17.06.2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Hvis du for eksempel vil at arbeideren bare skal arbeide tre timer hver dag denne uken og bruke en time på andre oppgaver.

#### <a name="updatedcontours-sample-payload"></a>Eksempelnyttelasten UpdatedContours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Dette er tilordningen etter at API-en for oppdatering av omfanget til tidsplanen er kjørt.

| &nbsp;     | Oppgave | Startdato | Sluttdato  | Antall | 13.06.2022 | 14.06.2022 | 15.06.2022 | 16.06.2022 | 17.06.2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 arbeider | T1   | 13.06.2022  | 17.06.2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Eksempelscenario**

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

** Flere eksempler

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
