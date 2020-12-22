---
title: Oversikt over Project Service Automation
description: Dette emnet gir informasjon om Dynamics 365 Project Service Automation til Dynamics 365 Finance-integreringsløsningen.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642465"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="f58b6-103">Oversikt over Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f58b6-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f58b6-104">Project Service Automation til Finance-integreringsløsningen bruker funksjonen for dataintegrering til å synkronisere data på tvers av forekomster av Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f58b6-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="f58b6-105">Integreringsmalene som er tilgjengelige med funksjonen for dataintegrering, muliggjør dataflyten om prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler for prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="f58b6-106">Hvis du bruker versjon 7.3.0, må du installere KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="f58b6-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="f58b6-107">Deretter kan du integrere fastprisprosjekter.</span><span class="sxs-lookup"><span data-stu-id="f58b6-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="f58b6-108">Hvis du bruker versjon 7.3.0 og overfører gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å kunne ta med de avgiftene i prosjektfakturaen.</span><span class="sxs-lookup"><span data-stu-id="f58b6-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="f58b6-109">Hvis du bruker versjon 8.0, kan du bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeoverslag, utgiftsoverslag og låsing av funksjoner.</span><span class="sxs-lookup"><span data-stu-id="f58b6-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="f58b6-110">Hvis du bruker versjon 8.0.1 eller senere, vil du kunne synkronisere faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="f58b6-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="f58b6-111">Før du kan integrere Project Service Automation Finance, må du konfigurere integrasjonsparameterne for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f58b6-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="f58b6-112">For mer informasjon, se [Integrasjonsparametere for Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f58b6-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="f58b6-113">Denne integreringsløsningen aktiverer direkte synkronisering i følgende scenarioer:</span><span class="sxs-lookup"><span data-stu-id="f58b6-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="f58b6-114">Vedlikehold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-115">Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-116">Vedlikehold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-117">Vedlikehold milepæler for prosjektkontraktlinje i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-118">Vedlikehold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-119">Vedlikehold utgiftstransaksjonskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f58b6-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="f58b6-120">Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-121">Opprett prosjektutgiftestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="f58b6-122">Opprett faktiske verdier for prosjekttid, utgift og avgift i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="f58b6-123">Datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="f58b6-123">Data synchronization</span></span>

<span data-ttu-id="f58b6-124">Illustrasjonen nedenfor viser hvordan data synkroniseres som en del av integrasjonen mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="f58b6-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="f58b6-125">Ikke alle maler er tilgjengelige for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="f58b6-125">Not all templates are currently available.</span></span> <span data-ttu-id="f58b6-126">Maler blir frigjort etter hvert som de fullføres.</span><span class="sxs-lookup"><span data-stu-id="f58b6-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="f58b6-127">[![Project Service Automation-integrasjon med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f58b6-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="f58b6-128">Systemkrav for Finance</span><span class="sxs-lookup"><span data-stu-id="f58b6-128">System requirements for Finance</span></span>

<span data-ttu-id="f58b6-129">Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere Enterprise Edition 7.3 med Platform Update 12 eller senere.</span><span class="sxs-lookup"><span data-stu-id="f58b6-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="f58b6-130">Systemkrav for Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f58b6-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="f58b6-131">Hvis du vil bruke Project Service Automation til Finance-integreringsløsningen, må du installere følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="f58b6-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f58b6-132">Dynamics 365 Project Service Automation9.0.0.0 eller nyere</span><span class="sxs-lookup"><span data-stu-id="f58b6-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="f58b6-133">Kundeemne til kontantløsning for Dynamics 365 Sales, versjon 1.14.0.0 (v14) eller senere</span><span class="sxs-lookup"><span data-stu-id="f58b6-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="f58b6-134">Project Service Automation til Finance-løsning for Dynamics 365 Project Service Automation versjon 1.0.0.0 eller senere</span><span class="sxs-lookup"><span data-stu-id="f58b6-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="f58b6-135">Installer Project Service Automation til Finance-integreringsløsningen i Project Service Automation-forekomsten</span><span class="sxs-lookup"><span data-stu-id="f58b6-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="f58b6-136">Last ned Project Service Automation til Finance-integreringsløsningen fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.</span><span class="sxs-lookup"><span data-stu-id="f58b6-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
