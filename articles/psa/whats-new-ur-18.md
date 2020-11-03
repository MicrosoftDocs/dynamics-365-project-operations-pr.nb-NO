---
title: Hva er nytt eller endret i Project Service Automation Update Release 18, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081574"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="2bfbd-103">Project Service Automation, Update Release 18, V3</span><span class="sxs-lookup"><span data-stu-id="2bfbd-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="2bfbd-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2bfbd-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2bfbd-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2bfbd-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2bfbd-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2bfbd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2bfbd-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 18.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="2bfbd-110">Denne versjonen har et build-nummer på V3.10.8.12 og er generelt tilgjengelig via en egen oppdatering i april 2020.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="2bfbd-111">Update Release 18</span><span class="sxs-lookup"><span data-stu-id="2bfbd-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2bfbd-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="2bfbd-112">Bug fixes</span></span>

<span data-ttu-id="2bfbd-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="2bfbd-113">**Time and Expense**</span></span>

- <span data-ttu-id="2bfbd-114">Løst: Flytene **Tilbake** , **Forespørsel** og **Avbryt godkjenning** bruker unntak med uklare feilmeldinger.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="2bfbd-115">Løst: Når **Avbryt godkjenning** mislykkes for en utgift, brukes det ikke en relevant unntaksfeil.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="2bfbd-116">Løst: Rutenettet Tidsoppføring håndterer feilaktig ikke-arbeidsdager i Australia etter bytte til sommertid (DST) i oktober.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="2bfbd-117">Løst: Feil standardlogikk forhindrer sending av utgifter.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="2bfbd-118">Løst: Når tidsoppføringsgodkjenning mislykkes, beholdes godkjenningen i tilstanden **Ventende**.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="2bfbd-119">Løst: SQL-feil ved massegodkjenninger (vranglås/tidsavbrudd).</span><span class="sxs-lookup"><span data-stu-id="2bfbd-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="2bfbd-120">Løst: Betydelige ytelsesproblemer i brukeropplevelsen forårsaket av oppdatering av teammedlemmer under godkjenning av tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="2bfbd-121">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="2bfbd-121">**Project Management**</span></span>

- <span data-ttu-id="2bfbd-122">Løst: Tidssonevarsel flyttet fra **Avstemming** -visningen til **Prosjekt** -hovedskjemaet.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="2bfbd-123">Løst: Kalendermalen brukes ikke som standard når et nytt prosjektskjema åpnes.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="2bfbd-124">Løst: For Chromium-baserte nettlesere kan ikke brukere enkelt velge foregående oppgaver de vil slette.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="2bfbd-125">Løst: Oppretting eller kopiering av **Prosjekt fra tom mal** henter urelaterte tilordninger.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="2bfbd-126">Løst: I bestemte kanttilfeller fører oppretting av en ny oppgave fra oppgaverutenettet at dupliserte oppføringer blir opprettet.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="2bfbd-127">Løst: I manuell modus kan ikke brukere oppdatere oppgavestartdatoer til senere enn gjeldende dato lagret.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="2bfbd-128">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="2bfbd-128">**Resource Management**</span></span>

- <span data-ttu-id="2bfbd-129">Løst: **Avstemming** -visningens rad for delsum beregner feilaktig bestillingsavvik etter at bestillinger er utvidet.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="2bfbd-130">Løst: **Avstemming** -visningen viser feilaktig ressurstilordninger når ressursen som kan bestilles, har en kalender som ikke samsvarer med prosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="2bfbd-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="2bfbd-131">**Sales**</span></span>

- <span data-ttu-id="2bfbd-132">Løst: Når tidsoppføringer godkjennes på nytt ( **Godkjenn > Avbryt >** godkjenn på nytt), blir det opprettet en duplikat faktisk ikke-belastbar.</span><span class="sxs-lookup"><span data-stu-id="2bfbd-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
