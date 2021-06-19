---
title: Hva er nytt eller endret i Project Service Automation Update Release 29, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 29, V3.
author: ruhercul
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010483"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="cc620-103">Hva er nytt eller endret i Project Service Automation Update Release 29, V3</span><span class="sxs-lookup"><span data-stu-id="cc620-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="cc620-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="cc620-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="cc620-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="cc620-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="cc620-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="cc620-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="cc620-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="cc620-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="cc620-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="cc620-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="cc620-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 29.</span><span class="sxs-lookup"><span data-stu-id="cc620-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="cc620-110">Denne versjonen har buildnummeret V3.10.47.7, og er generelt tilgjengelig via en egen oppdatering i februar 2021.</span><span class="sxs-lookup"><span data-stu-id="cc620-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="cc620-111">Update Release 29</span><span class="sxs-lookup"><span data-stu-id="cc620-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="cc620-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="cc620-112">Bug fixes</span></span>

<span data-ttu-id="cc620-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="cc620-113">**Time and Expense**</span></span>

<span data-ttu-id="cc620-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cc620-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc620-115">Brukere kan ikke se arbeidstimer som er logget på dager som ikke er arbeidsdager, i rutenettet for tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="cc620-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="cc620-116">Godkjente utgiftsoppføringer kan redigeres i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cc620-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="cc620-117">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="cc620-117">**Project Management**</span></span>

<span data-ttu-id="cc620-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cc620-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc620-119">Mangler valideringslogikk for å sikre at arbeidstimer for ressurstilordning ikke kan være negative.</span><span class="sxs-lookup"><span data-stu-id="cc620-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="cc620-120">Den egendefinerte handlingen **AssignResourcesForTask** oppdaterer alle felter i stedet for bare endrede felter.</span><span class="sxs-lookup"><span data-stu-id="cc620-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="cc620-121">Når du kopierer et prosjekt i et miljø med plugin-moduler eller arbeidsflyter som er registrert på **CreateProject**-hendelsen, oppdateres ikke **msdyn_bulkgenerationstatus**-attributtet hvis **CopyWBSToProject** mislykkes.</span><span class="sxs-lookup"><span data-stu-id="cc620-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="cc620-122">Når du utvider prosjektkalenderen, sorteres ikke arbeidsdagene i stigende rekkefølge, noe som fører til at enkelte prosjektoppgaveoppdateringer mislykkes.</span><span class="sxs-lookup"><span data-stu-id="cc620-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="cc620-123">Endring av prosjektlederen i et eksisterende prosjekt utløser logikken for standardisering av organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="cc620-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="cc620-124">**Salg**</span><span class="sxs-lookup"><span data-stu-id="cc620-124">**Sales**</span></span>

<span data-ttu-id="cc620-125">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="cc620-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="cc620-126">Fanen **Kontraktytelse** på **Kontrakt**-siden mislykkes stille under initialiseringen når det ikke finnes kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="cc620-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>