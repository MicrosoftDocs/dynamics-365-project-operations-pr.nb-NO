---
title: Hva er nytt eller endret i Project Service Automation versjon 3.x lanseringsbølge 1 2020
description: Dette emnet gir informasjon om hva som er nytt og endret i Project Service Automation versjon 3 lanseringsbølge 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754111"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="9a40f-103">Hva er nytt eller endret i Project Service Automation versjon 3 lanseringsbølge 1 2020</span><span class="sxs-lookup"><span data-stu-id="9a40f-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="9a40f-104">Emnet uthever viktige oppgraderingshensyn når du flytter til den nyeste versjonen av Project Service Automation (PSA) versjon 3.x lanseringsbølge 1 2020.</span><span class="sxs-lookup"><span data-stu-id="9a40f-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="9a40f-105">Tidsoppføring</span><span class="sxs-lookup"><span data-stu-id="9a40f-105">Time entry</span></span>
<span data-ttu-id="9a40f-106">Tidsregistreringsopplevelsen er utvidet for å levere funksjoner for å utvide tidsoppføringen til flere kundescenarioer.</span><span class="sxs-lookup"><span data-stu-id="9a40f-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="9a40f-107">Dette inkluderer muligheten til å legge til oppføringstyper, som nå har en bestemt virkemåte basert på feltskjemanavnet **Innstilling for tidsoppføring**, som vises om **Tidskilde**.</span><span class="sxs-lookup"><span data-stu-id="9a40f-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="9a40f-108">Hensyn ved oppgradering</span><span class="sxs-lookup"><span data-stu-id="9a40f-108">Upgrade consideration</span></span>
<span data-ttu-id="9a40f-109">For at denne funksjonaliteten skal kunne støttes, er rollene i PSA oppdatert til å inkludere nye rettigheter.</span><span class="sxs-lookup"><span data-stu-id="9a40f-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="9a40f-110">Disse rettighetene gir lesetilgang til den nye enheten, **Innstilling for tidsoppføring**.</span><span class="sxs-lookup"><span data-stu-id="9a40f-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="9a40f-111">Brukere som må ha mulighet til å logge tid, må tildeles brukerrollen **Tidsoppføringsbruker** i tillegg til eksisterende roller.</span><span class="sxs-lookup"><span data-stu-id="9a40f-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="9a40f-112">Denne rollen omfatter den nye funksjonaliteten og sørger for at tidsoppføringen vil fortsette å fungere.</span><span class="sxs-lookup"><span data-stu-id="9a40f-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="9a40f-113">Aktuelle endringer i utvidet tidsregistrering</span><span class="sxs-lookup"><span data-stu-id="9a40f-113">Currently extended time entry changes</span></span>
<span data-ttu-id="9a40f-114">For å minimere påvirkningen for gjeldende brukere av tidsoppføring er denne rolleendringen det eneste kjernekravet som kreves for å fortsette å bruke tidsoppføring.</span><span class="sxs-lookup"><span data-stu-id="9a40f-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="9a40f-115">Hvis du har opprettet egendefinerte visninger eller separate timeregistreringsopplevelser, må du angi feltene **Innstilling for tidsoppføring** til riktig PSA-verdi.</span><span class="sxs-lookup"><span data-stu-id="9a40f-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
