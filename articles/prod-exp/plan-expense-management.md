---
title: Konfigurere utgiftshåndtering
description: Denne artikkelen beskriver vurderinger og avgjørelser du må gjøre under planleggingsprosessen, før du konfigurerer utgiftshåndtering i Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271365"
---
# <a name="configure-expense-management"></a><span data-ttu-id="be289-103">Konfigurere utgiftshåndtering</span><span class="sxs-lookup"><span data-stu-id="be289-103">Configure expense management</span></span>

<span data-ttu-id="be289-104">Dette emnet beskriver vurderinger og avgjørelser du må gjøre under planleggingsprosessen, før du konfigurerer Utgiftshåndtering.</span><span class="sxs-lookup"><span data-stu-id="be289-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="be289-105">I Utgiftshåndtering kan du lagre informasjon om betalingsmetoder, reiserekvisisjoner, reiseregninger, policyer og så videre.</span><span class="sxs-lookup"><span data-stu-id="be289-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="be289-106">Ettersom mange av beslutningene du tar når du planlegger konfigurasjonen for Utgiftshåndtering, er basert på organisasjonens hierarki og finansielle struktur, må du referere til planleggingsdokumentene for disse områdene.</span><span class="sxs-lookup"><span data-stu-id="be289-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="be289-107">Konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="be289-107">Intercompany expenses</span></span>

<span data-ttu-id="be289-108">Når du aktiverer konserninterne utgifter, tillater du at juridiske enheter og ansatte påløper utgifter på vegne av en annen juridisk enhet, og krever inn betaling fra den juridiske enheten for ansettelse innenfor organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="be289-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="be289-109">En ansatt i juridisk enhet A fullfører for eksempel et prosjekt for juridisk enhet B, og prosjektet påløper reiserelaterte utgifter.</span><span class="sxs-lookup"><span data-stu-id="be289-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="be289-110">Hvis konserninterne utgifter er aktivert, kan den ansatte deretter sende en reiseregning som vil postere utgiften til juridisk enhet B, og utgiften må deretter betales av juridisk enhet A. Hvis organisasjonen ikke har flere juridiske enheter, trenger du ikke å aktivere konserninterne utgifter.</span><span class="sxs-lookup"><span data-stu-id="be289-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="be289-111">**Beslutning:** Vil du aktivere konserninterne utgifter?</span><span class="sxs-lookup"><span data-stu-id="be289-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="be289-112">Finansadministrasjon</span><span class="sxs-lookup"><span data-stu-id="be289-112">Financial management</span></span>

<span data-ttu-id="be289-113">Utgiftshåndtering er tett integrert med den økonomiske administreringen av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="be289-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="be289-114">Mye av konfigurasjonene for Utgiftshåndtering er basert på beslutningene du har tatt om organisasjonens økonomi.</span><span class="sxs-lookup"><span data-stu-id="be289-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="be289-115">Avsnittene nedenfor beskriver de forskjellige områdene som krever planlegging og beslutninger, basert på organisasjonens finansielle avgjørelser og veiledninger fra lederteamet.</span><span class="sxs-lookup"><span data-stu-id="be289-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="be289-116">Kostgodtgjørelser</span><span class="sxs-lookup"><span data-stu-id="be289-116">Per diems</span></span>

<span data-ttu-id="be289-117">Du må definere den ansattes kostgodtgjørelse som organisasjonen tilbyr.</span><span class="sxs-lookup"><span data-stu-id="be289-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="be289-118">Fordi kostgodtgjørelse vanligvis brukes til å dekke utgifter som måltider, overnatting og andre tilfeldige utgifter, kan du lage regler for kostgodtgjørelsene som organisasjonen tilbyr.</span><span class="sxs-lookup"><span data-stu-id="be289-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="be289-119">Kostgodtgjørelsessatser kan baseres på tiden på året, reisestedet eller begge deler.</span><span class="sxs-lookup"><span data-stu-id="be289-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="be289-120">Når du definerer en kostgodtgjørelsesregel, kan du angi at en prosentsats av kostgodtgjørelsessatsen skal tilbakeholdes hvis en arbeider mottar gratis måltider eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="be289-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="be289-121">Du kan også definere kostgodtgjørelsessatser for å angi et minimum og maksimum antall timer som kostgodtgjørelsessatsen kan gjelde for en arbeiders reise.</span><span class="sxs-lookup"><span data-stu-id="be289-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="be289-122">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-122">**Decisions:**</span></span>

