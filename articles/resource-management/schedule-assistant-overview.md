---
title: Oversikt over planleggingsassistent
description: Dette emnet inneholder informasjon om hvordan du arbeider med planleggingsassistenten for å bestille ressurser.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014128"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="b9548-103">Oversikt over planleggingsassistent</span><span class="sxs-lookup"><span data-stu-id="b9548-103">Schedule assistant overview</span></span>

<span data-ttu-id="b9548-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b9548-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b9548-105">Planleggingsassistenten brukes til å reservere ressurser basert på behov som er definert av prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="b9548-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="b9548-106">Planleggingsassistenten er avhengig av parameterne som er angitt i ressurskravet for å finne ressursen.</span><span class="sxs-lookup"><span data-stu-id="b9548-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="b9548-107">Planleggingsassistenten anbefaler ressurser som samsvarer med relevante krav, for eksempel hvilke tidsvinduer eller ferdigheter som kreves.</span><span class="sxs-lookup"><span data-stu-id="b9548-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="b9548-108">Når egnede ressurser er identifisert, kan ressurs- eller prosjektlederen reservere ressursen i arbeidet.</span><span class="sxs-lookup"><span data-stu-id="b9548-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b9548-109">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="b9548-109">Prerequisites</span></span>

<span data-ttu-id="b9548-110">Planleggingsassistenten er en del av Universal Resource Scheduling-løsningen.</span><span class="sxs-lookup"><span data-stu-id="b9548-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="b9548-111">Denne løsningen er inkludert og installert med Dynamics 365 Project Operations, Dynamics 365 Field Service og Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="b9548-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="b9548-112">Samsvare krav og ressurser</span><span class="sxs-lookup"><span data-stu-id="b9548-112">Matching requirements and resources</span></span>

<span data-ttu-id="b9548-113">Et generert ressurskrav er basert på detaljer som for eksempel:</span><span class="sxs-lookup"><span data-stu-id="b9548-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="b9548-114">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="b9548-114">Characteristics</span></span>
-   <span data-ttu-id="b9548-115">Roller</span><span class="sxs-lookup"><span data-stu-id="b9548-115">Roles</span></span>
-   <span data-ttu-id="b9548-116">Forretningsenheter</span><span class="sxs-lookup"><span data-stu-id="b9548-116">Business units</span></span>
-   <span data-ttu-id="b9548-117">Ressurspreferanser</span><span class="sxs-lookup"><span data-stu-id="b9548-117">Resource preferences</span></span>
-   <span data-ttu-id="b9548-118">Innsatsomfang</span><span class="sxs-lookup"><span data-stu-id="b9548-118">Effort contours</span></span>
-   <span data-ttu-id="b9548-119">Tidssone</span><span class="sxs-lookup"><span data-stu-id="b9548-119">Time zone</span></span>

<span data-ttu-id="b9548-120">Planleggingsassistenten bruker disse detaljene til å filtrere ressurser.</span><span class="sxs-lookup"><span data-stu-id="b9548-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="b9548-121">Start planleggingsassistenten.</span><span class="sxs-lookup"><span data-stu-id="b9548-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="b9548-122">Det er to måter å starte planleggingsassistenten på.</span><span class="sxs-lookup"><span data-stu-id="b9548-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="b9548-123">Hvis du bruker hybrid modus, kan du velge et teammedlem med et ressurskrav som ikke er oppfylt, i rutenettet for teammedlemmer, og deretter velge **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="b9548-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="b9548-124">Hvis du bruker sentral modus, er det ressurslederen som finner og velger ressursen.</span><span class="sxs-lookup"><span data-stu-id="b9548-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="b9548-125">Filtre i planleggingsassistenten</span><span class="sxs-lookup"><span data-stu-id="b9548-125">Schedule assistant filters</span></span>

<span data-ttu-id="b9548-126">Når planleggingsassistenten kjører, vises detaljene fra ressurskravet som filtrerte verdier i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="b9548-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="b9548-127">Ressurslederen eller prosjektlederen kan finjustere resultatene ved å justere filtrene, slik at de dekker planleggingsbehovene.</span><span class="sxs-lookup"><span data-stu-id="b9548-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="b9548-128">Filterruten viser arbeidsrelaterte alternativer, blant annet følgende:</span><span class="sxs-lookup"><span data-stu-id="b9548-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="b9548-129">Start og slutt for arbeidet</span><span class="sxs-lookup"><span data-stu-id="b9548-129">Work start and end</span></span>
-   <span data-ttu-id="b9548-130">Kjennetegn</span><span class="sxs-lookup"><span data-stu-id="b9548-130">Characteristics</span></span>
-   <span data-ttu-id="b9548-131">Roller</span><span class="sxs-lookup"><span data-stu-id="b9548-131">Roles</span></span>
-   <span data-ttu-id="b9548-132">Organisasjonsenheter</span><span class="sxs-lookup"><span data-stu-id="b9548-132">Organizational units</span></span>
-   <span data-ttu-id="b9548-133">Ressursstyringsfirma</span><span class="sxs-lookup"><span data-stu-id="b9548-133">Resourcing company</span></span>
-   <span data-ttu-id="b9548-134">Ressurstyper</span><span class="sxs-lookup"><span data-stu-id="b9548-134">Resource types</span></span>
-   <span data-ttu-id="b9548-135">Foretrukne ressurser</span><span class="sxs-lookup"><span data-stu-id="b9548-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]