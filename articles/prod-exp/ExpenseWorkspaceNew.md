---
title: Ugiftsrapporter i ny utforming
description: Dette emnet gir informasjon om den nyutformede og nyskapte opplevelsen for oppføring av reiseregninger.
author: ryansandness
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: bd334d3404e9baae4f8314173834d9fbb708d574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993700"
---
# <a name="redesigned-expense-reports"></a>Ugiftsrapporter i ny utforming

Oppføring av reiseregninger har blitt utformet på nytt for å forenkle prosessen med å fylle dem ut og redusere tiden som kreves. Her er hovedkomponentene i den nye reiseregningsopplevelsen:

- Et nytt arbeidsområde for reiseregning som gjør det mulig å få tilgang til representantens utgifter.
- En ny kvitteringsfunksjon som passer bedre til å vise kvitteringer på hodenivå, og forenkle prosessen med å knytte kvitteringer til utgiftslinjer.
- Et nytt skrivebeskyttet rutenett som gjør det mulig å vise mange flere utgiftslinjer og flere kolonner med data. Nå kan du se alle spesifiserte linjer og dele linjer, sammen med de overordnede utgiftene.
- En forenklet rute for redigering av utgifter.
- Nyutformede feil, advarsler og policymeldinger hjelper deg med å sørge for at du har den rette konteksten for å forstå problemet og hvordan det kan løses. Microsoft har fjernet mange meldinger som ble vist før brukere hadde en salgsmulighet til å fullføre oppgavene sine og løse problemene, for eksempel en ufullstendig spesifiseringsmelding.
- En ny side for angivelse av hvilke felt som kreves av organisasjonen, hvilke felt som er valgfrie, og hvilke felt som ikke bør registreres. Denne siden hjelper til med å redusere antall felt som brukerne må angi.
- Et nytt utseende og en ny stil for reiseregninger, slik at rapportene ikke lenger ser ut som om de ble utformet for regnskapsansatte.

Hvis du vil aktivere den nye opplevelsen, bruker du arbeidsområdet **Funksjonsbehandling** til å aktivere den nyskapte funksjonen **Reiseregning**. Når du aktiverer denne funksjonen, oppstår følgende handlinger:

- Det eksisterende arbeidsområdet for utgifter erstattes av det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet for utgiftsfelt.
- Ingen eksisterende menyelementer for reiseregninger (den eksisterende siden) eller felt for reiseregninger fjernes.
- Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.

## <a name="new-features"></a>Nye funksjoner

| Ny funksjon | Beskrivelse |
|---|----|
| Synlighet for utgiftsfelt | På en ny konfigurasjonsside kan du angi hvilke felt som skal deaktiveres for en organisasjon, hvilke felt som må være obligatoriske, og hvilke felt som er anbefalt. |
| Obligatoriske felter | Med en ny enkel konfigurasjon kan du gjøre noen felt obligatoriske uten å måtte bruke policyrammeverket. |
| Valgfrie felt | Det er lagt til en ny side for valgfrie felt. På denne måten slipper de ansatte føle at de er nødt til å angi feltene, men feltene er fortsatt enkelt tilgjengelige. |
| Legg til kvitteringer som ikke er vedlagt | Muligheten til å legge til kvitteringer som ikke er vedlagt, i reiseregningen er mer synlig fra arbeidsområdet og i utgiftsrapporten. |
| Forbedrede meldinger | Det er bedre innsyn i utgiftslinjer som har advarsler eller feil. |
| Reduksjon i meldinger på meldingslinjen| Antallet infologg-meldinger ble redusert, og det ble gjort et forsøk på å forhindre at duplikate meldinger vises i mange tilfeller. |
| Vanlige handlinger gruppert sammen | Grensesnittet ble renset da det ble lagt til en ny handlingsknapp for de fleste vanlige handlinger på linjenivå, og tillegging av en ellipseknapp (...) for hodet og andre sjeldnere handlinger. |
| Nytt arbeidsområde for å øke synligheten | Et nytt arbeidsområde ensretter funksjoner og koblinger som gjør det mulig for brukerne å flytte til forskjellige områder. |
| Legg til eksisterende utgifter og kvitterringer under oppretting av utgift | Når du oppretter reiseregninger, kan du legge til alle eller valgte utgifter og kvitteringer. |
| Valutakalkulator | En valutakalkulator er lagt til, slik at du kan beregne valutakursen for direkte transaksjoner med flere valutaer. |
| Lagre og legg til nye utgiftslinjer | Knappene **Lagre** og **Ny** er tilgjengelige når nye utgifter angis, for å hjelpe deg med å angi utgiftslinjer raskt. |
| Bedre oversikt over delte og spesifiserte linjer | Spesifiserte og delte linjer blir lagt til direkte i listen over utgifter for å øke synligheten og hjelpe deg med å avgjøre om det er policyfeil eller andre feil. |
| Vis kvitteringer under spesifisering | Kvitteringer kan vises under spesifisering. |

Den første lanseringen er fokusert på scenarioer for utgiftsregistrering. Et gjennomgangs- eller godkjenningsscenario av reiseregninger vil fortsette å bruke den eksisterende siden for utgiftsoppføring.

Følgende funksjoner finnes på den eksisterende siden, men fortsatt ikke på den nye siden. Disse funksjonene vil bli innført på nytt i de neste utgivelsene:

- Godkjenninger
- Godkjenning av leverandørgjelde og muligheten til å redigere regnskapet
- Flere oppføringspunkter
- Integrering av reiserekvisisjon
- Dataenhet for synlighet av utgiftsfelt
- Oppføring for kostgodtgjørelsesutgifter
- Arbeidsflyt på linjenivå
- Midlertidig godkjennerstøtte
- Avansert spesifisering


[!INCLUDE[footer-include](../includes/footer-banner.md)]