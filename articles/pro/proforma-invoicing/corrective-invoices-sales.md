---
title: Kredittee og korrigerte fakturaer
description: Dette emnet gir informasjon om korrigerte fakturaer i Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081731"
---
# <a name="credits-and-corrected-invoices"></a><span data-ttu-id="80b87-103">Kredittee og korrigerte fakturaer</span><span class="sxs-lookup"><span data-stu-id="80b87-103">Credits and corrected invoices</span></span>

<span data-ttu-id="80b87-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="80b87-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80b87-105">En bekreftet prosjektfaktura kan korrigeres mot prosessendringer eller kreditter som forhandlet med kunden og prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="80b87-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="80b87-106">Hvis du vil redigere en bekreftet faktura, åpner du den bekreftede fakturaen og velger **Rett opp denne fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="80b87-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="80b87-107">Dette valget er ikke tilgjengelig hvis ikke en prosjektfaktura er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="80b87-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="80b87-108">Det opprettes en ny utkastfaktura fra den bekreftede fakturaen.</span><span class="sxs-lookup"><span data-stu-id="80b87-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="80b87-109">Alle fakturalinjedetaljer fra den tidligere bekreftede fakturaen kopieres til det nye utkastet.</span><span class="sxs-lookup"><span data-stu-id="80b87-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="80b87-110">Her følger noen av nøkkelpunktene for å forstå linjedetaljene i den nye korrigerte fakturaen:</span><span class="sxs-lookup"><span data-stu-id="80b87-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="80b87-111">Alle antall blir oppdatert til null.</span><span class="sxs-lookup"><span data-stu-id="80b87-111">All quantities are updated to zero.</span></span> <span data-ttu-id="80b87-112">Programmet forutsetter at alle fakturerte varer er fullt kreditert.</span><span class="sxs-lookup"><span data-stu-id="80b87-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="80b87-113">Du kan om nødvendig oppdatere disse antallene manuelt, slik at de gjenspeiler antallet som blir fakturert, og ikke det antallet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="80b87-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="80b87-114">Basert på antallet du angir, beregner programmet det krediterte antallet.</span><span class="sxs-lookup"><span data-stu-id="80b87-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="80b87-115">Dette beløpet gjenspeiles i de faktiske verdiene som opprettes når den rettede fakturaen er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="80b87-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="80b87-116">Hvis du gjør endringer i avgiftsbeløpet, må du angi riktig avgiftsbeløp og ikke avgiftsbeløpet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="80b87-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="80b87-117">Tidligere bekreftede produktbaserte kontraktlinjer kopieres ikke.</span><span class="sxs-lookup"><span data-stu-id="80b87-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="80b87-118">Behandling av rettelser i en produktbasert prosjektfaktura støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="80b87-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="80b87-119">Milepælrettelser behandles alltid som fulle kreditter.</span><span class="sxs-lookup"><span data-stu-id="80b87-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="80b87-120">Honorar- eller forskuddsbeløp kan korrigeres hvis kunden var fakturert for et feil beløp.</span><span class="sxs-lookup"><span data-stu-id="80b87-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="80b87-121">Avstemminger av honorarer og forskudd kan korrigeres hvis et feilaktig beløp ble brukt til å avstemme mot kostnadene på en tidligere bekreftet faktura.</span><span class="sxs-lookup"><span data-stu-id="80b87-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80b87-122">Fakturalinjedetaljer som er rettelser i andre allerede fakturerte gebyrer,har feltet **Korrigering** angitt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80b87-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="80b87-123">Fakturaer som har korrigerte fakturalinjedetaljer, har et felt kalt **Har rettelser** , som også er angitt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80b87-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="80b87-124">Faktiske verdier opprettet ved bekreftelse av en korrigert faktura:</span><span class="sxs-lookup"><span data-stu-id="80b87-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="80b87-125">Nedenfor finner du faktiske verdier som opprettes av programmet, ved bekreftelse av en korreksjon basert på operasjonene som ble utført på det korrigerte fakturautkastet før bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="80b87-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="80b87-126">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="80b87-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="80b87-127">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="80b87-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="80b87-128">Bekreft rettelsen av et fakturert forskudd eller honorar.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="80b87-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-129">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="80b87-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="80b87-130">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="80b87-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-131">En tilbakeføring av en faktisk salgsverdi opprettes for beløpet for honoraret eller forskuddet for å tilbakeføre det opprinnelige fakturerte salget.</span><span class="sxs-lookup"><span data-stu-id="80b87-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-132">En ny fakturert salgsverdi opprettes for det korrigerte beløpet for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet.</span><span class="sxs-lookup"><span data-stu-id="80b87-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-133">En ikke-fakturert faktisk salgsverdi av et negativt beløp for den korrigerte fakturalinjen som er basert på honoraret eller forskuddet, som skal brukes til avstemming.</span><span class="sxs-lookup"><span data-stu-id="80b87-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="80b87-134">En bekreftelse av rettelsen av et tidligere avstemt honorar eller forskudd.</span><span class="sxs-lookup"><span data-stu-id="80b87-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-135">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="80b87-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="80b87-136">Dette beløpet er positivt og er ment å nulle ut den negative verdien som ble opprettet under den forrige avstemmingen.</span><span class="sxs-lookup"><span data-stu-id="80b87-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-137">En tilbakeført fakturert faktisk salgsverdi for beløpet på den forrige fakturaen.</span><span class="sxs-lookup"><span data-stu-id="80b87-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-138">En ny fakturert salgsverdi for det korrigerte honorarbeløpet som brukes i den korrigerte fakturaen.</span><span class="sxs-lookup"><span data-stu-id="80b87-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-139">En ikke-fakturert faktisk salgsverdi med et negativt beløp fra den korrigerte honoraret eller forskuddet som er til overs, som skal brukes til avstemming på senere fakturaer.</span><span class="sxs-lookup"><span data-stu-id="80b87-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="80b87-140">Fakturering av hele kreditten til en tidligere fakturert tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-141">En fakturert salgsreversering for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="80b87-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-142">En ny ikke-fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="80b87-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="80b87-143">Fakturering av den delvise kreditten på en tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-144">En fakturert salgsreversering for timene og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="80b87-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-145">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="80b87-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-146">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående timer og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="80b87-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="80b87-147">Fakturering av hele kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-148">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="80b87-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-149">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="80b87-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="80b87-150">Fakturering av deler av kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-151">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for en utgift.</span><span class="sxs-lookup"><span data-stu-id="80b87-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-152">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den korrigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="80b87-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-153">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående antall og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="80b87-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="80b87-154">Fakturering av hele kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-155">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="80b87-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-156">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="80b87-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="80b87-157">Fakturering av deler av kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="80b87-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-158">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="80b87-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-159">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="80b87-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="80b87-160">Fakturering av hele kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="80b87-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-161">En fakturert salgsreversering for beløpet på den opprinnelige fakturalinjedetaljen for milepælen.</span><span class="sxs-lookup"><span data-stu-id="80b87-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="80b87-162">Faktura- eller faktureringsstatusen for milepælen på prosjektkontraktlinjen er oppdatert til **Klar for fakturerring**.</span><span class="sxs-lookup"><span data-stu-id="80b87-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="80b87-163">Fakturering av deler av kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="80b87-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-164">Støttes ikke</span><span class="sxs-lookup"><span data-stu-id="80b87-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="80b87-165">Kreditter og rettelser for en tidligere fakturert produktbasert kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="80b87-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="80b87-166">Støttes ikke</span><span class="sxs-lookup"><span data-stu-id="80b87-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
