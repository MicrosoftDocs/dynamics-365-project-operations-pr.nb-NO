---
title: Tilbakekalling av tidligere godkjente oppføringer
description: Denne emne forklarer hvordan et prosjektteammedlem kan be om tilbakekalling av tidligere sendte og godkjente oppføringer for tids-, utgifts- og materialbruk, og hvordan en prosjektleder kan godkjenne eller avvise forespørsler om tilbakekalling.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586586"
---
# <a name="recall-previously-approved-entries"></a>Tilbakekalling av tidligere godkjente oppføringer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Et prosjektteammedlem som sender en tids-, utgifts- eller materialbruksoppføring, kan tilbakekalle denne oppføringen etter at den er godkjent. Tilbakekallingsprosessen har to hovedtrinn:

1. En sender ber om en tilbakekalling.
2. En godkjenner godkjenner forespørselen.

## <a name="request-a-recall"></a>Be om tilbakekalling

Følg disse trinnene for å be om tilbakekalling av godkjente tids-, utgifts- eller materialbruksoppføringer.

1. Følg ett av disse trinnene, avhengig av typen oppføring du vil tilbakekalle:

    - For tidsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Tidsoppføring** og velger alle tidsoppføringer for en bestemt kombinasjon av et prosjekt og en oppgave. Du kan også merke enkeltcellene for tid på en bestemt dato for et bestemt prosjekt i rutenettet.
    - For utgiftsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Utgifter** og velger raden for utgiftsoppføringen som skal tilbakekalles.
    - For materialbruksoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Logg over materialbruk** og velger raden for materialbruksoppføringen som skal tilbakekalles.

2. Velg **Tilbakekall**. En bekreftelsesdialogboks vises. Hvis de valgte tids-, utgifts- eller materialbruksoppføringene allerede er godkjent, blir du bedt om å angi en årsak til tilbakekallingen.
3. Angi en årsak til tilbakekallingen, og velg deretter **OK** for å bekrefte operasjonen. Systemet sender personen som godkjente oppføringene, en forespørsel om å godkjenne tilbakekallingen.

> [!IMPORTANT]
> Du kan ikke opprette en tilbakekallingsforespørsel for en godkjent tids-, utgifts- eller materialbruksoppføring som allerede er fakturert til kunden. Hvis du prøver, får du en melding som sier at tids-, utgifts- eller materialbruksoppføringen ikke kan tilbakekalles fordi den allerede er fakturert. I dette tilfellet kan du bare be om en tilbakekalling av oppføringen hvis en korrigeringsfaktura brukes til å gi kunden full kreditt eller refundering på den opprinnelige fakturaen.

## <a name="approve-or-reject-a-recall-request"></a>Godkjenne eller avvise en tilbakekallingsforespørsel

Følg denne fremgangsmåten for å godkjenne eller avvise en tilbakekallingsforespørsel.

1. Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.
2. På listesiden **Godkjenninger** endrer du visningen til **Tilbakekallingsforespørsler å godkjenne**. Det vises en liste over sendte forespørsler om tilbakekalling.
3. Velg én eller flere oppføringer, og velg deretter **Godkjenn** eller **Avvis**.
4. Hvis du valgte **Godkjenn**, får du en advarsel som forklarer innvirkningen av godkjenningen. Velg **OK** for å bekrefte handlingen. Tilbakekallingsforespørselen godkjennes.

    –eller–

    Hvis du valgte **Avvis**, blir tilbakekallingsforespørselen avvist.

> [!IMPORTANT]
> Når en tilbakekalling er godkjent, ser systemet etter eventuell fakturaaktivitet på tids-, utgifts- eller materialbruksoppføringer, akkurat som når den ble forespurt. Hvis en oppføring allerede er fakturert, eller hvis den er på et fakturautkast, mottar godkjenneren en feilmelding som sier at tiden eller utgiften ikke kan godkjennes for tilbakekalling fordi den allerede er fakturert. I dette tilfellet kan godkjenneren bare godkjenne tilbakekallingen hvis en korrigeringsfaktura brukes til å gi kunden full kreditt eller refundering på den opprinnelige fakturaen.

## <a name="impact-of-a-recall-request"></a>Innvirkning av en tilbakekallingsforespørsel

Når en godkjenning tilbakekalles, får dette både driftsinnvirkning og finansiell innvirkning.

### <a name="operational-impact"></a>Driftsinnvirkning

Hvis en tilbakekallingsforespørsel godkjennes, merkes godkjenningsoppføringen som **Avvist**. Statusen for oppføringen endres til enten **Returnert** eller **Avvist**, avhengig av om det er en tidsoppføring eller en utgifts- eller materialbruksoppføring.

Prosjektteammedlemmet kan vise oppføringer, redigere og sende oppføringer på nytt, eller slette oppføringer fullstendig.

Hvis en tilbakekallingsforespørsel blir avvist, blir statusen for oppføringen fortsatt **Godkjent**, og oppføringen kan ikke redigeres av prosjektteammedlemmet eller godkjenneren for prosjektet.

### <a name="financial-impact"></a>Økonomisk innvirkning

Hvis en tilbakekallingsforespørsel godkjennes, oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:

- Feltet **Justeringsstatus** oppdateres til **Justert**.
- Feltet **Faktureringsstatus** oppdateres til **Kansellert**.

Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier. For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene. De eneste verdiene som ikke kopieres over, er antallsverdiene. Disse verdiene reverseres i stedet. Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**. Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres**, og feltet **Faktureringsstatus** settes til **Annullert**. På grunn av disse endringene vil det registrerte forbruket og restinntekten for prosjektet ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.

Hvis en tilbakekallingsforespørsel blir avvist, er det ingen økonomisk innvirkning på prosjektet.

## <a name="changes-to-time-entry-records"></a>Endringer i tidsregistreringsoppføringer

Illustrasjonen nedenfor viser endringene som utføres for godkjente tidsoppføringer og de tilsvarende godkjenningsoppføringene når de tilbakekalles.

![Overganger for tidsoppføringstilstand.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Endringer i registreringsoppføringer for utgifter og materialbruk

Illustrasjonen nedenfor viser endringene som utføres for godkjente utgifts- og materialbruksoppføringer og de tilsvarende godkjenningsoppføringene når de tilbakekalles.

![Overganger for utgiftsoppføringstilstand.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
