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
ms.openlocfilehash: 0e1ff0db42adb8b991b26dca1585bd603b2e2276
ms.sourcegitcommit: f57408d6637f670b920d7ce95f8ace8eb1963093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/17/2021
ms.locfileid: "5664655"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="fbe05-103">Hva er nytt eller endret i Project Service Automation Update Release 29, V3</span><span class="sxs-lookup"><span data-stu-id="fbe05-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fbe05-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fbe05-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fbe05-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="fbe05-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fbe05-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="fbe05-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fbe05-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="fbe05-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fbe05-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fbe05-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fbe05-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 29.</span><span class="sxs-lookup"><span data-stu-id="fbe05-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="fbe05-110">Denne versjonen har buildnummeret V3.10.47.7, og er generelt tilgjengelig via en egen oppdatering i februar 2021.</span><span class="sxs-lookup"><span data-stu-id="fbe05-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="fbe05-111">Update Release 29</span><span class="sxs-lookup"><span data-stu-id="fbe05-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fbe05-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="fbe05-112">Bug fixes</span></span>

<span data-ttu-id="fbe05-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="fbe05-113">**Time and Expense**</span></span>

<span data-ttu-id="fbe05-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="fbe05-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbe05-115">Brukere kan ikke se arbeidstimer som er logget på dager som ikke er arbeidsdager, i rutenettet for tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="fbe05-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="fbe05-116">Godkjente utgiftsoppføringer kan redigeres i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="fbe05-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="fbe05-117">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="fbe05-117">**Project Management**</span></span>

<span data-ttu-id="fbe05-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="fbe05-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbe05-119">Mangler valideringslogikk for å sikre at arbeidstimer for ressurstilordning ikke kan være negative.</span><span class="sxs-lookup"><span data-stu-id="fbe05-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="fbe05-120">Den egendefinerte handlingen **AssignResourcesForTask** oppdaterer alle felter i stedet for bare endrede felter.</span><span class="sxs-lookup"><span data-stu-id="fbe05-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="fbe05-121">Når du kopierer et prosjekt i et miljø med plugin-moduler eller arbeidsflyter som er registrert på **CreateProject**-hendelsen, oppdateres ikke **msdyn_bulkgenerationstatus**-attributtet hvis **CopyWBSToProject** mislykkes.</span><span class="sxs-lookup"><span data-stu-id="fbe05-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="fbe05-122">Når du utvider prosjektkalenderen, sorteres ikke arbeidsdagene i stigende rekkefølge, noe som fører til at enkelte prosjektoppgaveoppdateringer mislykkes.</span><span class="sxs-lookup"><span data-stu-id="fbe05-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="fbe05-123">Endring av prosjektlederen i et eksisterende prosjekt utløser logikken for standardisering av organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="fbe05-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="fbe05-124">**Salg**</span><span class="sxs-lookup"><span data-stu-id="fbe05-124">**Sales**</span></span>

<span data-ttu-id="fbe05-125">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="fbe05-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbe05-126">Fanen **Kontraktytelse** på **Kontrakt**-siden mislykkes stille under initialiseringen når det ikke finnes kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="fbe05-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
