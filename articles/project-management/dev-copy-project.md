---
title: Utvikle prosjektmaler med Kopier prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter prosjektmaler ved hjelp av den egendefinerte handlingen Kopier prosjekt.
author: stsporen
ms.date: 01/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d12301b4e7baabeb0f045f9a11d4695fc026339af3fa7650db7177c495c71e90
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989277"
---
# <a name="develop-project-templates-with-copy-project"></a>Utvikle prosjektmaler med Kopier prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations støtter muligheten til å kopiere et prosjekt og gjenopprette eventuelle tildelinger til de generelle ressursene som representerer rollen. Kunder kan bruke denne funksjonaliteten til å bygge grunnleggende prosjektmaler.

Når du velger **Kopier prosjekt**, oppdateres statusen for målprosjektet. Bruk **Statusårsak** til å avgjøre når kopieringshandlingen er fullført. Ved å velge **Kopier prosjekt** oppdateres også startdatoen for prosjektet til nåværende startdato hvis det ikke registreres noen måldato i målprosjektenheten.

## <a name="copy-project-custom-action"></a>Egendefinert handling Kopier prosjekt 

### <a name="name"></a>Navn 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Inndataparametere
Det finnes tre inndataparametere:

| Parameter          | Type   | Verdier                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Enhetsreferanse | Kildeprosjekt |
| Mål             | Enhetsreferanse | Målprosjekt |


- **{"clearTeamsAndAssignments":true}**: Standard virkemåte for prosjektet på nettet, og vil fjerne alle tilordninger og teammedlemmer.
- **{"removeNamedResources":true}** Standard virkemåte for Project Operations, og vil tilbakestille tilordninger til generelle ressurser.

For mer informasjon om handlinger, se [Bruke web-API-handlinger](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Angi felt som skal kopieres 
Når handlingen kalles, ser **Kopier prosjekt** på prosjektvisningen **Kopier prosjektkolonner** for å finne ut hvilke felter som skal kopieres når prosjektet kopieres.


### <a name="example"></a>Eksempel
Følgende eksempel viser hvordan du kaller den egendefinerte handlingen **CopyProject** med parameteren **removeNamedResources** angitt.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]