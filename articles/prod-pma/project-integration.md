---
title: Integrasjon med Microsoft Project Client
description: Det kan være komplisert å planlegge og vedlikeholde en prosjektplan, så prosjektledere trenger å bruke verktøy som hjelper dem med å administrere denne oppgaven. Integrasjon med Microsoft Project Client gir støtte for å åpne og administrere en arbeidsnedbrytningsstruktur for et prosjekt.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269847"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="6c378-104">Integrasjon med Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c378-105">Det kan være komplisert å planlegge og vedlikeholde en prosjektplan, så prosjektledere trenger å bruke verktøy som hjelper dem med å administrere denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="6c378-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="6c378-106">Integrasjon med Microsoft Project Client gir støtte for å åpne og administrere en arbeidsnedbrytningsstruktur for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6c378-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="6c378-107">Prosjektlederen kan publisere eventuelle endringer tilbake til arbeidsnedbrytningsstrukturen for Dynamics 365 Finance-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6c378-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="6c378-108">Hvis du bruker juli-oppdateringen (versjon 10.0.4), må du installere KB 4054797 og 4055884.</span><span class="sxs-lookup"><span data-stu-id="6c378-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="6c378-109">Konfigurere tilleggsprogrammet Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="6c378-110">Hvis du vil aktivere integreringen med Microsoft Project Client, må et Microsoft Dynamics 365-tillegg installeres i brukerens klient for Microsoft Project-programmet.</span><span class="sxs-lookup"><span data-stu-id="6c378-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="6c378-111">Dette gjøres ved å åpne **Arbeidsområdet for prosjektstyring**.</span><span class="sxs-lookup"><span data-stu-id="6c378-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="6c378-112">•   Klikk **Konfigurer prosjektklienttillegg** fra delen **Koblinger** > **Oppsett** i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="6c378-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="6c378-113">•   Klikk **Åpne**, og klikk deretter **Kjør** når du blir bedt om det.</span><span class="sxs-lookup"><span data-stu-id="6c378-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="6c378-114">Åpne og rediger et eksisterende utkast for en arbeidsnedbrytningsstruktur i Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="6c378-115">Hvis et prosjekt i Dynamics 365 Finance allerede har opprettet en arbeidsnedbrytningsstruktur, kan arbeidsnedbrytningsstrukturen åpnes i Microsoft Project Client-programmet hvis arbeidsnedbrytningsstrukturen er i utkaststatus.</span><span class="sxs-lookup"><span data-stu-id="6c378-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="6c378-116">Hvis du vil åpne fra **Prosjekt**-siden, klikker du **Åpne i Microsoft Project**-koblingen i kategorien **Plan**. Du kan også åpne denne siden i Microsoft Project Client-programmet ved å klikke **Åpne** i kategorien **Microsoft Dynamics 365**. Velg **Juridisk enhet** og **Prosjekt** fra listen.</span><span class="sxs-lookup"><span data-stu-id="6c378-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="6c378-117">Hvis du bruker Internet Explorer som webleser, må du klikke **Lagre** for å åpne manuelt fra plasseringen som filen er lastet ned til.</span><span class="sxs-lookup"><span data-stu-id="6c378-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="6c378-118">Du kan også klikke **Lagre og åpne** for å åpne filen i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="6c378-119">Ikke gi nytt navn til filen når du lagrer.</span><span class="sxs-lookup"><span data-stu-id="6c378-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="6c378-120">Før du redigerer filen ved hjelp av Microsoft Project Client, må du sjekke den ut. Klikk **Sjekk ut** i kategorien **Microsoft Dynamics 365**. Dette hindrer at andre brukere kan redigere arbeidsnedbrytningsstrukturen fra Finance samtidig.</span><span class="sxs-lookup"><span data-stu-id="6c378-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="6c378-121">Hvis du vil publisere arbeidsnedbrytningsstruktur etter at du har fullført eventuelle redigeringer, klikker du **Sjekk inn** i kategorien **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6c378-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="6c378-122">Hvis et prosjektteam allerede er lagt til i prosjektet i Finance, vil ressurslisten fylles ut med teammedlemmene.</span><span class="sxs-lookup"><span data-stu-id="6c378-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="6c378-123">Hvis et prosjektteam ennå ikke er lagt til i prosjektet, kan du velge ressurser og bygge teamet i Microsoft Project Client ved å klikke **Ressurser**-knappen i kategorien **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6c378-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="6c378-124">Følgende data blir synkronisert til Finance som en del av innsjekkingsprosessen:</span><span class="sxs-lookup"><span data-stu-id="6c378-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="6c378-125">•   Aktivitetsnavn</span><span class="sxs-lookup"><span data-stu-id="6c378-125">•   Task name</span></span>

