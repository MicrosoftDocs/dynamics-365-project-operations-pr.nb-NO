---
title: Bekrefte en proforma prosjektfaktura
description: Dette emnet inneholder informasjon om bekreftelse av proformaprosjektfakturaer i Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004138"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="1bf67-103">Bekrefte en proforma prosjektfaktura</span><span class="sxs-lookup"><span data-stu-id="1bf67-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="1bf67-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="1bf67-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1bf67-105">Når en proformafaktura er bekreftet, oppdateres statusen for prosjektfakturaen til **Bekreftet**.</span><span class="sxs-lookup"><span data-stu-id="1bf67-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="1bf67-106">Når en faktura er bekreftet, blir den skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="1bf67-107">Fremover kan fakturaen bare korrigeres hvis det er noen kundestartede rettelser eller kreditter.</span><span class="sxs-lookup"><span data-stu-id="1bf67-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="1bf67-108">Tabellen nedenfor viser de faktiske verdiene som opprettes av systemet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="1bf67-109">Disse faktiske verdiene opprettes når bestemte operasjoner utføres på utkastfakturaen for prosjektet før den er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="1bf67-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1bf67-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="1bf67-111">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1bf67-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-112">Fakturere et forskudd eller honorar</span><span class="sxs-lookup"><span data-stu-id="1bf67-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-113">E fakturert salgsverdi av typen <strong>Honorar</strong> opprettes for beløpet for forskuddet eller honoraret.</span><span class="sxs-lookup"><span data-stu-id="1bf67-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-114">En ikke-fakturert faktisk salgsverdi av et negativt beløp for honoraret eller forskuddet som skal brukes til avstemming.</span><span class="sxs-lookup"><span data-stu-id="1bf67-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-115">Etter fullstendig avstemming av et honorar eller forskudd på en faktura.</span><span class="sxs-lookup"><span data-stu-id="1bf67-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-116">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="1bf67-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1bf67-117">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="1bf67-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-118">En fakturert faktisk salgsverdi for beløpet på denne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1bf67-119">Etter delvis avstemming av et honorar eller forskudd på en faktura.</span><span class="sxs-lookup"><span data-stu-id="1bf67-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-120">En tilbakeføring av ikke-fakturert salg for honoraret eller forskuddet som ble opprettet for avstemming.</span><span class="sxs-lookup"><span data-stu-id="1bf67-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="1bf67-121">Dette beløpet er positivt fordi det er ment å nulle ut den negative verdien som ble opprettet da honoraret eller forskuddet ble fakturert.</span><span class="sxs-lookup"><span data-stu-id="1bf67-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-122">En fakturert faktisk salgsverdi for beløpet på denne fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-123">En negativ, ikke-fakturert faktisk salgsverdi av resten av beløpet for honoraret eller forskuddet som skal brukes til avstemming på fremtidige fakturaer.</span><span class="sxs-lookup"><span data-stu-id="1bf67-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-124">Fakturering av en tidstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-125">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-126">En fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1bf67-127">Fakturering av en tidstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-128">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-129">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-130">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av timene og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-131">Fakturering av en tidstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-132">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-133">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-134">Fakturering av en utgiftstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-135">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-136">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige utgiftsgodkjenningen</span><span class="sxs-lookup"><span data-stu-id="1bf67-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1bf67-137">Fakturering av en utgiftstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-138">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-139">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-140">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-141">Fakturering av en utgiftstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-142">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-143">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-144">Fakturering av en materialtransaksjon uten redigeringer i utkastfakturaen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-145">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="1bf67-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-146">En fakturert faktisk salgsverdi for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="1bf67-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="1bf67-147">Fakturering av en materialtransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-148">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av tidsbruk.</span><span class="sxs-lookup"><span data-stu-id="1bf67-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-149">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-150">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-151">Fakturering av en materialtransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="1bf67-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-152">En ufakturert tilbakeføring av salg for antallet og beløpet i den opprinnelige godkjenningen av materialbruk.</span><span class="sxs-lookup"><span data-stu-id="1bf67-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-153">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="1bf67-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1bf67-154">Fakturering av et gebyr.</span><span class="sxs-lookup"><span data-stu-id="1bf67-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-155">En ikke-fakturert salgsreversering for gebyrbeløpet på den opprinnelige journallinjen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-156">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige gebyrjournallinjen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1bf67-157">Fakturering av en milepæl.</span><span class="sxs-lookup"><span data-stu-id="1bf67-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-158">En fakturert faktisk salgsverdi for milepælbeløpet på den opprinnelige milepælen på prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="1bf67-159">Fakturering av en produktbasert kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="1bf67-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="1bf67-160">En fakturert faktisk salgsverdi for produktlinjen med antallet og beløpet som kommer fra den produktbaserte kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="1bf67-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
