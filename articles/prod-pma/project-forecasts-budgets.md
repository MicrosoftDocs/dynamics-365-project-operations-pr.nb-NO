---
title: Prosjektprognoser og budsjetter
description: Microsoft Dynamics 365 Finance inneholder prosjektprognoser og prosjektbudsjetter, slik at du kan administrere og kontrollere prosjektene dine.
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081733"
---
# <a name="project-forecasts-and-budgets"></a>Prosjektprognoser og budsjetter

[!include [banner](../includes/banner.md)]

Det er to måter å administrere og kontrollere prosjektene på: prosjektprognoser og prosjektbudsjetter. 

Bruk prosjektprognoser hvis organisasjonen har et driftsperspektiv og hvis den fokuserer på inntekter og kostnader som er avledet fra bestemte transaksjoner. Bruk prosjektbudsjettering hvis organisasjonen fokuserer mer på finansbeløpene. 

Både prosjektprognoser og prosjektbudsjetter bruker prognosemodeller til å oppbevare de prosjekterte transaksjonsbeløpene. 

Hver metode har sine fordeler. Du bør vurdere følgende punkter før du velger en metode for organisasjonen.

|   Tilordningsmetode       |           Prosjektprognose            |        Prosjektbudsjettering                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **Periodetilordning**     | Du kan ikke eksplisitt tilordne transaksjoner til et regnskapsperiode. I stedet er prognosen og kontrollen for prognosen basert på levetiden til prosjektet. Siden prognoser er basert på en bestemt dato, må du utlede perioden fra datoen. | Du kan tilordne transaksjoner til hele prosjektet eller en regnskapsperiode. Hvis du tildeler over en periode, kan du videreføre ubrukte beløp til neste regnskapsperiode. |
| **Vise transaksjoner**  | Du kan vise transaksjoner i prognoseskjemaer, der du kan se prognosene for hele firmaet og for alle prosjekter, uavhengig av hierarkiet. Du kan fokusere på et bestemt prosjekt ved å filtrere dataene.                                       | Du kan vise budsjetterte transaksjoner for ett enkelt prosjekthierarki. Derfor kan du vise transaksjonsdetaljer for et overordnet prosjekt eller tilhørende delprosjekter.                 |
| **Transaksjonsvariabler** | Når du skriver inn prognosetransaksjoner, kan du bruke hvert attributt som finnes for en faktisk transaksjon. Dette gir mer detaljert informasjon i prognosen. Du kan for eksempel angi detaljer om antall, arbeidere, elementer eller linjeegenskaper.         | Når du angir budsjettdetaljer, kan du bruke bare beløp, kategorier og aktiviteter.                    |
| **Sikkerhet**              | Prognoser er basert på transaksjoner som du angir i prognoseplanen, og som ikke innebærer noen prosesskontrollmekanisme. Alle arbeidere som har tillatelser til et prognoseskjema, kan revidere informasjon uten godkjenning.                                        | Ved budsjettering brukes arbeidsflytsystemet, som gjør det mulig å bruke endringsadministrasjon, og du kan opprettholde en logg over endringene.         |
| **Oppføringstyper**           | Transaksjonsoppføringer for prognoser er basert på antall enheter og kostnader og salgsenhetspriser.  | Budsjettdetaljer er basert på beløp, som deles mellom kostnader og inntekter.                                          |
| **Prognosemodeller**       | Siden hver prognose må tilknyttes en modell, kan du opprette flere prognosemodeller og også konfigurere undermodeller.           | Prosjektbudsjettering begrenser prognosemodellene som brukes til budsjettering. Færre prognosemodeller kan bidra til å øke konsekvensen i projeksjoner.                           |
| **Kostnadsoverskridelser**         | Du kan bare tillate eller ikke tillate kostnadsoverskridelse av transaksjoner som vil føre til et kostnadsoverskridelse.   | Prosjektbudsjettering gir flere kontrollalternativer for brukere. Du kan tillate advarsler og overskridelser.                    |
| **Kontroll**               | Prognosekontroll utføres ved hjelp av prognosereduksjon. Faktiske beløp trekkes fra transaksjonssaldoer for prognoser uten revisjonsspor. Dette kan gjøre det vanskeligere å spore hvor de faktiske transaksjonene inntraff.                   | I prosjektbudsjettkontrollen trekkes faktiske beløp fra beløp i det gjenstående budsjettet. Dette gjør det mulig å tilbakestille revisjonsspor.                                   |

## <a name="project-forecasts"></a>Prosjektprognoser
Når du bruker prosjektprognoser, kan du angi prognosetransaksjoner i prognoseskjemaer for hver transaksjonstype. Hvert attributt som er tilgjengelig for en faktisk transaksjon, kan brukes for en prognosetransaksjon, for eksempel linjefortjeneste, linjeattributter, arbeidere eller beskrivelser. Du kan også projisere hvor lenge etter at en kostnad påløper, at en kunde faktureres. 

