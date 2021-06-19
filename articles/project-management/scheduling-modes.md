---
title: Planleggingsmoduser
description: Dette emnet inneholder informasjon om planleggingsmoduser.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116719"
---
# <a name="scheduling-modes"></a><span data-ttu-id="49acf-103">Planleggingsmoduser</span><span class="sxs-lookup"><span data-stu-id="49acf-103">Scheduling modes</span></span>

<span data-ttu-id="49acf-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="49acf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="49acf-105">Dynamics 365 Project Operations gjør det mulig for organisasjoner å definere hvordan de behandler endringer i viktige variabler i oppgaver i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="49acf-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="49acf-106">Basert på de spesielle behovene organisasjonen har, kan prosjektledere gjøre endringer i planleggingsmodusen når et prosjekt blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="49acf-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="49acf-107">Det er tre planleggingsmoduser tilgjengelig i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="49acf-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="49acf-108">Fast varighet (dette er standardmodusen)</span><span class="sxs-lookup"><span data-stu-id="49acf-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="49acf-109">Fast innsats (*Arbeid*)</span><span class="sxs-lookup"><span data-stu-id="49acf-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="49acf-110">Faste enheter</span><span class="sxs-lookup"><span data-stu-id="49acf-110">Fixed units</span></span>

<span data-ttu-id="49acf-111">Verdiene som påvirkes av definisjonen av en bestemt planleggingsmodus, bestemmes av følgende formel:</span><span class="sxs-lookup"><span data-stu-id="49acf-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="49acf-112">Innsats = Varighet x enheter</span><span class="sxs-lookup"><span data-stu-id="49acf-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="49acf-113">Når du definerer planleggingsmodusen for et prosjekt, angir du en av disse verdiene, som da ikke kan endres.</span><span class="sxs-lookup"><span data-stu-id="49acf-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="49acf-114">Når du holder denne verdien som en konstant, prioriteres verdien, som varsler at systemet ikke skal endre den når de to andre verdiene endres.</span><span class="sxs-lookup"><span data-stu-id="49acf-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="49acf-115">Tabellen nedenfor inneholder informasjon om virkningene ved valg av en bestemt modus.</span><span class="sxs-lookup"><span data-stu-id="49acf-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="49acf-116">**I denne oppgaven**</span><span class="sxs-lookup"><span data-stu-id="49acf-116">**In this task**</span></span>             | <span data-ttu-id="49acf-117">**Hvis du reviderer enheter**</span><span class="sxs-lookup"><span data-stu-id="49acf-117">**If you revise units**</span></span>   | <span data-ttu-id="49acf-118">**Hvis du reviderer varighet**</span><span class="sxs-lookup"><span data-stu-id="49acf-118">**If you revise duration**</span></span> | <span data-ttu-id="49acf-119">**Hvis du reviderer innsats**</span><span class="sxs-lookup"><span data-stu-id="49acf-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="49acf-120">Faste enheter-oppgaver</span><span class="sxs-lookup"><span data-stu-id="49acf-120">Fixed units task</span></span>     | <span data-ttu-id="49acf-121">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-121">Duration is recalculated.</span></span> | <span data-ttu-id="49acf-122">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-122">Effort is recalculated.</span></span>    | <span data-ttu-id="49acf-123">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="49acf-124">Fast innsats-oppgave</span><span class="sxs-lookup"><span data-stu-id="49acf-124">Fixed effort task</span></span>    | <span data-ttu-id="49acf-125">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-125">Duration is recalculated.</span></span> | <span data-ttu-id="49acf-126">Enheter beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-126">Units are recalculated.</span></span>    | <span data-ttu-id="49acf-127">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="49acf-128">Fast varighet-oppgave</span><span class="sxs-lookup"><span data-stu-id="49acf-128">Fixed duration task</span></span>  | <span data-ttu-id="49acf-129">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-129">Effort is recalculated.</span></span>   | <span data-ttu-id="49acf-130">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-130">Effort is recalculated.</span></span>    | <span data-ttu-id="49acf-131">Enheter beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="49acf-131">Units are recalculated.</span></span>   |

<span data-ttu-id="49acf-132">Hvis du vil ha mer informasjon om implikasjonene av en bestemt modus, kan du se [Endre oppgavetypen for å få mer nøyaktig planlegging](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="49acf-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="49acf-133">I emnet brukes termen **Arbeid** i stedet for **Innsats**.</span><span class="sxs-lookup"><span data-stu-id="49acf-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="49acf-134">Endre organisasjonens planleggingsmodus</span><span class="sxs-lookup"><span data-stu-id="49acf-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="49acf-135">Fullfør trinnene nedenfor for å definere planleggingsmodusen for en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="49acf-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="49acf-136">Gå til **Innstillinger** \> **Generelt** \> **Parametere**, og velg deretter prosjektparameteren.</span><span class="sxs-lookup"><span data-stu-id="49acf-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="49acf-137">På siden **Prosjektparametere** velger du standard planleggingsmodus for organisasjonen, og deretter definerer du muligheten for at prosjektlederen skal kunne overstyre innstillingen når det opprettes et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="49acf-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="49acf-138">Endre innstillingen for planleggingsmodus for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="49acf-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="49acf-139">Hvis en organisasjon tillater at prosjektlederen overstyrer standard planleggingsmodus, kan prosjektlederen endre dette når de oppretter et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="49acf-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="49acf-140">Når prosjektet er lagret, kan imidlertid ikke planleggingsmodusen endres.</span><span class="sxs-lookup"><span data-stu-id="49acf-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="49acf-141">Kopierte prosjekter</span><span class="sxs-lookup"><span data-stu-id="49acf-141">Copied projects</span></span>

<span data-ttu-id="49acf-142">Siden et prosjekt opprettes når kopieringsprosjekthandlingen utføres, kan ikke prosjektlederen angi planleggingsmodus.</span><span class="sxs-lookup"><span data-stu-id="49acf-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="49acf-143">Målprosjektet vil som standard alltid være i modusen definert på organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="49acf-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="49acf-144">Kopierte oppgaver</span><span class="sxs-lookup"><span data-stu-id="49acf-144">Copied tasks</span></span>

<span data-ttu-id="49acf-145">Når en oppgave kopieres fra ett prosjekt til et annet, arver oppgaven planleggingsmodusen for målprosjektet.</span><span class="sxs-lookup"><span data-stu-id="49acf-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
