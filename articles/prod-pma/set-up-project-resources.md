---
title: Definere prosjektressurser
description: Dette emnet gir informasjon om å sette opp eller be om prosjektressurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081792"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="bb71b-103">Definere prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="bb71b-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb71b-104">Du må sette opp en kalender og knytte den til en ansatt eller en arbeider.</span><span class="sxs-lookup"><span data-stu-id="bb71b-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="bb71b-105">Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="bb71b-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="bb71b-106">Under kalenderinstallasjonen kan prosjektledere utføre ressursutjevning som en del av ressursoptimaliseringen.</span><span class="sxs-lookup"><span data-stu-id="bb71b-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="bb71b-107">Restriksjoner kan brukes på ressurser basert på kalendertidsplanen.</span><span class="sxs-lookup"><span data-stu-id="bb71b-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="bb71b-108">Du kan sette opp en kalender på **Kalenderere** -siden.</span><span class="sxs-lookup"><span data-stu-id="bb71b-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="bb71b-109">Når du definerer en arbeider som en prosjektressurs, kan du velge blant arbeidere som arbeider i firmaet som du konfigurerer ressurser for.</span><span class="sxs-lookup"><span data-stu-id="bb71b-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="bb71b-110">Du kan også velge arbeidere fra andre selskaper i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="bb71b-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="bb71b-111">Disse arbeiderne kalles konserninterne ressurser.</span><span class="sxs-lookup"><span data-stu-id="bb71b-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="bb71b-112">Fremgangsmåten nedenfor forklarer hvordan du konfigurerer en arbeider som en prosjektressurs i firmaet, og hvordan du oppretter en konsernintern prosjektressurs.</span><span class="sxs-lookup"><span data-stu-id="bb71b-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="bb71b-113">Konfigurere en arbeider som en prosjektressurs</span><span class="sxs-lookup"><span data-stu-id="bb71b-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="bb71b-114">På siden **Arbeidere** i listen **Arbeidere** velger du arbeideren som du legger til som prosjektressurs, og åpner arbeideroppføringen.</span><span class="sxs-lookup"><span data-stu-id="bb71b-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="bb71b-115">I handlingsruten velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="bb71b-116">Velg en kalender, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="bb71b-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="bb71b-117">Du kan også angi standardprosjekter for en ressurs som en type forhåndstilordning.</span><span class="sxs-lookup"><span data-stu-id="bb71b-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="bb71b-118">Forhåndstildelinger kan brukes når ressurslederen eller prosjektlederen vet hvilke prosjekter ressursen skal jobbe med på forhånd.</span><span class="sxs-lookup"><span data-stu-id="bb71b-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="bb71b-119">Forhåndstildelinger kan også være basert på forespørselen fra en prosjektsponsor eller kunde.</span><span class="sxs-lookup"><span data-stu-id="bb71b-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="bb71b-120">Hvis du vil forhåndstilordne et prosjekt, velger du det gjeldende prosjektet på siden **Tilordne prosjekter** i kategorien **Prosjekter** på listen **Gjenværende prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="bb71b-121">Konfigurere en konsernintern ressurs</span><span class="sxs-lookup"><span data-stu-id="bb71b-121">Set up an intercompany resource</span></span>

<span data-ttu-id="bb71b-122">Når du definerer en arbeider som en konsernintern ressurs, må du fullføre oppsettet i både utlånsselskapet og lånefirmaet.</span><span class="sxs-lookup"><span data-stu-id="bb71b-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="bb71b-123">I utlånsfirmaet</span><span class="sxs-lookup"><span data-stu-id="bb71b-123">In the lending company</span></span>

1. <span data-ttu-id="bb71b-124">Kontroller at utlånsfirmaet er valgt i Finance, og fullfør deretter fremgangsmåten i forrige del, "Konfigurere en arbeider som en prosjektressurs".</span><span class="sxs-lookup"><span data-stu-id="bb71b-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="bb71b-125">På siden **Konserninternt regnskap** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="bb71b-126">I feltet **ID for juridisk enhet** velger du utlånsselskapet.</span><span class="sxs-lookup"><span data-stu-id="bb71b-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="bb71b-127">Fyll ut de gjenværende feltene etter behov, og velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="bb71b-128">På siden **Overføringspris** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="bb71b-129">I feltet **Juridisk enhet som låner** velger du riktig selskap.</span><span class="sxs-lookup"><span data-stu-id="bb71b-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="bb71b-130">Hvis du vil låne låneselskapet bare ressursen du opprettet i begynnelsen av denne delen, velger du navnet på ressursen du opprettet, i **Ressurs** -feltet.</span><span class="sxs-lookup"><span data-stu-id="bb71b-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="bb71b-131">Hvis du vil gjøre alle ressursene i utlånsfirmaet tilgjengelige for lånefirmaet, lar du **Ressurs** -feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="bb71b-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="bb71b-132">På siden **Parametere for prosjektstyring og regnskap** , i kategorien **Konsernintern** , setter du **Aktiver konsernintern ressursplanlegging og timeregistreringer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bb71b-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="bb71b-133">I lånefirmaet</span><span class="sxs-lookup"><span data-stu-id="bb71b-133">In the borrowing company</span></span>

- <span data-ttu-id="bb71b-134">På siden **Ressursliste** , i søkefilteret, skriver du inn navnet på ressursen du opprettet for utlånsfirmaet, for å kontrollere at navnet er inkludert i ressurslisten for lånefirmaet.</span><span class="sxs-lookup"><span data-stu-id="bb71b-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="bb71b-135">Be om prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="bb71b-135">Request project resources</span></span>
<span data-ttu-id="bb71b-136">Funksjonaliteten for planlegging av prosjektressurser gjør det bare for ressursledere å distribuere bemannede ressurser på engasjementer eller prosjekter.</span><span class="sxs-lookup"><span data-stu-id="bb71b-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="bb71b-137">Hvis du vil aktivere denne funksjonaliteten, må du utføre følgende oppgaver eller kontrollere at de er fullført:</span><span class="sxs-lookup"><span data-stu-id="bb71b-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="bb71b-138">Angi nummerserier.</span><span class="sxs-lookup"><span data-stu-id="bb71b-138">Set up number sequences.</span></span>
- <span data-ttu-id="bb71b-139">Konfigurere prosjektstyrings- og regnskapsflyter.</span><span class="sxs-lookup"><span data-stu-id="bb71b-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="bb71b-140">Aktivere ressursforespørselsflyter.</span><span class="sxs-lookup"><span data-stu-id="bb71b-140">Enable resource request workflows.</span></span>

<span data-ttu-id="bb71b-141">Når de foregående oppgavene er fullført, kan du utføre følgende oppgaver slik du ønsker:</span><span class="sxs-lookup"><span data-stu-id="bb71b-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="bb71b-142">Opprett en ressursforespørsel fra en uforpliktende bemannet ressurs.</span><span class="sxs-lookup"><span data-stu-id="bb71b-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="bb71b-143">Overvåk ressursforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bb71b-143">Monitor resource requests.</span></span>
- <span data-ttu-id="bb71b-144">Oppfyll ressursforespørsler.</span><span class="sxs-lookup"><span data-stu-id="bb71b-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="bb71b-145">Be om en bemannet ressurs fra en WBS.</span><span class="sxs-lookup"><span data-stu-id="bb71b-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="bb71b-146">Reserver ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.</span><span class="sxs-lookup"><span data-stu-id="bb71b-146">Book resources to a project without having a request for a staffed resource.</span></span>
