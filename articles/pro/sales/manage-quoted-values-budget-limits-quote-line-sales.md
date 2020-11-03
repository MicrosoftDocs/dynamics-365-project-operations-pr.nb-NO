---
title: Prosjektbaserte tilbudslinjer (Pro)
description: Dette emnet gir informasjon om hvordan du bruker prosjektbaserte tilbudslinjer for prosjektarbeid. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081550"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="d08f7-104">Prosjektbaserte tilbudslinjer (Pro)</span><span class="sxs-lookup"><span data-stu-id="d08f7-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="d08f7-105">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d08f7-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d08f7-106">Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement.</span><span class="sxs-lookup"><span data-stu-id="d08f7-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d08f7-107">Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="d08f7-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d08f7-108">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="d08f7-108">Billing Method</span></span>
- <span data-ttu-id="d08f7-109">Prosjekt- og oppgavetilordning</span><span class="sxs-lookup"><span data-stu-id="d08f7-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d08f7-110">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="d08f7-110">Included Transaction classes</span></span>
- <span data-ttu-id="d08f7-111">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="d08f7-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d08f7-112">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="d08f7-112">Chargeability setup</span></span>
- <span data-ttu-id="d08f7-113">Estimering ved hjelp av tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="d08f7-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d08f7-114">Kunder for tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="d08f7-114">Quote line Customers</span></span>

<span data-ttu-id="d08f7-115">Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="d08f7-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d08f7-116">Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="d08f7-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d08f7-117">**Felt**</span><span class="sxs-lookup"><span data-stu-id="d08f7-117">**Field**</span></span> | <span data-ttu-id="d08f7-118">**Relevans, formål og veiledning**</span><span class="sxs-lookup"><span data-stu-id="d08f7-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="d08f7-119">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="d08f7-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d08f7-120">Navn</span><span class="sxs-lookup"><span data-stu-id="d08f7-120">Name</span></span> | <span data-ttu-id="d08f7-121">Navnet på tilbudslinjen som skal hjelpe deg med å identifisere den diskrete komponenten i tilbudet som beregnes.</span><span class="sxs-lookup"><span data-stu-id="d08f7-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d08f7-122">Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-123">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="d08f7-123">Billing Method</span></span> | <span data-ttu-id="d08f7-124">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d08f7-125">Dette feltet inneholder de to hovedkontraktmodellene som støttes av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d08f7-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d08f7-126">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="d08f7-126">- Fixed price</span></span></br><span data-ttu-id="d08f7-127">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="d08f7-127">- Time and material.</span></span>| <span data-ttu-id="d08f7-128">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-129">Project</span><span class="sxs-lookup"><span data-stu-id="d08f7-129">Project</span></span> | <span data-ttu-id="d08f7-130">Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d08f7-131">Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="d08f7-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d08f7-132">Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj.</span><span class="sxs-lookup"><span data-stu-id="d08f7-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d08f7-133">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d08f7-134">Inkluderte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-134">Included Tasks</span></span> | <span data-ttu-id="d08f7-135">Angir om denne tilbudslinjen brukes til alle eller noen av prosjektoppgavene for det valgte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d08f7-136">Dette feltet har følgende mulige verdier:</span><span class="sxs-lookup"><span data-stu-id="d08f7-136">This field has the following possible values:</span></span></br><span data-ttu-id="d08f7-137">- Alle prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-137">- All project tasks</span></span></br><span data-ttu-id="d08f7-138">- Bare valgte prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-138">- Selected project tasks only</span></span></br><span data-ttu-id="d08f7-139">En tom verdi i dette feltet tilsvarer alternativet **Alle prosjektoppgaver**.</span><span class="sxs-lookup"><span data-stu-id="d08f7-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d08f7-140">Når **Bare valgte prosjektoppgaver** er valgt på prosjektsiden, kan du bruke kategorien **Faktureringsoppsett for oppgave** til å velge bestemte oppgaver for å knytte dem til denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d08f7-141">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-142">Inkluder tid</span><span class="sxs-lookup"><span data-stu-id="d08f7-142">Include Time</span></span> | <span data-ttu-id="d08f7-143">Et **Ja**/**Nei** -flagg angir om tidstransaksjoner eller lønnskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-144">Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-145">Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d08f7-146">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-147">Inkluder utgift</span><span class="sxs-lookup"><span data-stu-id="d08f7-147">Include Expense</span></span> | <span data-ttu-id="d08f7-148">Et **Ja**/**Nei** -flagg angir om utgiftskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-149">Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-150">Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d08f7-151">Denne feltverdien kopieres over til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-152">Inkluder gebyr</span><span class="sxs-lookup"><span data-stu-id="d08f7-152">Include Fee</span></span> | <span data-ttu-id="d08f7-153">Et **Ja**/**Nei** -flagg angir om gebyrer på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-154">Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d08f7-155">Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d08f7-156">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-157">Tilbudsbeløp</span><span class="sxs-lookup"><span data-stu-id="d08f7-157">Quoted Amount</span></span> | <span data-ttu-id="d08f7-158">Dette er beløpet som skal tilbys til kunden for alt arbeidet som er prognostisert på denne prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d08f7-159">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d08f7-160">Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="d08f7-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d08f7-161">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-162">Beregnet mva</span><span class="sxs-lookup"><span data-stu-id="d08f7-162">Estimated Tax</span></span> | <span data-ttu-id="d08f7-163">Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d08f7-164">Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="d08f7-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d08f7-165">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-166">Tilbudsbeløp etter mva</span><span class="sxs-lookup"><span data-stu-id="d08f7-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d08f7-167">Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d08f7-168">Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*.</span><span class="sxs-lookup"><span data-stu-id="d08f7-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d08f7-169">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-170">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="d08f7-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d08f7-171">Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="d08f7-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d08f7-172">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d08f7-173">Kundebudsjett</span><span class="sxs-lookup"><span data-stu-id="d08f7-173">Customer Budget</span></span> | <span data-ttu-id="d08f7-174">Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d08f7-175">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d08f7-176">Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="d08f7-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d08f7-177">**Regel 1** : Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver** , inkluderes et prosjekt på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="d08f7-177">**Rule 1** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project is included in the quote line.</span></span>

