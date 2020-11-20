---
title: Importer estimater for et prosjekt til en prosjektbasert tilbudslinje
description: Dette emnet gir informasjon om hvordan du importerer estimater fra et prosjekt til en tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fda8fee6dcf55126077fb6b8c502ee9dada9b44c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125595"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Importer estimater for et prosjekt til en prosjektbasert tilbudslinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Hvis det opprettes et prosjekt i løpet av trinnet før salg, kan du velge å importere det økonomiske estimatet fra prosjektet til den prosjektbaserte tilbudslinjen.

1. Pass på at den prosjektbaserte tilbudslinjen har prosjektinformasjonen i **Prosjekt**-feltet.
2. I kategorien **Tilbudslinjedetaljer** velger du **Importer fra prosjektberegningen**.
3. Velg ett av følgende alternativer for oppsumering i dialogboksen som åpnes:

  - **Transaksjonsklasse**
  - **Kategori**
  - **Rolle** 
  - **Prosjektoppgave**

Avhengig av hva du velger, kopieres estimatet fra prosjektet for alle transaksjonsklasser som er inkludert i tilbudslinjen. Hvis du vil kontrollere hvilke transaksjonsklasser som er inkludert, velger du kategorien **Generelt** på den prosjektbaserte tilbudslinjen, og deretter kontrollerer du verdiene for **Inkluder tid**, **Inkluder utgifter** og **Inkluder gebyrer**.

Når du importerer estimater, blir prissettingen som standard basert på på prosjektprislistene som er knyttet til tilbudet, og faktureringstypen som er satt opp på den prosjektbaserte tilbudslinjen. Hvis en rolle eller kategori er konfigurert på den prosjektbaserte tilbudslinjen som ikke-belastbar, vil den importerte estimatlinjen bli angitt som ikke-belastbar, og den vil ikke øke den oppgitte verdien på tilbudslinjen.

Når en tilbudslinje har linjedetaljer, summeres feltene **Tilbudsverdi** og **Beregnet mva** på tilbudslinjen, og de kan ikke redigeres.

Når det er merket av for flere sammendragsalternativer, prøver systemet å summere etter alle de valgte alternativene. Resultatet er at utdataene for importerte tilbudslinjer vil være mer enn hvis du bare valgte ett sammendragsalternativ.

Hvis for eksempel prosjektet har følgende estimatlinjer for utgifter.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| Oppgave A | Flybilletter | 1. oktober 2020 | 4 | 400 | 1600 |
| Oppgave B | Hotell | 1. oktober 2020 | 4 | 200 | 800 |
| Oppgave C | Hotell | 1. november 2020 | 2 | 200 | 400 |

Når brukeren velger å oppsummere etter transaksjonsklasse, blir følgende informasjon importert.

| Oppgave | Fane | Dato | Antall | Enhetspris | Mengde |
| --- | --- | --- | --- | --- | --- |
| | | 1. oktober 2020 | 3.34 | 840 | 2800 |

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
