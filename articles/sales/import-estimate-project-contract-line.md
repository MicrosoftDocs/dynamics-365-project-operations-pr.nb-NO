---
title: Importere et estimat til en prosjektbasert kontraktlinje
description: Dette emnet gir informasjon om hvordan du importerer estimater fra et prosjekt til en kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6dde924c24dcffe2a8fb690e6eb429e4c3d9fb28
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126405"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importere et estimat til en prosjektbasert kontraktlinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

I Dynamics 365 Project Operations kan du importere estimater fra et prosjekt til en prosjektbasert kontraktlinje.

1. Kontroller at **Prosjekt**-feltet på den prosjektbaserte kontraktlinjen er fylt ut.
2. I kategorien **Kontraktlinjedetaljer** i delrutenettet velger du **Importer fra prosjektberegningen**. Det vises en dialogside med sammendragsalternativer. Tilgjengelige sammendragsalternativer er **Transaksjonsklasse**, **Kategori**, **Rolle** og **Prosjektoppgave**. Avhengig av valgene for sammendrag kopieres estimatet fra prosjektet for alle transaksjonsklassene og oppgavene som er inkludert på denne kontraktlinjen. 
3. Hvis du vil kontrollere hvilke transaksjonsklasser som er inkludert, velger du kategorien **Generelt** på kontraktlinjen, og deretter kontrollerer du verdiene i feltene **Inkluder tid**, **Inkluder utgifter** og **Inkluder gebyrer**.

Når du importerer estimater, blir prissettingen som standard basert på prosjektprislistene som er knyttet til kontrakten og fakturatypen som er konfigurert på kontraktlinjen. Hvis en rolle eller kategori er konfigurert på kontraktlinjen som ikke-belastbar, vil den importerte estimatlinjen for rollen eller kategorien være ikke-belastbar, og den vil ikke øke den verdien på kontraktlinjen.

Når en kontraktlinje har linjedetaljer, summeres feltene **Kontraktverdi** og **Beregnet mva** på kontraktlinjen, og de kan ikke redigeres.

Når det er merket av for flere sammendragsalternativer, prøver systemet å summere etter alle de valgte alternativene. Sammendragsresultatet fører til flere importerte kontraktlinjer enn hvis du velger bare ett sammendragsalternativ.

Hvis for eksempel prosjektet hadde følgende estimatlinjer for utgifter:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse**, blir følgende informasjon importert:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1. oktober 2020 | 3.34 | 840 | 2800 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse** og **Kategori**, blir følgende informasjon importert:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotell | 1. oktober 2020 | 6 | 200 | 1200 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse**, **Kategori** og **Bladnodeoppgave**, blir følgende informasjon importert. Legg merke til at dette resultatet er det samme som det som var i prosjektet:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |
