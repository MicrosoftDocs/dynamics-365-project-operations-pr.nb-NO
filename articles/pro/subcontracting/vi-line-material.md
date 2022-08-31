---
title: Leverandørfakturalinjer for produkter
description: Denne artikkelen forklarer hvordan du registrerer leverandørfakturalinjer for produkter og bruker de forskjellige feltene til å registrere produktkjøp fra leverandører.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261571"
---
# <a name="vendor-invoice-lines-for-products"></a>Leverandørfakturalinjer for produkter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan ha leverandørfakturalinjer for produkter (også referert til som materiell). Prosjektledere kan bruke leverandørfakturalinjer for produkter til å registrere kostnadene for produkter som ble kjøpt inn på prosjekter.

Det kan hende at leverandørfakturalinjer for produkter refererer til en underleverandørlinje for materialer. Hvis en leverandørfakturalinje for produkter refererer til en underleverandør, kan prosjektledere samsvare og kontrollere produktene som faktureres av leverandørfakturalinjen mot bruken av innkjøpte produkter som er registrert av underleverandører og godkjent av prosjektledere.

Tabellen nedenfor inneholder informasjon om feltene på leverandørfakturalinjer for produkter.

| Felt | Bekrivelse | Funksjonsinnvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen, for å hjelpe med identifisering. | Dette navnet vises som den første kolonnen i alle oppslag som er basert på leverandørfakturalinjer. |
| Bekrivelse | En kort beskrivelse av produktene som faktureres av leverandøren på leverandørfakturalinjen. | None |
| Underkontrakt | Underkontrakten som produktene opprinnelig ble bestilt på. | Når en underkontrakt er valgt for leverandørfakturaen, arver alle linjene på leverandørfakturaen dette valget. En leverandørfaktura kan ikke ha leverandørfakturalinjer som refererer til ulike underkontrakter. |
| Underkontraktlinje | Underkontraktlinjen som produktene ble bestilt på. Listen over underkontraktslinjer som kan velges, er begrenset til linjene på den valgte underkontrakten. | Når en underkontraktlinje er valgt på en leverandørfakturalinje for produkter, angis standardverdier for feltene **Prosjekt**, **Oppgave** og **Produkt** fra de tilsvarende feltene på underkontraktlinjen. Hvis den valgte underkontraktlinjen har verdier i feltene **Prosjekt**, **Oppgave** og **Produkt**, kan ikke verdiene i de tilsvarende feltene på leverandørfakturalinjen avvike fra disse verdiene. |
| Transaksjonsdato | Datoen da faktiske kostnader for leverandørfakturalinjen registreres på prosjektet. | None|
| Transaksjonsklasse | Når produkter faktureres, må dette feltet settes til **Materiale**. | Verdien **Materiale** angir at leverandørfakturalinjen brukes til å registrere fakturabeløpet for materialer som ble kjøpt. |
| Project | Navnet på prosjektet som produktene som blir fakturert, ble brukt på. | Dette feltet er obligatorisk og kan ikke være tomt. |
| Oppgave | Navnet på prosjektoppgaven som produktene som blir fakturert, ble brukt på. Dette feltet er bare tilgjengelig hvis et prosjekt er valgt. Valg av en prosjektoppgave er valgfritt. | Hvis dette feltet er tomt, kan prosjektlederen samsvare med leverandørfakturalinjen til det innkjøpte produktet som brukes for en hvilken som helst oppgave i prosjektet. Hvis fakturalinjen for leverandørfaktura ikke refererer til en underordnet linje, og dette feltet står tomt, blir ikke den faktiske kostnaden som opprettes av leverandørfakturalinjen, koblet til noen faktiske verdier for ikke-fakturert salg. Hvis oppgavebasert fakturering er konfigurert i dette tilfellet, vil ikke kostnadene kunne faktureres til sluttkunden. |
| Velg produkt | Velg om produktet som faktureres, er et eksisterende produkt fra katalogen eller et produkt som ikke er i produktkatalogen. | Standardverdien angis fra underkontraktlinjen når en underkontraktlinje er valgt. |
| Produkt | Velg produktet fra katalogen. Hvis produktet ikke er i produktkatalogen, skriver du inn produktnavnet. | Dette feltet brukes til å angi standard innkjøpspriser for eksisterende produkter. |
| Antall | Angi antallet av materialet som blir fakturert av leverandøren på denne fakturalinjen. | None |
| Enhetsgruppe | Velg enhetsgruppen for enheten som antallet som faktureres uttrykkes i. | None |
| Enhet | Standardverdien er basisenheten for enhetsgruppen som er valgt. Du kan endre denne verdien for å betale i en hvilken som helst enhet i den valgte enhetsgruppen. | Kombinasjonen av verdiene for **Produkt** og **Enhet** brukes som standard eller beregnet verdi for **Enhetspris**-feltet på leverandørfakturalinjen. |
| Enhetspris | Standard enhetspris bruker kombinasjonen av verdiene for **Produkt** og **Enhet** fra prosjektprislisten som gjelder for transaksjonsdatoen på leverandørfakturalinjen. | None |
| Delsum | Dette skrivebeskyttede feltet beregnes som *Antall* &times; *Enhetspris* hvis verdier er angitt både i **Antall**-feltet og **Enhetspris**-feltet. Hvis ett av eller begge disse feltene er tomme, kan du angi en verdi i dette feltet. | None |
| Salgsavgift | Angi mva-beløpet. | None |
| Totalbeløp | Det totale beløpet for leverandørfakturalinjen, inkludert avgifter. Dette feltet beregnes som *Delsum* + *Merverdiavgift*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
