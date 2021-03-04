---
title: Behandling av utgiftskvittering
description: Dette emnet gir informasjon om optisk tegngjenkjenning (OCR) for kvitteringer. Denne funksjonen er utformet for å forbedre brukeropplevelsen når reiseregninger opprettes i Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 64901610144f9dfe274bd4c2294ab32659743a1a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960304"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="23ccb-104">Behandling av utgiftskvittering</span><span class="sxs-lookup"><span data-stu-id="23ccb-104">Expense receipt processing</span></span>

<span data-ttu-id="23ccb-105">Utgiftsregistrering er forbedret gjennom innføringen av optisk tegngjenkjenning (OCR) for kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="23ccb-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="23ccb-106">Denne funksjonen er utformet for å forbedre brukeropplevelsen når reiseregninger opprettes.</span><span class="sxs-lookup"><span data-stu-id="23ccb-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="23ccb-107">Nøkkelfunksjoner</span><span class="sxs-lookup"><span data-stu-id="23ccb-107">Key features</span></span>

- <span data-ttu-id="23ccb-108">Forhandlernavn, dato og totalt beløp hentes ut fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="23ccb-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="23ccb-109">Funksjonen prøver å samsvare ikke-tilknyttede mottak med ikke-tilknyttede utgiftstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="23ccb-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="23ccb-110">Brukerne kan opprette manuelt angitte utgiftstransaksjoner fra kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="23ccb-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="23ccb-111">Eksempler på bruk</span><span class="sxs-lookup"><span data-stu-id="23ccb-111">Usage examples</span></span>

<span data-ttu-id="23ccb-112">Hvis du automatisk vil legge ved kvitteringer som inkluderer kredittkorttransaksjoner når en reiseregning opprettes, kan du gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="23ccb-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="23ccb-113">Åpne arbeidsområdet **Utgiftshåndtering**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="23ccb-114">I kategorien **Kvitteringer** kontrollerer du at det finnes ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="23ccb-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="23ccb-115">Du kan også laste opp kvitteringer i kategorien **Kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="23ccb-116">I kategorien **Utgifter** kontrollerer du at det finnes ikke-tilknyttede utgifter.</span><span class="sxs-lookup"><span data-stu-id="23ccb-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="23ccb-117">Vanligvis importerer utgiftsadministrator disse utgiftene fra kredittkortleverandøren.</span><span class="sxs-lookup"><span data-stu-id="23ccb-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="23ccb-118">Velg **Ny reiseregning**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-118">Select **New expense report**.</span></span> <span data-ttu-id="23ccb-119">Legg merke til at du kan ta med utgifter og nå også kvitteringer når du oppretter en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="23ccb-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="23ccb-120">Hvis du legger til både utgifter og kvitteringer, utløses automatisk avstemming av kvitteringene mot utgiftene.</span><span class="sxs-lookup"><span data-stu-id="23ccb-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="23ccb-121">Gjør følgende for å opprette en utgift eller samsvare en utgift fra en kvittering:</span><span class="sxs-lookup"><span data-stu-id="23ccb-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="23ccb-122">Legg ved en kvittering i en reiseregning ved å velge kategorien **Kvitteringer** og deretter **Legg til kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="23ccb-123">Under det opplastede bildet av kvitteringen legger du merke til alternativene **Opprett** og **Samsvar**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="23ccb-124">Velg **Opprett** for å opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som trekkes ut fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="23ccb-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="23ccb-125">Hvis du velger **Samsvar**, prøver systemet å samsvare en eksisterende utgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="23ccb-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="23ccb-126">Installasjon</span><span class="sxs-lookup"><span data-stu-id="23ccb-126">Installation</span></span>

