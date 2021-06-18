---
title: Hva er nytt eller endret i Project Service Automation versjon 3.x lanseringsbølge 1 2020
description: Dette emnet gir informasjon om hva som er nytt og endret i Project Service Automation versjon 3 lanseringsbølge 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996848"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="fd18a-103">Hva er nytt eller endret i Project Service Automation versjon 3 lanseringsbølge 1 2020</span><span class="sxs-lookup"><span data-stu-id="fd18a-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fd18a-104">Emnet uthever viktige oppgraderingshensyn når du flytter til den nyeste versjonen av Project Service Automation (PSA) versjon 3.x lanseringsbølge 1 2020.</span><span class="sxs-lookup"><span data-stu-id="fd18a-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="fd18a-105">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="fd18a-105">Time entry</span></span>
<span data-ttu-id="fd18a-106">Tidsregistreringsopplevelsen er utvidet for å levere funksjoner for å utvide tidsoppføringen til flere kundescenarioer.</span><span class="sxs-lookup"><span data-stu-id="fd18a-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="fd18a-107">Dette inkluderer muligheten til å legge til oppføringstyper, som nå har en bestemt virkemåte basert på feltskjemanavnet **Innstilling for tidsoppføring**, som vises om **Tidskilde**.</span><span class="sxs-lookup"><span data-stu-id="fd18a-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="fd18a-108">En ny løsning, kalt Time, Expense, Statusing og Approvals (TESA), er lagt til for å støtte denne funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="fd18a-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="fd18a-109">Hensyn ved oppgradering</span><span class="sxs-lookup"><span data-stu-id="fd18a-109">Upgrade consideration</span></span>
<span data-ttu-id="fd18a-110">For at denne funksjonaliteten skal kunne støttes, er rollene i PSA oppdatert til å inkludere nye rettigheter.</span><span class="sxs-lookup"><span data-stu-id="fd18a-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="fd18a-111">Disse rettighetene gir lesetilgang til den nye enheten, **Innstilling for tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="fd18a-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="fd18a-112">Brukere som må ha mulighet til å logge tid, må tildeles brukerrollen **Tidsoppføringsbruker** i tillegg til eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="fd18a-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="fd18a-113">Denne rollen omfatter den nye funksjonaliteten og sørger for at tidsoppføringen vil fortsette å fungere.</span><span class="sxs-lookup"><span data-stu-id="fd18a-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="fd18a-114">Hvis du i tillegg har egendefinerte apper som inneholder alle skjemaer for enheten for tidsoppføring, må du fjerne **Hurtigopprettingsskjema for TESA-tidsoppføring** fra modulen.</span><span class="sxs-lookup"><span data-stu-id="fd18a-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="fd18a-115">Aktuelle endringer i utvidet tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="fd18a-115">Currently extended time entry changes</span></span>
<span data-ttu-id="fd18a-116">For å minimere påvirkningen for gjeldende brukere av tidsoppføring er denne rolleendringen det eneste kjernekravet som kreves for å fortsette å bruke tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="fd18a-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="fd18a-117">Hvis du har opprettet egendefinerte visninger eller separate timeregistreringsopplevelser, må du angi feltene **Innstilling for tidsoppføring** til riktig PSA-verdi.</span><span class="sxs-lookup"><span data-stu-id="fd18a-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]