<span data-ttu-id="d08f7-178">**Regel 2** : Hvis feltet **Inkluderte oppgaver** er tomt, eller hvis det er satt til **Alle prosjektoppgaver** , kan et prosjekt og en bestemt transaksjonsklasse bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="d08f7-178">**Rule 2** : If the **Included Tasks** field is blank, or if it is set to **All project tasks** , a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d08f7-179">**Regel 3** : Hvis feltet **Inkluderte oppgaver** er satt til **Bare valgte prosjektoppgaver** , kan et prosjekt og en bestemt transaksjonsklasse inkluderes på flere prosjektbaserte tilbudslinjer i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="d08f7-179">**Rule 3** : If the **Included Tasks** field is set to **Selected project tasks only** , a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d08f7-180">**Regel 4** : Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="d08f7-180">**Rule 4** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d08f7-181">**Regel 5** : Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="d08f7-181">**Rule 5** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d08f7-182">
                    <strong>Salgsmulighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d08f7-183">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d08f7-184">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d08f7-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d08f7-186">
                    <strong>Inkluderte oppgaver</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d08f7-187">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d08f7-188">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d08f7-189">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d08f7-190">
                    <strong>Gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d08f7-191">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d08f7-192">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d08f7-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-193">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-194">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-196">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-197">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-198">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-199">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-200">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-201">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-202">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-202">Violation of Rule #2.</span></span> <span data-ttu-id="d08f7-203">Klokkeslett, utgift og avgifter i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-204">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-205">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d08f7-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-207">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-208">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-209">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-210">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-211">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-212">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-213">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-215">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-216">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-217">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-218">No</span><span class="sxs-lookup"><span data-stu-id="d08f7-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-219">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-220">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-221">Brudd på regel nr. 2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-221">Violation of Rule #2.</span></span> <span data-ttu-id="d08f7-222">Klokkeslett og avgifter i P1-prosjektet er inkludert på tilbudslinjene QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-223">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-224">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d08f7-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-226">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-227">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-228">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-229">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-230">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-231">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-232">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-234">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-235">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-236">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-237">No</span><span class="sxs-lookup"><span data-stu-id="d08f7-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-238">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-239">Gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d08f7-240">Tid og avgifter i P1-prosjektet er inkludert i QL1.</span><span class="sxs-lookup"><span data-stu-id="d08f7-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d08f7-241">Utgift i P1-prosjektet er inkludert i QL2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d08f7-242">Det er ingen overlapping i hva som blir inkludert på hver tilbudslinje, og hva som er gyldig.</span><span class="sxs-lookup"><span data-stu-id="d08f7-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-243">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-244">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d08f7-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-246">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-247">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-248">No</span><span class="sxs-lookup"><span data-stu-id="d08f7-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-249">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-250">No</span><span class="sxs-lookup"><span data-stu-id="d08f7-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-251">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-252">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-254">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-255">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-256">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-257">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-258">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-259">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-260">Brudd på regel nr. 2 ovenfor</span><span class="sxs-lookup"><span data-stu-id="d08f7-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d08f7-261">Q1 inkluderer tid, utgifter og gebyrer på et delsett med oppgaver i prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="d08f7-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d08f7-262">QL2 inkluderer tid, utgifter og gebyrer for hele prosjekt P1 og overlapper med det som er inkludert i Q1.</span><span class="sxs-lookup"><span data-stu-id="d08f7-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-263">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-264">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d08f7-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-266">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-267">Tomt</span><span class="sxs-lookup"><span data-stu-id="d08f7-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-268">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-269">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-270">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-271">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-272">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-274">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-275">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-276">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-277">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-278">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-279">Gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-280">Per regel nummer 3 over,</span><span class="sxs-lookup"><span data-stu-id="d08f7-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d08f7-281">Q1 inkluderer tid, utgifter og gebyrer på et delsett med oppgaver i prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="d08f7-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d08f7-282">QL2 inkluderer tid, utgifter og gebyrer for et delsett med oppgaver i prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="d08f7-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d08f7-283">Den eneste ekstra valideringen er rundt delsettet med oppgaver på QL1 som er forskjellige fra delsettet med oppgaver på QL2.</span><span class="sxs-lookup"><span data-stu-id="d08f7-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d08f7-284">Dette sikrer at det ikke er noen overlappinger.</span><span class="sxs-lookup"><span data-stu-id="d08f7-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d08f7-285">Dette gjøres av systemet når oppgaver er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-286">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-287">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d08f7-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-289">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-290">Bare valgte oppgaver</span><span class="sxs-lookup"><span data-stu-id="d08f7-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-291">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-292">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-293">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-294">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-295">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-297">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-298">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="d08f7-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-299">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-300">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-301">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d08f7-302">Gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-303">Basert på regel nr. 5 er Q1 og Q2 to tilbud på samme salgsmulighet, slik at de kan beregne de samme komponentene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d08f7-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-304">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-305">2. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-307">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-308">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="d08f7-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-309">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-310">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-311">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-312">O1</span><span class="sxs-lookup"><span data-stu-id="d08f7-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-313">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-315">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-316">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="d08f7-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-317">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-318">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-319">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d08f7-320">Gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d08f7-321">Basert på regel nr. 4 er Q1 og Q2 to tilbud for ulike salgsmuligheter, slik at de ikke kan beregne de samme komponentene for det samme prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d08f7-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d08f7-322">O2</span><span class="sxs-lookup"><span data-stu-id="d08f7-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d08f7-323">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="d08f7-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d08f7-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-325">P1</span><span class="sxs-lookup"><span data-stu-id="d08f7-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d08f7-326">Alle prosjektoppgaver eller tom</span><span class="sxs-lookup"><span data-stu-id="d08f7-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-327">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d08f7-328">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d08f7-329">Ja</span><span class="sxs-lookup"><span data-stu-id="d08f7-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d08f7-330">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="d08f7-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

