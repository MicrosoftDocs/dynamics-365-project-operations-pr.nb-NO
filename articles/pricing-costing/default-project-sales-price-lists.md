---
title: Standard prislister
description: Denne artikkelen inneholder informasjon om standard salgs- og kostprislister i Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410275"
---
# <a name="default-price-lists"></a>Standard prislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

## <a name="sales-price-lists"></a>Salgsprislister

Hvert prosjekttilbud og hver kontrakt i Dynamics 365 Project Operations inneholder en standard salgsprisliste. 

### <a name="price-list-default-on-project-quotes"></a>Prisliste som standard i prosjekttilbud
Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal være standard i et prosjekttilbud:

1. Systemet ser på prislistene som er knyttet til forretningsforbindelsens prosjektprislister. 
1. Hvis det ikke finnes prosjektprislister som er knyttet til forretningsforbindelsesoppføringen, ser systemet på salgsprislistene som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjekttilbudet.
1. Deretter kontrollerer systemet datogyldigheten for prislistene som samsvarer med datointervallet for prosjekttilbudet. Spesielt gjelder dette for datoen da tilbudet ble opprettet.
1. Hvis det finnes flere prislister som er gyldige for datoen for prosjekttilbudet, blir alle prislistene standard i prosjekttilbudet.
1. Hvis det ikke er noen prislister som gjelder for datoen for prosjekttilbudet, finnes det ingen standard prosjektprisliste for prosjekttilbudet. Det vises en advarsel for prosjekttilbudet. Meldingen angir at faktiske verdier og estimater i prosjektet ikke vil være priset, siden det ikke finnes noen vedlagte prosjektprislister.

### <a name="price-list-default-on-project-contracts"></a>Prisliste som standard i prosjektkontrakter 
Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal være standard i en prosjektkontrakt:

1. Hvis kontrakten opprettes fra et tilbud, kopieres prosjektprislistene i tilbudet separat og knyttes til prosjektkontrakten.
1. Hvis kontrakten opprettes fra grunnen av, ser systemet på prislistene som er knyttet til prosjektprislistene for forretningsforbindelsen. Hvis det ikke finnes prosjektprislister som er knyttet til forretningsforbindelsesoppføringen, ser systemet etter salgsprislister som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjektkontrakten.
1. Deretter kontrollerer systemet datogyldigheten for prislistene som samsvarer med datointervallet for prosjektkontrakten. Spesielt gjelder dette for datoen da kontrakten ble opprettet.
1. Hvis det finnes flere prislister som er gyldige for datoen for prosjektkontrakten, blir alle prislistene standard i prosjektkontrakten.
1. Hvis det ikke er noen prislister som gjelder for datoen for kontrakten, finnes det ingen standard prosjektprislister for kontrakten. Det vises en advarsel for prosjektkontrakten. Meldingen angir at faktiske verdier og estimater i prosjektet ikke vil være priset, siden det ikke finnes noen vedlagte prosjektprislister.

## <a name="cost-price-lists"></a>Kostprislister

Kostprislister er ikke standard for noen som helst enhet i Project Operations. Det å fastsette kostprislisten som skal brukes for prosjektkostnader, utføres alltid per transaksjon. Systemet fullfører følgende prosess for å avgjøre hvilken prisliste som skal brukes for prosjektkostnader:

1. Systemet ser på prislistene som er knyttet til kontraktorganisasjonsenheten for prosjektet.
1. Deretter ser systemet på datogyldigheten for prislistene som samsvarer med datoen for konteksten for innkommende estimat eller konteksten for faktisk verdi.

    - *Kontekst for estimat* refererer til enhver av tre kontekster av estimering i Project Operations:

        - Prosjektestimatlinje
        - Tilbudslinjedetalj
        - Kontraktlinjedetalj

    - *Kontekst for faktisk verdi* refererer til enhver av tre kilder for faktiske verdier i Project Operations:

       - Oppføringsjournallinjer som opprettes manuelt, eller korrigeringsjournallinjer som opprettes i en korrigeringsjournal
       - Journallinjer som opprettes under innsending av tids-, utgifts- eller materialbrukslogger
       - Fakturalinjedetalj

    Når Project Operations samsvarer datogyldighet for den innkommende journallinjen eller fakturalinjedetaljen i *konteksten for faktisk verdi*, brukes feltet **Transaksjonsdato**.

    - Hvis flere prislister gjelder for datoen for konteksten for innkommende estimat eller konteksten for faktisk verdi, velges den sist opprettede prislisten.
    - Hvis ingen prislister er knyttet til kontraktorganisasjonsenheten for prosjektet, ser systemet på kostprislistene som er knyttet til prosjektparameterne som samsvarer med valutaen for prosjektet.

## <a name="enable-multi-currency-cost-price-list"></a>Aktiver kostprisliste med flere valutaer

Du finner denne innstillingen i **Innstillinger** \> **Parametere**. Standardverdien er **Nei**.

Når denne innstillingen er aktivert (det vil si at verdien er satt til **Ja**), fungerer systemet på følgende måte:

- Det tillater at kostprislister i enhver valuta knyttes til organisasjonsenheten. En kostprisliste i valutaen EUR kan for eksempel knyttes til en organisasjonsenhet i valutaen USD. Systemet fortsetter å validere at kostprislister som knyttes til en organisasjonsenhet, ikke har overlappende datogyldighet.
- Det validerer at kostprislister som er knyttet til prosjektparametere, ikke har overlappende datogyldighet, selv om de har ulike valutaer. Denne virkemåten er forskjellig fra standardvirkemåten (det vil si virkemåten når verdien er satt til **Nei**). I standardvirkemåten valideres bare kostprislister som har **samme** valuta, for ikke-overlappende datogyldighet.
- For en kontekst for innkommende transaksjon fastsetter den kostprislisten basert på bare datogyldighet. Denne virkemåten skiller seg fra standardvirkemåten, der systemet velger kostprislisten som samsvarer med både valutaen til prosjektet og datogyldighet.

På grunn av disse endringene i virkemåte kan Project Operations-kunder vedlikeholde en global kostprisliste som blir relevant for hele selskapet. De trenger ikke å ha prislister i hver valuta for operasjoner. Den globale prislisten har datogyldighet og gjør at kostnadssatser kan angis i hvilken som helst valuta for en bestemt kombinasjon av prisdimensjonsverdier. Valutaen for kostprislisten brukes bare til å angi standardverdier når elementoppføringer for **Rollepriser**, **Kategoripriser** og **Prisliste** opprettes. Den brukes ikke til å fastsette prislisten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
