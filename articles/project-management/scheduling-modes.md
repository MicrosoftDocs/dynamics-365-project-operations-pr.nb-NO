---
title: Planleggingsmoduser
description: Dette emnet inneholder informasjon om planleggingsmoduser.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981447"
---
# <a name="scheduling-modes"></a><span data-ttu-id="5866b-103">Planleggingsmoduser</span><span class="sxs-lookup"><span data-stu-id="5866b-103">Scheduling modes</span></span>

<span data-ttu-id="5866b-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5866b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="5866b-105">Dynamics 365 Project Operations gjør det mulig for organisasjoner å definere hvordan de behandler endringer i viktige variabler i oppgaver i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="5866b-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="5866b-106">Basert på de spesielle behovene organisasjonen har, kan prosjektledere gjøre endringer i planleggingsmodusen når et prosjekt blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="5866b-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="5866b-107">Det er tre planleggingsmoduser tilgjengelig i Project Operations:</span><span class="sxs-lookup"><span data-stu-id="5866b-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="5866b-108">Fast varighet (dette er standardmodusen)</span><span class="sxs-lookup"><span data-stu-id="5866b-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="5866b-109">Fast arbeid</span><span class="sxs-lookup"><span data-stu-id="5866b-109">Fixed work</span></span>
  - <span data-ttu-id="5866b-110">Faste enheter</span><span class="sxs-lookup"><span data-stu-id="5866b-110">Fixed units</span></span>

<span data-ttu-id="5866b-111">Verdiene som påvirkes av definisjonen av en bestemt planleggingsmodus, bestemmes av følgende formel:</span><span class="sxs-lookup"><span data-stu-id="5866b-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="5866b-112">Innsats (*Arbeid*) = Varighet x Enheter</span><span class="sxs-lookup"><span data-stu-id="5866b-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="5866b-113">Når du definerer planleggingsmodusen for et prosjekt, angir du en av disse verdiene, som da ikke kan endres.</span><span class="sxs-lookup"><span data-stu-id="5866b-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="5866b-114">Når du holder denne verdien som en konstant, prioriteres verdien, som varsler at systemet ikke skal endre den når de to andre verdiene endres.</span><span class="sxs-lookup"><span data-stu-id="5866b-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="5866b-115">Tabellen nedenfor inneholder informasjon om virkningene ved valg av en bestemt modus.</span><span class="sxs-lookup"><span data-stu-id="5866b-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="5866b-116">**I denne oppgaven**</span><span class="sxs-lookup"><span data-stu-id="5866b-116">**In this task**</span></span>             | <span data-ttu-id="5866b-117">**Hvis du reviderer enheter**</span><span class="sxs-lookup"><span data-stu-id="5866b-117">**If you revise units**</span></span>   | <span data-ttu-id="5866b-118">**Hvis du reviderer varighet**</span><span class="sxs-lookup"><span data-stu-id="5866b-118">**If you revise duration**</span></span> | <span data-ttu-id="5866b-119">**Hvis du reviderer innsats**</span><span class="sxs-lookup"><span data-stu-id="5866b-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="5866b-120">Faste enheter-oppgaver</span><span class="sxs-lookup"><span data-stu-id="5866b-120">Fixed units task</span></span>     | <span data-ttu-id="5866b-121">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-121">Duration is recalculated.</span></span> | <span data-ttu-id="5866b-122">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-122">Effort is recalculated.</span></span>    | <span data-ttu-id="5866b-123">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="5866b-124">Fast innsats-oppgave</span><span class="sxs-lookup"><span data-stu-id="5866b-124">Fixed effort task</span></span>    | <span data-ttu-id="5866b-125">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-125">Duration is recalculated.</span></span> | <span data-ttu-id="5866b-126">Enheter beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-126">Units are recalculated.</span></span>    | <span data-ttu-id="5866b-127">Varigheten beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="5866b-128">Fast varighet-oppgave</span><span class="sxs-lookup"><span data-stu-id="5866b-128">Fixed duration task</span></span>  | <span data-ttu-id="5866b-129">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-129">Effort is recalculated.</span></span>   | <span data-ttu-id="5866b-130">Innsats beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-130">Effort is recalculated.</span></span>    | <span data-ttu-id="5866b-131">Enheter beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="5866b-131">Units are recalculated.</span></span>   |

<span data-ttu-id="5866b-132">Hvis du vil ha mer informasjon om implikasjonene av en bestemt modus, kan du se [Endre oppgavetypen for å få mer nøyaktig planlegging](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="5866b-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="5866b-133">I emnet brukes termen **Arbeid** i stedet for **Innsats**.</span><span class="sxs-lookup"><span data-stu-id="5866b-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="5866b-134">Endre organisasjonens planleggingsmodus</span><span class="sxs-lookup"><span data-stu-id="5866b-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="5866b-135">Fullfør trinnene nedenfor for å definere planleggingsmodusen for en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="5866b-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="5866b-136">Gå til **Innstillinger** \> **Generelt** \> **Parametere**, og velg deretter prosjektparameteren.</span><span class="sxs-lookup"><span data-stu-id="5866b-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="5866b-137">På siden **Prosjektparametere** velger du standard planleggingsmodus for organisasjonen, og deretter definerer du muligheten for at prosjektlederen skal kunne overstyre innstillingen når det opprettes et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5866b-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="5866b-138">Endre innstillingen for planleggingsmodus for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="5866b-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="5866b-139">Hvis en organisasjon tillater at prosjektlederen overstyrer standard planleggingsmodus, kan prosjektlederen endre dette når de oppretter et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5866b-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="5866b-140">Når prosjektet er lagret, kan imidlertid ikke planleggingsmodusen endres.</span><span class="sxs-lookup"><span data-stu-id="5866b-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="5866b-141">Kopierte prosjekter</span><span class="sxs-lookup"><span data-stu-id="5866b-141">Copied projects</span></span>

<span data-ttu-id="5866b-142">Siden et prosjekt opprettes når kopieringsprosjekthandlingen utføres, kan ikke prosjektlederen angi planleggingsmodus.</span><span class="sxs-lookup"><span data-stu-id="5866b-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="5866b-143">Målprosjektet vil som standard alltid være i modusen definert på organisasjonsnivå.</span><span class="sxs-lookup"><span data-stu-id="5866b-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="5866b-144">Kopierte oppgaver</span><span class="sxs-lookup"><span data-stu-id="5866b-144">Copied tasks</span></span>

<span data-ttu-id="5866b-145">Når en oppgave kopieres fra ett prosjekt til et annet, arver oppgaven planleggingsmodusen for målprosjektet.</span><span class="sxs-lookup"><span data-stu-id="5866b-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
