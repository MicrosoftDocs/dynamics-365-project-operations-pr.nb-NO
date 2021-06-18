---
title: Opprette tidsoppføringer
description: Dette emnet gir informasjon om hvordan du oppretter tidsoppføringer.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bc8e52fef0aa02505e412c746343ce1410c40ac3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999278"
---
# <a name="create-time-entries"></a><span data-ttu-id="a04e0-103">Opprette tidsoppføringer</span><span class="sxs-lookup"><span data-stu-id="a04e0-103">Create time entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a04e0-104">I tidligere versjoner av Dynamics 365 Project Service Automation ble tidsoppføringer angitt med en ukebasis.</span><span class="sxs-lookup"><span data-stu-id="a04e0-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="a04e0-105">I versjon 3 av Project Service Automation registreres tidsoppføringer daglig.</span><span class="sxs-lookup"><span data-stu-id="a04e0-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="a04e0-106">Etter at du har opprettet en oppføring, kan du imidlertid masseopprette eller kopiere dem.</span><span class="sxs-lookup"><span data-stu-id="a04e0-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="a04e0-107">Opprette en tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="a04e0-107">Create a time entry</span></span>

<span data-ttu-id="a04e0-108">Følg denne fremgangsmåten for å opprette en tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="a04e0-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="a04e0-109">På siden **Tidsoppføringer** velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="a04e0-110">I dialogboksen **Hurtigoppretting: Tidsoppføring** angir du varigheten til tidsoppføringen i minutter, timer eller dager.</span><span class="sxs-lookup"><span data-stu-id="a04e0-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="a04e0-111">Varigheten må angis i følgende format: *x* minutter, *x* timer eller *x* dager.</span><span class="sxs-lookup"><span data-stu-id="a04e0-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="a04e0-112">Timer og dager kan også angis som desimaler, for eksempel *x,x* timer eller *x,x* dager.</span><span class="sxs-lookup"><span data-stu-id="a04e0-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="a04e0-113">Velg type tidsoppføring og prosjektet du vil angi tidsoppføring for.</span><span class="sxs-lookup"><span data-stu-id="a04e0-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="a04e0-114">Finn aktiviteten for denne tidsoppføringen i feltet **Prosjektoppgave**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a04e0-115">Hvis du skal opprette en tidsoppføring for en oppgave som ikke er tilordnet til en bruker, går du til **Prosjektoppgave**, velger **Søk**-knappen, velger **Endre visning** og deretter **Alle aktive prosjektoppgaver** for å vise alle oppgavene.</span><span class="sxs-lookup"><span data-stu-id="a04e0-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="a04e0-116">Angi en beskrivelse hvis det kreves en beskrivelse, og velg deretter **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="a04e0-117">Når tidsoppføringen er opprettet og lagret, kan du redigere den i tidsrutenettet for tidsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="a04e0-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="a04e0-118">Tidsoppføringsrutenettet støtter to formater:</span><span class="sxs-lookup"><span data-stu-id="a04e0-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="a04e0-119">Du kan angi tidsoppføringer i **tt:mm**-format.</span><span class="sxs-lookup"><span data-stu-id="a04e0-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="a04e0-120">Dette formatet blir deretter konvertert til timer og brøker.</span><span class="sxs-lookup"><span data-stu-id="a04e0-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="a04e0-121">Du kan skrive inn timer og brøker direkte.</span><span class="sxs-lookup"><span data-stu-id="a04e0-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="a04e0-122">Vær oppmerksom på at brøkene i en time ikke er minutter.</span><span class="sxs-lookup"><span data-stu-id="a04e0-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="a04e0-123">Derfor representerer 1,5 timer 1 time og 30 minutter.</span><span class="sxs-lookup"><span data-stu-id="a04e0-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="a04e0-124">Den samme regelen gjelder for deler av en dag.</span><span class="sxs-lookup"><span data-stu-id="a04e0-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="a04e0-125">Én dag er 24 timer, og 0,5 dager representerer 12 timer.</span><span class="sxs-lookup"><span data-stu-id="a04e0-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="a04e0-126">Masseopprette tidsoppføringer</span><span class="sxs-lookup"><span data-stu-id="a04e0-126">Bulk create time entries</span></span>

<span data-ttu-id="a04e0-127">Etter at du har opprettet noen få oppføringer, kan du bruke dem til å opprette flere tidsoppføringer samtidig.</span><span class="sxs-lookup"><span data-stu-id="a04e0-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="a04e0-128">På siden **Tidsoppføringer** velger du **Kopier uke**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="a04e0-129">I feltgruppen **Fra periode** i feltene **Startdato** og **Sluttdato** definerer du datointervallet tidsoppføringer skal kopieres fra.</span><span class="sxs-lookup"><span data-stu-id="a04e0-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="a04e0-130">I feltgruppen **Til-periode** i feltet **Startdato** angir du datoen tidsoppføringer skal opprettes for.</span><span class="sxs-lookup"><span data-stu-id="a04e0-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="a04e0-131">Velg **Kopier** for å opprette en kopi av tidsoppføringene som samsvarer med ukedagen som er angitt i feltgruppen **Til periode**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="a04e0-132">Mandagens tidsoppføring fra forrige uke blir for eksempel kopiert til mandag for uken som er angitt i feltgruppen **Til-periode**.</span><span class="sxs-lookup"><span data-stu-id="a04e0-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="a04e0-133">Importere data for tidsoppføringer</span><span class="sxs-lookup"><span data-stu-id="a04e0-133">Import data for time entries</span></span>

<span data-ttu-id="a04e0-134">Du kan importere data fra prosjektbestillinger og -tilordninger.</span><span class="sxs-lookup"><span data-stu-id="a04e0-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="a04e0-135">Når du importerer data, kan du angi datointervallet for bestillinger for å importere og deretter eksplisitt velge bestillinger som skal opprettes som **Utkast**-tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a04e0-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="a04e0-136">Funksjoner for å gruppere etter, sortere, søke og filtrere</span><span class="sxs-lookup"><span data-stu-id="a04e0-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="a04e0-137">Du kan gruppere og filtrere tidsoppføringer etter dimensjonene som er angitt i kolonnene.</span><span class="sxs-lookup"><span data-stu-id="a04e0-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="a04e0-138">I feltet **Grupper etter** velger du dimensjonen som skal brukes til å filtrere tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a04e0-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="a04e0-139">Du kan også sortere tidsoppføringsregistreringer i stigende eller synkende rekkefølge ved å bruke sorteringspilen i kolonneoverskriftene.</span><span class="sxs-lookup"><span data-stu-id="a04e0-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="a04e0-140">Du kan også vise eller skjule oppføringer ved å velge **Filter**-knappen på kolonneoverskriftene og deretter, i **Søk**-boksen, angi teksten som skal brukes til å søke etter tidsoppføringer etter prosjektnavn, prosjektoppgave, tidsoppføring eller ressurs.</span><span class="sxs-lookup"><span data-stu-id="a04e0-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]