---
title: Hva er nytt eller endret i Project Service Automation Update Release 19, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: b9baeca9e79e233c25a6310e426d755b9162bbad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280725"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="1df3f-103">Project Service Automation, Update Release 19, V3</span><span class="sxs-lookup"><span data-stu-id="1df3f-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="1df3f-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1df3f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1df3f-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="1df3f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1df3f-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="1df3f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1df3f-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="1df3f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1df3f-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1df3f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1df3f-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 19.</span><span class="sxs-lookup"><span data-stu-id="1df3f-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="1df3f-110">Denne versjonen har et build-nummer på V3.10.30.41 og er generelt tilgjengelig via en egen oppdatering i mai 2020.</span><span class="sxs-lookup"><span data-stu-id="1df3f-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="1df3f-111">Update Release 19</span><span class="sxs-lookup"><span data-stu-id="1df3f-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1df3f-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="1df3f-112">Bug fixes</span></span>

<span data-ttu-id="1df3f-113">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="1df3f-113">**Time and Expense**</span></span>

<span data-ttu-id="1df3f-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="1df3f-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="1df3f-115">Feil avledet av import av tidsoppføringer som ikke vises riktig.</span><span class="sxs-lookup"><span data-stu-id="1df3f-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="1df3f-116">Timeregistreringsrutenettet støtter ikke **Bare dato**-feltvirkemåte.</span><span class="sxs-lookup"><span data-stu-id="1df3f-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="1df3f-117">Prosjektressurser kan ikke opprette en utgift med et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="1df3f-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="1df3f-118">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="1df3f-118">**Project Management**</span></span>

<span data-ttu-id="1df3f-119">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="1df3f-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="1df3f-120">Oppgaver to nivåer lengre ned forårsaker feil beregning av arbeidstid ved fullføring (EAC).</span><span class="sxs-lookup"><span data-stu-id="1df3f-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="1df3f-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1df3f-121">**Sales**</span></span>

<span data-ttu-id="1df3f-122">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="1df3f-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="1df3f-123">Handlingen **Beregn på nytt** virker ikke med detaljer for utgiftkontraktlinje eller tilbudslinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="1df3f-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="1df3f-124">**Oppdater priser** mangler for utgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="1df3f-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="1df3f-125">Kunder kan ikke velge egendefinerte kontraktstatusårsaker fra **Prosjektkontrakt**-siden.</span><span class="sxs-lookup"><span data-stu-id="1df3f-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="1df3f-126">Kunder opplever redusert ytelse ved oppretting av en egendefinert prisliste fra et tilbud.</span><span class="sxs-lookup"><span data-stu-id="1df3f-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="1df3f-127">Kunder opplever inkonsekvens med **enhet**-standarder på **Tilbudslinjedetaljer**- og **Kontraktlinjedetaljer**-sidene.</span><span class="sxs-lookup"><span data-stu-id="1df3f-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="1df3f-128">Hvis du legger til kategorivarer i ikke-belastbare transaksjoner på en belastbar kontraktlinje, respekterer den ikke **Ikke-belastbar**-faktureringstype for transaksjonskategorien.</span><span class="sxs-lookup"><span data-stu-id="1df3f-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="1df3f-129">Kunder kan ikke bruke de nylig tillagte rollene og kategoriene i tidligere opprettede kontrakter.</span><span class="sxs-lookup"><span data-stu-id="1df3f-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="1df3f-130">Kunder opplever redusert ytelse, henter unødvendig inn PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="1df3f-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="1df3f-131">Roller som ikke er belastbare i **Ressurskategorier**-listen, må legges til i **Belastbare roller**-fanen som **Ikke-belastbare** på kontraktlinjen for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="1df3f-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="1df3f-132">Kunder kan oppleve redusert ytelse ved oppretting av et prosjekt fordi **GetBookableResourceIdFromUser** henter alle kolonner med ressurser som kan reserveres, i stedet for bare primær-ID-en.</span><span class="sxs-lookup"><span data-stu-id="1df3f-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="1df3f-133">**TransactionType**-enheten mangler plugin-modulen for oppdatering av forhåndsvalidering for å hindre brukere i å skrive inn **Enheter** og **UnitGroups** som ikke er gyldige for transaksjonstyper.</span><span class="sxs-lookup"><span data-stu-id="1df3f-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="1df3f-134">**Fjern**-trinnet fungerer ikke for import av tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="1df3f-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]