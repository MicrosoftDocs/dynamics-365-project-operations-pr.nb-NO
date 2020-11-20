---
title: Samsvare et mottak med utgift ved hjelp av OCR (optisk tegngjenkjenning)
description: Dette emnet gir informasjon om optisk tegngjenkjenning (OCR) for kvitteringer.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 55f63c8c092942b73a55c9d86d867bca600f42e5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124335"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="2e000-103">Samsvare et mottak med utgift ved hjelp av OCR (optisk tegngjenkjenning)</span><span class="sxs-lookup"><span data-stu-id="2e000-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="2e000-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="2e000-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2e000-105">Utgiftsregistrering er forbedret gjennom innføringen av optisk tegngjenkjenning (OCR) for kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="2e000-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="2e000-106">Denne funksjonaliteten er utformet for å forbedre brukeropplevelsen ved opprettelse av reiseregninger.</span><span class="sxs-lookup"><span data-stu-id="2e000-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="2e000-107">Nøkkelfunksjoner</span><span class="sxs-lookup"><span data-stu-id="2e000-107">Key features</span></span>

- <span data-ttu-id="2e000-108">Systemet trekker ut forhandlernavn, dato og totalt beløp fra mottak.</span><span class="sxs-lookup"><span data-stu-id="2e000-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="2e000-109">Systemet prøver å samsvare ikke-tilknyttede mottak med ikke-tilknyttede utgiftstransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="2e000-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="2e000-110">Du kan opprette manuelt angitte utgiftstransaksjoner fra mottak.</span><span class="sxs-lookup"><span data-stu-id="2e000-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="2e000-111">Legge ved kvitteringer i en reiseregning</span><span class="sxs-lookup"><span data-stu-id="2e000-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="2e000-112">Hvis du automatisk vil legge ved kvitteringer som inkluderer kredittkorttransaksjoner når en reiseregning opprettes, kan du følge fremgangsmåten nedenfor.</span><span class="sxs-lookup"><span data-stu-id="2e000-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="2e000-113">Åpne arbeidsområdet **Utgiftshåndtering**.</span><span class="sxs-lookup"><span data-stu-id="2e000-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="2e000-114">I kategorien **Kvitteringer** kontrollerer du at det finnes ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="2e000-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="2e000-115">Du kan også laste opp kvitteringer i kategorien **Kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="2e000-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="2e000-116">I kategorien **Utgifter** kontrollerer du at det finnes ikke-tilknyttede utgifter.</span><span class="sxs-lookup"><span data-stu-id="2e000-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="2e000-117">Vanligvis importerer utgiftsadministrator disse utgiftene fra kredittkortleverandøren.</span><span class="sxs-lookup"><span data-stu-id="2e000-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="2e000-118">Velg **Ny reiseregning**.</span><span class="sxs-lookup"><span data-stu-id="2e000-118">Select **New expense report**.</span></span> <span data-ttu-id="2e000-119">Legg merke til at du kan ta med utgifter og nå også kvitteringer når du oppretter en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="2e000-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="2e000-120">Hvis du legger til både utgifter og kvitteringer, utløses automatisk avstemming av kvitteringene mot utgiftene.</span><span class="sxs-lookup"><span data-stu-id="2e000-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="2e000-121">Opprette eller samsvare kvitteringer mot en reiseregning</span><span class="sxs-lookup"><span data-stu-id="2e000-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="2e000-122">Fullfør fremgangsmåten nedenfor for å opprette en utgift eller samsvare en utgift fra en kvittering.</span><span class="sxs-lookup"><span data-stu-id="2e000-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="2e000-123">Legg ved en kvittering i en reiseregning ved å velge kategorien **Kvitteringer** og deretter **Legg til kvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="2e000-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="2e000-124">Under det opplastede bildet av kvitteringen legger du merke til alternativene **Opprett** og **Samsvar**.</span><span class="sxs-lookup"><span data-stu-id="2e000-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="2e000-125">Velg **Opprett** for å opprette en manuelt angitt utgiftstransaksjon, og fyll ut verdiene som trekkes ut fra kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="2e000-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="2e000-126">Hvis du velger **Samsvar**, prøver systemet å samsvare en eksisterende utgift med kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="2e000-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="2e000-127">Installasjon</span><span class="sxs-lookup"><span data-stu-id="2e000-127">Installation</span></span>

