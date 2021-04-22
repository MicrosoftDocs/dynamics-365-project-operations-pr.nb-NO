---
title: Faktiske verdier
description: Denne emne inneholder informasjon om hvordan du arbeider med faktiske verdier i Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 304c51a4e502ad6ecec1fd821e98d6604ddd59ba
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852556"
---
# <a name="actuals"></a><span data-ttu-id="a1232-103">Faktiske verdier</span><span class="sxs-lookup"><span data-stu-id="a1232-103">Actuals</span></span> 

<span data-ttu-id="a1232-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a1232-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a1232-105">Faktiske verdier representerer den gjennomgåtte og godkjente økonomiske og planlagte fremdriften for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a1232-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="a1232-106">De opprettes som et resultat av godkjenning av tid, utgifter, materialbruksoppføringer og loggoppføringer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a1232-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="a1232-107">Journallinjer og tidssending</span><span class="sxs-lookup"><span data-stu-id="a1232-107">Journal lines and time submission</span></span>

<span data-ttu-id="a1232-108">Hvis du vil ha mer informasjon om tidsregistrering, kan du se [Oversikt over tidsregistrering](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1232-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a1232-109">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a1232-109">Time and materials</span></span>

<span data-ttu-id="a1232-110">Når en tidsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.</span><span class="sxs-lookup"><span data-stu-id="a1232-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a1232-111">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-111">Fixed price</span></span>

<span data-ttu-id="a1232-112">Når en tidsoppføring som er sendt, kobles til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.</span><span class="sxs-lookup"><span data-stu-id="a1232-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a1232-113">Standardprising</span><span class="sxs-lookup"><span data-stu-id="a1232-113">Default pricing</span></span>

<span data-ttu-id="a1232-114">Logikken for oppretting av standardpriser finnes på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="a1232-115">Feltverdiene fra tidsoppføringen kopieres til journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="a1232-116">Disse verdiene inneholder transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet i den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="a1232-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="a1232-117">Feltene som påvirker standardpriser, for eksempel **Rolle** og **Ressursenhet**, brukes til å bestemme passende pris på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a1232-118">Du kan legge til et egendefinert felt for tidsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="a1232-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="a1232-119">Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**.</span><span class="sxs-lookup"><span data-stu-id="a1232-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a1232-120">Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav.</span><span class="sxs-lookup"><span data-stu-id="a1232-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a1232-121">Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a1232-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="a1232-122">Journallinjer og sending av grunnleggende utgifter</span><span class="sxs-lookup"><span data-stu-id="a1232-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="a1232-123">Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Oversikt over utgifter](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a1232-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a1232-124">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a1232-124">Time and materials</span></span>

<span data-ttu-id="a1232-125">Når en grunnleggende utgiftsregistrering som er sendt, er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materialer, oppretter systemet to journallinjer, én for kostnad og én for ufakturert salg.</span><span class="sxs-lookup"><span data-stu-id="a1232-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a1232-126">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-126">Fixed price</span></span>

<span data-ttu-id="a1232-127">Når en innsendt enkel utgiftsoppføring er knyttet til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.</span><span class="sxs-lookup"><span data-stu-id="a1232-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a1232-128">Standardprising</span><span class="sxs-lookup"><span data-stu-id="a1232-128">Default pricing</span></span>

<span data-ttu-id="a1232-129">Logikken for å angi standardpriser for utgifter er basert på utgiftskategorien.</span><span class="sxs-lookup"><span data-stu-id="a1232-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="a1232-130">Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="a1232-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a1232-131">Feltene som påvirker standardpriser, for eksempel **Transaksjonskategori** og **Enhet**, brukes til å bestemme passende pris på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a1232-132">Dette fungerer imidlertid bare når prismodellen i prislisten er **Pris per enhet**.</span><span class="sxs-lookup"><span data-stu-id="a1232-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="a1232-133">Hvis prismetoden er **Kostpris** eller **Påslag over kostnad**, blir prisen som angis når utgiftsoppføringen opprettes, brukt til kostnad, og prisen på salgsjournallinjen beregnes basert på prismetoden.</span><span class="sxs-lookup"><span data-stu-id="a1232-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="a1232-134">Du kan legge til et egendefinert felt i utgiftsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="a1232-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="a1232-135">Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**.</span><span class="sxs-lookup"><span data-stu-id="a1232-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a1232-136">Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav.</span><span class="sxs-lookup"><span data-stu-id="a1232-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a1232-137">Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a1232-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="a1232-138">Innsending av journallinjer og materialbrukslogg</span><span class="sxs-lookup"><span data-stu-id="a1232-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="a1232-139">Hvis du vil ha mer informasjon om utgiftsregistrering, kan du se [Logg over materialbruk](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="a1232-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="a1232-140">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a1232-140">Time and materials</span></span>

<span data-ttu-id="a1232-141">Når en innsendt loggoppføring for materialbruk er koblet til et prosjekt som er tilordnet en kontraktlinje for tid og materiell, opprettes det to journallinjer, én for kostnad og én for ikke-fakturert salg.</span><span class="sxs-lookup"><span data-stu-id="a1232-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="a1232-142">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-142">Fixed price</span></span>

<span data-ttu-id="a1232-143">Når en innsendt loggoppføring for materialbruk er knyttet til et prosjekt som er tilordnet en kontraktlinje for fast pris, oppretter systemet én journallinje for kostnad.</span><span class="sxs-lookup"><span data-stu-id="a1232-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="a1232-144">Standardprising</span><span class="sxs-lookup"><span data-stu-id="a1232-144">Default pricing</span></span>

<span data-ttu-id="a1232-145">Logikken for å angi standardpriser for materiale er basert på produkt- og enhetskombinasjonen.</span><span class="sxs-lookup"><span data-stu-id="a1232-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="a1232-146">Både transaksjonsdatoen, kontraktlinjen som prosjektet er tilordnet, og valutaresultatet brukes til å bestemme den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="a1232-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a1232-147">Feltene som påvirker standardpriser, for eksempel **Produkt-ID** og **Ressursenhet**, brukes til å bestemme passende pris på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="a1232-148">Dette fungerer imidlertid bare for katalogprodukter.</span><span class="sxs-lookup"><span data-stu-id="a1232-148">However, this only works for catalog products.</span></span> <span data-ttu-id="a1232-149">Når det gjelder produkter som ikke er i katalogen, brukes prisen som angis når oppføringen i materialbruksloggen opprettes, for kostnad og salgspris på journallinjene.</span><span class="sxs-lookup"><span data-stu-id="a1232-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="a1232-150">Du kan legge til et egendefinert felt i oppføringen **Logg over materialbruk**.</span><span class="sxs-lookup"><span data-stu-id="a1232-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="a1232-151">Hvis du vil at feltverdien skal overføres til faktiske verdier, oppretter du feltet i tabellene **Faktiske verdier** og **Journallinje**.</span><span class="sxs-lookup"><span data-stu-id="a1232-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="a1232-152">Bruk egendefinert kode til å overføre den valgte feltverdien fra Tidsoppføring til Faktiske verdier via journallinjen ved hjelp av transaksjonsopphav.</span><span class="sxs-lookup"><span data-stu-id="a1232-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="a1232-153">Hvis du vil ha mer informasjon om transaksjonsopphav og tilkoblinger, kan du se [Koble faktiske verdier til opprinnelige oppføringer](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="a1232-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="a1232-154">Bruk oppføringsjournaler til å registrere kostnader</span><span class="sxs-lookup"><span data-stu-id="a1232-154">Use entry journals to record costs</span></span>

<span data-ttu-id="a1232-155">Du kan bruke oppføringsjournaler til å registrere kostnad eller omsetning i transaksjonsklassene for materialer, gebyr, tid, utgift eller avgift.</span><span class="sxs-lookup"><span data-stu-id="a1232-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a1232-156">Journaler kan brukes til følgende formål:</span><span class="sxs-lookup"><span data-stu-id="a1232-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="a1232-157">Flytt faktiske verdier for transaksjoner fra et annet system til Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a1232-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="a1232-158">Registrer kostnader som er påløpt i et annet system.</span><span class="sxs-lookup"><span data-stu-id="a1232-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="a1232-159">Disse kostnadene kan omfatte innkjøps- eller underleveransekostnader.</span><span class="sxs-lookup"><span data-stu-id="a1232-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1232-160">Programmet validerer ikke journallinjetypen eller den relaterte prisingen som er angitt på journallinjen.</span><span class="sxs-lookup"><span data-stu-id="a1232-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a1232-161">Derfor bør bare en bruker som er fullstendig klar over regnskapsinnvirkningen de faktiske verdiene har på prosjektet, bruke oppføringsjournaler til å opprette faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="a1232-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="a1232-162">På grunn av innvirkningen til denne journaltypen bør du være nøye når du skal velge hvem som skal ha tilgang til å opprette oppføringsjournaler.</span><span class="sxs-lookup"><span data-stu-id="a1232-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="a1232-163">Registrer faktiske verdier basert på prosjekthendelser</span><span class="sxs-lookup"><span data-stu-id="a1232-163">Record actuals based on project events</span></span>

<span data-ttu-id="a1232-164">Project Operations registrerer de finansielle transaksjonene som inntreffer under et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a1232-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a1232-165">Disse transaksjonene registreres som faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="a1232-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="a1232-166">Følgende tabeller viser de forskjellige typene faktiske verdier som opprettes, avhengig av om prosjektet er et tids-og-materiale-prosjekt eller et fastprisprosjekt, er i forsalgsfasen eller er et internt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a1232-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="a1232-167">Ressursen tilhører samme organisasjonsenhet som prosjektets kontraktenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a1232-168">Hendelse</span><span class="sxs-lookup"><span data-stu-id="a1232-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a1232-169">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a1232-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a1232-170">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="a1232-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a1232-171">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a1232-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a1232-172">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a1232-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a1232-173">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a1232-174">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a1232-174">Actuals</span></span></th>
<th><span data-ttu-id="a1232-175">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a1232-175">Transaction currency</span></span></th>
<th><span data-ttu-id="a1232-176">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-176">Fixed price</span></span></th>
<th><span data-ttu-id="a1232-177">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a1232-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1232-178">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="a1232-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a1232-179">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a1232-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-180">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="a1232-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a1232-181">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a1232-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1232-182">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a1232-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a1232-183">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-183">Cost actual</span></span></td>
<td><span data-ttu-id="a1232-184">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-185">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-186">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a1232-187">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-188">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-189">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="a1232-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a1232-190">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1232-191">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a1232-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a1232-192">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-192">Cost actual</span></span></td>
<td><span data-ttu-id="a1232-193">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-194">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-195">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-196">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-197">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-198">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-199">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-200">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-201">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1232-202">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a1232-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a1232-203">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a1232-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a1232-204">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-205">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a1232-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-206">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-207">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-208">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-209">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a1232-209">Billed sales</span></span></td>
<td><span data-ttu-id="a1232-210">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1232-211">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a1232-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a1232-212">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a1232-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a1232-213">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-214">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-215">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-216">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-217">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-218">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-219">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-220">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-221">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1232-222">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a1232-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a1232-223">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a1232-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a1232-224">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a1232-225">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a1232-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a1232-226">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a1232-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a1232-227">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-228">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-229">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-230">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a1232-230">Billed sales</span></span></td>
<td><span data-ttu-id="a1232-231">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1232-232">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a1232-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a1232-233">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a1232-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a1232-234">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-235">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-236">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-237">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-238">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="a1232-239">Ressursen tilhører en annen organisasjonsenhet enn prosjektets kontraktenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a1232-240">Hendelse</span><span class="sxs-lookup"><span data-stu-id="a1232-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a1232-241">Fakturerbart eller solgt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a1232-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a1232-242">Prosjekt i forsalgsfasen</span><span class="sxs-lookup"><span data-stu-id="a1232-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a1232-243">Internt prosjekt</span><span class="sxs-lookup"><span data-stu-id="a1232-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a1232-244">Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="a1232-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a1232-245">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a1232-246">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a1232-246">Actuals</span></span></th>
<th><span data-ttu-id="a1232-247">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a1232-247">Transaction currency</span></span></th>
<th><span data-ttu-id="a1232-248">Fast pris</span><span class="sxs-lookup"><span data-stu-id="a1232-248">Fixed price</span></span></th>
<th><span data-ttu-id="a1232-249">Transaksjonsvaluta</span><span class="sxs-lookup"><span data-stu-id="a1232-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a1232-250">En tidsoppføring opprettes.</span><span class="sxs-lookup"><span data-stu-id="a1232-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a1232-251">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a1232-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-252">En tidsoppføring sendes.</span><span class="sxs-lookup"><span data-stu-id="a1232-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a1232-253">Ingen aktivitet i den faktiske enheten</span><span class="sxs-lookup"><span data-stu-id="a1232-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a1232-254">Tiden godkjennes, og ingen endringer av eller økning av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a1232-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a1232-255">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-255">Cost actual</span></span></td>
<td><span data-ttu-id="a1232-256">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a1232-257">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a1232-258">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a1232-259">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a1232-260">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-261">Ufakturert faktisk salg – belastbart</span><span class="sxs-lookup"><span data-stu-id="a1232-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a1232-262">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-263">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a1232-264">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-265">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a1232-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a1232-266">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a1232-267">Tiden godkjennes, og en reduksjon av fakturerbar tid oppstår under godkjenning.</span><span class="sxs-lookup"><span data-stu-id="a1232-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a1232-268">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-268">Cost actual</span></span></td>
<td><span data-ttu-id="a1232-269">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-270">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-271">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-272">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-273">Faktisk kostnad</span><span class="sxs-lookup"><span data-stu-id="a1232-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-274">Kostnad for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a1232-275">Valuta for ressursenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-276">Salg mellom organisasjoner</span><span class="sxs-lookup"><span data-stu-id="a1232-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a1232-277">Valuta for kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="a1232-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-278">Ufakturert faktisk salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-279">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-280">Ufakturert faktisk salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-281">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1232-282">En faktura bekreftes, og ingen endringer av eller økning av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a1232-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a1232-283">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a1232-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a1232-284">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-285">Fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a1232-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-286">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-287">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a1232-288">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-289">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a1232-289">Billed sales</span></span></td>
<td><span data-ttu-id="a1232-290">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1232-291">En faktura bekreftes, og en reduksjon av fakturerbar tid oppstår.</span><span class="sxs-lookup"><span data-stu-id="a1232-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a1232-292">Ufakturert salg omgjort</span><span class="sxs-lookup"><span data-stu-id="a1232-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a1232-293">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-294">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-295">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-296">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a1232-297">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-298">Fakturert salg – belastbart for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-299">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-300">Fakturert salg – ikke-belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-301">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a1232-302">En faktura korrigeres for å øke det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a1232-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a1232-303">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a1232-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a1232-304">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a1232-305">Tilbakeføring av fakturert salg for milepæl</span><span class="sxs-lookup"><span data-stu-id="a1232-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a1232-306">Endring i milepælstatus fra <strong>Fakturert</strong> til <strong>Klar for faktura</strong></span><span class="sxs-lookup"><span data-stu-id="a1232-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a1232-307">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-308">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a1232-309">Ikke aktuelt</span><span class="sxs-lookup"><span data-stu-id="a1232-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-310">Fakturert salg</span><span class="sxs-lookup"><span data-stu-id="a1232-310">Billed sales</span></span></td>
<td><span data-ttu-id="a1232-311">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a1232-312">En faktura korrigeres for å redusere det belastbare antallet.</span><span class="sxs-lookup"><span data-stu-id="a1232-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a1232-313">Fakturert salg – tilbakeføring</span><span class="sxs-lookup"><span data-stu-id="a1232-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a1232-314">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-315">Fakturert salg for det nye antallet</span><span class="sxs-lookup"><span data-stu-id="a1232-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a1232-316">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a1232-317">Ufakturert salg – belastbart for forskjellen</span><span class="sxs-lookup"><span data-stu-id="a1232-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a1232-318">Valuta for prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="a1232-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
