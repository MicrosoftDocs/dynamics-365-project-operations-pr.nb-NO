---
title: Hva er nytt eller endret i Project Service Automation Update Release 32, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129678"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="30a55-103">Hva er nytt eller endret i Project Service Automation Update Release 32, V3</span><span class="sxs-lookup"><span data-stu-id="30a55-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="30a55-104">Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen.</span><span class="sxs-lookup"><span data-stu-id="30a55-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="30a55-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="30a55-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="30a55-106">Den er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="30a55-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="30a55-107">Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="30a55-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="30a55-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="30a55-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="30a55-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 32.</span><span class="sxs-lookup"><span data-stu-id="30a55-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="30a55-110">Denne versjonen har buildnummeret V3.10.53.108 og er vanligvis tilgjengelig via en egenoppdatering i juni 2021.</span><span class="sxs-lookup"><span data-stu-id="30a55-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="30a55-111">Update Release 32</span><span class="sxs-lookup"><span data-stu-id="30a55-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="30a55-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="30a55-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="30a55-113">Generelt</span><span class="sxs-lookup"><span data-stu-id="30a55-113">General</span></span>

- <span data-ttu-id="30a55-114">Når en større oppgradering mislykkes, bør bare hovedinngangspunktene i programmet blokkeres for å sikre at delte enheter fremdeles er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="30a55-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="30a55-115">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="30a55-115">Time and Expense</span></span>

<span data-ttu-id="30a55-116">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="30a55-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="30a55-117">**TimeEntriesImportFromResourceAssignment** vedlikeholder ikke start- og sluttidspunktene for omfangsdelen for ressurstilordningen.</span><span class="sxs-lookup"><span data-stu-id="30a55-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="30a55-118">Når du velger **Åpne oppføring** i rutenettet for **Tidsoppføring**, kan det hende du ikke kan velge andre skjemaer.</span><span class="sxs-lookup"><span data-stu-id="30a55-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="30a55-119">Når du importerer tilordninger til tidsoppføringer, kan klientkodespørringen generere en lang URL-adresse som mislykkes i spørringen.</span><span class="sxs-lookup"><span data-stu-id="30a55-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="30a55-120">Når en verdi er slettet fra en celle i rutenettet for **Tidsoppføring**, blir ikke fokuset værende i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="30a55-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="30a55-121">**Avvis**-knappen er fjernet fra visningen **Behandling av godkjenninger** for moderne godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="30a55-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="30a55-122">Stabiliteten og ytelsen til massegodkjenning av tidsregistrering påvirkes av vranglåser, og det oppstår en feil under behandling av tilpassinger som er relatert til **Tidsoppføring**-enheten.</span><span class="sxs-lookup"><span data-stu-id="30a55-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="30a55-123">Prosjektplanlegging</span><span class="sxs-lookup"><span data-stu-id="30a55-123">Project Planning</span></span>

- <span data-ttu-id="30a55-124">Det genereres et nullreferanseunntak når du oppdaterer et prosjekt som har en nullverdi i feltet **Kontraktenhet**.</span><span class="sxs-lookup"><span data-stu-id="30a55-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="30a55-125">**Oppdater totalsummer for prosjektet** feilberegner gjenstående kostnad og gjenstående salg for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="30a55-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="30a55-126">Overflødige prisberegninger påvirker ytelsen som er relatert til oppdateringer for ressurstilordninger.</span><span class="sxs-lookup"><span data-stu-id="30a55-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="30a55-127">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="30a55-127">Resource Management</span></span>

<span data-ttu-id="30a55-128">Følgende problem er løst:</span><span class="sxs-lookup"><span data-stu-id="30a55-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="30a55-129">Når kalenderkapasiteten for en ressurs som kan reserves, er mer enn 1, gjenkjenner Project Service Automation feilaktig kapasiteten som 0 (null).</span><span class="sxs-lookup"><span data-stu-id="30a55-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="30a55-130">Derfor oppstår en uendelig løkkei tidsplanvisningen.</span><span class="sxs-lookup"><span data-stu-id="30a55-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="30a55-131">Salg</span><span class="sxs-lookup"><span data-stu-id="30a55-131">Sales</span></span>

<span data-ttu-id="30a55-132">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="30a55-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="30a55-133">Når det opprettes en journallinje som har en egendefinert transaksjonstype, oppstår følgende nullreferanseunntak: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="30a55-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="30a55-134">Roller og kategorier som er deaktivert før et tilbud er kopiert, må ikke legges til belastbare roller og kategorier for det nylig kopierte tilbud.</span><span class="sxs-lookup"><span data-stu-id="30a55-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="30a55-135">Dokumentdatoen og regnskapsdatoen er ikke justert med startdatoen som er angitt på en fakturalinjedetalj som opprettes direkte på et fakturautkast.</span><span class="sxs-lookup"><span data-stu-id="30a55-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="30a55-136">Nullreferanseunntak genereres i scenarier som er relatert til inaktivering av roller og kategorier før et tilbud kopieres.</span><span class="sxs-lookup"><span data-stu-id="30a55-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="30a55-137">Handlingen **Oppdater priser** på **Prosjekter**-siden oppdaterer ikke kostnadsestimater og materielle estimater.</span><span class="sxs-lookup"><span data-stu-id="30a55-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