<span data-ttu-id="6c378-126">•   Startdato</span><span class="sxs-lookup"><span data-stu-id="6c378-126">•   Start date</span></span>

<span data-ttu-id="6c378-127">•   Sluttdato</span><span class="sxs-lookup"><span data-stu-id="6c378-127">•   Finish date</span></span>

<span data-ttu-id="6c378-128">•   Foregående oppgaver</span><span class="sxs-lookup"><span data-stu-id="6c378-128">•   Predecessors</span></span>

<span data-ttu-id="6c378-129">•   Ressursnavn</span><span class="sxs-lookup"><span data-stu-id="6c378-129">•   Resource names</span></span>

<span data-ttu-id="6c378-130">•   Fane</span><span class="sxs-lookup"><span data-stu-id="6c378-130">•   Category</span></span>

<span data-ttu-id="6c378-131">•   Ressurskategori</span><span class="sxs-lookup"><span data-stu-id="6c378-131">•   Resource category</span></span>

<span data-ttu-id="6c378-132">•   Arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="6c378-132">•   Work hours</span></span>

<span data-ttu-id="6c378-133">•   Merknader</span><span class="sxs-lookup"><span data-stu-id="6c378-133">•   Notes</span></span>

<span data-ttu-id="6c378-134">•   Prioritet</span><span class="sxs-lookup"><span data-stu-id="6c378-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="6c378-135">Hvis du legger til andre kolonner i Microsoft Project Client-filen, blir de ikke lagret i filen, og vises ikke når filen åpnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="6c378-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="6c378-136">Opprette arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="6c378-137">Slik oppretter du en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project Client:</span><span class="sxs-lookup"><span data-stu-id="6c378-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="6c378-138">Åpne Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="6c378-139">I kategorien **Microsoft Dynamics 365** klikker du **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="6c378-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="6c378-140">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6c378-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="6c378-141">Velg **Prosjektet**.</span><span class="sxs-lookup"><span data-stu-id="6c378-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="6c378-142">Klikk **Sjekk ut** i kategorien **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6c378-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="6c378-143">Når du er klar til å publisere til Finance, klikker du **Sjekk inn** i kategorien **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="6c378-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="6c378-144">Erstatte den eksisterende arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="6c378-145">Følg denne fremgangsmåten for å opprette en ny arbeidsnedbrytningsstruktur med Microsoft Project Client og erstatte en eksisterende arbeidsnedbrytningsstruktur for et eksisterende prosjekt:</span><span class="sxs-lookup"><span data-stu-id="6c378-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="6c378-146">Åpne Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="6c378-147">Opprett tidsplanen i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="6c378-148">I kategorien **Microsoft Dynamics 365** klikker du **Lagre endringer** > **Erstatt eksisterende prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="6c378-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="6c378-149">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6c378-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="6c378-150">Velg **Prosjektet**.</span><span class="sxs-lookup"><span data-stu-id="6c378-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="6c378-151">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c378-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="6c378-152">Opprette et nytt prosjekt fra Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="6c378-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="6c378-153">Åpne Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="6c378-154">Opprett tidsplanen i Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="6c378-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="6c378-155">I kategorien **Microsoft Dynamics 365** klikker du **Lagre endringer** > **Lagre til nytt prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="6c378-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="6c378-156">Velg **Juridisk enhet** for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6c378-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="6c378-157">Angi **Prosjekt-ID** om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="6c378-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="6c378-158">Angi **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="6c378-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="6c378-159">Velg **Prosjekttype**, **Prosjektgruppe** og **Prosjektkontrakt-ID**.</span><span class="sxs-lookup"><span data-stu-id="6c378-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="6c378-160">Du kan også opprette en ny prosjektkontrakt ved å klikke **Ny**.</span><span class="sxs-lookup"><span data-stu-id="6c378-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="6c378-161">Velg **Kalenderen** som skal brukes for ressurser.</span><span class="sxs-lookup"><span data-stu-id="6c378-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="6c378-162">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c378-162">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="6c378-163">Tillegget for prosjektklienten støtter ikke følgende tegn i prosjekt-ID-formatet:</span><span class="sxs-lookup"><span data-stu-id="6c378-163">The Project Client add-in doesn’t support the following characters in the project ID format:</span></span>
> 
>   - <span data-ttu-id="6c378-164">Understrek</span><span class="sxs-lookup"><span data-stu-id="6c378-164">Underscore</span></span>
>   - <span data-ttu-id="6c378-165">Periode</span><span class="sxs-lookup"><span data-stu-id="6c378-165">Period</span></span>
>   - <span data-ttu-id="6c378-166">Mellomrom</span><span class="sxs-lookup"><span data-stu-id="6c378-166">Space</span></span>
>   - <span data-ttu-id="6c378-167">Skråstrek</span><span class="sxs-lookup"><span data-stu-id="6c378-167">Slash</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
