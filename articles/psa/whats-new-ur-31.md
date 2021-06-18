---
title: Hva er nytt eller endret i Project Service Automation Update Release 31, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 31, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999143"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="d9b36-103">Hva er nytt eller endret i Project Service Automation Update Release 31, V3</span><span class="sxs-lookup"><span data-stu-id="d9b36-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d9b36-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d9b36-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d9b36-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="d9b36-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d9b36-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d9b36-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d9b36-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="d9b36-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d9b36-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d9b36-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d9b36-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 31.</span><span class="sxs-lookup"><span data-stu-id="d9b36-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="d9b36-110">Denne versjonen har et build-nummer på V3.10.52.77 og er generelt tilgjengelig via en egen oppdatering i mai 2021.</span><span class="sxs-lookup"><span data-stu-id="d9b36-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="d9b36-111">Update Release 31</span><span class="sxs-lookup"><span data-stu-id="d9b36-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d9b36-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="d9b36-112">Bug fixes</span></span>

<span data-ttu-id="d9b36-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="d9b36-113">**Time and Expense**</span></span>

<span data-ttu-id="d9b36-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="d9b36-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9b36-115">Kommandoknappene for tidsregistreringskontroll på siden **Ressurs som kan reserveres**, var forvirrende.</span><span class="sxs-lookup"><span data-stu-id="d9b36-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="d9b36-116">Det ble generert et nullreferanseunntak i **Project.SetTrackingFields** under godkjenning av en tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="d9b36-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="d9b36-117">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="d9b36-117">**Resource Management**</span></span>

<span data-ttu-id="d9b36-118">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="d9b36-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9b36-119">**Opprett teammedlem** viser ikke metadatainnstillingen for bestillingsoppsett for **Status for registrert standardbestilling** på riktig måte.</span><span class="sxs-lookup"><span data-stu-id="d9b36-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="d9b36-120">Når du oppgraderer fra PSA 1.X til 3.X, mislykkes oppgraderingsprosessen på **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="d9b36-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="d9b36-121">**Salg**</span><span class="sxs-lookup"><span data-stu-id="d9b36-121">**Sales**</span></span>

<span data-ttu-id="d9b36-122">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="d9b36-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="d9b36-123">Faktisk omsetning konverterer beløpene til prosjektvalutaen i sporingsrutenettet.</span><span class="sxs-lookup"><span data-stu-id="d9b36-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="d9b36-124">Valutastandarden er uklar når du oppretter journallinjer, tilbudslinjer og kontraktlinjer i scenarier der standardvalutaen for en organisasjon er forskjellig fra prosjektvalutaen.</span><span class="sxs-lookup"><span data-stu-id="d9b36-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="d9b36-125">Spørringen **Venter på korrigering av journalvalidering** filtreres ikke etter prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d9b36-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="d9b36-126">Resterende salg beregnes feil på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="d9b36-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="d9b36-127">Tilbud basert på en kontakt mislykkes når de opprettes uten en prisliste.</span><span class="sxs-lookup"><span data-stu-id="d9b36-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="d9b36-128">Ingen behandlingsspinner vises når du velger **Bekreft faktura**.</span><span class="sxs-lookup"><span data-stu-id="d9b36-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="d9b36-129">Ingen behandlingsspinner vises når du velger **Opprett faktura**.</span><span class="sxs-lookup"><span data-stu-id="d9b36-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="d9b36-130">Hvis du lukker et tilbud som tapt, annulleres ikke bestillingene.</span><span class="sxs-lookup"><span data-stu-id="d9b36-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







