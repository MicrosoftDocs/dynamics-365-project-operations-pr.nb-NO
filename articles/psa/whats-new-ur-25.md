---
title: Hva er nytt eller endret i Project Service Automation Update Release 25, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183555"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="6c33b-103">Hva er nytt eller endret i Project Service Automation Update Release 25, V3</span><span class="sxs-lookup"><span data-stu-id="6c33b-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="6c33b-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6c33b-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6c33b-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="6c33b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6c33b-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6c33b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6c33b-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="6c33b-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6c33b-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6c33b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6c33b-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endret for Project Service Automation V3, Update Release 25. Denne versjonen har et buildnummer V 3.10.43.76 og er allment tilgjengelig via en egen oppdatering i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="6c33b-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="6c33b-110">Update Release 25</span><span class="sxs-lookup"><span data-stu-id="6c33b-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6c33b-111">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="6c33b-111">Bug fixes</span></span>

<span data-ttu-id="6c33b-112">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="6c33b-112">**Time and Expense**</span></span>

<span data-ttu-id="6c33b-113">Følgende problem er løst:</span><span class="sxs-lookup"><span data-stu-id="6c33b-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="6c33b-114">Tidsregistreringsdiagrammet viser ytterligere data basert på for stor intervall som hentes.</span><span class="sxs-lookup"><span data-stu-id="6c33b-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="6c33b-115">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="6c33b-115">**Resource Management**</span></span>

<span data-ttu-id="6c33b-116">Følgende problem er løst:</span><span class="sxs-lookup"><span data-stu-id="6c33b-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="6c33b-117">Lagt til Package Deployer for å hoppe over Universal Resource Scheduling-oppdateringsimporten hvis det allerede finnes en oppdatering med høyere versjon.</span><span class="sxs-lookup"><span data-stu-id="6c33b-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="6c33b-118">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="6c33b-118">**Project Management**</span></span>

<span data-ttu-id="6c33b-119">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="6c33b-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c33b-120">Korrigerte avrundings- og valutakursavvik som fører til feil planlagt kostnad i prosjektsporingsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="6c33b-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="6c33b-121">Støtter muligheten til å vise to eller flere reaksjonsrutenett i **Prosjekt**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="6c33b-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="6c33b-122">Gitt validering for å gi mulighet til å tilordne en aktivitet etter sluttdatoen for kalenderen, noe som fører til en mislykket ressurstilordning.</span><span class="sxs-lookup"><span data-stu-id="6c33b-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="6c33b-123">Forbedret feilhåndtering for å løse nullreferanseunntak som genereres fra følgende:</span><span class="sxs-lookup"><span data-stu-id="6c33b-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="6c33b-124">Plugin-modul **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="6c33b-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="6c33b-125">**PreValidateProjectTaskCreate** når en prosjektoppgave opprettes uten et tilknyttet prosjekt</span><span class="sxs-lookup"><span data-stu-id="6c33b-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="6c33b-126">Plugin-modul **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="6c33b-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="6c33b-127">Plugin-modul **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="6c33b-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="6c33b-128">Plugin-modul **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="6c33b-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="6c33b-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="6c33b-129">**Sales**</span></span>

<span data-ttu-id="6c33b-130">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="6c33b-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="6c33b-131">Forbedret feilbehandling for å løse nullreferanseunntak generert fra **Kopier prosjekt: estimering av administrasjon av hjelperessurser**.</span><span class="sxs-lookup"><span data-stu-id="6c33b-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="6c33b-132">**Ikke klar til fakturering** på en **Faktureringsrestanse for Tid og materiale** fjerner ikke faktureringsstatus.</span><span class="sxs-lookup"><span data-stu-id="6c33b-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="6c33b-133">Korrigerte **Pris**-knapper med feiletikett i kategorien **Rollepris** og **Katalogelementer**.</span><span class="sxs-lookup"><span data-stu-id="6c33b-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>
