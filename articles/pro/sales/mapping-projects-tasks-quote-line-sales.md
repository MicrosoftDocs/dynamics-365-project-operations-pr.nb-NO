---
title: Tilordne prosjekter og oppgaver til en prosjektbasert tilbudslinje
description: Dette emnet gir informasjon om hvordan du tilordner prosjekter og oppgaver til en prosjektbasert oppgavelinje.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 871d323136cd982bd48ed9aa2b9c34017951d2d8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130725"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="65480-103">Tilordne prosjekter og oppgaver til en prosjektbasert tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="65480-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="65480-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="65480-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="65480-105">På prosjektbaserte tilbudslinjer kan du tilordne de spesifikke oppgavene til et prosjekt som allerede er knyttet til en tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="65480-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="65480-106">Når du tilordner oppgaver til en tilbudslinje, vil følgende elementer du har definert i tilbudslinjen, bare gjelde for disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="65480-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="65480-107">Faktureringsmetode</span><span class="sxs-lookup"><span data-stu-id="65480-107">Billing method</span></span>
- <span data-ttu-id="65480-108">Alternativer for belastbarhet</span><span class="sxs-lookup"><span data-stu-id="65480-108">Chargeability options</span></span>
- <span data-ttu-id="65480-109">Må ikke overskrides-grenser</span><span class="sxs-lookup"><span data-stu-id="65480-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="65480-110">Kunder</span><span class="sxs-lookup"><span data-stu-id="65480-110">Customers</span></span>

<span data-ttu-id="65480-111">Du kan for eksempel ha et prosjekt der én fase er en fast pris, og alle de andre fasene er tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="65480-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="65480-112">I dette tilfellet kan du knytte den første fasen og alle underordnede oppgaver til tilbudslinjen for fasen med fast pris som faktureringsmetode.</span><span class="sxs-lookup"><span data-stu-id="65480-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="65480-113">Du kan deretter knytte alle de andre fasene til tilbudslinjen som er basert på tid og materialer.</span><span class="sxs-lookup"><span data-stu-id="65480-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="65480-114">Knytte oppgaver til prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="65480-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="65480-115">Du kan knytte oppgaver til tilbudslinjer fra følgende plasseringer:</span><span class="sxs-lookup"><span data-stu-id="65480-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="65480-116">**Prosjekt**-siden > **Oppgavefakturering**-fanen (valgtritt)</span><span class="sxs-lookup"><span data-stu-id="65480-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="65480-117">**Tilbudslinje**-siden > **Belastbare oppgaver**-fanen</span><span class="sxs-lookup"><span data-stu-id="65480-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="65480-118">Fra prosjektsiden</span><span class="sxs-lookup"><span data-stu-id="65480-118">From the Project page</span></span>

<span data-ttu-id="65480-119">**Prosjekt**-siden gir den optimale opplevelsen for tilordning av oppgaver til tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="65480-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="65480-120">Du kan bruke denne siden til å velge flere oppgaver og knytte til alle disse, samt underordnede oppgaver, til den valgte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="65480-121">I kategorien **Generelt** for en prosjektbasert tilbudslinje, kontrollerer du at **Prosjekt**-feltet er fylt ut.</span><span class="sxs-lookup"><span data-stu-id="65480-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="65480-122">I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="65480-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="65480-123">Lagre den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-123">Save the project-based quote line.</span></span> <span data-ttu-id="65480-124">Når skjemaet oppdateres, vises kategorien **Belastbare oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="65480-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="65480-125">I kategorien **Generelt** velger du koblingen for prosjektet fra **Prosjekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="65480-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="65480-126">På siden **Prosjekr** velger du kategorien **Oppgavefakturering**.</span><span class="sxs-lookup"><span data-stu-id="65480-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="65480-127">I det andre rutenettet, som gjelder for oppgavespesifikke faktureringsoppsett, velger du én eller flere oppgaver, og deretter velger du **Tilknytt tilbudslinjer**.</span><span class="sxs-lookup"><span data-stu-id="65480-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="65480-128">På dialogsiden som vises, velger du en tilbudslinje som viser prosjektbaserte tilbudslinjer i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="65480-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="65480-129">I feltet **Faktureringstype** angir du om disse oppgavene er belastbare eller ikke-belastbare.</span><span class="sxs-lookup"><span data-stu-id="65480-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="65480-130">Merk av i avmerkingsboksen for å angi om tilknytningen skal inkludere underordnede oppgaver for de valgte oppgavene.</span><span class="sxs-lookup"><span data-stu-id="65480-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="65480-131">Hvis du merker av i boksen, knyttes underordnede oppgaver for de valgte oppgavene til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="65480-132">Velg **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="65480-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="65480-133">Fra tilbudslinjesiden</span><span class="sxs-lookup"><span data-stu-id="65480-133">From the Quote line page</span></span>

