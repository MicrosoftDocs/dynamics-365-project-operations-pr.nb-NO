---
title: Oversikt over prosjektbaserte kontraktlinjer
description: Dette emnet inneholder informasjon om arbeid med prosjektbaserte kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858170"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="685f5-103">Oversikt over prosjektbaserte kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="685f5-103">Project-based contract lines overview</span></span>

<span data-ttu-id="685f5-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="685f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="685f5-105">Prosjektbaserte kontraktlinjer i Dynamics 365 Project Operations er utformet for å inneholde estimat- og faktureringsavtaler for bestemte komponenter av prosjektarbeid for et engasjement.</span><span class="sxs-lookup"><span data-stu-id="685f5-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="685f5-106">Strukturen til en prosjektbasert kontraktlinje utvides for prosjektestimater og faktureringsscenarioer med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="685f5-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="685f5-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="685f5-107">Billing method</span></span>
- <span data-ttu-id="685f5-108">Prosjekt- og oppgavetilordning</span><span class="sxs-lookup"><span data-stu-id="685f5-108">Project and task mapping</span></span>
- <span data-ttu-id="685f5-109">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="685f5-109">Included transaction classes</span></span>
- <span data-ttu-id="685f5-110">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="685f5-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="685f5-111">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="685f5-111">Chargeability setup</span></span>
- <span data-ttu-id="685f5-112">Estimater ved hjelp av kontraktlinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="685f5-112">Estimates using contract line details</span></span>
- <span data-ttu-id="685f5-113">Kontraktlinjekunder</span><span class="sxs-lookup"><span data-stu-id="685f5-113">Contract line customers</span></span>

