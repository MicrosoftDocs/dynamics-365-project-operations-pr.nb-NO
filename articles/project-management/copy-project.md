---
title: Kopiere et prosjekt
description: Denne emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091266"
---
# <a name="copy-a-project"></a><span data-ttu-id="efa67-103">Kopier et prosjekt</span><span class="sxs-lookup"><span data-stu-id="efa67-103">Copy a project</span></span>

<span data-ttu-id="efa67-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="efa67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="efa67-105">Med Dynamics 365 Project Operations kan du raskt bygge nye prosjekter ved å velge **Kopier prosjekt** i **Prosjekter**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="efa67-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="efa67-106">Hvis du vil kopiere et prosjekt, åpner du prosjektet du vil kopiere, og deretter velger du **Kopier prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="efa67-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="efa67-107">Handlingen kopierer følgende:</span><span class="sxs-lookup"><span data-stu-id="efa67-107">The action will copy the following:</span></span>

- <span data-ttu-id="efa67-108">Prosjektegenskaper</span><span class="sxs-lookup"><span data-stu-id="efa67-108">Project properties</span></span> 
- <span data-ttu-id="efa67-109">Arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="efa67-109">Work breakdown structure</span></span>
- <span data-ttu-id="efa67-110">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="efa67-110">Project team members</span></span>
- <span data-ttu-id="efa67-111">Prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="efa67-111">Project estimates</span></span>
- <span data-ttu-id="efa67-112">Prosjektets utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="efa67-112">Project expense estimates</span></span>
- <span data-ttu-id="efa67-113">Prosjektmaterialestimater</span><span class="sxs-lookup"><span data-stu-id="efa67-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="efa67-114">Prosjektegenskaper</span><span class="sxs-lookup"><span data-stu-id="efa67-114">Project properties</span></span>

<span data-ttu-id="efa67-115">Når prosjektet kopieres, blir verdiene i følgende felt kopiert:</span><span class="sxs-lookup"><span data-stu-id="efa67-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="efa67-116">Navn</span><span class="sxs-lookup"><span data-stu-id="efa67-116">Name</span></span>
- <span data-ttu-id="efa67-117">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="efa67-117">Description</span></span>
- <span data-ttu-id="efa67-118">Kunde</span><span class="sxs-lookup"><span data-stu-id="efa67-118">Customer</span></span>
- <span data-ttu-id="efa67-119">Kalendermal</span><span class="sxs-lookup"><span data-stu-id="efa67-119">Calendar Template</span></span>
- <span data-ttu-id="efa67-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="efa67-120">Currency</span></span>
- <span data-ttu-id="efa67-121">Kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="efa67-121">Contracting Unit</span></span>
- <span data-ttu-id="efa67-122">Prosjektleder</span><span class="sxs-lookup"><span data-stu-id="efa67-122">Project Manager</span></span>
- <span data-ttu-id="efa67-123">Status</span><span class="sxs-lookup"><span data-stu-id="efa67-123">Status</span></span>
- <span data-ttu-id="efa67-124">Generell prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="efa67-124">Overall Project Status</span></span>
- <span data-ttu-id="efa67-125">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="efa67-125">Comments</span></span>
- <span data-ttu-id="efa67-126">Estimater</span><span class="sxs-lookup"><span data-stu-id="efa67-126">Estimates</span></span>
- <span data-ttu-id="efa67-127">Beregnet startdato: Dette er datoen da prosjektet ble opprettet fra kopien.</span><span class="sxs-lookup"><span data-stu-id="efa67-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="efa67-128">Beregnet sluttdato: Denne datoen justeres basert på startdatoen for det nye prosjektet som ble gjort fra kopien.</span><span class="sxs-lookup"><span data-stu-id="efa67-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="efa67-129">Innsats (timer)</span><span class="sxs-lookup"><span data-stu-id="efa67-129">Effort (Hours)</span></span>
- <span data-ttu-id="efa67-130">Estimert arbeidskostnad</span><span class="sxs-lookup"><span data-stu-id="efa67-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="efa67-131">Estimert utgiftskostnad</span><span class="sxs-lookup"><span data-stu-id="efa67-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="efa67-132">Estimert materialkostnad</span><span class="sxs-lookup"><span data-stu-id="efa67-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="efa67-133">Kopieringsprosjektet kjører lenge.</span><span class="sxs-lookup"><span data-stu-id="efa67-133">Copy project is a long running operation.</span></span> <span data-ttu-id="efa67-134">Prosjektoppføringer, de relevante attributtene og mange relaterte enheter kopieres også.</span><span class="sxs-lookup"><span data-stu-id="efa67-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="efa67-135">På grunn av hvor lenge operasjonen har kjørt, låses målprosjektsiden for redigering til kopioperasjonen er fullført.</span><span class="sxs-lookup"><span data-stu-id="efa67-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="efa67-136">Arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="efa67-136">Work breakdown structure</span></span>

<span data-ttu-id="efa67-137">Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert.</span><span class="sxs-lookup"><span data-stu-id="efa67-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="efa67-138">Navngitte ressurser erstattes av generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="efa67-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="efa67-139">Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes planleggingen på nytt, og varigheten på oppgavene kan bli endret.</span><span class="sxs-lookup"><span data-stu-id="efa67-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="efa67-140">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="efa67-140">Project team members</span></span>

<span data-ttu-id="efa67-141">Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene.</span><span class="sxs-lookup"><span data-stu-id="efa67-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="efa67-142">Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="efa67-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="efa67-143">Navngitte ressurser konverteres til generelle teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="efa67-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="efa67-144">Estimater</span><span class="sxs-lookup"><span data-stu-id="efa67-144">Estimates</span></span>

<span data-ttu-id="efa67-145">Når prosjektet kopieres, kopieres ressurs-, utgifts- og materialestimatlinjer fra kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="efa67-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="efa67-146">Hvis du vil ha informasjon om hvordan du programmatisk får tilgang til Kopier Project, kan du se [Utvikle prosjektmaler med Kopier prosjekt](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="efa67-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
