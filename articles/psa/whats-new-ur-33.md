---
title: Hva er nytt eller endret i Project Service Automation Update Release 33, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334578"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="86e98-103">Hva er nytt eller endret i Project Service Automation Update Release 33, V3</span><span class="sxs-lookup"><span data-stu-id="86e98-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="86e98-104">Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="86e98-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="86e98-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="86e98-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="86e98-106">Den er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="86e98-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="86e98-107">Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="86e98-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="86e98-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="86e98-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="86e98-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 33.</span><span class="sxs-lookup"><span data-stu-id="86e98-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="86e98-110">Denne versjonen har et build-nummer på V3.10.54.98 og er allment tilgjengelig via en egenoppdatering i juli 2021.</span><span class="sxs-lookup"><span data-stu-id="86e98-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="86e98-111">Update Release 33</span><span class="sxs-lookup"><span data-stu-id="86e98-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="86e98-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="86e98-112">Bug fixes</span></span>

<span data-ttu-id="86e98-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="86e98-113">**Time and Expense**</span></span>

<span data-ttu-id="86e98-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="86e98-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="86e98-115">To låste felter, **msdyn_description** og **msdyn_externaldescription** kan redigeres etter sending.</span><span class="sxs-lookup"><span data-stu-id="86e98-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="86e98-116">Det vises en feilmelding hvis det opprettes en utgift som ikke er relatert til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="86e98-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="86e98-117">Når det opprettes en tidsoppføring, brukes en inaktiv rolle som standard i ressursrollen.</span><span class="sxs-lookup"><span data-stu-id="86e98-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="86e98-118">Journallinjer som er knyttet til en tilbakekalt og slettet utgift, slettes ikke.</span><span class="sxs-lookup"><span data-stu-id="86e98-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="86e98-119">Oppdater visningen **Prosjektoppgaveliste** i **Hurtigopprettingsskjema for tidsoppføring** for å endre datoen som vises som standard, til startdatoen for oppgaven.</span><span class="sxs-lookup"><span data-stu-id="86e98-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="86e98-120">Når du oppretter en tidsoppføring fra fanen **Relatert** for ressursen som kan reserveres, opprettes tidsoppføringen feil for den påloggede brukeren i stedet for den overordnede ressursen som kan reserveres.</span><span class="sxs-lookup"><span data-stu-id="86e98-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="86e98-121">Nye felter er lagt til i dialogboksen **MDD for massegodkjenning**.</span><span class="sxs-lookup"><span data-stu-id="86e98-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="86e98-122">**Prosjektplanlegging**</span><span class="sxs-lookup"><span data-stu-id="86e98-122">**Project planning**</span></span>

<span data-ttu-id="86e98-123">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="86e98-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="86e98-124">Treg prosjektopprettingsytelse når maler for prosjektarbeidstimer brukes med komplekse kalendere.</span><span class="sxs-lookup"><span data-stu-id="86e98-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="86e98-125">Når startdatoen er større enn sluttdatoen, vises det en feil i kopieringsprosjektmalen på grunn av forskjeller i tidskomponenten i hvert felt.</span><span class="sxs-lookup"><span data-stu-id="86e98-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="86e98-126">**Ressursstyring**</span><span class="sxs-lookup"><span data-stu-id="86e98-126">**Resource management**</span></span>

<span data-ttu-id="86e98-127">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="86e98-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="86e98-128">En feil parameter brukes i spørringen om ressursutnyttelse, og XML fører til feil filterresultater i rutenettet **Ressursutnyttelse**.</span><span class="sxs-lookup"><span data-stu-id="86e98-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="86e98-129">Bekreftelsen **Utvid bestillinger** viser feil sluttdato for bestillinger.</span><span class="sxs-lookup"><span data-stu-id="86e98-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="86e98-130">**Salg**</span><span class="sxs-lookup"><span data-stu-id="86e98-130">**Sales**</span></span>

<span data-ttu-id="86e98-131">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="86e98-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="86e98-132">Det vises en feilmelding hvis en kategoripris opprettes med manglende verdier.</span><span class="sxs-lookup"><span data-stu-id="86e98-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="86e98-133">Det vises en feilmelding hvis en kontraktlinjemilepæl opprettes uten en ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="86e98-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
