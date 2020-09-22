---
title: Prosjektkontrakter
description: Dette emnet inneholder eksempler på prosjektkontraktene som du kan opprette for ulike typer prosjekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere prosjektkunder.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754146"
---
# <a name="project-contracts"></a><span data-ttu-id="5199a-103">Prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="5199a-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5199a-104">Denne artikkelen inneholder eksempler på prosjektkontraktene som du kan opprette for ulike typer prosjekter og finansieringskilder, og hvordan du kan administrere kontrakter og fakturere prosjektkunder.</span><span class="sxs-lookup"><span data-stu-id="5199a-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="5199a-105">Prosjekttypen som du oppretter for en prosjektkontrakt, bestemmer metoden som brukes til å fakturere prosjektkunder.</span><span class="sxs-lookup"><span data-stu-id="5199a-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="5199a-106">Du kan endre en prosjektkontrakt og det relaterte prosjektet, men du kan ikke endre prosjekttypen.</span><span class="sxs-lookup"><span data-stu-id="5199a-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="5199a-107">Ved hjelp av en prosjektkontrakt kan du fakturere ett eller flere prosjekter samtidig.</span><span class="sxs-lookup"><span data-stu-id="5199a-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="5199a-108">Prosjektkontrakten bidrar også til å garantere en konsekvent faktureringsprosedyre for hvert delprosjekt i en prosjektstruktur.</span><span class="sxs-lookup"><span data-stu-id="5199a-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="5199a-109">Hvert prosjekt som blir fakturert, må tilknyttes en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="5199a-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="5199a-110">Innstillingene for en prosjektkontrakt gjelder for alle prosjekter og delprosjekter som er tilknyttet prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="5199a-111">En prosjektkontrakt kan angi én eller flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="5199a-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="5199a-112">Derfor kan du dele opp faktureringen mellom flere fond, konfigurere finansieringsgrenser, slik at finansieringskilder ikke blir fakturert mer enn et bestemt beløp og konfigurere finansieringsregler for belastning av utgifter.</span><span class="sxs-lookup"><span data-stu-id="5199a-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="5199a-113">Finansiering for prosjektkontrakter</span><span class="sxs-lookup"><span data-stu-id="5199a-113">Funding for project contracts</span></span>
<span data-ttu-id="5199a-114">Noen prosjektkontrakter spesifiserer at flere parter deler ansvaret for finansiering av prosjektkostnadene.</span><span class="sxs-lookup"><span data-stu-id="5199a-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="5199a-115">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="5199a-115">Here are some examples:</span></span>

