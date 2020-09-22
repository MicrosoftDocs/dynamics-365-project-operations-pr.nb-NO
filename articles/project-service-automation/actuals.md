---
title: Faktisk
description: Denne emnet gir informasjon om faktiske verdier for prosjekter.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754178"
---
# <a name="actuals"></a><span data-ttu-id="a8c49-103">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a8c49-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a8c49-104">Faktiske verdier er mengden arbeid som er fullført på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8c49-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a8c49-105">Faktiske verdier for prosjekter kan spores tilbake til kildedokumentene.</span><span class="sxs-lookup"><span data-stu-id="a8c49-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a8c49-106">Disse kildedokumentene inneholder time-, utgifts- og journaloppføringer, og også fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a8c49-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hvordan faktiske verdier for prosjekter spores i kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a8c49-108">Sende inn en tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-108">Submitting a time entry</span></span>

<span data-ttu-id="a8c49-109">Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer.</span><span class="sxs-lookup"><span data-stu-id="a8c49-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a8c49-110">Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg.</span><span class="sxs-lookup"><span data-stu-id="a8c49-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a8c49-111">Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad.</span><span class="sxs-lookup"><span data-stu-id="a8c49-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a8c49-112">Logikk for angivelse av standardpriser finnes på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a8c49-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a8c49-113">Alle feltverdiene fra en tidsoppføring kopieres til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a8c49-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a8c49-114">Disse feltene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="a8c49-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a8c49-115">Feltene som påvirker standardpriser, for eksempel **Rolle** og **Organisasjonsenhet**, fører til at en passende pris registreres som standard på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a8c49-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a8c49-116">Hvis du legger til et egendefinert felt for tidsoppføringen, og du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet på den faktiske enheten og bruker felttilordninger til å kopiere feltet fra tidsoppføringen til den faktiske verdien.</span><span class="sxs-lookup"><span data-stu-id="a8c49-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a8c49-117">Sende en utgiftsoppføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-117">Submitting an expense entry</span></span>

<span data-ttu-id="a8c49-118">Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer.</span><span class="sxs-lookup"><span data-stu-id="a8c49-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a8c49-119">Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg.</span><span class="sxs-lookup"><span data-stu-id="a8c49-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a8c49-120">Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad.</span><span class="sxs-lookup"><span data-stu-id="a8c49-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a8c49-121">Logikk for angivelse av standardpriser for utgifter er basert på utgiftskategorien som er valgt på siden **Utgiftsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="a8c49-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a8c49-122">Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="a8c49-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a8c49-123">For selve prisen blir imidlertid beløpet som brukeren angav, angitt direkte på de relaterte utgiftsjournallinjene for kostnad og salg som standard.</span><span class="sxs-lookup"><span data-stu-id="a8c49-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a8c49-124">I den gjeldende versjonen av PSA er kategoribasert oppføring av standard priser per enhet på utgiftsoppføringer ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="a8c49-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="a8c49-125">Bruke journaler til å registrere kostnader</span><span class="sxs-lookup"><span data-stu-id="a8c49-125">Using journals to record costs</span></span>

<span data-ttu-id="a8c49-126">I PSA kan du registrere kostnader eller omsetninger i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift.</span><span class="sxs-lookup"><span data-stu-id="a8c49-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a8c49-127">En journal har et hode, linjer og en **bekreftelseshandling**.</span><span class="sxs-lookup"><span data-stu-id="a8c49-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a8c49-128">Her er noen scenarioer der du kan bruke en journal:</span><span class="sxs-lookup"><span data-stu-id="a8c49-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a8c49-129">Du må registrere faktiske kostnader og salg for materialer på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8c49-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a8c49-130">Du må flytte de faktiske transaksjonstransaksjonene fra et annet system til PSA.</span><span class="sxs-lookup"><span data-stu-id="a8c49-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a8c49-131">Du må registrere kostnader som har oppstått i et annet system, for eksempel innkjøps- eller underleveransekostnader.</span><span class="sxs-lookup"><span data-stu-id="a8c49-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a8c49-132">Registrere faktiske verdier basert på prosjekthendelser</span><span class="sxs-lookup"><span data-stu-id="a8c49-132">Recording actuals based on project events</span></span>

