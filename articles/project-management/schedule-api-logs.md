---
title: Logger for prosjektplanlegging
description: Dette emnet inneholder informasjon og eksempler som hjelper deg å bruke loggene for prosjektplanlegging til å spore feil som er knyttet til API-ene for prosjektplanleggingstjeneste og prosjektplanlegging.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877635"
---
# <a name="project-scheduling-logs"></a>Logger for prosjektplanlegging

_**Gjelder:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_, _Project for the Web_

Microsoft Dynamics 365 Project Operations bruker [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) som hovedplanleggingsmotor. Project Operations bruker de nye API-ene (programmeringsgrensesnittene) for prosjektplanlegging i stedet for standard nett-API-er (programmeringsgrensesnitt) for Microsoft Dataverse til å opprette, oppdatere og slette prosjektoppgaver, ressurstilordninger, oppgaveavhengigheter, prosjektsamlinger og prosjektteammedlemmer. Når opprettelses-, oppdaterings- eller sletteoperasjoner kjøres programmatisk på WBS-enheter (arbeidsnedbrytningsstruktur), kan det imidlertid oppstå feil. Det er implementert to nye administrative logger for å spore disse feilene og historikken over operasjoner: **Operasjonssett** og **Prosjektplanleggingstjeneste**. Gå til **Innstillinger** \> **Planleggingsintegrering** for å få tilgang til disse loggene.

Illustrasjonen nedenfor viser datamodellen for loggene for prosjektplanlegging.

