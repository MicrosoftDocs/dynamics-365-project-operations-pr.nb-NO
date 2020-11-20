---
title: Tilbakekalle godkjente tids- eller utgiftsoppføringer
description: Dette emnet gir informasjon om hvordan du tilbakekaller en tidligere godkjent prosjekttid eller utgiftstransaksjon.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 102da39d5940874a8e1f4220437ecdf386a7187b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120555"
---
# <a name="recall-approved-time-or-expense-entries"></a>Tilbakekalle godkjente tids- eller utgiftsoppføringer

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Et prosjektteammedlem eller en annen person som sender en tids- eller utgiftsoppføring, kan tilbakekalle denne tids- eller utgiftsoppføringen etter at den er godkjent. Prosessen for å tilbakekalle en godkjent tids- eller utgiftsoppføring har to trinn:

1. En sender ber om en tilbakekalling.
2. En godkjenner godkjenner tilbakekallingen.

## <a name="request-a-recall"></a>Be om tilbakekalling

Følg disse trinnene for å be om tilbakekalling av en godkjent tids- eller utgiftsoppføring.

1. For tidsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Tidsoppføring**.

    –eller–

    For utgiftsoppføringer går du til **Prosjekter** \> **Mitt arbeid** \> **Utgifter**.

2. For tidsoppføringer velger du alle tidsoppføringer for en bestemt kombinasjon av et prosjekt og en oppgave. Du kan også merke enkeltcellene for tid på en bestemt dato for et bestemt prosjekt i rutenettet.

    –eller–

    For utgiftsoppføringer velger du raden for utgiftsoppføringen som skal tilbakekalles.

3. Velg **Tilbakekall**. En bekreftelsesdialogboks vises. Hvis de valgte tids- og utgiftsoppføringene allerede er godkjent, blir du bedt om å angi en årsak til tilbakekallingen.
4. Angi en årsak til tilbakekallingen, og velg deretter **OK** for å bekrefte operasjonen. Systemet sender personen som godkjente oppføringene, en forespørsel om å godkjenne tilbakekallingen.

> [!NOTE]
> Selv om godkjente tids- og utgiftsoppføringer kan tilbakekalles, kan ikke en tilbakekallingsforespørsel opprettes hvis et godkjent tid eller utgifts allerede er fakturert til kunden. En bruker som prøver å opprette en tilbakekallingsforespørsel, mottar en melding som angir at tiden eller utgiften ikke kan kalles tilbake fordi den allerede er fakturert.

## <a name="approve-or-reject-a-recall-request"></a>Godkjenne eller avvise en tilbakekallingsforespørsel

Følg denne fremgangsmåten for å godkjenne eller avvise en tilbakekallingsforespørsel.

1. Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.
2. På listesiden **Godkjenninger** endrer du visningen til **Tilbakekallingsforespørsler å godkjenne**. Det vises en liste over sendte forespørsler om tilbakekalling.
3. Velg én eller flere oppføringer, og velg deretter **Godkjenn** eller **Avvis**.
4. Hvis du valgte **Godkjenn**, får du en advarsel som forklarer innvirkningen av godkjenningen. Velg **OK** for å bekrefte handlingen. Tilbakekallingsforespørselen godkjennes.

    –eller–

    Hvis du valgte **Avvis**, blir tilbakekallingsforespørselen avvist.

> [!NOTE]
> Når en tilbakekalling blir forespurt, når en tilbakekalling blir godkjent, ser systemet etter eventuell fakturaaktivitet på tids- eller utgiftsoppføringer. Hvis en oppføring allerede er fakturert, eller hvis den er på et fakturautkast, mottar godkjenneren en feilmelding som sier at tiden eller utgiften ikke kan godkjennes for tilbakekalling fordi den allerede er fakturert.

## <a name="impact-of-a-recall-request"></a>Innvirkning av en tilbakekallingsforespørsel

Når en godkjenning tilbakekalles, får dette både driftsinnvirkning og finansiell innvirkning.

### <a name="operational-impact"></a>Driftsinnvirkning

Hvis en tilbakekallingsforespørsel godkjennes, merkes godkjenningsoppføringen som **Avvist**. Statusen for oppføringen endres til enten **Returnert** eller **Avvist**, avhengig av om det er en tidsoppføring eller en utgiftsoppføring.

Prosjektteammedlemmet kan vise oppføringer, redigere og sende oppføringer på nytt, eller slette oppføringer helt.

Hvis en tilbakekallingsforespørsel blir avvist, blir statusen for oppføringen fortsatt **Godkjent**, og oppføringen kan ikke redigeres av prosjektteammedlemmet eller godkjenneren for prosjektet.

### <a name="financial-impact"></a>Økonomisk innvirkning

Hvis en tilbakekallingsforespørsel godkjennes, oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:

- Feltet **Justeringsstatus** oppdateres til **Justert**.
- Feltet **Faktureringsstatus** oppdateres til **Kansellert**.

Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier. For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene. De eneste verdiene som ikke kopieres over, er antallsverdiene. Disse verdiene reverseres i stedet. Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**. Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres**, og feltet **Faktureringsstatus** settes til **Annullert**. På grunn av disse endringene vil det registrerte forbruket og restinntekten for prosjektet ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.

Hvis en tilbakekallingsforespørsel blir avvist, er det ingen økonomisk innvirkning på prosjektet.

## <a name="changes-to-time-entry-records"></a>Endringer i tidsregistreringsoppføringer

Illustrasjonen nedenfor viser endringene som utføres for godkjente tidsoppføringer når de tilbakekalles.

![Overganger for tidsoppføringstilstand](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Endringer i utgiftsregistreringsoppføringer

Illustrasjonen nedenfor viser endringene som utføres for godkjente utgiftsoppføringer når de tilbakekalles.

![Overganger for utgiftsoppføringstilstand](media/ExpenseEntryStateTransitions.png)
