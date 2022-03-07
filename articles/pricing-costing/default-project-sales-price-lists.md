---
title: Standard prislister
description: Dette emnet gir information om standard salgs- og kostprislister i Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5e38e2f0b553b789956c6d73d481ab0ed2ce3a77815e7cf8c058a0b4666c558
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989878"
---
# <a name="default-price-lists"></a>Standard prislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

## <a name="sales-price-lists"></a>Salgsprislister

Hvert prosjekttilbud og hver kontrakt i Dynamics 365 Project Operations inneholder en standard salgsprisliste. 

### <a name="price-list-default-on-project-quotes"></a>Prisliste som standard i prosjekttilbud
Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal være standard i et prosjekttilbud:

1. Systemet ser på prislistene som er knyttet til forretningsforbindelsens prosjektprislister. 
2. Hvis det finnes prosjektprislister som er knyttet til forretningsforbindelsesoppføringen, ser systemet på salgsprislistene som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjekttilbudet.
3. Deretter kontrollerer systemet datogyldigheten for prislistene som samsvarer med datointervallet for prosjekttilbudet. Spesielt gjelder dette for datoen da tilbudet ble opprettet.
4. Hvis det finnes flere prislister som er gyldige for datoen for prosjekttilbudet, blir alle prislistene standard i prosjekttilbudet.
5. Hvis det ikke er noen prislister som gjelder for datoen for prosjekttilbudet, finnes det ingen standard prosjektprisliste for prosjekttilbudet. Det vises en advarsel for prosjekttilbudet. Meldingen angir at faktiske verdier og estimater i prosjektet ikke vil være priset, siden det ikke finnes noen vedlagte prosjektprislister.

### <a name="price-list-default-on-project-contracts"></a>Prisliste som standard i prosjektkontrakter 
Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal være standard i en prosjektkontrakt:

1. Hvis kontrakten opprettes fra et tilbud, kopieres prosjektprislistene i tilbudet separat og knyttes til prosjektkontrakten.
2. Hvis kontrakten opprettes fra grunnen av, ser systemet på prislistene som er knyttet til prosjektprislistene for forretningsforbindelsen. Hvis det ikke finnes prosjektprislister som er knyttet til forretningsforbindelsesoppføringen, ser systemet etter salgsprislister som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjektkontrakten.
4. Deretter kontrollerer systemet datogyldigheten for prislistene som samsvarer med datointervallet for prosjektkontrakten. Spesielt gjelder dette for datoen da kontrakten ble opprettet.
5. Hvis det finnes flere prislister som er gyldige for datoen for prosjektkontrakten, blir alle prislistene standard i prosjektkontrakten.
6. Hvis det ikke er noen prislister som gjelder for datoen for kontrakten, finnes det ingen standard prosjektprislister for kontrakten. Det vises en advarsel for prosjektkontrakten. Meldingen angir at faktiske verdier og estimater i prosjektet ikke vil være priset, siden det ikke finnes noen vedlagte prosjektprislister.

## <a name="cost-price-lists"></a>Kostprislister

Kostprislister er ikke standard for noen som helst enhet i Project Operations. Det å bestemme kostprislisten som skal brukes for prosjektkostnader, utføres alltid i øyeblikket. Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal brukes for prosjektkostnader:

1. Systemet ser først etter prislistene som er knyttet til kontraktorganisasjonsenheten for prosjektet.
2. Deretter ser systemet på datogyldigheten for prislistene som samsvarer med datoen for det innkommende estimatet eller den faktiske linjen. I denne situasjonen refererer *estimatlinjen* til alle tre kontekster av estimering i Project Operations:

    - Prosjektestimatlinje
    - Tilbudslinjedetalj
    - Kontraktlinjedetalj
  
3. Hvis det finnes flere prislister som gjelder for datoen i det innkommende estimatet eller de faktiske verdien, velges den sist opprettede prislisten.
4. Hvis det ikke finnes prislister som er knyttet til kontraktorganisasjonsenheten for prosjeket, ser systemet på kostprislistene som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjektet.
5. Deretter ser systemet på datogyldigheten for prislistene som samsvarer med datoen for det innkommende estimatet eller den faktiske linjen. 
6. Hvis det finnes flere prislister som gjelder for datoen i det innkommende estimatet eller de faktiske verdien, velges den sist opprettede prislisten.
7. Hvis det ikke er knyttet noen kostprislister til prosjektparameterne som samsvarer med valutaen og den gyldige datoen, settes kostnadssatsen til null (0) på det innkommende estimatet eller den faktiske linjen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]