<span data-ttu-id="23ccb-127">Denne funksjonen fungerer sammen med funksjonen **Nyskapte utgiftsrapporter**, noe som forenkler utgiftsopplevelsen.</span><span class="sxs-lookup"><span data-stu-id="23ccb-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="23ccb-128">Denne funksjonen er bare tilgjengelig for nivå 2+-miljøer, som er sandkasse og produksjon.</span><span class="sxs-lookup"><span data-stu-id="23ccb-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="23ccb-129">Hvis du vil bruke disse avanserte utgiftsfunksjonene, installerer du tilleggsprogrammet for reiseregning og utlegg for Microsoft Dynamics 365 Finance, og deretter aktiverer du funksjonene i forekomsten.</span><span class="sxs-lookup"><span data-stu-id="23ccb-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="23ccb-130">Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="23ccb-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="23ccb-131">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="23ccb-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="23ccb-132">Gå til **Detaljert informasjon**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="23ccb-133">Velg **Vedlikehold**, eller rull ned til hurtigfanen **Tilleggsprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="23ccb-134">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="23ccb-135">Velg **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="23ccb-136">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="23ccb-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="23ccb-137">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-137">Select **Install**.</span></span>

<span data-ttu-id="23ccb-138">Aktiver følgende funksjoner i arbeidsområdet **Funksjonsbehandling**:</span><span class="sxs-lookup"><span data-stu-id="23ccb-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="23ccb-139">Nyskapte utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="23ccb-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="23ccb-140">Automatisk samsvar og opprette utgift fra kvittering</span><span class="sxs-lookup"><span data-stu-id="23ccb-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="23ccb-141">Når du aktiverer disse funksjonene, oppstår følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="23ccb-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="23ccb-142">Det eksisterende arbeidsområdet for **utgiftshåndtering** erstattes av det nye arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="23ccb-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="23ccb-143">Det legges til et nytt menyelement for synlighet for utgiftsfelt.</span><span class="sxs-lookup"><span data-stu-id="23ccb-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="23ccb-144">Du kan fremdeles åpne siden for de tidligere **reiseregningene** ved å gå til **Utgiftshåndtering > Mine utgifter > Reiseregninger**.</span><span class="sxs-lookup"><span data-stu-id="23ccb-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="23ccb-145">Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.</span><span class="sxs-lookup"><span data-stu-id="23ccb-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="23ccb-146">Kvitteringer blir behandlet gjennom Microsoft Azure Cognitive Services, og metadata blir trukket ut og lagt til.</span><span class="sxs-lookup"><span data-stu-id="23ccb-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="23ccb-147">Det legges til et alternativ som du kan bruke til å opprette en reiseregning som inkluderer samsvarte, ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="23ccb-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="23ccb-148">Ved hjelp av et alternativ som legges til i reiseregninger, kan du opprette en utgiftslinje fra en kvittering, eller forsøk på å samsvare en eksisterende kvittering med en eksisterende utgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="23ccb-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="23ccb-149">Hvis du vil ha mer informasjon om funksjonen Nyskapte utgiftsrapporter, kan du se [Nyskapte utgiftsrapporter](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="23ccb-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="23ccb-150">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="23ccb-150">Frequently asked questions</span></span>

<span data-ttu-id="23ccb-151">**Bruker Microsoft dataene mine for modellene sine?**</span><span class="sxs-lookup"><span data-stu-id="23ccb-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="23ccb-152">Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for mottaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="23ccb-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="23ccb-153">Denne modellen er ikke basert på mottakene du laster opp.</span><span class="sxs-lookup"><span data-stu-id="23ccb-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="23ccb-154">**Hvor er denne funksjonen tilgjengelig og behandlet?**</span><span class="sxs-lookup"><span data-stu-id="23ccb-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="23ccb-155">USA støttes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="23ccb-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="23ccb-156">**Hvor havner kvitteringene mine?**</span><span class="sxs-lookup"><span data-stu-id="23ccb-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="23ccb-157">Økonomiavdelingen Cognitive Services for å trekke ut feltdataene.</span><span class="sxs-lookup"><span data-stu-id="23ccb-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="23ccb-158">Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandlingen utføres.</span><span class="sxs-lookup"><span data-stu-id="23ccb-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="23ccb-159">Når behandlingen er fullført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="23ccb-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="23ccb-160">Kvitteringer lagres fremdeles i økonomi.</span><span class="sxs-lookup"><span data-stu-id="23ccb-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="23ccb-161">Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonen i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="23ccb-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
