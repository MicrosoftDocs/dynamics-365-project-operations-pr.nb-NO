---
title: Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje – Lite
description: Dette emnet gir informasjon om hvordan du legger til belastbare komponenter i kontraktlinjer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513891"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En prosjektbasert kontraktlinje har *inkluderte* komponenter og *belastbare* komponenter.

Inkluderte komponenter er komponenter som er underlagt følgende:

  - Faktureringsmetode og kundedelinger
  - Må ikke overskrides-grenser 
  - Innstillinger for fakturafrekvens som er definert på den prosjektbaserte kontraktlinjen

Et delsett av de inkluderte komponentene kan merkes som belastbarte ved hjelp av feltet **Faktureringstype**. Feltet **Faktureringstype** er et alternativsett som tillater følgende verdier i konteksten for en kontraktlinje:

  - Belastbar
  - Ikke-belastbar

Belastbare komponenter kan defineres for oppgaver, roller og transaksjonskategorier.

Belastbar er definert i oppgaver for en prosjektkontraktlinje og gjelder for alle transaksjonsklasser som finnes på linjen. Hvis **Inkluder oppgaver**-feltet på en kontraktlinje er tomt eller satt til ***Hele prosjektet***, er ikke **Belastbare oppgaver**-fanen tilgjengelig.

Belastbarhet definert for roller for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Tid**. Hvis feltet **Inkluder td** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare roller**-fanen tilgjengelig.

Belastbarhet definert for transaksjonskategorier for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Utgift**. Hvis feltet **Inkluder utgifter** på en kontraktlinje er satt til **Nei**, er ikke **Belastbare kategorier**-fanen tilgjengelig.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Oppdatere en prosjektoppgave som belastbar eller ikke-belastbar

En prosjektoppgave kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje, noe som gjør følgende oppsett mulig:

Hvis en prosjektbasert kontraktlinje inkluderer **Tid** og en bestemt oppgave, er **T1** knyttet til den som belastbar. Hvis det er en ny kontraktlinje som inkluderer **Utgift**, kan du knytte T1-oppgaven på kontraktlinjen som ikke-belastbar. Resultatet er at all tid som registreres på oppgaven, er belastbar, og at alle utgifter er ikke-belastbare.

Du kan konfigurere faktureringstypen for en oppgave i kategorien **Belastbare oppgaver** på kontraktlinjen ved å oppdatere **Fakturatype**-feltet i delrutenettet for kontraktlinjeoppgaver. Du kan også oppdatere **Faktureringstype**-feltet i delrutenettet for faktureringsoppsettet for oppgaven for prosjektet som viser kontraktlinjene som er knyttet til en oppgave.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Oppdatere en rolle som belastbar eller ikke-belastbar

En rolle kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.

Du kan konfigurere fakturerings typen for en rolle på **Belastbare roller**-fanen på en kontraktlinje. Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare roller**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori som belastbar eller ikke-belastbar

En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt kontraktlinje.

Du kan konfigurere faktureringstypen for en transaksjon på **Belastbare kategorier**-fanen på en prosjektbasert kontraktlinje. Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare kategorier**.

### <a name="resolve-chargeability"></a>Løse belastbarhet

Et estimat eller en faktisk verdi som er opprettet for tid, blir bare betraktet som belastbar hvis **Tid** er inkludert på kontraktlinjen, og hvis **Oppgave** og **Rolle** er konfigurert som belastbar på kontraktlinjen.

Et estimat eller en faktisk verdi som er opprettet for utgift, blir bare betraktet som belastbar hvis **Utgift** er inkludert på kontraktlinjen, og hvis kategoriene **Oppgave** og **Transaksjon** er konfigurert som belastbar på kontraktlinjen.


| Inkluderer tid | Inkluderer utgift | Inkluderer oppgaver | Rolle           | Fane       | Oppgave                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Ja           | Ja              | Hele prosjektet | Belastbar     | Belastbar     | Fakturering på en faktisk tidsverdi: **Belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Belastbar**           |
| Ja           | Ja              | Valgte oppgaver | Belastbar     | Belastbar     | Fakturering på en faktisk tidsverdi: **Belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Belastbar**           |
| Ja           | Ja              | Valgte oppgaver | Ikke-belastbar | Belastbar     | Fakturering på en faktisk tidsverdi: **Ikke-belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Belastbar**       |
| Ja           | Ja              | Valgte oppgaver | Belastbar     | Belastbar     | Fakturering på en faktisk tidsverdi: **Ikke-belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Ikke-belastbar** |
| Ja           | Ja              | Valgte oppgaver | Ikke-belastbar | Belastbar     | Fakturering på en faktisk tidsverdi: **Ikke-belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Ikke-belastbar** |
| Ja           | Ja              | Valgte oppgaver | Ikke-belastbar | Ikke-belastbar | Fakturering på en faktisk tidsverdi: **Ikke-belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Ikke-belastbar** |
| No            | Ja              | Hele prosjektet | Kan ikke angis   | Belastbar     | Fakturering på en faktisk tidsverdi: **Ikke tilgjengelig**</br>Faktureringstype for en faktisk utgiftsverdi: **Belastbar**          |
| No            | Ja              | Hele prosjektet | Kan ikke angis   | Ikke-belastbar | Fakturering på en faktisk tidsverdi: **Ikke tilgjengelig**</br> Faktureringstype for en faktisk utgiftsverdi: **Ikke-belastbar**     |
| Ja           | No               | Hele prosjektet | Belastbar     | Kan ikke angis   | Fakturering på en faktisk tidsverdi: **Belastbar** </br> Faktureringstype for en faktisk utgiftsverdi: **Ikke tilgjengelig**        |
| Ja           | No               | Hele prosjektet | Ikke-belastbar | Kan ikke angis   | Fakturering på en faktisk tidsverdi: **Ikke-belastbar** </br>Faktureringstype for en faktisk utgiftsverdi: **Ikke tilgjengelig**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]