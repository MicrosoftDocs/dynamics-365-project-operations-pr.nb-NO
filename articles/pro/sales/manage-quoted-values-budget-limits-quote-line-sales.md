---
title: Oversikt over prosjektbaserte tilbudslinjer
description: Dette emnet gir informasjon om hvordan du bruker prosjektbaserte tilbudslinjer for prosjektarbeid.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369883"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="c4515-103">Oversikt over prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="c4515-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="c4515-104">_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="c4515-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c4515-105">Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement.</span><span class="sxs-lookup"><span data-stu-id="c4515-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c4515-106">Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="c4515-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c4515-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="c4515-107">Billing Method</span></span>
- <span data-ttu-id="c4515-108">Prosjekt- og oppgavetilordning</span><span class="sxs-lookup"><span data-stu-id="c4515-108">Project and Task Mapping</span></span>
- <span data-ttu-id="c4515-109">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="c4515-109">Included Transaction classes</span></span>
- <span data-ttu-id="c4515-110">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="c4515-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c4515-111">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="c4515-111">Chargeability setup</span></span>
- <span data-ttu-id="c4515-112">Estimering ved hjelp av tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="c4515-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c4515-113">Kunder for tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="c4515-113">Quote line Customers</span></span>

<span data-ttu-id="c4515-114">Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="c4515-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c4515-115">Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="c4515-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c4515-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="c4515-116">**Field**</span></span> | <span data-ttu-id="c4515-117">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="c4515-117">**Description**</span></span> | <span data-ttu-id="c4515-118">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="c4515-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c4515-119">Navn</span><span class="sxs-lookup"><span data-stu-id="c4515-119">Name</span></span> | <span data-ttu-id="c4515-120">Navnet på tilbudslinjen som gjør det enklere å identifisere den diskrete komponenten i tilbudet som blir beregnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c4515-121">Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="c4515-122">Billing Method</span></span> | <span data-ttu-id="c4515-123">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c4515-124">Dette feltet omfatter de to hovedkontraktsmodellene som støttes av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c4515-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c4515-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="c4515-125">- Fixed price</span></span></br><span data-ttu-id="c4515-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="c4515-126">- Time and material.</span></span>| <span data-ttu-id="c4515-127">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-128">Project</span><span class="sxs-lookup"><span data-stu-id="c4515-128">Project</span></span> | <span data-ttu-id="c4515-129">Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="c4515-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c4515-130">Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="c4515-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c4515-131">Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj.</span><span class="sxs-lookup"><span data-stu-id="c4515-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c4515-132">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="c4515-133">Inkluderte oppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-133">Included Tasks</span></span> | <span data-ttu-id="c4515-134">Angir om denne tilbudslinjen brukes til alle eller noen av prosjektoppgavene for det valgte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c4515-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="c4515-135">Dette feltet har følgende mulige verdier:</span><span class="sxs-lookup"><span data-stu-id="c4515-135">This field has the following possible values:</span></span></br><span data-ttu-id="c4515-136">- Alle prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-136">- All project tasks</span></span></br><span data-ttu-id="c4515-137">- Bare valgte prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-137">- Selected project tasks only</span></span></br><span data-ttu-id="c4515-138">En tom verdi i dette feltet tilsvarer alternativet **Alle prosjektoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="c4515-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="c4515-139">Når **Bare valgte prosjektoppgaver** velges på prosjektsiden, kan du på fanen **Faktureringsoppsett for oppgave** velge spesifikke oppgaver og tilordne dem til denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="c4515-140">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-141">Inkluder tid</span><span class="sxs-lookup"><span data-stu-id="c4515-141">Include Time</span></span> | <span data-ttu-id="c4515-142">En **Ja**/**Nei**-verdi angir om tidstransaksjoner eller arbeidskostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudstlinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-143">Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-144">Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c4515-145">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-146">Inkluder utgift</span><span class="sxs-lookup"><span data-stu-id="c4515-146">Include Expense</span></span> | <span data-ttu-id="c4515-147">En **Ja**/**Nei**-verdi angir om utgiftskostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-148">Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-149">Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c4515-150">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-151">Inkluder materiale</span><span class="sxs-lookup"><span data-stu-id="c4515-151">Include Material</span></span> | <span data-ttu-id="c4515-152">En **Ja**/**Nei**-verdi angir om materialkostnader for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-153">En **Nei**-verdi angir at materialkostnader ikke skal tas med i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-154">En **Ja**-verdi angir at materialkostnader skal tas med i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c4515-155">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-156">Inkluder gebyr</span><span class="sxs-lookup"><span data-stu-id="c4515-156">Include Fee</span></span> | <span data-ttu-id="c4515-157">En **Ja**/**Nei**-verdi angir om gebyrer for det valgte prosjektet skal tas med i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-158">Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c4515-159">Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c4515-160">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-161">Tilbudsbeløp</span><span class="sxs-lookup"><span data-stu-id="c4515-161">Quoted Amount</span></span> | <span data-ttu-id="c4515-162">Dette er beløpet som blir tilbudt kunden for alt arbeidet som beregnes på denne prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c4515-163">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c4515-164">Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="c4515-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c4515-165">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-166">Beregnet mva</span><span class="sxs-lookup"><span data-stu-id="c4515-166">Estimated Tax</span></span> | <span data-ttu-id="c4515-167">Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c4515-168">Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="c4515-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c4515-169">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-170">Tilbudsbeløp etter mva</span><span class="sxs-lookup"><span data-stu-id="c4515-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="c4515-171">Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="c4515-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c4515-172">Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*.</span><span class="sxs-lookup"><span data-stu-id="c4515-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c4515-173">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-174">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="c4515-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="c4515-175">Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="c4515-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c4515-176">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c4515-177">Kundebudsjett</span><span class="sxs-lookup"><span data-stu-id="c4515-177">Customer Budget</span></span> | <span data-ttu-id="c4515-178">Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="c4515-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c4515-179">Denne verdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet blir vunnet.</span><span class="sxs-lookup"><span data-stu-id="c4515-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c4515-180">Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="c4515-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c4515-181">**Regel 1**: Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver**, inkluderes et prosjekt på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="c4515-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="c4515-182">**Regel 2**: Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="c4515-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c4515-183">**Regel 3**: Hvis feltet **Inkluderte oppgaver** er satt til **Bare valgte prosjektoppgaver**, kan et prosjekt og en bestemt transaksjonsklasse inkluderes på flere prosjektbaserte tilbudslinjer i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="c4515-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="c4515-184">**Regel 4**: Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="c4515-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c4515-185">**Regel 5**: Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="c4515-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="c4515-186">
                    <strong>Salgsmulighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="c4515-187">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="c4515-188">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c4515-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="c4515-190">
                    <strong>Inkluderte oppgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="c4515-191">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="c4515-192">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="c4515-193">
                    <strong>Inkluder materiale</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c4515-194">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c4515-195">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="c4515-196">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="c4515-197">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c4515-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-198">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-199">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-200">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-201">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-202">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-203">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-204">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-205">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-206">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-207">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-208">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="c4515-208">Violation of Rule #2.</span></span> <span data-ttu-id="c4515-209">Tid, utgift og gebyrer i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-210">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-211">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-212">QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-213">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-214">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-215">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-216">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-217">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-218">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-219">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-220">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-221">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-222">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-223">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-224">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-225">No</span><span class="sxs-lookup"><span data-stu-id="c4515-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-226">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-227">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-228">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-229">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="c4515-229">Violation of Rule #2.</span></span> <span data-ttu-id="c4515-230">Tid, materiale og gebyrer i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-231">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-232">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-233">QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-234">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-235">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-236">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-237">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-238">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-239">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-240">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-241">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-242">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-243">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-244">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-245">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-246">No</span><span class="sxs-lookup"><span data-stu-id="c4515-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-247">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-248">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-249">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-250">Tid, materiale og gebyrer for P1-prosjektet er inkludert på QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="c4515-251">Utgift i P1-prosjektet er inkludert i QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="c4515-252">Ingen overlapping i hva som inkluderes på hver tilbudslinje, og er derfor gyldig.</span><span class="sxs-lookup"><span data-stu-id="c4515-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-253">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-254">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-255">QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-256">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-257">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-258">No</span><span class="sxs-lookup"><span data-stu-id="c4515-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-259">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-260">No</span><span class="sxs-lookup"><span data-stu-id="c4515-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-261">No</span><span class="sxs-lookup"><span data-stu-id="c4515-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-262">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-263">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-264">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-265">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-266">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-267">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-268">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-269">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-270">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-271">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-272">Brudd på regel nr. 2</span><span class="sxs-lookup"><span data-stu-id="c4515-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="c4515-273">Q1 inkluderer tid, materiale, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1</span><span class="sxs-lookup"><span data-stu-id="c4515-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="c4515-274">QL2 inkluderer tid, utgifter og gebyrer for hele prosjektet P1 og derfor overlapper med hva som inkluderes på Q1.</span><span class="sxs-lookup"><span data-stu-id="c4515-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-275">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-276">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-277">QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-278">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-279">Tomt</span><span class="sxs-lookup"><span data-stu-id="c4515-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-280">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-281">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-282">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-283">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-284">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-285">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-286">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-287">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-288">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-289">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-290">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-291">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-292">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-293">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-294">I henhold til regel nr. 3</span><span class="sxs-lookup"><span data-stu-id="c4515-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="c4515-295">Q1 inkluderer tid, materiale, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="c4515-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c4515-296">QL2 inkluderer tid, materialer, utgifter og gebyrer for et delsett med oppgaver på prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="c4515-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c4515-297">Den eneste ekstra valideringen er rundt delsettet av oppgaver på QL1, som skiller seg fra delsettet av oppgaver på QL2, for å sikre at det ikke er noen overlapping.</span><span class="sxs-lookup"><span data-stu-id="c4515-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="c4515-298">Dette gjøres av systemet når oppgaver er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="c4515-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-299">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-300">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-301">QL2</span><span class="sxs-lookup"><span data-stu-id="c4515-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-302">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-303">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="c4515-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-304">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-305">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-306">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-307">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-308">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-309">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-310">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-311">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-312">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="c4515-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-313">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-314">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-315">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-316">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-317">Gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-318">I henhold til regel nr. 5, er Q1 og Q2 to tilbud på samme salgsmulighet, slik at begge kan estimeres for de samme komponentene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="c4515-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-319">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-320">2. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-321">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-322">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-323">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="c4515-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-324">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-325">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-326">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-327">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-328">O1</span><span class="sxs-lookup"><span data-stu-id="c4515-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-329">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-330">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-331">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-332">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="c4515-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-333">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-334">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-335">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-336">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-337">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="c4515-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c4515-338">I henhold til regel nr. 4, er Q1 og Q2 to tilbud på forskjellige salgsmuligheter, slik at de ikke kan estimeres for de samme komponentene i det samme prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c4515-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="c4515-339">O2</span><span class="sxs-lookup"><span data-stu-id="c4515-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="c4515-340">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="c4515-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="c4515-341">QL1</span><span class="sxs-lookup"><span data-stu-id="c4515-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-342">P1</span><span class="sxs-lookup"><span data-stu-id="c4515-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="c4515-343">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="c4515-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="c4515-344">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="c4515-345">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="c4515-346">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c4515-347">Ja</span><span class="sxs-lookup"><span data-stu-id="c4515-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
