---
title: Leverandørfakturalinjer for utgiftskategorier
description: Denne artikkelen forklarer hvordan du registrerer leverandørfakturalinjer for utgiftskategorier.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261712"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Leverandørfakturalinjer for utgiftskategorier

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan ha leverandørfakturalinjer for utgiftskategorier. Prosjektledere kan bruke leverandørfakturalinjer for utgiftskategorier til å registrere kostnadene for tjenester som er innkjøpt, som utgiftskategorier.

Det kan hende at leverandørfakturalinjer for utgiftskategorier refererer til en underleverandørlinje for utgiftskategorier. Hvis en leverandørfakturalinje for utgiftskategorier refererer til en underleverandør, kan prosjektledere samsvare og kontrollere utgifter som faktureres av leverandørfakturalinjen, i forhold til utgifter som er registrert i disse utgiftskategoriene og godkjent av prosjektledere på prosjektet.

Tabellen nedenfor inneholder informasjon om feltene på leverandørfakturalinjer for utgiftskategorier.

| Felt | Bekrivelse | Funksjonsinnvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen, for å hjelpe med identifisering. | Dette navnet vises som den første kolonnen i alle oppslag som er basert på leverandørfakturalinjer. |
| Bekrivelse | En kort beskrivelse av servicene som faktureres av leverandøren på leverandørfakturalinjen. | None |
| Underkontrakt | Underkontrakten som tjenestene opprinnelig ble bestilt på. | Når en underkontrakt er valgt for leverandørfakturaen, arver alle linjene på leverandørfakturaen dette valget. En leverandørfaktura kan ikke ha leverandørfakturalinjer som refererer til ulike underkontrakter. |
| Underkontraktlinje | Underkontraktlinjen som tjenestene ble bestilt på. Listen over underkontraktslinjer som kan velges, er begrenset til linjene på den valgte underkontrakten. | Når en underkontraktlinje er valgt på en leverandørfakturalinje for utgiftskategorier, angis standardverdier for feltene **Prosjekt**, **Oppgave** og **Transaksjonskategori** fra de tilsvarende feltene på underkontraktlinjen. Hvis den valgte underkontraktlinjen har verdier i feltene **Prosjekt**, **Prosjektoppgave** og **Transaksjonskategori**, kan ikke verdiene i de tilsvarende feltene på leverandørfakturalinjen avvike fra disse verdiene. |
| Transaksjonsdato | Datoen da faktiske kostnader for leverandørfakturalinjen registreres på prosjektet. |None |
| Transaksjonsklasse | Velg **Utgift** for å registrere en leverandørfaktura for en utgiftskategori. | Verdien **Utgift** angir at leverandørfakturalinjen brukes til å registrere fakturabeløpet for tjenester som ble kjøpt, som utgiftskategorier. |
| Project | Navnet på prosjektet som tjenestene som blir fakturert, ble brukt på. | Dette feltet er obligatorisk og kan ikke være tomt. |
| Oppgave | Navnet på prosjektoppgaven som tjenestene som blir fakturert, ble brukt på. Dette feltet er bare tilgjengelig hvis et prosjekt er valgt. Valg av en prosjektoppgave er valgfritt. | Hvis dette feltet er tomt, kan prosjektlederen samsvare med leverandørfakturalinjen til utgifter som registreres for en hvilken som helst oppgave i prosjektet. Hvis fakturalinjen for leverandørfaktura ikke refererer til en underordnet linje, og dette feltet står tomt, blir ikke den faktiske kostnaden som opprettes av leverandørfakturalinjen, koblet til noen faktiske verdier for ikke-fakturert salg. Hvis oppgavebasert fakturering er konfigurert i dette tilfellet, kan det hende at kostnadene ikke kan faktureres til sluttkunden. |
| Transaksjonskategori | Transaksjonskategorien som faktureres. En tilsvarende utgiftskategori må opprettes for den valgte transaksjonskategorien. | Kombinasjonen av verdiene for **Transaksjonskategori** og **Enhet** brukes som standard eller beregnet verdi for **Enhetspris**-feltet på leverandørfakturalinjen. |
| Antall | Angi antallet som blir fakturert av leverandøren på fakturalinjen. |None|
| Enhetsgruppe | En standardverdi angis basert på enhetsgruppen for den valgte transaksjonskategorien. | None |
| Enhet | Standardverdien er basisenheten for enhetsgruppen som er valgt. Du kan endre denne verdien for å kjøpe en hvilken som helst enhet i enhetsgruppen. | Kombinasjonen av verdiene for **Transaksjonskategori** og **Enhet** brukes som standard eller beregnet verdi for **Enhetspris**-feltet på leverandørfakturalinjen. |
| Enhetspris | Standard enhetspris bruker kombinasjonen av verdiene for **Transaksjonskategori** og **Enhet** fra prosjektprislisten som gjelder for transaksjonsdatoen på leverandørfakturalinjen. | Hvis prisen for den aktuelle prosjektprislisten er angitt i en enhet som er forskjellig fra enheten på leverandørfakturalinjen, bruker systemet enhetskonverteringen til å beregne enhetsprisen. |
| Delsum | Dette skrivebeskyttede feltet beregnes som *Antall* &times; *Enhetspris* hvis verdier er angitt både i **Antall**-feltet og **Enhetspris**-feltet. Hvis ett av eller begge disse feltene er tomme, kan du angi en verdi i dette feltet.| None |
| Salgsavgift | Angi mva-beløpet. | None |
| Totalbeløp | Det totale beløpet for leverandørfakturalinjen, inkludert avgifter. Dette feltet beregnes som *Delsum* + *Merverdiavgift*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
