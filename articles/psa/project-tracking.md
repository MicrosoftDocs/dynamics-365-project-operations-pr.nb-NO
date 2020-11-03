---
title: Prosjektfremdrift og kostnadsforbruk
description: Dette emnet gir informasjon om sporing av prosjektfremdrift og kostnadsforbruk.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081781"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="d96e4-103">Prosjektfremdrift og kostnadsforbruk</span><span class="sxs-lookup"><span data-stu-id="d96e4-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d96e4-104">Behovet for å spore fremdriften mot en tidsplan varierer etter bransje.</span><span class="sxs-lookup"><span data-stu-id="d96e4-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="d96e4-105">Noen bransjer sporer på et detaljert nivå, mens andre bransjer sporer på et høyere nivå.</span><span class="sxs-lookup"><span data-stu-id="d96e4-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="d96e4-106">Dette emnet viser hvordan du planlegger for å oppfylle organisasjonens krav.</span><span class="sxs-lookup"><span data-stu-id="d96e4-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="d96e4-107">Visning av innsatssporing</span><span class="sxs-lookup"><span data-stu-id="d96e4-107">Effort tracking view</span></span>

<span data-ttu-id="d96e4-108">Visningen **Innsatssporing** sporer fremdriften for oppgavene i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="d96e4-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="d96e4-109">Den sammenligner de faktiske arbeidsinnsatstimene på en oppgave med oppgavens planlagte innsatstimer.</span><span class="sxs-lookup"><span data-stu-id="d96e4-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="d96e4-110">Project Service Automation bruker følgende formler til å beregne sporingsmåledata:</span><span class="sxs-lookup"><span data-stu-id="d96e4-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="d96e4-111">Opprinnelig ved opprettelsen av oppgaven: Planlagt kostnad blir satt til beregnet kostnad som fullført.</span><span class="sxs-lookup"><span data-stu-id="d96e4-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="d96e4-112">Når faktiske verdier er registrert på oppgaven, blir følgende beregnet på sporingsvisningen for arbeid</span><span class="sxs-lookup"><span data-stu-id="d96e4-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="d96e4-113">Fremdriftsprosent = faktisk innsats brukt til dags dato ÷ sluttestimat (EAC)</span><span class="sxs-lookup"><span data-stu-id="d96e4-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="d96e4-114">Estimat for fullføring (ETC) = sluttestimat (EAC) – faktisk innsats brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="d96e4-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="d96e4-115">EAC = resterende innsats + faktisk innsats brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="d96e4-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="d96e4-116">Forventet innsatsavvik = planlagt innsats – EAC</span><span class="sxs-lookup"><span data-stu-id="d96e4-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="d96e4-117">Project Service Automation viser en projeksjon av innsatsvariasjonen for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="d96e4-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="d96e4-118">Hvis EAC er større enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mer tid enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="d96e4-119">Derfor er den bak tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="d96e4-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="d96e4-120">Hvis EAC er mindre enn den planlagte innsatsen, blir aktiviteten beregnet for å ta mindre tid enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="d96e4-121">Derfor er den foran tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="d96e4-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="d96e4-122">Projisere innsats på nytt</span><span class="sxs-lookup"><span data-stu-id="d96e4-122">Reprojecting effort</span></span>

<span data-ttu-id="d96e4-123">Det er vanlig at en prosjektleder kan revidere de opprinnelige beregningene på en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="d96e4-124">Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="d96e4-125">Vi anbefaler imidlertid ikke at prosjektledere endrer tallene i den opprinnelige planen, fordi den opprinnelige planen for prosjektet er den etablerte sannhetskilden for prosjektets tidsplan og kostnadsestimat, som alle interessenter i prosjektet har godtatt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="d96e4-126">Det er to måter en prosjektleder kan reprojisere innsats på aktiviteter:</span><span class="sxs-lookup"><span data-stu-id="d96e4-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="d96e4-127">Overstyr standard anslagstid med ny beregning av gjenstående gjenstående innsats for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d96e4-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="d96e4-128">Overstyr standard fremdriftsprosent med ny beregning av den virkelige fremdriften for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d96e4-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="d96e4-129">Hver av disse metodene forårsaker en ny beregning av aktivitetens ETC, EAC og fremdriftsprosent samt beregnet innsatsavvik for en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="d96e4-130">EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.</span><span class="sxs-lookup"><span data-stu-id="d96e4-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="d96e4-131">Reprojisering av innsats i aktivitetssammendrag</span><span class="sxs-lookup"><span data-stu-id="d96e4-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="d96e4-132">Innsats i aktivitetssammendrag eller beholderaktivitet kan projiseres på nytt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="d96e4-133">Uansett om brukeren reaktiverer prosjekter ved hjelp av gjenstående innsats eller fremdriftsprosenten for aktivitetssammendraget, starter følgende sett med beregninger:</span><span class="sxs-lookup"><span data-stu-id="d96e4-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="d96e4-134">EAC, ETC og fremdriftsprosent for aktiviteten beregnes.</span><span class="sxs-lookup"><span data-stu-id="d96e4-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="d96e4-135">Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC var på aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d96e4-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="d96e4-136">Den nye EAC for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="d96e4-137">De berørte underordnede oppgavene til bladnodene får ETC og fremdriftsprosenten beregnet på nytt basert på EAC-verdien.</span><span class="sxs-lookup"><span data-stu-id="d96e4-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="d96e4-138">Dette fører til en ny projeksjon for innsatsavviket i aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="d96e4-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="d96e4-139">EAC-er for aktivitetssammendragene helt til rotnoden beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="d96e4-140">Kostnadssporingsvisning</span><span class="sxs-lookup"><span data-stu-id="d96e4-140">Cost tracking view</span></span> 