<span data-ttu-id="a8c49-133">PSA registrerer de finansielle transaksjonene som inntreffer under et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8c49-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a8c49-134">Disse transaksjonene registreres som **faktiske verdier**.</span><span class="sxs-lookup"><span data-stu-id="a8c49-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a8c49-135">Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8c49-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a8c49-136">**Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet**</span><span class="sxs-lookup"><span data-stu-id="a8c49-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a8c49-137">Hendelse</span><span class="sxs-lookup"><span data-stu-id="a8c49-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a8c49-138">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a8c49-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c49-139">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="a8c49-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c49-140">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a8c49-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a8c49-141">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a8c49-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a8c49-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c49-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8c49-143">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a8c49-143">Actuals</span></span></th>
<th><span data-ttu-id="a8c49-144">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c49-144">Transaction currency</span></span></th>
<th><span data-ttu-id="a8c49-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c49-145">Fixed price</span></span></th>
<th><span data-ttu-id="a8c49-146">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c49-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8c49-147">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="a8c49-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c49-148">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a8c49-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-149">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="a8c49-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c49-150">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a8c49-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c49-151">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a8c49-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c49-152">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-152">Cost actual</span></span></td>
<td><span data-ttu-id="a8c49-153">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-154">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-155">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a8c49-156">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-158">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="a8c49-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a8c49-159">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c49-160">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a8c49-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c49-161">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-161">Cost actual</span></span></td>
<td><span data-ttu-id="a8c49-162">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-163">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-164">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-165">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-167">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-168">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-169">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-170">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c49-171">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a8c49-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c49-172">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a8c49-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c49-173">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-174">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a8c49-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-175">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-176">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-177">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-178">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a8c49-178">Billed sales</span></span></td>
<td><span data-ttu-id="a8c49-179">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c49-180">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a8c49-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c49-181">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a8c49-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c49-182">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-183">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-184">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-185">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-186">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-187">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-188">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-189">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-190">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c49-191">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a8c49-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c49-192">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c49-193">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a8c49-194">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a8c49-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a8c49-195">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a8c49-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a8c49-196">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-197">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-198">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-199">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a8c49-199">Billed sales</span></span></td>
<td><span data-ttu-id="a8c49-200">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c49-201">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a8c49-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c49-202">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c49-203">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-204">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-205">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-206">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-207">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a8c49-208">**Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet**</span><span class="sxs-lookup"><span data-stu-id="a8c49-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a8c49-209">Hendelse</span><span class="sxs-lookup"><span data-stu-id="a8c49-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a8c49-210">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a8c49-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c49-211">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="a8c49-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a8c49-212">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a8c49-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a8c49-213">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a8c49-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a8c49-214">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c49-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a8c49-215">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a8c49-215">Actuals</span></span></th>
<th><span data-ttu-id="a8c49-216">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c49-216">Transaction currency</span></span></th>
<th><span data-ttu-id="a8c49-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a8c49-217">Fixed price</span></span></th>
<th><span data-ttu-id="a8c49-218">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a8c49-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a8c49-219">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="a8c49-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c49-220">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a8c49-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-221">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="a8c49-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a8c49-222">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a8c49-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a8c49-223">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a8c49-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c49-224">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-224">Cost actual</span></span></td>
<td><span data-ttu-id="a8c49-225">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c49-226">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c49-227">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c49-228">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a8c49-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-230">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="a8c49-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a8c49-231">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-232">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a8c49-233">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-234">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a8c49-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a8c49-235">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a8c49-236">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a8c49-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a8c49-237">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-237">Cost actual</span></span></td>
<td><span data-ttu-id="a8c49-238">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-239">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-240">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-241">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a8c49-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-243">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a8c49-244">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-245">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a8c49-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a8c49-246">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a8c49-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-247">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-248">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-249">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-250">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c49-251">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a8c49-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c49-252">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a8c49-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c49-253">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-254">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a8c49-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-255">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-256">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a8c49-257">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-258">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a8c49-258">Billed sales</span></span></td>
<td><span data-ttu-id="a8c49-259">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c49-260">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a8c49-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a8c49-261">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a8c49-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a8c49-262">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-263">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-264">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-265">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a8c49-266">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-267">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-268">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-269">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-270">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a8c49-271">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a8c49-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c49-272">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c49-273">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a8c49-274">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a8c49-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a8c49-275">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a8c49-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a8c49-276">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-277">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a8c49-278">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a8c49-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-279">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a8c49-279">Billed sales</span></span></td>
<td><span data-ttu-id="a8c49-280">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a8c49-281">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a8c49-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a8c49-282">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a8c49-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a8c49-283">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-284">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a8c49-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a8c49-285">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a8c49-286">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a8c49-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a8c49-287">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a8c49-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
