---
title: Utgiftsoppføring (Lite)
description: Dette emnet gir informasjon om hvordan du arbeider medutgifts registrering i en Lite-distribusjon.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081504"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="17352-103">Utgiftsoppføring (Lite)</span><span class="sxs-lookup"><span data-stu-id="17352-103">Expense entry (lite)</span></span>

<span data-ttu-id="17352-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="17352-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="17352-105">Basic-, eller Lite-utgiftsbehandling er muligheten til å registrere enkle utgifter.</span><span class="sxs-lookup"><span data-stu-id="17352-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="17352-106">Du kan registrere utgifter mot et prosjekt, og deretter vil prosjektgodkjenneren se gjennom og godkjenne dem.</span><span class="sxs-lookup"><span data-stu-id="17352-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="17352-107">Hvis du vil ha mer informasjon om utgiftsfunksjonene i Dynamics 365 Project Operations, kan du se [Oversikt over utgifter](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="17352-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="17352-108">Registrere en grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="17352-108">Capture a basic expense</span></span>

<span data-ttu-id="17352-109">Du kan registrer utgiftene dine, slik at du kan sende dem til godkjenneren.</span><span class="sxs-lookup"><span data-stu-id="17352-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="17352-110">Gå til **Utgifter** , og velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="17352-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="17352-111">På siden **Ny utgift** angir du utgiftsinformasjonen, og deretter velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="17352-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="17352-112">Sende inn en grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="17352-112">Submit a basic expense</span></span>

<span data-ttu-id="17352-113">Når du er ferdig med å registrere alle utgiftene, og du er klar til å få dem godkjent, må du sende dem.</span><span class="sxs-lookup"><span data-stu-id="17352-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="17352-114">Gå til **Utgifter** , og velg en utgift.</span><span class="sxs-lookup"><span data-stu-id="17352-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="17352-115">Du kan også velge alle utgiftene ved hjelp av avmerkingsboksen i hodet.</span><span class="sxs-lookup"><span data-stu-id="17352-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="17352-116">Velg **Send inn**.</span><span class="sxs-lookup"><span data-stu-id="17352-116">Select **Submit**.</span></span> <span data-ttu-id="17352-117">Systemet behandler de valgte oppføringene og oppretter deretter forespørsler om utgiftsgodkjenning.</span><span class="sxs-lookup"><span data-stu-id="17352-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="17352-118">Tilbakekalle en grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="17352-118">Recall a basic expense</span></span>

<span data-ttu-id="17352-119">Når du sender inn en utgift ved en feil, kan du tilbakekalle den.</span><span class="sxs-lookup"><span data-stu-id="17352-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="17352-120">Tiden som kreves for å tilbakekalle en utgiftsoppføring, avhenger av godkjenningsfasen.</span><span class="sxs-lookup"><span data-stu-id="17352-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="17352-121">Hvis godkjenneren ikke har godkjent oppføringen ennå, kan tilbakekallingen skje umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="17352-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="17352-122">Hvis imidlertid oppføringen allerede er godkjent, blir godkjenneren bedt om å godkjenne tilbakekallingen og tilbakeføre transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="17352-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="17352-123">Gå til **Utgifter** , og velg deretter utgiften du vil tilbakekalle, i listen over utgifter.</span><span class="sxs-lookup"><span data-stu-id="17352-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="17352-124">Velg **Tilbakekall**.</span><span class="sxs-lookup"><span data-stu-id="17352-124">Select **Recall**.</span></span> <span data-ttu-id="17352-125">Hvis utgiftsoppføringen ennå ikke er godkjent, tilbakekaller systemet den umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="17352-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="17352-126">Hvis utgifts oppføringen allerede er godkjent, blir det opprettet en tilbakekallingsforespørsel for å varsle godkjenneren om at du vil reversere utgiften.</span><span class="sxs-lookup"><span data-stu-id="17352-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="17352-127">Godkjenneren vil deretter bekrefte at reverseringen kan utføres, og oppføringen vil bli returnert.</span><span class="sxs-lookup"><span data-stu-id="17352-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="17352-128">Slette en grunnleggende utgift</span><span class="sxs-lookup"><span data-stu-id="17352-128">Delete a basic expense</span></span>

<span data-ttu-id="17352-129">Utgifter som ennå ikke er sendt, kan slettes.</span><span class="sxs-lookup"><span data-stu-id="17352-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="17352-130">Hvis du vil slette en utgift som allerede er sendt, må du først tilbakekalle den.</span><span class="sxs-lookup"><span data-stu-id="17352-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="17352-131">Se også</span><span class="sxs-lookup"><span data-stu-id="17352-131">See also</span></span>

- [<span data-ttu-id="17352-132">Oversikt over godkjenninger</span><span class="sxs-lookup"><span data-stu-id="17352-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
