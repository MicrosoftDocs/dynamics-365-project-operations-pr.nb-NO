---
title: Bekrefte en proforma prosjektbasert faktura
description: Dette emnet inneholder informasjon om bekreftelse av en proforma prosjektbasert faktura.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 53c647dca506822312053fb5c9b086a2947974c2
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867143"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="6a7f3-103">Bekrefte en proforma prosjektbasert faktura</span><span class="sxs-lookup"><span data-stu-id="6a7f3-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="6a7f3-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="6a7f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6a7f3-105">Når en proformafaktura er bekreftet, oppdateres statusen for prosjektfakturaen til **Bekreftet**.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="6a7f3-106">Når en faktura er bekreftet, blir den skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="6a7f3-107">Fremover kan fakturaen bare korrigeres hvis det er noen kundestartede rettelser eller kreditter.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="6a7f3-108">Tabellen nedenfor viser de faktiske verdiene som opprettes av systemet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="6a7f3-109">Disse faktiske verdiene opprettes når bestemte operasjoner utføres på utkastfakturaen for prosjektet før den er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="6a7f3-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a7f3-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="6a7f3-111">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6a7f3-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-112">Fakturere et forskudd eller honorar</span><span class="sxs-lookup"><span data-stu-id="6a7f3-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-113">E fakturert salgsverdi av typen <strong>Honorar</strong> opprettes for beløpet for forskuddet eller honoraret.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-114">En ufakturert faktisk salgsverdi med et negativt beløp for honoraret eller forskuddet som skal brukes til avstemming.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-115">Etter fullstendig avstemming av et honorar eller forskudd på en faktura.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-116">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6a7f3-117">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-118">En fakturert faktisk salgsverdi for beløpet på denne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6a7f3-119">Etter delvis avstemming av et honorar eller forskudd på en faktura.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-120">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="6a7f3-121">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-122">En fakturert faktisk salgsverdi for beløpet på denne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-123">En negativ, ikke-fakturert faktisk salgsverdi av resten av beløpet for honoraret eller forskuddet som skal brukes til avstemming på fremtidige fakturaer.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-124">Fakturering av en tidstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-125">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-126">En fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6a7f3-127">Fakturering av en tidstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-128">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-129">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-130">En ny ufakturert faktisk salgsverdi som er ikke-belastbar for de resterende timene og beløpet etter at de korrigerte tallene er trukket fra i de redigerte fakturalinjedetaljene, en reversering av den faktiske salgsverdien og tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-131">Fakturering av en tidstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-132">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-133">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-134">Fakturering av en utgiftstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-135">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-136">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6a7f3-137">Fakturering av en utgiftstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-138">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-139">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-140">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-141">Fakturering av en utgiftstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-142">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-143">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-144">Fakturering av en materialtransaksjon uten redigeringer i utkastfakturaen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-145">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-146">En fakturert faktisk salgsverdi for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="6a7f3-147">Fakturering av en materialtransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-148">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av tidsbruk.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-149">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-150">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-151">Fakturering av en materialtransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-152">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-153">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6a7f3-154">Fakturering av et gebyr.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-155">En ikke-fakturert salgsreversering for gebyrbeløpet på den opprinnelige journallinjen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-156">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige gebyrjournallinjen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="6a7f3-157">Fakturering av en milepæl.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="6a7f3-158">En fakturert faktisk salgsverdi for milepælbeløpet på den opprinnelige milepælen på prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="6a7f3-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
