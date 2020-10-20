---
title: Oversikt over modi for ressursstyring
description: Dette emnet gir information om ressursstyringsfunksjonaliteten i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930103"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="049db-103">Oversikt over modi for ressursstyring</span><span class="sxs-lookup"><span data-stu-id="049db-103">Resource management modes overview</span></span>

<span data-ttu-id="049db-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="049db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="049db-105">Dynamics 365 Project Operations støtter to moduser for at du skal kunne kjøre den generelle bestillingsflyten.</span><span class="sxs-lookup"><span data-stu-id="049db-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="049db-106">Administrasjonsmodusen defineres som en prosjektparameter og kan endres hvis forretningsbehovene endres.</span><span class="sxs-lookup"><span data-stu-id="049db-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="049db-107">Sentral modus</span><span class="sxs-lookup"><span data-stu-id="049db-107">Central mode</span></span>
<span data-ttu-id="049db-108">Organisasjoner som sentraliserer fordelingen av ressurser til prosjekter, kan bruke sentral modus til å sørge for at prosjektledere kan definere ressurskrav på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="049db-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="049db-109">Innfrielse av ressurskravene er delegert til en ressursleder.</span><span class="sxs-lookup"><span data-stu-id="049db-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="049db-110">Prosjektledere kan godta eller avvise ressurser som er foreslått av ressurslederen.</span><span class="sxs-lookup"><span data-stu-id="049db-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Sentral modus](./media/resource-management-central.png)

<span data-ttu-id="049db-112">Hvis du vil administrere ressurser med sentral modus, kan du se følgende:</span><span class="sxs-lookup"><span data-stu-id="049db-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="049db-113">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="049db-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="049db-114">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="049db-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="049db-115">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="049db-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="049db-116">Oppfyll en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="049db-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="049db-117">Godta eller avvise en foreslått prosjektressurs fra en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="049db-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="049db-118">Hybrid modus</span><span class="sxs-lookup"><span data-stu-id="049db-118">Hybrid mode</span></span>
<span data-ttu-id="049db-119">Organisasjoner som trenger fleksibilitet ved tildeling av ressurser, kan bruke hybrid modus til å sørge for at både prosjektledere og ressursledere kan bestille ressurser.</span><span class="sxs-lookup"><span data-stu-id="049db-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybrid modus](./media/resource-management-hybrid.png)

<span data-ttu-id="049db-121">I tillegg til de støttede prosessene i sentral modus, kan du se følgende emner for å administrere alle andre støttede bestillingsflyter i hybrid modus:</span><span class="sxs-lookup"><span data-stu-id="049db-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="049db-122">Bestill en ressurs direkte til et prosjekt:</span><span class="sxs-lookup"><span data-stu-id="049db-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="049db-123">Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver</span><span class="sxs-lookup"><span data-stu-id="049db-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="049db-124">Bestill en ressurs fra et ressurskrav:</span><span class="sxs-lookup"><span data-stu-id="049db-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="049db-125">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="049db-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="049db-126">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="049db-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