Prognosetransaksjoner er basert på enheter og beløp. 

Du må knytte hver prosjektprognose til en prognosemodell. Når du skriver inn en prognosetransaksjon, foreslås det automatisk en prognosemodell. Prognosemodellen fungerer som en beholder for prognosetransaksjonene. 

Du kan angi prognosemodeller som undermodeller for en modell. På denne måten kan du lage prognoser etter region, tidsperiode og avdeling. Du kan kopiere prognosetransaksjonene i en modell for å opprette en ny modell, og du kan også overføre transaksjonene til økonomimodulen. Fordi det finnes en én-til-én-relasjon mellom en prognose og en modell, utgjør hver prognosemodell et separat budsjett for et prosjekt. 

Prognosemodeller kan bruke prognosereduksjon som en kontrollmekanisme for prosjekter. Ved prognosereduksjon reduserer faktiske transaksjoner prognosetransaksjonssaldoer. Siden prognosereduksjon brukes på det høyeste prosjektet i hierarkiet, gir det imidlertid en begrenset visning av endringene i prognosen. Hvis for eksempel en arbeider er tilknyttet et delprosjekt, blir de faktiske transaksjonene for arbeideren postert til det overordnede prosjektet. Dette kan gjøre det vanskelig å spore endringer fordi du ikke enkelt kan bestemme hvilken transaksjon i hvilket delprosjekt som førte til en reduksjon i prognosebeløpet. Derfor er det lurt å opprette en kopi av en prognosemodell som prognosereduksjon skal bruke. Du kan deretter bruke rapporter til å vise hva som opprinnelig ble anslått. 

Du kan revidere, kopiere, slette eller overføre prosjektprognoser til et økonomimodulbudsjett. Det er imidlertid ingen prosesskontroll. Alle arbeidere som har rettighet til et prognoseskjema, kan gjøre endringer uten gjennomgang.

-   **Revider** – Du kan revidere en prognosetransaksjon i de samme skjemaene der de opprinnelige oppføringene ble utført.
-   **Kopier eller slett** – Når du kopierer prognosetransaksjoner, kopierer du transaksjonslinjene for én prognosemodell til en annen prognosemodell. Når du sletter en prognose, sletter du prognosetransaksjonene fra en prognosemodell. Hvis du vil begrense prognosetransaksjonene som blir kopiert eller slettet, velger du bestemte transaksjonstyper og -datoer. Dette gjør det mulig for deg å kopiere eller slette bare bestemte deler av en prognose.
-   **Overfør** – Når du overfører en prosjektprognose til et økonomimodulbudsjett, overfører du prognosetransaksjonene for en prognosemodell til et økonomimodulbudsjett. Du kan overskrive alle tidligere overførte transaksjoner i økonomimodulbudsjettet som du overfører prosjektprognosen til.

## <a name="project-budgets"></a>Prosjektbudsjetter
Prosjektbudsjettering er en enklere metode enn prognostisering, selv om den integreres med prognosemodeller. Det bruker et enkelt oppføringsskjema for de opprinnelige budsjettdetaljene og -endringene, og tillater projeksjoner som bare er basert på beløp, kategori eller aktivitet. 

I prosjektbudsjettering må alle opprinnelige budsjetter og revisjoner sendes til en prosjektarbeidsflyt for godkjenning. Arbeidsflyter gir deg økt kontroll over prosessen og oppretter en endringsloggoppføring. 

Prosjektbudsjettering ligner økonomimodulbudsjettering, men er raskere og enklere å konfigurere. Mange av alternativene i økonomimodulbudsjettering, for eksempel nummerserier eller valuta, må ikke konfigureres separat for prosjekter.

Prosjektbudsjetter knyttes automatisk til to prognosemodeller, én for opprinnelig budsjett og én for gjenstående budsjett. Derfor kan rapporter som er basert på prognosemodeller, bruke budsjettdata. Når et prosjektbudsjett er utført, oppretter systemet prognosetransaksjoner basert på de tilknyttede modellene, som brukes til rapporterings- og kontrollformål.

## <a name="forecast-models"></a>Prognosemodeller
Prognosemodeller har et hierarki med ett lag. Dette betyr at én prosjektprognose må tilknyttes én prognosemodell.

Hvis du bruker prosjektprognose, kan du identifisere modeller som undermodeller. Du kan deretter opprette prognoser etter avdeling, tidsperiode og område. Du kan for eksempel opprette en prognosemodell for et år, og deretter kan du opprette undermodeller for regionale prognose for nordøst, sørøst, nordvest og sørvest som regionale ledere sender. Ved å velge forskjellige alternativer i de tilgjengelige rapportene, kan du vise informasjon etter total prognose eller etter delmodell.





[!INCLUDE[footer-include](../includes/footer-banner.md)]