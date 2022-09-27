---
title: Ressurser for underkontraktlinje
description: Denne artikkelen forklarer hvordan du angir de dedikerte ressursene fra leverandøren for en bestemt underkontraktlinje for tid.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522385"
---
# <a name="subcontract-line-resources"></a>Ressurser for underkontraktlinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan en leverandør angi ressurser som skal brukes til å levere ressurskapasiteten som blir kjøpt på underkontraktlinjen for tid.

## <a name="create-subcontract-line-resources"></a>Opprett ressurser for underkontraktlinje

Fullfør fremgangsmåten nedenfor for å opprette ressurser for underkontraktlinje.

1. Velg **Underkontrakter** i navigasjonsruten, og åpne underkontrakten du vil arbeide med.
2. Åpne underkontraktlinjen for et tidspunkt du vil angi leverandørressurser for.
3. Velg **+ Ny ressurs for underkontraktlinje** i delskjemaet i fanen **Ressurser for underkontrakt**.
4. Angi den nødvendige informasjonen på siden **Ny ressurs for underkontraktslinje**, og velg deretter **Lagre og lukk**.

Tabellen nedenfor forklarer feltene for ressursen for underkontraktlinjen.

| Felt | Beskrivelse | Funksjonsinnvirkning |
| ----- | ----------- | ----------------- |
| Ressurs som kan reserveres | Velg en ressurs som kan reserveres, av typen **Kontraktarbeider** som du vil bruke som ressurs på underkontraktlinjen.| Hvis du ikke har opprettet en ressurs som kan reserveres for kontraktarbeideren, lar du dette feltet stå tomt. En ressurs som kan reserveres, blir opprettet når du lagrer oppføringen.  |
| Kontakt | Du kan opprette en underkontraktlinjeressurs fra en eksisterende kontakt. Bruk oppslaget til å vise listen over aktive kontakter i systemet. Velg en kontakt for leverandøren av denne underkontrakten. Hvis kontaktpersonen du valgte, ikke er en gyldig kontakt for leverandøren på underkontrakten, lagres ikke ressursoppføringen for underkontraktlinjen.| Hvis det ikke finnes ressurs som kan reserveres, for den valgte kontakten, oppretter systemet en ressurs som kan reserveres, for den valgte kontakten før ressursen for underkontraktlinjen opprettes. |
| User | Du kan opprette en linjeressurs for underkontrakt ved å velge en aktiv bruker. Bruk oppslaget til å vise listen over aktive brukere i systemet.| Hvis det ikke finnes ressurs som kan reserveres, for den valgte brukeren, oppretter systemet en ressurs som kan reserveres, for den valgte brukeren før ressursen for underkontraktlinjen opprettes. |
| Startdato | Datoen da oppgaven til underkontraktsarbeideren starter.| Hvis denne ressursen bestilles for en periode som faller før dette datointervallet, vises det en advarsel. |
| Sluttdato | Datoen da oppgaven til underkontraktsarbeideren er fullført.| Hvis denne ressursen bestilles for en periode som faller etter dette datointervallet, vises det en advarsel. |
| Innsats | Det totale antallet innsatstimer den kontrakterte arbeideren bruker på denne underkontraktlinjen.| Hvis denne ressursen reserveres utover innsatsen som er tildelt på denne underkontrakten, vises det en advarsel. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