- <span data-ttu-id="be289-123">Standard kostgodtgjørelsesregler for første og siste dag:</span><span class="sxs-lookup"><span data-stu-id="be289-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="be289-124">Hva er minste antall timer en ansatt kan kreve for en dag og likevel motta kostgodtgjørelse?</span><span class="sxs-lookup"><span data-stu-id="be289-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="be289-125">Blir det en reduksjon av beløpet som tilbys for måltider første dag og siste dag?</span><span class="sxs-lookup"><span data-stu-id="be289-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="be289-126">Hva det er en reduksjon, hva er prosentandelen av reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="be289-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="be289-127">Blir det en reduksjon av beløpet som tilbys for et hotell første dag og siste dag?</span><span class="sxs-lookup"><span data-stu-id="be289-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="be289-128">Hva det er en reduksjon, hva er prosentandelen av reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="be289-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="be289-129">Blir det en reduksjon av beløpet som tilbys for andre utgifter som påløpte første dag og siste dag?</span><span class="sxs-lookup"><span data-stu-id="be289-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="be289-130">Hva det er en reduksjon, hva er prosentandelen av reduksjonen?</span><span class="sxs-lookup"><span data-stu-id="be289-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="be289-131">Standardregler for kostgodtgjørelse:</span><span class="sxs-lookup"><span data-stu-id="be289-131">Default per diem rules:</span></span>

    - <span data-ttu-id="be289-132">Er det en prosentvis reduksjon i kostgodtgjørelsen for hvert måltid, hvis måltidet for eksempel er gratis?</span><span class="sxs-lookup"><span data-stu-id="be289-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="be289-133">Hva det er en reduksjon, hva er reduksjonsprosenten for hvert måltid?</span><span class="sxs-lookup"><span data-stu-id="be289-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="be289-134">Beregnes måltidsreduksjonen per dag, per tur eller per antall måltider per dag?</span><span class="sxs-lookup"><span data-stu-id="be289-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="be289-135">Skal kostgodtgjørelsesbeløpene avrundes på vanlig måte eller rundes opp?</span><span class="sxs-lookup"><span data-stu-id="be289-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="be289-136">Er kostgodtgjørelsen beregnet i en 24-timers periode eller på en kalenderdag?</span><span class="sxs-lookup"><span data-stu-id="be289-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="be289-137">Kostgodtgjørelsesregler som er basert på sted:</span><span class="sxs-lookup"><span data-stu-id="be289-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="be289-138">Varierer kostgodtgjørelsessatser etter sted?</span><span class="sxs-lookup"><span data-stu-id="be289-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="be289-139">Hvilke steder er inkludert?</span><span class="sxs-lookup"><span data-stu-id="be289-139">What locations are included?</span></span>
    - <span data-ttu-id="be289-140">Hvis kostgodtgjørelsessatsene varierer i henhold til sted, hvilket prosentbeløp tilbys for følgende typer utgifter for hvert sted:</span><span class="sxs-lookup"><span data-stu-id="be289-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="be289-141">Måltider</span><span class="sxs-lookup"><span data-stu-id="be289-141">Meals</span></span>
        - <span data-ttu-id="be289-142">Hotell</span><span class="sxs-lookup"><span data-stu-id="be289-142">Hotel</span></span>
        - <span data-ttu-id="be289-143">Andre utgifter</span><span class="sxs-lookup"><span data-stu-id="be289-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="be289-144">Journaler og kontoer i Utgiftshåndtering</span><span class="sxs-lookup"><span data-stu-id="be289-144">Expense management journals and accounts</span></span>

