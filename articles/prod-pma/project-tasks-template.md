---
title: Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgaver direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 16cd38f2f190414d7be9c93e8ab90d55006f47e1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009988"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="8feb8-103">Synkronisere prosjektoppgaver direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="8feb8-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8feb8-104">Dette emnet beskriver malen og den underliggende oppgaven som brukes til å synkronisere prosjektoppgaver direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8feb8-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="8feb8-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner er tilgjengelig i versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="8feb8-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="8feb8-106">Hvis du bruker Enterprise Edition 7.3.0 etter at du har installert KB-4132657 og KB-4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske verdier, og til å konfigurere låsing av funksjoner.</span><span class="sxs-lookup"><span data-stu-id="8feb8-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="8feb8-107">Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="8feb8-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="8feb8-108">Integrering av faktiske data er tilgjengelig i versjon 8.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="8feb8-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="8feb8-109">Dataflyt for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="8feb8-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="8feb8-110">Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="8feb8-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="8feb8-111">Integreringsmalen som er tilgjengelig med funksjonen for dataintegrering, muliggjør dataflyt om prosjektoppgaver fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="8feb8-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8feb8-112">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="8feb8-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="8feb8-113">[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="8feb8-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="8feb8-114">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="8feb8-114">Template and task</span></span>

<span data-ttu-id="8feb8-115">Hvis du vil ha tilgang til malen, går du til Microsoft Power Apps og velger **Prosjekter**, og deretter velger du **Nytt prosjekt** i øverste høyre hjørne for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="8feb8-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="8feb8-116">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektoppgaver fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="8feb8-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="8feb8-117">**Navn på malen i dataintegrering:** Prosjektoppgaver (PSA til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="8feb8-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="8feb8-118">**Navn på oppgaven i prosjektet:** Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="8feb8-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="8feb8-119">Før synkronisering av prosjektoppgaver kan forekomme, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="8feb8-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="8feb8-120">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="8feb8-120">Entity set</span></span>

| <span data-ttu-id="8feb8-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="8feb8-121">Project Service Automation</span></span> | <span data-ttu-id="8feb8-122">Finans</span><span class="sxs-lookup"><span data-stu-id="8feb8-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="8feb8-123">Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="8feb8-123">Project Tasks</span></span>              | <span data-ttu-id="8feb8-124">Integreringsenhet for prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="8feb8-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="8feb8-125">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="8feb8-125">Entity flow</span></span>

<span data-ttu-id="8feb8-126">Prosjektoppgaver administreres i Project Service Automation, og de synkroniseres til Finance som prosjektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="8feb8-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="8feb8-127">Oppsett av forhåndskrav og tilordning</span><span class="sxs-lookup"><span data-stu-id="8feb8-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="8feb8-128">Før synkronisering av prosjektoppgaver kan forekomme, må du synkronisere prosjektkontrakter og prosjekter.</span><span class="sxs-lookup"><span data-stu-id="8feb8-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="8feb8-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="8feb8-129">Power Query</span></span>

<span data-ttu-id="8feb8-130">Du må bruke Microsoft Power Query for Excel til å filtrere data hvis denne betingelsen er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="8feb8-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="8feb8-131">Du har ressursspesifikke oppføringer i en prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="8feb8-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="8feb8-132">Hvis du må bruke Power Query, følger du denne retningslinjen:</span><span class="sxs-lookup"><span data-stu-id="8feb8-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="8feb8-133">Malen Prosjektoppgaver (PSA til Fin og Ops) har et standardfilter som utelater ressursspesifikke oppføringer fra en prosjektoppgave ved å sette filteret på **IsLineTask** til **Usann**.</span><span class="sxs-lookup"><span data-stu-id="8feb8-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="8feb8-134">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="8feb8-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="8feb8-135">Maltilordning i dataintegrering</span><span class="sxs-lookup"><span data-stu-id="8feb8-135">Template mapping in Data integration</span></span>

<span data-ttu-id="8feb8-136">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordningene i dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="8feb8-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="8feb8-137">Tilordningen viser feltinformasjonen som blir synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="8feb8-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="8feb8-138">[![Maltilordning](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="8feb8-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]