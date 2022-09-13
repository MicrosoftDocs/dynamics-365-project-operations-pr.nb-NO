---
title: Fastslå kostnadssatser for prosjektestimater og faktiske verdier
description: Denne artikkelen inneholder informasjon om hvordan kostnadssatser i prosjektestimater og faktiske verdier fastsettes.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410167"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Fastslå kostnadssatser for prosjektestimater og faktiske verdier

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

For å fastsette kostprislisten og kostnadssatser i konteksten for estimat og faktisk verdi bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktsenhet** i det relaterte prosjektet.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Fastsette kostnadssatser kontekster for estimat og faktisk verdi for tid

Kontekst for estimat for **Tid** henviser til følgende:

- Tilbudslinjedetaljer for **Tid**.
- Kontraktlinjedetaljer for **Tid**.
- Ressurstilordninger i et prosjekt.

Kontekst for faktisk verdi for **Tid** henviser til følgende:

- Oppførings- og korrigeringsjournallinjer for **Tid**.
- Journallinjer som opprettes når en tidsoppføring sendes inn.

Når en kostprisliste for salg er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

1. Systemet samsvarer kombinasjonen av feltene **Rolle** og **Ressursenhet** i konteksten for estimat eller faktisk verdi for **Tid** med rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prissettingsdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare andre felter enn eller i tillegg til **Rolle** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje.
1. Hvis systemet finner en rolleprislinje som har en kostnadssats for kombinasjonen av **Rolle** og **Ressursenhet**, brukes denne kostnadssatsen som standard kostnadssats.
1. Hvis systemet ikke kan samsvare verdiene til **Rolle** og **Ressursenhet**, henter det rolleprislinjer som har samsvarende verdier for **Rolle**-feltet, men nullverdier for feltet **Ressursenhet**. Når systemet har funnet en samsvarende rolleprisoppføring, brukes kostnadssatsen fra denne oppføringen som standard kostnadssats.

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

Når en kostprisliste for salg er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

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

Når en kostprisliste for salg er fastsatt, fullfører systemet følgende trinn for å angi standard kostnadssats.

1. Systemet bruker kombinasjonen av feltene **Produkt** og **Enhet** i konteksten for estimat eller faktisk verdi for **Materiale** mot prislisteelementlinjene i prislisten.
1. Hvis systemet finner en prislisteelementlinje som har en kostnadssats for kombinasjonen av **Produkt** og **Enhet**, brukes denne kostnadssatsen som standard kostnadssats.
1. Hvis systemet ikke kan samsvare verdiene for **Produkt** og **Enhet**, settes enhetskostnaden til **0** (null) som standard.
1. Hvis systemet ikke kan finne en samsvarende prislisteelementlinje i konteksten for estimat eller faktisk verdi, men prismodellen er en annen enn **Valutabeløp**, settes enhetskostnaden til **0** som standard. Dette skjer fordi Project Operations bare støtter prismodellen **Valutabeløp** for materiale som brukes i et prosjekt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
