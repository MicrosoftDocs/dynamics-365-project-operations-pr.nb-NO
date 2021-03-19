---
title: Overføre prosjektbudsjetter ved regnskapsårets slutt
description: Denne artikkelen inneholder informasjon om hvordan gjenstående budsjettbeløp skal overføres til fremtidige år, og oppretting av detaljer for budsjettregisteret.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289741"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="6bec6-103">Overføre prosjektbudsjetter ved regnskapsårets slutt</span><span class="sxs-lookup"><span data-stu-id="6bec6-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6bec6-104">Når du arbeider med et prosjekt over flere år, kan det hende at gjenstående budsjett vises på slutten av regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6bec6-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="6bec6-105">Du kan overføre de gjenstående budsjettbeløpene til et fremtidig år, og du kan opprette budsjettregisterdetaljer for beløpene i de tilknyttede kontoene i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="6bec6-106">Før du overfører de resterende beløpene, kan du se gjennom og analysere de gjenstående budsjettbeløpene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="6bec6-107">Se gjennom og analysere gjenstående budsjettbeløp</span><span class="sxs-lookup"><span data-stu-id="6bec6-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="6bec6-108">Fullfør fremgangsmåten nedenfor for å se gjennom budsjettbeløpene ved årets slutt for prosjekter, men ikke overføre beløpene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="6bec6-109">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="6bec6-110">På siden **Videreføringsprosess for prosjektbudsjett**, på fanen **Alternativer for årsavslutning**, verifiserer du at **Viderefør gjenstående prosjektbudsjettbeløp** ikke er aktivert.</span><span class="sxs-lookup"><span data-stu-id="6bec6-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="6bec6-111">På **Parametere**-fanen, i **Prosjektbudsjettår**-feltet, velger du regnskapsåret du vil vise det resterende budsjettbeløpet for.</span><span class="sxs-lookup"><span data-stu-id="6bec6-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="6bec6-112">I feltet **Første regnskapsår** velger du regnskapsåret du vil vise det resterende budsjettbeløpet for.</span><span class="sxs-lookup"><span data-stu-id="6bec6-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="6bec6-113">I feltet **Fra prognosemodell** velger du **Gjenstående budsjett**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="6bec6-114">Hvis du vil inkludere prosjekter som oppfyller de valgte vilkårene, og som ikke har noe gjenstående budsjett, velger du **Vis null gjenstående**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="6bec6-115">I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer emd de valgte kriteriene, og velg deretter **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="6bec6-116">Hvis du vil utforme en databasespørring som laster inn et bestemt sett med budsjetter iruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="6bec6-117">Hvis du vil ha mer informasjon om en bestemt linje i ruten, velger du linjen, og deretter velger du **Vis budsjettdetaljer** eller **Vis kontoer**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="6bec6-118">Videreføre gjenstående budsjettbeløp</span><span class="sxs-lookup"><span data-stu-id="6bec6-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="6bec6-119">Når du behandler gjenstående budsjettbeløper, kan du opprette transaksjoner i hovedboken for beløpene du viderefører.</span><span class="sxs-lookup"><span data-stu-id="6bec6-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="6bec6-120">Hvis du vil opprette hovedboktransaksjoner, full fører du trinnene i delen [Videreføre budsjettbeløp og opprette hovedboktransaksjoner](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="6bec6-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="6bec6-121">Budsjettbeløp som videreflres, overføres til prognosemodellen som er valgt på siden **Prognosemodeller** som prognosemodellen for videreføringen.</span><span class="sxs-lookup"><span data-stu-id="6bec6-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="6bec6-122">Videreføre budsjettbeløp og opprette hovedboktransaksjoner</span><span class="sxs-lookup"><span data-stu-id="6bec6-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="6bec6-123">Velg **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="6bec6-124">På siden **Videreføringsprosess for prosjektbudsjett** velger du **Årsavslutning**, og aktiver deretter **Viderefør gjenstående prosjektbudsjettbeløp** og **Opprett budsjettregisteroppføringer i hovedbok**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="6bec6-125">På **Parametere**-fanen, i feltgruppen **Prosjektparametere**, velger du følgende:</span><span class="sxs-lookup"><span data-stu-id="6bec6-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="6bec6-126">**Prosjektbudsjettår**: Velg begynnelsen for regnskapsåret du vil vise de resterende budsjettbeløpene for.</span><span class="sxs-lookup"><span data-stu-id="6bec6-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="6bec6-127">**Resultat**: Opprett resultattransaksjoner i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="6bec6-128">**VIA**: Opprett VIA-transaksjoner (varer i arbeid) i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="6bec6-129">**Lønn**: Opprett lønnstildelingstransaksjoner i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="6bec6-130">I feltgruppen **Hovedbok** oppgir du følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="6bec6-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="6bec6-131">I feltet **Første regnskapsår** velger du regnskapsåret du vil overføre de resterende budsjettbeløpene til, for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="6bec6-132">Standardverdien er ett år etter verdien i feltet **Prosjektbudsjettår**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="6bec6-133">I feltet **Videreføringsperiode** velger du perioden du vil opprette budsjettregisterdetaljer for, i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="6bec6-134">Dette er vanligvis den første perioden i det første regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6bec6-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="6bec6-135">I feltgruppen **Kopier fra/til** oppgir du følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="6bec6-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="6bec6-136">I feltet **Fra prognosemodell** velger du prosjektbudsjettprognosemodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="6bec6-137">I feltet **Til hovedbokbudsjettmodell** velger du hovedbokbudsjettmodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre til hovedboken.</span><span class="sxs-lookup"><span data-stu-id="6bec6-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="6bec6-138">Velg **Overfør salgsvaluta** for å bruke prosjektets salgsvaluta for hovedboktransaksjonene som opprettes når du overfører budsjettbeløpene for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="6bec6-139">Når det ikke er merket av for alternativet, bruker transaksjonene regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="6bec6-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="6bec6-140">Velg **Vis null gjenstående** for å inkludere prosjekter som ikke har gjenstående budsjettbeløp, men som oppfyller de andre kriteriene du velger i prosjektene som vises i den nederste ruten.</span><span class="sxs-lookup"><span data-stu-id="6bec6-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="6bec6-141">I kategorien **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med kriteriene du har valgt.</span><span class="sxs-lookup"><span data-stu-id="6bec6-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="6bec6-142">Hvis du foretrekker å utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="6bec6-143">For hvert prosjekt du vil behandle, velger du alternativet i begynnelsen av linjen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6bec6-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="6bec6-144">Hvis du vil velge alle eller de fleste prosjektene, merker du av øverst til venstre.</span><span class="sxs-lookup"><span data-stu-id="6bec6-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="6bec6-145">Hvis du vil utelate behandlingen av et prosjekt, fjerner du merket for dette prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6bec6-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="6bec6-146">Hvis du vil overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret og opprette budsjettregisterdetaljer i hovedboken, velger du **Behandle**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="6bec6-147">Videreføre budsjettbeløp uten å opprette hovedboktransaksjoner</span><span class="sxs-lookup"><span data-stu-id="6bec6-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="6bec6-148">Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Budsjetter** > **Viderefør budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="6bec6-149">På siden **Videreføringsprosess for prosjektbudsjett**, i feltet **Alternativer for årsavslutning**, velger du **Viderefør gjenstående prosjektbudsjettbeløp**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="6bec6-150">I **Parametere**-gruppen, i **Prosjektbudsjettår**-feltet, velger du regnskapsåret du vil vise de resterende budsjettbeløpene for.</span><span class="sxs-lookup"><span data-stu-id="6bec6-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="6bec6-151">I gruppen **Kopier fra/til** oppgir du følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="6bec6-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="6bec6-152">I feltet **Fra prognosemodell** velger du prosjektbudsjettprognosemodellen som er knyttet til de gjenstående budsjettbeløpene du vil overføre for prosjektene.</span><span class="sxs-lookup"><span data-stu-id="6bec6-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="6bec6-153">Velg **Vis null gjenstående** hvis du vil inkludere prosjekter ikke har noe gjenstående budsjett, men som oppfyller de andre kriteriene du har valgt.</span><span class="sxs-lookup"><span data-stu-id="6bec6-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="6bec6-154">I gruppen **Velg budsjetter** velger du **Hent alle budsjetter** for å laste alle budsjetter som samsvarer med kriteriene du har valgt.</span><span class="sxs-lookup"><span data-stu-id="6bec6-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="6bec6-155">Hvis du vil utforme en databasespørring som laster inn et bestemt sett med prosjektbudsjetter i ruten, velger du **Hent valgte budsjetter**.</span><span class="sxs-lookup"><span data-stu-id="6bec6-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="6bec6-156">For hvert prosjekt du vil behandle, velger du alternativet i begynnelsen av linjen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6bec6-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="6bec6-157">Velg **Behandle** for å overføre de gjenstående budsjettbeløpene for de valgte prosjektene til det valgte regnskapsåret.</span><span class="sxs-lookup"><span data-stu-id="6bec6-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]