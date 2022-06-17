---
title: Oversikt over leverandøroppbevaring
description: Denne artikkelen inneholder en oversikt over funksjoner for leverandøroppbevaring.
author: sigitac
ms.date: 10/01/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 680786f239125905f3b8746cb8318732aa74d9e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916852"
---
# <a name="vendor-retention-overview"></a>Oversikt over leverandøroppbevaring

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Det kan hende at organisasjonen din vil beholde en del av betalingen til leverandører som arbeider med prosjekter for organisasjonen. Før du betaler leverandøren, vil du kanskje forsikre deg om at varene og tjenestene de leverte, oppfyller forventningene.

Når du forhandler kjøp for prosjekter med leverandører, kan du angi vilkårene for leverandørhonorar som inkluderer prosentandelen eller beløpet som skal beholdes. Etter hvert som leverandøren leverer varer og tjenester, trekker du den angitte prosentsatsen for oppbevaring eller beløp fra betalingen til leverandøren. Når prosjektet er fullført eller når en midlertidig fase som er angitt i leverandørkontrakten, frigir du det tilbakeholdte beløpet og oppretter en betaling til leverandøren.

## <a name="vendor-retention-example"></a>Eksempel på leverandøroppbevaring

Eksemplet nedenfor viser hvordan en prosentandel av et leverandørfakturabeløp beholdes basert på prosentsatsen som er fullført for et prosjekt.

Contoso Robotics USA har inngått en kontrakt med leverandøren Fabrikam om å levere 100 timer opplæring for fornyelse av utstyrsprosjektet. Den totale kontraktverdien er USD 30 000 med en avtalt innkjøpspris på USD 300 per time.

Opplæring skal leveres i tre faser med følgende tidsplan:

- Fase 1: 50 timer eller 50 prosent av prosjektet
- Fase 2: 30 timer eller 80 prosent av prosjektet totalt
- Fase 3: 20 timer eller 100 prosent av prosjektet

Tabellen nedenfor viser oppbevaringsvilkår.

| **Prosentandel leverte enheter** | **Prosentandel som skal beholdes** | **Prosentandel som skal frigis** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100% | 0 % | 100% |

Transaksjonene fører til følgende beløp:

- Fase 1:
  - Beløpet som skal betales er 50 x 300 eller 15 000.
  - 20 prosent av beløpet, eller 3 000, beholdes og frigis på et senere tidspunkt.
  - Beløpet som betales til leverandøren, er 12 000.
- Fase 2:
  - Beløpet som skal betales er 30 x 300 eller 9 000.
  - 10 prosent av beløpet, eller 900, beholdes.
  - 10 prosent av de 3 000 som ble beholdt i fase 1, eller 300, frigis.
  - Beløpet som betales til leverandøren, er 8 400. Dette beløpet er 9 000 mindre enn oppbevaringen på 900 pluss de 300 som ble frigitt fra fase 1-oppbevaringen.
- Fase 3:
  - Beløpet som skal betales er 20 x 300 eller 6 000.
  - Ingen beløp beholdes.
  - Beløpet som frigis, er 3 600. Dette beløpet består av de 3 000 som ble beholdt i fase 1, mindre enn 300 fra fase 1 som ble frigitt i fase 2, pluss 900 som ble beholdt i fase 2.
  - Beløpet som betales til leverandøren, er 9 600. Dette beløpet består av det tilbakeholdte beløpet på 3 600 pluss 6 000 for fullføring av fase 3.

Totalbeløpet som er betalt til leverandøren etter at de tre fasene er fullført, er 30 000, som er totalbeløpet for bestillingen (15 000 + 9 000 + 6 000).
