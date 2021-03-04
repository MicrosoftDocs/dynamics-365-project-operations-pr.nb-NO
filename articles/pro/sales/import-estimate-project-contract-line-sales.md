---
title: Importere et estimat til en prosjektbasert kontraktlinje – Lite
description: Dette emnet gir informasjon om hvordan du importerer økonomiske estimater fra et prosjekt til en kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b462af163fef1bfcbbc4f945df722d4e8a71fb1a
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177478"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importere et estimat til en prosjektbasert kontraktlinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan du importere estimater fra et prosjekt til en prosjektbasert kontraktlinje.

1. Kontroller at **Prosjekt**-feltet på den prosjektbaserte kontraktlinjen er fylt ut.
2. I kategorien **Kontraktlinjedetaljer** i delrutenettet velger du **Importer fra prosjektberegningen**. Det vises en dialogside med sammendragsalternativer. Tilgjengelige sammendragsalternativer er **Transaksjonsklasse**, **Kategori**, **Rolle** og **Prosjektoppgave**.
3. Avhengig av hva du velger for sammendrag, kopieres estimatet fra prosjektet for alle transaksjonsklasser og oppgaver som er inkludert på denne kontraktlinjen. Hvis du vil kontrollere hvilke transaksjonsklasser som er inkludert, velger du kategorien **Generelt** på den prosjektbaserte kontraktlinjen, og deretter kontrollerer du verdiene i feltene **Inkluder tid**, **Inkluder utgifter** og **Inkluder gebyrer**. 
4. Hvis du vil se hvilke oppgaver som er inkludert, velger du kategorien **Belastbare oppgaver** på kontraktlinjen. Basert på de tilknyttede oppgavene som har feltet **Inkluderte transaksjonsklasser** angitt til **Ja**, importeres alle estimater for disse kombinasjonene av oppgave og transaksjonsklasse til kontraktlinjen.

Når du importerer estimater, blir prissettingen som standard basert på prosjektprislistene som er knyttet til oppsettet av kontrakt og fakturatype på kontraktlinjen. Hvis en oppgave, rolle eller kategori er konfigurert på kontraktlinjen som ikke-belastbar, vil den importerte estimatlinjen være ikke-belastbar, og den vil ikke øke den verdien på kontraktlinjen.

Når en kontraktlinje har linjedetaljer, summeres feltene **Kontraktverdi** og **Beregnet mva** på kontraktlinjen, og de kan ikke redigeres.

Når det er merket av for flere sammendragsalternativer, prøver systemet å summere etter alle de valgte alternativene. Sammendragsresultatet fører til flere importerte kontraktlinjer enn hvis du velger bare ett sammendragsalternativ.

Hvis for eksempel prosjektet har følgende estimatlinjer for utgifter:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse**, blir følgende informasjon importert:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 1. oktober 2020 | 3.34 | 840 | 2800 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse** og **Kategori**, blir følgende informasjon importert:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| &nbsp;| Hotell | 1. oktober 2020 | 6 | 200 | 1200 |

Når brukeren velger å oppsummere etter **Transaksjonsklasse**, **Kategori** og **Bladnodeoppgave**, blir følgende informasjon importert. Legg merke til at dette resultatet er det samme som i prosjektet:

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]