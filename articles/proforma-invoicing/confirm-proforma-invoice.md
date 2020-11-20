---
title: Bekrefte en proformafaktura
description: Dette emnet gir informasjon om å bekrefte en proformafaktura.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128115"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="efc31-103">Bekrefte en proformafaktura</span><span class="sxs-lookup"><span data-stu-id="efc31-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="efc31-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="efc31-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="efc31-105">Når en proformafaktura er bekreftet, oppdateres statusen for prosjektfakturaen til **Bekreftet**.</span><span class="sxs-lookup"><span data-stu-id="efc31-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="efc31-106">Når en faktura er bekreftet, blir den skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="efc31-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="efc31-107">Derfra kan fakturaen bare korrigeres hvis det finnes kundeiverksatte rettelser eller kreditt, eller når den er merket som betalt.</span><span class="sxs-lookup"><span data-stu-id="efc31-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="efc31-108">Tabellen nedenfor viser de faktiske verdiene som opprettes av systemet.</span><span class="sxs-lookup"><span data-stu-id="efc31-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="efc31-109">Disse faktiske verdiene opprettes når bestemte operasjoner utføres på utkastfakturaen for prosjektet før den er bekreftet.</span><span class="sxs-lookup"><span data-stu-id="efc31-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="efc31-110">
                    <strong>Scenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efc31-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="efc31-111">
                    <strong>Faktiske verdier opprettet ved bekreftelse</strong>
                </span><span class="sxs-lookup"><span data-stu-id="efc31-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efc31-112">Fakturering av en tidstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="efc31-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-113">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-114">En fakturert faktisk salgsverdi for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="efc31-115">Fakturering av en tidstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="efc31-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-116">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-117">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="efc31-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-118">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av timene og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="efc31-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efc31-119">Fakturering av en tidstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="efc31-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-120">En ikke-fakturert salgsreversering for timene og beløpet på den opprinnelige tidsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-121">En ny ikke-fakturert faktisk salgsverdi som er belastbar for timene og beløpet på den redigerte fakturalinjedetaljen, en reversering av den ikke-fakturerte faktiske salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="efc31-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efc31-122">Fakturering av en utgiftstransaksjon uten redigeringer på fakturautkastet.</span><span class="sxs-lookup"><span data-stu-id="efc31-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-123">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-124">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="efc31-125">Fakturering av en utgiftstransaksjon som ble redigert for å redusere antallet.</span><span class="sxs-lookup"><span data-stu-id="efc31-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-126">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-127">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="efc31-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-128">En ny ikke-fakturert faktisk salgsverdi som er ikke-belastbar for resten av antallet og beløpet etter å ha trukket fra de korrigerte tallene på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og tilsvarende av den fakturerte faktiske salgsverdien.</span><span class="sxs-lookup"><span data-stu-id="efc31-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efc31-129">Fakturering av en utgiftstransaksjon som ble redigert for å øke antallet.</span><span class="sxs-lookup"><span data-stu-id="efc31-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-130">En ikke-fakturert salgsreversering for antallet og beløpet på den opprinnelige utgiftsgodkjenningen.</span><span class="sxs-lookup"><span data-stu-id="efc31-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-131">En ny ikke-fakturert faktisk salgsverdi som er belastbar for antallet og beløpet på den redigerte fakturalinjedetaljen, en reversering av den faktiske, ikke-fakturerte salgsverdien og en tilsvarende fakturert faktisk salgsverdi.</span><span class="sxs-lookup"><span data-stu-id="efc31-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="efc31-132">Fakturering av et gebyr.</span><span class="sxs-lookup"><span data-stu-id="efc31-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-133">En ikke-fakturert salgsreversering for gebyrbeløpet på den opprinnelige journallinjen.</span><span class="sxs-lookup"><span data-stu-id="efc31-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-134">En fakturert faktisk salgsverdi for antallet og beløpet på den opprinnelige gebyrjournallinjen.</span><span class="sxs-lookup"><span data-stu-id="efc31-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="efc31-135">Fakturering av en milepæl.</span><span class="sxs-lookup"><span data-stu-id="efc31-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="efc31-136">En fakturert faktisk salgsverdi for milepælbeløpet på den opprinnelige milepælen på prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="efc31-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
