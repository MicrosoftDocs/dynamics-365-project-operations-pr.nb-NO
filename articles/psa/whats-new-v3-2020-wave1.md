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
ms.reviewer: johnmichalak
ms.openlocfilehash: 073b70b4ae02d943eb0794b51e888815ee16f438
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577892"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Hva er nytt eller endret i Project Service Automation versjon 3 lanseringsbølge 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Emnet uthever viktige oppgraderingshensyn når du flytter til den nyeste versjonen av Project Service Automation (PSA) versjon 3.x lanseringsbølge 1 2020.

## <a name="time-entry"></a>Tidsoppføring
Tidsregistreringsopplevelsen er utvidet for å levere funksjoner for å utvide tidsoppføringen til flere kundescenarioer. Dette inkluderer muligheten til å legge til oppføringstyper, som nå har en bestemt virkemåte basert på feltskjemanavnet **Innstilling for tidsoppføring**, som vises om **Tidskilde**. En ny løsning, kalt Time, Expense, Statusing og Approvals (TESA), er lagt til for å støtte denne funksjonaliteten.

### <a name="upgrade-consideration"></a>Hensyn ved oppgradering
For at denne funksjonaliteten skal kunne støttes, er rollene i PSA oppdatert til å inkludere nye rettigheter. Disse rettighetene gir lesetilgang til den nye enheten, **Innstilling for tidsoppføring**.

Brukere som må ha mulighet til å logge tid, må tildeles brukerrollen **Tidsoppføringsbruker** i tillegg til eksisterende roller. Denne rollen omfatter den nye funksjonaliteten og sørger for at tidsoppføringen vil fortsette å fungere.

Hvis du i tillegg har egendefinerte apper som inneholder alle skjemaer for enheten for tidsoppføring, må du fjerne **Hurtigopprettingsskjema for TESA-tidsoppføring** fra modulen.

### <a name="currently-extended-time-entry-changes"></a>Aktuelle endringer i utvidet tidsregistrering
For å minimere påvirkningen for gjeldende brukere av tidsoppføring er denne rolleendringen det eneste kjernekravet som kreves for å fortsette å bruke tidsoppføring. Hvis du har opprettet egendefinerte visninger eller separate timeregistreringsopplevelser, må du angi feltene **Innstilling for tidsoppføring** til riktig PSA-verdi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
