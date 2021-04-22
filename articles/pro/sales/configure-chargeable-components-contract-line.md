---
title: Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje
description: Dette emnet gir informasjon om hvordan du legger til belastbare komponenter i kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858485"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="3468d-103">Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje</span><span class="sxs-lookup"><span data-stu-id="3468d-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="3468d-104">_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="3468d-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3468d-105">En prosjektbasert kontraktlinje har *inkluderte* komponenter og *belastbare* komponenter.</span><span class="sxs-lookup"><span data-stu-id="3468d-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="3468d-106">Inkluderte komponenter er komponenter som er underlagt følgende:</span><span class="sxs-lookup"><span data-stu-id="3468d-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="3468d-107">Faktureringsmetode og kundedelinger</span><span class="sxs-lookup"><span data-stu-id="3468d-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="3468d-108">Må ikke overskrides-grenser</span><span class="sxs-lookup"><span data-stu-id="3468d-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="3468d-109">Innstillinger for fakturafrekvens som er definert på den prosjektbaserte kontraktlinjen</span><span class="sxs-lookup"><span data-stu-id="3468d-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="3468d-110">Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="3468d-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="3468d-111">Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en kontraktlinje:</span><span class="sxs-lookup"><span data-stu-id="3468d-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="3468d-112">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-112">Chargeable</span></span>
  - <span data-ttu-id="3468d-113">Ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-113">Non-chargeable</span></span>

<span data-ttu-id="3468d-114">Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="3468d-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="3468d-115">Belastbar er definert i oppgaver for en prosjektkontraktlinje og gjelder for alle transaksjonsklasser som finnes på linjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="3468d-116">Hvis **Inkluder oppgaver**-feltet på en kontraktlinje er tomt eller satt til **Hele prosjektet**, er ikke **Belastbare oppgaver**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3468d-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="3468d-117">Belastbarhet definert for roller for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Tid**.</span><span class="sxs-lookup"><span data-stu-id="3468d-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="3468d-118">Hvis feltet **Inkluder td** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare roller**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3468d-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="3468d-119">Belastbarhet definert for transaksjonskategorier for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="3468d-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="3468d-120">Hvis feltet **Inkluder utgifter** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare kategorier**-fanen tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="3468d-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3468d-121">Oppdatere en prosjektoppgave som belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="3468d-122">En prosjektoppgave kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje, noe som gjør følgende oppsett mulig:</span><span class="sxs-lookup"><span data-stu-id="3468d-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="3468d-123">Hvis en prosjektbasert kontraktlinje inkluderer **Tid** og en bestemt oppgave, er **T1** knyttet til den som belastbar.</span><span class="sxs-lookup"><span data-stu-id="3468d-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="3468d-124">Hvis det er en ny kontraktlinje som inkluderer **Utgift**, kan du knytte T1-oppgaven på kontraktlinjen som ikke-belastbar.</span><span class="sxs-lookup"><span data-stu-id="3468d-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="3468d-125">Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter er ikke-belastbare.</span><span class="sxs-lookup"><span data-stu-id="3468d-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="3468d-126">Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på kontraktlinjen ved å oppdatere **Fakturatype**-feltet i delrutenettet for kontraktlinjeoppgaver.</span><span class="sxs-lookup"><span data-stu-id="3468d-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="3468d-127">Du kan også oppdatere **Faktureringstype**-feltet i delrutenettet for faktureringsoppsettet for oppgaven for prosjektet som viser kontraktlinjene som er knyttet til en oppgave.</span><span class="sxs-lookup"><span data-stu-id="3468d-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3468d-128">Oppdatere en rolle som belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="3468d-129">En rolle kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="3468d-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="3468d-130">Du kan konfigurere fakturerings typen for en rolle på **Belastbare roller**-fanen på en kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="3468d-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="3468d-131">Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare roller**.</span><span class="sxs-lookup"><span data-stu-id="3468d-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="3468d-132">Oppdatere en transaksjonskategori som belastbar eller ikke-belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="3468d-133">En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="3468d-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="3468d-134">Du kan konfigurere faktureringstypen for en transaksjon på **Belastbare kategorier**-fanen på en prosjektbasert kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="3468d-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="3468d-135">Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare kategorier**.</span><span class="sxs-lookup"><span data-stu-id="3468d-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="3468d-136">Løse belastbarhet</span><span class="sxs-lookup"><span data-stu-id="3468d-136">Resolve chargeability</span></span>

