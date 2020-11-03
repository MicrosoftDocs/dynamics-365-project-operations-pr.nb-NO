---
title: Opprette avanserte kontrakter for fakturering basert på fremdrift
description: Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan generere fakturaer for kunder basert på en prosentandel av fullført arbeid.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 1a83785a9db4dffc4585acf11ef971c08594f312
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081749"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="cd77e-103">Opprette avanserte kontrakter for fakturering basert på fremdrift</span><span class="sxs-lookup"><span data-stu-id="cd77e-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd77e-104">Dette emnet forklarer hvordan du oppretter prosjektkontrakter slik at du kan opprette fakturaer for kunder basert på en prosentandel av fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="cd77e-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="cd77e-105">Fakturabeløpene beregnes automatisk for budsjettkategoriene for arbeid som du har angitt for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="cd77e-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="cd77e-106">Faktureringstiden angis når du forhandler prosjektkontrakten med kunden.</span><span class="sxs-lookup"><span data-stu-id="cd77e-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="cd77e-107">Bruk fremgangsmåtene i dette emnet til å sette opp en kontrakt, et tilknyttet prosjekt og faktureringsreglene som beregner fakturabeløpene for budsjettkategoriene for arbeid som du har angitt for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="cd77e-108">Når du har opprettet kontrakten og prosjektet, kan du sette opp detaljer for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="cd77e-109">Du kan for eksempel definere aktiviteter og tilordne arbeidere til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="cd77e-110">Eksempel</span><span class="sxs-lookup"><span data-stu-id="cd77e-110">Example</span></span>

<span data-ttu-id="cd77e-111">Organisasjonen din er et selskap som utvikler programvare.</span><span class="sxs-lookup"><span data-stu-id="cd77e-111">Your organization is a software development firm.</span></span> <span data-ttu-id="cd77e-112">Du går med på å utvikle en lønnsregnskapspakke for en kunde for en total pris på 200 000 kroner.</span><span class="sxs-lookup"><span data-stu-id="cd77e-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="cd77e-113">Organisasjonen din godtar å fakturere kunden etter hvert som du fullfører bestemte prosentandeler av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="cd77e-114">Du konfigurerer følgende prosjektkategorier for arbeidet slik at du kan bruke dem i faktureringsprosessen:</span><span class="sxs-lookup"><span data-stu-id="cd77e-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="cd77e-115">Konsulentvirksomhet</span><span class="sxs-lookup"><span data-stu-id="cd77e-115">Consulting</span></span>
- <span data-ttu-id="cd77e-116">Utforming</span><span class="sxs-lookup"><span data-stu-id="cd77e-116">Design</span></span>
- <span data-ttu-id="cd77e-117">Installasjon</span><span class="sxs-lookup"><span data-stu-id="cd77e-117">Installation</span></span>

<span data-ttu-id="cd77e-118">Du definerer også faktureringsregler som automatisk beregner fakturabeløpene for prosentandelen av prosjektarbeid som er fullført for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="cd77e-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="cd77e-119">Budsjettsjefen oppretter et budsjett for prosjektkategoriene.</span><span class="sxs-lookup"><span data-stu-id="cd77e-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="cd77e-120">Mengden fullført arbeid beregnes automatisk som en prosentandel av faktisk arbeid sammenlignet med de budsjetterte mengdene.</span><span class="sxs-lookup"><span data-stu-id="cd77e-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd77e-121">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="cd77e-121">Prerequisites</span></span>

<span data-ttu-id="cd77e-122">Før du oppretter et prosjekt som bruker faktureringsregler, må du angi nummersekvensene for faktureringsregler og en gebyrjournal som brukes til å postere fremdriftsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="cd77e-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="cd77e-123">Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="cd77e-124">På siden **Parametere for prosjektstyring og regnskap** , i kategorien **Nummersekvenser** , setter du opp nummersekvensen du vil bruke når faktureringsregler opprettes.</span><span class="sxs-lookup"><span data-stu-id="cd77e-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="cd77e-125">Gå til **Prosjektstyring og regnskap** \> **Journaler** \> **Gebyr**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="cd77e-126">På siden **Gebyrjournal** velger du **Ny** og angir journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-126">On the **Fee journal** page, select **New** , and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="cd77e-127">Opprette en kontrakt for fremdriftsfaktureringer</span><span class="sxs-lookup"><span data-stu-id="cd77e-127">Create a contract for progress billings</span></span>

