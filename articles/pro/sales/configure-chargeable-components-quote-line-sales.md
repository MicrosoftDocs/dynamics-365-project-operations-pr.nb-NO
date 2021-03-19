---
title: Konfigurere de belastbare komponentene i en tilbudslinje – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer belastbare og ikke-belastbare komponenter på en prosjektbasert tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273885"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurere de belastbare komponentene i en tilbudslinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En prosjektbasert tilbudslinje har konseptet *inkluderte* komponenter og *belastbare* komponenter.

Inkluderte komponenter er underlagt følgende:

  - Faktureringsmetode og kundedelinger
  - Må ikke overskrides-grenser 
  - Innstillinger for fakturafrekvens som er definert på den prosjektbaserte tilbudslinjen

Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**. Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en tilbudslinje:

  - Belastbar
  - Ikke-belastbar

Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.

Belastbarhet er definert i oppgavene for en tilbudslinje og gjelder for alle transaksjonsklasser som finnes på denne linjen. Hvis feltet **Inkluder oppgaver** satt til **Hele prosjektet** eller er tomt, er ikke **Belastbare oppgaver**-fanen tilgjengelig.

Belastbarhet er definert for roller for en tilbudslinje og gjelder bare transaksjonsklassen **Tid**. Hvis feltet **Inkluder td** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare roller**-fanen tilgjengelig.

Belastbarhet er definert for transaksjonskategorier for en tilbudslinje og gjelder bare transaksjonsklassen **Utgift**. Hvis feltet **Inkluder utgifter** er satt til **Nei** på en prosjekttilbudslinje, er ikke **Belastbare kategorier**-fanen tilgjengelig.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Oppdatere en prosjektoppgave til å være belastbar eller ikke-belastbar

En prosjektoppgave kan være belastbar eller ikke-belastbar i konteksten til en bestemt prosjektbasert tilbudslinje, noe som gjør følgende oppsett mulig:

Hvis en prosjektbasert tilbudslinje inkluderer **Tid** og oppgaven **T1**, knyttes oppgaven til tilbudslinjen som belastbar. Hvis det er en ny tilbudslinje som inkluderer **Utgifter**, kan du knytte til **T1**-oppgaven på tilbudslinjen som ikke-belastbar. Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter som registreres på oppgaven, er ikke-belastbare.

Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på en prosjektbasert tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Tilbudslinjeoppgaver**. Du kan også oppdatere faktureringstypen for en prosjektoppgave i **Faktureringstype**-feltet i delrutenettet på faktureringsoppsettet for oppgaven for prosjektet som viser tilbudslinjene som er knyttet til en oppgave.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Oppdatere en rolle til å være belastbar eller ikke-belastbar

En rolle kan være belastbar eller ikke-belastbar i konteksten for en bestemt prosjektbasert tilbudslinje.

Du kan konfigurere faktureringstypen for en rolle i kategorien **Belastbare roller** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare roller**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar

En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt tilbudslinje.

Du kan konfigurere faktureringstypen for en transaksjon i kategorien **Belastbare kategorier** på en tilbudslinje ved å oppdatere **Fakturatype**-feltet i delrutenettet **Belastbare kategorier**.

### <a name="resolve-chargeability"></a>Løse belastbarhet
Et estimat eller en faktisk verdi som er opprettet for tid, blir bare betraktet som belastbar hvis **Tid** er inkludert på tilbudslinjen, og hvis **Oppgave** og **Rolle** er konfigurert som belastbar på tilbudslinjen.

Et estimat eller en faktisk verdi som er opprettet for utgift, blir bare betraktet som belastbar hvis **Utgift** er inkludert på tilbudslinjen, og hvis kategoriene **Oppgave** og **Transaksjonskategori** er konfigurert som belastbar på tilbudslinjen.

| Inkluderer tid | Inkluderer utgift | Inkluderte oppgaver | Rolle | Fane | Oppgave | Fakturering |
| --- | --- | --- | --- | --- | --- | --- |
| Ja | Ja | Hele prosjektet | Belastbar | Belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Bare valgte oppgaver | Belastbar | Belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Belastbar</br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Bare valgte oppgaver | Ikke-belastbar | Belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar</br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Bare valgte oppgaver | Belastbar | Belastbar | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar</br> Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| Ja | Ja | Bare valgte oppgaver | Ikke-belastbar | Belastbar | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar</br> Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| Ja | Ja | Bare valgte oppgaver | Ikke-belastbar | Ikke-belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar</br> Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| No | Ja | Hele prosjektet | Kan ikke angis | Belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| No | Ja | Hele prosjektet | Kan ikke angis | Ikke-belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| Ja | No | Hele prosjektet | Belastbar | Kan ikke angis | Kan ikke angis | Fakturering på en faktisk tidsverdi: Belastbar</br>Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |
| Ja | No | Hele prosjektet | Ikke-belastbar | Kan ikke angis | Kan ikke angis | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]