---
title: Opprette et prosjektteam
description: Dette emnet gir informasjon om hvordan du oppretter og administrerer prosjektteam.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006208"
---
# <a name="create-a-project-team"></a><span data-ttu-id="f50bd-103">Opprette et prosjektteam</span><span class="sxs-lookup"><span data-stu-id="f50bd-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f50bd-104">Hvis du vil bruke rollene som ble opprettet tidligere i et prosjekt, må en prosjektleder knytte rollene til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f50bd-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="f50bd-105">Det kan tilordnes flere roller for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="f50bd-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="f50bd-106">Disse rollene blir automatisk merket under reservering for å unngå forvirring.</span><span class="sxs-lookup"><span data-stu-id="f50bd-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="f50bd-107">Hvis prosjektlederen for eksempel krever tre ingeniører, genereres det automatisk tre programvareingeniørroller som har **programvareingeniør 1**, **programvareingeniør 2** og **programvareingeniør 3** som etikett.</span><span class="sxs-lookup"><span data-stu-id="f50bd-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="f50bd-108">Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter under søk etter en ressurs.</span><span class="sxs-lookup"><span data-stu-id="f50bd-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="f50bd-109">Du kan legge til flere karakteristikker som kreves for å presisere søket ytterligere.</span><span class="sxs-lookup"><span data-stu-id="f50bd-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="f50bd-110">Visningsinnstillinger kan også tilpasses for å gi en bedre visning av ressurstilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="f50bd-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="f50bd-111">Det finnes alternativer for å vise tilgjengelighet for time, dag, uke, måned, kvartal og år.</span><span class="sxs-lookup"><span data-stu-id="f50bd-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="f50bd-112">Det finnes også et alternativ for å vise tilgjengelig og gjenstående kapasitet på ressurser.</span><span class="sxs-lookup"><span data-stu-id="f50bd-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="f50bd-113">Dette alternativet er nyttig for tidsstyring når du beregner tilgjengelig tid for aktiviteter eller ressurstilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="f50bd-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="f50bd-114">Prosjektlederen kan velge en rolle på siden og deretter velge å reservere en ressurs som fyller rollen, hvis det er en tilgjengelig ressurs som passer til kravet.</span><span class="sxs-lookup"><span data-stu-id="f50bd-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="f50bd-115">Vær oppmerksom på at ressursene ikke må reserveres på dette tidspunktet i planleggingsfasen.</span><span class="sxs-lookup"><span data-stu-id="f50bd-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="f50bd-116">Når du oppretter en WBS, kan du erstatte roller med bemannede ressurser for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="f50bd-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="f50bd-117">Hvis roller erstattes med bemannede ressurser i WBS, oppdaterer ressursoppsettet automatisk prosjektgruppens liste og planlegging.</span><span class="sxs-lookup"><span data-stu-id="f50bd-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="f50bd-118">[![Prosjektteamoppføring som inkluderer både roller og faktiske ressurser](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="f50bd-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="f50bd-119">Prosjektlederen har forskjellige alternativer for bestilling av en ressurs for et prosjekt, for eksempel **Gjenstående kapasitet**, **Full kapasitet**, **Kapasitet i prosent** og **Angi timer**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="f50bd-120">Disse bestillingsalternativene kan kanselleres når som helst hvis ressurstilordningene endres.</span><span class="sxs-lookup"><span data-stu-id="f50bd-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="f50bd-121">To typer bestillinger støttes:</span><span class="sxs-lookup"><span data-stu-id="f50bd-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="f50bd-122">**Forpliktende bestilling** – Ressursreservasjonen ble godkjent og bekreftet til å fungere på avtalene for den angitte varigheten.</span><span class="sxs-lookup"><span data-stu-id="f50bd-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="f50bd-123">**Ikke-forpliktende bestilling** – Ressursreservasjonene ble foreløpig angitt til å fungere på avtalene for den angitte varigheten.</span><span class="sxs-lookup"><span data-stu-id="f50bd-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="f50bd-124">Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.</span><span class="sxs-lookup"><span data-stu-id="f50bd-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="f50bd-125">Opprette et prosjektteam</span><span class="sxs-lookup"><span data-stu-id="f50bd-125">Create a project team</span></span>

1. <span data-ttu-id="f50bd-126">På listesiden **Alle prosjekter** velger du et prosjekt, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="f50bd-127">I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato pluss én måned.</span><span class="sxs-lookup"><span data-stu-id="f50bd-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="f50bd-128">Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="f50bd-129">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-129">Select **Add**.</span></span>
4. <span data-ttu-id="f50bd-130">I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Overordnet prosjektleder**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="f50bd-131">Velg **Nødvendige kompetanser**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="f50bd-132">På siden **Velg egenskaper** velges egenskapene som du tidligere har angitt for rollen overordnet prosjektleder, som standard.</span><span class="sxs-lookup"><span data-stu-id="f50bd-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="f50bd-133">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-133">Select **OK**.</span></span>
7. <span data-ttu-id="f50bd-134">På siden **Legg til roller i prosjektet**, i feltet **Antall ressurser**, angir du **1**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="f50bd-135">I **Ressurs**-feltet viser oppslaget alle ressurser som har de nødvendige kompetansene.</span><span class="sxs-lookup"><span data-stu-id="f50bd-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="f50bd-136">Velg **Daniel Goldschmid**, og velg deretter **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="f50bd-137">Velg **Legg til** på siden **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="f50bd-138">I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="f50bd-139">I feltet **Antall ressurser** angir du **5**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="f50bd-140">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-140">Select **Create**.</span></span>
12. <span data-ttu-id="f50bd-141">På siden **Prosjekter** velger du **Fullfør ressurs**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="f50bd-142">Overvåke prosjektteam</span><span class="sxs-lookup"><span data-stu-id="f50bd-142">Monitor project teams</span></span>
1. <span data-ttu-id="f50bd-143">På siden **Alle prosjekter** velger du koblingen **Prosjekt-ID** for prosjektet **XYZ-oppgraderingsfase 2**.</span><span class="sxs-lookup"><span data-stu-id="f50bd-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="f50bd-144">På hurtigfanen **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som vises, er riktige.</span><span class="sxs-lookup"><span data-stu-id="f50bd-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]