---
title: Utvikle prosjektmaler med Kopier prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter prosjektmaler ved hjelp av den egendefinerte handlingen Kopier prosjekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081560"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="0b1a6-103">Utvikle prosjektmaler med Kopier prosjekt</span><span class="sxs-lookup"><span data-stu-id="0b1a6-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="0b1a6-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0b1a6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0b1a6-105">Dynamics 365 Project Operations har støtte for muligheten til å kopiere et prosjekt og tilbakestille eventuelle tildelinger til de generelle ressursene som representerer rollen.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="0b1a6-106">Kunder kan bruke denne funksjonaliteten til å bygge grunnleggende prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="0b1a6-107">Når du velger **Kopier prosjekt** , oppdateres statusen for målprosjektet.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-107">When you select **Copy Project** , the status of the target project is updated.</span></span> <span data-ttu-id="0b1a6-108">Bruk **Statusårsak** til å avgjøre når kopieringshandlingen er fullført.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="0b1a6-109">Ved å velge **Kopier prosjekt** oppdateres også startdatoen for prosjektet til nåværende startdato hvis det ikke registreres noen måldato i målprosjektenheten.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="0b1a6-110">Egendefinert handling Kopier prosjekt</span><span class="sxs-lookup"><span data-stu-id="0b1a6-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="0b1a6-111">Navn</span><span class="sxs-lookup"><span data-stu-id="0b1a6-111">Name</span></span> 

<span data-ttu-id="0b1a6-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="0b1a6-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="0b1a6-113">Inndataparametere</span><span class="sxs-lookup"><span data-stu-id="0b1a6-113">Input parameters</span></span>
<span data-ttu-id="0b1a6-114">Det finnes tre inndataparametere:</span><span class="sxs-lookup"><span data-stu-id="0b1a6-114">There are three input parameters:</span></span>

| <span data-ttu-id="0b1a6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0b1a6-115">Parameter</span></span>          | <span data-ttu-id="0b1a6-116">Type</span><span class="sxs-lookup"><span data-stu-id="0b1a6-116">Type</span></span>   | <span data-ttu-id="0b1a6-117">Verdier</span><span class="sxs-lookup"><span data-stu-id="0b1a6-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="0b1a6-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="0b1a6-118">ProjectCopyOption</span></span>  | <span data-ttu-id="0b1a6-119">String</span><span class="sxs-lookup"><span data-stu-id="0b1a6-119">String</span></span> | <span data-ttu-id="0b1a6-120">**{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="0b1a6-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="0b1a6-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="0b1a6-121">SourceProject</span></span>      | <span data-ttu-id="0b1a6-122">Enhetsreferanse</span><span class="sxs-lookup"><span data-stu-id="0b1a6-122">Entity Reference</span></span> | <span data-ttu-id="0b1a6-123">Kildeprosjekt</span><span class="sxs-lookup"><span data-stu-id="0b1a6-123">Source Project</span></span> |
| <span data-ttu-id="0b1a6-124">Mål</span><span class="sxs-lookup"><span data-stu-id="0b1a6-124">Target</span></span>             | <span data-ttu-id="0b1a6-125">Enhetsreferanse</span><span class="sxs-lookup"><span data-stu-id="0b1a6-125">Entity Reference</span></span> | <span data-ttu-id="0b1a6-126">Målprosjekt</span><span class="sxs-lookup"><span data-stu-id="0b1a6-126">Target Project</span></span> |


- <span data-ttu-id="0b1a6-127">**{"clearTeamsAndAssignments":true}** : Standard virkemåte for prosjektet på nettet, og vil fjerne alle tilordninger og teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-127">**{"clearTeamsAndAssignments":true}** : Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="0b1a6-128">**{"removeNamedResources":true}** Standard virkemåte for Project Operations, og vil tilbakestille tilordninger til generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="0b1a6-129">For mer informasjon om handlinger, se [Bruke web-API-handlinger](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="0b1a6-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="0b1a6-130">Angi felt som skal kopieres</span><span class="sxs-lookup"><span data-stu-id="0b1a6-130">Specify fields to copy</span></span> 
<span data-ttu-id="0b1a6-131">Når handlingen kalles, ser **Kopier prosjekt** på prosjektvisningen **Kopier prosjektkolonner** for å finne ut hvilke felter som skal kopieres når prosjektet kopieres.</span><span class="sxs-lookup"><span data-stu-id="0b1a6-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
