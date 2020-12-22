---
title: Opprette en løsning for egendefinerte prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter løsninger for egendefinerte prisdimensjoner.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441501dff23d16960381b3f9fb4b2cceba2b3ba5
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514009"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="5e6af-103">Opprette en løsning for egendefinerte prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="5e6af-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="5e6af-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="5e6af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="5e6af-105">Alle egendefinerte endringer i prisdimensjonen må være i en egen løsning.</span><span class="sxs-lookup"><span data-stu-id="5e6af-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="5e6af-106">Denne anbefalte fremgangsmåten gir deg fleksibiliteten å oppdatere eller fjerne endringer etter behov, hjelper deg med å bruke arbeidet ditt om igjen, og gjør det enklere å overføre til andre forekomster.</span><span class="sxs-lookup"><span data-stu-id="5e6af-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="5e6af-107">Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **Administrert** løsning, og deretter importerer du den til andre forekomster for gjenbruk.</span><span class="sxs-lookup"><span data-stu-id="5e6af-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="5e6af-108">Opprette en løsning for egendefinerte prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="5e6af-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="5e6af-109">Velg **Innstillinger** > **Løsninger**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="5e6af-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="5e6af-110">Gi løsningen navnet *<your organization name>-prisdimensjonener*.</span><span class="sxs-lookup"><span data-stu-id="5e6af-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="5e6af-111">Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="5e6af-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Opprette egendefinert prisdimensjonsløsninger](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="5e6af-113">Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen</span><span class="sxs-lookup"><span data-stu-id="5e6af-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="5e6af-114">Legg til følgende Project Service-enheter i prisløsningen for å gjøre viktige skjemaendringer i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="5e6af-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="5e6af-115">Når du har fullført denne prosedyren, gjenkjenner enhetene de nye prisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="5e6af-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="5e6af-116">Velg **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du på **<*ditt organisasjonsnavn*> prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="5e6af-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="5e6af-117">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="5e6af-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="5e6af-118">I dialogboksen **Løsningskomponenter** velger du følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="5e6af-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="5e6af-119">**Faktisk**</span><span class="sxs-lookup"><span data-stu-id="5e6af-119">**Actual**</span></span>
   - <span data-ttu-id="5e6af-120">**Ressurs som kan reserveres**</span><span class="sxs-lookup"><span data-stu-id="5e6af-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="5e6af-121">**Estimatlinje**</span><span class="sxs-lookup"><span data-stu-id="5e6af-121">**Estimate Line**</span></span>
   - <span data-ttu-id="5e6af-122">**Prosjektoppgave**</span><span class="sxs-lookup"><span data-stu-id="5e6af-122">**Project Task**</span></span>
   - <span data-ttu-id="5e6af-123">**Fakturalinjedetalj**</span><span class="sxs-lookup"><span data-stu-id="5e6af-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="5e6af-124">**Journallinje**</span><span class="sxs-lookup"><span data-stu-id="5e6af-124">**Journal Line**</span></span>
   - <span data-ttu-id="5e6af-125">**Detalj for prosjektkontraktlinjer**</span><span class="sxs-lookup"><span data-stu-id="5e6af-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="5e6af-126">**Prosjektteammedlem**</span><span class="sxs-lookup"><span data-stu-id="5e6af-126">**Project Team Member**</span></span>
   - <span data-ttu-id="5e6af-127">**Tilbudslinjedetalj**</span><span class="sxs-lookup"><span data-stu-id="5e6af-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="5e6af-128">**Rolleprispåslag**</span><span class="sxs-lookup"><span data-stu-id="5e6af-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="5e6af-129">**Rollepris**</span><span class="sxs-lookup"><span data-stu-id="5e6af-129">**Role Price**</span></span>
   - <span data-ttu-id="5e6af-130">**Tidsoppføring**</span><span class="sxs-lookup"><span data-stu-id="5e6af-130">**Time Entry**</span></span>
 
   ![Legg til eksisterende egendefinerte løsninger for prisdimensjoner](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="5e6af-132">Du kan gjennomgå komponentene for hver enhet som blir lagt til, og den endelige listen over enhetsverdier for hver enhet.</span><span class="sxs-lookup"><span data-stu-id="5e6af-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="5e6af-133">Inkluder alle skjemaer og visninger for hver av enhetene som er valgt.</span><span class="sxs-lookup"><span data-stu-id="5e6af-133">Include all forms and views for each of the selected entities.</span></span>

  ![Enheter lagt til](./media/solution-component-selection.png)


5.  <span data-ttu-id="5e6af-135">Når du blir bedt om å inkludere avhengige enheter for de valgte enhetene, velger du **Nei, ikke ta med nødvendige komponenter.**</span><span class="sxs-lookup"><span data-stu-id="5e6af-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Inkludere avhengige enheter](./media/Do-not-include-required.png)
