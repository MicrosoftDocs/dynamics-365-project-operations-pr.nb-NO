---
title: Oversikt over prosjekttilbudslinjer
description: Dette emnet inneholder informasjon om bruk av prosjekttilbudslinjer for prosjektarbeid.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996308"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="031ae-103">Oversikt over prosjekttilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="031ae-103">Project quote lines overview</span></span>

<span data-ttu-id="031ae-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="031ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="031ae-105">Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement.</span><span class="sxs-lookup"><span data-stu-id="031ae-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="031ae-106">Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="031ae-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="031ae-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="031ae-107">Billing Method</span></span>
- <span data-ttu-id="031ae-108">Prosjekttilordning</span><span class="sxs-lookup"><span data-stu-id="031ae-108">Project Mapping</span></span>
- <span data-ttu-id="031ae-109">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="031ae-109">Included Transaction classes</span></span>
- <span data-ttu-id="031ae-110">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="031ae-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="031ae-111">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="031ae-111">Chargeability setup</span></span>
- <span data-ttu-id="031ae-112">Estimering ved hjelp av tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="031ae-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="031ae-113">Kunder for tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="031ae-113">Quote line Customers</span></span>

<span data-ttu-id="031ae-114">Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="031ae-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="031ae-115">Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="031ae-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="031ae-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="031ae-116">**Field**</span></span> | <span data-ttu-id="031ae-117">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="031ae-117">**Description**</span></span> | <span data-ttu-id="031ae-118">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="031ae-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="031ae-119">Navn</span><span class="sxs-lookup"><span data-stu-id="031ae-119">Name</span></span> | <span data-ttu-id="031ae-120">Navnet på tilbudslinjen som skal hjelpe deg med å identifisere den diskrete komponenten i tilbudet som beregnes.</span><span class="sxs-lookup"><span data-stu-id="031ae-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="031ae-121">Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="031ae-122">Billing Method</span></span> | <span data-ttu-id="031ae-123">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="031ae-124">Dette feltet omfatter de to hovedkontraktsmodellene som støttes av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="031ae-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="031ae-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="031ae-125">- Fixed price</span></span></br><span data-ttu-id="031ae-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="031ae-126">- Time and material.</span></span>| <span data-ttu-id="031ae-127">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-128">Project</span><span class="sxs-lookup"><span data-stu-id="031ae-128">Project</span></span> | <span data-ttu-id="031ae-129">Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="031ae-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="031ae-130">Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="031ae-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="031ae-131">Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj.</span><span class="sxs-lookup"><span data-stu-id="031ae-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="031ae-132">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-133">Inkluder tid</span><span class="sxs-lookup"><span data-stu-id="031ae-133">Include Time</span></span> | <span data-ttu-id="031ae-134">Et **Ja**/**Nei**-flagg angir om tidstransaksjoner eller lønnskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-135">Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-136">Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="031ae-137">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-138">Inkluder utgift</span><span class="sxs-lookup"><span data-stu-id="031ae-138">Include Expense</span></span> | <span data-ttu-id="031ae-139">Et **Ja**/**Nei**-flagg angir om utgiftskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-140">Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-141">Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="031ae-142">Denne feltverdien kopieres over til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-143">Inkluder gebyr</span><span class="sxs-lookup"><span data-stu-id="031ae-143">Include Fee</span></span> | <span data-ttu-id="031ae-144">Et **Ja**/**Nei**-flagg angir om gebyrer på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-145">Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="031ae-146">Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="031ae-147">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-148">Tilbudsbeløp</span><span class="sxs-lookup"><span data-stu-id="031ae-148">Quoted Amount</span></span> | <span data-ttu-id="031ae-149">Dette er beløpet som skal tilbys til kunden for alt arbeidet som er prognostisert på denne prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="031ae-150">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="031ae-151">Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="031ae-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="031ae-152">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-153">Beregnet mva</span><span class="sxs-lookup"><span data-stu-id="031ae-153">Estimated Tax</span></span> | <span data-ttu-id="031ae-154">Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="031ae-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="031ae-155">Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="031ae-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="031ae-156">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-157">Tilbudsbeløp etter mva</span><span class="sxs-lookup"><span data-stu-id="031ae-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="031ae-158">Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="031ae-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="031ae-159">Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*.</span><span class="sxs-lookup"><span data-stu-id="031ae-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="031ae-160">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-161">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="031ae-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="031ae-162">Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="031ae-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="031ae-163">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="031ae-164">Kundebudsjett</span><span class="sxs-lookup"><span data-stu-id="031ae-164">Customer Budget</span></span> | <span data-ttu-id="031ae-165">Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="031ae-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="031ae-166">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="031ae-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="031ae-167">Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="031ae-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="031ae-168">**Regel 1**: En bestemt transaksjonsklasse på det valgte prosjektet kan bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="031ae-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="031ae-169">**Regel 2**: Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="031ae-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="031ae-170">**Regel 3**: Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="031ae-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="031ae-171">
                    <strong>Salgsmulighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="031ae-172">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="031ae-173">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="031ae-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="031ae-175">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="031ae-176">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="031ae-177">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="031ae-178">
                    <strong>gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="031ae-179">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="031ae-180">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="031ae-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-181">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-182">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-183">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-184">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-185">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-186">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-187">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-188">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-189">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="031ae-189">Violation of Rule #1.</span></span> <span data-ttu-id="031ae-190">Klokkeslett, utgift og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="031ae-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-191">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-192">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-193">QL2</span><span class="sxs-lookup"><span data-stu-id="031ae-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-194">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-195">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-196">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-197">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-197">Yes</span></span> </p>
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
<span data-ttu-id="031ae-198">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-199">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-200">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-201">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-202">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-203">No</span><span class="sxs-lookup"><span data-stu-id="031ae-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-204">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-205">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-206">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="031ae-206">Violation of Rule #1.</span></span> <span data-ttu-id="031ae-207">Klokkeslett og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="031ae-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-208">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-209">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-210">QL2</span><span class="sxs-lookup"><span data-stu-id="031ae-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-211">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-212">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-213">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-214">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-214">Yes</span></span> </p>
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
<span data-ttu-id="031ae-215">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-216">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-217">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-218">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-219">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-220">No</span><span class="sxs-lookup"><span data-stu-id="031ae-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-221">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-222">Gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="031ae-223">Tid og avgifter i P1-prosjektet er inkludert i QL1.</span><span class="sxs-lookup"><span data-stu-id="031ae-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="031ae-224">Utgift i P1-prosjektet er inkludert i QL2.</span><span class="sxs-lookup"><span data-stu-id="031ae-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="031ae-225">Det er ingen overlapping i hva som blir inkludert på hver tilbudslinje, så den er gyldig.</span><span class="sxs-lookup"><span data-stu-id="031ae-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-226">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-227">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-228">QL2</span><span class="sxs-lookup"><span data-stu-id="031ae-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-229">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-230">No</span><span class="sxs-lookup"><span data-stu-id="031ae-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-231">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-232">No</span><span class="sxs-lookup"><span data-stu-id="031ae-232">No</span></span> </p>
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
<span data-ttu-id="031ae-233">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-234">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-235">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-236">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-237">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-238">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-239">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-240">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-241">Brudd på regel nr. 1 ovenfor</span><span class="sxs-lookup"><span data-stu-id="031ae-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="031ae-242">Q1 inkluderer tid, utgifter og avgifter for hele prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="031ae-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="031ae-243">QL2 inkluderer tid, utgifter og gebyrer for hele prosjekt P1 og overlapper med det som er inkludert i Q1.</span><span class="sxs-lookup"><span data-stu-id="031ae-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-244">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-245">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-246">QL2</span><span class="sxs-lookup"><span data-stu-id="031ae-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-247">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-248">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-249">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-250">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-250">Yes</span></span> </p>
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
<span data-ttu-id="031ae-251">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-252">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-253">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-254">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-255">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-256">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-257">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="031ae-258">Gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-259">Basert på regel nr. 2 er Q1 og Q2 to tilbud på samme salgsmulighet, slik at de kan beregne de samme komponentene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="031ae-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-260">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-261">2. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="031ae-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-263">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-264">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-265">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-266">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-266">Yes</span></span> </p>
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
<span data-ttu-id="031ae-267">O1</span><span class="sxs-lookup"><span data-stu-id="031ae-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-268">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-269">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-270">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-271">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-272">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-273">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="031ae-274">Gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="031ae-275">Basert på regel nr. 3 er Q1 og Q2 to tilbud for ulike salgsmuligheter, slik at de ikke kan beregne de samme komponentene for det samme prosjektet.</span><span class="sxs-lookup"><span data-stu-id="031ae-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="031ae-276">O2</span><span class="sxs-lookup"><span data-stu-id="031ae-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="031ae-277">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="031ae-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-278">QL1</span><span class="sxs-lookup"><span data-stu-id="031ae-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-279">P1</span><span class="sxs-lookup"><span data-stu-id="031ae-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-280">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="031ae-281">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="031ae-282">Ja</span><span class="sxs-lookup"><span data-stu-id="031ae-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="031ae-283">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="031ae-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
