---
title: Hva er nytt eller endret i Project Service Automation Update Release 14, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147170"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="a06f7-103">Project Service Automation, Update Release 14, V3</span><span class="sxs-lookup"><span data-stu-id="a06f7-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a06f7-104">Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="a06f7-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="a06f7-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="a06f7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a06f7-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a06f7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a06f7-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="a06f7-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="a06f7-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a06f7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a06f7-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 14.</span><span class="sxs-lookup"><span data-stu-id="a06f7-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="a06f7-110">Denne versjonen har buildnummer V3.10.4.21 og er tilgjengelig i henhold til følgende tidsplan:</span><span class="sxs-lookup"><span data-stu-id="a06f7-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="a06f7-111">**Generell tilgjengelighet (egen oppdatering):** januar 2020</span><span class="sxs-lookup"><span data-stu-id="a06f7-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="a06f7-112">**Automatisk oppdatering:** februar 2020</span><span class="sxs-lookup"><span data-stu-id="a06f7-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="a06f7-113">Update Release 14</span><span class="sxs-lookup"><span data-stu-id="a06f7-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="a06f7-114">Forbedringer</span><span class="sxs-lookup"><span data-stu-id="a06f7-114">Enhancements</span></span>

- <span data-ttu-id="a06f7-115">Sales</span><span class="sxs-lookup"><span data-stu-id="a06f7-115">Sales</span></span>

     - <span data-ttu-id="a06f7-116">Egendefinerte feltverdier fra **Tilbudslinjedetaljer** kopieres til **Detaljer for prosjektkontraktlinjer** når et tilbud blir oppdatert til **Lukket som vunnet**.</span><span class="sxs-lookup"><span data-stu-id="a06f7-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="a06f7-117">Bekreftede prosjekter kan bli **Lukket som tapte**.</span><span class="sxs-lookup"><span data-stu-id="a06f7-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="a06f7-118">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="a06f7-118">Resource Management</span></span>

     - <span data-ttu-id="a06f7-119">Når du utvider bestillinger, blir brukerne bedt om å oppgi en bekreftelsesdialogboks for å summere bestillingsresultater og opprette en kobling for å vedlikeholde bestillinger.</span><span class="sxs-lookup"><span data-stu-id="a06f7-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="a06f7-120">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="a06f7-120">Bug fixes</span></span>

- <span data-ttu-id="a06f7-121">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="a06f7-121">Time and Expense</span></span>

     - <span data-ttu-id="a06f7-122">Fikset: Forbedret brukeropplevelsen når brukeren ikke har valgt noen oppføringer som skal rettes opp.</span><span class="sxs-lookup"><span data-stu-id="a06f7-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="a06f7-123">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="a06f7-123">Resource Management</span></span>

     - <span data-ttu-id="a06f7-124">Fikset: Bestilling av en ressurs flere ganger overflyter navnet på den bestillbare ressursen.</span><span class="sxs-lookup"><span data-stu-id="a06f7-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="a06f7-125">Sales</span><span class="sxs-lookup"><span data-stu-id="a06f7-125">Sales</span></span>

     - <span data-ttu-id="a06f7-126">Fikset: Total salgspris beregnes ikke før brukeren også har angitt en kostpris for utgiftsestimater i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a06f7-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="a06f7-127">Fikset: Lukking av et tilbud som **Vunnet** mislykkes hvis den tilknyttede prosjektkontrakten ikke er i **Utkast**-tilstand.</span><span class="sxs-lookup"><span data-stu-id="a06f7-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