-   <span data-ttu-id="5199a-116">En stor kunde som har flere divisjoner ber om at finansiering av et prosjekt deles etter divisjon.</span><span class="sxs-lookup"><span data-stu-id="5199a-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="5199a-117">Firmaet deler kostnadene for et stort prosjekt med en ekstern organisasjon.</span><span class="sxs-lookup"><span data-stu-id="5199a-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="5199a-118">Et veiprosjekt er medfinansiert av to kommuner.</span><span class="sxs-lookup"><span data-stu-id="5199a-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="5199a-119">Et broprosjekt er finansiert av en offentlig bevilgning og en privat bedrift.</span><span class="sxs-lookup"><span data-stu-id="5199a-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="5199a-120">I Dynamics 365 Finance kan du dele opp faktureringen for en enkelt transaksjon eller et helt prosjekt mellom flere kunder, tilskudd eller organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="5199a-121">I prosjekter som har flere innsamlingsverktøy, kalles alle parter som bidrar til finansieringen for et avansert finansieringsprosjekt, finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="5199a-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="5199a-122">Når en kunde, organisasjon eller et tilskudd er definert som en finansieringskilde, kan den/det tilordnes til én eller flere finansieringsregler.</span><span class="sxs-lookup"><span data-stu-id="5199a-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="5199a-123">Finansieringsregler inneholder kriteriene som avgjør hvordan gebyrer tildeles de ulike finansieringskildene for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5199a-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="5199a-124">Fordi lagerførte varer, for eksempel de som vises på innkjøpsrekvisisjoner og bestillinger, ikke kan deles, kan ikke kostnads beløpet deles mellom flere finansieringskilder på distribusjonstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="5199a-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="5199a-125">Derfor forblir finansieringskildeverdien 0 (null) helt til lageravgangen blir postert.</span><span class="sxs-lookup"><span data-stu-id="5199a-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="5199a-126">Når lageravgangen blir postert, blir kostnadsbeløpet fordelt i henhold til reglene for forretningsforbindelsesdistribusjonen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="5199a-127">Her er noen trinn du kan utføre for å gjøre det enklere å dele opp faktureringen blant flere finansieringskilder:</span><span class="sxs-lookup"><span data-stu-id="5199a-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="5199a-128">Angi at alle transaksjoner som er angitt for et prosjekt, bruker samme salgsvaluta som prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="5199a-129">Angi finansieringsgrenser, slik at en finansieringskilde ikke blir fakturert mer enn et bestemt beløp mot et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5199a-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="5199a-130">Konfigurere finansieringsregler og finansieringsgrenser for hver arbeider, vare, kategori, kategorigruppe og transaksjonstype (eller for alle transaksjonstyper).</span><span class="sxs-lookup"><span data-stu-id="5199a-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="5199a-131">Velg valgfrie start- og sluttdatoer for å definere perioden hver finansieringsregel er gyldig.</span><span class="sxs-lookup"><span data-stu-id="5199a-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="5199a-132">Angi prosentandelen som hver finansieringskilde er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="5199a-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="5199a-133">Angi hvilken finansieringskilde som er ansvarlig for avrundingsdifferanser som er forårsaket av beregning av finansieringstilordninger.</span><span class="sxs-lookup"><span data-stu-id="5199a-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="5199a-134">Definer regler som avgjør hvordan prosjektkostnader faktureres til eksterne kunder og belastes interne organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="5199a-135">Registrer transaksjoner i en på vent-finansieringskonto til flere finansieringer kan innhentes, eller til du bestemmer deg for å bære kostnadene internt.</span><span class="sxs-lookup"><span data-stu-id="5199a-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="5199a-136">Hvis du vil avgjøre hvilken avgiftsgruppe som skal knyttes til en transaksjon, søker du etter en avgiftsgruppetilordning.</span><span class="sxs-lookup"><span data-stu-id="5199a-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="5199a-137">Hvis det ikke er utført en avgiftsgruppetilordning på prosjektnivået, søkes det i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="5199a-138">Eksempel: Flere finansieringskilder (enkel)</span><span class="sxs-lookup"><span data-stu-id="5199a-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="5199a-139">Tabellen nedenfor inneholder scenarier for administrasjon av finansieringsfordeling mellom flere finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="5199a-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="5199a-140">Disse scenariene er basert på følgende antakelser:</span><span class="sxs-lookup"><span data-stu-id="5199a-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="5199a-141">Prioritetsinnstillinger er beregnet på kapitalfordelingen før det tas hensyn til andre finansieringsregelvilkår.</span><span class="sxs-lookup"><span data-stu-id="5199a-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="5199a-142">Det er ikke angitt et datointervall for å definere perioden d når finansieringsregelen er gyldig.</span><span class="sxs-lookup"><span data-stu-id="5199a-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5199a-143"><strong>Scenario</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="5199a-144"><strong>Finansieringskilde</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="5199a-145"><strong>Fordelingsprosent</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="5199a-146"><strong>Tildelingsprioritet</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5199a-147">Du vil fordele kostnader til én finansieringskilde til midlene er oppbrukt, tildele kostnader til en annen finansieringskilde til midlene er oppbrukt, og til slutt tilordne de gjenstående kostnadene til en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-148">Finansieringskilde　1</span><span class="sxs-lookup"><span data-stu-id="5199a-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="5199a-149">Finansieringskilde　2</span><span class="sxs-lookup"><span data-stu-id="5199a-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="5199a-150">Finansieringskilde　3</span><span class="sxs-lookup"><span data-stu-id="5199a-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-151">100%</span><span class="sxs-lookup"><span data-stu-id="5199a-151">100%</span></span></li>
<li><span data-ttu-id="5199a-152">100%</span><span class="sxs-lookup"><span data-stu-id="5199a-152">100%</span></span></li>
<li><span data-ttu-id="5199a-153">100%</span><span class="sxs-lookup"><span data-stu-id="5199a-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-154">1</span><span class="sxs-lookup"><span data-stu-id="5199a-154">1</span></span></li>
<li><span data-ttu-id="5199a-155">2</span><span class="sxs-lookup"><span data-stu-id="5199a-155">2</span></span></li>
<li><span data-ttu-id="5199a-156">3</span><span class="sxs-lookup"><span data-stu-id="5199a-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5199a-157">Du vil fordele 75 prosent av kostnader til én finansieringskilde og 25 prosent til en annen finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5199a-158">Når en av disse finansieringskildene er oppbrukt, vil du betale de gjenstående kostnadene fra en tredje finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-159">Finansieringskilde　1</span><span class="sxs-lookup"><span data-stu-id="5199a-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="5199a-160">Finansieringskilde　2</span><span class="sxs-lookup"><span data-stu-id="5199a-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="5199a-161">Finansieringskilde　3</span><span class="sxs-lookup"><span data-stu-id="5199a-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-162">75 %</span><span class="sxs-lookup"><span data-stu-id="5199a-162">75%</span></span></li>
<li><span data-ttu-id="5199a-163">25 %</span><span class="sxs-lookup"><span data-stu-id="5199a-163">25%</span></span></li>
<li><span data-ttu-id="5199a-164">100%</span><span class="sxs-lookup"><span data-stu-id="5199a-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-165">1</span><span class="sxs-lookup"><span data-stu-id="5199a-165">1</span></span></li>
<li><span data-ttu-id="5199a-166">1</span><span class="sxs-lookup"><span data-stu-id="5199a-166">1</span></span></li>
<li><span data-ttu-id="5199a-167">2</span><span class="sxs-lookup"><span data-stu-id="5199a-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5199a-168">Du vil fordele 75 prosent av kostnader til én finansieringskilde og 25 prosent til en annen finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5199a-169">Når en av disse finansieringskildene er oppbrukt, vil du dele de gjenstående kostnadene mellom en tredje finansieringskilde og en fjerde finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-170">Finansieringskilde　1</span><span class="sxs-lookup"><span data-stu-id="5199a-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="5199a-171">Finansieringskilde　2</span><span class="sxs-lookup"><span data-stu-id="5199a-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="5199a-172">Finansieringskilde　3</span><span class="sxs-lookup"><span data-stu-id="5199a-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="5199a-173">Finansieringskilde　4</span><span class="sxs-lookup"><span data-stu-id="5199a-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-174">75 %</span><span class="sxs-lookup"><span data-stu-id="5199a-174">75%</span></span></li>
<li><span data-ttu-id="5199a-175">25 %</span><span class="sxs-lookup"><span data-stu-id="5199a-175">25%</span></span></li>
<li><span data-ttu-id="5199a-176">50 %</span><span class="sxs-lookup"><span data-stu-id="5199a-176">50%</span></span></li>
<li><span data-ttu-id="5199a-177">50 %</span><span class="sxs-lookup"><span data-stu-id="5199a-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-178">1</span><span class="sxs-lookup"><span data-stu-id="5199a-178">1</span></span></li>
<li><span data-ttu-id="5199a-179">1</span><span class="sxs-lookup"><span data-stu-id="5199a-179">1</span></span></li>
<li><span data-ttu-id="5199a-180">2</span><span class="sxs-lookup"><span data-stu-id="5199a-180">2</span></span></li>
<li><span data-ttu-id="5199a-181">2</span><span class="sxs-lookup"><span data-stu-id="5199a-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5199a-182">Du vil fordele de første 25 prosentene av kostnader til én finansieringskilde og resten til en annen finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-183">Finansieringskilde　1</span><span class="sxs-lookup"><span data-stu-id="5199a-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="5199a-184">Finansieringskilde　2</span><span class="sxs-lookup"><span data-stu-id="5199a-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-185">25 %</span><span class="sxs-lookup"><span data-stu-id="5199a-185">25%</span></span></li>
<li><span data-ttu-id="5199a-186">100%</span><span class="sxs-lookup"><span data-stu-id="5199a-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5199a-187">1</span><span class="sxs-lookup"><span data-stu-id="5199a-187">1</span></span></li>
<li><span data-ttu-id="5199a-188">2</span><span class="sxs-lookup"><span data-stu-id="5199a-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="5199a-189">Eksempel: Flere finansieringskilder (komplisert)</span><span class="sxs-lookup"><span data-stu-id="5199a-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="5199a-190">Du har tre finansieringskilder som du vil bruke i følgende rekkefølge:</span><span class="sxs-lookup"><span data-stu-id="5199a-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="5199a-191">Bruk finansieringskilde 2 og finansieringskilde 3 likt til finansieringskilde 2 er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="5199a-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="5199a-192">Fortsett å bruke finansieringskilde 3 til den er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="5199a-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="5199a-193">Bruk finansieringskilde 1 etter at finansieringskilde 3 er oppbrukt.</span><span class="sxs-lookup"><span data-stu-id="5199a-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="5199a-194">Hvis du vil nå dette målet, må du først gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="5199a-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="5199a-195">Definer finansieringsgrenser for finansieringskilde 2 og finansieringskilde 3 for de respektive beløpene.</span><span class="sxs-lookup"><span data-stu-id="5199a-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="5199a-196">Opprett følgende finansieringsregler:</span><span class="sxs-lookup"><span data-stu-id="5199a-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="5199a-197">Regel 1 (prioritet 1): Tildel 50 prosent av transaksjoner til finansieringskilde 2 og 50 prosent til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="5199a-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="5199a-198">Regel 2 (prioritet 2): Tildel 100 prosent av transaksjoner til finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="5199a-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="5199a-199">Regel 3 (prioritet 3): Tildel 100 prosent av transaksjoner til finansieringskilde 1.</span><span class="sxs-lookup"><span data-stu-id="5199a-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="5199a-200">Denne installasjonen fungerer fordi transaksjoner kontrolleres mot regler og grenser for å avgjøre om noen av dem gjelder for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="5199a-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="5199a-201">Hvis ingen spesifikke regler eller begrensninger gjelder for transaksjonen, gjelder Alle transaksjoner-regelen.</span><span class="sxs-lookup"><span data-stu-id="5199a-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="5199a-202">Regelen Alle transaksjoner samsvarer med alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="5199a-203">Hvis det blir funnet en regel som samsvarer med en transaksjon, brukes prosentandelen som er tilordnet i den regelen, først, men bare etter at samsvarene er kontrollert mot eventuelle begrensninger som er satt opp.</span><span class="sxs-lookup"><span data-stu-id="5199a-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="5199a-204">Hvis en grense er nådd og midlene til en finansieringskilde er oppbrukt, blir finansieringsregelen som er knyttet til finansieringsgrensen, ignorert, og programmet kontrollerer den neste regelen som gjelder.</span><span class="sxs-lookup"><span data-stu-id="5199a-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="5199a-205">I noen tilfeller kan bare deler av en transaksjon tildeles under en regel.</span><span class="sxs-lookup"><span data-stu-id="5199a-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="5199a-206">Dette kan skje fordi en grense er nådd når transaksjonen fordeles.</span><span class="sxs-lookup"><span data-stu-id="5199a-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="5199a-207">I dette tilfellet fordeles bare et bestemt beløp i henhold til den regelen, for eksempel 50 prosent for hver finansieringskilde.</span><span class="sxs-lookup"><span data-stu-id="5199a-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="5199a-208">Dette er tilfellet i regel 1, som er beskrevet tidligere i denne delen.</span><span class="sxs-lookup"><span data-stu-id="5199a-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="5199a-209">Resten fordeles i henhold til neste regel i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="5199a-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="5199a-210">Følgende tabell undersøker dette scenarioet mer detaljert.</span><span class="sxs-lookup"><span data-stu-id="5199a-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5199a-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="5199a-212"><strong>Detaljer</strong></span><span class="sxs-lookup"><span data-stu-id="5199a-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5199a-213">Finansieringsregler</span><span class="sxs-lookup"><span data-stu-id="5199a-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-214">Regel 1 (prioritet 1): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="5199a-215">Tildel finansieringskilde 2 på 50 % og finansieringskilde 3 på 50 %.</span><span class="sxs-lookup"><span data-stu-id="5199a-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="5199a-216">Regel 2 (prioritet 2): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="5199a-217">Tilordne finansieringskilde 3 på 100 %.</span><span class="sxs-lookup"><span data-stu-id="5199a-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="5199a-218">Regel 3 (prioritet 2): Alle transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="5199a-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="5199a-219">Tilordne finansieringskilde 1 på 100 %.</span><span class="sxs-lookup"><span data-stu-id="5199a-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5199a-220">Finansieringsgrenser</span><span class="sxs-lookup"><span data-stu-id="5199a-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-221">Grense for finansieringskilde 1 = 10 000.00</span><span class="sxs-lookup"><span data-stu-id="5199a-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="5199a-222">Grense for finansieringskilde 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="5199a-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="5199a-223">Grense for finansieringskilde 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="5199a-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5199a-224">Transaksjon 1</span><span class="sxs-lookup"><span data-stu-id="5199a-224">Transaction 1</span></span></td>
<td><span data-ttu-id="5199a-225"><strong>Transaksjonsbeløp:</strong> 100,00<strong>Finansiering:</strong> Transaksjonen betales bare i henhold til regel 1, fordi transaksjonen er fullt betalt etter at regel 1 er brukt.</span><span class="sxs-lookup"><span data-stu-id="5199a-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="5199a-226">Transaksjonen er finansiert likt mellom finansieringskilde 2 og finansieringskilde 3.</span><span class="sxs-lookup"><span data-stu-id="5199a-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="5199a-227">Finansieringskilde 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="5199a-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="5199a-228">Finansieringskilde 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="5199a-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5199a-229">Transaksjon 2</span><span class="sxs-lookup"><span data-stu-id="5199a-229">Transaction 2</span></span></td>
<td><span data-ttu-id="5199a-230"><strong>Transaksjonsbeløp:</strong> 5 000,00<strong>Finansiering:</strong> Transaksjonen betales i henhold til alle tre regler.</span><span class="sxs-lookup"><span data-stu-id="5199a-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="5199a-231"><strong>Regel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="5199a-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="5199a-232">Finansieringskilde 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="5199a-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="5199a-233">Finansieringskilde 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="5199a-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="5199a-234">
<strong>Regel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="5199a-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="5199a-235">Finansieringskilde 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="5199a-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="5199a-236">
<strong>Regel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="5199a-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="5199a-237">Finansieringskilde 1: 3850.00 (= 5000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="5199a-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5199a-238">Totalt antall midler som er fordelt for hver finansieringskilde</span><span class="sxs-lookup"><span data-stu-id="5199a-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="5199a-239">Finansieringskilde 1: 3850.00</span><span class="sxs-lookup"><span data-stu-id="5199a-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="5199a-240">Finansieringskilde 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="5199a-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="5199a-241">Finansieringskilde 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="5199a-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="5199a-242">Faktureringsregler</span><span class="sxs-lookup"><span data-stu-id="5199a-242">Billing rules</span></span>
<span data-ttu-id="5199a-243">Når du forhandler en prosjektkontrakt med en kunde, definerer du hvordan og når du kan fakturere kunden for arbeid på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5199a-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="5199a-244">Etter at du har satt opp prosjektkontrakten og prosjektet, kan du definere faktureringsregler for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="5199a-245">Faktureringsregler er basert på prosjektvilkår som er angitt i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="5199a-246">Faktureringsreglene du kan opprette, avhenger av betingelsene i prosjektkontrakten og prosjekttypen, for eksempel Tid og materiale eller Fast pris, som du knytter til faktureringsregelen.</span><span class="sxs-lookup"><span data-stu-id="5199a-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="5199a-247">Du kan opprette mer enn én faktureringsregel for en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="5199a-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="5199a-248">Du kan også tilordne en faktureringsregel til flere prosjekter som er knyttet til den samme prosjektkontrakten, og som har lignende faktureringsvilkår.</span><span class="sxs-lookup"><span data-stu-id="5199a-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="5199a-249">Du kan definere følgende typer faktureringsregler:</span><span class="sxs-lookup"><span data-stu-id="5199a-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="5199a-250">**Leveringsenhet** – Fakturere en kunde når du fullfører en leveringsenhet.</span><span class="sxs-lookup"><span data-stu-id="5199a-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="5199a-251">Du definerer leveringsenhetene i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="5199a-252">**Fremdrift** – Fakturere en kunde når du fullfører en bestemt prosentdel av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="5199a-253">Du kan angi en faktureringsregel for automatisk å beregne prosentandelen av fullført arbeid, eller du kan manuelt beregne prosentandelen av fullført arbeid og beløpet for å fakturere kunden.</span><span class="sxs-lookup"><span data-stu-id="5199a-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="5199a-254">**Milepæl** – Fakturerer en kunde for hele beløpet for en prosjektmilepæl når milepælen er nådd.</span><span class="sxs-lookup"><span data-stu-id="5199a-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="5199a-255">**Gebyr** – Fakturer en kunde for tjenestene pluss et administrasjonsgebyr, som vanligvis er en prosentdel av prisen på tjenestene.</span><span class="sxs-lookup"><span data-stu-id="5199a-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="5199a-256">**Tid og materialer** – Fakturerer en kunde for verdien av tid og materialer som brukes på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5199a-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="5199a-257">For alle typer faktureringsregler kan du angi en tilbakeholdelsesprosent som trekkes fra kundefakturaer til et prosjekt når en avtalt fase.</span><span class="sxs-lookup"><span data-stu-id="5199a-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="5199a-258">Tilbakeholdelsesprosenten for betalingen er angitt i prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="5199a-259">Beløpet beregnes basert på, og trekkes fra, totalverdien for linjene i en kundefaktura.</span><span class="sxs-lookup"><span data-stu-id="5199a-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="5199a-260">For faktureringsreglene **Tid og materiale** og **Fremdrift** kan du tilordne belastbare kategorier.</span><span class="sxs-lookup"><span data-stu-id="5199a-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="5199a-261">Belastbare kategorier angir transaksjonene som skal tas med i kundefakturaer.</span><span class="sxs-lookup"><span data-stu-id="5199a-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="5199a-262">Når du er klar til å fakturere kunden, beregnes beløpet som skal faktureres for prosjektet, basert på faktureringsreglene, og et prosjektfakturaforslag genereres.</span><span class="sxs-lookup"><span data-stu-id="5199a-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="5199a-263">Avsnittene nedenfor inneholder eksempler som viser hvordan du konfigurerer og behandler faktureringsregler for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="5199a-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="5199a-264">Eksempel: Opprett en faktureringsregel som er basert på antallet enheter som er levert</span><span class="sxs-lookup"><span data-stu-id="5199a-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="5199a-265">Organisasjonen går inn i en avtale for å gi totalt fem opplæringsøkter til en kundes ansatte til en kostnad på 10 000 per opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="5199a-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="5199a-266">Du fakturerer kunden etter hver opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="5199a-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="5199a-267">Når du definerer faktureringsreglene for kontrakten, bruker du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="5199a-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="5199a-268">Leveringsenheten er én opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="5199a-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="5199a-269">Enhetsprisen er 10 000 per opplæringsøkt.</span><span class="sxs-lookup"><span data-stu-id="5199a-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="5199a-270">Det totale antallet enheter er fem opplæringsøkter.</span><span class="sxs-lookup"><span data-stu-id="5199a-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="5199a-271">Når du har fullført én opplæringsøkt, kan du opprette en faktura på 10 000 for den første enheten som er levert, og sende fakturaen til kunden.</span><span class="sxs-lookup"><span data-stu-id="5199a-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="5199a-272">Eksempel: Opprett en faktureringsregel som er basert på en bestemt prosentandel av prosjektfullførelsen (manuell beregning)</span><span class="sxs-lookup"><span data-stu-id="5199a-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="5199a-273">Organisasjonen din, et programvarekonsulentfirma, inngår en avtale med en kunde for å utvikle en del av et produkt som kunden utvikler.</span><span class="sxs-lookup"><span data-stu-id="5199a-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="5199a-274">Organisasjonen din godtar å levere programvarekoden over en periode på seks måneder.</span><span class="sxs-lookup"><span data-stu-id="5199a-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="5199a-275">Kunden avtaler å betale organisasjonen en sum på 100 000 for arbeidet.</span><span class="sxs-lookup"><span data-stu-id="5199a-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="5199a-276">Du oppretter en faktureringsregel for å fakturere kunden basert på prosentandelen av arbeid som er fullført på prosjektet, som angitt i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="5199a-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="5199a-277">På slutten av den første måneden møter du kunden for å bestemme fullføringsprosenten for arbeidet som er fullført.</span><span class="sxs-lookup"><span data-stu-id="5199a-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="5199a-278">Når du og kunden ser gjennom prosjektet, avgjør du at prosjektet er 15 % fullført.</span><span class="sxs-lookup"><span data-stu-id="5199a-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="5199a-279">Du oppretter en faktura på 15 000 (15 prosent av 100 000) og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="5199a-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="5199a-280">Eksempel: Opprett en faktureringsregel som er basert på en bestemt prosentandel av prosjektfullførelsen (automatisk beregning)</span><span class="sxs-lookup"><span data-stu-id="5199a-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="5199a-281">Organisasjonen din, et selskap for programvareutvikling, avtaler å utvikle en lønnsregnskapspakke for en kunde for 30 000.</span><span class="sxs-lookup"><span data-stu-id="5199a-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="5199a-282">Kunden avtaler å betale organisasjonen basert på en prosentandel fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="5199a-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="5199a-283">Du beregner at prosjektkostnadene er 20 000.</span><span class="sxs-lookup"><span data-stu-id="5199a-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="5199a-284">Prosjektkontrakten spesifiserer arbeidskategoriene du bruker i faktureringsprosessen.</span><span class="sxs-lookup"><span data-stu-id="5199a-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="5199a-285">Du definerer faktureringsregler som automatisk beregner fakturabeløpene for prosentandelen arbeid som er fullført for hver kategori.</span><span class="sxs-lookup"><span data-stu-id="5199a-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5199a-286">Du definerer et budsjett for hver kategori:</span><span class="sxs-lookup"><span data-stu-id="5199a-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="5199a-287">**Utvikling** – Kostnad på 15 000 og omsetning på 20 000</span><span class="sxs-lookup"><span data-stu-id="5199a-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="5199a-288">**Installasjon** – Kostnad på 5 000 og omsetning på 10 000</span><span class="sxs-lookup"><span data-stu-id="5199a-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="5199a-289">Når du oppretter en kundefaktura for første gang, beregnes fakturabeløpet automatisk basert på følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="5199a-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="5199a-290">Etter en måned sender arbeideren i prosjektet en timeregistrering for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="5199a-291">Kostnaden for arbeiderens timer er 5 000 for utvikling og 1 000 for installasjon.</span><span class="sxs-lookup"><span data-stu-id="5199a-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="5199a-292">Utviklingsarbeidet er 33 prosent fullført (5 000 faktisk kostnad / 15 000 budsjettkostnader), og installasjonsarbeidet er 20 prosent fullført (1 000 faktisk kostnad / 5 000 budsjettkostnad).</span><span class="sxs-lookup"><span data-stu-id="5199a-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="5199a-293">Fakturabeløpet på 8 667 beregnes automatisk (33 prosent av 20 000 + 20 prosent av 10 000).</span><span class="sxs-lookup"><span data-stu-id="5199a-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="5199a-294">Du oppretter en faktura på 8,667 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="5199a-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="5199a-295">Eksempel: Opprett en faktureringsregel som er basert på avtalte milepæler</span><span class="sxs-lookup"><span data-stu-id="5199a-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="5199a-296">Organisasjonen din, et konsulentfirma for ledelse, avtaler å gjennomføre markedsundersøkelse for et forbrukerprodukt som kunden planlegger å selge.</span><span class="sxs-lookup"><span data-stu-id="5199a-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="5199a-297">Kunden avtaler å bruke tjenestene dine i tre måneder, fra og med mars, og godtar å betale organisasjonen 50 000.</span><span class="sxs-lookup"><span data-stu-id="5199a-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="5199a-298">Prosjektet har tre milepæler:</span><span class="sxs-lookup"><span data-stu-id="5199a-298">The project has three milestones:</span></span>

