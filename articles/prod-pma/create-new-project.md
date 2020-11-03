---
title: Opprett et nytt prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter et nytt prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081755"
---
# <a name="create-a-new-project"></a><span data-ttu-id="7a900-103">Opprett et nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="7a900-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a900-104">Fullfør fremgangsmåten nedenfor for å opprette et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="7a900-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="7a900-105">På siden **Prosjektledelse** velger du **Nytt prosjekt** , og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="7a900-105">On the **Project management** page, select **New project** , and enter the following values:</span></span>

    - <span data-ttu-id="7a900-106">**Prosjekttype:** Tid og materiale</span><span class="sxs-lookup"><span data-stu-id="7a900-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="7a900-107">**Prosjektnavn:** XYZ-oppgraderingsfase 2</span><span class="sxs-lookup"><span data-stu-id="7a900-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="7a900-108">**Prosjektgruppe:** TM\_VIA</span><span class="sxs-lookup"><span data-stu-id="7a900-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="7a900-109">**Prosjektkontrakt-ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="7a900-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="7a900-110">Velg **Opprett prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="7a900-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="7a900-111">Tilordne en ressurs til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="7a900-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="7a900-112">På siden **Arbeidere** i listen **Arbeidere** velger du oppføringen for arbeideren som du tidligere konfigurerte kompentanser for, åpne arbeideroppføringen.</span><span class="sxs-lookup"><span data-stu-id="7a900-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="7a900-113">I handlingsruten i kategorien **Prosjekt** i gruppen **Oppsett** velger du **Tilordne prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="7a900-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="7a900-114">På siden **Prosjekttilordninger for ressursvalidering** i kategorien **Prosjekt** i feltet **Legg til prosjekt i valgte prosjekter** filtrerer du på prosjektet **XYZ-oppgraderingsfase 2**.</span><span class="sxs-lookup"><span data-stu-id="7a900-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="7a900-115">I ruten **Gjenstående prosjekter** velger du et prosjekt, og deretter velger du pilknappen for å legge den til i ruten **Valgte prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="7a900-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="7a900-116">Du kan også tilordne kategorier for en ressurs slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="7a900-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="7a900-117">Kategoritypen er enten **Kostnad** eller **Omsetning**.</span><span class="sxs-lookup"><span data-stu-id="7a900-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="7a900-118">Kategoritypen bestemmes av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="7a900-118">The category type is determined by your organization.</span></span> <span data-ttu-id="7a900-119">Hvis ingen kategorier er tilordnet en ressurs, slår Finance opp standardkategorien på timepriser for kostnad og omsetning.</span><span class="sxs-lookup"><span data-stu-id="7a900-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="7a900-120">Konfigurere egenskaper for prosjektressurs og rolle</span><span class="sxs-lookup"><span data-stu-id="7a900-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="7a900-121">En prosjektleder kan bruke prosjektbemanningsfunksjonaliteten til å opprette rollene som kreves for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7a900-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="7a900-122">Roller kan brukes hvis bekreftede ressurser fremdeles er ukjente når ressurser blir reservert.</span><span class="sxs-lookup"><span data-stu-id="7a900-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="7a900-123">Roller kan være midlertidig reservert som planlagte ressurser, slik at du kan fortsette planleggingen av prosjektplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7a900-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="7a900-124">[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="7a900-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="7a900-125">**Scenario:** Contoso ble engasjert for å fullføre et Tid og materiale-prosjekt som har et godkjent prosjektcharter.</span><span class="sxs-lookup"><span data-stu-id="7a900-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="7a900-126">Juniorprosjektlederen holder fremdeles på med å ferdigstille prosjektomfanget.</span><span class="sxs-lookup"><span data-stu-id="7a900-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="7a900-127">Ressurslederen identifiserer for øyeblikket bestemte ressurser som blir reservert for å arbeide med det nye prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7a900-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="7a900-128">På grunn av den kritiske prosjekttypen ba prosjektsponsoren om at den overordnede prosjektlederen kunne ha én av rollene.</span><span class="sxs-lookup"><span data-stu-id="7a900-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="7a900-129">Ressurslederen må skaffe den nye ressursen og definere rollen i systemet i tilfelle juniorprosjektlederen krever ressursinformasjon under planleggingen av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7a900-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="7a900-130">Fremgangsmåten nedenfor viser hvordan ressurslederen kan konfigurere rollen som overordnet prosjektleder og knytte ressursegenskaper til den.</span><span class="sxs-lookup"><span data-stu-id="7a900-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="7a900-131">Senere kan rollen brukes til å søke etter tilgjengelige ressurser som samsvarer med de nødvendige ressurskompetansene.</span><span class="sxs-lookup"><span data-stu-id="7a900-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="7a900-132">På siden **Konfigurer roller** velger du **Ny** , og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="7a900-132">On the **Setup roles** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="7a900-133">**Rolle-ID:** Overordnet prosjektleder</span><span class="sxs-lookup"><span data-stu-id="7a900-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="7a900-134">**Beskrivelse:** Overordnet prosjektleder</span><span class="sxs-lookup"><span data-stu-id="7a900-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="7a900-135">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="7a900-135">Select **Create**.</span></span>
