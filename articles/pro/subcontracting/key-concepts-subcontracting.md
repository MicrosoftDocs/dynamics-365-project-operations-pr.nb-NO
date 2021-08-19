---
title: Nøkkelkonsepter i underkontrakter
description: Dette emnet forklarer noen viktige konsepter som gjelder underkontrakter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 01d2e57b99015c346be15e3504440c14cb9a54e24215c0b1c052c5112f4b940a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994288"
---
# <a name="key-concepts-in-subcontracting"></a>Nøkkelkonsepter i underkontrakter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Produktemnet forklarer noen viktige konsepter du bør være klar over før du begynner å bruke funksjonen for underkontrakter i Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Kontraktsenhet på underkontrakten

Kontraktsenheten representerer divisjonen eller praksisen som eier leveringen av det endelige prosjektet. Kontraktsenheten er også divisjonen som angis i kontraktrelasjonen med leverandøren.

## <a name="purchase-currency"></a>Kjøpsvaluta

I Project Operations er kjøpsvalutaen valutaen som underkontrakten opprettes i. Det er også valutaen som underleverandørkostnaden for et prosjekt registreres i. Kjøpsvalutaen kan være forskjellig fra prosjektvalutaen, og prosjektvalutaen kan i sin tur være forskjellig fra salgsvalutaen.

## <a name="billing-methods-on-subcontract-lines"></a>Faktureringsmetoder på underkontraktslinjer

For prosjekter finnes det vanligvis kontraktmodeller med fast pris og forbruk. Project Operations støtter disse faktureringsmetodene i salgs- og kjøpskontekst. For et kjøp fungerer faktureringsmetoder på følgende måte:

- **Tid og materiell** – Når en underleverandørlinje bruker faktureringsmetodene **Tid og Materiale**, registreres tidskostnadene for prosjektet som underleverandører, som arbeider med det prosjektet og registrerer klokkeslett. Disse kostnadstransaksjonene fra underleverandører samsvares deretter med linjeelementene i leverandørfakturaer. I denne modellen kan prosjektledere som bruker Project Operations, samsvare og kontrollere leverandørfakturalinjer med underleverandørtid som registreres og godkjennes. Når verifiseringen er fullført, blir faktiske kostnader som er registrert etter godkjenning, tilbakeført, og nye faktiske kostnader som er basert på leverandørfakturaen, opprettes på prosjektet.
- **Fast pris** – I denne kontraktmodellen med fast avgift er leverandørfakturaer basert på faste milepæler. Underleverandørressurser kan imidlertid også rapportere klokkeslett. Tiden blir så gjennomgått og godkjent av prosjektlederen. Når den er godkjent, oppretter Project Operations midlertidige faktiske kostnader for prosjektet. Når leverandøren har sendt en faktura for en milepæl, kan prosjektlederen samsvare med tidligere registrerte kostnader i forhold til milepælen. Når verifiseringen er fullført, tilbakeføres de faktiske kostnadene og de milepælbaserte kostnadene registreres.

## <a name="project-price-lists-on-subcontracts"></a>Prosjektprislister for underkontrakter

Prosjektprislister er prislister som brukes til å angi innkjøpspriser for tid, utgifter og andre prosjektrelaterte komponenter. Det kan finnes flere prislister, og hver av dem kan ha en egen underleverandør i Project Operations. Project Operations støtter ikke overlappende gyldighetsdatoer i prosjektprislister for en underkontrakt.

## <a name="transaction-classes-on-subcontracts"></a>Transaksjonsklasser på underkontrakter

Project Operations støtter fire typer transaksjonsklasser:

- Tid
- Utgift
- Materiale
- Gebyr

Innkjøpskostnader kan bare beregnes og påløpes i transaksjonsklasser for **tid**, **utgifter** og **materiell**. **Avgift** er en transaksjonsklasse som bare gjelder omsetning, og er ikke tilgjengelig i innkjøpsinnholdet.

## <a name="purchase-pricing-dimensions"></a>Kjøpsprisdimensjoner

Prissettingsdimensjoner gjør det mulig å bestemme hvilke attributter som skal brukes til innkjøpsprisoppsett og standardtransaksjoner i tide. Når det gjelder innkjøp, støtter Project Operations bare faste dimensjonssett for konfigurasjon og standardinnkjøp. Når det gjelder konfigurasjon av innkjøpspris og standardkonfigurasjon på underkontraktlinjer og underkontrakttransaksjoner, er attributtene **Rolle** og **Ressurs som kan reserveres**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
