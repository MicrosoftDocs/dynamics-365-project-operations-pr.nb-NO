---
title: Opprette egendefinerte løsninger for prisdimensjoner
description: Dette emnet forklarer hvordan du oppretter en egendefinert løsning når du oppretter egendefinerte prisdimensjoner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012328"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="a6204-103">Opprette egendefinerte løsninger for prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="a6204-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="a6204-104">Alle egendefinerte endringer i prisdimensjonen må være i en egen løsning.</span><span class="sxs-lookup"><span data-stu-id="a6204-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="a6204-105">Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst.</span><span class="sxs-lookup"><span data-stu-id="a6204-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="a6204-106">Når du har gjort de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.</span><span class="sxs-lookup"><span data-stu-id="a6204-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="a6204-107">Velg **Innstillinger** > **Løsninger**, og velg deretter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a6204-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="a6204-108">Gi løsningen navnet **\<your organization name>-prisdimensjoner**, angi den gjenstående nødvendige informasjonen, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="a6204-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Opprette en egendefinert løsning for prisdimensjoner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="a6204-110">Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen</span><span class="sxs-lookup"><span data-stu-id="a6204-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="a6204-111">Du må legge til følgende Project Service-enheter i prisløsningen.</span><span class="sxs-lookup"><span data-stu-id="a6204-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="a6204-112">Fullfør trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="a6204-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="a6204-113">Velg **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.</span><span class="sxs-lookup"><span data-stu-id="a6204-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="a6204-114">I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.</span><span class="sxs-lookup"><span data-stu-id="a6204-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="a6204-115">I dialogboksen **Løsningskomponenter** velger du følgende enheter:</span><span class="sxs-lookup"><span data-stu-id="a6204-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="a6204-116">Faktisk</span><span class="sxs-lookup"><span data-stu-id="a6204-116">Actual</span></span>
- <span data-ttu-id="a6204-117">Ressurs som kan reserveres</span><span class="sxs-lookup"><span data-stu-id="a6204-117">Bookable Resource</span></span>
- <span data-ttu-id="a6204-118">Estimatlinje</span><span class="sxs-lookup"><span data-stu-id="a6204-118">Estimate Line</span></span>
- <span data-ttu-id="a6204-119">Prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="a6204-119">Project Task</span></span>
- <span data-ttu-id="a6204-120">Fakturalinjedetalj</span><span class="sxs-lookup"><span data-stu-id="a6204-120">Invoice Line Detail</span></span>
- <span data-ttu-id="a6204-121">Journallinje</span><span class="sxs-lookup"><span data-stu-id="a6204-121">Journal Line</span></span>
- <span data-ttu-id="a6204-122">Detalj for prosjektkontraktlinjer</span><span class="sxs-lookup"><span data-stu-id="a6204-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="a6204-123">Prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="a6204-123">Project Team Member</span></span>
- <span data-ttu-id="a6204-124">Tilbudslinjedetalj</span><span class="sxs-lookup"><span data-stu-id="a6204-124">Quote Line Detail</span></span>
- <span data-ttu-id="a6204-125">Rolleprispåslag</span><span class="sxs-lookup"><span data-stu-id="a6204-125">Role Price Markup</span></span>
- <span data-ttu-id="a6204-126">Rollepris</span><span class="sxs-lookup"><span data-stu-id="a6204-126">Role Price</span></span> 
- <span data-ttu-id="a6204-127">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="a6204-127">Time Entry</span></span> 

> ![Legg til eksisterende enheter i prisdimensjonsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Velg løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="a6204-130">Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.</span><span class="sxs-lookup"><span data-stu-id="a6204-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="a6204-131">Når du blir bedt om å inkludere avhengige enheter for de valgte enhetene, klikker du **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a6204-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Ikke ta med alle relaterte komponenter](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]