3. <span data-ttu-id="7a900-136">Velg rollen **Overordnet prosjektleder** , og velg deretter **Konfigurer egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="7a900-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="7a900-137">I feltet for **Type kjennetegn** velger du **Ferdighet**.</span><span class="sxs-lookup"><span data-stu-id="7a900-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="7a900-138">I feltet **Tilgjengelige kjennetegn** angir du ferdigheten du vil søke etter.</span><span class="sxs-lookup"><span data-stu-id="7a900-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="7a900-139">I feltet for **Type kjennetegn** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="7a900-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="7a900-140">I feltet **Tilgjengelige kjennetegn** angir du sertifikattypen du vil søke etter.</span><span class="sxs-lookup"><span data-stu-id="7a900-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="7a900-141">Tilordne en prosjektressurs til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="7a900-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="7a900-142">På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2** -prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7a900-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="7a900-143">I kategorien **Prosjektteam og planlegging** velger du **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="7a900-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="7a900-144">I feltet **Rolle** velger du **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="7a900-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="7a900-145">Velg **Bestill fra kalender**.</span><span class="sxs-lookup"><span data-stu-id="7a900-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="7a900-146">På siden **Ressurstilgjengelighet** velger du **Visningsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="7a900-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="7a900-147">Angi følgende verdier på siden **Juster visningsinnstillinger** :</span><span class="sxs-lookup"><span data-stu-id="7a900-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="7a900-148">**Format for visning av datoområde:** Dag</span><span class="sxs-lookup"><span data-stu-id="7a900-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="7a900-149">**Vis tilgjengelighetsbeskrivelser:** Ja</span><span class="sxs-lookup"><span data-stu-id="7a900-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="7a900-150">**Vis gjenstående kapasitet:** Ja</span><span class="sxs-lookup"><span data-stu-id="7a900-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="7a900-151">Velg en ressurs fra listen over ressurser.</span><span class="sxs-lookup"><span data-stu-id="7a900-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="7a900-152">Velg **Forpliktende bestilling** og **Full kapasitet**.</span><span class="sxs-lookup"><span data-stu-id="7a900-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="7a900-153">Tilordne en ressurs til en standardrolle</span><span class="sxs-lookup"><span data-stu-id="7a900-153">Assign a resource to a default role</span></span>

<span data-ttu-id="7a900-154">For å hjelpe kan prosjekt- og ressursledere drille ned ytterligere på ressursene som kan reserveres for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="7a900-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="7a900-155">Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig innhentet ressurs.</span><span class="sxs-lookup"><span data-stu-id="7a900-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="7a900-156">Når Daniel for eksempel ble leid inn, hadde han erfaringen og ferdighetene til å fylle rollen som forretningsanalytiker.</span><span class="sxs-lookup"><span data-stu-id="7a900-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="7a900-157">Ressursbehandleren tilordnet denne rollen som Daniels standardrolle.</span><span class="sxs-lookup"><span data-stu-id="7a900-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="7a900-158">Derfor har ressurslederen lagt til Daniel i en pulje av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.</span><span class="sxs-lookup"><span data-stu-id="7a900-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="7a900-159">Under ressursreservasjon kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter.</span><span class="sxs-lookup"><span data-stu-id="7a900-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="7a900-160">De kan bruke denne informasjonen som ett vilkår når de utfører beslutningsanalyse med flere vilkår under ressursfullføring.</span><span class="sxs-lookup"><span data-stu-id="7a900-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="7a900-161">De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har spesifikke ferdigheter, utdanning og erfaring for et gitt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="7a900-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="7a900-162">**Scenario:** Et godkjent prosjekt har startet, og rollen overordnet prosjektleder er reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen.</span><span class="sxs-lookup"><span data-stu-id="7a900-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="7a900-163">Ressursbehandleren har nå hentet en ressurs for å fullføre rollen overordnet prosjektleder.</span><span class="sxs-lookup"><span data-stu-id="7a900-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="7a900-164">På siden **Ressursliste** velger du **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="7a900-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="7a900-165">På siden **Ressursrolle** velger du **Ny** , og angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="7a900-165">On the **Resource role** page, select **New** , and enter the following values:</span></span>

    - <span data-ttu-id="7a900-166">**Gyldig:** ngi gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="7a900-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="7a900-167">**Utløp:** Angi **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="7a900-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="7a900-168">**Rolle-ID** : Angi **Overordnet prosjektleder**.</span><span class="sxs-lookup"><span data-stu-id="7a900-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="7a900-169">Velg **Lagre** , og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="7a900-169">Select **Save** , and then close the page.</span></span>
4. <span data-ttu-id="7a900-170">I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og sertifikatet **PMP**.</span><span class="sxs-lookup"><span data-stu-id="7a900-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
