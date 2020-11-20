---
title: Konfigurere utgiftskategorier
description: Dette emnet gir informasjon om hvordan du setter opp utgiftskategorier og delte kategorier for reiseregninger.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123795"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="cb2cb-103">Konfigurere utgiftskategorier</span><span class="sxs-lookup"><span data-stu-id="cb2cb-103">Set up expense categories</span></span>

<span data-ttu-id="cb2cb-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="cb2cb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cb2cb-105">Når ansatte oppretter reiseregninger, må hver utgift som de registrerer, tilknyttes en utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="cb2cb-106">Utgiftskategorier er avledet fra delte kategorier som kan deles på tvers av de juridiske enhetene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="cb2cb-107">Disse utgiftskategoriene kan også deles i andre områder, avhengig av hvordan organisasjonen er definert.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="cb2cb-108">Basert på definisjonen av organisasjonen og veiledning fra implementeringsteamet må du bestemme om kategoriene som brukes i utgiftshåndtering, bare skal brukes i utgiftshåndtering, eller om de skal deles i andre områder.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="cb2cb-109">Disse kategoriene kan deles mellom prosjektstyring og regnskaps- og utgiftshåndtering, eller mellom prosjektledelsen og regnskap og produksjon.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="cb2cb-110">De kan imidlertid ikke deles mellom utgiftshåndtering og produksjon.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="cb2cb-111">Før du kan starte oppsettsprosessen, må følgende avgjørelser tas for hver utgiftskategori:</span><span class="sxs-lookup"><span data-stu-id="cb2cb-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="cb2cb-112">Hva er utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-112">What is the expense category?</span></span> <span data-ttu-id="cb2cb-113">Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.</span><span class="sxs-lookup"><span data-stu-id="cb2cb-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="cb2cb-114">Kan utgiftskategorien også brukes til prosjektstyring og regnskap?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="cb2cb-115">I så fall må du også ta følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="cb2cb-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="cb2cb-116">Hvilke kostnadskontoer skal brukes til følgende utgifter?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="cb2cb-117">Kostnad</span><span class="sxs-lookup"><span data-stu-id="cb2cb-117">Cost</span></span>
        - <span data-ttu-id="cb2cb-118">Lønnstildeling</span><span class="sxs-lookup"><span data-stu-id="cb2cb-118">Payroll allocation</span></span>
        - <span data-ttu-id="cb2cb-119">VIA – kostverdi</span><span class="sxs-lookup"><span data-stu-id="cb2cb-119">WIP-cost value</span></span>
        - <span data-ttu-id="cb2cb-120">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="cb2cb-120">Cost-item</span></span>
        - <span data-ttu-id="cb2cb-121">VIA-kostnadsverdielement</span><span class="sxs-lookup"><span data-stu-id="cb2cb-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="cb2cb-122">Påløpt tap</span><span class="sxs-lookup"><span data-stu-id="cb2cb-122">Accrued loss</span></span>
        - <span data-ttu-id="cb2cb-123">VIA – påløpt tap</span><span class="sxs-lookup"><span data-stu-id="cb2cb-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="cb2cb-124">Hvilke omsetningskontoer skal brukes for følgende omsetningskilder?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="cb2cb-125">Fakturert omsetning</span><span class="sxs-lookup"><span data-stu-id="cb2cb-125">Invoiced revenue</span></span>
        - <span data-ttu-id="cb2cb-126">Påløpt omsetning – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="cb2cb-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="cb2cb-127">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="cb2cb-127">WIP-sales value</span></span>
        - <span data-ttu-id="cb2cb-128">Påløpt omsetning – produksjon</span><span class="sxs-lookup"><span data-stu-id="cb2cb-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="cb2cb-129">VIA – produksjon</span><span class="sxs-lookup"><span data-stu-id="cb2cb-129">WIP-production</span></span>
        - <span data-ttu-id="cb2cb-130">Påløpt omsetning – fortjeneste</span><span class="sxs-lookup"><span data-stu-id="cb2cb-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="cb2cb-131">VIA – fortjeneste</span><span class="sxs-lookup"><span data-stu-id="cb2cb-131">WIP-profit</span></span>
        - <span data-ttu-id="cb2cb-132">Påløpt omsetning – abonnement</span><span class="sxs-lookup"><span data-stu-id="cb2cb-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="cb2cb-133">VIA – abonnement</span><span class="sxs-lookup"><span data-stu-id="cb2cb-133">WIP-subscription</span></span>

- <span data-ttu-id="cb2cb-134">Hva er utgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-134">What is the expense type?</span></span>
- <span data-ttu-id="cb2cb-135">Hva er standard betalingsmetode for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="cb2cb-136">Må utgifter i utgiftskategorien være spesifiserte?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="cb2cb-137">Hva er standard hovedkonto for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="cb2cb-138">Hva er standard mva-gruppe for varesalg for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="cb2cb-139">Er det tillatt med flere betalingsmetoder for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="cb2cb-140">I så fall, hvilke?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-140">If so, what are they?</span></span>
- <span data-ttu-id="cb2cb-141">Finnes det underkategorier i utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="cb2cb-142">Hvis det finnes underkategorier, må du også ta følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="cb2cb-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="cb2cb-143">Er noen av underkategoriene utelukket fra avgiftsfradrag?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="cb2cb-144">Hva er mva-gruppen for varesalg for underkategoriene?</span><span class="sxs-lookup"><span data-stu-id="cb2cb-144">What is the item sales tax group of the subcategories?</span></span>
