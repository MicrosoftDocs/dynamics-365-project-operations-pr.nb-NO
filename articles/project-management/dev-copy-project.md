---
title: Utvikle prosjektmaler med Kopier prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter prosjektmaler ved hjelp av den egendefinerte handlingen Kopier prosjekt.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590910"
---
# <a name="develop-project-templates-with-copy-project"></a>Utvikle prosjektmaler med Kopier prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations støtter muligheten til å kopiere et prosjekt og gjenopprette eventuelle tildelinger til de generelle ressursene som representerer rollen. Kunder kan bruke denne funksjonaliteten til å bygge grunnleggende prosjektmaler.

Når du velger **Kopier prosjekt**, oppdateres statusen for målprosjektet. Bruk **Statusårsak** til å avgjøre når kopieringshandlingen er fullført. Ved å velge **Kopier prosjekt** oppdateres også startdatoen for prosjektet til nåværende startdato hvis det ikke registreres noen måldato i målprosjektenheten.

## <a name="copy-project-custom-action"></a>Egendefinert handling Kopier prosjekt

### <a name="name"></a>Name 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Inndataparametere

Det finnes tre inndataparametere:

- **ReplaceNamedResources** eller **ClearTeamsAndAssignments** – Angi bare ett av alternativene. Ikke angi begge deler.

    - **\{"ReplaceNamedResources":true\}** – Standard virkemåte for Project Operations. Alle navngitte ressurser erstattes med generelle ressurser.
    - **\{"ClearTeamsAndAssignments":true\}** – Standard virkemåte for Project for the Web. Alle tilordninger og teammedlemmer fjernes.

- **SourceProject** – Enhetsreferansen for kildeprosjektet det skal kopieres fra. Denne parameteren kan ikke være null.
- **Target** – Enhetsreferansen for målprosjektet det skal kopieres til. Denne parameteren kan ikke være null.

Tabellen nedenfor gir et kort sammendrag av de tre parameterne.

| Parameter                | Type             | Verdi                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **Sann** eller **Usann** |
| ClearTeamsAndAssignments | Boolean          | **Sann** eller **Usann** |
| SourceProject            | Enhetsreferanse | Kildeprosjektet    |
| Target                   | Enhetsreferanse | Målprosjektet    |

For mer informasjon om handlinger, se [Bruke web-API-handlinger](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Valideringer

Følgende valideringer blir utført.

1. Null kontrollerer og henter kilde- og målprosjektene for å bekrefte eksistensen av begge prosjektene i organisasjonen.
2. Systemet validerer at målprosjektet er gyldig for kopiering ved å kontrollere følgende betingelser:

    - Det finnes ingen tidligere aktivitet i prosjektet (inkludert valg av **Oppgaver**-fanen), og prosjektet er nylig opprettet.
    - Det finnes ingen tidligere kopi, det er ikke forespurt import om dette prosjektet, og prosjektet har ikke en **Mislykket**-status.

3. Operasjonen kalles ikke opp ved hjelp av HTTP.

## <a name="specify-fields-to-copy"></a>Angi felt som skal kopieres

Når handlingen kalles, ser **Kopier prosjekt** på prosjektvisningen **Kopier prosjektkolonner** for å finne ut hvilke felter som skal kopieres når prosjektet kopieres.

### <a name="example"></a>Eksempel

Følgende eksempel viser hvordan du kaller opp den egendefinerte handlingen **CopyProjectV3** med parametersettet **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
