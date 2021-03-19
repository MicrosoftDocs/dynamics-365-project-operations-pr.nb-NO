---
title: Nyskapte utgiftsrapporter
description: Denne emne forklarer den nye utformingen og nyskapte opplevelsen for innlegging av utgiftsrapport.
author: suvaidya
manager: AnnBe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: aaa7dd24915982cf137b5959f2f4c244b9c1e012
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499728"
---
# <a name="expense-reports-reimagined"></a>Nyskapte utgiftsrapporter

Oppføring av reiseregninger har blitt utformet på nytt for å forenkle prosessen og redusere tiden som kreves for å fullføre en rapport. Her er hovedkomponentene i den nye reiseregningsopplevelsen:

- Et nytt arbeidsområde for reiseregning som gjør det mulig å få tilgang til representantens utgifter.
- En ny kvitteringsfunksjon som passer bedre til å vise kvitteringer på hodenivå, og forenkle prosessen med å knytte kvitteringer til utgiftslinjer.
- Et nytt skrivebeskyttet rutenett som gjør det mulig å vise mange flere utgiftslinjer og flere kolonner med data. Nå kan du se alle spesifiserte linjer og dele linjer, sammen med de overordnede utgiftene.
- En forenklet rute for redigering av utgifter.
- Nyutformede feil, advarsler og policymeldinger for å gi den rette konteksten og forstå problemet og hvordan det kan løses. Vi har fjernet flere av meldingene som ble vist før brukerne kunne fullføre oppgavene sine og løse problemene.
- En ny side for å angi obligatoriske felt, valgfrie felt og felt som ikke skal tas med. På denne siden kan du redusere antall felt som må angis.
- Et nytt utseende og en ny stil for reiseregninger, slik at rapportene ikke lenger ser ut som om de ble utformet for regnskapsansatte.

Hvis du vil aktivere den nye opplevelsen, bruker du arbeidsområdet **Funksjonsbehandling** til å aktivere den nyskapte funksjonen **Reiseregning**. Når du aktiverer denne funksjonen, oppstår følgende handlinger:

- Det eksisterende arbeidsområdet for utgifter erstattes av det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet for utgiftsfelt.
- Ingen eksisterende menyelementer for reiseregninger (den eksisterende siden) eller felt for reiseregninger fjernes.
- Arbeidsflyter og godkjenninger fører deg fremdelses til den eksisterende reiseregningssiden.

## <a name="getting-started-video-for-new-users"></a>Komme-i-gang-video for nye brukere

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[Utgiftsopplevelsen i Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0)-videoen (vist ovenfor) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) tilgjengelig på YouTube.

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
| Legg til eksisterende utgifter og kvitterringer under oppretting av utgift | Når du oppretter utgiftsrapporter, kan du legge til alle utgifter eller velge ikke-tilknyttede utgifter. Ikke-tilknyttede utgifter er utgifter som ble importert fra feeden for bedriftskredittkortet, eller utgifter som ble manuelt opprettet av brukeren, men som ikke er knyttet til en utgiftsrapport.|
| Valutakalkulator | En valutakalkulator er lagt til, slik at du kan beregne valutakursen for direkte transaksjoner med flere valutaer. |
| Lagre og legg til nye utgiftslinjer | Knappene **Lagre** og **Ny** er tilgjengelige når nye utgifter angis, for å hjelpe deg med å angi utgiftslinjer raskt. |
| Bedre oversikt over delte og spesifiserte linjer | Spesifiserte og delte linjer blir lagt til direkte i listen over utgifter for å øke synligheten og hjelpe deg med å avgjøre om det er noen feil. |
| Vis kvitteringer under spesifisering | Kvitteringer kan vises under spesifisering. |
| Kontantforskuddvalg | Velg ett eller flere forskudd for å utføre én enkelt utgiftstransaksjon. |
| Kontantforskuddsaldo | Gå gjennom forskuddssaldoen i sanntid når du oppretter en utgiftsoppføring mot godkjente og betalte forskudd. |

Den første lanseringen er fokusert på scenarioer for utgiftsregistrering. Et gjennomgangs- eller godkjenningsscenario av reiseregninger vil fortsette å bruke den eksisterende siden for utgiftsoppføring.

Følgende funksjoner støttes ikke i det nyskapte utgiftsarbeidsområdet:

- Integrering av reiserekvisisjon
- Utgiftsoppføring for kostgodtgjørelse
- Midlertidig godkjennerstøtte
- Mulighet til å vise arbeidsflytlogg


[!INCLUDE[footer-include](../includes/footer-banner.md)]
