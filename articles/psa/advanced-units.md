---
title: Enhetsgrupper og enheter
description: Dette emnet inneholder informasjon om enhetsgrupper og enheter.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145595"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="e0f9e-103">Enhetsgrupper og enheter</span><span class="sxs-lookup"><span data-stu-id="e0f9e-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e0f9e-104">Enhetsgrupper og enheter er basisenheter i Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="e0f9e-105">En enhet er en enkelt målenhet, og flere enheter kan grupperes i enhetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="e0f9e-106">En enhetsgruppe kalles noen ganger en enhetstidsplan i brukergrensesnittet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="e0f9e-107">Her er noen eksempler på enheter og enhetsgrupper:</span><span class="sxs-lookup"><span data-stu-id="e0f9e-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="e0f9e-108">**Enhetsgruppe**: Avstand</span><span class="sxs-lookup"><span data-stu-id="e0f9e-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="e0f9e-109">**Enheter**: Mile, kilometer og så videre.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="e0f9e-110">**Enhetsgruppe**: Tid</span><span class="sxs-lookup"><span data-stu-id="e0f9e-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="e0f9e-111">**Enheter**: Time, dag, uke og så videre.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="e0f9e-112">Når du definerer flere enheter i en enhetsgruppe, må du også angi en konverteringsfaktor mellom dem ved å angi den første enheten som er angitt som standard- eller primærenhet for enhetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="e0f9e-113">For eksempel, i en **Tid**-enhetsgruppe, hvis du definerer **Time** som den første enheten, tilordner systemet **Time** som standardenhet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="e0f9e-114">Hvis neste enhet du angir, er **Dag**, må du konfigurere en konverteringsfaktor for **Dag** til **Time**.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="e0f9e-115">Hvis du deretter legger til **Uke** som en tredje enhet, må du angi en konverteringsfaktor for **Uke** i form av **Dag** eller **Time**.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="e0f9e-116">Følgende bilde viser et eksempel på oppsett for **Dag**-enheten, der **Antall**-feltet viser antall timer i løpet av en dag, og i **Uke**, der **Antall**-feltet viser antall dager i uken.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Enhetsgruppe: informasjonsside](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="e0f9e-118">Bruke enheter og enhetsgrupper</span><span class="sxs-lookup"><span data-stu-id="e0f9e-118">Using units and unit groups</span></span>

<span data-ttu-id="e0f9e-119">Dynamics 365 Project Service Automation bruker enheter og enhetsgrupper til å behandle estimater og oppføringer for både utgifter og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="e0f9e-120">For utgifter har hver utgiftskategori en standard enhetsgruppe og enhet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="e0f9e-121">Disse verdiene angis som standardverdier for prislisteoppføringer for utgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="e0f9e-122">Du har for eksempel en utgiftskategori som kalles **Reisegodtgjørelse**.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="e0f9e-123">Den har en enhetsgruppe som har navnet **Distanse** og en standardenhet med navnet **Mile**.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="e0f9e-124">Hvis du konfigurerer **Distanse**-enhetsgruppen slik at den har to enheter (**Mile** og **Kilometer**), kan du angi to priser for **Reisegodtgjørelse**-kategorien i én prisliste: pris per mile og pris per kilometer.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="e0f9e-125">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="e0f9e-125">Expense category</span></span>  | <span data-ttu-id="e0f9e-126">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="e0f9e-126">Unit group</span></span>  | <span data-ttu-id="e0f9e-127">Enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-127">Unit</span></span>      | <span data-ttu-id="e0f9e-128">Prismodell</span><span class="sxs-lookup"><span data-stu-id="e0f9e-128">Pricing method</span></span>  | <span data-ttu-id="e0f9e-129">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="e0f9e-130">Reisegodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="e0f9e-130">Mileage</span></span>           | <span data-ttu-id="e0f9e-131">Avstand</span><span class="sxs-lookup"><span data-stu-id="e0f9e-131">Distance</span></span>      | <span data-ttu-id="e0f9e-132">Mile</span><span class="sxs-lookup"><span data-stu-id="e0f9e-132">Mile</span></span>      | <span data-ttu-id="e0f9e-133">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-133">Price per unit</span></span>    | <span data-ttu-id="e0f9e-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="e0f9e-134">10 USD</span></span>            |
| <span data-ttu-id="e0f9e-135">Reisegodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="e0f9e-135">Mileage</span></span>           | <span data-ttu-id="e0f9e-136">Avstand</span><span class="sxs-lookup"><span data-stu-id="e0f9e-136">Distance</span></span>      | <span data-ttu-id="e0f9e-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="e0f9e-137">Kilometer</span></span> | <span data-ttu-id="e0f9e-138">Pris per enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-138">Price per unit</span></span>    |  <span data-ttu-id="e0f9e-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="e0f9e-139">6 USD</span></span>            |

<span data-ttu-id="e0f9e-140">Når du angir en utgift i et prosjekt, bestemmer systemet prisen gjennom kombinasjonen av kategorien og enheten i utgiften.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="e0f9e-141">Utgiftsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="e0f9e-141">Expense description</span></span>        | <span data-ttu-id="e0f9e-142">Utgiftskategori</span><span class="sxs-lookup"><span data-stu-id="e0f9e-142">Expense category</span></span>  | <span data-ttu-id="e0f9e-143">Enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-143">Unit</span></span>  | <span data-ttu-id="e0f9e-144">Antall</span><span class="sxs-lookup"><span data-stu-id="e0f9e-144">Quantity</span></span>  | <span data-ttu-id="e0f9e-145">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="e0f9e-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="e0f9e-146">Kjøring til klientsted</span><span class="sxs-lookup"><span data-stu-id="e0f9e-146">Drive to client location</span></span> | <span data-ttu-id="e0f9e-147">Reisegodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="e0f9e-147">Mileage</span></span>             | <span data-ttu-id="e0f9e-148">Mile</span><span class="sxs-lookup"><span data-stu-id="e0f9e-148">Mile</span></span>  | <span data-ttu-id="e0f9e-149">10</span><span class="sxs-lookup"><span data-stu-id="e0f9e-149">10</span></span>        | <span data-ttu-id="e0f9e-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="e0f9e-150">10 USD</span></span>         |

<span data-ttu-id="e0f9e-151">For tid har hvert prislistehode et **Standard tidsenhet**-felt.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="e0f9e-152">Verdien angis når du oppretter prislistehodet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="e0f9e-153">Denne enheten brukes deretter til å angi alle rollebaserte priser i denne prislisten.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="e0f9e-154">Estimatlinjer for feltet **Tid i tilbud** kan uttrykkes i en hvilken som helst enhet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="e0f9e-155">Estimatlinjer på prosjekter og tidsoppføringer for prosjekter kan imidlertid bruke bare **Time**-enheten.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="e0f9e-156">Hvis enheten i tidsoppføringen eller på estimatlinjen ikke samsvarer med enheten på prislistelinjen for den aktuelle rollen, konverterer systemet prisen til enhetene som er definert i prosjektestimatet eller den faktiske transaksjonen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="e0f9e-157">Følgende eksempel viser hvordan PSA bruker enhetsgruppen, enhetene og konverteringsfaktorene.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="e0f9e-158">Enheter</span><span class="sxs-lookup"><span data-stu-id="e0f9e-158">Units</span></span>

   - <span data-ttu-id="e0f9e-159">**Enhetsgruppe**: Tid</span><span class="sxs-lookup"><span data-stu-id="e0f9e-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="e0f9e-160">**Enheter**: Time</span><span class="sxs-lookup"><span data-stu-id="e0f9e-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="e0f9e-161">**Dag** – omregningsfaktor: 8 timer</span><span class="sxs-lookup"><span data-stu-id="e0f9e-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="e0f9e-162">**Uke** – omregningsfaktor: 40 timer</span><span class="sxs-lookup"><span data-stu-id="e0f9e-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="e0f9e-163">Prislisteoppsett for prosjekt A:</span><span class="sxs-lookup"><span data-stu-id="e0f9e-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="e0f9e-164">**Navn**: Salgspriser i UK 2016</span><span class="sxs-lookup"><span data-stu-id="e0f9e-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="e0f9e-165">**Standard tidsenhet**: Dag</span><span class="sxs-lookup"><span data-stu-id="e0f9e-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="e0f9e-166">**Valuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="e0f9e-166">**Currency**: GBP</span></span>

| <span data-ttu-id="e0f9e-167">Rolle</span><span class="sxs-lookup"><span data-stu-id="e0f9e-167">Role</span></span>      | <span data-ttu-id="e0f9e-168">Enhetsgruppe</span><span class="sxs-lookup"><span data-stu-id="e0f9e-168">Unit group</span></span> | <span data-ttu-id="e0f9e-169">Enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-169">Unit</span></span> | <span data-ttu-id="e0f9e-170">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-170">Organizational unit</span></span> | <span data-ttu-id="e0f9e-171">Pris</span><span class="sxs-lookup"><span data-stu-id="e0f9e-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="e0f9e-172">Utvikler</span><span class="sxs-lookup"><span data-stu-id="e0f9e-172">Developer</span></span> | <span data-ttu-id="e0f9e-173">Time</span><span class="sxs-lookup"><span data-stu-id="e0f9e-173">Time</span></span>       | <span data-ttu-id="e0f9e-174">Day</span><span class="sxs-lookup"><span data-stu-id="e0f9e-174">Day</span></span>  | <span data-ttu-id="e0f9e-175">Ekeli UK</span><span class="sxs-lookup"><span data-stu-id="e0f9e-175">Contoso UK</span></span>          | <span data-ttu-id="e0f9e-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="e0f9e-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="e0f9e-177">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="e0f9e-177">Time entry</span></span>

<span data-ttu-id="e0f9e-178">Tabellen nedenfor viser den resulterende transaksjonen på salgssiden som opprettes av PSA for et prosjekt på tre timer.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="e0f9e-179">Prosjekt</span><span class="sxs-lookup"><span data-stu-id="e0f9e-179">Project</span></span>   | <span data-ttu-id="e0f9e-180">Oppgave</span><span class="sxs-lookup"><span data-stu-id="e0f9e-180">Task</span></span>    | <span data-ttu-id="e0f9e-181">Rolle</span><span class="sxs-lookup"><span data-stu-id="e0f9e-181">Role</span></span>      | <span data-ttu-id="e0f9e-182">Antall</span><span class="sxs-lookup"><span data-stu-id="e0f9e-182">Quantity</span></span> | <span data-ttu-id="e0f9e-183">Enhet</span><span class="sxs-lookup"><span data-stu-id="e0f9e-183">Unit</span></span>  | <span data-ttu-id="e0f9e-184">Enhetspris</span><span class="sxs-lookup"><span data-stu-id="e0f9e-184">Unit price</span></span> | <span data-ttu-id="e0f9e-185">Ufakturert salgsbeløp</span><span class="sxs-lookup"><span data-stu-id="e0f9e-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="e0f9e-186">Prosjekt A</span><span class="sxs-lookup"><span data-stu-id="e0f9e-186">Project A</span></span> | <span data-ttu-id="e0f9e-187">Utforming</span><span class="sxs-lookup"><span data-stu-id="e0f9e-187">Design</span></span>  | <span data-ttu-id="e0f9e-188">Utvikler</span><span class="sxs-lookup"><span data-stu-id="e0f9e-188">Developer</span></span> | <span data-ttu-id="e0f9e-189">3</span><span class="sxs-lookup"><span data-stu-id="e0f9e-189">3</span></span>        | <span data-ttu-id="e0f9e-190">Hour</span><span class="sxs-lookup"><span data-stu-id="e0f9e-190">Hour</span></span>  | <span data-ttu-id="e0f9e-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="e0f9e-191">100 GBP</span></span>    | <span data-ttu-id="e0f9e-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="e0f9e-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="e0f9e-193">Vanlige spørsmål om tidsenheter</span><span class="sxs-lookup"><span data-stu-id="e0f9e-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="e0f9e-194">Konverterer PSA til andre enheter når det gjelder utgifter?</span><span class="sxs-lookup"><span data-stu-id="e0f9e-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="e0f9e-195">Nr.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-195">No.</span></span> <span data-ttu-id="e0f9e-196">Enhetskonverteringen fungerer bare for tid.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-196">Unit conversion works only for time.</span></span> <span data-ttu-id="e0f9e-197">For utgifter, hvis systemet ikke finner en pris for kombinasjonen av utgiftskategori og enhet, settes prisen til 0,00 som standard.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="e0f9e-198">Hvorfor konverterer PSA tidsenheter?</span><span class="sxs-lookup"><span data-stu-id="e0f9e-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="e0f9e-199">I noen land eller områder er det juridiske krav for at faktureringspriser skal angis i dager.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="e0f9e-200">Prisforhandling og rabattering i løpet av tilbudssyklusen utføres ved hjelp av dagsrater for hver fakturerbare rolle.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="e0f9e-201">Tidsplanestimat og tidsregistrering utføres i timer.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="e0f9e-202">PSA konverterer tidsenheter for å støtte denne forskjellen i tidsenheter.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="e0f9e-203">Kan tidsenheter endres i prosjektestimater?</span><span class="sxs-lookup"><span data-stu-id="e0f9e-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="e0f9e-204">Nr.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-204">No.</span></span> <span data-ttu-id="e0f9e-205">Tidsplanestimering er for øyeblikket begrenset til timer og kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="e0f9e-206">Kan enheter og enhetsgrupper redigeres, slettes og legges til?</span><span class="sxs-lookup"><span data-stu-id="e0f9e-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="e0f9e-207">Ja.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-207">Yes.</span></span> <span data-ttu-id="e0f9e-208">Med unntak av **Tid**-enhetsgruppen og **Time**-enheten kan alle enheter slettes eller redigeres, og det kan legges til nye enheter.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="e0f9e-209">I PSA kan **Tid**-enhetsgruppen og **Time**-enheten ikke slettes.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="e0f9e-210">De kan imidlertid oppdateres med en oversatt tekst for **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e0f9e-210">However, they can be updated with a translated text for the **Name** field.</span></span>
