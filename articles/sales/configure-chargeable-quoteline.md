---
title: Konfigurere de belastbare komponentene i en prosjektbasert tilbudslinje
description: Dette emnet gir informasjon om inkluderte, belastbare og ikke-belastbare komponenter på prosjektbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 36765ab3687a8aaf3ae4a631516a1d61c14e981e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642555"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurere de belastbare komponentene i en prosjektbasert tilbudslinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektbasert tilbudslinje kan ha inkluderte komponenter og belastbare komponenter.

Inkluderte komponenter er underlagt innstillingene for faktureringsmetoden, kundeoppdelingene, overskridelsesgrensene og fakturafrekvensen som er definert på den prosjektbaserte tilbudslinjen.
Et delsett av de inkluderte komponentene kan merkes som belastbart ved hjelp av **Faktureringstype**. Du kan velge ett av følgende alternativer i **Faktureringstype**-feltet i konteksten for en tilbudslinje:

   - Belastbar
   - Ikke-belastbar

Belastbare komponenter kan defineres for roller og transaksjonskategorier.

Belastbarhet som er definert på roller for en tilbudslinje for prosjekter gjelder bare transaksjonsklassen for **Tid**. Hvis en prosjekttilbudslinje har **Inkluder tid** = **Nei**, er ikke **Belastbare roller**-fanen tilgjengelig.

Belastbarhet som er definert på transaksjonskategorier for en prosjekttilbudslinje, gjelder bare for **Utgift**-transaksjonsklassen. Hvis en prosjekttilbudslinje har **Inkluder utgifter** = **Nei**, er ikke **Belastbare kategorier**-fanen tilgjengelig.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Oppdatere en rolle til å være belastbar eller ikke-belastbar
En rolle kan være belastbar eller ikke-belastbar på en prosjektbasert tilbudslinje. Faktureringstypen for en rolle kan konfigureres i **Belastbare roller**-fanen for en prosjektbasert tilbudslinje. Dette gjør du ved å oppdatere **Faktureringstype** på **Belastbare roller**-delrutenettet. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Oppdatere en transaksjonskategori til å være belastbar eller ikke-belastbar
En transaksjonskategori kan være belastbar eller ikke-belastbar på en prosjektbasert tilbudslinje. Faktureringstypen for en transaksjon kan konfigureres i **Belastbare roller**-fanen for en prosjektbasert tilbudslinje. Dette gjør du ved å oppdatere **Faktureringstype**-feltet i delrutenettet **Belastbare kategorier**. 

## <a name="resolve-chargeability"></a>Løse belastbarhet

Et estimat eller faktisk opprettet for tid, blir bare betraktet som belastbar hvis tiden tas med i tilbudslinjen, og hvis rollen er konfigurert som belastbar.
Et estimat eller faktisk opprettet for en utgift, blir bare betraktet som belastbar hvis utgiften tas med i tilbudslinjen, og hvis transaksjonskategorien er konfigurert som belastbar på tilbudslinjen. Tabellen nedenfor viser hvordan belastbarhet blir standardverdi på hver faktisk. Standardverdiene er basert på de inkluderte komponentene og faktureringstypen som er angitt i tilbudslinjen.

| Inkluderer tid | Inkluderer utgift | Rolle | Fane | Oppgave |
| --- | --- | --- | --- | --- |
| Ja | Ja | Belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Ikke-belastbar | Belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| Ja | Ja | Ikke-belastbar | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| No | Ja | Kan ikke angis | Belastbar | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Belastbar |
| No | Ja | Kan ikke angis | Ikke-belastbar | Fakturering på en faktisk tidsverdi: Ikke tilgjengelig </br>Faktureringstype for en faktisk utgiftsverdi: Ikke-belastbar |
| Ja | No | Belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Belastbar </br>Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |
| Ja | No | Ikke-belastbar | Kan ikke angis | Fakturering på en faktisk tidsverdi: Ikke-belastbar </br> Faktureringstype for en faktisk utgiftsverdi: Ikke tilgjengelig |