<span data-ttu-id="cd77e-128">Følg denne prosedyren for å opprette en prosjektkontrakt for et fastprisprosjekt.</span><span class="sxs-lookup"><span data-stu-id="cd77e-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="cd77e-129">Du oppretter en prosjektfaktura når arbeidet som er fullført på prosjektet, når en bestemt prosentandel.</span><span class="sxs-lookup"><span data-stu-id="cd77e-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="cd77e-130">Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="cd77e-131">På siden **Prosjektkontrakter** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="cd77e-132">I dialogboksen **Ny prosjektkontrakt** angir du følgende felt:</span><span class="sxs-lookup"><span data-stu-id="cd77e-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="cd77e-133">**Navn**</span><span class="sxs-lookup"><span data-stu-id="cd77e-133">**Name**</span></span>
    - <span data-ttu-id="cd77e-134">**Finansieringstype**</span><span class="sxs-lookup"><span data-stu-id="cd77e-134">**Funding type**</span></span>
    - <span data-ttu-id="cd77e-135">**Finansieringskilde**</span><span class="sxs-lookup"><span data-stu-id="cd77e-135">**Funding source**</span></span>
    - <span data-ttu-id="cd77e-136">**Salgsvaluta** – som standard brukes denne valutaen til kundefakturaer som er knyttet til prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="cd77e-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="cd77e-137">Du kan imidlertid endre salgsvalutaen for en bestemt kundefaktura.</span><span class="sxs-lookup"><span data-stu-id="cd77e-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="cd77e-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-138">Select **OK**.</span></span> <span data-ttu-id="cd77e-139">Informasjonen kopieres til overskriften på **Prosjektkontrakter** -siden.</span><span class="sxs-lookup"><span data-stu-id="cd77e-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="cd77e-140">På **Prosjektkontrakter** -siden fyller du ut resten av den nødvendige informasjonen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="cd77e-141">Opprette et prosjekt for fremdriftsfaktureringer</span><span class="sxs-lookup"><span data-stu-id="cd77e-141">Create a project for progress billings</span></span>

<span data-ttu-id="cd77e-142">Følg fremgangsmåten nedenfor for å opprette et prosjekt og eventuelle delprosjekter som er tilknyttet en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="cd77e-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="cd77e-143">Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="cd77e-144">På siden **Alle prosjekter** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="cd77e-145">I dialogboksen **Nytt prosjekt** , i **Prosjekttype** -feltet, velger du **Tid og materiale**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="cd77e-146">Velg en prosjektgruppe.</span><span class="sxs-lookup"><span data-stu-id="cd77e-146">Select a project group.</span></span> <span data-ttu-id="cd77e-147">En prosjektgruppe definerer bokføringsinformasjonen for prosjektene som er tilordnet gruppen.</span><span class="sxs-lookup"><span data-stu-id="cd77e-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="cd77e-148">Velg **Opprett prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-148">Select **Create project**.</span></span>
6. <span data-ttu-id="cd77e-149">Etter at du har opprettet prosjektet, setter du prosjektstadiet til **Pågår**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="cd77e-150">Opprette et budsjett for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="cd77e-150">Create a budget for a project</span></span>

<span data-ttu-id="cd77e-151">Budsjettkategorier brukes til å automatisk beregne fakturabeløpene for prosentandelen arbeid som er fullført for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="cd77e-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="cd77e-152">Følg fremgangsmåten nedenfor for å opprette budsjettkategorier for de estimerte kostnadene.</span><span class="sxs-lookup"><span data-stu-id="cd77e-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="cd77e-153">Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="cd77e-154">På siden **Alle prosjekter** velger du og åpner det ønskede prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="cd77e-155">På **Prosjekter** -siden, i handlingsruten, i **Planlegg** -kategorien, i **Budsjett** -gruppen velger du **Prosjektbudsjett**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="cd77e-156">På **Prosjektbudsjett** -siden angir du en estimert kostnad for hver kategori i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="cd77e-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="cd77e-157">Opprette faktureringsregler for fremdriftsfaktureringer</span><span class="sxs-lookup"><span data-stu-id="cd77e-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="cd77e-158">Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="cd77e-159">Velg en prosjektkontrakt på siden **Prosjektkontrakter** , og åpne den.</span><span class="sxs-lookup"><span data-stu-id="cd77e-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="cd77e-160">På siden med prosjektkontrakter, på hurtigfanen **Faktureringsregler** , velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="cd77e-161">På siden **Faktureringsregel** , i **Linjetype** -feltet, velger du **Fremdrift**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="cd77e-162">På hurtigfanen **Linjedetaljer for faktureringsregel** , i **Kontraktverdi** -feltet, angir du totalverdien for kontrakten.</span><span class="sxs-lookup"><span data-stu-id="cd77e-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="cd77e-163">I **Kategori** -feltet velger du kategorien der gebyrtransaksjonen skal bokføres.</span><span class="sxs-lookup"><span data-stu-id="cd77e-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="cd77e-164">I **Prosjekt** -feltet velger du prosjektet som bruker denne faktureringsregelen.</span><span class="sxs-lookup"><span data-stu-id="cd77e-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="cd77e-165">Valgfritt: Tilordne faktureringsregelen til flere prosjekter.</span><span class="sxs-lookup"><span data-stu-id="cd77e-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="cd77e-166">På hurtigfanen **Prosjekt** , i delen **Tilgjengelige prosjekter** , velger du et prosjekt, og deretter velger du pil høyre for å legge til prosjektet i delen **Valgte prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="cd77e-167">Valgfritt: Beregne prosentbeløpet som kunden tilbakeholder fra betalinger på en faktura.</span><span class="sxs-lookup"><span data-stu-id="cd77e-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="cd77e-168">På hurtigfanen **Tilbakeholdelsesbetingelser for betaling** velger du finansieringskilden, og deretter angir du tilbakeholdelsesprosenten i feltet **Tilbakeholdelsesprosent**.</span><span class="sxs-lookup"><span data-stu-id="cd77e-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="cd77e-169">Gjenta disse trinnene for å opprette flere faktureringsregler for prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="cd77e-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
