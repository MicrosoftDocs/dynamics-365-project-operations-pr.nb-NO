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
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Hva er nytt eller endret i Project Service Automation versjon 3 lanseringsbølge 1 2020
Emnet uthever viktige oppgraderingshensyn når du flytter til den nyeste versjonen av Project Service Automation (PSA) versjon 3.x lanseringsbølge 1 2020.

## <a name="time-entry"></a>Tidsoppføring
Tidsregistreringsopplevelsen er utvidet for å levere funksjoner for å utvide tidsoppføringen til flere kundescenarioer. Dette inkluderer muligheten til å legge til oppføringstyper, som nå har en bestemt virkemåte basert på feltskjemanavnet **Innstilling for tidsoppføring**, som vises om **Tidskilde**.

### <a name="upgrade-consideration"></a>Hensyn ved oppgradering
For at denne funksjonaliteten skal kunne støttes, er rollene i PSA oppdatert til å inkludere nye rettigheter. Disse rettighetene gir lesetilgang til den nye enheten, **Innstilling for tidsoppføring**.

Brukere som må ha mulighet til å logge tid, må tildeles brukerrollen **Tidsoppføringsbruker** i tillegg til eksisterende roller. Denne rollen omfatter den nye funksjonaliteten og sørger for at tidsoppføringen vil fortsette å fungere.

### <a name="currently-extended-time-entry-changes"></a>Aktuelle endringer i utvidet tidsregistrering
For å minimere påvirkningen for gjeldende brukere av tidsoppføring er denne rolleendringen det eneste kjernekravet som kreves for å fortsette å bruke tidsoppføring. Hvis du har opprettet egendefinerte visninger eller separate timeregistreringsopplevelser, må du angi feltene **Innstilling for tidsoppføring** til riktig PSA-verdi.
