---
title: Faktiske verdier
description: Dette emnet gir informasjon om å arbeide med faktiske verdier i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081610"
---
# <a name="actuals"></a><span data-ttu-id="17938-103">Faktiske verdier</span><span class="sxs-lookup"><span data-stu-id="17938-103">Actuals</span></span> 

<span data-ttu-id="17938-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="17938-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="17938-105">Faktiske verdier er mengden arbeid som er fullført på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17938-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="17938-106">De opprettes som et resultat av tids- og utgiftsoppføringer og journaloppføringer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="17938-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="17938-107">Journallinjer og tidssending</span><span class="sxs-lookup"><span data-stu-id="17938-107">Journal lines and time submission</span></span>

<span data-ttu-id="17938-108">Hvis du vil ha mer informasjon om tidsregistrering, kan du se [Oversikt over tidsregistrering](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="17938-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="17938-109">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="17938-109">Time and materials</span></span>

<span data-ttu-id="17938-110">Når en tidsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.</span><span class="sxs-lookup"><span data-stu-id="17938-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="17938-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-111">Fixed price</span></span>

<span data-ttu-id="17938-112">Når en tidsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.</span><span class="sxs-lookup"><span data-stu-id="17938-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="17938-113">Standardprising</span><span class="sxs-lookup"><span data-stu-id="17938-113">Default pricing</span></span>

<span data-ttu-id="17938-114">Logikken for oppretting av standardpriser finnes på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="17938-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="17938-115">Feltverdiene fra tidsoppføringen kopieres til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="17938-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="17938-116">Disse verdiene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="17938-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="17938-117">Feltene som påvirker standardprising, for eksempel **Rolle** og **Organisasjonsenhet** , brukes til å bestemme den passende prisen på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="17938-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="17938-118">Du kan legge til et egendefinert felt for tidsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="17938-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="17938-119">Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet på den faktiske enheten og bruker felttilordninger til å kopiere feltet fra tidsoppføringen til den faktiske verdien.</span><span class="sxs-lookup"><span data-stu-id="17938-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="17938-120">Journallinjer og sending av grunnleggende utgifter</span><span class="sxs-lookup"><span data-stu-id="17938-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="17938-121">Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Oversikt over utgifter](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="17938-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="17938-122">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="17938-122">Time and materials</span></span>

<span data-ttu-id="17938-123">Når en grunnleggende utgiftsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.</span><span class="sxs-lookup"><span data-stu-id="17938-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="17938-124">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-124">Fixed price</span></span>

<span data-ttu-id="17938-125">Når en grunnleggende utgiftsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.</span><span class="sxs-lookup"><span data-stu-id="17938-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="17938-126">Standardprising</span><span class="sxs-lookup"><span data-stu-id="17938-126">Default pricing</span></span>

<span data-ttu-id="17938-127">Logikken for å angi standardpriser for utgifter er basert på utgiftskategorien.</span><span class="sxs-lookup"><span data-stu-id="17938-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="17938-128">Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="17938-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="17938-129">Beløpet som er angitt for selve prisen, blir imidlertid som standard angitt direkte på de relaterte utgiftsjournallinjene for kostnad og salg som standard.</span><span class="sxs-lookup"><span data-stu-id="17938-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="17938-130">Kategoribasert oppføring av standardpriser per enhet på utgiftsoppføringer er ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="17938-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="17938-131">Bruk oppføringsjournaler til å registrere kostnader</span><span class="sxs-lookup"><span data-stu-id="17938-131">Use entry journals to record costs</span></span>

<span data-ttu-id="17938-132">Du kan bruke oppføringsjournaler til å registrere kostnad eller omsetning i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift.</span><span class="sxs-lookup"><span data-stu-id="17938-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="17938-133">Journaler kan brukes til følgende formål:</span><span class="sxs-lookup"><span data-stu-id="17938-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="17938-134">Registrer de faktiske kostnadene for materialer og salg på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17938-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="17938-135">Flytt faktiske verdier for transaksjoner fra et annet system til Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="17938-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="17938-136">Registrer kostnader som er påløpt i et annet system.</span><span class="sxs-lookup"><span data-stu-id="17938-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="17938-137">Disse kostnadene kan omfatte innkjøps- eller underleveransekostnader.</span><span class="sxs-lookup"><span data-stu-id="17938-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17938-138">Programmet validerer ikke journallinjetypen eller den relaterte prisingen som er angitt på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="17938-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="17938-139">Derfor bør bare en bruker som er fullstendig klar over regnskapsinnvirkningen de faktiske verdiene har på prosjektet, bruke oppføringsjournaler til å opprette faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="17938-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="17938-140">På grunn av innvirkningen til denne journaltypen bør du være nøye når du skal velge hvem som skal ha tilgang til å opprette oppføringsjournaler.</span><span class="sxs-lookup"><span data-stu-id="17938-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="17938-141">Registrer faktiske verdier basert på prosjekthendelser</span><span class="sxs-lookup"><span data-stu-id="17938-141">Record actuals based on project events</span></span>

<span data-ttu-id="17938-142">Project Operations registrerer de finansielle transaksjonene som inntreffer under et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17938-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="17938-143">Disse transaksjonene registreres som faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="17938-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="17938-144">Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="17938-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="17938-145">Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet</span><span class="sxs-lookup"><span data-stu-id="17938-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="17938-146">Hendelse</span><span class="sxs-lookup"><span data-stu-id="17938-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="17938-147">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="17938-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="17938-148">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="17938-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="17938-149">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="17938-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="17938-150">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="17938-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="17938-151">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="17938-152">Faktisk</span><span class="sxs-lookup"><span data-stu-id="17938-152">Actuals</span></span></th>
<th><span data-ttu-id="17938-153">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="17938-153">Transaction currency</span></span></th>
<th><span data-ttu-id="17938-154">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-154">Fixed price</span></span></th>
<th><span data-ttu-id="17938-155">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="17938-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="17938-156">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="17938-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="17938-157">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="17938-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-158">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="17938-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="17938-159">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="17938-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="17938-160">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="17938-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="17938-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-161">Cost actual</span></span></td>
<td><span data-ttu-id="17938-162">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-164">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="17938-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-167">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="17938-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="17938-168">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="17938-169">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="17938-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="17938-170">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-170">Cost actual</span></span></td>
<td><span data-ttu-id="17938-171">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-172">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-173">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-174">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-175">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-176">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="17938-177">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-178">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-179">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="17938-180">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="17938-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="17938-181">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="17938-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="17938-182">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-183">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="17938-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-184">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-185">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-186">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-187">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="17938-187">Billed sales</span></span></td>
<td><span data-ttu-id="17938-188">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="17938-189">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="17938-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="17938-190">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="17938-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="17938-191">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-192">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-193">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-194">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-195">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-196">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="17938-197">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-198">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-199">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="17938-200">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="17938-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="17938-201">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="17938-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="17938-202">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="17938-203">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="17938-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="17938-204">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="17938-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="17938-205">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-206">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-207">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-208">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="17938-208">Billed sales</span></span></td>
<td><span data-ttu-id="17938-209">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="17938-210">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="17938-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="17938-211">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="17938-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="17938-212">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-213">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="17938-214">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-215">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-216">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="17938-217">Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet</span><span class="sxs-lookup"><span data-stu-id="17938-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="17938-218">Hendelse</span><span class="sxs-lookup"><span data-stu-id="17938-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="17938-219">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="17938-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="17938-220">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="17938-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="17938-221">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="17938-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="17938-222">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="17938-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="17938-223">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="17938-224">Faktisk</span><span class="sxs-lookup"><span data-stu-id="17938-224">Actuals</span></span></th>
<th><span data-ttu-id="17938-225">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="17938-225">Transaction currency</span></span></th>
<th><span data-ttu-id="17938-226">Fast pris</span><span class="sxs-lookup"><span data-stu-id="17938-226">Fixed price</span></span></th>
<th><span data-ttu-id="17938-227">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="17938-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="17938-228">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="17938-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="17938-229">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="17938-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-230">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="17938-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="17938-231">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="17938-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="17938-232">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="17938-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="17938-233">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-233">Cost actual</span></span></td>
<td><span data-ttu-id="17938-234">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="17938-235">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="17938-236">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="17938-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="17938-238">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-239">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="17938-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="17938-240">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-241">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="17938-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="17938-242">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="17938-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-243">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="17938-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="17938-244">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="17938-245">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="17938-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="17938-246">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-246">Cost actual</span></span></td>
<td><span data-ttu-id="17938-247">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-248">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-249">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-250">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-251">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="17938-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-252">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="17938-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="17938-253">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="17938-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-254">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="17938-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="17938-255">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="17938-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-256">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="17938-257">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-258">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-259">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="17938-260">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="17938-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="17938-261">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="17938-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="17938-262">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-263">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="17938-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-264">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-265">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="17938-266">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-267">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="17938-267">Billed sales</span></span></td>
<td><span data-ttu-id="17938-268">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="17938-269">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="17938-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="17938-270">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="17938-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="17938-271">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-272">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-273">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-274">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="17938-275">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-276">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="17938-277">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-278">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-279">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="17938-280">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="17938-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="17938-281">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="17938-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="17938-282">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="17938-283">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="17938-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="17938-284">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="17938-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="17938-285">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-286">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="17938-287">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="17938-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-288">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="17938-288">Billed sales</span></span></td>
<td><span data-ttu-id="17938-289">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="17938-290">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="17938-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="17938-291">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="17938-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="17938-292">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-293">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="17938-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="17938-294">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="17938-295">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="17938-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="17938-296">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="17938-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
