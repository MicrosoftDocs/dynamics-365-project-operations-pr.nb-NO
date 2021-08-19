---
title: Forskudd og honorarbaserte kontrakter
description: Dette emnet gir information om hvordan honorarbaserte kontraktmodeller og forskudd i Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87e275cb72f1edc5a2a9913b4aa47d461d1f3d3d9bf177bf0ffba8b463f4ce01
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994423"
---
# <a name="advances-and-retainer-based-contracts"></a>Forskudd og honorarbaserte kontrakter


_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations støtter honorarbaserte kontrakter. En honorarbasert kontrakt er et forhandlet sett med likt fordelte betalinger som kunden faktureres for, i løpet av prosjektets varighet. Denne typen kontrakt brukes vanligvis til faktureringsmodeller for tid og materiale eller forbruksbaserte faktureringsmodeller, der det er nødvendig å gi kunden en forutsigbar faktura- og betalingsplan. Faktiske påløpte inntekter for hver periode blir avstemt mot betalingen som er mottatt fra kunden i begynnelsen av perioden. I henhold til konseptet for faktureringsmodellen for tid og materialer kan omsetningsverdiene som påløper i hver periode, variere etter de påløpte kostnadene. Hvis den påløpte omsetningen er større enn beløpet som er mottatt i begynnelsen av perioden, kan firmaet som leverer prosjektet, gjøre følgende:

- Bare fakturere kunden for det oveskytende 
- Utsette avstemmingen av omsetningen til neste faktureringsperiode, og levere én endelig faktura ved slutten av prosjektet for alle resterende ikke-avstemte inntekter

Hovedforskjellen mellom en honorarbasert kontrakt modell og en kontraktmodell med fastpris i Project Operations er at i kontraktmodellen med fastpris er ikke fakturabeløpet knyttet til eller bundet til de påløpte kostnadene. Faktureringen følger en milepælbasert tilnærming som er justert etter kostnadene som er påløpt for den perioden. I en honorarbasert kontrakt blir omsetning som kan faktureres, registrert basert på faktureringsmetoden på kontraktlinjen. Når faktureringsmetoden er tid og materiell, er den fakturerbare omsetningen knyttet til påløpte kostnader i en gitt periode, og kan variere fra periode til periode. Kunden faktureres imidlertid bare for beløpet tilsvarende det periodiske honoraret. Systemet bruker en annen faktura på slutten av perioden for å avstemme den fakturerbare omsetningen som er registrert i løpet av perioden, mot beløpet som kunden ble fakturert for ved starten av perioden.

Fordelen med denne metoden er at kundens kostnader blir forutsigbare i honorarplanen, i motsetning til i en typisk modell med tid og materiell. Organisasjonen som leverer prosjektet, har også noe plass til å dekke risikoen for å tilbakebetale kostnader som som er pådratt på grunn av eventuelle økninger i omfanget, som en fastprismodell ikke ville tillatt.

I tillegg til en periodisk honorarbasert tidsplan kan Project Operations registrere et éngangsforskudd fra en kunde og avstemme det mot de ulike prosjektkostnadskomponentene.

Honoraret i Project Operations er ikke tilgjengelig for bruk før det er fakturert til kunden. Dette angis av følgende felt i delrutenettet for forskudd og honorarer.

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| Tilgjengelig beløp | Beløpet som er tilgjengelig for bruk i honorar- eller forskuddsoppføringen. | Før forskuddet eller honoraret er fakturert, er det ikke tilgjengelig for bruk, noe som betyr at det tilgjengelige beløpet vil være null. |
| Brukt beløp | Beløpet som allerede er brukt for honoraret eller forskuddet. | Et forskudd eller honorar kan avstemmes delvis på en faktura med faktiske kostnader, der en del av det er merket som allerede brukt. Resten av forskudds- eller honorarbeløpet er tilgjengelig for avstemming på en fremtidig faktura med faktiske kostnader. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]