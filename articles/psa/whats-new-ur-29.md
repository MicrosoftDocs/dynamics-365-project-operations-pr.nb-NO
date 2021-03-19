---
title: Hva er nytt eller endret i Project Service Automation Update Release 29, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 29, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499683"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="b18d9-103">Hva er nytt eller endret i Project Service Automation Update Release 29, V3</span><span class="sxs-lookup"><span data-stu-id="b18d9-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b18d9-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b18d9-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b18d9-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="b18d9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b18d9-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="b18d9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b18d9-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="b18d9-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b18d9-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b18d9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b18d9-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 29.</span><span class="sxs-lookup"><span data-stu-id="b18d9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="b18d9-110">Denne versjonen har buildnummeret V3.10.45.98, og er generelt tilgjengelig via en egen oppdatering i februar 2021.</span><span class="sxs-lookup"><span data-stu-id="b18d9-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="b18d9-111">Update Release 29</span><span class="sxs-lookup"><span data-stu-id="b18d9-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b18d9-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="b18d9-112">Bug fixes</span></span>

<span data-ttu-id="b18d9-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="b18d9-113">**Time and Expense**</span></span>

<span data-ttu-id="b18d9-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b18d9-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b18d9-115">Brukere kan ikke se arbeidstimer som er logget på dager som ikke er arbeidsdager, i rutenettet for tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="b18d9-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="b18d9-116">Godkjente utgiftsoppføringer kan redigeres i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="b18d9-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="b18d9-117">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="b18d9-117">**Project Management**</span></span>

<span data-ttu-id="b18d9-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b18d9-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b18d9-119">Mangler valideringslogikk for å sikre at arbeidstimer for ressurstilordning ikke kan være negative.</span><span class="sxs-lookup"><span data-stu-id="b18d9-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="b18d9-120">Den egendefinerte handlingen **AssignResourcesForTask** oppdaterer alle felter i stedet for bare endrede felter.</span><span class="sxs-lookup"><span data-stu-id="b18d9-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="b18d9-121">Når du kopierer et prosjekt i et miljø med plugin-moduler eller arbeidsflyter som er registrert på **CreateProject**-hendelsen, oppdateres ikke **msdyn_bulkgenerationstatus**-attributtet hvis **CopyWBSToProject** mislykkes.</span><span class="sxs-lookup"><span data-stu-id="b18d9-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="b18d9-122">Når du utvider prosjektkalenderen, sorteres ikke arbeidsdagene i stigende rekkefølge, noe som fører til at enkelte prosjektoppgaveoppdateringer mislykkes.</span><span class="sxs-lookup"><span data-stu-id="b18d9-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="b18d9-123">Endring av prosjektlederen i et eksisterende prosjekt utløser logikken for standardisering av organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="b18d9-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="b18d9-124">**Salg**</span><span class="sxs-lookup"><span data-stu-id="b18d9-124">**Sales**</span></span>

<span data-ttu-id="b18d9-125">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="b18d9-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="b18d9-126">Fanen **Kontraktytelse** på **Kontrakt**-siden mislykkes stille under initialiseringen når det ikke finnes kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="b18d9-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
