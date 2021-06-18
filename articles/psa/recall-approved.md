---
title: Tilbakekalle godkjente tids- eller utgiftsoppføringer
description: Dette emnet gir informasjon om hvordan du tilbakekaller en tidligere godkjent prosjekttid eller utgiftstransaksjon.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998198"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="c79f0-103">Tilbakekalle godkjente tids- eller utgiftsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c79f0-103">Recall approved time or expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c79f0-104">Et prosjektteammedlem eller en annen person som sender en tids- eller utgiftsoppføring, kan tilbakekalle denne tids- eller utgiftsoppføringen etter at den er godkjent.</span><span class="sxs-lookup"><span data-stu-id="c79f0-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="c79f0-105">Prosessen for å tilbakekalle en godkjent tids- eller utgiftsoppføring har to trinn:</span><span class="sxs-lookup"><span data-stu-id="c79f0-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="c79f0-106">En sender ber om en tilbakekalling.</span><span class="sxs-lookup"><span data-stu-id="c79f0-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="c79f0-107">En godkjenner godkjenner tilbakekallingen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="c79f0-108">Be om tilbakekalling</span><span class="sxs-lookup"><span data-stu-id="c79f0-108">Request a recall</span></span>

<span data-ttu-id="c79f0-109">Følg disse trinnene for å be om tilbakekalling av en godkjent tids- eller utgiftsoppføring.</span><span class="sxs-lookup"><span data-stu-id="c79f0-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="c79f0-110">For tidsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="c79f0-111">–eller–</span><span class="sxs-lookup"><span data-stu-id="c79f0-111">–or–</span></span>

    <span data-ttu-id="c79f0-112">For utgiftsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Utgifter**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="c79f0-113">For tidsoppføringer velger du alle tidsoppføringer for en bestemt kombinasjon av et prosjekt og en oppgave.</span><span class="sxs-lookup"><span data-stu-id="c79f0-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="c79f0-114">Du kan også merke enkeltcellene for tid på en bestemt dato for et bestemt prosjekt i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="c79f0-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="c79f0-115">–eller–</span><span class="sxs-lookup"><span data-stu-id="c79f0-115">–or–</span></span>

    <span data-ttu-id="c79f0-116">For utgiftsoppføringer velger du raden for utgiftsoppføringen som skal tilbakekalles.</span><span class="sxs-lookup"><span data-stu-id="c79f0-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="c79f0-117">Velg **Tilbakekall**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-117">Select **Recall**.</span></span> <span data-ttu-id="c79f0-118">En bekreftelsesdialogboks vises.</span><span class="sxs-lookup"><span data-stu-id="c79f0-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="c79f0-119">Hvis de valgte tids- og utgiftsoppføringene allerede er godkjent, blir du bedt om å angi en årsak til tilbakekallingen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="c79f0-120">Angi en årsak til tilbakekallingen, og velg deretter **OK** for å bekrefte operasjonen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="c79f0-121">Systemet sender personen som godkjente oppføringene, en forespørsel om å godkjenne tilbakekallingen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="c79f0-122">Selv om godkjente tids- og utgiftsoppføringer kan tilbakekalles, kan ikke en tilbakekallingsforespørsel opprettes hvis et godkjent tid eller utgifts allerede er fakturert til kunden.</span><span class="sxs-lookup"><span data-stu-id="c79f0-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="c79f0-123">En bruker som prøver å opprette en tilbakekallingsforespørsel, mottar en melding som angir at tiden eller utgiften ikke kan kalles tilbake fordi den allerede er fakturert.</span><span class="sxs-lookup"><span data-stu-id="c79f0-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="c79f0-124">Godkjenne eller avvise en tilbakekallingsforespørsel</span><span class="sxs-lookup"><span data-stu-id="c79f0-124">Approve or reject a recall request</span></span>

