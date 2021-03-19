---
title: Kopiere et prosjekt
description: Denne emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479531"
---
# <a name="copy-a-project"></a><span data-ttu-id="6abc9-103">Kopier et prosjekt</span><span class="sxs-lookup"><span data-stu-id="6abc9-103">Copy a project</span></span>

<span data-ttu-id="6abc9-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6abc9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6abc9-105">Med Dynamics 365 Project Operations kan du raskt bygge nye prosjekter ved å velge **Kopier prosjekt** i **Prosjekter**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="6abc9-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="6abc9-106">Hvis du vil kopiere et prosjekt, åpner du prosjektet du vil kopiere, og deretter velger du **Kopier prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="6abc9-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="6abc9-107">Handlingen kopierer følgende:</span><span class="sxs-lookup"><span data-stu-id="6abc9-107">The action will copy:</span></span>

- <span data-ttu-id="6abc9-108">Prosjektegenskaper (Beregnet startdato kopieres fra kildeprosjektet)</span><span class="sxs-lookup"><span data-stu-id="6abc9-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="6abc9-109">Arbeidsnedbrytningsstrukturen</span><span class="sxs-lookup"><span data-stu-id="6abc9-109">The Work breakdown structure</span></span>
- <span data-ttu-id="6abc9-110">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="6abc9-110">Project team members</span></span>
- <span data-ttu-id="6abc9-111">Prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="6abc9-111">Project estimates</span></span>
- <span data-ttu-id="6abc9-112">Prosjektets utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="6abc9-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="6abc9-113">Prosjektegenskaper</span><span class="sxs-lookup"><span data-stu-id="6abc9-113">Project properties</span></span>

<span data-ttu-id="6abc9-114">Når prosjektet kopieres, blir verdiene i følgende felt kopiert:</span><span class="sxs-lookup"><span data-stu-id="6abc9-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="6abc9-115">Navn</span><span class="sxs-lookup"><span data-stu-id="6abc9-115">Name</span></span>
- <span data-ttu-id="6abc9-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6abc9-116">Description</span></span>
- <span data-ttu-id="6abc9-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="6abc9-117">Customer</span></span>
- <span data-ttu-id="6abc9-118">Kalendermal</span><span class="sxs-lookup"><span data-stu-id="6abc9-118">Calendar Template</span></span>
- <span data-ttu-id="6abc9-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="6abc9-119">Currency</span></span>
- <span data-ttu-id="6abc9-120">Kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="6abc9-120">Contracting Unit</span></span>
- <span data-ttu-id="6abc9-121">Prosjektleder</span><span class="sxs-lookup"><span data-stu-id="6abc9-121">Project Manager</span></span>
- <span data-ttu-id="6abc9-122">Status</span><span class="sxs-lookup"><span data-stu-id="6abc9-122">Status</span></span>
- <span data-ttu-id="6abc9-123">Generell prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="6abc9-123">Overall Project Status</span></span>
- <span data-ttu-id="6abc9-124">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="6abc9-124">Comments</span></span>
- <span data-ttu-id="6abc9-125">Estimater</span><span class="sxs-lookup"><span data-stu-id="6abc9-125">Estimates</span></span>
- <span data-ttu-id="6abc9-126">Beregnet startdato</span><span class="sxs-lookup"><span data-stu-id="6abc9-126">Estimated Start Date</span></span>
- <span data-ttu-id="6abc9-127">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="6abc9-127">Finish Date</span></span>
- <span data-ttu-id="6abc9-128">Innsats (timer)</span><span class="sxs-lookup"><span data-stu-id="6abc9-128">Effort (Hours)</span></span>
- <span data-ttu-id="6abc9-129">Estimert arbeidskostnad</span><span class="sxs-lookup"><span data-stu-id="6abc9-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="6abc9-130">Estimert utgiftskostnad</span><span class="sxs-lookup"><span data-stu-id="6abc9-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="6abc9-131">Arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="6abc9-131">Work breakdown structure</span></span>

<span data-ttu-id="6abc9-132">Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert.</span><span class="sxs-lookup"><span data-stu-id="6abc9-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="6abc9-133">Navngitte ressurser erstattes av generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="6abc9-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="6abc9-134">Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes planleggingen på nytt, og varigheten på oppgavene kan bli endret.</span><span class="sxs-lookup"><span data-stu-id="6abc9-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="6abc9-135">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="6abc9-135">Project team members</span></span>

<span data-ttu-id="6abc9-136">Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene.</span><span class="sxs-lookup"><span data-stu-id="6abc9-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="6abc9-137">Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6abc9-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="6abc9-138">Navngitte ressurser konverteres til generelle teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="6abc9-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="6abc9-139">Estimater</span><span class="sxs-lookup"><span data-stu-id="6abc9-139">Estimates</span></span>

<span data-ttu-id="6abc9-140">Når prosjektet kopieres, blir både ressurs- og kostnadsestimatlinjer kopiert fra kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="6abc9-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="6abc9-141">Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="6abc9-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
