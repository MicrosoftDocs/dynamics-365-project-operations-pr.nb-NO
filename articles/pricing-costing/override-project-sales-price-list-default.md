---
title: Overstyre salgsprislister for prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte prislister for salg.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275550"
---
# <a name="override-project-sales-price-lists"></a>Overstyre salgsprislister for prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

## <a name="customer-specific-project-price-lists"></a>Kundespesifikke prosjektprislister

Kundespesifikke prisavtaler kan konfigureres som prosjektprislister på en forretningsforbindelsesoppføring i Dynamics 365 Project Operations.

Hvis du vil definere en kundespesifikk prosjektprisliste, navigerer du til forretningsforbindelsesoppføringen i **Salg**-området.

1. Åpne listesiden **Forretningsforbindelser**.
2. Finn og dobbeltklikk en kundeoppføring for å åpne detaljsiden **Forretningsforbindelse**.
3. På **Prosjektprislister**-fanen velger du **+ Ny prosjektprisliste**.
4. På siden **Ny prosjektprisliste** velger du en prisliste fra rullegardinlisten. Bare prislister som har konteksten satt til **Salg**, og der valutaen samsvarer med valutaen for forretningsforbindelsen, er inkludert.
5. Angi et navn på tilknytningen, og velg **Lagre**. En kundespesifikk prosjektprisliste opprettes. Denne prislisten blir brukt til å angi standard prosjektpriser i prosjekttilbud eller kontrakter som er opprettet for denne kunden, der datoen for opprettelsen av tilbud eller prosjektkontrakt faller innenfor datogyldigheten for prislisten.

## <a name="custom-pricing-on-project-quotes"></a>Egendefinerte priser på prosjekttilbud

I prosjekttilbud kan du ha prosjektpriser som starter med en standard prisliste som angis som standard fra kunden eller fra prosjektparameterne.

Når du trenger egendefinerte priser for prosjektrelatert arbeid på et bestemt tilbud, kan du få dette fra den tilknyttede enheten for prosjektprislister.

Fullfør fremgangsmåten nedenfor for å definere tilbudsspesifikke prosjektpriser.

1. Åpne prosjekttilbudet og velg kategorien **Prosjektprislister**.
2. I delrutenettet velger du **Opprett egendefinert prising**.

Alle prosjektprislistene som er knyttet til tilbudet, kopieres til nye prislister. Navnene på de nye prislistene gjenspeiler navnet på tilbudet med et dato- og tidsstempel for når disse prislistene ble opprettet.

Du kan bruke hver av disse prislistene til å gjøre oppdateringer for arbeids- (rollepris) og utgiftspriser (kategoripris). Disse prisene gjelder bare for dette prosjekttilbudet.

## <a name="price-lists-on-a-project-contract"></a>Prosjektlister på en prosjektkontrakt

I en prosjektkontrakt blir alltid prosjektprissetting som standard en egendefinert prisliste med navnet på kontrakten og det opprettede dato/klokkeslett-stempelet lagt til i navnet. Dette gjelder enten kontrakten ble opprettet da tilbudet ble vunnet, eller hvis kontrakten ble opprettet fra grunnen av. Du kan om nødvendig fjerne denne tilordningen til den egendefinerte prislisten og knytte en standard prisliste til prosjektkontrakten i stedet.

Når du knytter en standard prisliste til prosjektprislistene i tilbud eller kontrakt, vil eventuelle endringer som gjøres i prisene i prislisten, ha innvirkning på alle tilbud og kontrakter som bruker prislisten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]