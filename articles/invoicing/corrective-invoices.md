---
title: Opprette korrigerte prosjektbaserte fakturaer
description: Dette emnet inneholder informasjon om korrigerte fakturaer i Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0423fe9895b91431b2a83a8fff81118205b0736
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001637"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="2aa95-103">Opprette korrigerte prosjektbaserte fakturaer</span><span class="sxs-lookup"><span data-stu-id="2aa95-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="2aa95-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="2aa95-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2aa95-105">En bekreftet prosjektfaktura kan korrigeres mot prosessendringer eller kreditter som forhandlet med kunden og prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="2aa95-106">Hvis du vil redigere en bekreftet faktura, åpner du den bekreftede fakturaen og velger **Rett opp denne fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="2aa95-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2aa95-107">Dette valget er ikke tilgjengelig hvis ikke en prosjektfaktura er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="2aa95-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="2aa95-108">Det opprettes en ny utkastfaktura fra den bekreftede fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="2aa95-109">Alle fakturalinjedetaljer fra den tidligere bekreftede fakturaen kopieres til det nye utkastet.</span><span class="sxs-lookup"><span data-stu-id="2aa95-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="2aa95-110">Her er noen viktige punkter som hjelper deg med å forstå mer om linjedetaljene i den nye korrigerte fakturaen:</span><span class="sxs-lookup"><span data-stu-id="2aa95-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="2aa95-111">Alle antall blir oppdatert til null.</span><span class="sxs-lookup"><span data-stu-id="2aa95-111">All quantities are updated to zero.</span></span> <span data-ttu-id="2aa95-112">Dette forutsetter at alle fakturerte elementer er kreditert fullt ut.</span><span class="sxs-lookup"><span data-stu-id="2aa95-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="2aa95-113">Du kan om nødvendig oppdatere disse antallene manuelt, slik at de gjenspeiler antallet som blir fakturert, og ikke det antallet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="2aa95-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="2aa95-114">Basert på antallet du angir, beregner programmet det krediterte antallet.</span><span class="sxs-lookup"><span data-stu-id="2aa95-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="2aa95-115">Dette beløpet gjenspeiles i de faktiske verdiene som opprettes når den rettede fakturaen er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="2aa95-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="2aa95-116">Hvis du gjør endringer i avgiftsbeløpet, må du angi riktig avgiftsbeløp og ikke avgiftsbeløpet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="2aa95-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="2aa95-117">Milepælrettelser behandles alltid som fulle kreditter.</span><span class="sxs-lookup"><span data-stu-id="2aa95-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="2aa95-118">Honorar- eller forskuddsbeløp kan korrigeres hvis kunden var fakturert for et feil beløp.</span><span class="sxs-lookup"><span data-stu-id="2aa95-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="2aa95-119">Avstemminger av honorarer og forskudd kan korrigeres hvis et feilaktig beløp ble brukt til å avstemme mot kostnadene på en tidligere bekreftet faktura.</span><span class="sxs-lookup"><span data-stu-id="2aa95-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aa95-120">Fakturalinjedetaljer som er rettelser i andre allerede fakturerte omkostnader, har feltet **Korrigering** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2aa95-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="2aa95-121">Fakturaer som har korrigerte fakturalinjedetaljer, har et felt kalt **Har rettelser**, som også er angitt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2aa95-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="2aa95-122">Faktiske verdier opprettet ved bekreftelse av en korrigert faktura</span><span class="sxs-lookup"><span data-stu-id="2aa95-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="2aa95-123">Tabellen nedenfor viser de faktiske verdiene som opprettes når en korrigeringsfaktura bekreftes.</span><span class="sxs-lookup"><span data-stu-id="2aa95-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="2aa95-124">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2aa95-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="2aa95-125">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="2aa95-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2aa95-126">Bekreft rettelsen av et fakturert forskudd eller honorar.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="2aa95-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-127">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="2aa95-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2aa95-128">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="2aa95-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-129">En tilbakeføring av en faktisk salgsverdi opprettes for beløpet for honoraret eller forskuddet for å tilbakeføre det opprinnelige fakturerte salget.</span><span class="sxs-lookup"><span data-stu-id="2aa95-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-130">En ny fakturert salgsverdi opprettes for det korrigerte beløpet for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet.</span><span class="sxs-lookup"><span data-stu-id="2aa95-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-131">En ikke-fakturert faktisk salgsverdi av et negativt beløp for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet, som skal brukes til avstemming.</span><span class="sxs-lookup"><span data-stu-id="2aa95-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="2aa95-132">En bekreftelse av rettelsen av et tidligere avstemt honorar eller forskudd.</span><span class="sxs-lookup"><span data-stu-id="2aa95-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-133">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="2aa95-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="2aa95-134">Dette beløpet er positivt og er ment å nulle ut den negative verdien som ble opprettet under den forrige avstemmingen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-135">En tilbakeført fakturert faktisk salgsverdi for beløpet på den forrige fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-136">En ny fakturert salgsverdi for det korrigerte honorarbeløpet som brukes i den korrigerte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-137">En ikke-fakturert faktisk salgsverdi med et negativt beløp fra den korrigerte honoraret eller forskuddet som er til overs, som skal brukes til avstemming på senere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="2aa95-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2aa95-138">Fakturering av hele kreditten til en tidligere fakturert tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-139">En fakturert salgsreversering for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="2aa95-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-140">En ny ikke-fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="2aa95-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2aa95-141">Fakturering av den delvise kreditten på en tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-142">En fakturert salgsreversering for timene og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="2aa95-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-143">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="2aa95-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-144">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående timer og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="2aa95-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2aa95-145">Fakturering av hele kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-146">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="2aa95-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-147">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="2aa95-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="2aa95-148">Fakturering av deler av kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-149">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for en utgift.</span><span class="sxs-lookup"><span data-stu-id="2aa95-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-150">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den korrigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="2aa95-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-151">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående antall og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="2aa95-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2aa95-152">Fakturering av hele kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-153">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="2aa95-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-154">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="2aa95-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="2aa95-155">Fakturering av deler av kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="2aa95-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-156">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="2aa95-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-157">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="2aa95-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2aa95-158">Fakturering av hele kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="2aa95-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-159">En fakturert salgsreversering for beløpet på den opprinnelige fakturalinjedetaljen for milepælen.</span><span class="sxs-lookup"><span data-stu-id="2aa95-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="2aa95-160">Fakturastatusen for milepælen oppdateres fra en <b>kundefaktura som er postert</b> som <b>Klar for fakturering</b>.</span><span class="sxs-lookup"><span data-stu-id="2aa95-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="2aa95-161">Fakturering av deler av kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="2aa95-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="2aa95-162">Støttes ikke</span><span class="sxs-lookup"><span data-stu-id="2aa95-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
