---
title: Hva er nytt eller endret i Project Service Automation Update Release 28, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150635"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="045fd-103">Hva er nytt eller endret i Project Service Automation Update Release 28, V3</span><span class="sxs-lookup"><span data-stu-id="045fd-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="045fd-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="045fd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="045fd-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="045fd-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="045fd-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="045fd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="045fd-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="045fd-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="045fd-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="045fd-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="045fd-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endret for Project Service Automation V3, Update Release 28. Denne versjonen har et buildnummer V3.10.46.32 og er allment tilgjengelig via en egen oppdatering i januar 2021.</span><span class="sxs-lookup"><span data-stu-id="045fd-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="045fd-110">Update Release 28</span><span class="sxs-lookup"><span data-stu-id="045fd-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="045fd-111">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="045fd-111">Bug fixes</span></span>

<span data-ttu-id="045fd-112">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="045fd-112">**Time and Expense**</span></span>

<span data-ttu-id="045fd-113">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="045fd-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="045fd-114">Brukere kan bruke **Masseredigering** til å oppdatere tidsoppføringer som er godkjent og sendt.</span><span class="sxs-lookup"><span data-stu-id="045fd-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="045fd-115">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="045fd-115">**Project Management**</span></span>

<span data-ttu-id="045fd-116">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="045fd-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="045fd-117">I tilfeller der oppgave-GUID tolkes som et tall, kan ikke oppgaver åpnes for redigering ved hjelp av **Rediger oppgave** på båndet på siden **Arbeidsnedbrytningsstruktur**.</span><span class="sxs-lookup"><span data-stu-id="045fd-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="045fd-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="045fd-118">**Sales**</span></span>

<span data-ttu-id="045fd-119">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="045fd-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="045fd-120">Det genereres et nullreferanseunntak når plugin-modulen **GetEstimatesForProject** startes.</span><span class="sxs-lookup"><span data-stu-id="045fd-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="045fd-121">**Merk som klar for fakturering** i milepælrutenettet oppdaterer bare attributter delvis, med unntak av attributtet **InvoiceStatus**, som blir oppdatert.</span><span class="sxs-lookup"><span data-stu-id="045fd-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