![Datamodell for logger for prosjektplanlegging.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Logg for operasjonssett

Loggen for operasjonssett sporer kjøringen av et operasjonssett som brukes til å kjøre én eller mange opprettelses-, oppdaterings-, eller sletteoperasjoner i en satsvis jobb for prosjekter, prosjektoppgaver, ressurstilordninger, prosjektsamlinger eller prosjektteammedlemmer. Feltet **Operasjon i status** viser den generelle statusen for operasjonssettet. Detaljene for operasjonssettnyttelasten registreres i relaterte oppføringer for operasjonssettdetaljer.

### <a name="operation-set"></a>Operasjonssett

Tabellen nedenfor viser feltene som er knyttet til enheten **Operasjonssett**.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Datoen/klokkeslettet da operasjonssettet fullførtes eller mislyktes.                                                | CompletedOn            |
| msdyn_correlationid   | Verdien for **correlationId** for forespørselen.                                                                  | CorrelationId          |
| msdyn_description     | Beskrivelsen av operasjonssettet.                                                                        | Description            |
| msdyn_executedon      | Datoen/klokkeslettet da oppføringen ble kjørt.                                                                       | Kjørt den            |
| msdyn_operationsetId  | Den unike identifikatoren for enhetsforekomster.                                                                   | OperationSet           |
| msdyn_Project         | Prosjektet som er knyttet til operasjonssettet.                                                            | Project                |
| msdyn_projectid       | Verdien for **projectId** for forespørselen.                                                                      | ProjectId (avskrevet) |
| msdyn_projectName     | Ikke aktuelt.                                                                                              | Ikke aktuelt         |
| msdyn_PSSErrorLog     | Den unike identifikatoren for feilloggen for prosjektplanleggingstjeneste som er knyttet til operasjonssettet. | PSS-feillogg          |
| msdyn_PSSErrorLogName | Ikke aktuelt.                                                                                              | Ikke aktuelt         |
| msdyn_status          | Statusen for operasjonssettet.                                                                             | Status                 |
| msdyn_statusName      | Ikke aktuelt.                                                                                              | Ikke aktuelt         |
| msdyn_useraadid       | Objekt-ID-en for Azure Active Directory (Azure AD) for brukeren som forespørselen tilhører.                     | UserAADID              |

### <a name="operation-set-detail"></a>Operasjonssettdetalj

Tabellen nedenfor viser feltene som er knyttet til enheten **Operasjonssettdetalj**.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | De serialiserte Dataverse-feltene for forespørselen.                                            | CdsPayload            |
| msdyn_entityname           | Navnet på enheten for forespørselen.                                                     | EntityName            |
| msdyn_httpverb             | Forespørselsmetoden.                                                                         | HTTP-verb (avskrevet) |
| msdyn_httpverbName         | Ikke aktuelt.                                                                             | Ikke aktuelt        |
| msdyn_operationset         | Den unike identifikatoren for operasjonssettet som oppføringen hører til i.                      | OperationSet          |
| msdyn_operationsetdetailId | Den unike identifikatoren for enhetsforekomster.                                                  | OperationSet-detaljer   |
| msdyn_operationsetName     | Ikke aktuelt.                                                                             | Ikke aktuelt        |
| msdyn_operationtype        | Operasjonstypen for operasjonssettdetaljen.                                             | OperationType         |
| msdyn_operationtypeName    | Ikke aktuelt.                                                                             | Ikke aktuelt        |
| msdyn_psspayload           | De serialiserte feltene for Prosjektplanleggingstjeneste for forespørselen.                           | PssPayload            |
| msdyn_recordid             | Identifikatoren for forespørselsoppføringen.                                                       | Oppførings-ID             |
| msdyn_requestnumber        | Et automatisk generert nummer som identifiserer rekkefølgen forespørsler ble mottatt i. | Forespørselsnummer        |

## <a name="project-scheduling-service-error-logs"></a>Feillogger for prosjektplanleggingstjeneste

Feilloggene for prosjektplanleggingstjeneste registrerer feil som oppstår når prosjektplanleggingstjenesten prøver operasjonen **Lagre** eller **Åpne**. Det finnes tre scenarioer som støttes der disse loggene genereres:

- Det oppstår kritiske feil i handlinger som brukere starter (en tilordning kan for eksempel ikke opprettes på grunn av manglende rettigheter).
- Prosjektplanleggingstjenesten kan ikke programmatisk opprette, oppdatere, slette eller utføre andre gjennomgripende operasjoner på en enhet.
- Brukeren får feil når en oppføring ikke kan åpnes (for eksempel når et prosjekt åpnes eller informasjonen til et teammedlem oppdateres).

### <a name="project-scheduling-service-log"></a>Logg for prosjektplanleggingstjeneste

Tabellen nedenfor viser feltene som tas med i loggen for prosjektplanleggingstjeneste.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Kallsstakken for unntaket.                                               | Kallstakk     |
| msdyn_correlationid | Korrelasjons-ID-en for feilen.                                               | CorrelationId  |
| msdyn_errorcode     | Et felt som brukes til å lagre Dataverse-feilkoden eller HTTP-feilkoden. | Feilkode     |
| msdyn_HelpLink      | En kobling til den offentlige hjelpedokumentasjon.                                       | Hjelpekobling      |
| msdyn_log           | Loggen fra prosjektplanleggingstjenesten.                                   | Logg            |
| msdyn_project       | Prosjektet som er knyttet til feilloggen.                             | Project        |
| msdyn_projectName   | Navnet på prosjektet hvis nyttelasten i operasjonssettet skal beholdes. | Ikke aktuelt |
| msdyn_psserrorlogId | Den unike identifikatoren for enhetsforekomster.                                     | PSS-feillogg  |
| msdyn_SessionId     | Økt-ID-en for prosjektet.                                                        | Økt-ID     |

## <a name="error-log-cleanup"></a>Opprydding av feillogg

Begge loggene for prosjektplanleggingstjeneste og loggen for operasjonssett kan ryddes opp hver 90. dag. Alle oppføringer som er eldre enn 90 dager, blir slettet. Hvis du imidlertid endrer verdien for feltet **msdyn_StateOperationSetAge** på siden **Prosjektparametere**, kan administratorer justere oppryddingsomfanget slik at det er mellom 1 og 120 dager. Det finnes flere måter å endre denne verdien på:

- Tilpass enheten **Prosjektparameter** ved å opprette en egendefinert side og legge til feltet **Alder på foreldet operasjonssett**.
- Bruk klientkode som bruker [WebApi software development kit (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Bruk Service SDK-kode som bruker Xrm SDK **updateRecord**-metoden (klient-API-referanse) i modelldrevne apper. Power Apps omfatter en beskrivelse og støttede parametere for **updateRecord**-metoden.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
