---
title: Administrere tidssoner
description: Når et prosjekt opprettes, er tidssonen basert på tidssonen som er definert i den brukte arbeidstidsmalen.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119835"
---
# <a name="manage-time-zones"></a><span data-ttu-id="2c920-103">Administrere tidssoner</span><span class="sxs-lookup"><span data-stu-id="2c920-103">Manage time zones</span></span>

<span data-ttu-id="2c920-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="2c920-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="2c920-105">Prosjekter</span><span class="sxs-lookup"><span data-stu-id="2c920-105">Projects</span></span>

<span data-ttu-id="2c920-106">Når et prosjekt opprettes, er tidssonen basert på tidssonen som er definert i den brukte arbeidstidsmalen.</span><span class="sxs-lookup"><span data-stu-id="2c920-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="2c920-107">I **prosjektet** er datoene alltid relative i forhold til tidssonen for brukeren som er logget på i hver kategori, med unntak av **Oppgave**-kategorien. Når du viser arbeidsnedbrytningsstrukturen, vises alltid datoene i tidssonen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2c920-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="2c920-108">Oppgaver</span><span class="sxs-lookup"><span data-stu-id="2c920-108">Tasks</span></span>

<span data-ttu-id="2c920-109">Når du oppretter en oppgave, kontrolleres start- og sluttidspunktet og timene/dagen etter arbeidstiden til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2c920-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="2c920-110">Hvis en oppgave for eksempel er opprettet med et prosjekt der tids sonen er -8 PST, og har følgende arbeidstid: 09:00 til 17:00 mandag til fredag, vil alle oppgaver som er opprettet uten en tilordning, respektere start- og sluttidspunktet for prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="2c920-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="2c920-111">Administrere ressurser med tidssoner</span><span class="sxs-lookup"><span data-stu-id="2c920-111">Manage resources with time zones</span></span>

<span data-ttu-id="2c920-112">For å få nøyaktige og forutsigbare resultater når du bruker **Utvid bestilling**, er det to viktige krav som må oppfylles:</span><span class="sxs-lookup"><span data-stu-id="2c920-112">For accurate and predictable results when using **Extend Booking**, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="2c920-113">Brukeren må konfigurere tidssonen for enheten slik at den samsvarer medtids sonen som er angitt i systemets **tilpassingsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2c920-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Tidssoneinnstillinger i Windows 10](media/reconcile-assignments-03.png)

  ![Tidssoneinnstillinger i innstillinger for personalisering](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="2c920-116">Ressursen som kan bestilles, må ha minst ett minutt med arbeidstid som overlapper med konturene som brukes til å definere den ønskede utvidelsen.</span><span class="sxs-lookup"><span data-stu-id="2c920-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="2c920-117">Eksempel: Følgende ressurser med arbeidstid som faller mellom 09:00 og 19:00.</span><span class="sxs-lookup"><span data-stu-id="2c920-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Sammenligning av ressursomfang](media/reconcile-assignments-05.png)

<span data-ttu-id="2c920-119">Følgende tabell viser:</span><span class="sxs-lookup"><span data-stu-id="2c920-119">The following table shows:</span></span>

- <span data-ttu-id="2c920-120">En prosjektkalendermal</span><span class="sxs-lookup"><span data-stu-id="2c920-120">A project calendar template</span></span>
- <span data-ttu-id="2c920-121">Ressurs A: Denne ressursen har samme kalender og er i samme tidssone som prosjektet.</span><span class="sxs-lookup"><span data-stu-id="2c920-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="2c920-122">Starttidspunktet for bestillinger blir kl. 9:00.</span><span class="sxs-lookup"><span data-stu-id="2c920-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="2c920-123">Ressurs B: Denne ressursen befinner seg i en annen tidssone enn prosjektet, og starter 07:00 i sin tidssone.</span><span class="sxs-lookup"><span data-stu-id="2c920-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="2c920-124">Imidlertid vil bestillinger starte på 9:00 som det første starttidspunktet for tilordningsomfanget.</span><span class="sxs-lookup"><span data-stu-id="2c920-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="2c920-125">Ressurs C og D: Ressursene befinner seg i andre tidssoner, begge forskjellige fra hverandre og prosjektet, og bestillinger startes ikke tidligere enn de respektive starttidspunktene som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="2c920-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="2c920-126">Enhet</span><span class="sxs-lookup"><span data-stu-id="2c920-126">Entity</span></span>  |<span data-ttu-id="2c920-127">Kalender</span><span class="sxs-lookup"><span data-stu-id="2c920-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="2c920-128">Prosjektkalendermal</span><span class="sxs-lookup"><span data-stu-id="2c920-128">Project calendar template</span></span>   | ![prosjektkalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="2c920-130">Ressurs A</span><span class="sxs-lookup"><span data-stu-id="2c920-130">Resource A</span></span>  | ![Ressurs A-kalender](media/reconcile-assignments-06.png) |
|<span data-ttu-id="2c920-132">Ressurs B</span><span class="sxs-lookup"><span data-stu-id="2c920-132">Resource B</span></span>  |  ![Ressurs B-kalender](media/reconcile-assignments-07.png) |
|<span data-ttu-id="2c920-134">Ressurs C</span><span class="sxs-lookup"><span data-stu-id="2c920-134">Resource C</span></span>  |  ![Ressurs C-kalender](media/reconcile-assignments-08.png) |
|<span data-ttu-id="2c920-136">Ressurs D</span><span class="sxs-lookup"><span data-stu-id="2c920-136">Resource D</span></span>  | ![Ressurs D-kalender](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="2c920-138">Når du navigerer til **Avstemming**-visningen, vises ressurstilordningene og de tilknyttede bestillingsmanglene.</span><span class="sxs-lookup"><span data-stu-id="2c920-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Avstemmingsvisning før utvidelse](media/reconcile-assignments-10.png)

<span data-ttu-id="2c920-140">Etter at du har brukt funksjonen for å forlenge bestillingen til hver ressurs, blir alle bestillinger utvidet for hver ressurs, fordi arbeidstiden til hver ressurs overlappet med konturene av mangelen.</span><span class="sxs-lookup"><span data-stu-id="2c920-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Avstemmingsvisning etter bestillingsutvidelse](media/reconcile-assignments-11.png) 

<span data-ttu-id="2c920-142">Legg merke til at en nærmere kikk på detaljene i bestillingene viser forskjeller i starttidspunktet for bestillingene.</span><span class="sxs-lookup"><span data-stu-id="2c920-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="2c920-143">Bestillingene starter tidligst på starttidspunktet til tilordningsprofilen, og ikke senere enn den tilgjengelige starttiden til ressursen.</span><span class="sxs-lookup"><span data-stu-id="2c920-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nye bestillinger for ressursene på planleggingstavlen](media/reconcile-assignments-12.png)
