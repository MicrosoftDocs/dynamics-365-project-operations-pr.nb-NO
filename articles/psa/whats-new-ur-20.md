---
title: Hva er nytt eller endret i Project Service Automation Update Release 20, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006523"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="c6ec1-103">Project Service Automation, Update Release 20, V3</span><span class="sxs-lookup"><span data-stu-id="c6ec1-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="c6ec1-104">Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="c6ec1-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="c6ec1-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="c6ec1-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="c6ec1-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="c6ec1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="c6ec1-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 20.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="c6ec1-110">Denne versjonen har et build-nummer på V 3.10.31.37 og er generelt tilgjengelig via en egen oppdatering i juni 2020.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="c6ec1-111">Update Release 20</span><span class="sxs-lookup"><span data-stu-id="c6ec1-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="c6ec1-112">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="c6ec1-112">Bug fixes</span></span>

<span data-ttu-id="c6ec1-113">**Prosjektledelse**</span><span class="sxs-lookup"><span data-stu-id="c6ec1-113">**Project Management**</span></span>

<span data-ttu-id="c6ec1-114">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c6ec1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="c6ec1-115">Import av prosjektteammedlemmer med en tildelingsmetode som krever timer, fører til en uklar feilmelding når de angitte timene er null.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="c6ec1-116">Brukere får en feilaktig feilmelding når maksimalt antall tegn er angitt i **Beskrivelse**-feltet for en prosjektoppgave.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="c6ec1-117">Siden for **nedlasting av Microsoft Dynamics 365 Project Service Automation-tillegg** omdirigerer til den engelske nedlastingssiden når brukerens språkinnstillinger er satt til japansk.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="c6ec1-118">Når det oppstår en serverfeil, blir synkroniseringsetiketten i **Planlegg**-fanen i **Prosjekter**-skjema noen ganger forblir.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="c6ec1-119">Overflødige oppgaveoppdateringer blir sendt til serveren når en oppgave blir endret.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="c6ec1-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="c6ec1-120">**Sales**</span></span>

<span data-ttu-id="c6ec1-121">Følgende problemer har blitt løst:</span><span class="sxs-lookup"><span data-stu-id="c6ec1-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="c6ec1-122">På **Kontrakt**-skjemaet oppretter dobbeltklikking **Opprett faktura** to fakturaer for én enkelt oppføring av faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="c6ec1-123">I Internet Explorer 11 kan ikke brukere opprette utgiftsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="c6ec1-124">Tilbakeføring av kostnader og tilbakeføring av ufakturerte faktiske verdier blir ikke koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="c6ec1-125">**Oppdater faktiske verdier**-knappen på **Prosjekt**-skjemaet oppdaterer ikke **Faktiske timer for oppgaven**.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="c6ec1-126">**PreValidateProjectTeamMemberCreate**-plugin-modulen kan opprette dupliserte generiske ressurser som kan reserveres, når attributtet **msdyn_isgenericresourceprojectscoped** er satt til **Usann**.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="c6ec1-127">**Rekalkulerer** fjerne belastbare kostnader for produktbasert tilbudslinjedetaljer og kontraktlinjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="c6ec1-128">I bestemte scenarier viser **PostEstimateLineUpdate**-plugin-modulen en unntaksfeil med null referanse.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="c6ec1-129">Tidsfasevarighet i **Diagram for lønnsomhetsanalyse** samsvarer ikke med varigheten for kostnadene i detaljen for tilbudslinjen for fastpris i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="c6ec1-130">Enhet og enhetsgruppeverdier bruker ikke riktige standardinnstillinger for utgiftskategorier i skjemaene **Kontraktlinjedetaljer** og **Tilbudslinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="c6ec1-131">**Kostpris for organisasjonsenhet**-lister tillater overlapping i ikrafttredelsesdato.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="c6ec1-132">Brukere har ikke tillatelse til å endre **Organisasjonsenhet** når ordretypen ikke er arbeidsbasert fordi den vil føre til en unntaksfeil med nullreferanse.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="c6ec1-133">Når du prøver å navigere fra skjemaet **Tilbudslinjedetaljer** tilbake til **Tilbud**-fanen, oppdateres skjemaet og viser **Sammendrag**-fanen.</span><span class="sxs-lookup"><span data-stu-id="c6ec1-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]