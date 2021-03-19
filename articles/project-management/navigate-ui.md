---
title: Navigasjon i brukergrensesnittet
description: Dette emnet gir informasjon om prosjektledelse i Dynamics 365 Project-operasjoner.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286755"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="32399-103">Navigasjon i brukergrensesnittet</span><span class="sxs-lookup"><span data-stu-id="32399-103">Navigating the user interface</span></span>

<span data-ttu-id="32399-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="32399-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="32399-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="32399-105">Overview</span></span>

<span data-ttu-id="32399-106">Hovedprosjektskjemaet er delt inn i flere kategorier.</span><span class="sxs-lookup"><span data-stu-id="32399-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="32399-107">Hver kategori representerer et forskjellig detaljnivå i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="32399-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="32399-108">**Sammendrag**: Gir en beskrivelse av prosjektet og aggregerer både planlagt og faktisk prosjekt ytelse.</span><span class="sxs-lookup"><span data-stu-id="32399-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Kategorien Sammendrag og felt](media/navigation7.png)

- <span data-ttu-id="32399-110">**Oppgaver**: Gir detaljer om arbeidsnedbrytningsstrukturen representert av en rutenettvisning, en tavlevisning og et Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="32399-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Kategorien Oppgave og felt](media/navigation8.png)

- <span data-ttu-id="32399-112">**Team**: Inneholder detaljer om prosjektdeltakerne.</span><span class="sxs-lookup"><span data-stu-id="32399-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="32399-113">Den tilordnede innsatsen for hvert teammedlem blir også oppsummert i denne visningen.</span><span class="sxs-lookup"><span data-stu-id="32399-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Kategorien Team og felt](media/navigation9.png)

- <span data-ttu-id="32399-115">**Ressurstilordninger**: Gir en tidsinndelt visning av innsatsen for hver ressurs i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="32399-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Kategorien Ressurstilordninger og felt](media/navigation10.png)

- <span data-ttu-id="32399-117">**Ressursavstemming**: Gir en tidsinndelt visning av forskjellene mellom tilordningene til hver navngitt ressurs og deres bestillinger.</span><span class="sxs-lookup"><span data-stu-id="32399-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Kategorien Ressursavstemming og felt](media/navigation11.png)

- <span data-ttu-id="32399-119">**Estimater**: Gir en tidsinndelt visning av kostnads- og salgsestimatene for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="32399-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Kategorien Estimater og felt](media/navigation12.png)

- <span data-ttu-id="32399-121">**Sporing**: Gir en visning som viser fremdriften for oppgaver i arbeidsnedbrytingsstrukturen for innsats, kostnad og salg.</span><span class="sxs-lookup"><span data-stu-id="32399-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Kategorien Sporing og felt](media/navigation13.png)

- <span data-ttu-id="32399-123">**Salg**: Inneholder dypkoblinger til tilbud og kontrakter som er knyttet til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="32399-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="32399-124">**Utgiftsestimater**: Gir et rutenett som definerer prosjektutgifter basert på organisatoriske utgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="32399-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Kategorien Utgiftsestimater og felt](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="32399-126">Rutenettkontroller</span><span class="sxs-lookup"><span data-stu-id="32399-126">Grid controls</span></span>

<span data-ttu-id="32399-127">Nedenfor vises en kort oversikt over vanlige kontroller som finnes på de forskjellige prosjektplanleggingsfanene.</span><span class="sxs-lookup"><span data-stu-id="32399-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="32399-128">Refresh</span><span class="sxs-lookup"><span data-stu-id="32399-128">Refresh</span></span>

<span data-ttu-id="32399-129">**Oppdater**: Henter de nyeste dataene fra serveren hvis det har oppstått endringer etter at rutenettet ble lastet inn.</span><span class="sxs-lookup"><span data-stu-id="32399-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Oppdater-knapp](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="32399-131">Grupper etter</span><span class="sxs-lookup"><span data-stu-id="32399-131">Group by</span></span>

<span data-ttu-id="32399-132">**Grupper etter**: Oppdaterer grupperingen av radene i rutenettet for å gjenspeile enten ressurser, roller eller kategorier basert på brukerens behov.</span><span class="sxs-lookup"><span data-stu-id="32399-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Grupper etter-knappen](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="32399-134">Forrige/Neste</span><span class="sxs-lookup"><span data-stu-id="32399-134">Previous/Next</span></span>

<span data-ttu-id="32399-135">**Forrige**/**Neste**: Oppdater de synlige tidsperiodene i de tidsinndelte rutenettene.</span><span class="sxs-lookup"><span data-stu-id="32399-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Knappene Forrige og Neste](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="32399-137">Tidsskala</span><span class="sxs-lookup"><span data-stu-id="32399-137">Timescale</span></span>

<span data-ttu-id="32399-138">**Tidsskala**: Endre aggregasjonen til tidsinndelte data mellom dager, uker, måneder og år.</span><span class="sxs-lookup"><span data-stu-id="32399-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Tidsskala-knappen](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="32399-140">Utvid</span><span class="sxs-lookup"><span data-stu-id="32399-140">Expand</span></span>

<span data-ttu-id="32399-141">**Utvid**: Gjengir det synlige rutenettet i fullskjermmodus, og gir mer mulighet til å se flere roller.</span><span class="sxs-lookup"><span data-stu-id="32399-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![Utvid-knappen](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="32399-143">Tidsfase etter</span><span class="sxs-lookup"><span data-stu-id="32399-143">Time-phase by</span></span>

<span data-ttu-id="32399-144">**Tidsfase etter**: Oppdater grupperingen av radene i rutenettet for å gjenspeile kostnadsestimater for salgsestimater.</span><span class="sxs-lookup"><span data-stu-id="32399-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="32399-145">Denne kontrollen gjelder også for estimatskriptet og rutenettet for sporing.</span><span class="sxs-lookup"><span data-stu-id="32399-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Tidsfase etter-knappen](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="32399-147">Legg til kolonne</span><span class="sxs-lookup"><span data-stu-id="32399-147">Add column</span></span>

<span data-ttu-id="32399-148">**Legg til kolonne**: Gjør det mulig for brukeren å definere de synlige kolonnene i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="32399-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="32399-149">Bare medfølgende kolonner kan legges til i rutenettet på skjemaet **Prosjektplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="32399-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Legg til kolonne-knappen](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]