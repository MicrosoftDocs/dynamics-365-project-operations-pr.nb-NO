---
title: Opprette og bekrefte korrigeringsjournaler
description: Dette emnet gir informasjon om hvordan du oppretter og bekrefter en korrigeringsjournal.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996668"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="0234f-103">Opprette og bekrefte korrigeringsjournaler</span><span class="sxs-lookup"><span data-stu-id="0234f-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="0234f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0234f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0234f-105">Noen ganger kan en tids- eller utgiftsoppføring være angitt feil.</span><span class="sxs-lookup"><span data-stu-id="0234f-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="0234f-106">En konsulent kan for eksempel velge feil dato ved oppretting av en tidsoppføring, eller de kan transponere tallene ved angivelse av en utgift.</span><span class="sxs-lookup"><span data-stu-id="0234f-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="0234f-107">Hvis en konsulent ikke kan gjøre oppdateringene til de sendte oppføringene, kan en administrator direkte korrigere oppføringen for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="0234f-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="0234f-108">Hvis du vil fullføre fremgangsmåtene i dette emnet, må du ha administratortillatelser.</span><span class="sxs-lookup"><span data-stu-id="0234f-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="0234f-109">Korrigere godkjente tidsoppføringer</span><span class="sxs-lookup"><span data-stu-id="0234f-109">Correct approved time entries</span></span>     

<span data-ttu-id="0234f-110">Fullfør fremgangsmåten nedenfor for å rette én eller flere tidsoppføringer for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="0234f-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="0234f-111">I **Salg**-området velger du **Transaksjoner** og velger deretter **Godkjent tid**.</span><span class="sxs-lookup"><span data-stu-id="0234f-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="0234f-112">I listen **Godkjent tid** finner og velger du én eller flere godkjente tidsoppføringer som skal korrigeres.</span><span class="sxs-lookup"><span data-stu-id="0234f-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="0234f-113">Du kan bruke filteret til å finne relaterte oppføringer.</span><span class="sxs-lookup"><span data-stu-id="0234f-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="0234f-114">Du kan for eksempel filtrere på en prosjekt-ID og velge alle godkjente tidsoppføringer med denne prosjekt-ID-en.</span><span class="sxs-lookup"><span data-stu-id="0234f-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="0234f-115">Velg **Korriger oppføringer**.</span><span class="sxs-lookup"><span data-stu-id="0234f-115">Select **Correct entries**.</span></span> <span data-ttu-id="0234f-116">En ny korrigeringsjournal opprettes automatisk med den angitte typen **Tidskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="0234f-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="0234f-117">Oppføringene du har valgt, blir lagt til i journalen.</span><span class="sxs-lookup"><span data-stu-id="0234f-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="0234f-118">På siden **Ny journal** angir du en **beskrivelse** for korrigeringsjournalen, og deretter velger du kategorien **Korrigeringer for tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="0234f-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="0234f-119">I delen **Nye verdier for tidsoppføringer** oppdaterer du feltene med riktig informasjon etter behov.</span><span class="sxs-lookup"><span data-stu-id="0234f-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="0234f-120">Du kan for eksempel endre det tilordnede prosjektet eller en ressurs som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="0234f-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="0234f-121">Velg **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="0234f-121">Select **Preview**.</span></span> <span data-ttu-id="0234f-122">Velg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0234f-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="0234f-123">I kategorien **Journallinjer** kan du vise en liste over de opprinnelige faktiske verdiene som er relatert til de valgte tidsoppføringene som er tilbakeført, og de korrigerte tilsvarende linjene som er blitt opprettet.</span><span class="sxs-lookup"><span data-stu-id="0234f-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="0234f-124">Hvis det skal utføres flere rettelser, gjentar du trinn 5 og 6.</span><span class="sxs-lookup"><span data-stu-id="0234f-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="0234f-125">Alle de korrigerte faktiske verdiene vil ha samme verdier som du har valgt i delen **Nye verdier for tidsoppføringer**.</span><span class="sxs-lookup"><span data-stu-id="0234f-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="0234f-126">Hvis korrigeringene vises som forventet, velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="0234f-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="0234f-127">Velg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0234f-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="0234f-128">Gå tilbake til **Salg**-området, velg **Prosjekter**, og åpne deretter prosjektet som du akkurat oppdaterte tidsoppføringene for.</span><span class="sxs-lookup"><span data-stu-id="0234f-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="0234f-129">På **Prosjekter**-siden i kategorien **Faktiske verdier** kan du vise endringene du har utført.</span><span class="sxs-lookup"><span data-stu-id="0234f-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="0234f-130">Hvis kategorien **Faktiske verdier** ikke vises, velger du **Relatert** > **Faktiske verdier**.</span><span class="sxs-lookup"><span data-stu-id="0234f-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="0234f-131">I listen **Tilknyttet visning for faktiske data** kan du se at de opprinnelige tidsoppføringene som er tilbakeført, fremdeles er oppført, og dette gjelder også for de tilsvarende korrigerte tidsoppføringene.</span><span class="sxs-lookup"><span data-stu-id="0234f-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="0234f-132">I følgende grafikk er det for eksempel to linjeelementer med et antall på 8,00 som har debiteringer oppført i Beløp-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="0234f-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="0234f-133">I tillegg finnes det to linjeelementer med et antall på -8,00 som viser krediterte beløp i Beløp-kolonnen.</span><span class="sxs-lookup"><span data-stu-id="0234f-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="0234f-134">Disse korrigeringene får antallet til å bli null.</span><span class="sxs-lookup"><span data-stu-id="0234f-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="0234f-135">Korrigere godkjente utgiftsoppføringer</span><span class="sxs-lookup"><span data-stu-id="0234f-135">Correct approved expense entries</span></span>

