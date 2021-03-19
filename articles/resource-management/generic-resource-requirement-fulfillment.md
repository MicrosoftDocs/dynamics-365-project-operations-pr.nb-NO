---
title: Oppfyllelse av generelle ressurskrav
description: Dette emnet gir informasjon om hvordan du bestiller navngitte ressurser for et generisk ressurskrav.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fef896ae12c196d5566ad54f3e15373020e4e28a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279600"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="c7018-103">Oppfyllelse av generelle ressurskrav</span><span class="sxs-lookup"><span data-stu-id="c7018-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="c7018-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c7018-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c7018-105">Du kan bestille en navngitt ressurs som erstatter en generisk ressurs som har et ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="c7018-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="c7018-106">På siden **Prosjekter** velger du kategorien **Team**.</span><span class="sxs-lookup"><span data-stu-id="c7018-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="c7018-107">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="c7018-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="c7018-108">Du kan også åpne ressurskravet og deretter klikke **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="c7018-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="c7018-109">På siden **Planleggingsassistent** velger du en navngitt ressurs som skal reserveres til prosjektteamet, og deretter klikker du **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="c7018-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="c7018-110">Når bestillingen er fullført og oppfylt med en navngitt ressurs, erstattes den generelle ressursen med den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="c7018-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="c7018-111">Tilordningene i tidsplanen oppdateres også med den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="c7018-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="c7018-112">Oppfylle en generisk ressurs med flere navngitte ressurser</span><span class="sxs-lookup"><span data-stu-id="c7018-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="c7018-113">Å oppfylle et krav for en generell ressurs med flere navngitte ressurser ligner på å tilordne én enkelt navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="c7018-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="c7018-114">Det er for eksempel en oppgave med en varighet på fem dager, og 120 timer arbeid.</span><span class="sxs-lookup"><span data-stu-id="c7018-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="c7018-115">Denne oppgaven kan ikke full føres av én ressurs som arbeider med en vanlig 8-timers dag i løpet av en uke på fem dager.</span><span class="sxs-lookup"><span data-stu-id="c7018-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="c7018-116">Kravet er for 120 timer i løpet av fem dager, som er 24 timer per dag.</span><span class="sxs-lookup"><span data-stu-id="c7018-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="c7018-117">Dette er et eksempel på når flere navngitte ressurser er nødvendige for å oppfylle en generisk ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="c7018-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="c7018-118">Du må reservere flere ressurser for å oppfylle behovet.</span><span class="sxs-lookup"><span data-stu-id="c7018-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="c7018-119">Hovedforskjellen i dette scenariet er at den generelle ressursen beholdes i teamet som er tilordnet til oppgaven, og medlemmer av ressursteamet som er bestilt, blir ikke tilordnet som en del av posisjonen.</span><span class="sxs-lookup"><span data-stu-id="c7018-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="c7018-120">Prosjektlederen kan tilordne arbeidet slik det passer til de navngitte ressursene.</span><span class="sxs-lookup"><span data-stu-id="c7018-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="c7018-121">**Avstemming**-visningen kan hjelpe en prosjektleder med å dele opp bestillinger på tvers av flere ressurser i oppgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="c7018-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="c7018-122">Dette gjøres ikke automatisk fordi et scenario som er mer komplisert enn det enkle eksemplet ovenfor, for eksempel hvor du har en gruppe oppgaver som utgjør behovet, må intensjonen av hvordan prosjektlederen vil tilordne, antas av systemet.</span><span class="sxs-lookup"><span data-stu-id="c7018-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="c7018-123">Siden systemet ikke kan forstå hensikt, er det sannsynlig at antakelsene vil være forskjellige fra tiltenkt, og det skjer et uriktig eller uforutsigbart resultat.</span><span class="sxs-lookup"><span data-stu-id="c7018-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="c7018-124">Det forutsigbare resultatet er at den generelle ressursen holdes tilordnet til prosjektlederen med hensikt oppretter tildelinger, med hjelp av **Avstemming**-visningen.</span><span class="sxs-lookup"><span data-stu-id="c7018-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]