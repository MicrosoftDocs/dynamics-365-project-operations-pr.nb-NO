---
title: Oversikt over modi for ressursstyring
description: Dette emnet gir information om ressursstyringsfunksjonaliteten i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118530"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="49a36-103">Oversikt over modi for ressursstyring</span><span class="sxs-lookup"><span data-stu-id="49a36-103">Resource management modes overview</span></span>

<span data-ttu-id="49a36-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="49a36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49a36-105">Dynamics 365 Project Operations støtter to moduser for at du skal kunne kjøre den generelle bestillingsflyten.</span><span class="sxs-lookup"><span data-stu-id="49a36-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="49a36-106">Administrasjonsmodusen defineres som en prosjektparameter og kan endres hvis forretningsbehovene endres.</span><span class="sxs-lookup"><span data-stu-id="49a36-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="49a36-107">Sentral modus</span><span class="sxs-lookup"><span data-stu-id="49a36-107">Central mode</span></span>
<span data-ttu-id="49a36-108">Organisasjoner som sentraliserer fordelingen av ressurser til prosjekter, kan bruke sentral modus til å sørge for at prosjektledere kan definere ressurskrav på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="49a36-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="49a36-109">Innfrielse av ressurskravene er delegert til en ressursleder.</span><span class="sxs-lookup"><span data-stu-id="49a36-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="49a36-110">Prosjektledere kan godta eller avvise ressurser som er foreslått av ressurslederen.</span><span class="sxs-lookup"><span data-stu-id="49a36-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Sentral modus](./media/resource-management-central.png)

<span data-ttu-id="49a36-112">Hvis du vil administrere ressurser med sentral modus, kan du se følgende:</span><span class="sxs-lookup"><span data-stu-id="49a36-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="49a36-113">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="49a36-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="49a36-114">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="49a36-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="49a36-115">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="49a36-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="49a36-116">Oppfyll en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="49a36-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="49a36-117">Godta eller avvise en foreslått prosjektressurs fra en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="49a36-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="49a36-118">Hybrid modus</span><span class="sxs-lookup"><span data-stu-id="49a36-118">Hybrid mode</span></span>
<span data-ttu-id="49a36-119">Organisasjoner som trenger fleksibilitet ved tildeling av ressurser, kan bruke hybrid modus til å sørge for at både prosjektledere og ressursledere kan bestille ressurser.</span><span class="sxs-lookup"><span data-stu-id="49a36-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybrid modus](./media/resource-management-hybrid.png)

<span data-ttu-id="49a36-121">I tillegg til de støttede prosessene i sentral modus, kan du se følgende emner for å administrere alle andre støttede bestillingsflyter i hybrid modus:</span><span class="sxs-lookup"><span data-stu-id="49a36-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="49a36-122">Bestill en ressurs direkte til et prosjekt:</span><span class="sxs-lookup"><span data-stu-id="49a36-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="49a36-123">Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver</span><span class="sxs-lookup"><span data-stu-id="49a36-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="49a36-124">Bestill en ressurs fra et ressurskrav:</span><span class="sxs-lookup"><span data-stu-id="49a36-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="49a36-125">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="49a36-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="49a36-126">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="49a36-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
