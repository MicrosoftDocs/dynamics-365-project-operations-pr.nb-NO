---
title: Hva er nytt eller endret i Project Service Automation Update Release 15, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 15, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 86aadca637939120d0ccd839e7c425e9e8d38aec
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006838"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="4fe2b-103">Project Service Automation, Update Release 15, V3</span><span class="sxs-lookup"><span data-stu-id="4fe2b-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4fe2b-104">Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="4fe2b-105">Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4fe2b-106">Denne versjonen er kompatibel med Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4fe2b-107">Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="4fe2b-108">For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4fe2b-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4fe2b-109">Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for PSA V3, Update Release 15.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="4fe2b-110">Denne versjonen har buildnummer V3.10.5.28 og er vanligvis tilgjengelig via en egen oppdatering i januar 2020.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="4fe2b-111">Update Release 15</span><span class="sxs-lookup"><span data-stu-id="4fe2b-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="4fe2b-112">Forbedringer</span><span class="sxs-lookup"><span data-stu-id="4fe2b-112">Enhancements</span></span>

- <span data-ttu-id="4fe2b-113">Prosjektledelse</span><span class="sxs-lookup"><span data-stu-id="4fe2b-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4fe2b-114">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="4fe2b-114">Bug fixes</span></span>

- <span data-ttu-id="4fe2b-115">Tid og utgift</span><span class="sxs-lookup"><span data-stu-id="4fe2b-115">Time and Expense</span></span>

  - <span data-ttu-id="4fe2b-116">Fikset: Legg til feilbehandling ved innlasting i avstemmingsvisningen.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="4fe2b-117">Fikset: Prosjektressurshub: Endre navn på **Beløp** for å redusere tvetydighet.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="4fe2b-118">Fikset: Juster visningen **Kopier tidsoppføringskolonner** for å inkluderer typen.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="4fe2b-119">Fikset: Redigering av tidsoppføringsvarighet i rutenettvisningen ved hjelp av desimaltall resulterer i en ukjent feil for noen tall.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="4fe2b-120">Prosjektledelse</span><span class="sxs-lookup"><span data-stu-id="4fe2b-120">Project Management</span></span>

  - <span data-ttu-id="4fe2b-121">Fikset: Rullegardinmenyen for **Bruk i sporingsvisning** utvides nå basert på bredden på alternativene.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="4fe2b-122">Fikset: Ved administrasjon av prosjekter i +13-tidssonen kan oppgaveberegninger vise unøyaktige resultater.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="4fe2b-123">Fikset: **Sluttid for teammedlemmer** er rettet opp ved bruk av 24-timers kalender.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="4fe2b-124">Fikset: Reaktiverte **BPF** i **msdyn_project**-hovedskjemaet.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="4fe2b-125">Fikset: Tildelingsberegning ignorerer ikke lenger én dag.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="4fe2b-126">Fikset: Et nytt varslingsbanner er lagt til i prosjektskjemaet når tidssonen er forskjellig mellom brukeren og prosjektet.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="4fe2b-127">Sales</span><span class="sxs-lookup"><span data-stu-id="4fe2b-127">Sales</span></span>

  - <span data-ttu-id="4fe2b-128">Fikset: Oppslagsvisning for utgiftsestimat kan brukes til å filtrere duplikater.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="4fe2b-129">Fikset: Kode i **PluginDomain.ExecuteInTryCatchBlock(..)** skjuler ikke lenger opprinnelsen til unntaket.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="4fe2b-130">Fikset: Feilmelding vises ikke lenger i **Prosjektoppslag** i skjemaet **Tilbudslinje** når det er mer enn 1000 prosjekter.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="4fe2b-131">Fikset: **Estimater**-rutenett for arbeidsberegninger og utgiftsoverslag viser nå riktig valutasymbol.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="4fe2b-132">Fikset: Når en organisasjon oppdaterer PSA fra Update Release 14 til Update Release 15, vises ikke lenger kategorien **Planlegg** som tom i skjemaet **Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="4fe2b-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]