<span data-ttu-id="685f5-114">Følgende tabell inneholder feltene i kategorien **Generelt** i prosjektbaserte kontraktlinjer som hjelper deg med å sette opp grunnlaget for et detaljert grunnleggende estimat og faktureringsordninger for prosjektbasert arbeid.</span><span class="sxs-lookup"><span data-stu-id="685f5-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="685f5-115">Felt</span><span class="sxs-lookup"><span data-stu-id="685f5-115">Field</span></span> | <span data-ttu-id="685f5-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="685f5-116">Description</span></span> | <span data-ttu-id="685f5-117">Nedstrøms påvirkning</span><span class="sxs-lookup"><span data-stu-id="685f5-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="685f5-118">**Navn**</span><span class="sxs-lookup"><span data-stu-id="685f5-118">**Name**</span></span> | <span data-ttu-id="685f5-119">Navnet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-119">Name of the contract line.</span></span> <span data-ttu-id="685f5-120">Dette identifiserer den separate komponenten i kontrakten som blir estimert.</span><span class="sxs-lookup"><span data-stu-id="685f5-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="685f5-121">For en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra en tilsvarende verdi av den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="685f5-122">Navnet som kopieres over prosjektfakturalinjen som opprettes fra denne kontraktlinjen når fakturaen opprettes.</span><span class="sxs-lookup"><span data-stu-id="685f5-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="685f5-123">**Faktureringsmetode**</span><span class="sxs-lookup"><span data-stu-id="685f5-123">**Billing Method**</span></span> | <span data-ttu-id="685f5-124">På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="685f5-125">Dette er et alternativsett som representerer de to hovedkontraktmodellene som støttes av Project Operations:</span><span class="sxs-lookup"><span data-stu-id="685f5-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="685f5-126">- **Fast pris**</span><span class="sxs-lookup"><span data-stu-id="685f5-126">- **Fixed Price**</span></span></br><span data-ttu-id="685f5-127">- **Tid og materiale**</span><span class="sxs-lookup"><span data-stu-id="685f5-127">- **Time and Material**</span></span> | <span data-ttu-id="685f5-128">Basert på faktureringsmetoden for den refererte kontraktlinjen blir den faktiske transaksjonen behandlet.</span><span class="sxs-lookup"><span data-stu-id="685f5-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="685f5-129">Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for tid og materialer, opprettes det poster for kostnader og ufakturerte faktiske salgsverdier.</span><span class="sxs-lookup"><span data-stu-id="685f5-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="685f5-130">Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for fast pris, blir bare en faktisk kostnad opprettet.</span><span class="sxs-lookup"><span data-stu-id="685f5-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="685f5-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="685f5-131">**Project**</span></span> | <span data-ttu-id="685f5-132">Bruk dette feltet til å identifisere prosjektet som skal brukes til å levere arbeidet på dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="685f5-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="685f5-133">Denne verdien brukes sammen med **Inkluderte oppgaver** og **Inkluderte transaksjonsklasser** til å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring.</span><span class="sxs-lookup"><span data-stu-id="685f5-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="685f5-134">**Inkluderte oppgaver**</span><span class="sxs-lookup"><span data-stu-id="685f5-134">**Included Tasks**</span></span> | <span data-ttu-id="685f5-135">Angir om denne kontraktlinjen inneholder alle prosjektoppgaver for det valgte prosjektet eller bare et delsett av oppgavene.</span><span class="sxs-lookup"><span data-stu-id="685f5-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="685f5-136">Dette er et alternativsett som har følgende mulige verdier:</span><span class="sxs-lookup"><span data-stu-id="685f5-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="685f5-137">- **Alle prosjektoppgaver**</span><span class="sxs-lookup"><span data-stu-id="685f5-137">- **All Project Tasks**</span></span></br><span data-ttu-id="685f5-138">- **Bare valgte prosjektoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="685f5-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="685f5-139">En tom verdi i dette feltet er det samme som å velge **Alle prosjektoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="685f5-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="685f5-140">Hvis **Bare valgte oppgaver** er valgt, kan du velge bestemte oppgaver og knytte dem til denne kontraktlinjen i kategorien **Faktureringsoppsett for oppgave** på siden **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="685f5-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="685f5-141">Verdien brukes sammen med klassene **Prosjekt** og **Inkludert transaksjon** for å løse kontraktlinjereferansen på en linjeoppføring for faktisk eller beregnet verdi.</span><span class="sxs-lookup"><span data-stu-id="685f5-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="685f5-142">**Inkluder tid**</span><span class="sxs-lookup"><span data-stu-id="685f5-142">**Include Time**</span></span> | <span data-ttu-id="685f5-143">En **Ja**/**Nei**-verdi angir om tidstransaksjoner eller arbeidskostnader for det valgte prosjektet skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="685f5-144">En **Nei**-verdi angir at tidstransaksjonene eller arbeidskostnader ikke skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="685f5-145">En **Ja**-verdi angir at de tas med.</span><span class="sxs-lookup"><span data-stu-id="685f5-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="685f5-146">Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring.</span><span class="sxs-lookup"><span data-stu-id="685f5-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="685f5-147">**Inkluder utgift**</span><span class="sxs-lookup"><span data-stu-id="685f5-147">**Include Expense**</span></span> | <span data-ttu-id="685f5-148">En **Ja**/**Nei**-verdi angir om utgiftskostnader for det valgte prosjektet skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="685f5-149">En **Nei**-verdi angir at utgiftskostnaden ikke skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="685f5-150">En **Ja**-verdi angir at den tas med.</span><span class="sxs-lookup"><span data-stu-id="685f5-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="685f5-151">Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring.</span><span class="sxs-lookup"><span data-stu-id="685f5-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="685f5-152">**Inkluder materialer**</span><span class="sxs-lookup"><span data-stu-id="685f5-152">**Include Materials**</span></span> | <span data-ttu-id="685f5-153">En **Ja**/**Nei**-verdi angir om materialkostnader for det valgte prosjektet skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="685f5-154">En **Nei**-verdi angir at materialkostnader ikke skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="685f5-155">En **Ja**-verdi angir at den tas med.</span><span class="sxs-lookup"><span data-stu-id="685f5-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="685f5-156">Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring.</span><span class="sxs-lookup"><span data-stu-id="685f5-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="685f5-157">**Inkluder gebyr**</span><span class="sxs-lookup"><span data-stu-id="685f5-157">**Include Fee**</span></span> | <span data-ttu-id="685f5-158">En **Ja**/**Nei**-verdi angir om gebyrer for det valgte prosjektet skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="685f5-159">En **Nei**-verdi angir at avgiftene ikke skal tas med på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="685f5-160">En **Ja**-verdi angir at de tas med.</span><span class="sxs-lookup"><span data-stu-id="685f5-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="685f5-161">Denne verdien brukes sammen med prosjektet for å løse kontraktlinjereferansen for en faktisk verdi eller estimatlinjeoppføring.</span><span class="sxs-lookup"><span data-stu-id="685f5-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="685f5-162">**Avtalt beløp**</span><span class="sxs-lookup"><span data-stu-id="685f5-162">**Contracted Amount**</span></span> | <span data-ttu-id="685f5-163">På en kontraktlinje med fast pris er dette beløpet den avtalte verdien som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="685f5-164">På en kontraktlinje for tid og materialer er dette beløpet en estimert verdi av hva som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="685f5-165">På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="685f5-166">Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra beløpet på kontraktlinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="685f5-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="685f5-167">Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre beløpene i linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="685f5-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="685f5-168">På en fastpriskontraktlinje brukes denne verdien til å generere beløpet før avgift på periodiske faktureringsmilepæler.</span><span class="sxs-lookup"><span data-stu-id="685f5-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="685f5-169">**Beregnet mva**</span><span class="sxs-lookup"><span data-stu-id="685f5-169">**Estimated Tax**</span></span> | <span data-ttu-id="685f5-170">Brukeren kan redigere dette feltet for å angi det estimerte avgiftsbeløpet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="685f5-171">Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra avgiftsbeløpet på kontraktlinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="685f5-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="685f5-172">Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre avgiftsbeløpene i linjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="685f5-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="685f5-173">På en fastpriskontraktlinje brukes denne verdien til å generere avgiften på periodiske faktureringsmilepæler.</span><span class="sxs-lookup"><span data-stu-id="685f5-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="685f5-174">**Avtalt beløp etter mva**</span><span class="sxs-lookup"><span data-stu-id="685f5-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="685f5-175">Kontraktlinjebeløpet etter mva.</span><span class="sxs-lookup"><span data-stu-id="685f5-175">The contract line amount after tax.</span></span> <span data-ttu-id="685f5-176">Dette feltet er skrivebeskyttet og beregnes som **Avtalt beløp + avgift**.</span><span class="sxs-lookup"><span data-stu-id="685f5-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="685f5-177">På en fastpriskontraktlinje brukes denne verdien til å generere periodiske faktureringsmilepæler.</span><span class="sxs-lookup"><span data-stu-id="685f5-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="685f5-178">**Må ikke overskrides-grense**</span><span class="sxs-lookup"><span data-stu-id="685f5-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="685f5-179">Brukeren kan redigere dette feltet, og det er bare tilgjengelig i prosjektbaserte kontraktlinjer der faktureringsmetoden er satt til tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="685f5-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="685f5-180">Brukeren kan redigere dette feltet.</span><span class="sxs-lookup"><span data-stu-id="685f5-180">The user can edit this field.</span></span> <span data-ttu-id="685f5-181">Når en faktisk verdi for tid og materiale refererer til denne kontraktlinjen for tid og materialer, evalueres beløpet på den faktiske verdien mot grensen som ikke må overskrides på denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="685f5-182">Denne evalueringen er fullført etter at de allerede brukte og beregnede beløpene er inkludert.</span><span class="sxs-lookup"><span data-stu-id="685f5-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="685f5-183">**Kundebudsjett**</span><span class="sxs-lookup"><span data-stu-id="685f5-183">**Customer Budget**</span></span> | <span data-ttu-id="685f5-184">Dette feltet er redigerbart og kopieres fra det tilsvarende feltet på tilbudslinjen, hvis kontrakten ble opprettet fra et tilbud.</span><span class="sxs-lookup"><span data-stu-id="685f5-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="685f5-185">Dette feltet brukes bare til informasjon og har ikke noen nedstrøms signifikans.</span><span class="sxs-lookup"><span data-stu-id="685f5-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="685f5-186">Valideringsreglene for alternativene i kategorien Generelt for prosjektbaserte kontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="685f5-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="685f5-187">Regel 1: Hvis feltet **Inkluderte aktiviteter** er tomt eller satt til **Alle prosjektoppgaver**, inkluderes alle oppgavene for prosjektet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="685f5-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="685f5-188">Regel 2: Når feltet **Inkluderte oppgaver** er tomt eller eksplisitt satt til **Alle prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse bare tas med på én prosjektbasert kontraktlinje i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="685f5-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="685f5-189">Regel 3: Når feltet **Inkluderte oppgaver** er satt til **Bare valgte prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse tas med på flere prosjektbasert kontraktlinjer i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="685f5-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="685f5-190">
                    <strong>Kontrakt</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="685f5-191">
                    <strong>Kontraktlinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="685f5-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="685f5-193">
                    <strong>Inkluderte oppgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="685f5-194">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="685f5-195">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="685f5-196">
                    <strong>Inkluder materialer</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="685f5-197">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="685f5-198">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="685f5-199">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="685f5-200">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="685f5-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-201">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-202">CL1</span><span class="sxs-lookup"><span data-stu-id="685f5-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-203">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-204">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-205">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-206">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-207">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-208">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-209">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="685f5-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-210">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="685f5-210">Violation of Rule #2.</span></span> <span data-ttu-id="685f5-211">Tid, utgifter, materialer og gebyrer for P1-prosjektet er inkludert både på kontraktlinje CL1 og CL2.</span><span class="sxs-lookup"><span data-stu-id="685f5-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-212">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-213">CL2</span><span class="sxs-lookup"><span data-stu-id="685f5-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-214">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-215">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-216">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-217">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-218">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-219">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-220">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-221">CL1</span><span class="sxs-lookup"><span data-stu-id="685f5-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-222">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-223">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-224">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-225">No</span><span class="sxs-lookup"><span data-stu-id="685f5-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-226">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-227">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-228">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="685f5-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-229">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="685f5-229">Violation of Rule #2.</span></span> <span data-ttu-id="685f5-230">Tid, materialer og gebyrer for P1-prosjektet er inkludert både på kontraktlinje CL1 og CL2.</span><span class="sxs-lookup"><span data-stu-id="685f5-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-231">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-232">CL2</span><span class="sxs-lookup"><span data-stu-id="685f5-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-233">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-234">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-235">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-236">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-237">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-238">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-239">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-240">CL1</span><span class="sxs-lookup"><span data-stu-id="685f5-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-241">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-242">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-243">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-244">No</span><span class="sxs-lookup"><span data-stu-id="685f5-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-245">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-246">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-247">Gyldig</span><span class="sxs-lookup"><span data-stu-id="685f5-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-248">Tid, materialer og gebyrer for P1-prosjektet er inkludert på CL1.</span><span class="sxs-lookup"><span data-stu-id="685f5-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="685f5-249">Utgift i P1-prosjektet er inkludert i CL2.</span><span class="sxs-lookup"><span data-stu-id="685f5-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="685f5-250">Ingen overlapping i hva som inkluderes på hver kontraktlinje, og er derfor gyldig.</span><span class="sxs-lookup"><span data-stu-id="685f5-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-251">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-252">CL2</span><span class="sxs-lookup"><span data-stu-id="685f5-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-253">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-254">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-255">No</span><span class="sxs-lookup"><span data-stu-id="685f5-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-256">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-257">No</span><span class="sxs-lookup"><span data-stu-id="685f5-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-258">No</span><span class="sxs-lookup"><span data-stu-id="685f5-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-259">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-260">CL1</span><span class="sxs-lookup"><span data-stu-id="685f5-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-261">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-262">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="685f5-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-263">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-264">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-265">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-266">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-267">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="685f5-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-268">Brudd på regel nr. 2</span><span class="sxs-lookup"><span data-stu-id="685f5-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="685f5-269">C1 inkluderer tid, materialer, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="685f5-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="685f5-270">CL2 inkluderer tid, materialer, utgifter og gebyrer for hele prosjekt P1, og overlapper derfor med det som er inkludert på C1.</span><span class="sxs-lookup"><span data-stu-id="685f5-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-271">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-272">CL2</span><span class="sxs-lookup"><span data-stu-id="685f5-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-273">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-274">Tomt</span><span class="sxs-lookup"><span data-stu-id="685f5-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-275">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-276">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-277">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-278">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-279">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-280">CL1</span><span class="sxs-lookup"><span data-stu-id="685f5-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-281">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-282">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="685f5-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-283">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-284">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-285">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-286">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-287">Gyldig</span><span class="sxs-lookup"><span data-stu-id="685f5-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="685f5-288">I henhold til regel nr. 3</span><span class="sxs-lookup"><span data-stu-id="685f5-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="685f5-289">C1 inkluderer tid, utgifter, materialer og gebyrer for et delsett med oppgaver på prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="685f5-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="685f5-290">CL2 inkluderer tid, utgifter, materialer og gebyrer for et delsett med oppgaver på prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="685f5-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="685f5-291">Den eneste ekstra valideringen er om delsettet av oppgaver på CL1 skiller seg fra delsettet av oppgaver på CL2, for å sikre at det ikke overlapper der.</span><span class="sxs-lookup"><span data-stu-id="685f5-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="685f5-292">Dette gjøres av systemet når oppgaver er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="685f5-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="685f5-293">C1</span><span class="sxs-lookup"><span data-stu-id="685f5-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="685f5-294">CL2</span><span class="sxs-lookup"><span data-stu-id="685f5-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-295">P1</span><span class="sxs-lookup"><span data-stu-id="685f5-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="685f5-296">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="685f5-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-297">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="685f5-298">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-299">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="685f5-300">Ja</span><span class="sxs-lookup"><span data-stu-id="685f5-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
