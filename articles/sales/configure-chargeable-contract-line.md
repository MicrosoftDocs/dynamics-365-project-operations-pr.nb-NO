---
title: Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje
description: Dette emnet gir informasjon om inkluderte, belastbare og ikke-belastbare komponenter på kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081557"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurere belastbare komponenter for en prosjektbasert kontraktlinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektbasert kontraktlinje har konseptet inkluderte, belastbare og ikke-belastbare komponenter.

Inkluderte komponenter er underlagt faktureringsmetoden, kundedelinger, grenser som ikke må overskrides, og innstillinger for faktureringshyppighet som er definert på den prosjektbaserte kontraktlinjen.

Et delsett av de inkluderte komponentene kan merkes som belastbarte ved å oppdatere feltet **Faktureringstype**.

Belastbare komponenter kan defineres for roller og transaksjonskategorier.

For en prosjektkontraktlinje gjelder belastbarhet definert for en rolle bare for transaksjonsklassen **Tid**. Hvis **Inkluder td** er satt til **Nei** på en prosjektkontraktlinje, er ikke **Belastbare roller** -fanen tilgjengelig.

Belastbarhet definert for transaksjonskategorier for en prosjektkontraktlinje gjelder bare transaksjonsklassen **Utgift**. Hvis **Inkluder utgifter** er satt til **Nei** på en prosjektkontraktlinje, er ikke **Belastbare kategorier** -fanen tilgjengelig.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Oppdatere en rolle til å være belastbar eller ikke-belastbar

En rolle kan være belastbar eller ikke-belastbar på en bestemt prosjektbasert kontraktlinje.

På **Belastbare roller** -fanen på en prosektbasert kontraktlinje, i delrutenettet **Belastbare kategorier** , i feltet **Faktureringstype** , oppdaterer du faktureringstypen for en rolle.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar

En transaksjonskategori kan være belastbar eller ikke-belastbar på en bestemt prosjektbasert kontraktlinje.

På **Belastbare kategorier** -fanen på en prosjektbasert kontraktlinje, i delrutenettet **Belastbare kategorier** , i feltet **Faktureringstype** , oppdaterer du faktureringstypen for en transaksjon.

### <a name="resolve-chargeability"></a>Løse belastbarhet

Et estimat eller en faktisk verdi som er opprettet for tid, blir bare betraktet som belastbar hvis tid er inkludert på kontraktlinjen, og hvis rollen er konfigurert som belastbar på kontraktlinjen.

Et estimat eller en faktisk verdi som er opprettet for utgift, blir bare betraktet som belastbar hvis utgiften er inkludert på kontraktlinjen, og hvis transaksjonskategorien er konfigurert som belastbar på kontraktlinjen.

| Inkluderer tid | Inkluderer utgift | Rolle | Fane | Oppgave |
| --- | --- | --- | --- | --- |
| Ja | Ja | Belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Ikke-belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Ikke-belastbar | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| No | Ja | Kan ikke angis | Belastbar | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| No | Ja | Kan ikke angis | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| Ja | No | Belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |
| Ja | No | Ikke-belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br> Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |
