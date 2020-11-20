---
title: Oversikt over faktiske verdier
description: Denne emnet gir informasjon om faktiske verdier for prosjekter.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129780"
---
# <a name="actuals-overview"></a><span data-ttu-id="01018-103">Oversikt over faktiske verdier</span><span class="sxs-lookup"><span data-stu-id="01018-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="01018-104">Faktiske verdier er mengden arbeid som er fullført på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="01018-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="01018-105">Faktiske verdier for prosjekter kan spores tilbake til kildedokumentene.</span><span class="sxs-lookup"><span data-stu-id="01018-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="01018-106">Disse kildedokumentene inneholder time-, utgifts- og journaloppføringer, og også fakturaer.</span><span class="sxs-lookup"><span data-stu-id="01018-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Hvordan faktiske verdier for prosjekter spores i kildedokumenter](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="01018-108">Sende inn en tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="01018-108">Submitting a time entry</span></span>

<span data-ttu-id="01018-109">Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer.</span><span class="sxs-lookup"><span data-stu-id="01018-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="01018-110">Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg.</span><span class="sxs-lookup"><span data-stu-id="01018-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="01018-111">Når en tidsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad.</span><span class="sxs-lookup"><span data-stu-id="01018-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="01018-112">Logikk for angivelse av standardpriser finnes på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="01018-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="01018-113">Alle feltverdiene fra en tidsoppføring kopieres til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="01018-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="01018-114">Disse feltene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="01018-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="01018-115">Feltene som påvirker standardpriser, for eksempel **Rolle** og **Organisasjonsenhet**, fører til at en passende pris registreres som standard på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="01018-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="01018-116">Hvis du legger til et egendefinert felt for tidsoppføringen, og du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet på den faktiske enheten og bruker felttilordninger til å kopiere feltet fra tidsoppføringen til den faktiske verdien.</span><span class="sxs-lookup"><span data-stu-id="01018-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="01018-117">Sende en utgiftsoppføring</span><span class="sxs-lookup"><span data-stu-id="01018-117">Submitting an expense entry</span></span>

<span data-ttu-id="01018-118">Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for tid og materialer i PSA, opprettes det to journallinjer.</span><span class="sxs-lookup"><span data-stu-id="01018-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="01018-119">Den ene linje gjelder kostnad, og den andre linjen er for ikke-fakturert salg.</span><span class="sxs-lookup"><span data-stu-id="01018-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="01018-120">Når en utgiftsoppføring sendes til et prosjekt som er tilordnet en kontraktlinje for fast pris, opprettes det en journallinje bare for kostnad.</span><span class="sxs-lookup"><span data-stu-id="01018-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="01018-121">Logikk for angivelse av standardpriser for utgifter er basert på utgiftskategorien som er valgt på siden **Utgiftsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="01018-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="01018-122">Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="01018-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="01018-123">For selve prisen blir imidlertid beløpet som brukeren angav, angitt direkte på de relaterte utgiftsjournallinjene for kostnad og salg som standard.</span><span class="sxs-lookup"><span data-stu-id="01018-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="01018-124">I den gjeldende versjonen av PSA er kategoribasert oppføring av standard priser per enhet på utgiftsoppføringer ikke tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="01018-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="01018-125">Bruke oppføringsjournaler til å registrere kostnader</span><span class="sxs-lookup"><span data-stu-id="01018-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="01018-126">I PSA gir oppføringsjournaler deg tilgang til å registrere kostnad eller omsetninger i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift.</span><span class="sxs-lookup"><span data-stu-id="01018-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="01018-127">En journal har et hode, linjer og en **bekreftelseshandling**.</span><span class="sxs-lookup"><span data-stu-id="01018-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="01018-128">Her er noen scenarioer der du kan bruke en journal:</span><span class="sxs-lookup"><span data-stu-id="01018-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="01018-129">Du må registrere faktiske kostnader og salg for materialer på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="01018-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="01018-130">Du må flytte de faktiske transaksjonstransaksjonene fra et annet system til PSA.</span><span class="sxs-lookup"><span data-stu-id="01018-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="01018-131">Du må registrere kostnader som har oppstått i et annet system, for eksempel innkjøps- eller underleveransekostnader.</span><span class="sxs-lookup"><span data-stu-id="01018-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01018-132">Bruk av oppføringsjournaler til å opprette faktiske verdier bør bare utføres av en bruker som er helt oppmerksom på den regnskapsmessige innvirkningen de faktiske verdiene har på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="01018-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="01018-133">Dette skyldes at programmet ikke validerer journallinjetypen eller den relaterte prissettingen som er angitt på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="01018-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="01018-134">På grunn av virkningen av denne journaltypen må du være forsiktig med hvem som gis tilgang til å opprette oppføringsjournaler.</span><span class="sxs-lookup"><span data-stu-id="01018-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="01018-135">Registrere faktiske verdier basert på prosjekthendelser</span><span class="sxs-lookup"><span data-stu-id="01018-135">Recording actuals based on project events</span></span>

<span data-ttu-id="01018-136">PSA registrerer de finansielle transaksjonene som inntreffer under et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="01018-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="01018-137">Disse transaksjonene registreres som **faktiske verdier**.</span><span class="sxs-lookup"><span data-stu-id="01018-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="01018-138">Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="01018-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="01018-139">**Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet**</span><span class="sxs-lookup"><span data-stu-id="01018-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="01018-140">Hendelse</span><span class="sxs-lookup"><span data-stu-id="01018-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="01018-141">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="01018-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="01018-142">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="01018-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="01018-143">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="01018-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="01018-144">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="01018-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="01018-145">Fast pris</span><span class="sxs-lookup"><span data-stu-id="01018-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="01018-146">Faktisk</span><span class="sxs-lookup"><span data-stu-id="01018-146">Actuals</span></span></th>
<th><span data-ttu-id="01018-147">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="01018-147">Transaction currency</span></span></th>
<th><span data-ttu-id="01018-148">Fast pris</span><span class="sxs-lookup"><span data-stu-id="01018-148">Fixed price</span></span></th>
<th><span data-ttu-id="01018-149">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="01018-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="01018-150">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="01018-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="01018-151">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="01018-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-152">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="01018-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="01018-153">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="01018-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01018-154">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="01018-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01018-155">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-155">Cost actual</span></span></td>
<td><span data-ttu-id="01018-156">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-157">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-158">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="01018-159">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-160">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-161">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="01018-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="01018-162">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01018-163">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="01018-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01018-164">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-164">Cost actual</span></span></td>
<td><span data-ttu-id="01018-165">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-166">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-167">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-168">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-169">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-170">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01018-171">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-172">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-173">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01018-174">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="01018-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01018-175">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="01018-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01018-176">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-177">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="01018-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-178">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-179">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-180">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-181">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="01018-181">Billed sales</span></span></td>
<td><span data-ttu-id="01018-182">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01018-183">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="01018-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01018-184">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="01018-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01018-185">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-186">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-187">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-188">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-189">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-190">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01018-191">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-192">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-193">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01018-194">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="01018-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01018-195">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="01018-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01018-196">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="01018-197">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="01018-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="01018-198">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="01018-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="01018-199">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-200">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-201">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-202">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="01018-202">Billed sales</span></span></td>
<td><span data-ttu-id="01018-203">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01018-204">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="01018-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01018-205">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="01018-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01018-206">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-207">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="01018-208">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-209">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-210">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="01018-211">**Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet**</span><span class="sxs-lookup"><span data-stu-id="01018-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="01018-212">Hendelse</span><span class="sxs-lookup"><span data-stu-id="01018-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="01018-213">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="01018-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="01018-214">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="01018-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="01018-215">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="01018-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="01018-216">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="01018-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="01018-217">Fast pris</span><span class="sxs-lookup"><span data-stu-id="01018-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="01018-218">Faktisk</span><span class="sxs-lookup"><span data-stu-id="01018-218">Actuals</span></span></th>
<th><span data-ttu-id="01018-219">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="01018-219">Transaction currency</span></span></th>
<th><span data-ttu-id="01018-220">Fast pris</span><span class="sxs-lookup"><span data-stu-id="01018-220">Fixed price</span></span></th>
<th><span data-ttu-id="01018-221">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="01018-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="01018-222">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="01018-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="01018-223">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="01018-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-224">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="01018-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="01018-225">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="01018-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="01018-226">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="01018-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01018-227">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-227">Cost actual</span></span></td>
<td><span data-ttu-id="01018-228">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="01018-229">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="01018-230">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="01018-231">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="01018-232">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-233">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="01018-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="01018-234">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-235">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="01018-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="01018-236">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="01018-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-237">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="01018-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="01018-238">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="01018-239">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="01018-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="01018-240">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-240">Cost actual</span></span></td>
<td><span data-ttu-id="01018-241">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-242">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-243">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-244">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-245">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="01018-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-246">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="01018-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="01018-247">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="01018-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-248">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="01018-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="01018-249">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="01018-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-250">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01018-251">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-252">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-253">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01018-254">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="01018-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01018-255">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="01018-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01018-256">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-257">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="01018-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-258">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-259">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="01018-260">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-261">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="01018-261">Billed sales</span></span></td>
<td><span data-ttu-id="01018-262">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01018-263">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="01018-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="01018-264">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="01018-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="01018-265">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-266">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-267">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-268">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="01018-269">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-270">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="01018-271">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-272">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-273">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="01018-274">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="01018-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01018-275">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="01018-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01018-276">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="01018-277">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="01018-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="01018-278">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="01018-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="01018-279">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-280">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="01018-281">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="01018-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-282">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="01018-282">Billed sales</span></span></td>
<td><span data-ttu-id="01018-283">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="01018-284">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="01018-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="01018-285">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="01018-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="01018-286">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-287">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="01018-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="01018-288">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="01018-289">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="01018-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="01018-290">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="01018-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