<span data-ttu-id="0234f-136">Fullfør fremgangsmåten nedenfor for å korrigere én eller flere utgiftsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="0234f-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="0234f-137">I **Salg**-området, i den venstre navigasjonsruten, under **Transaksjoner**, velger du **Godkjente utgifter**.</span><span class="sxs-lookup"><span data-stu-id="0234f-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="0234f-138">I listen **Godkjente utgifter** velger du prosjektet du vil korrigere, og deretter velger du **Korriger oppføringer**.</span><span class="sxs-lookup"><span data-stu-id="0234f-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="0234f-139">En ny korrigeringsjournal opprettes automatisk med den angitte typen **Utgiftskorrigering**.</span><span class="sxs-lookup"><span data-stu-id="0234f-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="0234f-140">På siden **Ny journal** skriver du en **beskrivelse** for korrigeringen, og i kategorien **Utgiftskorrigering**, i delen **Nye verdier for utgifter** velger du datafeltene du vil korrigere for de valgte utgiftslinjene.</span><span class="sxs-lookup"><span data-stu-id="0234f-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="0234f-141">Du kan for eksempel tilordne utgiften til et annet **prosjekt** eller korrigere verdiene for **Utgiftskategori**, **Utgiftsdato** eller **Ressurs som kan reserveres**.</span><span class="sxs-lookup"><span data-stu-id="0234f-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="0234f-142">Velg **Forhåndsvisning**.</span><span class="sxs-lookup"><span data-stu-id="0234f-142">Select **Preview**.</span></span> <span data-ttu-id="0234f-143">Velg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0234f-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="0234f-144">Verifiser korrigeringene i kategorien **Journallinjer**. Du kan vise en liste over de opprinnelige faktiske verdiene som er relatert til de valgte utgiftsoppføringene som er tilbakeført, og de korrigerte tilsvarende linjene som er blitt opprettet.</span><span class="sxs-lookup"><span data-stu-id="0234f-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="0234f-145">Hvis de korrigerte verdiene er som forventet, velger du **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="0234f-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="0234f-146">Velg **OK** i dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0234f-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="0234f-147">Hvis verdiene ikke vises som forventet, velger du **Avbryt** for å gå tilbake til listen **Godkjente utgifter**.</span><span class="sxs-lookup"><span data-stu-id="0234f-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="0234f-148">Gjenta trinn 2 til 5.</span><span class="sxs-lookup"><span data-stu-id="0234f-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="0234f-149">De korrigerte faktiske verdiene vil ha samme verdier som du har valgt i delen **Nye verdier for utgifter**.</span><span class="sxs-lookup"><span data-stu-id="0234f-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="0234f-150">Etter at du har bekreftet korrigeringsjournalen, navigerer du tilbake til prosjektet eller prosjektene du oppdaterte, for å vise endringene.</span><span class="sxs-lookup"><span data-stu-id="0234f-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="0234f-151">På prosjektsiden, i kategorien **Faktiske verdier**, går du gjennom **Tilknyttet visning for faktiske data**.</span><span class="sxs-lookup"><span data-stu-id="0234f-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="0234f-152">De opprinnelige oppføringene og de korrigerte oppføringene vises.</span><span class="sxs-lookup"><span data-stu-id="0234f-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="0234f-153">Følgende grafikk viser opprinnelige utgiftsoppføringsbeløp og tilhørende korrigerte utgiftsoppføringsbeløp.</span><span class="sxs-lookup"><span data-stu-id="0234f-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]