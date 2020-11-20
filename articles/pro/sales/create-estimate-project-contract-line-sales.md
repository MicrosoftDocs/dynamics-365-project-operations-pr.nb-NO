---
title: Estimere en prosjektbasert kontraktlinje – Lite
description: Dette emnet inneholder informasjon om estimering av en prosjektbasert kontraktlinje.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2d0d8309fcb4300e33ed2f5933259f99ad7e0d6a
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180429"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimere en prosjektbasert kontraktlinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations inneholder en prosjektbasert kontraktlinje detaljer som hjelper deg med å estimere kostnaden og potensiell omsetning på arbeidet som er involvert i å levere kontraktlinjen.

For å beregne en prosjektbasert kontraktlinje går du til kategorien **Kontraktlinjedetalj** på den prosjektbaserte **Kontraktlinje**.  Det er to måter å opprette et estimat på en prosjektbasert kontraktlinje på:

   - Opprett et estimat direkte på kontraktlinjen ved å legge til kontraktlinjedetaljer manuelt.
   - Opprett et prosjekt og en prosjektplan, og knytt deretter prosjektet og aktivitetene til kontraktlinjen i prosjektet. Dette gjør at du kan importere prosjektplananslaget til kontraktlinjen basert på komponentene som er inkludert på kontraktlinjen.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Opprette et estimat direkte på en prosjektbasert kontraktlinje

1. Gå til kontraktlinjen, og velg kategorien **Kontraktlinjedetaljer**. Linjene du oppretter i denne kategorien, oppsummeres og vises som **Kontraktverdi** for denne **Kontraktlinjen**. 
2. I underrutenettet **Kontraktlinjedetaljer** velger du **+ Ny kontraktlinjedetalj**. Det åpnes en glidebryter for hurtigopprettelse. Følgende felt er tilgjengelige i skjemaet **Kontraktlinjedetaljer**:

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Beskrivelse** | **Hurtigoppretting** | En beskrivelse av det spesifikke estimatet. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Transaksjonsklasse** | **Hurtigoppretting** | Denne rullegardinlisten er en liste over transaksjonsklasser som er inkludert i kategorien **Generelt** på den prosjektbaserte kontraktlinjen. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Rolle** | **Hurtigoppretting** | Rollen til personen som utfører dette arbeidet eller oppretter utgiften. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Kategori** | **Hurtigoppretting** | Kategorien for arbeidet eller utgiften. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Startdato** | **Hurtigoppretting** | Arbeidets startdato. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Sluttdato** | **Hurtigoppretting** | Arbeidets sluttdato. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Ressursenhet** | **Hurtigoppretting** | Ressursenheten som oppretter denne kostnaden og angir ressursen som skal arbeide med den. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. Dette feltet brukes også ved henting av kostpris. |
| **Tidsplan for enhet** | **Hurtigoppretting** | Enhetsgruppen for arbeidet eller utgiften. Enhetene tilhører en enhetsplan eller en gruppe enheter. Eksempelvis er *Mil* og *Kilometer (KMS)* enheter som tilhører en gruppe enheter som beskriver avstand. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Enhet** | **Hurtigoppretting** | Enheten for arbeid eller utgift. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Antall** | **Hurtigoppretting** | Mengden for arbeid eller utgift. | Dette feltet brukes som standard for den relaterte kontraktlinjedetaljen for kostnader som opprettes automatisk. |
| **Enhetspris** | **Hurtigoppretting** | Fakturasats for rollen som utfører arbeidet, eller salgsprisen for utgiftskategorien. Dette feltet er som standard **Tid** basert på kombinasjonen av rolle og ressursenhet på prosjektprislisten som gjelder for startdatoen. For utgifter er dette feltets standard fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er **pris per enhet**, finnes det ingen standard, og dette feltet blir stående tomt. | Kostnadssatsen for rollen som utfører arbeidet, eller kostnad per enhet for utgiftskategorien. Dette feltet er som standard angitt til **Tid basert på rolle** og ressursenhetskombinasjonen på rolleprislinjen for kostprislisten som er knyttet til kontraktsenheten som er gjeldende for startdatoen. For utgifter er dette feltets standard basert på kategoriprislinjen for kostprislisten som er knyttet til kontraktenheten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, finnes det ingen standard, og dette feltet blir stående tomt. |
| **Beregnet mva** | **Hurtigoppretting** | Den beregnede avgiften for dette arbeidet eller denne utgiften som inndata fra brukeren. | Den beregnede avgiften for dette arbeidet eller denne utgiften som inndata fra brukeren. |
| **Beløp** | **Hurtigoppretting** | Verdien i dette feltet kan legges til av brukeren hvis feltene **Antall** og **Pris** står tomme. Hvis **Antall** og **Pris** er utfylt, er feltet **Mengde** skrivebeskyttet, og det beregnes som **(Antall \* Enhetspris) + avgift**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Oppdatere priser på kontraktlinjedetaljer

Hvis du endrer priser på prosjektprislisten som er knyttet til kontrakten eller kostnadsprislisten for kontraktsenheten, kan du oppdatere prisene i de enkelte kontraktlinjedetaljene for å gjenspeile endringen. På siden **Kontrakt** velger du **Omberegn**. En advarsel vises for å informere deg om at prisene for alle kontraktlinjene på denne kontrakten blir tilbakestilt. Velg **Ja** å oppdatere priser for både salgs- og kostnadskontraktlinjedetaljer.

## <a name="access-contract-line-details-for-cost"></a>Få tilgang til kontraktlinjedetaljer for kostnad

I kategorien **Kontraktlinjedetaljer** velger du en rad i rutenettet for å vise handlinger på verktøylinjen i delrutenettet. Den første handlingen på verktøylinjen for underrutenett er **Åpne kostnadsdetaljer**. Hvis du vil vise den beslektede kostnadssatsen og beløpet for denne kontraktlinjedetaljen, velger du **Åpne kostnadsdetaljer**. 

> [!NOTE]
> Hvis du endrer verdiene for ressursstyringsfirma, ressursstyringsenhet, mengde, datoer, rolle eller kategori på kontraktlinjedetaljene for **Kostnad**, endres også de tilsvarende verdiene på kontraktlinjedetaljen for **Salg**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktlinjedetaljer for kostnad og salg

Kontraktlinjedetaljene for **Salg** angir standardvalutaen fra prosjektprislisten som er gyldig for startdatoen for kontraktlinjedetaljene.

Kontraktlinjedetaljene for **Kostnad** angir standardvalutaen fra prislisten for kontraktenheten for kontrakten som er gyldig for startdatoen for kontraktlinjedetaljen for **Kostnad**.

Beregning av fortjeneste konverterer beløpene for kontraktlinjedetaljer for **Kostnad** og **Salg** til standardvalutaen for miljøet for å rapportere de samlede faktiske og beregnede marginene på kontrakten.

> [!NOTE]
> Det kan oppstå valutaavrundingsfeil og endrede marginer på grunn av manglende datoeffektivitet for vekslingskurs. Bruk bare disse beregningene på prosjektkontrakter som har estimater, og ikke for faktisk lovpålagt eller annen rapportering som krever høyere nøyaktighet for avrunding og bevissthet om datoeffektivitet for valutakurser.
