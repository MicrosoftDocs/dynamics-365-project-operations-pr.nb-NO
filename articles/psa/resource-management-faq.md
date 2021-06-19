---
title: Vanlige spørsmål om ressursbehandling
description: Dette emnet inneholder svar på vanlige spørsmål om ressursbehandling.
author: ruhercul
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008773"
---
# <a name="resource-management-faq"></a><span data-ttu-id="8c3ac-103">Vanlige spørsmål om ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="8c3ac-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="8c3ac-104">Hva er forskjellen mellom et teammedlem og et ressurskrav?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="8c3ac-105">Et prosjektteammedlem kan tildeles oppgaver, bestilte eller overbestilte, og angis som en godkjenner.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="8c3ac-106">Et ressurskrav kan eksistere uten et prosjektteammedlem, som et utkast til behov.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="8c3ac-107">Hva er forskjellen mellom foreslåtte og ikke-forpliktende timer?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="8c3ac-108">Foreslåtte timer og ikke-forpliktende timer er forskjellige i synligheten.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="8c3ac-109">Foreslåtte timer vises bare for ressursledere og prosjektlederen som igangsatte behovet ved å bruke en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="8c3ac-110">Ikke-forpliktende timer er synlige for alle som har tilgang til planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="8c3ac-111">Hvordan kan jeg vise ikke-forpliktende timer for ressurser i et team?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="8c3ac-112">Ikke-forpliktende bestillinger kan utføres når du bestiller et ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="8c3ac-113">Ressurser som er ikke-forpliktende bestilt i et prosjektteam, vises som teammedlemmer som har ikke-forpliktende timer.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="8c3ac-114">De vises også på planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="8c3ac-115">Hvordan endrer jeg de nødvendige timene, og start- og sluttdatoene for en ressurs (genereøt eller navngitt) som jeg har bestilt?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="8c3ac-116">Når ressursene er bestilt, velger du **Vedlikehold bestillinger** for å gjøre eventuelle endringer som kreves.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="8c3ac-117">Hvilke ressurstyper støtter Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="8c3ac-118">**Bruker** og **Kontakt** er de eneste ressurstypene som støttes i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="8c3ac-119">Selv om du kan opprette andreressurs typer (for eksempel **Utstyr** og **Gruppe**), er det ingen ende-til-ende-brukstilfelle som støttes for dem.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="8c3ac-120">Hva er forskjellen mellom en tilordning og en bestilling?</span><span class="sxs-lookup"><span data-stu-id="8c3ac-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="8c3ac-121">Tildelinger er tilordningen av ressurser til prosjektoppgaver i prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="8c3ac-122">Ressursene kan være enten reelle ressurser eller generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="8c3ac-123">Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="8c3ac-124">Forpliktende bestillinger bruker kapasiteten til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="8c3ac-125">Ideelt sett bør bestillinger og tildelinger for reelle ressurser være de samme, fordi de ikke er forskjellige.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="8c3ac-126">PSA håndhever imidlertid ikke denne avtalen.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="8c3ac-127">Avstemming-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.</span><span class="sxs-lookup"><span data-stu-id="8c3ac-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]