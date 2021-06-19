---
title: Konfigurere de belastbare komponentene i en tilbudslinje
description: Dette emnet gir informasjon om hvordan du konfigurerer belastbare og ikke-belastbare komponenter på en prosjektbasert tilbudslinje.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003778"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="e3473-103">Konfigurere de belastbare komponentene i en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="e3473-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="e3473-104">_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="e3473-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e3473-105">En prosjektbasert tilbudslinje har konseptet *inkluderte* komponenter og *belastbare* komponenter.</span><span class="sxs-lookup"><span data-stu-id="e3473-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="e3473-106">Inkluderte komponenter er underlagt følgende:</span><span class="sxs-lookup"><span data-stu-id="e3473-106">Included components are subject to:</span></span>

  - <span data-ttu-id="e3473-107">Faktureringsmetode og kundedelinger</span><span class="sxs-lookup"><span data-stu-id="e3473-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="e3473-108">Må ikke overskrides-grenser</span><span class="sxs-lookup"><span data-stu-id="e3473-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="e3473-109">Innstillinger for fakturafrekvens som er definert på den prosjektbaserte tilbudslinjen</span><span class="sxs-lookup"><span data-stu-id="e3473-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="e3473-110">Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="e3473-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="e3473-111">Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en tilbudslinje:</span><span class="sxs-lookup"><span data-stu-id="e3473-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="e3473-112">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-112">Chargeable</span></span>
  - <span data-ttu-id="e3473-113">Ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-113">Non-chargeable</span></span>

<span data-ttu-id="e3473-114">Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="e3473-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="e3473-115">Belastbarhet er definert i oppgavene for en tilbudslinje og gjelder for alle transaksjonsklasser som finnes på denne linjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="e3473-116">Hvis feltet **Inkluder oppgaver** satt til **Hele prosjektet** eller er tomt, er ikke **Belastbare oppgaver**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e3473-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="e3473-117">Belastbarhet er definert for roller for en tilbudslinje og gjelder bare transaksjonsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="e3473-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="e3473-118">Hvis feltet **Inkluder td** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare roller**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e3473-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="e3473-119">Belastbarhet er definert for transaksjonskategorier for en tilbudslinje og gjelder bare transaksjonsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="e3473-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="e3473-120">Hvis feltet **Inkluder utgifter** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare kategorier**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="e3473-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e3473-121">Oppdatere en prosjektoppgave til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e3473-122">En prosjektoppgave kan være belastbar eller ikke-belastbar i konteksten til en bestemt prosjektbasert tilbudslinje, noe som gjør følgende oppsett mulig.</span><span class="sxs-lookup"><span data-stu-id="e3473-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="e3473-123">Hvis en prosjektbasert tilbudslinje inkluderer **Tid** og oppgaven **T1**, knyttes oppgaven til tilbudslinjen som belastbar.</span><span class="sxs-lookup"><span data-stu-id="e3473-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="e3473-124">Hvis det er en ny tilbudslinje som inkluderer **Utgifter**, kan du knytte til **T1**-oppgaven på tilbudslinjen som ikke-belastbar.</span><span class="sxs-lookup"><span data-stu-id="e3473-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="e3473-125">Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter som registreres på oppgaven, er ikke-belastbare.</span><span class="sxs-lookup"><span data-stu-id="e3473-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="e3473-126">Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på en prosjektbasert tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Tilbudslinjeoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="e3473-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="e3473-127">Du kan også oppdatere faktureringstypen for en prosjektoppgave i **Faktureringstype**-feltet i delrutenettet på faktureringsoppsettet for oppgaven for prosjektet som viser tilbudslinjene som er knyttet til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="e3473-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e3473-128">Oppdatere en rolle til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e3473-129">En rolle kan være belastbar eller ikke-belastbar i konteksten for en bestemt prosjektbasert tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="e3473-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="e3473-130">Du kan konfigurere faktureringstypen for en rolle i kategorien **Belastbare roller** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare roller**.</span><span class="sxs-lookup"><span data-stu-id="e3473-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e3473-131">Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e3473-132">En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="e3473-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="e3473-133">Du kan konfigurere faktureringstypen for en transaksjon i kategorien **Belastbare kategorier** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare kategorier**.</span><span class="sxs-lookup"><span data-stu-id="e3473-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="e3473-134">Løse belastbarhet</span><span class="sxs-lookup"><span data-stu-id="e3473-134">Resolve chargeability</span></span>
<span data-ttu-id="e3473-135">Et estimat eller en faktisk verdi opprettet for tid regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="e3473-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="e3473-136">**Tid** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="e3473-137">**Rolle** er konfigurert som belastbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="e3473-138">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="e3473-139">Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="e3473-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="e3473-140">Et estimat eller en faktisk verdi opprettet for utgift regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="e3473-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="e3473-141">**Utgift** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="e3473-142">**Transaksjonskategori** er konfigurert som belastbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="e3473-143">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="e3473-144">Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="e3473-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="e3473-145">Et estimat eller en faktisk verdi opprettet for materialer regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="e3473-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="e3473-146">**Materialer** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="e3473-147">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="e3473-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="e3473-148">Hvis disse to tingene er oppfylt, skal **oppgaven** også være konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="e3473-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-149">
                    <strong>Inkluderer tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e3473-150">
                    <strong>Inkluderer utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e3473-151">
                    <strong>Inkluder materialer</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="e3473-152">
                    <strong>Inkluderte oppgaver</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-153">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-155">
                    <strong>Oppgave</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="e3473-156">
                    <strong>Innvirkning på belastbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-157">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-158">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-159">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-160">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-161">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-162">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-163">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-164">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-165">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-166">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-167">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-168">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-169">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-170">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3473-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-171">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-172">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-173">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-174">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-175">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-176">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-177">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-178">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-179">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-180">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3473-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-181">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-182">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-183">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-184">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-185">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-186">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-187">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-188">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-189">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-190">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3473-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-191">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-192">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-193">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-194">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-195">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-196">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-197">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-198">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-199">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-200">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3473-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-201">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-202">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-203">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-204">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-205">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-206">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-207">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-208">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-209">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-210">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="e3473-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-211">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-212">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-213">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-214">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-215">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-216">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-218">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-219">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-220">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-221">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-222">
                    <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-223">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-224">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-225">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-226">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-228">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-229">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-230">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-231">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-232">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-233">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-234">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-235">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-236">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-237">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e3473-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-239">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-240">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-241">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-242">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-243">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-244">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-245">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-246">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-247">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e3473-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e3473-249">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-250">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-251">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-252">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-253">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-254">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-255">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-256">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-257">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-258">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e3473-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-260">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-261">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-262">Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-263">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-264">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-265">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="e3473-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e3473-266">Faktureringstype for en faktisk materialeverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e3473-267">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e3473-268">Ja</span><span class="sxs-lookup"><span data-stu-id="e3473-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e3473-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e3473-270">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="e3473-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e3473-271">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e3473-272">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e3473-273">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="e3473-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e3473-274">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-275">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e3473-276">Faktureringstype for en faktisk materialeverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3473-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
