---
title: Ressurser for underkontraktlinje
description: Dette emnet forklarer hvordan du angir de dedikerte ressursene som leveres av leverandøren, for en bestemt underkontraktlinje for tid.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323383"
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
4. Angi den nødvendige informasjonen på siden **Ny milepæl for underkontraktlinje**, og velg deretter **Lagre og lukk**.

Tabellen nedenfor forklarer feltene for ressursen for underkontraktlinjen.

| Felt |  Beskrivelse |
| ----- | ------------ |
| Ressurs som kan reserveres | Velg en ressurs som kan reserveres, av typen Kontraktarbeider som du vil bruke som ressurs på underkontraktlinjen. Hvis du ikke har opprettet en ressurs som kan reserveres, for kontraktarbeideren ennå, lar du dette feltet stå tomt. En ressurs som kan reserveres, opprettes når du lagrer oppføringen.  |
| Kontakt | Hvis feltet **Ressurs som kan reserveres** er tomt, kan du opprette ressursen for underkontraktlinjen fra en eksisterende kontakt. Bruk oppslaget til å vise listen over aktive kontakter i systemet. Velg en kontakt for leverandøren av denne underkontrakten. Kontakten du velger, valideres når du lagrer oppføringen. Hvis kontakten du valgte, ikke er en gyldig kontakt, lagres ikke oppføringen. Hvis det ikke finnes ressurs som kan reserveres, for den valgte kontakten, oppretter systemet en ressurs som kan reserveres, for den valgte kontakten før ressursen for underkontraktlinjen opprettes. |
| User | Hvis feltet **Ressurs som kan reserveres** er tomt, kan du opprette en ressurs for underkontraktlinjen ved å velge en aktiv bruker. Bruk oppslaget til å vise listen over aktive brukere i systemet. Hvis det ikke finnes ressurs som kan reserveres, for den valgte brukeren, oppretter systemet en ressurs som kan reserveres, for den valgte brukeren før ressursen for underkontraktlinjen opprettes. |
| Startdato | Datoen da oppgaven til underkontraktsarbeideren starter. Hvis denne ressursen bestilles for en periode som faller før dette datointervallet, vises det en advarsel. |
| Sluttdato | Datoen da oppgaven til underkontraktsarbeideren er fullført. Hvis denne ressursen bestilles for en periode som faller etter dette datointervallet, vises det en advarsel. |
| Innsats | Det totale antallet innsatstimer underkontraktsarbeideren bruker på denne underkontraktlinjen. Hvis denne ressursen reserveres utover innsatsen vedkommende er tildelt på denne underkontrakten, vises det en advarsel. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
