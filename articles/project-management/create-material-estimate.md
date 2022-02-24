---
title: Økonomiske estimater for materialer på prosjekter
description: Dette emnet inneholder informasjon om hvordan du definerer eller beregner prosjektbasert materiell.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788881"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Økonomiske estimater for materialer på prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations gjør det mulig for prosjektledere å definere prosjektbaserte materialekostnader for hvert prosjekt eller hver oppgave. Hvert materialestimat kan knyttes til en bestemt prosjektoppgave. Utgifter kategoriseres i ulike utgiftskategorier, som defineres på organisasjonsnivå. Priser og kostnader for hver utgiftskategori defineres i prislisten. 

Fullfør fremgangsmåten nedenfor for å vise, legge til eller slette et estimat for prosjektmateriell.

1. Gå til **Prosjekter**, og velg prosjektet du vil oppdatere.
2. I kategorien **Materialestimater** viser du listen over prosjektmaterialestimater.
3. Velg **Nytt materialestimat** for å opprette et nytt materialestimat. Du kan også velge et materialestimat som skal slettes, og deretter velge **Slett materialestimat**.

Tabellen nedenfor inneholder informasjon om feltene på **materialestimatlinjen** for et prosjekt. 

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Oppgave | En liste over oppgavene i prosjektet. Dette inkluderer sammendrags- og bladnodeoppgaver. | Når du velger en oppgave for en materialestimatlinje, påvirkes den estimerte materialkostnaden og det estimert materialsalget for en oppgave. Hvis dette feltet står tomt, spores materialestimatet og oppsummeres bare på prosjektnivå. |
| Velg produkt |  Du kan angi om estimatlinjen gjelder et eksisterende produkt (i produktkatalogen) eller et produkt som ikke er i produktkatalogen. | Dette feltet avgjør om du velger et produkt fra katalogen eller et produkt som ikke er i produktkatalogen. |
| Produkt | ID-en for produktet fra produktkatalogen. Når du velger en produkt-ID, oppdateres verdien i feltet **Velg produkt** automatisk til **Eksisterende produkt**. ID-en brukes til å hente kost- og salgsprisene fra prislisten. | Dette feltet har ingen nedstrøms påvirkning. |
| Beskrivelse av produkt ikke i produktkatalog | Et tekstfelt for å skrive inn navnet på produktet. Dette feltet skal brukes når **Ikke i produktkatalog** er valgt i **Velg produkt**-feltet.| Dette feltet har ingen nedstrøms påvirkning. |
| Startdato | Den forventede datoen for bruk av materialet. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetsgruppe | Standardverdien i dette feltet kommer fra standard enhetsgruppe for katalogproduktet. Du kan oppdatere dette feltet for å velge en annen enhetsgruppe. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhet | Verdien i dette feltet kommer fra standardenheten for det valgte produktet. Du kan oppdatere dette feltet for å velge en annen enhet. | Endring av enheten fører til en annen standard enhetspris og -kostnad. |
| Antall | Det estimerte antallet av produktet som skal brukes på prosjektet. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhetskost | Enhetskostnaden for det valgte produktet og enhetskombinasjonen som angitt i den aktuelle kostnadsprislisten. | Enhetskostnaden vises alltid i kostnadsvalutaen for prosjektet. Hvis det ikke er definert noen enhetskostnad for kombinasjonen av produktet og enhetsoppsettet i prislisten, settes enhetskostnaden til 0,00 som standard. |
| Enhetspris | Prisen for det valgte produktet og enhetskombinasjonen som satt opp i den aktuelle salgsprislisten. | Enhetsprisen vises alltid i salgsvalutaen for prosjektet. Hvis det ikke er satt opp en enhetspris for kombinasjonen av produktet og enhetsoppsettet i prislisten, settes enhetsprisen til 0,00 som standard.|
| Totale kostnader | Kostnadsbeløpet som beregnes som antall \* enhetskostnad.| Kostnadsbeløpet vises alltid i kostnadsvalutaen for prosjektet. |
| Totalt salg | Salgsbeløpet som beregnes som antall \* enhetspris. | Salgsbeløpet vises alltid i salgsvalutaen for prosjektet. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
