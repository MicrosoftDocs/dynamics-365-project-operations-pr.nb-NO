---
title: Konfigurere de belastbare komponentene i en tilbudslinje
description: Dette emnet gir informasjon om hvordan du konfigurerer belastbare og ikke-belastbare komponenter på en prosjektbasert tilbudslinje.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858305"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="d0f25-103">Konfigurere de belastbare komponentene i en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="d0f25-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="d0f25-104">_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="d0f25-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d0f25-105">En prosjektbasert tilbudslinje har konseptet *inkluderte* komponenter og *belastbare* komponenter.</span><span class="sxs-lookup"><span data-stu-id="d0f25-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="d0f25-106">Inkluderte komponenter er underlagt følgende:</span><span class="sxs-lookup"><span data-stu-id="d0f25-106">Included components are subject to:</span></span>

  - <span data-ttu-id="d0f25-107">Faktureringsmetode og kundedelinger</span><span class="sxs-lookup"><span data-stu-id="d0f25-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="d0f25-108">Må ikke overskrides-grenser</span><span class="sxs-lookup"><span data-stu-id="d0f25-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="d0f25-109">Innstillinger for fakturafrekvens som er definert på den prosjektbaserte tilbudslinjen</span><span class="sxs-lookup"><span data-stu-id="d0f25-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="d0f25-110">Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="d0f25-111">Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en tilbudslinje:</span><span class="sxs-lookup"><span data-stu-id="d0f25-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="d0f25-112">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-112">Chargeable</span></span>
  - <span data-ttu-id="d0f25-113">Ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-113">Non-chargeable</span></span>

<span data-ttu-id="d0f25-114">Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="d0f25-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="d0f25-115">Belastbarhet er definert i oppgavene for en tilbudslinje og gjelder for alle transaksjonsklasser som finnes på denne linjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="d0f25-116">Hvis feltet **Inkluder oppgaver** satt til **Hele prosjektet** eller er tomt, er ikke **Belastbare oppgaver**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d0f25-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="d0f25-117">Belastbarhet er definert for roller for en tilbudslinje og gjelder bare transaksjonsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="d0f25-118">Hvis feltet **Inkluder td** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare roller**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d0f25-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="d0f25-119">Belastbarhet er definert for transaksjonskategorier for en tilbudslinje og gjelder bare transaksjonsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="d0f25-120">Hvis feltet **Inkluder utgifter** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare kategorier**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d0f25-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d0f25-121">Oppdatere en prosjektoppgave til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d0f25-122">En prosjektoppgave kan være belastbar eller ikke-belastbar i konteksten til en bestemt prosjektbasert tilbudslinje, noe som gjør følgende oppsett mulig.</span><span class="sxs-lookup"><span data-stu-id="d0f25-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="d0f25-123">Hvis en prosjektbasert tilbudslinje inkluderer **Tid** og oppgaven **T1**, knyttes oppgaven til tilbudslinjen som belastbar.</span><span class="sxs-lookup"><span data-stu-id="d0f25-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="d0f25-124">Hvis det er en ny tilbudslinje som inkluderer **Utgifter**, kan du knytte til **T1**-oppgaven på tilbudslinjen som ikke-belastbar.</span><span class="sxs-lookup"><span data-stu-id="d0f25-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="d0f25-125">Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter som registreres på oppgaven, er ikke-belastbare.</span><span class="sxs-lookup"><span data-stu-id="d0f25-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="d0f25-126">Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på en prosjektbasert tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Tilbudslinjeoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="d0f25-127">Du kan også oppdatere faktureringstypen for en prosjektoppgave i **Faktureringstype**-feltet i delrutenettet på faktureringsoppsettet for oppgaven for prosjektet som viser tilbudslinjene som er knyttet til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="d0f25-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d0f25-128">Oppdatere en rolle til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d0f25-129">En rolle kan være belastbar eller ikke-belastbar i konteksten for en bestemt prosjektbasert tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="d0f25-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="d0f25-130">Du kan konfigurere faktureringstypen for en rolle i kategorien **Belastbare roller** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare roller**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="d0f25-131">Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="d0f25-132">En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="d0f25-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="d0f25-133">Du kan konfigurere faktureringstypen for en transaksjon i kategorien **Belastbare kategorier** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare kategorier**.</span><span class="sxs-lookup"><span data-stu-id="d0f25-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="d0f25-134">Løse belastbarhet</span><span class="sxs-lookup"><span data-stu-id="d0f25-134">Resolve chargeability</span></span>
<span data-ttu-id="d0f25-135">Et estimat eller en faktisk verdi opprettet for tid regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="d0f25-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="d0f25-136">**Tid** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="d0f25-137">**Rolle** er konfigurert som belastbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="d0f25-138">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="d0f25-139">Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="d0f25-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="d0f25-140">Et estimat eller en faktisk verdi opprettet for utgift regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="d0f25-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="d0f25-141">**Utgift** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="d0f25-142">**Transaksjonskategori** er konfigurert som belastbar på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="d0f25-143">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="d0f25-144">Hvis disse tre tingene er oppfylt, er **oppgaven** også konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="d0f25-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="d0f25-145">Et estimat eller en faktisk verdi opprettet for materialer regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="d0f25-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="d0f25-146">**Materialer** er inkludert på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="d0f25-147">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d0f25-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="d0f25-148">Hvis disse to tingene er oppfylt, skal **oppgaven** også være konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="d0f25-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-149">
                    <strong>Inkluderer tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d0f25-150">
                    <strong>Inkluderer utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d0f25-151">
                    <strong>Inkluder materialer</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="d0f25-152">
                    <strong>Inkluderte oppgaver</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-153">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-155">
                    <strong>Oppgave</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="d0f25-156">
                    <strong>Innvirkning på belastbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-157">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-158">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-159">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-160">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-161">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-162">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-163">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-164">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-165">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-166">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-167">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-168">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-169">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-170">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d0f25-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-171">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-172">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-173">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-174">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-175">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-176">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-177">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-178">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-179">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-180">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d0f25-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-181">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-182">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-183">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-184">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-185">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-186">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-187">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-188">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-189">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-190">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d0f25-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-191">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-192">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-193">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-194">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-195">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-196">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-197">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-198">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-199">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-200">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d0f25-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-201">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-202">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-203">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-204">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-205">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-206">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-207">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-208">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-209">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-210">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d0f25-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-211">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-212">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-213">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-214">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-215">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-216">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-218">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-219">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-220">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-221">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-222">
                    <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-223">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-224">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-225">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-226">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-228">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-229">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-230">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-231">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-232">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-233">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-234">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-235">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-236">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-237">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d0f25-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-239">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-240">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-241">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-242">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-243">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-244">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-245">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-246">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-247">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="d0f25-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="d0f25-249">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-250">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-251">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-252">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-253">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-254">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-255">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-256">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-257">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-258">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d0f25-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-260">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-261">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-262">Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-263">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-264">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-265">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="d0f25-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="d0f25-266">Faktureringstype for en faktisk materialeverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="d0f25-267">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="d0f25-268">Ja</span><span class="sxs-lookup"><span data-stu-id="d0f25-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="d0f25-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="d0f25-270">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="d0f25-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="d0f25-271">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="d0f25-272">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="d0f25-273">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="d0f25-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="d0f25-274">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-275">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="d0f25-276">Faktureringstype for en faktisk materialeverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d0f25-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
