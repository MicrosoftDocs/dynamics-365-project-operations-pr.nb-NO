---
title: Prosjektbaserte tilbudslinjer
description: Dette emnet gir informasjon om hvordan du bruker prosjektbaserte tilbudslinjer for prosjektarbeid.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081487"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="62e1e-103">Prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="62e1e-103">Project-based quote lines</span></span>

<span data-ttu-id="62e1e-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="62e1e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62e1e-105">Prosjektbaserte tilbudslinjer er utformet for å bidra til å estimere prosjektarbeidet på et engasjement.</span><span class="sxs-lookup"><span data-stu-id="62e1e-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="62e1e-106">Strukturen i en prosjektbasert tilbudslinje utvides for prosjektestimater med følgende konsepter:</span><span class="sxs-lookup"><span data-stu-id="62e1e-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="62e1e-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="62e1e-107">Billing Method</span></span>
- <span data-ttu-id="62e1e-108">Prosjekttilordning</span><span class="sxs-lookup"><span data-stu-id="62e1e-108">Project Mapping</span></span>
- <span data-ttu-id="62e1e-109">Inkluderte transaksjonsklasser</span><span class="sxs-lookup"><span data-stu-id="62e1e-109">Included Transaction classes</span></span>
- <span data-ttu-id="62e1e-110">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="62e1e-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="62e1e-111">Belastbarhets-oppsett</span><span class="sxs-lookup"><span data-stu-id="62e1e-111">Chargeability setup</span></span>
- <span data-ttu-id="62e1e-112">Estimering ved hjelp av tilbudslinjedetaljer</span><span class="sxs-lookup"><span data-stu-id="62e1e-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="62e1e-113">Kunder for tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="62e1e-113">Quote line Customers</span></span>

