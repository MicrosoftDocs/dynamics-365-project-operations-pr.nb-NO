---
title: Utgiftsrapporter og flere godkjennere
description: Dette emnet gir informasjon om reiseregninger som krever at flere enn én person må godkjennes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081623"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="e2fd5-103">Utgiftsrapporter og flere godkjennere</span><span class="sxs-lookup"><span data-stu-id="e2fd5-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="e2fd5-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e2fd5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e2fd5-105">Det kan hende at mer enn én person må godkjenne en sendt reiseregning, avhengig av organisasjonens godkjenningspolicyer for utgifter.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="e2fd5-106">Når du konfigurerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for én eller flere godkjennere av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="e2fd5-107">Du kan for eksempel angi at alle reiseregninger skal godkjennes av to separate personer, lederen av den ansatte som sendte rapporten, og leverandørgjeld-koordinatoren.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="e2fd5-108">Hvis du bestemmer deg for å kreve flere godkjennere av reiseregninger, kan du legge til arbeidsflytelementene på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="e2fd5-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="e2fd5-109">Legg til ett godkjenningselement som har ett trinn.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-109">Add one approval element that has one step.</span></span> <span data-ttu-id="e2fd5-110">Det kan for eksempel hende at trinnet krever at en reiseregning tilordnes en brukergruppe, og at den godkjennes av 50 prosent av brukergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="e2fd5-111">Legg til ett godkjenningselement som har flere trinn.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="e2fd5-112">Godkjenningselementet kan for eksempel ha følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="e2fd5-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="e2fd5-113">Lederen av den ansatte som sendte reiseregningen, godkjenner den.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="e2fd5-114">Leverandørgjeld-assistenten verifiserer kvitteringene og reiseregningselementene.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="e2fd5-115">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="e2fd5-116">Legg til flere godkjenningselementer med ett trinn.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="e2fd5-117">Du kan for eksempel legge til et separat godkjenningselement for hvert av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="e2fd5-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="e2fd5-118">Den ansattes overordnede godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="e2fd5-119">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="e2fd5-119">The budget owner approves the expense report.</span></span>