<span data-ttu-id="2e000-128">Hvis du vil bruke disse avanserte utgiftsfunksjonene, installerer du tilleggsprogrammet for reiseregning og utlegg for Microsoft Dynamics 365 Finance, og deretter aktiverer du funksjonene i forekomsten.</span><span class="sxs-lookup"><span data-stu-id="2e000-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="2e000-129">Du kan få tilgang til tillegget fra prosjektet i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2e000-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2e000-130">Logg på LCS, og åpne ønsket miljø.</span><span class="sxs-lookup"><span data-stu-id="2e000-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="2e000-131">Gå til **Detaljert informasjon**.</span><span class="sxs-lookup"><span data-stu-id="2e000-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="2e000-132">Velg **Vedlikehold**, eller rull ned til hurtigfanen **Tilleggsprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="2e000-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="2e000-133">Velg **Installer et nytt tillegg**.</span><span class="sxs-lookup"><span data-stu-id="2e000-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="2e000-134">Velg **Expense Management Service**.</span><span class="sxs-lookup"><span data-stu-id="2e000-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="2e000-135">Følg installasjonsveiledningen, og godta vilkårene.</span><span class="sxs-lookup"><span data-stu-id="2e000-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="2e000-136">Velg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="2e000-136">Select **Install**.</span></span>

<span data-ttu-id="2e000-137">Aktiver følgende funksjoner i arbeidsområdet **Funksjonsbehandling**:</span><span class="sxs-lookup"><span data-stu-id="2e000-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="2e000-138">Nyskapte utgiftsrapporter</span><span class="sxs-lookup"><span data-stu-id="2e000-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="2e000-139">Automatisk samsvar og opprette utgift fra kvittering</span><span class="sxs-lookup"><span data-stu-id="2e000-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="2e000-140">Når du aktiverer disse funksjonene, oppstår følgende handlinger:</span><span class="sxs-lookup"><span data-stu-id="2e000-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="2e000-141">Det eksisterende arbeidsområdet for **utgiftshåndtering** erstattes av det nye arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="2e000-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2e000-142">Det legges til et nytt menyelement for synlighet for utgiftsfelt.</span><span class="sxs-lookup"><span data-stu-id="2e000-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2e000-143">Du kan fremdeles åpne siden for de tidligere **reiseregningene** ved å gå til **Utgiftshåndtering > Mine utgifter > Reiseregninger**.</span><span class="sxs-lookup"><span data-stu-id="2e000-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="2e000-144">Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.</span><span class="sxs-lookup"><span data-stu-id="2e000-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="2e000-145">Kvitteringer blir behandlet gjennom Microsoft Azure Cognitive Services, og metadata blir trukket ut og lagt til.</span><span class="sxs-lookup"><span data-stu-id="2e000-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="2e000-146">Det legges til et alternativ som du kan bruke til å opprette en reiseregning som inkluderer samsvarte, ikke-tilknyttede kvitteringer.</span><span class="sxs-lookup"><span data-stu-id="2e000-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="2e000-147">Ved hjelp av et alternativ som legges til i reiseregninger, kan du opprette en utgiftslinje fra en kvittering, eller forsøk på å samsvare en eksisterende kvittering med en eksisterende utgiftslinje.</span><span class="sxs-lookup"><span data-stu-id="2e000-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2e000-148">Vanlige spørsmål</span><span class="sxs-lookup"><span data-stu-id="2e000-148">Frequently asked questions</span></span>

<span data-ttu-id="2e000-149">**Bruker Microsoft dataene mine for modellene sine?**</span><span class="sxs-lookup"><span data-stu-id="2e000-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="2e000-150">Nei, Microsoft har bygget en generell maskinlæringsmodell for tjenesten for mottaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="2e000-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="2e000-151">Denne modellen er ikke basert på mottakene du laster opp.</span><span class="sxs-lookup"><span data-stu-id="2e000-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="2e000-152">**Hvor er denne funksjonen tilgjengelig og behandlet?**</span><span class="sxs-lookup"><span data-stu-id="2e000-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="2e000-153">USA støttes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="2e000-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="2e000-154">**Hvor havner kvitteringene mine?**</span><span class="sxs-lookup"><span data-stu-id="2e000-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="2e000-155">Økonomiavdelingen Cognitive Services for å trekke ut feltdataene.</span><span class="sxs-lookup"><span data-stu-id="2e000-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="2e000-156">Cognitive Services beholder en kopi av kvitteringen i opptil 24 timer, mens behandlingen utføres.</span><span class="sxs-lookup"><span data-stu-id="2e000-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="2e000-157">Når behandlingen er fullført, fjerner Cognitive Services kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="2e000-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="2e000-158">Kvitteringer lagres fremdeles i økonomi.</span><span class="sxs-lookup"><span data-stu-id="2e000-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="2e000-159">Hvis du vil ha mer informasjon, kan du se [Aktivere kvitteringsforståelse med den nye funksjonen i Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="2e000-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