<span data-ttu-id="c79f0-125">Følg denne fremgangsmåten for å godkjenne eller avvise en tilbakekallingsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="c79f0-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="c79f0-126">Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="c79f0-127">På listesiden **Godkjenninger** endrer du visningen til **Tilbakekallingsforespørsler å godkjenne**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="c79f0-128">Det vises en liste over sendte forespørsler om tilbakekalling.</span><span class="sxs-lookup"><span data-stu-id="c79f0-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="c79f0-129">Velg én eller flere oppføringer, og velg deretter **Godkjenn** eller **Avvis**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="c79f0-130">Hvis du valgte **Godkjenn**, får du en advarsel som forklarer innvirkningen av godkjenningen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="c79f0-131">Velg **OK** for å bekrefte handlingen.</span><span class="sxs-lookup"><span data-stu-id="c79f0-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="c79f0-132">Tilbakekallingsforespørselen godkjennes.</span><span class="sxs-lookup"><span data-stu-id="c79f0-132">The recall request is approved.</span></span>

    <span data-ttu-id="c79f0-133">–eller–</span><span class="sxs-lookup"><span data-stu-id="c79f0-133">–or–</span></span>

    <span data-ttu-id="c79f0-134">Hvis du valgte **Avvis**, blir tilbakekallingsforespørselen avvist.</span><span class="sxs-lookup"><span data-stu-id="c79f0-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="c79f0-135">Når en tilbakekalling blir forespurt, når en tilbakekalling blir godkjent, ser systemet etter eventuell fakturaaktivitet på tids- eller utgiftsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="c79f0-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="c79f0-136">Hvis en oppføring allerede er fakturert, eller hvis den er på et fakturautkast, mottar godkjenneren en feilmelding som sier at tiden eller utgiften ikke kan godkjennes for tilbakekalling fordi den allerede er fakturert.</span><span class="sxs-lookup"><span data-stu-id="c79f0-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="c79f0-137">Innvirkning av en tilbakekallingsforespørsel</span><span class="sxs-lookup"><span data-stu-id="c79f0-137">Impact of a recall request</span></span>

<span data-ttu-id="c79f0-138">Når en godkjenning tilbakekalles, får dette både driftsinnvirkning og finansiell innvirkning.</span><span class="sxs-lookup"><span data-stu-id="c79f0-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="c79f0-139">Driftsinnvirkning</span><span class="sxs-lookup"><span data-stu-id="c79f0-139">Operational impact</span></span>

<span data-ttu-id="c79f0-140">Hvis en tilbakekallingsforespørsel godkjennes, merkes godkjenningsoppføringen som **Avvist**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="c79f0-141">Statusen for oppføringen endres til enten **Returnert** eller **Avvist**, avhengig av om det er en tidsoppføring eller en utgiftsoppføring.</span><span class="sxs-lookup"><span data-stu-id="c79f0-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="c79f0-142">Prosjektteammedlemmet kan vise oppføringer, redigere og sende oppføringer på nytt, eller slette oppføringer helt.</span><span class="sxs-lookup"><span data-stu-id="c79f0-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="c79f0-143">Hvis en tilbakekallingsforespørsel blir avvist, blir statusen for oppføringen fortsatt **Godkjent**, og oppføringen kan ikke redigeres av prosjektteammedlemmet eller godkjenneren for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c79f0-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="c79f0-144">Økonomisk innvirkning</span><span class="sxs-lookup"><span data-stu-id="c79f0-144">Financial impact</span></span>

<span data-ttu-id="c79f0-145">Hvis en tilbakekallingsforespørsel godkjennes, oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="c79f0-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="c79f0-146">Feltet **Justeringsstatus** oppdateres til **Justert**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="c79f0-147">Feltet **Faktureringsstatus** oppdateres til **Kansellert**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="c79f0-148">Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="c79f0-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="c79f0-149">For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene.</span><span class="sxs-lookup"><span data-stu-id="c79f0-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="c79f0-150">De eneste verdiene som ikke kopieres over, er antallsverdiene.</span><span class="sxs-lookup"><span data-stu-id="c79f0-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="c79f0-151">Disse verdiene reverseres i stedet.</span><span class="sxs-lookup"><span data-stu-id="c79f0-151">These values are reversed instead.</span></span> <span data-ttu-id="c79f0-152">Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="c79f0-153">Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres**, og feltet **Faktureringsstatus** settes til **Annullert**.</span><span class="sxs-lookup"><span data-stu-id="c79f0-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="c79f0-154">På grunn av disse endringene vil det registrerte forbruket og restinntekten for prosjektet ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.</span><span class="sxs-lookup"><span data-stu-id="c79f0-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="c79f0-155">Hvis en tilbakekallingsforespørsel blir avvist, er det ingen økonomisk innvirkning på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="c79f0-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="c79f0-156">Endringer i tidsregistreringsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c79f0-156">Changes to time entry records</span></span>

<span data-ttu-id="c79f0-157">Illustrasjonen nedenfor viser endringene som utføres for godkjente tidsoppføringer når de tilbakekalles.</span><span class="sxs-lookup"><span data-stu-id="c79f0-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Overganger for tidsoppføringstilstand](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="c79f0-159">Endringer i utgiftsregistreringsoppføringer</span><span class="sxs-lookup"><span data-stu-id="c79f0-159">Changes to expense entry records</span></span>

<span data-ttu-id="c79f0-160">Illustrasjonen nedenfor viser endringene som utføres for godkjente utgiftsoppføringer når de tilbakekalles.</span><span class="sxs-lookup"><span data-stu-id="c79f0-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Overganger for utgiftsoppføringstilstand](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]