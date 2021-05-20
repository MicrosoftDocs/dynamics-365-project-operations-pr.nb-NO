---
title: Utvikle prosjektmaler med Kopier prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter prosjektmaler ved hjelp av den egendefinerte handlingen Kopier prosjekt.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949826"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="a57c2-103">Utvikle prosjektmaler med Kopier prosjekt</span><span class="sxs-lookup"><span data-stu-id="a57c2-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="a57c2-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a57c2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a57c2-105">Dynamics 365 Project Operations støtter muligheten til å kopiere et prosjekt og gjenopprette eventuelle tildelinger til de generelle ressursene som representerer rollen.</span><span class="sxs-lookup"><span data-stu-id="a57c2-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="a57c2-106">Kunder kan bruke denne funksjonaliteten til å bygge grunnleggende prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="a57c2-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="a57c2-107">Når du velger **Kopier prosjekt**, oppdateres statusen for målprosjektet.</span><span class="sxs-lookup"><span data-stu-id="a57c2-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="a57c2-108">Bruk **Statusårsak** til å avgjøre når kopieringshandlingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="a57c2-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="a57c2-109">Ved å velge **Kopier prosjekt** oppdateres også startdatoen for prosjektet til nåværende startdato hvis det ikke registreres noen måldato i målprosjektenheten.</span><span class="sxs-lookup"><span data-stu-id="a57c2-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="a57c2-110">Egendefinert handling Kopier prosjekt</span><span class="sxs-lookup"><span data-stu-id="a57c2-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="a57c2-111">Navn</span><span class="sxs-lookup"><span data-stu-id="a57c2-111">Name</span></span> 

<span data-ttu-id="a57c2-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="a57c2-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="a57c2-113">Inndataparametere</span><span class="sxs-lookup"><span data-stu-id="a57c2-113">Input parameters</span></span>
<span data-ttu-id="a57c2-114">Det finnes tre inndataparametere:</span><span class="sxs-lookup"><span data-stu-id="a57c2-114">There are three input parameters:</span></span>

| <span data-ttu-id="a57c2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a57c2-115">Parameter</span></span>          | <span data-ttu-id="a57c2-116">Type</span><span class="sxs-lookup"><span data-stu-id="a57c2-116">Type</span></span>   | <span data-ttu-id="a57c2-117">Verdier</span><span class="sxs-lookup"><span data-stu-id="a57c2-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="a57c2-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="a57c2-118">ProjectCopyOption</span></span>  | <span data-ttu-id="a57c2-119">String</span><span class="sxs-lookup"><span data-stu-id="a57c2-119">String</span></span> | <span data-ttu-id="a57c2-120">**{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="a57c2-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="a57c2-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="a57c2-121">SourceProject</span></span>      | <span data-ttu-id="a57c2-122">Enhetsreferanse</span><span class="sxs-lookup"><span data-stu-id="a57c2-122">Entity Reference</span></span> | <span data-ttu-id="a57c2-123">Kildeprosjekt</span><span class="sxs-lookup"><span data-stu-id="a57c2-123">Source Project</span></span> |
| <span data-ttu-id="a57c2-124">Mål</span><span class="sxs-lookup"><span data-stu-id="a57c2-124">Target</span></span>             | <span data-ttu-id="a57c2-125">Enhetsreferanse</span><span class="sxs-lookup"><span data-stu-id="a57c2-125">Entity Reference</span></span> | <span data-ttu-id="a57c2-126">Målprosjekt</span><span class="sxs-lookup"><span data-stu-id="a57c2-126">Target Project</span></span> |


- <span data-ttu-id="a57c2-127">**{"clearTeamsAndAssignments":true}**: Standard virkemåte for prosjektet på nettet, og vil fjerne alle tilordninger og teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="a57c2-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="a57c2-128">**{"removeNamedResources":true}** Standard virkemåte for Project Operations, og vil tilbakestille tilordninger til generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="a57c2-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="a57c2-129">For mer informasjon om handlinger, se [Bruke web-API-handlinger](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="a57c2-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="a57c2-130">Angi felt som skal kopieres</span><span class="sxs-lookup"><span data-stu-id="a57c2-130">Specify fields to copy</span></span> 
<span data-ttu-id="a57c2-131">Når handlingen kalles, ser **Kopier prosjekt** på prosjektvisningen **Kopier prosjektkolonner** for å finne ut hvilke felter som skal kopieres når prosjektet kopieres.</span><span class="sxs-lookup"><span data-stu-id="a57c2-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="a57c2-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="a57c2-132">Example</span></span>
<span data-ttu-id="a57c2-133">Følgende eksempel viser hvordan du kaller den egendefinerte handlingen **CopyProject** med parameteren **removeNamedResources** angitt.</span><span class="sxs-lookup"><span data-stu-id="a57c2-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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