---
title: Hva er nytt eller endret i Project Service Automation Update Release 17.5, hurtigreparasjon, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 17.5, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 03/13/2020
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
ms.openlocfilehash: 359eb8f8ca41d69d4f30dd44497a4deb6a6c4f8d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081575"
---
# <a name="project-service-automation-update-release-175-v3"></a><span data-ttu-id="dd047-103">Project Service Automation, Update Release 17.5, V3</span><span class="sxs-lookup"><span data-stu-id="dd047-103">Project Service Automation Update Release 17.5, V3</span></span>

<span data-ttu-id="dd047-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="dd047-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="dd047-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="dd047-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="dd047-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="dd047-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dd047-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="dd047-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="dd047-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dd047-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dd047-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for V3, Update Release 17.5.</span><span class="sxs-lookup"><span data-stu-id="dd047-109">This topic lists the features and fixes that are new or changed for V3, Update Release 17.5.</span></span> <span data-ttu-id="dd047-110">Denne versjonen har buildnummer V3.10.7.32 og er generelt tilgjengelig via en egen oppdatering fra mars 2020.</span><span class="sxs-lookup"><span data-stu-id="dd047-110">This version has a build number of V3.10.7.32 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-175"></a><span data-ttu-id="dd047-111">Update Release 17.5</span><span class="sxs-lookup"><span data-stu-id="dd047-111">Update Release 17.5</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dd047-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="dd047-112">Bug fixes</span></span>


<span data-ttu-id="dd047-113">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="dd047-113">**Project Management**</span></span>

- <span data-ttu-id="dd047-114">Løst: Synkroniseringsproblemer på serversiden som oppstod for oppgaver med lang varighet.</span><span class="sxs-lookup"><span data-stu-id="dd047-114">Fixed: Addressed server-side synchronization issues that occur with long duration tasks.</span></span>
- <span data-ttu-id="dd047-115">Løst: 24-timers arbeidstidsmaler som unøyaktig la til en ekstra dag i aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="dd047-115">Fixed: Addressed 24-hour work hour templates inaccurately adding an additional day to tasks.</span></span>
- <span data-ttu-id="dd047-116">Løst: +13 GMT arbeidstidsmaler som unøyaktig forskjøv oppgavene én dag fremover.</span><span class="sxs-lookup"><span data-stu-id="dd047-116">Fixed: Addressed +13 GMT work hour templates inaccurately shifting tasks one day ahead.</span></span>

