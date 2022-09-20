---
title: Fastslå salgspriser for prosjektestimater og faktiske verdier
description: Denne artikkelen inneholder informasjon om hvordan salgspriser for estimater og faktiske verdier i et prosjekt fastsettes.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475197"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Fastslå salgspriser for prosjektestimater og faktiske verdier

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

For å fastsette salgspriser på estimater og faktiske verdier i Microsoft Dynamics 365 Project Operations bruker systemet først datoen og valutaen i konteksten for innkommende estimat eller faktisk verdi til å fastsette salgsprislisten. Systemet bruker feltet **Transaksjonsdato** i den spesifikke konteksten for faktisk verdi til å fastsette hvilken prisliste som gjelder. Verdien for **Transaksjonsdato** for det innkommende estimatet eller den faktiske verdien sammenlignes med verdiene for **Effektiv startdato** (tidssoneuavhengig) og **Effektiv sluttdato** (tidssoneuavhengig) i prislisten. Når salgsprislisten er fastsatt, fastsetter systemet salgs- eller fakturasatsen.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Fastsette salgssatser på faktiske og estimerte linjer for tid

Kontekst for estimat for **Tid** henviser til følgende:

- Tilbudslinjedetaljer for **Tid**.
- Kontraktlinjedetaljer for **Tid**.
- Ressurstilordninger i et prosjekt.

Kontekst for faktisk verdi for **Tid** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Tid**.
- Journallinjer som opprettes når en tidsoppføring sendes inn.
- Fakturalinjedetaljer for **Tid**. 

Når en prisliste for salg er fastsatt, fullfører systemet følgende trinn for å angi standard fakturasats.

1. Systemet samsvarer kombinasjonen av feltene **Rolle** og **Ressursenhet** i konteksten for estimat eller faktisk verdi for **Tid** med rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker de bruksklare prisdimensjonene for fakturasatser. Hvis du har konfigurert prising slik at den er basert på andre felter enn eller i tillegg til **Rolle** og **Ressursenhet**, er det denne kombinasjonen av felter som brukes til å hente en samsvarende rolleprislinje.
1. Hvis systemet finner en rolleprislinje som har en fakturasats for kombinasjonen av feltene **Rolle** og **Ressursenhet**, brukes denne fakturasatsen som standard fakturasats.
1. Hvis systemet ikke kan samsvare verdiene til **Rolle** og **Ressursenhet**, henter det rolleprislinjer som har samsvarende verdier for **Rolle**-feltet, men nullverdier for feltet **Ressursenhet**. Når systemet har funnet en samsvarende rolleprisoppføring, brukes fakturasatsen fra denne oppføringen som standard fakturasats. Dette samsvaret forutsetter en bruksklar konfigurasjon for den relative prioriteten for **Rolle** i forhold til **Ressursenhet** som en salgsprisdimensjon.

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av feltene **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres den foregående virkemåten tilsvarende. Systemet henter rolleprisoppføringer som har verdier som samsvarer med hver prisdimensjonsverdi, i prioritert rekkefølge. Rader som har nullverdier for disse dimensjonene, kommer sist.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsette salgssatser på faktiske og estimerte linjer for utgift

Kontekst for estimat for **Utgift** henviser til følgende:

- Tilbudslinjedetaljer for **Utgift**.
- Kontraktlinjedetaljer for **Utgift**.
- Utgiftsestimatlinjer i et prosjekt.

Kontekst for faktisk verdi for **Utgift** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Utgift**.
- Journallinjer som opprettes når en utgiftsoppføring sendes inn.
- Fakturalinjedetaljer for **Utgift**. 

Når en prisliste for salg er fastsatt, fullfører systemet følgende trinn for angi standard enhetssalgspris.

1. Systemet samsvarer kombinasjonen av feltene **Kategori** og **Enhet** på estimatlinjen for **Utgift** med kategoriprislinjene i prislisten.
1. Hvis systemet finner en kategoriprislinje som har en salgssats for kombinasjonen av **Kategori** og **Enhet**, brukes denne salgssatsen som standard salgssats.
1. Hvis systemet finner en samsvarende kategoriprislinje, kan prismodellen brukes til å angi standard salgspris. Tabellen nedenfor viser standard virkemåte for utgiftspriser i Project Operations.

    | Kontekst | Prismodell | Standardpris |
    | --- | --- | --- |
    | Estimat | Pris per enhet | Basert på kategoriprislinjen. |
    |        | Kostpris | 0.00 |
    |        | Påslag over kostnad | 0.00 |
    | Faktisk | Pris per enhet | Basert på kategoriprislinjen. |
    |        | Kostpris | Basert på de relaterte faktiske kostnadene. |
    |        | Påslag over kostnad | En markering brukes, som definert av kategoriprislinjen, på enhetskostnadssatsen for den relaterte faktiske kostnaden. |

1. Hvis systemet ikke kan samsvare verdiene i feltene **Kategori** og **Enhet**, settes salgssatsen til **0** (null) som standard.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Fastsette salgssatser på linjer med faktiske verdier og estimater for materialer

Kontekst for estimat for **Materiale** henviser til følgende:

- Tilbudslinjedetaljer for **Materiale**.
- Kontraktlinjedetaljer for **Materiale**.
- Materialestimatlinjer i et prosjekt.

Kontekst for faktisk verdi for **Materiale** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Materiale**.
- Journallinjer som opprettes når en logg over materialbruk sendes inn.
- Fakturalinjedetaljer for **Materiale**. 

Når en prisliste for salg er fastsatt, fullfører systemet følgende trinn for angi standard enhetssalgspris.

1. Systemet samsvarer kombinasjonen av feltene **Produkt** og **Enhet** på estimatlinjen for **Materiale** med prislisteelementlinjene i prislisten.
1. Hvis systemet finner en prislisteelementlinje som har en salgssats for kombinasjonen av **Produkt** og **Enhet**, og prismetoden er **Valutabeløp**, brukes salgsprisen som er angitt på prislinjen. 
1. Hvis verdiene i feltene **Produkt** og **Enhet** ikke samsvarer, eller hvis prismodellen er en annen enn **Valutabeløp**, settes salgssatsen til **0** (null) som standard. Dette skjer fordi Project Operations bare støtter prismodellen **Valutabeløp** for materiale som brukes i et prosjekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
