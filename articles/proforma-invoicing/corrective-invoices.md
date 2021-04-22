---
title: Korrigerte prosjektbaserte fakturaer
description: Dette emnet inneholder informasjon om hvordan du oppretter og bekrefter korrigerte prosjektbaserte fakturaer i Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867053"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="821bc-103">Korrigerte prosjektbaserte fakturaer</span><span class="sxs-lookup"><span data-stu-id="821bc-103">Corrective project-based invoices</span></span>

<span data-ttu-id="821bc-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="821bc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="821bc-105">En bekreftet prosjektfaktura kan korrigeres mot prosessendringer eller kreditter som forhandlet med kunden og prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="821bc-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="821bc-106">Hvis du vil redigere en bekreftet faktura, åpner du den bekreftede fakturaen og velger **Rett opp denne fakturaen**.</span><span class="sxs-lookup"><span data-stu-id="821bc-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="821bc-107">Dette valget er ikke tilgjengelig med mindre en prosjektfaktura er bekreftet, eller den prosjektbaserte fakturaen har forskudd eller honorarer eller avstemminger av forskudd eller honorarer.</span><span class="sxs-lookup"><span data-stu-id="821bc-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="821bc-108">Det opprettes en ny utkastfaktura fra den bekreftede fakturaen.</span><span class="sxs-lookup"><span data-stu-id="821bc-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="821bc-109">Alle fakturalinjedetaljer fra den tidligere bekreftede fakturaen kopieres til det nye utkastet.</span><span class="sxs-lookup"><span data-stu-id="821bc-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="821bc-110">Her følger noen av nøkkelpunktene for å forstå linjedetaljene i den nye korrigerte fakturaen:</span><span class="sxs-lookup"><span data-stu-id="821bc-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="821bc-111">Alle antall blir oppdatert til null.</span><span class="sxs-lookup"><span data-stu-id="821bc-111">All quantities are updated to zero.</span></span> <span data-ttu-id="821bc-112">Dynamics 365 Project Operations forutsetter at alle fakturerte elementer er kreditert fullt ut.</span><span class="sxs-lookup"><span data-stu-id="821bc-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="821bc-113">Du kan om nødvendig oppdatere disse antallene manuelt, slik at de gjenspeiler antallet som blir fakturert, og ikke det antallet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="821bc-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="821bc-114">Basert på antallet du angir, beregner programmet det krediterte antallet.</span><span class="sxs-lookup"><span data-stu-id="821bc-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="821bc-115">Dette beløpet gjenspeiles i de faktiske verdiene som opprettes når den rettede fakturaen er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="821bc-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="821bc-116">Hvis du gjør endringer i avgiftsbeløpet, må du angi riktig avgiftsbeløp og ikke avgiftsbeløpet som krediteres.</span><span class="sxs-lookup"><span data-stu-id="821bc-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="821bc-117">Milepælrettelser behandles alltid som fulle kreditter.</span><span class="sxs-lookup"><span data-stu-id="821bc-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="821bc-118">For fakturalinjedetaljer som er rettelser i andre allerede fakturerte omkostnader, er feltet **Korrigering** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="821bc-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="821bc-119">For fakturaer som har korrigerte fakturalinjedetaljer, er feltet **Har korrigeringer** satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="821bc-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="821bc-120">Faktiske verdier opprettet ved bekreftelse av en korrigert faktura</span><span class="sxs-lookup"><span data-stu-id="821bc-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="821bc-121">Tabellen nedenfor viser de faktiske verdiene som opprettes når en korrigeringsfaktura bekreftes.</span><span class="sxs-lookup"><span data-stu-id="821bc-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="821bc-122">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="821bc-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="821bc-123">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="821bc-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="821bc-124">Fakturering av hele kreditten til en tidligere fakturert tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-125">En fakturert salgsreversering for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="821bc-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-126">En ny ikke-fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="821bc-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="821bc-127">Fakturering av den delvise kreditten på en tidstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-128">En fakturert salgsreversering for timene og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for tid.</span><span class="sxs-lookup"><span data-stu-id="821bc-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-129">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="821bc-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-130">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående timer og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="821bc-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="821bc-131">Fakturering av hele kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-132">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="821bc-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-133">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for utgiften.</span><span class="sxs-lookup"><span data-stu-id="821bc-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="821bc-134">Fakturering av deler av kreditten til en tidligere fakturert utgiftstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-135">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for en utgift.</span><span class="sxs-lookup"><span data-stu-id="821bc-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-136">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den korrigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="821bc-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-137">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående antall og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="821bc-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="821bc-138">Fakturering av den fulle kreditten for en tidligere fakturert materialtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-139">En fakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige fakturalinjedetaljer for material.</span><span class="sxs-lookup"><span data-stu-id="821bc-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-140">En ny ufakturert faktisk salgsverdi for antallet og beløpet i den opprinnelige fakturalinjedetaljer for material.</span><span class="sxs-lookup"><span data-stu-id="821bc-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="821bc-141">Fakturering av delvis kreditt på en materialtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-142">En fakturert tilbakeføring av salg for antallet og beløpet som var fakturert i den opprinnelige fakturalinjedetaljen for material.</span><span class="sxs-lookup"><span data-stu-id="821bc-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-143">En ny ufakturert faktisk salgsverdi som er belastbar for antallet og beløpet på de redigerte fakturalinjedetaljen, en reversering av dette og tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="821bc-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-144">En ny ikke-fakturert faktisk salgsverdi som er belastbar for gjenstående antall og beløp etter at de korrigerte tallene er trukket fra på fakturalinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="821bc-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="821bc-145">Fakturering av hele kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-146">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="821bc-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-147">En ny ikke-fakturert faktisk salgsverdi for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="821bc-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="821bc-148">Fakturering av deler av kreditten til en tidligere fakturert gebyrtransaksjon.</span><span class="sxs-lookup"><span data-stu-id="821bc-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-149">En fakturert salgsreversering for antallet og beløpet som er fakturert på den opprinnelige fakturalinjedetaljen for gebyret.</span><span class="sxs-lookup"><span data-stu-id="821bc-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-150">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av dette og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="821bc-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="821bc-151">Fakturering av hele kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="821bc-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-152">En fakturert salgsreversering for beløpet på den opprinnelige fakturalinjedetaljen for milepælen.</span><span class="sxs-lookup"><span data-stu-id="821bc-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="821bc-153">Fakturastatusen for milepælen oppdateres fra en <b>kundefaktura som er postert</b> som <b>Klar for fakturering</b>.</span><span class="sxs-lookup"><span data-stu-id="821bc-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="821bc-154">Fakturering av deler av kreditten til en tidligere fakturert milepæl.</span><span class="sxs-lookup"><span data-stu-id="821bc-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="821bc-155">Dette scenarioet støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="821bc-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
