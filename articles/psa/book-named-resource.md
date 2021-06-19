---
title: Bestille navngitte ressurser fra ressurskrav
description: Dette emnet gir informasjon om bestilling av navngitte ressurser for et generisk ressurskrav.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: c2f97107de938975491770ab4e2ed18a3145d0e3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013408"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="113ef-103">Bestille navngitte ressurser fra ressurskrav</span><span class="sxs-lookup"><span data-stu-id="113ef-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="113ef-104">Du kan bestille en navngitt ressurs som erstatter en generisk ressurs som har et ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="113ef-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="113ef-105">I Project Service Automation (PSA), på **Prosjekter**-siden, klikker du på kategorien **Team**.</span><span class="sxs-lookup"><span data-stu-id="113ef-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="113ef-106">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="113ef-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="113ef-107">Du kan også åpne ressurskravet og deretter klikke **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="113ef-107">Or, open the resource requirement and then click **Book**.</span></span>


![Bestille et generisk teammedlem](media/RM-how-to-14.png)


3. <span data-ttu-id="113ef-109">På siden **Planleggingsassistent** velger du en navngitt ressurs som skal reserveres til prosjektteamet, og deretter klikker du **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="113ef-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Reservere et generisk teammedlem ved hjelp av planleggingsassistenten](media/RM-how-to-15.png)

<span data-ttu-id="113ef-111">Når bestillingen er fullført og oppfylt med en navngitt ressurs, erstattes den generelle ressursen med den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="113ef-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Navngitt teammedlem erstatter et generisk teammedlem](media/RM-how-to-16.png)

<span data-ttu-id="113ef-113">Tilordningene i tidsplanen oppdateres også med den navngitte ressursen.</span><span class="sxs-lookup"><span data-stu-id="113ef-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Navngitt teammedlem tilordnet til prosjektoppgaver](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="113ef-115">Oppfylle en generisk ressurs med flere navngitte ressurser</span><span class="sxs-lookup"><span data-stu-id="113ef-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="113ef-116">Å oppfylle et krav for en generell ressurs med flere navngitte ressurser ligner på å tilordne én enkelt navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="113ef-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="113ef-117">Det er for eksempel en oppgave med en varighet på fem dager, og 120 timer arbeid.</span><span class="sxs-lookup"><span data-stu-id="113ef-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="113ef-118">Denne oppgaven kan ikke full føres av én ressurs som arbeider med en vanlig 8-timers dag i løpet av en uke på fem dager.</span><span class="sxs-lookup"><span data-stu-id="113ef-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![En oppgave som krever 120 arbeidstimer over fem dager](media/RM-how-to-21.png)

<span data-ttu-id="113ef-120">Kravet er for 120 timer i løpet av fem dager, som er 24 timer per dag.</span><span class="sxs-lookup"><span data-stu-id="113ef-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Krav per dag](media/RM-how-to-22.png)

<span data-ttu-id="113ef-122">Dette er et eksempel på når flere navngitte ressurser er nødvendige for å oppfylle en generisk ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="113ef-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="113ef-123">Du må reservere flere ressurser for å oppfylle behovet.</span><span class="sxs-lookup"><span data-stu-id="113ef-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Bestille flere ressurser for å oppfylle behovet.](media/RM-how-to-23.png)

<span data-ttu-id="113ef-125">Hovedforskjellen i dette scenariet er at den generelle ressursen beholdes i teamet som er tilordnet til oppgaven, og medlemmer av ressursteamet som er bestilt, blir ikke tilordnet som en del av posisjonen.</span><span class="sxs-lookup"><span data-stu-id="113ef-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="113ef-126">Prosjektlederen kan tilordne arbeidet slik det passer til de navngitte ressursene.</span><span class="sxs-lookup"><span data-stu-id="113ef-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="113ef-127">**Avstemming**-visningen kan hjelpe en prosjektleder med å dele opp bestillinger på tvers av flere ressurser i oppgavetildelinger.</span><span class="sxs-lookup"><span data-stu-id="113ef-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="113ef-128">Dette gjøres ikke automatisk fordi et scenario som er mer komplisert enn det enkle eksemplet ovenfor, for eksempel hvor du har en gruppe oppgaver som utgjør behovet, må intensjonen av hvordan prosjektlederen vil tilordne, antas av systemet.</span><span class="sxs-lookup"><span data-stu-id="113ef-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="113ef-129">Siden systemet ikke kan forstå hensikt, er det sannsynlig at antakelsene vil være forskjellige fra tiltenkt, og det skjer et uriktig eller uforutsigbart resultat.</span><span class="sxs-lookup"><span data-stu-id="113ef-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="113ef-130">Det forutsigbare resultatet er at den generelle ressursen holdes tilordnet til prosjektlederen med hensikt oppretter tildelinger, med hjelp av **Avstemming**-visningen.</span><span class="sxs-lookup"><span data-stu-id="113ef-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]