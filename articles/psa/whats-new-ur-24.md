---
title: Hva er nytt eller endret i Project Service Automation Update Release 24, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146720"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="8d960-103">Project Service Automation, Update Release 24, V3</span><span class="sxs-lookup"><span data-stu-id="8d960-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8d960-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8d960-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8d960-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="8d960-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8d960-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8d960-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8d960-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="8d960-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8d960-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8d960-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8d960-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 24.</span><span class="sxs-lookup"><span data-stu-id="8d960-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="8d960-110">Denne versjonen har buildnummer V3.10.42.43 og er generelt tilgjengelig via en egen oppdatering i oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="8d960-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="8d960-111">Update Release 24</span><span class="sxs-lookup"><span data-stu-id="8d960-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8d960-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="8d960-112">Bug fixes</span></span>

<span data-ttu-id="8d960-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8d960-113">**Sales**</span></span>

<span data-ttu-id="8d960-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="8d960-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d960-115">Problem under angivelse av standard prisliste for produkter.</span><span class="sxs-lookup"><span data-stu-id="8d960-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="8d960-116">Ytelsen til vunnet tilbud er treg på grunn av den innebygde kopien av prisliste- og rolleprisoppføringene.</span><span class="sxs-lookup"><span data-stu-id="8d960-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="8d960-117">**Prosjektkontrakt/Salgshub** > **Produktlinjevare/Ordrelinjeantall** rundes automatisk av til nærmeste heltall.</span><span class="sxs-lookup"><span data-stu-id="8d960-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="8d960-118">Utvid til systemrettigheter ved lesing av prislister.</span><span class="sxs-lookup"><span data-stu-id="8d960-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="8d960-119">Kopier kundeadressefeltene **address1_freighttermscode** og **address1_shippingmethodcode** til tilbud/ordre.</span><span class="sxs-lookup"><span data-stu-id="8d960-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="8d960-120">**Tid og utgift**</span><span class="sxs-lookup"><span data-stu-id="8d960-120">**Time and Expense**</span></span>

<span data-ttu-id="8d960-121">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="8d960-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d960-122">**Rutenett for tidsoppføring** støtter ikke tidsvirkemåten for **Bare dato**.</span><span class="sxs-lookup"><span data-stu-id="8d960-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="8d960-123">**Tidsoppføring** oppdateres ikke automatisk.</span><span class="sxs-lookup"><span data-stu-id="8d960-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="8d960-124">Det kreves en manuell oppdatering.</span><span class="sxs-lookup"><span data-stu-id="8d960-124">A manual refresh is required.</span></span>
- <span data-ttu-id="8d960-125">Kan ikke importere tidsoppføringer fra en tilordning når det er en pause (0 timer) i tilordningene for en ressurs.</span><span class="sxs-lookup"><span data-stu-id="8d960-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="8d960-126">Når du oppretter en tidsoppføring, angir du starten til den samme som **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="8d960-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="8d960-127">Aktiver masseredigering for tidsregistrering på nytt.</span><span class="sxs-lookup"><span data-stu-id="8d960-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="8d960-128">**Ressursbehandling**</span><span class="sxs-lookup"><span data-stu-id="8d960-128">**Resource Management**</span></span>

<span data-ttu-id="8d960-129">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="8d960-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d960-130">Hvis du prøver å oppdatere statusen for en bestilling mellom flere dager uten et krav, blir det iverksatt et nullreferanseunntak.</span><span class="sxs-lookup"><span data-stu-id="8d960-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="8d960-131">Feil under innlasting av **avstemmingsvisningen**.</span><span class="sxs-lookup"><span data-stu-id="8d960-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="8d960-132">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="8d960-132">**Project Management**</span></span>

<span data-ttu-id="8d960-133">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="8d960-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="8d960-134">I **Prosjekttidsplan**, når du bytter fra **Manuell** til **Automatisk**, fullføres ikke automatisk lagring.</span><span class="sxs-lookup"><span data-stu-id="8d960-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="8d960-135">Utgiftskostnader bør ikke beregnes mot varians i **rutenettet for prosjektsporing**.</span><span class="sxs-lookup"><span data-stu-id="8d960-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="8d960-136">Inkonsekvent virkemåte for **Estimatmerke**-kolonner under innlasting, i forhold til endring av **Tidsfase**-typen.</span><span class="sxs-lookup"><span data-stu-id="8d960-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="8d960-137">De faktiske kostnadene i et prosjekt gjenspeiler kanskje ikke totalverdiene fra **Faktiske verdier**.</span><span class="sxs-lookup"><span data-stu-id="8d960-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="8d960-138">**Beregnet sluttdato** i kategorien **Sammendrag** samsvarer ikke med **WBS-plan**.</span><span class="sxs-lookup"><span data-stu-id="8d960-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="8d960-139">**Oppdater faktiske timer** ved redusering av innrykk fungerer ikke riktig.</span><span class="sxs-lookup"><span data-stu-id="8d960-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="8d960-140">En prosjektleder utenfor rot-**BU** kan ikke opprette et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="8d960-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="8d960-141">Endringer i oppgaven eller kategorien i **Utgiftsestimater** beholdes ikke.</span><span class="sxs-lookup"><span data-stu-id="8d960-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="8d960-142">**Kopi av kontrakt** kopierer faktureringsplanene og kjørestatusen.</span><span class="sxs-lookup"><span data-stu-id="8d960-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="8d960-143">Knappen **Oppdater faktiske verdier** beregner aktivitetssammendrag på feil måte.</span><span class="sxs-lookup"><span data-stu-id="8d960-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="8d960-144">Microsoft Project-tillegg: Reparer nullreferansefeil hvis et teammedlem har en tom ressursenhet.</span><span class="sxs-lookup"><span data-stu-id="8d960-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