<span data-ttu-id="be289-145">Utgiftshåndtering krever at du bruker flere journaler og kontoer.</span><span class="sxs-lookup"><span data-stu-id="be289-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="be289-146">Du må for eksempel avgjøre om den samme kontoen skal brukes til tvister om kontantforskudd og kredittkort.</span><span class="sxs-lookup"><span data-stu-id="be289-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="be289-147">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-147">**Decisions:**</span></span>

- <span data-ttu-id="be289-148">Hvilken hovedbokjournal bokføres godkjente reiseregninger i?</span><span class="sxs-lookup"><span data-stu-id="be289-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="be289-149">Hvilken konto brukes til forskudd?</span><span class="sxs-lookup"><span data-stu-id="be289-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="be289-150">Skal forskudd bli postert umiddelbart?</span><span class="sxs-lookup"><span data-stu-id="be289-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="be289-151">Betalingsmetoder</span><span class="sxs-lookup"><span data-stu-id="be289-151">Payment methods</span></span>

<span data-ttu-id="be289-152">Når du tillater at de ansatte kan påløpe utgifte på vegne av virksomheten, må du definere betalingsmetodene som de ansatte kan bruke.</span><span class="sxs-lookup"><span data-stu-id="be289-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="be289-153">Du kan for eksempel la de ansatte bruke kontanter eller et firmakredittkort.</span><span class="sxs-lookup"><span data-stu-id="be289-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="be289-154">Du kan også la de ansatte bruke personlige kredittkort og deretter refundere dem.</span><span class="sxs-lookup"><span data-stu-id="be289-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="be289-155">Du må ta følgende avgjørelser for hver betalingsmetode du tillater.</span><span class="sxs-lookup"><span data-stu-id="be289-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="be289-156">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-156">**Decisions:**</span></span>

- <span data-ttu-id="be289-157">Hvilke betalingsmetoder er tillatt?</span><span class="sxs-lookup"><span data-stu-id="be289-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="be289-158">Hvem eier utgiftene for betalingsmetoden?</span><span class="sxs-lookup"><span data-stu-id="be289-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="be289-159">Er det en motkontotype?</span><span class="sxs-lookup"><span data-stu-id="be289-159">Is there an offset account type?</span></span> <span data-ttu-id="be289-160">Hvis det er en motkontotype, hva er den?</span><span class="sxs-lookup"><span data-stu-id="be289-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="be289-161">Hvis det er en motkonto, hva er kontoen?</span><span class="sxs-lookup"><span data-stu-id="be289-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="be289-162">Hvis betalingsmetoden er et kredittkort, skal betalingsmetoden bare brukes med importerte transaksjoner?</span><span class="sxs-lookup"><span data-stu-id="be289-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="be289-163">Utgiftskategorier og delte kategorier</span><span class="sxs-lookup"><span data-stu-id="be289-163">Expense categories and shared categories</span></span>

<span data-ttu-id="be289-164">Når ansatte oppretter reiseregninger, må hver utgift som de registrerer, tilknyttes en utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="be289-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="be289-165">Utgiftskategorier er avledet fra delte kategorier som kan deles på tvers av de juridiske enhetene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="be289-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="be289-166">Disse kategoriene kan også deles i prosjektstyring og -regnskap, avhengig av hvilken måte organisasjonen er definert på.</span><span class="sxs-lookup"><span data-stu-id="be289-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="be289-167">Basert på definisjonen av organisasjonen og veiledning fra implementeringsteamet må du bestemme om kategoriene som brukes i utgiftshåndtering, bare skal brukes i utgiftshåndtering, eller om de skal deles mellom prosjektstyring og -regnskap og utgiftshåndtering.</span><span class="sxs-lookup"><span data-stu-id="be289-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="be289-168">Legg merke til at disse kategoriene kan deles mellom prosjekt og utgift eller prosjekt og produksjon, men ikke mellom utgift og produksjon.</span><span class="sxs-lookup"><span data-stu-id="be289-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="be289-169">Du må ta følgende avgjørelser for hver utgiftskategori.</span><span class="sxs-lookup"><span data-stu-id="be289-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="be289-170">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-170">**Decisions:**</span></span>

