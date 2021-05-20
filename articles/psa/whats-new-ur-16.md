---
title: Hva er nytt eller endret i Project Service Automation Update Release 16, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 16, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 33a711816e8cca34c4595aa0929de9a808a48b0f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949406"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="9100d-103">Project Service Automation, Update Release 16, V3</span><span class="sxs-lookup"><span data-stu-id="9100d-103">Project Service Automation Update Release 16, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9100d-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9100d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9100d-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="9100d-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="9100d-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9100d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9100d-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="9100d-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="9100d-108">For mer informasjon, se [Installere eller oppdatere en foretrukket løsning](/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="9100d-108">For more information, see [Install, Update a Preferred Solution](/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="9100d-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 16.</span><span class="sxs-lookup"><span data-stu-id="9100d-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="9100d-110">Denne versjonen har buildnummer V3.10.6.34 og er vanligvis tilgjengelig via en egen oppdatering i januar 2020.</span><span class="sxs-lookup"><span data-stu-id="9100d-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="9100d-111">Update Release 16</span><span class="sxs-lookup"><span data-stu-id="9100d-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9100d-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="9100d-112">Bug fixes</span></span>

-   <span data-ttu-id="9100d-113">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="9100d-113">Time and Expense</span></span>

    -   <span data-ttu-id="9100d-114">Løst: Brukere som forsøker å sende slettede tids- og utgiftsoppføringer til godkjenning, mottar nå relevante feilmeldinger.</span><span class="sxs-lookup"><span data-stu-id="9100d-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="9100d-115">Prosjektledelse</span><span class="sxs-lookup"><span data-stu-id="9100d-115">Project Management</span></span>

    -   <span data-ttu-id="9100d-116">Løst: Ressursenhetene som er definert for teammedlemmer i maler, overholdes når malene brukes på et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9100d-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="9100d-117">Løst: Forbedret håndtering av den nye tildelingen av oppføringseierskap.</span><span class="sxs-lookup"><span data-stu-id="9100d-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="9100d-118">Løst: Prosjekter som er i ferd med å bli kopiert, har ikke tillatelse til å kopieres før alle kopieringsoperasjonene er fullført.</span><span class="sxs-lookup"><span data-stu-id="9100d-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="9100d-119">Ressursbehandling</span><span class="sxs-lookup"><span data-stu-id="9100d-119">Resource Management</span></span>

    -   <span data-ttu-id="9100d-120">Løst: Utvid bestillinger håndterer nå korte varigheter på riktig måte, og det opprettes ikke lenger nulltimer for utvidede bestillinger.</span><span class="sxs-lookup"><span data-stu-id="9100d-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="9100d-121">Løst: Avstemmingsvisningen gjengir nå når prosjektets tidssone er +5:30 GMT, og brukerens tidssone er forskjellig.</span><span class="sxs-lookup"><span data-stu-id="9100d-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="9100d-122">Sales</span><span class="sxs-lookup"><span data-stu-id="9100d-122">Sales</span></span>

    -   <span data-ttu-id="9100d-123">Løst: Når et prosjekt som er tilordnet til en kontraktlinje, blir fjernet og et nytt prosjekt blir tilordnet, ble ikke de faktiske oppføringene i det nye prosjektet evaluert på nytt basert på fakturerings- og prisreglene som var definert i kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="9100d-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="9100d-124">Dette er løst i denne versjonen.</span><span class="sxs-lookup"><span data-stu-id="9100d-124">This has been fixed in this release.</span></span> <span data-ttu-id="9100d-125">Priser og faktiske oppføringer i det nylig tilordnede prosjektet blir tilbakeført og opprettet på nytt på riktig måte basert på priser og faktureringsregler for kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="9100d-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="9100d-126">De faktiske oppføringene i det ikke-tilordnede prosjektet blir også evaluert på nytt og opprettet på nytt som en følge av dette.</span><span class="sxs-lookup"><span data-stu-id="9100d-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="9100d-127">Løst: Ytterligere validering er lagt til i **Beløp**-feltet for en estimatlinje for å sikre at nullverdier ikke beholdes.</span><span class="sxs-lookup"><span data-stu-id="9100d-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="9100d-128">Løst: Når faktiske verdier er oppdatert i et prosjekt, er det lagt til en Oppdater-knapp i hovedskjemaet for prosjektet, slik at brukere kan synkronisere de faktiske verdiene på nytt.</span><span class="sxs-lookup"><span data-stu-id="9100d-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="9100d-129">Løst: Når brukere oppgraderer fra 2.X til 3.X, blir prosjekter med NULL-verdi for prosjektnavn tillatt.</span><span class="sxs-lookup"><span data-stu-id="9100d-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]