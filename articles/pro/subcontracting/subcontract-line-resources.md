---
title: Ressurser for underkontraktlinje
description: Denne artikkelen forklarer hvordan du angir de dedikerte ressursene fra leverandøren for en bestemt underkontraktlinje for tid.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 84fbbd6e1a82db2b2d998b5f41579396df884ec3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924166"
---
# <a name="subcontract-line-resources"></a>Ressurser for underkontraktlinje

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

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