<span data-ttu-id="3468d-137">Et estimat eller en faktisk verdi opprettet for tid regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="3468d-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="3468d-138">**Tid** er inkludert på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="3468d-139">**Rolle** er konfigurert som belastbar på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="3468d-140">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="3468d-141">Hvis disse tre tingene er oppfylt, er oppgaven konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="3468d-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="3468d-142">Et estimat eller en faktisk verdi opprettet for utgift regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="3468d-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="3468d-143">**Utgift** er inkludert på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="3468d-144">**Transaksjonskategori** er konfigurert som belastbar på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="3468d-145">**Inkluderte oppgaver** er satt til **Valgt oppgave** på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="3468d-146">Hvis disse tre tingene er oppfylt, er **oppgaven** konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="3468d-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="3468d-147">Et estimat eller en faktisk verdi opprettet for materialer regnes bare som belastbar hvis:</span><span class="sxs-lookup"><span data-stu-id="3468d-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="3468d-148">**Materialer** er inkludert på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="3468d-149">**Inkluderte oppgaver** er satt til **Valgte oppgaver** på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="3468d-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="3468d-150">Hvis disse to tingene er oppfylt, er **oppgaven** konfigurert som belastbar.</span><span class="sxs-lookup"><span data-stu-id="3468d-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-151">
                    <strong>Inkluderer tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3468d-152">
                    <strong>Inkluderer utgift</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3468d-153">
                    <strong>Inkluder materialer</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="3468d-154">
                    <strong>Inkluderte oppgaver</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-155">
                    <strong>Rolle</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-157">
                    <strong>Oppgave</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="3468d-158">
                    <strong>Innvirkning på belastbarhet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-159">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-160">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-161">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-162">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-163">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-164">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-165">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-166">Fakturering på en faktisk tidsverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-167">Faktureringstype for en faktisk utgiftsverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-168">Faktureringstype for en faktisk materialeverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-169">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-170">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-171">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-172">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="3468d-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-173">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-174">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-175">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-176">Fakturering på en faktisk tidsverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-177">Faktureringstype for en faktisk utgiftsverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-178">Faktureringstype for en faktisk materialeverdi: <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-179">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-180">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-181">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-182">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="3468d-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-183">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-184">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-185">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-186">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-187">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3468d-188">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-189">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-190">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-191">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-192">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="3468d-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-193">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-194">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-195">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-196">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-197">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-198">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-199">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-200">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-201">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-202">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="3468d-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-203">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-204">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-205">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-206">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-207">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-208">Faktureringstype for en faktisk materialeverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-209">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-210">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-211">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-212">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="3468d-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-213">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-214">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-215">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-216">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-217">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-218">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-220">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-221">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-222">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-223">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-224">
                    <strong>Belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-225">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-226">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-227">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3468d-228">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-230">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-231">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-232">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-233">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-234">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-235">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-236">Fakturering på en faktisk tidsverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-237">Faktureringstype for en faktisk utgiftsverdi: <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-238">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-239">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3468d-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-241">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-242">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-243">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-244">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-245">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-246">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3468d-247">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-248">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-249">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="3468d-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="3468d-251">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-252">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-253">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-254">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-255">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-256">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-257">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-258">Faktureringstype for en faktisk materialeverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-259">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-260">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3468d-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-262">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-263">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-264">Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-265">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-266">Fakturering på en faktisk tidsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3468d-267">Faktureringstype for en faktisk utgiftsverdi: Belastbar</span><span class="sxs-lookup"><span data-stu-id="3468d-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="3468d-268">Faktureringstype for en faktisk materialeverdi: <strong>Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="3468d-269">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="3468d-270">Ja</span><span class="sxs-lookup"><span data-stu-id="3468d-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="3468d-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="3468d-272">Hele prosjektet</span><span class="sxs-lookup"><span data-stu-id="3468d-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="3468d-273">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="3468d-274">
                    <strong>Ikke-belastbar</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="3468d-275">Kan ikke angis</span><span class="sxs-lookup"><span data-stu-id="3468d-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="3468d-276">Fakturering på en faktisk tidsverdi: <strong>Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-277">Faktureringstype for en faktisk utgiftsverdi:<strong> Ikke-belastbar </strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="3468d-278">Faktureringstype for en faktisk materialeverdi:<strong> Ikke tilgjengelig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="3468d-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