- <span data-ttu-id="be289-171">Hva er utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-171">What is the expense category?</span></span> <span data-ttu-id="be289-172">Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.</span><span class="sxs-lookup"><span data-stu-id="be289-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="be289-173">Kan utgiftskategorien også brukes til prosjektstyring og regnskap?</span><span class="sxs-lookup"><span data-stu-id="be289-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="be289-174">Hva er utgiftstypen?</span><span class="sxs-lookup"><span data-stu-id="be289-174">What is the expense type?</span></span>
- <span data-ttu-id="be289-175">Hva er standard betalingsmetode for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="be289-176">Må utgifter i utgiftskategorien være spesifiserte?</span><span class="sxs-lookup"><span data-stu-id="be289-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="be289-177">Hva er standard hovedkonto for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="be289-178">Hva er standard mva-gruppe for varesalg for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="be289-179">Er det tillatt med flere betalingsmetoder for utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="be289-180">Hvis flere betalingsmetoder er tillatt, hvilke i så fall?</span><span class="sxs-lookup"><span data-stu-id="be289-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="be289-181">Finnes det underkategorier i utgiftskategorien?</span><span class="sxs-lookup"><span data-stu-id="be289-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="be289-182">Hvis det finnes underkategorier, må du også ta følgende beslutninger:</span><span class="sxs-lookup"><span data-stu-id="be289-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="be289-183">Er noen av underkategoriene utelukket fra avgiftsfradrag?</span><span class="sxs-lookup"><span data-stu-id="be289-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="be289-184">Hva er mva-gruppen for varesalg for underkategoriene?</span><span class="sxs-lookup"><span data-stu-id="be289-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="be289-185">Hvis utgiftskategorien også brukes i Prosjektstyring og regnskap, må du svare på de gjenstående spørsmålene.</span><span class="sxs-lookup"><span data-stu-id="be289-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="be289-186">Hvis ikke, gå videre til neste del.</span><span class="sxs-lookup"><span data-stu-id="be289-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="be289-187">Hvilke kostnadskontoer skal brukes til følgende utgifter?</span><span class="sxs-lookup"><span data-stu-id="be289-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="be289-188">Kostnad</span><span class="sxs-lookup"><span data-stu-id="be289-188">Cost</span></span>
    - <span data-ttu-id="be289-189">Lønnstildeling</span><span class="sxs-lookup"><span data-stu-id="be289-189">Payroll allocation</span></span>
    - <span data-ttu-id="be289-190">VIA – kostverdi</span><span class="sxs-lookup"><span data-stu-id="be289-190">WIP-cost value</span></span>
    - <span data-ttu-id="be289-191">Kostnadselement</span><span class="sxs-lookup"><span data-stu-id="be289-191">Cost-item</span></span>
    - <span data-ttu-id="be289-192">VIA-kostnadsverdielement</span><span class="sxs-lookup"><span data-stu-id="be289-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="be289-193">Påløpt tap</span><span class="sxs-lookup"><span data-stu-id="be289-193">Accrued loss</span></span>
    - <span data-ttu-id="be289-194">VIA – påløpt tap</span><span class="sxs-lookup"><span data-stu-id="be289-194">WIP-accrued loss</span></span>

