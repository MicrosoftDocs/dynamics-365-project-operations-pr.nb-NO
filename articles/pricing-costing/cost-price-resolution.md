---
title: Fastslå kostnadssatser for prosjektbaserte estimater og faktiske verdier
description: Denne artikkelen inneholder informasjon om hvordan kostnadssatser i prosjektbaserte estimater og faktiske verdier fastsettes.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475291"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Fastslå kostnadssatser for prosjektbaserte estimater og faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

For å fastsette kostpriser på estimater og faktiske verdier i Microsoft Dynamics 365 Project Operations bruker systemet først datoen og valutaen i konteksten for innkommende estimat eller faktisk verdi til å fastsette salgsprislisten. Systemet bruker feltet **Transaksjonsdato** i den spesifikke konteksten for faktisk verdi til å fastsette hvilken prisliste som gjelder. Verdien for **Transaksjonsdato** for det innkommende estimatet eller den faktiske verdien sammenlignes med verdiene for **Effektiv startdato** (tidssoneuavhengig) og **Effektiv sluttdato** (tidssoneuavhengig) i prislisten. Når kostprislisten er fastsatt, fastsetter systemet kostnadssatsen.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Fastsette kostnadssatser kontekster for estimat og faktisk verdi for tid

Kontekst for estimat for **Tid** henviser til følgende:

- Tilbudslinjedetaljer for **Tid**.
- Kontraktlinjedetaljer for **Tid**.
- Ressurstilordninger i et prosjekt.

Kontekst for faktisk verdi for **Tid** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Tid**.
- Journallinjer som opprettes når en tidsoppføring sendes inn.

Når en kostprisliste er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

1. Systemet samsvarer kombinasjonen av feltene **Rolle**, **Ressursstyringsfirma** og **Ressursenhet** i konteksten for estimat eller faktisk verdi for **Tid** med rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prissettingsdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare andre felter enn eller i tillegg til **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje.
1. Hvis systemet finner en rolleprislinje som har en kostnadssats for kombinasjonen av **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, brukes denne kostnadssatsen som standard kostnadssats.
1. Hvis systemet ikke kan samsvare verdiene for **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, ignorerer det dimensjonen som har lavest prioritet, søker etter rolleprislinjer som har samsvar for de to andre dimensjonsverdiene, og fortsetter å ignorere dimensjoner helt til en samsvarende rolleprisrad blir funnet. Kostnadssatsen fra denne oppføringen blir brukt som standard kostnadssats. Hvis systemet ikke finner en samsvarende rolleprisrad, blir prisen satt til **0** (null) som standard.

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av feltene **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres den foregående virkemåten tilsvarende. Systemet henter rolleprisoppføringer som har verdier som samsvarer med hver prisdimensjonsverdi, i prioritert rekkefølge. Rader som har nullverdier for disse dimensjonene, kommer sist.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Fastsette kostnadssatser på faktiske og estimerte linjer for utgift

Kontekst for estimat for **Utgift** henviser til følgende:

- Tilbudslinjedetaljer for **Utgift**.
- Kontraktlinjedetaljer for **Utgift**.
- Utgiftsestimater i et prosjekt.

Kontekst for faktisk verdi for **Utgift** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Utgift**.
- Journallinjer som opprettes når en utgiftsoppføring sendes inn.

Når en kostprisliste er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

1. Systemet samsvarer kombinasjonen av feltene **Kategori** og **Enhet** i konteksten for estimat eller faktisk verdi for **Utgift** med kategoriprislinjene i prislisten.
1. Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av **Kategori** og **Enhet**, brukes denne kostnadssatsen som standard kostnadssats.
1. Hvis systemet ikke kan samsvare verdiene i feltene **Kategori** og **Enhet**, settes prisen til **0** (null) som standard.
1. Hvis systemet ikke kan finne en samsvarende kategoriprislinje i estimeringskonteksten, men prismodellen er en annen enn **Pris per enhet**, settes kostnadssatsen til **0** (null) som standard.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Fastsette kostnadssatser på linjer med faktiske verdier og estimatlinjer for materialer

Kontekst for estimat for **Materiale** henviser til følgende:

- Tilbudslinjedetaljer for **Materiale**.
- Kontraktlinjedetaljer for **Materiale**.
- Materialestimater i et prosjekt.

Kontekst for faktisk verdi for **Materiale** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Materiale**.
- Journallinjer som opprettes når en logg over materialbruk sendes inn.

Når en kostprisliste er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

1. Systemet bruker kombinasjonen av feltene **Produkt** og **Enhet** i konteksten for estimat eller faktisk verdi for **Materiale** mot prislisteelementlinjene i prislisten.
1. Hvis systemet finner en prislisteelementlinje som har en kostnadssats for kombinasjonen av **Produkt** og **Enhet**, brukes denne kostnadssatsen som standard kostnadssats.
1. Hvis systemet ikke kan samsvare verdiene for **Produkt** og **Enhet**, settes enhetskostnaden til **0** (null) som standard.
1. Hvis systemet ikke kan finne en samsvarende prislisteelementlinje i konteksten for estimat eller faktisk verdi, men prismodellen er en annen enn **Valutabeløp**, settes enhetskostnaden til **0** som standard. Dette skjer fordi Project Operations bare støtter prismodellen **Valutabeløp** for materiale som brukes i et prosjekt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
