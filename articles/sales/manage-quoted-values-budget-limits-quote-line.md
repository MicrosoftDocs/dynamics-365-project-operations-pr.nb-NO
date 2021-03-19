---
title: Oversikt over prosjektbaserte tilbudslinjer
description: Dette emnet gir informasjon om hvordan du bruker prosjektbaserte tilbudslinjer for prosjektarbeid.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e61a9fbf357123884397b930662d11f22bfdeaa0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277800"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="881a7-103">Oversikt over prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="881a7-103">Project-based quote lines overview</span></span>

<span data-ttu-id="881a7-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="881a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="881a7-105">Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement.</span><span class="sxs-lookup"><span data-stu-id="881a7-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="881a7-106">Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="881a7-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="881a7-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="881a7-107">Billing Method</span></span>
- <span data-ttu-id="881a7-108">Prosjekttilordning</span><span class="sxs-lookup"><span data-stu-id="881a7-108">Project Mapping</span></span>
- <span data-ttu-id="881a7-109">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="881a7-109">Included Transaction classes</span></span>
- <span data-ttu-id="881a7-110">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="881a7-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="881a7-111">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="881a7-111">Chargeability setup</span></span>
- <span data-ttu-id="881a7-112">Estimering ved hjelp av tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="881a7-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="881a7-113">Kunder for tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="881a7-113">Quote line Customers</span></span>

