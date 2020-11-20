---
title: Foreta en ikke-forpliktende bestilling på krav
description: Dette emnet gir informasjon om hvordan du foretar en ikke-forpliktende bestilling på krav.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124110"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="7305a-103">Foreta en ikke-forpliktende bestilling på krav</span><span class="sxs-lookup"><span data-stu-id="7305a-103">Soft-book requirements</span></span>

<span data-ttu-id="7305a-104">Et ressurskrav kan være forpliktende.</span><span class="sxs-lookup"><span data-stu-id="7305a-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="7305a-105">En forpliktende bestilling oppretter et forslag som bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="7305a-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="7305a-106">Forslaget sendes deretter tilbake til anmoderen for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="7305a-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="7305a-107">En ikke-forpliktende bestilling legger foreløpig til en ressurs i et prosjektteam og har en annen status på planleggingstavlen, men den forbruker ikke kapasiteten til ressursen.</span><span class="sxs-lookup"><span data-stu-id="7305a-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="7305a-108">Hvis du vil legge inn en ikke-forpliktende bestilling på en ressurs fra planleggingtavlen, setter du feltet **Bestillingsstatus** til **Ikke-forpliktende**.</span><span class="sxs-lookup"><span data-stu-id="7305a-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Bestillingsstatusen settes til Ikke-forpliktende](media/Resource-Management-image77.png)

<span data-ttu-id="7305a-110">Når kategorien **Team** er i visning **Navngitte teammedlemmer**, vises ressursen der.</span><span class="sxs-lookup"><span data-stu-id="7305a-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="7305a-111">Timene som det er foretatt en ikke-forpliktende bestilling på, rapporteres i kolonnen **Timer med ikke-forpliktende bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="7305a-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Ikke-forpliktende bestilte timer i visningen Navngitte teammedlemmer](media/Resource-Management-image78.png)

<span data-ttu-id="7305a-113">Ikke-forpliktende bestilte teammedlemmer kan tilordnes til oppgaver.</span><span class="sxs-lookup"><span data-stu-id="7305a-113">Soft-booked team members can be assigned to tasks.</span></span>

![Ikke-forpliktende bestilt teammedlem som er tilordnet en oppgave](media/Resource-Management-image79.png)

<span data-ttu-id="7305a-115">I kategorien **Avstemming** vises ingen bestillinger for en ikke-forpliktende ressurs, fordi kategorien **Avstemming** bare vurderer forpliktende bestillinger.</span><span class="sxs-lookup"><span data-stu-id="7305a-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Ikke-forpliktende bestilt ressurs uten bestillinger i kategorien Avstemming](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="7305a-117">Du kan ikke foreta en ikke-forpliktende bestilling av en ressurs fra et krav som ble generert fra et generelt teammedlem.</span><span class="sxs-lookup"><span data-stu-id="7305a-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="7305a-118">I planleggingstavlen brukes en annen farge for ikke-forpliktende bestillinger for en ressurs.</span><span class="sxs-lookup"><span data-stu-id="7305a-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Ikke-forpliktende bestilling fra planleggingstavlen](media/Resource-Management-image81.png)

<span data-ttu-id="7305a-120">Hvis du vil konvertere en ikke-forpliktende bestilling til en forpliktende bestilling, høyreklikker du den ikke-forpliktende bestillingen på planleggingstavlen og velger **Endre status** \> **Forpliktende bestilling** \> **Forpliktende**.</span><span class="sxs-lookup"><span data-stu-id="7305a-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Endre bestillingsstatusen til forpliktende](media/Resource-Management-image82.png)

<span data-ttu-id="7305a-122">Bestillingen endres, og statusen endres på planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="7305a-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="7305a-123">Fordi bestillingsstatusen nå er **Forpliktende**, vises ressursen som bestilt, og kapasiteten og tilgjengeligheten blir justert.</span><span class="sxs-lookup"><span data-stu-id="7305a-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="7305a-124">Du kan bruke samme metode til å annullere en forpliktende bestilling eller en ikke-forpliktende bestilling fra planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="7305a-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="7305a-125">Hvis du vil konvertere en ressurs som er ikke-forpliktende, til forpliktende, går du til kategorien **Team** for prosjektet og velger ressursen, og deretter velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="7305a-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Bekreft-kommandoen](media/Resource-Management-image83.png)
