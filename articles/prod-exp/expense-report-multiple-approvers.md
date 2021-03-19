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
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271725"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="a6def-103">Flere godkjennere av en reiseregning</span><span class="sxs-lookup"><span data-stu-id="a6def-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="a6def-104">Det kan hende at mer enn én person må godkjenne en reiseregning som er sendt inn av en ansatt, avhengig av organisasjonens godkjenningspolicyer for utgifter.</span><span class="sxs-lookup"><span data-stu-id="a6def-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="a6def-105">Når du konfigurerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for én eller flere godkjennere av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="a6def-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="a6def-106">Du kan for eksempel angi at alle reiseregninger skal godkjennes først av lederen til den ansatte som sendte rapporten, og deretter av leverandørgjeld-koordinatoren.</span><span class="sxs-lookup"><span data-stu-id="a6def-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="a6def-107">Hvis du bestemmer deg for å kreve flere godkjennere av reiseregninger, kan du legge til arbeidsflytelementene på følgende måter:</span><span class="sxs-lookup"><span data-stu-id="a6def-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="a6def-108">Legg til ett godkjenningselement som har ett trinn.</span><span class="sxs-lookup"><span data-stu-id="a6def-108">Add one approval element that has one step.</span></span> <span data-ttu-id="a6def-109">Det kan for eksempel hende at trinnet krever at en reiseregning tilordnes en brukergruppe, og at den godkjennes av 50 prosent av brukergruppens medlemmer.</span><span class="sxs-lookup"><span data-stu-id="a6def-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="a6def-110">Legg til ett godkjenningselement som har flere trinn.</span><span class="sxs-lookup"><span data-stu-id="a6def-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="a6def-111">Godkjenningselementet kan for eksempel ha følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="a6def-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="a6def-112">Lederen av den ansatte som sendte reiseregningen, godkjenner den.</span><span class="sxs-lookup"><span data-stu-id="a6def-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="a6def-113">Leverandørgjeld-assistenten verifiserer kvitteringene og reiseregningselementene.</span><span class="sxs-lookup"><span data-stu-id="a6def-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="a6def-114">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="a6def-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="a6def-115">Legg til flere godkjenningselementer med ett trinn.</span><span class="sxs-lookup"><span data-stu-id="a6def-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="a6def-116">Du kan for eksempel legge til et separat godkjenningselement for hvert av følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="a6def-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="a6def-117">Den ansattes overordnede godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="a6def-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="a6def-118">Budsjetteieren godkjenner reiseregningen.</span><span class="sxs-lookup"><span data-stu-id="a6def-118">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]