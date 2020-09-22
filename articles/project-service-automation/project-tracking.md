---
title: Fremdrift for prosjekt og kostnadsforbruk
description: Dette emnet gir informasjon om hvordan du sporer prosjektfremdrift og kostnadsforbruk.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754174"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="eea59-103">Fremdrift for prosjekt og kostnadsforbruk</span><span class="sxs-lookup"><span data-stu-id="eea59-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eea59-104">Behovet for å spore fremdriften mot en tidsplan varierer etter bransje.</span><span class="sxs-lookup"><span data-stu-id="eea59-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="eea59-105">Noen bransjer sporer på et detaljert nivå, mens andre bransjer sporer på et høyere nivå.</span><span class="sxs-lookup"><span data-stu-id="eea59-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="eea59-106">Dette emnet viser hvordan du planlegger for å oppfylle organisasjonens krav.</span><span class="sxs-lookup"><span data-stu-id="eea59-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="eea59-107">Visning av innsatssporing</span><span class="sxs-lookup"><span data-stu-id="eea59-107">Effort tracking view</span></span>

<span data-ttu-id="eea59-108">Visningen **Innsatssporing** sporer fremdriften for oppgavene i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="eea59-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="eea59-109">Den sammenligner de faktiske innsatstimene som er brukt på en oppgave, mot de planlagte innsatstimene for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eea59-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="eea59-110">PSA bruker følgende formler til å beregne sporingsmåledata:</span><span class="sxs-lookup"><span data-stu-id="eea59-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="eea59-111">Fremdriftsprosent = faktisk innsats brukt til dato ÷ planlagt innsats for oppgaven</span><span class="sxs-lookup"><span data-stu-id="eea59-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="eea59-112">Estimat for fullføring (ETC) = planlagt innsats – faktisk innsats brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="eea59-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="eea59-113">Estimat vedr fullføring (EAC) = resterende innsats + faktisk innsats brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="eea59-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="eea59-114">Forventet innsatsavvik = planlagt innsats – EAC</span><span class="sxs-lookup"><span data-stu-id="eea59-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="eea59-115">PSA viser en projeksjon av innsatsvariasjonen for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eea59-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="eea59-116">Hvis EAC er større enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mer tid enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="eea59-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="eea59-117">Derfor er den bak tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="eea59-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="eea59-118">Hvis EAC er mindre enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mindre tid enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="eea59-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="eea59-119">Derfor er den foran tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="eea59-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="eea59-120">Projisere innsats på nytt</span><span class="sxs-lookup"><span data-stu-id="eea59-120">Re-projecting effort</span></span>

<span data-ttu-id="eea59-121">Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="eea59-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="eea59-122">Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="eea59-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="eea59-123">Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.</span><span class="sxs-lookup"><span data-stu-id="eea59-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="eea59-124">Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:</span><span class="sxs-lookup"><span data-stu-id="eea59-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="eea59-125">Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="eea59-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="eea59-126">Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="eea59-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="eea59-127">Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="eea59-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="eea59-128">EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.</span><span class="sxs-lookup"><span data-stu-id="eea59-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="eea59-129">Reprojisering av innsats i aktivitetssammendrag</span><span class="sxs-lookup"><span data-stu-id="eea59-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="eea59-130">Innsats i aktivitetssammendrag eller beholderaktivitet kan projiseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="eea59-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="eea59-131">Uansett om brukeren reaktiverer prosjekter ved hjelp av gjenstående innsats eller fremdriftsprosenten for aktivitetssammendraget, starter følgende sett med beregninger:</span><span class="sxs-lookup"><span data-stu-id="eea59-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="eea59-132">EAC, ETC og fremdriftsprosent for aktiviteten beregnes.</span><span class="sxs-lookup"><span data-stu-id="eea59-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="eea59-133">Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC var på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="eea59-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="eea59-134">Den nye EAC for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet.</span><span class="sxs-lookup"><span data-stu-id="eea59-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="eea59-135">De berørte underordnede oppgavene til bladnodene får ETC og fremdriftsprosenten beregnet på nytt basert på EAC-verdien.</span><span class="sxs-lookup"><span data-stu-id="eea59-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="eea59-136">Dette fører til en ny projeksjon for innsatsavviket i aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="eea59-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="eea59-137">EAC-er for aktivitetssammendragene helt til rotnoden beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="eea59-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="eea59-138">Kostnadssporingsvisning</span><span class="sxs-lookup"><span data-stu-id="eea59-138">Cost tracking view</span></span> 