<span data-ttu-id="d96e4-141">**Kostnadssporings** -visningen sammenligner de faktiske kostnadene som ble brukt på en aktivitet, med de planlagte kostnadene.</span><span class="sxs-lookup"><span data-stu-id="d96e4-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="d96e4-142">Denne visningen viser bare arbeidskostnader og inkluderer ikke kostnader fra utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="d96e4-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="d96e4-143">Project Service Automation bruker følgende formler til å beregne sporingsmåledata:</span><span class="sxs-lookup"><span data-stu-id="d96e4-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="d96e4-144">Når en oppgave opprettes, er de planlagte kostnadene lik beregnet kostnad som fullført.</span><span class="sxs-lookup"><span data-stu-id="d96e4-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="d96e4-145">Når faktiske verdier er registrert på oppgaven, blir følgende beregnet på **Sporing** -visningen for kostnad:</span><span class="sxs-lookup"><span data-stu-id="d96e4-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="d96e4-146">Prosentandel av kostnadene som brukes = faktisk kostnad brukt til dato ÷ beregnet kostnad som fullført for aktiviteten</span><span class="sxs-lookup"><span data-stu-id="d96e4-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="d96e4-147">Kostnad for fullføring (CTC) = beregnet kostnad som fullført – faktisk kostnad brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="d96e4-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="d96e4-148">Beregnet kostnad som fullført = CTC + faktisk kostnad brukt til dags dato</span><span class="sxs-lookup"><span data-stu-id="d96e4-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="d96e4-149">Beregnet kostnadsavvik = planlagt kostnad – beregnet kostnad som fullført</span><span class="sxs-lookup"><span data-stu-id="d96e4-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="d96e4-150">En projeksjon av kostnadsavviket vises for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="d96e4-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="d96e4-151">Hvis beregnet kostnad som fullført er større enn den planlagte kostnaden, blir oppgaven beregnet til å koste mer enn det som opprinnelig ble planlagt.</span><span class="sxs-lookup"><span data-stu-id="d96e4-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="d96e4-152">Derfor tenderer den til å være over budsjettet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="d96e4-153">Hvis beregnet kostnad som fullført er minre enn den planlagte kostnaden, blir oppgaven beregnet til å koste mindre enn det som opprinnelig ble planlagt, og trender under budsjettet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="d96e4-154">Prosjektlederens nye projisering av kostnad</span><span class="sxs-lookup"><span data-stu-id="d96e4-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="d96e4-155">Når innsatsen reprojiseres, blir alt forbrukt CTC, beregnet kostnad som fullført, prosent av kostnad brukt og beregnet kostnadsavvik beregnet på nytt i visningen **Kostnadssporing**.</span><span class="sxs-lookup"><span data-stu-id="d96e4-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="d96e4-156">Oppsummering av prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="d96e4-156">Project status summary</span></span>

<span data-ttu-id="d96e4-157">Sporingsdata i visningene **Innsatssporing** og **Kostnadssporing** viser fremdrift og kostnadsforbruk på oppgavenivåene prosjektrotnode, aktivitetssammendrags og bladnode.</span><span class="sxs-lookup"><span data-stu-id="d96e4-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="d96e4-158">**Status** -delen på siden **Prosjektenhet** viser et sammendrag av status på prosjektnivå.</span><span class="sxs-lookup"><span data-stu-id="d96e4-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="d96e4-159">Statussammendragsfelt</span><span class="sxs-lookup"><span data-stu-id="d96e4-159">Status summary fields</span></span>

<span data-ttu-id="d96e4-160">Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d96e4-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="d96e4-161">Det bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer.</span><span class="sxs-lookup"><span data-stu-id="d96e4-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="d96e4-162">Med **Kommentarer** -feltet kan prosjektlederen angi spesifikke kommentarer om statusen.</span><span class="sxs-lookup"><span data-stu-id="d96e4-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="d96e4-163">Feltet **Status oppdatert** er ikke redigerbart, og verdien er et tidsstempel som angir når statusen sist ble oppdatert.</span><span class="sxs-lookup"><span data-stu-id="d96e4-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="d96e4-164">Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d96e4-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="d96e4-165">Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, kan du angi disse feltene til **Foran**.</span><span class="sxs-lookup"><span data-stu-id="d96e4-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="d96e4-166">Når tidsplan- og kostnadsavviket for rotnoden er negativ, kan du angi dem til **Bak**.</span><span class="sxs-lookup"><span data-stu-id="d96e4-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