- <span data-ttu-id="be289-195">Hvilke inntektskontoer skal brukes til følgende?</span><span class="sxs-lookup"><span data-stu-id="be289-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="be289-196">Fakturert omsetning</span><span class="sxs-lookup"><span data-stu-id="be289-196">Invoiced revenue</span></span>
    - <span data-ttu-id="be289-197">Påløpt omsetning – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="be289-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="be289-198">VIA – Salgsverdi</span><span class="sxs-lookup"><span data-stu-id="be289-198">WIP-sales value</span></span>
    - <span data-ttu-id="be289-199">Påløpt omsetning – produksjon</span><span class="sxs-lookup"><span data-stu-id="be289-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="be289-200">VIA – produksjon</span><span class="sxs-lookup"><span data-stu-id="be289-200">WIP-production</span></span>
    - <span data-ttu-id="be289-201">Påløpt omsetning – fortjeneste</span><span class="sxs-lookup"><span data-stu-id="be289-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="be289-202">VIA – fortjeneste</span><span class="sxs-lookup"><span data-stu-id="be289-202">WIP-profit</span></span>
    - <span data-ttu-id="be289-203">Påløpt omsetning – abonnement</span><span class="sxs-lookup"><span data-stu-id="be289-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="be289-204">VIA – abonnement</span><span class="sxs-lookup"><span data-stu-id="be289-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="be289-205">Avgifter</span><span class="sxs-lookup"><span data-stu-id="be289-205">Taxes</span></span>

<span data-ttu-id="be289-206">Når det gjelder utgiftsrelaterte avgifter, må du bestemme hva som er inkludert i eller aktivert i reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="be289-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="be289-207">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-207">**Decisions:**</span></span>

- <span data-ttu-id="be289-208">Er merverdiavgift inkludert i utgiftsbeløpene?</span><span class="sxs-lookup"><span data-stu-id="be289-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="be289-209">Skal avgiftsfradrag aktiveres for utgifter?</span><span class="sxs-lookup"><span data-stu-id="be289-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="be289-210">Hvis du bestemte deg for å bruke amerikanske regler for mva og skatt da du planla hovedboken, kan du ikke aktivere avgiftsfradrag for utgifter.</span><span class="sxs-lookup"><span data-stu-id="be289-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="be289-211">(Hvis du vil bruke amerikanske regler for merverdiavgift og skatt, setter du alternativet **Bruk skatteregler for mva** til **Ja**.)</span><span class="sxs-lookup"><span data-stu-id="be289-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="be289-212">Policyer</span><span class="sxs-lookup"><span data-stu-id="be289-212">Policies</span></span>

<span data-ttu-id="be289-213">Ved å opprette reise regningspolicyer kan du bidra til at organisasjonen sparer tid og penger når de ansatte påløper utgifter på vegne av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="be289-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="be289-214">Policyer hjelper deg med å sørge for at de ansatte holde seg til budsjettet, oppgir all nødvendig informasjon og bruker penger bare når det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="be289-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="be289-215">Du må ta følgende avgjørelser for hver reiseregningspolicy og hver godkjenningspolicy for reiseregninger som du oppretter.</span><span class="sxs-lookup"><span data-stu-id="be289-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="be289-216">**Beslutninger:**</span><span class="sxs-lookup"><span data-stu-id="be289-216">**Decisions:**</span></span>

- <span data-ttu-id="be289-217">Hva er navnet på policyen?</span><span class="sxs-lookup"><span data-stu-id="be289-217">What is the name of the policy?</span></span>
- <span data-ttu-id="be289-218">Hva er utgiftspolicyen for?</span><span class="sxs-lookup"><span data-stu-id="be289-218">What is the expense policy for?</span></span>
- <span data-ttu-id="be289-219">Hvis du tidligere har bestemt deg for å aktivere konserninterne utgifter, hvilke selskaper i organisasjonen vil denne policyen gjelde for?</span><span class="sxs-lookup"><span data-stu-id="be289-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="be289-220">Når blir policyen effektiv?</span><span class="sxs-lookup"><span data-stu-id="be289-220">When does the policy become effective?</span></span>
- <span data-ttu-id="be289-221">Når utløper policyen?</span><span class="sxs-lookup"><span data-stu-id="be289-221">When does the policy expire?</span></span>
- <span data-ttu-id="be289-222">Hva er policyregelen?</span><span class="sxs-lookup"><span data-stu-id="be289-222">What is the policy rule?</span></span>
- <span data-ttu-id="be289-223">Hva er resultatet av policyregelen?</span><span class="sxs-lookup"><span data-stu-id="be289-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]