<span data-ttu-id="eea59-139">**Kostnadssporings**-visningen sammenligner de faktiske kostnadene som ble brukt på en aktivitet, med de planlagte kostnadene på en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="eea59-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="eea59-140">Denne visningen viser bare arbeidskostnader og inkluderer ikke kostnader fra utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="eea59-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="eea59-141">PSA bruker følgende formler til å beregne sporingsmåledata:</span><span class="sxs-lookup"><span data-stu-id="eea59-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="eea59-142">Prosentandel av kostnadene som brukes = faktisk kostnad brukt til dato ÷ planlagt kostnad for aktiviteten</span><span class="sxs-lookup"><span data-stu-id="eea59-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="eea59-143">Kostnad for fullføring (CTC) = planlagt kostnad – faktisk kostnad brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="eea59-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="eea59-144">EAC = CTC + faktisk kostnad brukt til dato</span><span class="sxs-lookup"><span data-stu-id="eea59-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="eea59-145">Beregnet kostnadsavvik = planlagt kostnad – EAC</span><span class="sxs-lookup"><span data-stu-id="eea59-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="eea59-146">En projeksjon av kostnadsavviket vises for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="eea59-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="eea59-147">Hvis EAC er større enn den planlagte kostnaden, blir oppgaven beregnet til for å koste mer enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="eea59-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="eea59-148">Derfor tenderer den til å være over budsjettet.</span><span class="sxs-lookup"><span data-stu-id="eea59-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="eea59-149">Hvis EAC er mindre enn den planlagte kostnaden, blir oppgaven beregnet til å koste mindre enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="eea59-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="eea59-150">Derfor tenderer den til å være under budsjettet.</span><span class="sxs-lookup"><span data-stu-id="eea59-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="eea59-151">Prosjektlederens nye projisering av kostnad</span><span class="sxs-lookup"><span data-stu-id="eea59-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="eea59-152">Når innsatsen reprojiseres, blir alt forbrukt CTC, EAC, prosent av kostnad brukt og beregnet kostnadsavvik beregnet på nytt i visningen **Kostnadssporing**.</span><span class="sxs-lookup"><span data-stu-id="eea59-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="eea59-153">Oppsummering av prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="eea59-153">Project status summary</span></span>

<span data-ttu-id="eea59-154">Sporingsdata i visningene **Innsatssporing** og **Kostnadssporing** viser fremdrift og kostnadsforbruk på oppgavenivåene prosjektrotnode, aktivitetssammendrags og bladnode.</span><span class="sxs-lookup"><span data-stu-id="eea59-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="eea59-155">**Status**-delen på siden **Prosjektenhet** viser et sammendrag av status på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="eea59-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="eea59-156">Statussammendragsfelt</span><span class="sxs-lookup"><span data-stu-id="eea59-156">Status summary fields</span></span>

<span data-ttu-id="eea59-157">Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="eea59-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="eea59-158">Det bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer.</span><span class="sxs-lookup"><span data-stu-id="eea59-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="eea59-159">Med **Kommentarer**-feltet kan prosjektlederen angi spesifikke kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="eea59-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="eea59-160">Feltet **Status oppdatert** er ikke redigerbart, og verdien er et tidsstempel som angir når statusen sist ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="eea59-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="eea59-161">Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="eea59-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="eea59-162">Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, kan du angi disse feltene til **Foran**.</span><span class="sxs-lookup"><span data-stu-id="eea59-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="eea59-163">Når tidsplan- og kostnadsavviket for rotnoden er negativ, kan du angi dem til **Bak**.</span><span class="sxs-lookup"><span data-stu-id="eea59-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
