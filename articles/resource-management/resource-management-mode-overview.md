---
title: Oversikt over modi for ressursstyring
description: Dette emnet gir informasjon om ressursstyringsfunksjonaliteten i Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d132bcbef5421202d2f4899091f0dc75166dd66
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949961"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="427ea-103">Oversikt over modi for ressursstyring</span><span class="sxs-lookup"><span data-stu-id="427ea-103">Resource management modes overview</span></span>

<span data-ttu-id="427ea-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="427ea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="427ea-105">Dynamics 365 Project Operations støtter to moduser for at du skal kunne kjøre den totale bestillingsflyten.</span><span class="sxs-lookup"><span data-stu-id="427ea-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="427ea-106">Administrasjonsmodusen defineres som en prosjektparameter og kan endres hvis forretningsbehovene endres.</span><span class="sxs-lookup"><span data-stu-id="427ea-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="427ea-107">Sentral modus</span><span class="sxs-lookup"><span data-stu-id="427ea-107">Central mode</span></span>
<span data-ttu-id="427ea-108">Organisasjoner som sentraliserer fordelingen av ressurser til prosjekter, kan bruke sentral modus til å sørge for at prosjektledere kan definere ressurskrav på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="427ea-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="427ea-109">Innfrielse av ressurskravene er delegert til en ressursleder.</span><span class="sxs-lookup"><span data-stu-id="427ea-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="427ea-110">Prosjektledere kan godta eller avvise ressurser som er foreslått av ressurslederen.</span><span class="sxs-lookup"><span data-stu-id="427ea-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Sentral modus](./media/resource-management-central.png)

<span data-ttu-id="427ea-112">Hvis du vil administrere ressurser med sentral modus, kan du se følgende:</span><span class="sxs-lookup"><span data-stu-id="427ea-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="427ea-113">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="427ea-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="427ea-114">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="427ea-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="427ea-115">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="427ea-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="427ea-116">Oppfyll en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="427ea-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="427ea-117">Godta eller avvise en foreslått prosjektressurs fra en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="427ea-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="427ea-118">Hybrid modus</span><span class="sxs-lookup"><span data-stu-id="427ea-118">Hybrid mode</span></span>
<span data-ttu-id="427ea-119">Organisasjoner som trenger fleksibilitet ved tildeling av ressurser, kan bruke hybrid modus til å sørge for at både prosjektledere og ressursledere kan bestille ressurser.</span><span class="sxs-lookup"><span data-stu-id="427ea-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybrid modus](./media/resource-management-hybrid.png)

<span data-ttu-id="427ea-121">I tillegg til de støttede prosessene i sentral modus, kan du se følgende emner for å administrere alle andre støttede bestillingsflyter i hybrid modus:</span><span class="sxs-lookup"><span data-stu-id="427ea-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="427ea-122">Bestill en ressurs direkte til et prosjekt:</span><span class="sxs-lookup"><span data-stu-id="427ea-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="427ea-123">Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver</span><span class="sxs-lookup"><span data-stu-id="427ea-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="427ea-124">Bestill en ressurs fra et ressurskrav:</span><span class="sxs-lookup"><span data-stu-id="427ea-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="427ea-125">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="427ea-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="427ea-126">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="427ea-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]