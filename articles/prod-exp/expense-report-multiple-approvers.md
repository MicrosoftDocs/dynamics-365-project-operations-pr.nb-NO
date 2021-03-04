---
title: Flere godkjennere av en reiseregning
description: Dette emnet gir informasjon om reiseregninger som krever godkjenning fra flere personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960619"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="5417e-103">Flere godkjennere av en reiseregning</span><span class="sxs-lookup"><span data-stu-id="5417e-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="5417e-104">Det kan hende at mer enn én person må godkjenne en reiseregning som er sendt inn av en ansatt, avhengig av organisasjonens godkjenningspolicyer for utgifter.</span><span class="sxs-lookup"><span data-stu-id="5417e-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="5417e-105">Når du konfigurerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for én eller flere godkjennere av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="5417e-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="5417e-106">Du kan for eksempel angi at alle reiseregninger skal godkjennes først av lederen til den ansatte som sendte rapporten, og deretter av leverandørgjeld-koordinatoren.</span><span class="sxs-lookup"><span data-stu-id="5417e-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="5417e-107">Hvis du bestemmer deg for å kreve flere godkjennere av reiseregninger, kan du legge til arbeidsflytelementene på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="5417e-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="5417e-108">Legg til ett godkjenningselement som har ett trinn.</span><span class="sxs-lookup"><span data-stu-id="5417e-108">Add one approval element that has one step.</span></span> <span data-ttu-id="5417e-109">Det kan for eksempel hende at trinnet krever at en reiseregning tilordnes en brukergruppe, og at den godkjennes av 50 prosent av brukergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="5417e-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="5417e-110">Legg til ett godkjenningselement som har flere trinn.</span><span class="sxs-lookup"><span data-stu-id="5417e-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="5417e-111">Godkjenningselementet kan for eksempel ha følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="5417e-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="5417e-112">Lederen av den ansatte som sendte reiseregningen, godkjenner den.</span><span class="sxs-lookup"><span data-stu-id="5417e-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="5417e-113">Leverandørgjeld-assistenten verifiserer kvitteringene og reiseregningselementene.</span><span class="sxs-lookup"><span data-stu-id="5417e-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="5417e-114">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="5417e-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="5417e-115">Legg til flere godkjenningselementer med ett trinn.</span><span class="sxs-lookup"><span data-stu-id="5417e-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="5417e-116">Du kan for eksempel legge til et separat godkjenningselement for hvert av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="5417e-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="5417e-117">Den ansattes overordnede godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="5417e-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="5417e-118">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="5417e-118">The budget owner approves the expense report.</span></span>