<span data-ttu-id="881a7-114">Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="881a7-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="881a7-115">Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="881a7-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="881a7-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="881a7-116">**Field**</span></span> | <span data-ttu-id="881a7-117">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="881a7-117">**Description**</span></span> | <span data-ttu-id="881a7-118">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="881a7-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="881a7-119">Navn</span><span class="sxs-lookup"><span data-stu-id="881a7-119">Name</span></span> | <span data-ttu-id="881a7-120">Navnet på tilbudslinjen som skal hjelpe deg med å identifisere den diskrete komponenten i tilbudet som beregnes.</span><span class="sxs-lookup"><span data-stu-id="881a7-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="881a7-121">Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="881a7-122">Billing Method</span></span> | <span data-ttu-id="881a7-123">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="881a7-124">Dette feltet omfatter de to hovedkontraktsmodellene som støttes av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="881a7-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="881a7-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="881a7-125">- Fixed price</span></span></br><span data-ttu-id="881a7-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="881a7-126">- Time and material.</span></span>| <span data-ttu-id="881a7-127">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-128">Project</span><span class="sxs-lookup"><span data-stu-id="881a7-128">Project</span></span> | <span data-ttu-id="881a7-129">Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="881a7-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="881a7-130">Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="881a7-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="881a7-131">Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj.</span><span class="sxs-lookup"><span data-stu-id="881a7-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="881a7-132">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-133">Inkluder tid</span><span class="sxs-lookup"><span data-stu-id="881a7-133">Include Time</span></span> | <span data-ttu-id="881a7-134">Et **Ja**/**Nei**-flagg angir om tidstransaksjoner eller lønnskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-135">Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-136">Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="881a7-137">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-138">Inkluder utgift</span><span class="sxs-lookup"><span data-stu-id="881a7-138">Include Expense</span></span> | <span data-ttu-id="881a7-139">Et **Ja**/**Nei**-flagg angir om utgiftskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-140">Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-141">Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="881a7-142">Denne feltverdien kopieres over til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-143">Inkluder gebyr</span><span class="sxs-lookup"><span data-stu-id="881a7-143">Include Fee</span></span> | <span data-ttu-id="881a7-144">Et **Ja**/**Nei**-flagg angir om gebyrer på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-145">Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="881a7-146">Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="881a7-147">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-148">Tilbudsbeløp</span><span class="sxs-lookup"><span data-stu-id="881a7-148">Quoted Amount</span></span> | <span data-ttu-id="881a7-149">Dette er beløpet som skal tilbys til kunden for alt arbeidet som er prognostisert på denne prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="881a7-150">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="881a7-151">Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="881a7-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="881a7-152">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-153">Beregnet mva</span><span class="sxs-lookup"><span data-stu-id="881a7-153">Estimated Tax</span></span> | <span data-ttu-id="881a7-154">Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="881a7-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="881a7-155">Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="881a7-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="881a7-156">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-157">Tilbudsbeløp etter mva</span><span class="sxs-lookup"><span data-stu-id="881a7-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="881a7-158">Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="881a7-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="881a7-159">Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*.</span><span class="sxs-lookup"><span data-stu-id="881a7-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="881a7-160">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-161">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="881a7-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="881a7-162">Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="881a7-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="881a7-163">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="881a7-164">Kundebudsjett</span><span class="sxs-lookup"><span data-stu-id="881a7-164">Customer Budget</span></span> | <span data-ttu-id="881a7-165">Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="881a7-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="881a7-166">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="881a7-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="881a7-167">Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="881a7-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="881a7-168">**Regel 1**: En bestemt transaksjonsklasse på det valgte prosjektet kan bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="881a7-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="881a7-169">**Regel 2**: Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="881a7-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="881a7-170">**Regel 3**: Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="881a7-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="881a7-171">
                    <strong>Salgsmulighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="881a7-172">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="881a7-173">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="881a7-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="881a7-175">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="881a7-176">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="881a7-177">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="881a7-178">
                    <strong>gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="881a7-179">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="881a7-180">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="881a7-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-181">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-182">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-183">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-184">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-185">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-186">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-187">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-188">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-189">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="881a7-189">Violation of Rule #1.</span></span> <span data-ttu-id="881a7-190">Klokkeslett, utgift og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="881a7-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-191">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-192">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-193">QL2</span><span class="sxs-lookup"><span data-stu-id="881a7-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-194">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-195">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-196">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-197">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-197">Yes</span></span> </p>
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
<span data-ttu-id="881a7-198">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-199">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-200">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-201">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-202">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-203">No</span><span class="sxs-lookup"><span data-stu-id="881a7-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-204">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-205">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-206">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="881a7-206">Violation of Rule #1.</span></span> <span data-ttu-id="881a7-207">Klokkeslett og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="881a7-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-208">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-209">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-210">QL2</span><span class="sxs-lookup"><span data-stu-id="881a7-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-211">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-212">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-213">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-214">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-214">Yes</span></span> </p>
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
<span data-ttu-id="881a7-215">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-216">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-217">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-218">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-219">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-220">No</span><span class="sxs-lookup"><span data-stu-id="881a7-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-221">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-222">Gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="881a7-223">Tid og avgifter i P1-prosjektet er inkludert i QL1.</span><span class="sxs-lookup"><span data-stu-id="881a7-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="881a7-224">Utgift i P1-prosjektet er inkludert i QL2.</span><span class="sxs-lookup"><span data-stu-id="881a7-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="881a7-225">Det er ingen overlapping i hva som blir inkludert på hver tilbudslinje, så den er gyldig.</span><span class="sxs-lookup"><span data-stu-id="881a7-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-226">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-227">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-228">QL2</span><span class="sxs-lookup"><span data-stu-id="881a7-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-229">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-230">No</span><span class="sxs-lookup"><span data-stu-id="881a7-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-231">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-232">No</span><span class="sxs-lookup"><span data-stu-id="881a7-232">No</span></span> </p>
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
<span data-ttu-id="881a7-233">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-234">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-235">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-236">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-237">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-238">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-239">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-240">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-241">Brudd på regel nr. 1 ovenfor</span><span class="sxs-lookup"><span data-stu-id="881a7-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="881a7-242">Q1 inkluderer tid, utgifter og avgifter for hele prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="881a7-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="881a7-243">QL2 inkluderer tid, utgifter og gebyrer for hele prosjekt P1 og overlapper med det som er inkludert i Q1.</span><span class="sxs-lookup"><span data-stu-id="881a7-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-244">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-245">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-246">QL2</span><span class="sxs-lookup"><span data-stu-id="881a7-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-247">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-248">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-249">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-250">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-250">Yes</span></span> </p>
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
<span data-ttu-id="881a7-251">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-252">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-253">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-254">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-255">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-256">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-257">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="881a7-258">Gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-259">Basert på regel nr. 2 er Q1 og Q2 to tilbud på samme salgsmulighet, slik at de kan beregne de samme komponentene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="881a7-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-260">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-261">2. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="881a7-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-263">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-264">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-265">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-266">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-266">Yes</span></span> </p>
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
<span data-ttu-id="881a7-267">O1</span><span class="sxs-lookup"><span data-stu-id="881a7-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-268">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-269">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-270">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-271">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-272">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-273">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="881a7-274">Gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="881a7-275">Basert på regel nr. 3 er Q1 og Q2 to tilbud for ulike salgsmuligheter, slik at de ikke kan beregne de samme komponentene for det samme prosjektet.</span><span class="sxs-lookup"><span data-stu-id="881a7-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="881a7-276">O2</span><span class="sxs-lookup"><span data-stu-id="881a7-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="881a7-277">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="881a7-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-278">QL1</span><span class="sxs-lookup"><span data-stu-id="881a7-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-279">P1</span><span class="sxs-lookup"><span data-stu-id="881a7-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-280">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="881a7-281">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="881a7-282">Ja</span><span class="sxs-lookup"><span data-stu-id="881a7-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="881a7-283">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="881a7-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]