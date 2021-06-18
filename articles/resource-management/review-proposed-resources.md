---
title: Se gjennom foreslåtte ressurser
description: Dette emnet gir informasjon om hvordan du foreslår prosjektressurser.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 987ea08c77c1824182856c0d52ee0cd15e7029b9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000763"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="4b5e0-103">Se gjennom foreslåtte ressurser</span><span class="sxs-lookup"><span data-stu-id="4b5e0-103">Review proposed resources</span></span>

<span data-ttu-id="4b5e0-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="4b5e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b5e0-105">Ressursledere kan foreslå en ressurs til prosjektlederen ved å bruke en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="4b5e0-106">Fra rutenettet med forspørsler eller fra selve forespørselen velger du **Søk etter ressurser**.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="4b5e0-107">På siden **Planleggingsassistent** velger du ressursen, og deretter i ruten **Opprett ressursbestilling**, i feltet **Bestillingsstatus**, velger du **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="4b5e0-108">Følgende statusoppdateringer inntreffer:</span><span class="sxs-lookup"><span data-stu-id="4b5e0-108">The following status updates occur:</span></span>

- <span data-ttu-id="4b5e0-109">På siden **Planleggingsassistent** oppdateres statusindikatorene for å indikere at bestillingen er foreslått, ikke forpliktende bestilt.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="4b5e0-110">I ressursforespørselen endres statusen til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="4b5e0-111">I kategorien **Team** i prosjektet endres verdien for det generelle teammedlemmets **Forespørselsstatus** til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="4b5e0-112">Prosjektlederen kan enten godta eller avvise forslaget.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="4b5e0-113">Når ressursledere behandler ressursforespørsler, kan de bruke én av følgende metoder:</span><span class="sxs-lookup"><span data-stu-id="4b5e0-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="4b5e0-114">Foreslå flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å oppfylle de nødvendige timene.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="4b5e0-115">Foreslåtte timer deles deretter mellom flere ressurser som kan oppfylle de nødvendige timene.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="4b5e0-116">I dette scenariet kan ikke timene overlappe.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="4b5e0-117">Foreslå færre ressurser enn nødvendig.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="4b5e0-118">I dette scenariet er den foreslåtte ressurskapasiteten mindre enn de påkrevde timene som er angitt.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="4b5e0-119">Når anmoderen godtar de foreslåtte ressursene, opprettes det derfor et ressurskrav som ikke er fullført, for å fange opp det gjenstående behovet.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="4b5e0-120">Bestille flere ressurser for å tilfredsstille behovet hvis det ikke er noen enkelt ressurs tilgjengelig for å utføre arbeidet.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="4b5e0-121">Bestille færre ressurser enn nødvendig.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-121">Book fewer resources than are required.</span></span> <span data-ttu-id="4b5e0-122">I dette scenariet er de bestilte timene færre enn de obligatoriske timene.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="4b5e0-123">Systemet veileder deg om hvordan du foreslår ressurser i stedet for bestillinger, slik at anmoderen kan kontrollere og holde oversikt over gjenstående behov.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="4b5e0-124">Ressurstilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="4b5e0-124">Resource availability</span></span>

<span data-ttu-id="4b5e0-125">Det er svært viktig at ressurslederne kan vise tilgjengeligheten til ressurser og oppdatere bestillinger.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="4b5e0-126">I noen tilfeller er det ingen formell etterspørsel (ressursforespørsel), men en ressursleder må reagere på et ikke-planlagt behov som kommer gjennom kanaler, for eksempel en e-postmelding, telefonsamtale eller direkte melding.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="4b5e0-127">Ressursledere bruker planleggingstavlen til å oppdatere ressurser og bestillinger.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="4b5e0-128">Arbeidstimer for ressursen brukes som grunnlag for beregning av tilgjengeligheten for en ressurs.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="4b5e0-129">Ressursbestillinger opptar kapasiteten til ressursene.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="4b5e0-130">Planleggingstavlen bruker farger og skyggelegging til å vise bestillinger, tilgjengelighet og overbestillinger, samt statusen til bestillinger.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="4b5e0-131">Ved hjelp av en innstilling for planleggingstavlen kan du vise en forklaring.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="4b5e0-132">Hvis en pil mot høyre vises ved siden av en individuell bestillbar ressurs på planleggingstavlen, kan ressursen utvides for å vise detaljer om arbeidet som er bestilt av ressursen.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="4b5e0-133">Ettersom Dynamics 365 Project Operations bruker Universal Resource Scheduling-motoren, hvis du også har Dynamics 365 Field Service installert, kan du vise detaljene for ressursbestillinger for prosjekter, arbeidsordrer og alle andre enheter du har utvidet planlegging til.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="4b5e0-134">Hvis du vil vise flere detaljer om en individuell ressurs, høyreklikker du den for å åpne ressurskortet.</span><span class="sxs-lookup"><span data-stu-id="4b5e0-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]