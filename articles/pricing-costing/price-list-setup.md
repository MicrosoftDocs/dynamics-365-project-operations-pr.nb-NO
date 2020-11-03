---
title: Sette opp prislister
description: Dette emnet gir information om hvordan du setter opp kost- og salgsprislister.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 578f5641659a5d05785781afe7055fe4449cf799
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088039"
---
# <a name="set-up-price-lists"></a>Sette opp prislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prislister i Dynamics 365 Project Operations representerer en katalog med satser. Satsene uttrykker kostnads-, salgs- og fakturasatser. Alt etter om prislisten uttrykker kostnadssatser eller salgs- og fakturasatser, er konteksten til prislisten **Salg** eller **Kostnad**.

Følgende utvidelser er spesifikke for Project Operations og brukes på prislister fra Dynamics 365 Sales.

- **Kontekst** : Dette feltet inneholder verdiene som støttes, **Kostnad** og **Salg**. Verdien **Kjøp** støttes ikke. Sett konteksten til **Kostnad** for å lage en kostprisliste, eller sett konteksten til **Salg** for en salgsprisliste. Kostprislister løser prisen på kostnadstypen for estimatoppføringer og faktisk verdi-oppføringer. Salgsprislister løser prisen på beregnede og faktiske oppføringer for ikke-fakturerte og fakturerte salgstyper.
- **Tidsenhet** : Dette er standard tidsenhet som prisen er definert for, i den relaterte tabellen **Rollepris** for denne prislisten.
- **Prislisteenhet** : Dette skjulte feltet finnes i Project Operations for å differensiere prislister som er tilbuds- eller kontraktspesifikke, fra dem som gjelder for standard og globalt.

## <a name="price-list-header"></a>Prislistehode

Følgende tabell inneholder feltene i kategoroien **Generelt** for en prisliste som er unike for Project Operations, eller som har betydelige endringer i virkemåten fra prislister i Sales.

| Felt | Sted | Relevans, formål og veiledning | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Navn | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Identiteten for prislisten. | Prislisten vises med denne verdien for alle listesider og alternativer i rullegardinlister.|
| Kontekst | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Dette feltet kan settes til **Kostnad** eller **Salg**. | En prisliste som er satt til **Kostnad** , brukes til å slå opp prisen på kostnadsestimater og faktiske kostnader. En prisliste som er satt til **Salg** , brukes til å slå opp prisen på salgsestimater og faktiske salgsverdier. Bare prislister som har konteksten angitt til **Salg** , kan knyttes til prosjektprislister for kunder, prosjekttilbud eller kontrakter. |
| Startdato | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Startdatoen i perioden som prislisten er gyldig i. | Sammen med **Sluttdato** -feltet brukes dette feltet til å finne ut hvilken prisliste som gjelder for et bestemt estimat eller en faktisk linje. |
| Sluttdato | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Sluttdatoen i perioden som prislisten er gyldig i. | Sammen med **Startdato** -feltet brukes dette feltet til å finne ut hvilken prisliste som gjelder for et bestemt estimat eller en faktisk linje. |
| Valuta | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Dette feltet brukes til å standardisere valutaen for hver rolle, kategori eller prislisteelement som er relatert til denne prislisten. | I **salgsprislister** kan ikke roller, kategorier eler prislisteelementlinjer opprettes i andre valutaer enn denne valutaen. I **kostprislister** kan du rolleprislinje i hvilken som helst valuta. Valutaen som er definert her, brukes som standard. Brukeroppsettet som er relatert til rollepriser, kan overstyre denne verdien for å aktivere oppsett av arbeidskostsatser for en hvilken som helst valuta. Kategorikostnadssataser og prislisteelementkostnader kan bare konfigureres i valutaen som er definert her. |
| Tidsenhet | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Dette feltet brukes til å standardisere tidsenheten for hver rollelinje som er relatert til denne prislisten. | Denne feltverdien brukes bare på det relaterte rolleprisoppsettet. I **kost-** og **salgsprislister** kan du opprette en rolleprislinje i hvilken som tidsenhet. Tidsenheten som er definert her, brukes som standard. Brukeroppsettet som er relatert til rollepriser, kan overstyre denne verdien for å aktivere oppsett av arbeidskost- og fakturasatser for en hvilken som helst tidsenhet. |
| Beskrivelse | Kategorien **Generelt** og **hurtigopprettingsskjemaer** | Dette tekstfeltet gjør det mulig å ha en flerlinjet beskrivelse av prislisten. | Dette feltet vises i de **tilknyttede** visningene i prislisten i ulike enheter som har relaterte prislister. |