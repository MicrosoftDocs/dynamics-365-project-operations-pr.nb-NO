---
title: Arbeidsflyt for utgiftshåndtering
description: Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 Finance til å konfigurere en gjennomgangsprosess for reiseregninger i Utgiftshåndtering.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960574"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="6f5fc-103">Arbeidsflyt for utgiftshåndtering</span><span class="sxs-lookup"><span data-stu-id="6f5fc-103">Expense management workflow</span></span>

<span data-ttu-id="6f5fc-104">Du kan bruke arbeidsflytsystemet til å konfigurere en gjennomgangsprosess for reiseregninger i Utgiftshåndtering.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="6f5fc-105">Du kan konfigurere en arbeidsflyt som bruker følgende vilkår for å avgjøre hvem som godkjenner reiseregninger:</span><span class="sxs-lookup"><span data-stu-id="6f5fc-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="6f5fc-106">Rapporteringshierarkiet for ansatte og forhåndsdefinerte godkjenningsbegrensninger</span><span class="sxs-lookup"><span data-stu-id="6f5fc-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="6f5fc-107">Godkjenning på flere nivåer som støtter midlertidige godkjennere og en endelig godkjenner</span><span class="sxs-lookup"><span data-stu-id="6f5fc-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="6f5fc-108">Finansdimensjoner og prosjektansvar</span><span class="sxs-lookup"><span data-stu-id="6f5fc-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="6f5fc-109">Tilordning til bestemte brukere eller brukergrupper</span><span class="sxs-lookup"><span data-stu-id="6f5fc-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="6f5fc-110">Arbeidsflytgodkjenninger kan opprettes for reiseregninger, reiserekvisisjoner, forskudd og tilbakebetaling av MVA.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="6f5fc-111">**Eksempel**</span><span class="sxs-lookup"><span data-stu-id="6f5fc-111">**Example**</span></span>

<span data-ttu-id="6f5fc-112">Fremgangsmåten nedenfor er et eksempel på arbeidsflyten for en reiseregning i Utgiftshåndtering.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="6f5fc-113">En ansatt oppretter og lagrer en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="6f5fc-114">Den ansattes sender inn reiseregningen for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="6f5fc-115">Godkjenneren identifiseres basert på reglene som ble definert da arbeidsflyten ble konfigurert.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="6f5fc-116">Godkjenneren mottar en melding om at en reiseregning er klar til godkjenning.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="6f5fc-117">Godkjenneren ser gjennom reiseregningen og kontrollerer at følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="6f5fc-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="6f5fc-118">Utgiftene bryter ikke utgiftspolicyer.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="6f5fc-119">Hvis en utgiftspolicy brytes, kontrollerer godkjenneren at reiseregningen inkluderer en gyldig forretningsmessig begrunnelse.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="6f5fc-120">Elektroniske kvitteringer knyttes til reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="6f5fc-121">Godkjenneren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="6f5fc-122">Reiseregning tilordnes til koordinatoren for leverandørgjeld for postering.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="6f5fc-123">Ett av følgende trinn inntreffer, avhengig av om automatisk postering er konfigurert:</span><span class="sxs-lookup"><span data-stu-id="6f5fc-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="6f5fc-124">Hvis automatisk postering er konfigurert, blir reiseregningen behandlet for betaling, og statusen for reiseregningen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="6f5fc-125">Hvis automatisk postering ikke er konfigurert, kontrollerer koordinatoren for leverandørgjeld at alle originalkvitteringer er sendt, og at kvitteringene er i samsvar med utgiftene i reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="6f5fc-126">Alle avgiftskoder som angis i reiseregningen, må også verifiseres som riktige.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="6f5fc-127">Når disse kravene er bekreftet oppfylt, blir reiseregningen postert.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="6f5fc-128">Når reiseregningen er postert, blir betalingen godkjent for reiseregningen, og den ansatte blir refundert.</span><span class="sxs-lookup"><span data-stu-id="6f5fc-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
