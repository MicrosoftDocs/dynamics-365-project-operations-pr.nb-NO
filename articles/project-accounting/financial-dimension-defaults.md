---
title: Standardverdier for finansdimensjon
description: Dette emnet gir informasjon om hvordan du konfigurerer standardverdier for finansdimensjon.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131895"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="eeb78-103">Standardverdier for finansdimensjon</span><span class="sxs-lookup"><span data-stu-id="eeb78-103">Financial dimension defaults</span></span>

<span data-ttu-id="eeb78-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="eeb78-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="eeb78-105">Dynamics 365 Project Operations bruker [Finansdimensjoner](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions)-rammeverket i Dynamics 365 Finance for å gi ytterligere innsikt i prosjekters underfinansjournal og hovedboktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="eeb78-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="eeb78-106">Standard finansdimensjoner kan angis for en kunde, et prosjektfinansieringskilde, milepæl, prosjektkontraktlinje eller prosjekt.</span><span class="sxs-lookup"><span data-stu-id="eeb78-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="eeb78-107">Definere standard finansdimensjoner for en kunde</span><span class="sxs-lookup"><span data-stu-id="eeb78-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="eeb78-108">Kundedimensjonsstandarder er angitt i Finance.</span><span class="sxs-lookup"><span data-stu-id="eeb78-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="eeb78-109">Fullfør følgende trinn for å konfigurere dimensjonsstandarder.</span><span class="sxs-lookup"><span data-stu-id="eeb78-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="eeb78-110">Gå til **Utestående fordringer** > **Kunder** > **Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="eeb78-111">På siden **Kunder** i kategorien **Finansdimensjoner** angir du finansdimensjonsverdiene for en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="eeb78-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="eeb78-112">Definere standard finansdimensjoner for prosjektkontakter</span><span class="sxs-lookup"><span data-stu-id="eeb78-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="eeb78-113">Prosjektkontrakter opprettes og vedlikeholdes i Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="eeb78-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="eeb78-114">Regnskapsattributter for prosjektkontrakter angis i **Prosjektstyring og regnskap**-modulen i Finance.</span><span class="sxs-lookup"><span data-stu-id="eeb78-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="eeb78-115">Angi finansdimensjoner for en prosjektfinansieringskilde</span><span class="sxs-lookup"><span data-stu-id="eeb78-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="eeb78-116">Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="eeb78-117">Velg oppføringen du vil oppdatere, og i kategorien **Prosjektkontrakt** velger du **Vis standardregnskap**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="eeb78-118">Utvid **Relatert informasjon**, og velg kategorien **Finansieringskilder**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="eeb78-119">Angi finansdimensjonsstandarder.</span><span class="sxs-lookup"><span data-stu-id="eeb78-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="eeb78-120">Legg merke til at finansdimensjonene angis som standard fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="eeb78-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="eeb78-121">Angi finansdimensjoner for en prosjektkontaktlinje</span><span class="sxs-lookup"><span data-stu-id="eeb78-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="eeb78-122">Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Prosjektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="eeb78-123">Velg oppføringen du vil oppdatere, og i kategorien **Prosjektkontrakt** velger du **Vis standardregnskap**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="eeb78-124">Utvid **Relatert informasjon**, og velg kategorien **Kontraktlinjer**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="eeb78-125">Angi finansdimensjonsstandarder.</span><span class="sxs-lookup"><span data-stu-id="eeb78-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="eeb78-126">Finansdimensjonsstandardene er relevante og kan bare brukes med kontraktlinjer med fast pris (milepæl).</span><span class="sxs-lookup"><span data-stu-id="eeb78-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="eeb78-127">Disse standardene brukes på relaterte prosjekt a konto-transaksjoner og fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="eeb78-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="eeb78-128">Definere standard finansdimensjoner for prosjekter</span><span class="sxs-lookup"><span data-stu-id="eeb78-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="eeb78-129">Prosjekter opprettes og vedlikeholdes i CDS.</span><span class="sxs-lookup"><span data-stu-id="eeb78-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="eeb78-130">Regnskapsattributter for prosjekter angis i **Prosjektstyring og regnskap**-modulen i Finance.</span><span class="sxs-lookup"><span data-stu-id="eeb78-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="eeb78-131">Gå til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="eeb78-132">Velg oppføringen du vil oppdatere, og i kategorien **Prosjekt** velger du **Vis standardregnskap**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="eeb78-133">Utvid **Relatert informasjon**, og velg kategorien **Oppsett**.</span><span class="sxs-lookup"><span data-stu-id="eeb78-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="eeb78-134">Angi finansdimensjonsstandarder.</span><span class="sxs-lookup"><span data-stu-id="eeb78-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="eeb78-135">Legg merke til at finansdimensjonene angis som standard fra kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="eeb78-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="eeb78-136">Hvis prosjektet er knyttet til en kontraktlinje med flere prosjektkontraktkunder, brukes hovedkunden som standard for finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="eeb78-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="eeb78-137">Standardfinansdimensjoner for prosjekt brukes til å angi standarder for journallinje for tid, utgift og avgiftstransaksjoner i **Journal for Project Operations-integrering** og på relaterte prosjektfakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="eeb78-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>
