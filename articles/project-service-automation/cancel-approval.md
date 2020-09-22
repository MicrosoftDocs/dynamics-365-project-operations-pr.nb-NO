---
title: Avbryte tidligere godkjente tids- og utgiftsoppføringer
description: Dette emnet gir informasjon om hvordan du annullerer en godkjent prosjekttid og en utgiftstransaksjon.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754030"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="c189b-103">Avbryte tidligere godkjente tids- eller utgiftsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c189b-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c189b-104">I den nyeste versjonen av Dynamics 365 Project Service Automation kan godkjennere annullere tids- eller utgiftsoppføringer de tidligere har godkjent.</span><span class="sxs-lookup"><span data-stu-id="c189b-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="c189b-105">Avbryte en tidliger godkjent tids- eller utgiftsoppføring</span><span class="sxs-lookup"><span data-stu-id="c189b-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="c189b-106">Følg disse trinnene for å annullere en tids- eller utgiftsoppføring du har godkjent tidligere.</span><span class="sxs-lookup"><span data-stu-id="c189b-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="c189b-107">Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="c189b-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="c189b-108">På listesiden **Godkjenninger** endrer du visningen til **Mine tidligere godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="c189b-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="c189b-109">En liste over tids- og utgiftsoppføringene du godkjente tidligere, vises.</span><span class="sxs-lookup"><span data-stu-id="c189b-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="c189b-110">Velg én eller flere oppføringer, og velg deretter **Kanseller godkjenning**.</span><span class="sxs-lookup"><span data-stu-id="c189b-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="c189b-111">Du får en varselsmelding.</span><span class="sxs-lookup"><span data-stu-id="c189b-111">You receive a warning message.</span></span>
4. <span data-ttu-id="c189b-112">Velg **OK** for å annullere godkjenningen.</span><span class="sxs-lookup"><span data-stu-id="c189b-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="c189b-113">Forstå virkningen av å annullere godkjenning av en tids- eller godkjenningsoppføring</span><span class="sxs-lookup"><span data-stu-id="c189b-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="c189b-114">Når en godkjenning annulleres, får dette både driftsinnvirkning og finansiell innvirkning.</span><span class="sxs-lookup"><span data-stu-id="c189b-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="c189b-115">Driftsinnvirkning</span><span class="sxs-lookup"><span data-stu-id="c189b-115">Operational impact</span></span>

<span data-ttu-id="c189b-116">På driftssiden, når en godkjenning annulleres, tilbakestilles statusen for oppføringen til **Utkast**, og godkjenningen vises ikke lenger i visningen **Mine tidligere godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="c189b-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="c189b-117">I stedet vises den annullerte godkjenningen i visningen **Tidsoppføringer for godkjenning** eller **Utgiftsoppføringer for godkjenning**, avhengig av om den var en tidsoppføring eller en utgiftsoppføring.</span><span class="sxs-lookup"><span data-stu-id="c189b-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="c189b-118">I tillegg endres statusen for den relaterte tids- eller utgiftsoppføringen til **Sendt**, slik at den relaterte oppføringen samsvarer med godkjenninger som har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="c189b-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="c189b-119">Som godkjenner kan du redigere noen av feltene i en godkjenning som har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="c189b-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="c189b-120">Disse feltene inkluderer **Faktureringstype** og **Fakturerbare timer for tidsoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="c189b-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="c189b-121">Når du har gjort endringer, kan du godkjenne oppføringen på nytt.</span><span class="sxs-lookup"><span data-stu-id="c189b-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="c189b-122">Du kan også avvise oppføringen.</span><span class="sxs-lookup"><span data-stu-id="c189b-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="c189b-123">Hvis du avviser godkjenningen av en tidsoppføring, blir statusen for oppføringen endret til **Returnert**.</span><span class="sxs-lookup"><span data-stu-id="c189b-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="c189b-124">Hvis du avviser godkjenningen av en utgiftsoppføring, blir statusen endret til **Avvist**.</span><span class="sxs-lookup"><span data-stu-id="c189b-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="c189b-125">Det vil si at både returnerte og avviste oppføringer fungerer på samme måte som en oppføring som har statusen **Utkast**.</span><span class="sxs-lookup"><span data-stu-id="c189b-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="c189b-126">Et prosjektteammedlem kan enten gjøre de nødvendige endringene i oppføringen og deretter sende den på nytt for godkjenning, eller slette oppføringen helt.</span><span class="sxs-lookup"><span data-stu-id="c189b-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="c189b-127">Økonomisk innvirkning</span><span class="sxs-lookup"><span data-stu-id="c189b-127">Financial impact</span></span>

<span data-ttu-id="c189b-128">Et prosjekt berøres også finansielt når en godkjenning annulleres.</span><span class="sxs-lookup"><span data-stu-id="c189b-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="c189b-129">For det første oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="c189b-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="c189b-130">Justeringsstatusen settes til **Justert**.</span><span class="sxs-lookup"><span data-stu-id="c189b-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="c189b-131">Faktureringsstatusen settes til **Kansellert**.</span><span class="sxs-lookup"><span data-stu-id="c189b-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="c189b-132">Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="c189b-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="c189b-133">For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene.</span><span class="sxs-lookup"><span data-stu-id="c189b-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="c189b-134">De eneste verdiene som ikke kopieres over, er antallsverdiene.</span><span class="sxs-lookup"><span data-stu-id="c189b-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="c189b-135">Disse verdiene reverseres i stedet.</span><span class="sxs-lookup"><span data-stu-id="c189b-135">These values are reversed instead.</span></span> <span data-ttu-id="c189b-136">Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**.</span><span class="sxs-lookup"><span data-stu-id="c189b-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="c189b-137">Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres**, og faktureringsstatusen settes til **Annullert**.</span><span class="sxs-lookup"><span data-stu-id="c189b-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="c189b-138">Når du har gjort disse endringene, vil beløpet som er registrert som brukt på prosjektet, og restinntekten for prosjektet, ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.</span><span class="sxs-lookup"><span data-stu-id="c189b-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