<span data-ttu-id="65480-134">Du kan knytte prosjektoppgaver til tilbudslinjer fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden.</span><span class="sxs-lookup"><span data-stu-id="65480-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="65480-135">Det optimale stedet for å knytte prosjektoppgaver til tilbudslinjer er på **Oppgavefakturering**-fanen på **Prosjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="65480-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="65480-136">Hvis du knytter oppgaver fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden, må du knytte til hvert prosjekt manuelt.</span><span class="sxs-lookup"><span data-stu-id="65480-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="65480-137">I kategorien **Generelt** for en prosjektbasert tilbudslinje, kontrollerer du at et prosjekt er valgt i **Prosjekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="65480-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="65480-138">I feltet **Inkluderte oppgaver** velger du **Bare valgte oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="65480-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="65480-139">Lagre den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-139">Save the project-based quote line.</span></span> <span data-ttu-id="65480-140">Når skjemaet oppdateres, vises kategorien **Belastbare oppgaver**.</span><span class="sxs-lookup"><span data-stu-id="65480-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="65480-141">I kategorien **Belastbare oppgaver** velger du **Legg til en tilbudslinjeoppgave**.</span><span class="sxs-lookup"><span data-stu-id="65480-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="65480-142">På siden **Tilbudslinjeoppgave**, i **Oppgaver**-feltet velger du oppgaven, og i **Faktureringstype**-feltet velger du **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="65480-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="65480-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65480-143">Close the page.</span></span> <span data-ttu-id="65480-144">Den valgte oppgaven er nå knyttet til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="65480-145">Oppheve tilknytning av oppgaver fra prosjektbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="65480-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="65480-146">Fra prosjektsiden</span><span class="sxs-lookup"><span data-stu-id="65480-146">From the Project page</span></span>

<span data-ttu-id="65480-147">Denne metoden gir den mest optimale opplevelsen for oppheving av tilknytning av oppgaver fra tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="65480-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="65480-148">Du kan velge flere oppgaver og oppheve tilknytningen for alle disse, samt underordnede oppgaver, fra den valgte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="65480-149">I kategorien **Generelt** for en prosjektbasert tilbudslinje velger du prosjektkoblingen i **Prosjekt**-feltet.</span><span class="sxs-lookup"><span data-stu-id="65480-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="65480-150">På siden **Prosjekr** velger du kategorien **Oppgavefakturering**.</span><span class="sxs-lookup"><span data-stu-id="65480-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="65480-151">I det andre rutenettet, som gjelder for oppgavespesifikke faktureringsoppsett, velger du én eller flere oppgaver, og deretter velger du **Opphev tilknytning av tilbudslinjer**.</span><span class="sxs-lookup"><span data-stu-id="65480-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="65480-152">På dialogsiden som vises, velger du en tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="65480-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="65480-153">Merk av i avmerkingsboksen for å angi om tilknytningen også skal fjernes fra underordnede oppgaver for de valgte oppgavene.</span><span class="sxs-lookup"><span data-stu-id="65480-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="65480-154">Hvis du merker av i boksen, oppheves også tilknytningen for underordnede oppgaver for de valgte oppgavene til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="65480-155">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65480-155">Select **OK**.</span></span> <span data-ttu-id="65480-156">Du får en advarselsmelding om at hvis du fjerner denne tilknytningen, kan eventuelle faktiske verdier som tidligere er registrert for oppgaven, tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="65480-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="65480-157">Velg **OK** for å fortsette og fjerne tilknytningen mellom oppgaven og den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="65480-158">Fra tilbudslinjesiden</span><span class="sxs-lookup"><span data-stu-id="65480-158">From the Quote line page</span></span>

<span data-ttu-id="65480-159">Du kan oppheve tilknytning av prosjektoppgaver til tilbudslinjer fra kategorien **Belastbare oppgaver** på **Tilbudslinje**-siden.</span><span class="sxs-lookup"><span data-stu-id="65480-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="65480-160">I kategorien **Belastbare oppgaver** velger du **Slett en tilbudslinjeoppgave**.</span><span class="sxs-lookup"><span data-stu-id="65480-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="65480-161">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65480-161">Select **OK**.</span></span> <span data-ttu-id="65480-162">Du får en advarselsmelding om at hvis du fjerner denne tilknytningen, kan eventuelle faktiske verdier som tidligere er registrert for oppgaven, tilbakeføres.</span><span class="sxs-lookup"><span data-stu-id="65480-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="65480-163">Velg **OK** for å fortsette og fjerne tilknytningen mellom oppgaven og den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="65480-164">Denne prosedyren sletter ikke oppgaven fra prosjektet.</span><span class="sxs-lookup"><span data-stu-id="65480-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="65480-165">Den fjerner bare oppgavetilknytningen fra den prosjektbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="65480-165">It only removes the task association from the project-based quote line.</span></span>
