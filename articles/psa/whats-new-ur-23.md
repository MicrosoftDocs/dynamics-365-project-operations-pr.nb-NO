---
title: Hva er nytt eller endret i Project Service Automation Update Release 23, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 23, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150050"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="4104e-103">Project Service Automation, Update Release 23, V3</span><span class="sxs-lookup"><span data-stu-id="4104e-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4104e-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4104e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4104e-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="4104e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4104e-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4104e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4104e-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="4104e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4104e-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4104e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4104e-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 23.</span><span class="sxs-lookup"><span data-stu-id="4104e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="4104e-110">Denne versjonen har buildnummer V3.10.34.30 og er generelt tilgjengelig via en egen oppdatering i august 2020.</span><span class="sxs-lookup"><span data-stu-id="4104e-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="4104e-111">Update Release 23</span><span class="sxs-lookup"><span data-stu-id="4104e-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4104e-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="4104e-112">Bug fixes</span></span>

<span data-ttu-id="4104e-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="4104e-113">**Time and Expense**</span></span>

<span data-ttu-id="4104e-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="4104e-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="4104e-115">Håndtering av kantsak i **Slett prosjektteammedlem** for å gi et meningsfullt unntak.</span><span class="sxs-lookup"><span data-stu-id="4104e-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="4104e-116">Import av tilordning fører til et tomt fjerningsskjermbilde.</span><span class="sxs-lookup"><span data-stu-id="4104e-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="4104e-117">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="4104e-117">**Resource Management**</span></span>

<span data-ttu-id="4104e-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="4104e-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="4104e-119">**Rutenettet for ressursutnyttelse** viser feil data når tidsskalane er mer enn fem dager.</span><span class="sxs-lookup"><span data-stu-id="4104e-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="4104e-120">Når kunder oppretter en ressurs som kan reserverer, kan ikke plugin-modulen automatisk legge til ressursen i en Microsoft Office 365-gruppe.</span><span class="sxs-lookup"><span data-stu-id="4104e-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="4104e-121">**Avstemming**-visningen viser manuelle konturer i **Uke**- eller **Måned**-visningen.</span><span class="sxs-lookup"><span data-stu-id="4104e-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="4104e-122">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="4104e-122">**Project Management**</span></span>

<span data-ttu-id="4104e-123">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="4104e-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="4104e-124">Et stort antall **RetrieveMultiple for usersettings**-enheter forårsaker redusert ytelse for prosjektgodkjenninger og andre operasjoner.</span><span class="sxs-lookup"><span data-stu-id="4104e-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="4104e-125">Ressursoppslaget for rutenettet **Oppgaveplanlegging** er begrenset til bare å vise opptil fem teammedlemmer fra prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="4104e-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="4104e-126">Ressursoppslaget for rutenettet **Oppgaveplanlegging** filtrerer ikke inaktive ressurser.</span><span class="sxs-lookup"><span data-stu-id="4104e-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="4104e-127">Manuell modus fungerer ikke som forventet i arbeidsnedbrytingsstrukturen for prosjektplanlegging.</span><span class="sxs-lookup"><span data-stu-id="4104e-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="4104e-128">Rutenettet **Oppgaveplanlegging** viser **inaktive transaksjonskategorier**.</span><span class="sxs-lookup"><span data-stu-id="4104e-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="4104e-129">Rutenettet **Ressurstilordning** runder av på feil måte når en oppgave har flere tilordninger.</span><span class="sxs-lookup"><span data-stu-id="4104e-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="4104e-130">Avrundingsverdier er forskjellige mellom planlagt kostnad og faktisk kostnad for én enkelt oppgave.</span><span class="sxs-lookup"><span data-stu-id="4104e-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="4104e-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4104e-131">**Sales**</span></span>

<span data-ttu-id="4104e-132">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="4104e-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="4104e-133">Dobbeltklikk på **Hent alle transaksjonskategorier** oppretter flere linjer.</span><span class="sxs-lookup"><span data-stu-id="4104e-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