<span data-ttu-id="62e1e-114">Tabellen nedenfor inneholder informasjon om feltene i kategorien **Generelt** på prosjektbaserte tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="62e1e-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="62e1e-115">Disse feltene bidrar til å definere grunnlaget for en detaljert grunnberegning for prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="62e1e-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="62e1e-116">**Felt**</span><span class="sxs-lookup"><span data-stu-id="62e1e-116">**Field**</span></span> | <span data-ttu-id="62e1e-117">**Relevans, formål og veiledning**</span><span class="sxs-lookup"><span data-stu-id="62e1e-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="62e1e-118">**Nedstrøms påvirkning**</span><span class="sxs-lookup"><span data-stu-id="62e1e-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="62e1e-119">Navn</span><span class="sxs-lookup"><span data-stu-id="62e1e-119">Name</span></span> | <span data-ttu-id="62e1e-120">Navnet på tilbudslinjen som skal hjelpe deg med å identifisere den diskrete komponenten i tilbudet som beregnes.</span><span class="sxs-lookup"><span data-stu-id="62e1e-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="62e1e-121">Kopiert til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-122">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="62e1e-122">Billing Method</span></span> | <span data-ttu-id="62e1e-123">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra det tilsvarende feltet på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="62e1e-124">Dette feltet inneholder de to hovedkontraktmodellene som støttes av Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="62e1e-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="62e1e-125">- Fast pris</span><span class="sxs-lookup"><span data-stu-id="62e1e-125">- Fixed price</span></span></br><span data-ttu-id="62e1e-126">- Tid og materiale.</span><span class="sxs-lookup"><span data-stu-id="62e1e-126">- Time and material.</span></span>| <span data-ttu-id="62e1e-127">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-128">Project</span><span class="sxs-lookup"><span data-stu-id="62e1e-128">Project</span></span> | <span data-ttu-id="62e1e-129">Bruk dette valgfrie feltet til å identifisere prosjektet som skal brukes til å levere arbeidet med dette engasjementet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="62e1e-130">Når et prosjekt tilordnes til en tilbudslinje, hjelper det med å definere belastbare oppgaver og også med å hente inn et prosjektbasert estimat til tilbudslinjen som tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="62e1e-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="62e1e-131">Når et prosjekt ikke er tilordnet til en prosjektbasert tilbudslinje, bør estimatet opprettes manuelt ved å opprette hver tilbudslinjedetalj.</span><span class="sxs-lookup"><span data-stu-id="62e1e-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="62e1e-132">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-133">Inkluder tid</span><span class="sxs-lookup"><span data-stu-id="62e1e-133">Include Time</span></span> | <span data-ttu-id="62e1e-134">Et **Ja**/**Nei** -flagg angir om tidstransaksjoner eller lønnskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-135">Verdien **Nei** angir at tidstransaksjoner eller lønnskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-136">Verdien **Ja** angir at tidstransaksjoner eller lønnskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62e1e-137">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-138">Inkluder utgift</span><span class="sxs-lookup"><span data-stu-id="62e1e-138">Include Expense</span></span> | <span data-ttu-id="62e1e-139">Et **Ja**/**Nei** -flagg angir om utgiftskostnader på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-140">Verdien **Nei** angir at utgiftskostnader ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-141">Verdien **Ja** angir at utgiftskostnader inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62e1e-142">Denne feltverdien kopieres over til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-143">Inkluder gebyr</span><span class="sxs-lookup"><span data-stu-id="62e1e-143">Include Fee</span></span> | <span data-ttu-id="62e1e-144">Et **Ja**/**Nei** -flagg angir om gebyrer på det valgte prosjektet vil bli inkludert i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-145">Verdien **Nei** angir at gebyrer ikke inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="62e1e-146">Verdien **Ja** angir at gebyrer inkluderes i estimatet på denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="62e1e-147">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-148">Tilbudsbeløp</span><span class="sxs-lookup"><span data-stu-id="62e1e-148">Quoted Amount</span></span> | <span data-ttu-id="62e1e-149">Dette er beløpet som skal tilbys til kunden for alt arbeidet som er prognostisert på denne prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="62e1e-150">På et tilbud som er opprettet fra en salgsmulighet, kopieres denne verdien fra feltet **Kundebudsjett** på salgsmulighetslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="62e1e-151">Når den prosjektbaserte tilbudslinjen har linjedetaljer, er dette feltet låst for redigering og summeres fra beløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="62e1e-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="62e1e-152">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-153">Beregnet mva</span><span class="sxs-lookup"><span data-stu-id="62e1e-153">Estimated Tax</span></span> | <span data-ttu-id="62e1e-154">Dette er et redigerbart felt for brukeren å legge til det estimerte mva-beløpet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="62e1e-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="62e1e-155">Når en prosjektbasert tilbudslinje har linjedetaljer, er dette feltet låst for redigering og summeres fra avgiftsbeløpet i tilbudslinjedetaljene.</span><span class="sxs-lookup"><span data-stu-id="62e1e-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="62e1e-156">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-157">Tilbudsbeløp etter mva</span><span class="sxs-lookup"><span data-stu-id="62e1e-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="62e1e-158">Dette feltet er tilbudslinjebeløpet etter mva og er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="62e1e-159">Beløpet i dette feltet beregnes som *Oppgitt beløp + mva*.</span><span class="sxs-lookup"><span data-stu-id="62e1e-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="62e1e-160">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-161">Må ikke overskrides-grense</span><span class="sxs-lookup"><span data-stu-id="62e1e-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="62e1e-162">Dette feltet kan redigeres og er bare tilgjengelig på prosjektbaserte tilbudslinjer som har faktureringsmetoden **Tid og materialer**.</span><span class="sxs-lookup"><span data-stu-id="62e1e-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="62e1e-163">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="62e1e-164">Kundebudsjett</span><span class="sxs-lookup"><span data-stu-id="62e1e-164">Customer Budget</span></span> | <span data-ttu-id="62e1e-165">Feltet kan redigeres, og det kopieres fra det tilsvarende feltet på salgsmulighetslinjen hvis tilbudet ble opprettet fra en salgsmulighet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="62e1e-166">Denne feltverdien kopieres til prosjektkontraktlinjen som opprettes fra denne tilbudslinjen når tilbudet er vunnet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="62e1e-167">Valideringsregler for felt i kategorien Generelt på prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="62e1e-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="62e1e-168">**Regel 1** : En bestemt transaksjonsklasse på det valgte prosjektet kan bare inkluderes på én prosjektbasert tilbudslinje i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="62e1e-168">**Rule 1** : A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="62e1e-169">**Regel 2** : Hvis en salgsmulighet har flere tilbud, kan det finnes tilbudslinjer fra forskjellige tilbud som alle refererer til samme prosjekt og inkluderer samme transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="62e1e-169">**Rule 2** : If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="62e1e-170">**Regel 3** : Hvis tilbudene ikke tilhører samme salgsmulighet, kan de ikke inneholde samme prosjekt- og transaksjonsklasse.</span><span class="sxs-lookup"><span data-stu-id="62e1e-170">**Rule 3** : If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="62e1e-171">
                    <strong>Salgsmulighet</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="62e1e-172">
                    <strong>Tilbud</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62e1e-173">
                    <strong>Tilbudslinje</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62e1e-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="62e1e-175">
                    <strong>Inkluder tid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="62e1e-176">
                    <strong>Inkluder utgift</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="62e1e-177">
                    <strong>Inkluder</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="62e1e-178">
                    <strong>gebyr</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="62e1e-179">
                    <strong>Gyldig / ikke gyldig</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="62e1e-180">
                    <strong>Årsak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="62e1e-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-181">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-182">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-183">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-184">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-185">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-186">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-187">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-188">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-189">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="62e1e-189">Violation of Rule #1.</span></span> <span data-ttu-id="62e1e-190">Klokkeslett, utgift og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="62e1e-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-191">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-192">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-193">QL2</span><span class="sxs-lookup"><span data-stu-id="62e1e-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-194">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-195">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-196">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-197">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-197">Yes</span></span> </p>
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
<span data-ttu-id="62e1e-198">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-199">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-200">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-201">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-202">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-203">No</span><span class="sxs-lookup"><span data-stu-id="62e1e-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-204">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-205">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-206">Brudd på regel nr. 1.</span><span class="sxs-lookup"><span data-stu-id="62e1e-206">Violation of Rule #1.</span></span> <span data-ttu-id="62e1e-207">Klokkeslett og avgifter i P1-prosjektet er inkludert på begge tilbudslinjene, QL1 og QL2.</span><span class="sxs-lookup"><span data-stu-id="62e1e-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-208">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-209">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-210">QL2</span><span class="sxs-lookup"><span data-stu-id="62e1e-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-211">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-212">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-213">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-214">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-214">Yes</span></span> </p>
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
<span data-ttu-id="62e1e-215">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-216">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-217">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-218">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-219">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-220">No</span><span class="sxs-lookup"><span data-stu-id="62e1e-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-221">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-222">Gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="62e1e-223">Tid og avgifter i P1-prosjektet er inkludert i QL1.</span><span class="sxs-lookup"><span data-stu-id="62e1e-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="62e1e-224">Utgift i P1-prosjektet er inkludert i QL2.</span><span class="sxs-lookup"><span data-stu-id="62e1e-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="62e1e-225">Det er ingen overlapping i hva som blir inkludert på hver tilbudslinje, så den er gyldig.</span><span class="sxs-lookup"><span data-stu-id="62e1e-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-226">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-227">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-228">QL2</span><span class="sxs-lookup"><span data-stu-id="62e1e-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-229">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-230">No</span><span class="sxs-lookup"><span data-stu-id="62e1e-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-231">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-232">No</span><span class="sxs-lookup"><span data-stu-id="62e1e-232">No</span></span> </p>
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
<span data-ttu-id="62e1e-233">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-234">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-235">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-236">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-237">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-238">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-239">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-240">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-241">Brudd på regel nr. 1 ovenfor</span><span class="sxs-lookup"><span data-stu-id="62e1e-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="62e1e-242">Q1 inkluderer tid, utgifter og avgifter for hele prosjekt P1.</span><span class="sxs-lookup"><span data-stu-id="62e1e-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="62e1e-243">QL2 inkluderer tid, utgifter og gebyrer for hele prosjekt P1 og overlapper med det som er inkludert i Q1.</span><span class="sxs-lookup"><span data-stu-id="62e1e-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-244">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-245">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-246">QL2</span><span class="sxs-lookup"><span data-stu-id="62e1e-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-247">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-248">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-249">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-250">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-250">Yes</span></span> </p>
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
<span data-ttu-id="62e1e-251">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-252">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-253">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-254">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-255">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-256">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-257">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62e1e-258">Gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-259">Basert på regel nr. 2 er Q1 og Q2 to tilbud på samme salgsmulighet, slik at de kan beregne de samme komponentene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="62e1e-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-260">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-261">2. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-262">QL1 på Q2</span><span class="sxs-lookup"><span data-stu-id="62e1e-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-263">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-264">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-265">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-266">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-266">Yes</span></span> </p>
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
<span data-ttu-id="62e1e-267">O1</span><span class="sxs-lookup"><span data-stu-id="62e1e-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-268">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-269">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-270">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-271">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-272">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-273">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62e1e-274">Gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="62e1e-275">Basert på regel nr. 3 er Q1 og Q2 to tilbud for ulike salgsmuligheter, slik at de ikke kan beregne de samme komponentene for det samme prosjektet.</span><span class="sxs-lookup"><span data-stu-id="62e1e-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="62e1e-276">O2</span><span class="sxs-lookup"><span data-stu-id="62e1e-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="62e1e-277">1. kvartal</span><span class="sxs-lookup"><span data-stu-id="62e1e-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-278">QL1</span><span class="sxs-lookup"><span data-stu-id="62e1e-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-279">P1</span><span class="sxs-lookup"><span data-stu-id="62e1e-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-280">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="62e1e-281">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="62e1e-282">Ja</span><span class="sxs-lookup"><span data-stu-id="62e1e-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="62e1e-283">Ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="62e1e-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

