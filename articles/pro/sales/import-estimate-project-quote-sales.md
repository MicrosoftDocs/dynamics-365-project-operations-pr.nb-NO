---
title: Importere estimater fra et prosjekt til en prosjekttilbudslinje
description: Denne artikkelen inneholder informasjon om hvordan du importerer estimater fra et prosjekttilbudslinje.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824499"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Importere estimater fra et prosjekt til en prosjekttilbudslinje 

_**Gjelder for:** Lite-distribusjon – avtale til proformafakturering, Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Hvis det opprettes et prosjekt i løpet av trinnet før salg, kan du velge å importere det økonomiske estimatet fra prosjektet til den prosjektbaserte tilbudslinjen.

1. Pass på at den prosjektbaserte tilbudslinjen har prosjektinformasjonen i **Prosjekt**-feltet.
2. I kategorien **Tilbudslinjedetaljer** velger du **Importer fra prosjektberegningen**.
3. Velg ett av følgende alternativer for oppsumering i dialogboksen som åpnes.

  - **Transaksjonsklasse**
  - **Kategori**
  - **Rolle** 
  - **Prosjektoppgave**

Avhengig av hva du velger, kopieres estimatet fra prosjektet for alle transaksjonsklasser som er inkludert i tilbudslinjen. Hvis du vil kontrollere hvilke transaksjonsklasser som er inkludert, velger du **Generelt**-fanen på den prosjektbaserte tilbudslinjen, og deretter kontrollerer du verdiene for **Inkluder tid**, **Inkluder utgifter**, **Inkluder materialer** og **Inkluder gebyrer**.  Hvis du vil se hvilke oppgaver som er inkludert, velger du kategorien **Belastbare oppgaver** på tilbudslinjen.

Alt etter de tilknyttede oppgavene og de inkluderte transaksjonsklassene, importeres estimatene for disse kombinasjonene av oppgave og transaksjonsklasse til tilbudslinjen.

Når du importerer estimater, blir prissettingen som standard basert på på prosjektprislistene som er knyttet til tilbudet, og faktureringstypen som er satt opp på den prosjektbaserte tilbudslinjen. Hvis en oppgave, rolle eller kategori er konfigurert på den prosjektbaserte tilbudslinjen som ikke-belastbar, vil den importerte estimatlinjen bli angitt som ikke-belastbar, og den vil ikke øke den oppgitte verdien på tilbudslinjen.

Når en tilbudslinje har linjedetaljer, summeres feltene **Tilbudsverdi** og **Beregnet mva** på tilbudslinjen, og de kan ikke redigeres.

Når det er merket av for flere sammendragsalternativer, prøver systemet å summere etter alle de valgte alternativene. Resultatet er at utdataene for importerte tilbudslinjer vil være mer enn hvis du bare valgte ett sammendragsalternativ.

Hvis for eksempel prosjektet hadde følgende estimatlinjer for utgifter.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |

Når brukeren velger å oppsummere etter transaksjonsklasse, blir følgende informasjon importert.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
|||1. oktober 2020 | 3.34 | 840 | 2800 |

Når brukeren velger å oppsummere etter transaksjonsklasse og kategori, blir følgende informasjon importert.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| | Hotell | 1. oktober 2020 | 6 | 200 | 1200 |

Når brukeren velger å oppsummere etter transaksjonsklasse, kategori og bladnodeoppgave, blir følgende informasjon importert. Legg merke til at dette resultatet er det samme som det som var i prosjektet.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
