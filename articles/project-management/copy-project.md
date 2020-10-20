---
title: Kopiere et prosjekt
description: Dette emnet gir informasjon om kopiering av prosjekter i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908429"
---
# <a name="copy-a-project"></a><span data-ttu-id="abf5d-103">Kopiere et prosjekt</span><span class="sxs-lookup"><span data-stu-id="abf5d-103">Copy a project</span></span>

<span data-ttu-id="abf5d-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="abf5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="abf5d-105">Med Dynamics 365 Project Operations kan du raskt utvikle nye prosjekter ved hjelp av handlingen **Kopier prosjekt** i **Prosjekter**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="abf5d-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="abf5d-106">Hvis du vil kopiere et prosjekt, velger du et prosjekt, og deretter velger du **Kopier**.</span><span class="sxs-lookup"><span data-stu-id="abf5d-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="abf5d-107">Handlingen kopierer følgende:</span><span class="sxs-lookup"><span data-stu-id="abf5d-107">The action will copy:</span></span>

- <span data-ttu-id="abf5d-108">Prosjektegenskaper</span><span class="sxs-lookup"><span data-stu-id="abf5d-108">Project properties</span></span>
- <span data-ttu-id="abf5d-109">Arbeidsnedbrytningsstrukturen</span><span class="sxs-lookup"><span data-stu-id="abf5d-109">The Work breakdown structure</span></span>
- <span data-ttu-id="abf5d-110">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="abf5d-110">Project team members</span></span>
- <span data-ttu-id="abf5d-111">Prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="abf5d-111">Project estimates</span></span>
- <span data-ttu-id="abf5d-112">Prosjektets utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="abf5d-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="abf5d-113">Prosjektegenskaper</span><span class="sxs-lookup"><span data-stu-id="abf5d-113">Project properties</span></span>

<span data-ttu-id="abf5d-114">Når prosjektet kopieres, blir verdiene i følgende felt kopiert:</span><span class="sxs-lookup"><span data-stu-id="abf5d-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="abf5d-115">Navn</span><span class="sxs-lookup"><span data-stu-id="abf5d-115">Name</span></span>
- <span data-ttu-id="abf5d-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="abf5d-116">Description</span></span>
- <span data-ttu-id="abf5d-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="abf5d-117">Customer</span></span>
- <span data-ttu-id="abf5d-118">Kalendermal</span><span class="sxs-lookup"><span data-stu-id="abf5d-118">Calendar Template</span></span>
- <span data-ttu-id="abf5d-119">Valuta</span><span class="sxs-lookup"><span data-stu-id="abf5d-119">Currency</span></span>
- <span data-ttu-id="abf5d-120">Kontraktsenhet</span><span class="sxs-lookup"><span data-stu-id="abf5d-120">Contracting Unit</span></span>
- <span data-ttu-id="abf5d-121">Prosjektleder</span><span class="sxs-lookup"><span data-stu-id="abf5d-121">Project Manager</span></span>
- <span data-ttu-id="abf5d-122">Status</span><span class="sxs-lookup"><span data-stu-id="abf5d-122">Status</span></span>
- <span data-ttu-id="abf5d-123">Generell prosjektstatus</span><span class="sxs-lookup"><span data-stu-id="abf5d-123">Overall Project Status</span></span>
- <span data-ttu-id="abf5d-124">Kommentarer</span><span class="sxs-lookup"><span data-stu-id="abf5d-124">Comments</span></span>
- <span data-ttu-id="abf5d-125">Estimater</span><span class="sxs-lookup"><span data-stu-id="abf5d-125">Estimates</span></span>
- <span data-ttu-id="abf5d-126">Beregnet startdato</span><span class="sxs-lookup"><span data-stu-id="abf5d-126">Estimated Start Date</span></span>
- <span data-ttu-id="abf5d-127">Sluttdato</span><span class="sxs-lookup"><span data-stu-id="abf5d-127">Finish Date</span></span>
- <span data-ttu-id="abf5d-128">Innsats (timer)</span><span class="sxs-lookup"><span data-stu-id="abf5d-128">Effort (Hours)</span></span>
- <span data-ttu-id="abf5d-129">Estimert arbeidskostnad</span><span class="sxs-lookup"><span data-stu-id="abf5d-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="abf5d-130">Estimert utgiftskostnad</span><span class="sxs-lookup"><span data-stu-id="abf5d-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="abf5d-131">Arbeidsnedbrytningsstruktur</span><span class="sxs-lookup"><span data-stu-id="abf5d-131">Work breakdown structure</span></span>

<span data-ttu-id="abf5d-132">Når prosjektet kopieres, blir hele den ressurslastede arbeidsnedbrytningsstrukturen kopiert.</span><span class="sxs-lookup"><span data-stu-id="abf5d-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="abf5d-133">Navngitte ressurser erstattes av generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="abf5d-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="abf5d-134">Hvis de navngitte ressursene ikke har samme arbeidstid som den generelle ressursen, beregnes planleggingen på nytt, og varigheten på oppgavene kan bli endret.</span><span class="sxs-lookup"><span data-stu-id="abf5d-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="abf5d-135">Prosjektteammedlemmer</span><span class="sxs-lookup"><span data-stu-id="abf5d-135">Project team members</span></span>

<span data-ttu-id="abf5d-136">Når et prosjektteam kopieres fra kildeprosjektet, kopieres de generelle ressursene.</span><span class="sxs-lookup"><span data-stu-id="abf5d-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="abf5d-137">Tildeling av generelle ressurser blir også vedlikeholdt slik som i kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="abf5d-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="abf5d-138">Navngitte ressurser konverteres til generelle teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="abf5d-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="abf5d-139">Estimater</span><span class="sxs-lookup"><span data-stu-id="abf5d-139">Estimates</span></span>

<span data-ttu-id="abf5d-140">Når prosjektet kopieres, blir både ressurs- og kostnadsestimatlinjer kopiert fra kildeprosjektet.</span><span class="sxs-lookup"><span data-stu-id="abf5d-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>