-   <span data-ttu-id="5199a-299">Milepæl 1: Samle inn forbrukerdata – 31. mars</span><span class="sxs-lookup"><span data-stu-id="5199a-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="5199a-300">Milepæl 2: Analysere forbrukerdata – 30. april</span><span class="sxs-lookup"><span data-stu-id="5199a-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="5199a-301">Milepæl 3: Presentere et forslag til produktets levedyktighet – 31. mai</span><span class="sxs-lookup"><span data-stu-id="5199a-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="5199a-302">Kunden avtaler å betale organisasjonen 10 000 for den første milepælen, 20 000 for den andre milepælen og 20 000 for den tredje milepælen.</span><span class="sxs-lookup"><span data-stu-id="5199a-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="5199a-303">Når du setter opp prosjektkontrakten, godtar du at kunden faktureres basert på milepælen som er fullført.</span><span class="sxs-lookup"><span data-stu-id="5199a-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="5199a-304">Faktureringsregeloppsettet inkluderer følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="5199a-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="5199a-305">Definer milepælene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-305">Define the project milestones.</span></span>
-   <span data-ttu-id="5199a-306">Definer beløpet som skal faktureres for kunden når hver milepæl er fullført.</span><span class="sxs-lookup"><span data-stu-id="5199a-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="5199a-307">Når den første milepælen er fullført 31. mars, merker du milepælen som fullført, og deretter oppretter du en faktura på 10 000 og sender den til kunden.</span><span class="sxs-lookup"><span data-stu-id="5199a-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="5199a-308">Du kan ikke opprette en faktura for en milepæl før du har merket milepælen som fullført.</span><span class="sxs-lookup"><span data-stu-id="5199a-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="5199a-309">Eksempel: Opprett en faktureringsregel som er basert på tjenester pluss et administrasjonsgebyr</span><span class="sxs-lookup"><span data-stu-id="5199a-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="5199a-310">Organisasjonen din, et konsulentfirma for ledelse, avtaler å gjennomføre markedsundersøkelser for å evaluere levedyktigheten til et produkt som kunden, et detaljhandelsselskap, utvikler.</span><span class="sxs-lookup"><span data-stu-id="5199a-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="5199a-311">Vilkårene i avtalen angir at du tilbyr tjenestene til de tre beste ledelseskonsulentene, som skal utføre undersøkelsen på tid og materialer-basis.</span><span class="sxs-lookup"><span data-stu-id="5199a-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="5199a-312">Kunden godtar å betale 100 per time, pluss et 10 prosent administrasjonsgebyr for konsulenttimene som blir belastet prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5199a-313">Når du setter opp prosjektkontrakten, oppretter du en faktureringsregel som legger til 10 prosent administrasjonsgebyr på konsulenttimene som belastes prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5199a-314">Når du oppretter en faktura for kunden, faktureres kunden et administrasjonsgebyr på 10 %, pluss kostnadene for konsulenttimene.</span><span class="sxs-lookup"><span data-stu-id="5199a-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="5199a-315">Hvis de tre konsulenter for eksempel arbeidet totalt 200 timer på prosjektet, opprettes det en faktura på 22 000 basert på følgende beregning:</span><span class="sxs-lookup"><span data-stu-id="5199a-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="5199a-316">200 timer à 100 per time = 20 000</span><span class="sxs-lookup"><span data-stu-id="5199a-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="5199a-317">10 prosent administrasjonsgebyr = 2 000</span><span class="sxs-lookup"><span data-stu-id="5199a-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="5199a-318">Totalt fakturabeløp = 22 000</span><span class="sxs-lookup"><span data-stu-id="5199a-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="5199a-319">Hvis gebyrer er avgiftspliktige til en kunde, og du velger en mva-gruppe i prosjektkontrakten, angis mva-gruppen automatisk i en faktureringsregel for gebyrer.</span><span class="sxs-lookup"><span data-stu-id="5199a-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="5199a-320">Eksempel: Opprett en faktureringsregel for verdien av tid og materialer</span><span class="sxs-lookup"><span data-stu-id="5199a-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="5199a-321">Organisasjonen din, et programvarekonsulentfirma, er enige om å gi fem tekniske konsulenter mulighet til å arbeide med et programvareutviklingsprosjekt for en kunde i de neste seks månedene.</span><span class="sxs-lookup"><span data-stu-id="5199a-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="5199a-322">Kunden godtar å betale 150 for hver konsulenttime, pluss kostnadene for kontorutstyr.</span><span class="sxs-lookup"><span data-stu-id="5199a-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="5199a-323">Organisasjonen din sender en faktura til kunden i slutten av hver måned.</span><span class="sxs-lookup"><span data-stu-id="5199a-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="5199a-324">Når du setter opp prosjektkontrakten, godtar du at kunden faktureres hver måned for tid og materialer på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="5199a-325">Du oppretter en faktureringsregel som inneholder følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="5199a-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="5199a-326">Kontraktperioden er seks måneder.</span><span class="sxs-lookup"><span data-stu-id="5199a-326">The contract period is six months.</span></span>
-   <span data-ttu-id="5199a-327">Konsulenttiden blir beregnet med en sats på 150 per time.</span><span class="sxs-lookup"><span data-stu-id="5199a-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="5199a-328">Kontorrekvisita er fakturert med kostnad, og totale kostnader for prosjektet må ikke overskride 10 000.</span><span class="sxs-lookup"><span data-stu-id="5199a-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="5199a-329">Du oppretter en kundefaktura på slutten av hver kalendermåned i løpet av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="5199a-330">I løpet av den første måneden registreres totalt 800 timer av konsulentene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="5199a-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="5199a-331">Kostnadene for kontorutstyr som er belastet for prosjektet, er 2 000.</span><span class="sxs-lookup"><span data-stu-id="5199a-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="5199a-332">På slutten av måneden oppretter du derfor en faktura på 122 000, som beregnes som 800 timer til 150 per time, og i tillegg 2 000 for kontorutstyr.</span><span class="sxs-lookup"><span data-stu-id="5199a-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



