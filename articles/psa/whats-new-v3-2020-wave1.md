---
title: Hva er nytt eller endret i Project Service Automation versjon 3.x lanseringsbølge 1 2020
description: Denne artikkelen inneholder informasjon om hva som er nytt og endret i bølge 1 i 2020 for Project Service Automation versjon 3.
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
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928628"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Hva er nytt eller endret i Project Service Automation versjon 3 lanseringsbølge 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Artikkelen fremhever viktige oppgraderingshensyn ved overgang til den nyeste versjonen av bølge 1 i 2020 for Project Service Automation (PSA) versjon 3.x.

## <a name="time-entry"></a>Tidsoppføring
Tidsregistreringsopplevelsen er utvidet for å levere funksjoner for å utvide tidsoppføringen til flere kundescenarioer. Dette inkluderer muligheten til å legge til oppføringstyper, som nå har en bestemt virkemåte basert på feltskjemanavnet **Innstilling for tidsoppføring**, som vises om **Tidskilde**. En ny løsning, kalt Time, Expense, Statusing og Approvals (TESA), er lagt til for å støtte denne funksjonaliteten.

### <a name="upgrade-consideration"></a>Hensyn ved oppgradering
For at denne funksjonaliteten skal kunne støttes, er rollene i PSA oppdatert til å inkludere nye rettigheter. Disse rettighetene gir lesetilgang til den nye enheten, **Innstilling for tidsoppføring**.

Brukere som må ha mulighet til å logge tid, må tildeles brukerrollen **Tidsoppføringsbruker** i tillegg til eksisterende roller. Denne rollen omfatter den nye funksjonaliteten og sørger for at tidsoppføringen vil fortsette å fungere.

Hvis du i tillegg har egendefinerte apper som inneholder alle skjemaer for enheten for tidsoppføring, må du fjerne **Hurtigopprettingsskjema for TESA-tidsoppføring** fra modulen.

### <a name="currently-extended-time-entry-changes"></a>Aktuelle endringer i utvidet tidsregistrering
For å minimere påvirkningen for gjeldende brukere av tidsoppføring er denne rolleendringen det eneste kjernekravet som kreves for å fortsette å bruke tidsoppføring. Hvis du har opprettet egendefinerte visninger eller separate timeregistreringsopplevelser, må du angi feltene **Innstilling for tidsoppføring** til riktig PSA-verdi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
