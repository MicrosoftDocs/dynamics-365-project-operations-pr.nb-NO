---
title: Estimere en prosjektbasert tilbudslinje
description: Dette emnet gir informasjon om hvordan du oppretter et estimat på en prosjektbasert tilbudslinje.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273564"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimere en prosjektbasert tilbudslinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

En prosjektbasert tilbudslinje inneholder detaljer som bidrar til beregning av kostnader og potensiell omsetning på arbeidet som er involvert i å levere tilbudslinjen.

Hvis du vil beregne en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj** på den prosjektbasert tilbudslinjen. Det er to måter å opprette et estimat på en prosjektbasert tilbudslinje på:

- Opprett estimatet manuelt direkte på tilbudslinjen ved hjelp av tilbudslinjedetaljer 
- Opprett et prosjekt og en prosjektplan, og knytt deretter prosjektet og oppgavene i prosjektet til tilbudslinjen. Fremgangsmåten for import av beregningene for prosjektplanen til tilbudslinjen basert på informasjonen du har angitt, blir aktivert.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opprette estimater direkte på en prosjektbasert tilbudslinje

Hvis du vil opprette et estimat på en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj**. Linjeelementet du oppretter i denne kategorien, oppsummerer den tilbudte verdien for denne tilbudslinjen. 

Hvis du vil opprette tilbudslinjedetaljer, velger du **+ Ny tilbudslinjedetalj** i delrutenettet **Tilbudslinjedetaljer**. En glidebryter for hurtigoppretting åpner. følgende felt i skjemaet **Tilbudslinje**:

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtigoppretting | En beskrivelse av det spesifikke estimatet. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Transaksjonsklasse | Hurtigoppretting | Denne rullegardinlisten inneholder transaksjonsklassene som er inkludert i kategorien **Generelt** for den prosjektbaserte tilbudslinjen.  | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Rolle | Hurtigoppretting | Personen som skal utføre dette arbeidet, eller som vil forårsake denne utgiften. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Fane | Hurtigoppretting | Kategori for arbeidet eller utgiften. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Startdato | Hurtigoppretting | Arbeidets startdato. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Sluttdato | Hurtigoppretting | Sluttdato for arbeidet. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Ressursenhet | Hurtigoppretting | Ressursenheten som vil påføre denne kostnaden, og som gir ressursen mulighet til å arbeide med den. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. Dette feltet brukes også ved henting av kostpris. |
| Tidsplan for enhet | Hurtigoppretting | Enhetsgruppen for arbeidet eller utgiften. Enhetene tilhører en enhetsplan eller en gruppe enheter. Miles og kilometer er for eksempel enheter som tilhører en enhetsgruppe som beskriver distanse. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Enhet | Hurtigoppretting | Enheten for arbeidet eller utgiften. | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Antall | Hurtigoppretting | Antallet for arbeidet eller utgiften | Dette feltet er som standard den relaterte tilbudslinjendetaljen for kostnad som opprettes automatisk. |
| Enhetspris | Hurtigoppretting | Fakturasatsen for rollen som utfører arbeidet, eller salgsprisen for utgiftskategorien. Dette feltet er Tid som standard, basert på kombinasjonen av rolle og ressursenhet på prosjektprislisten som gjelder for startdatoen. For utgifter blir dette feltet som standard fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, finnes det ingen standard, og dette feltet blir stående tomt. | Kostnadssatsen for rollen som utfører arbeidet, eller kostnad per enhet for utgiftskategorien. Dette feltet er Tid som standard, basert på kombinasjonen av rolle og ressursenhet for prisen på kontraktenheten i tilbudsprislisten som gjelder for startdatoen. For utgifter blir dette feltet som standard fra prisoppsettet for transaksjonskategorien i kostprislisten til kontraktenheten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, finnes det ingen standard, og dette feltet blir stående tomt. |
| Beregnet mva | Hurtigoppretting | Du kan angi beregnet avgift eller utgift for dette arbeidet manuelt. | Dette feltet har ingen nedstrøms påvirkning. |
| Mengde | Hurtigoppretting | Du kan angi informasjon manuelt i dette feltet hvis feltene **Antall** og **Pris** står tomme. Hvis disse feltene ikke er tomme, blir dette feltet skrivebeskyttet og beregnet som (antall \* enhetspris) + avgift. | Dette feltet har ingen nedstrøms påvirkning. |

## <a name="update-prices-on-quote-line-details"></a>Oppdatere priser på tilbudslinjedetaljer

Hvis du har endret priser på prosjektprislisten som er knyttet til tilbudet, eller på kostnadsprislisten for kontraktenheten, kan du velge **Beregn på nytt** på **Tilbud**-siden for å oppdatere prisene i de enkelte tilbudslinjedetaljene for å gjenspeile denne endringen. Når du velger **Beregn på nytt**, vises det en advarsel som informerer deg om at priser på tilbudslinjedetaljer for alle tilbudslinjer i tilbudet blir tilbakestilt. Velg **Ja** for å oppdatere priser for både salgs- og kostnadstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få tilgang til tilbudslinjedetaljer for kostnad

I kategorien **Tilbudslinjedetaljer** velger du en rad i rutenettet for å aktivere noen handlinger på verktøylinjen i delrutenettet. Den første handlingen på verktøylinjen i rutenettet når en tilbudslinjedetalj er valgt, er **Åpne kostnadsdetaljer**. Velg **Åpne kostnadsdetaljer** for å vise den beslektede kostnadssatsen og beløpet for denne tilbuds linjen.

> [!NOTE]
> Endring av ressursenhetenhet, antall, dato, rolle eller kategoriverdier på tilbudslinjedetaljene for kostnad, endrer de tilsvarende verdiene i tilbudslinjedetaljene for salg.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta på tilbudslinjedetaljer for kostnad og salg

Valuta på tilbudslinjedetaljene for salg kommer som standard fra prosjektprislisten som er effektiv, for startdatoen for tilbudslinjedetaljene.

Valuta på tilbudslinjedetaljene for kostnad kommer som standard fra kontraktenheten for tilbudet som er effektiv, for startdatoen for tilbudslinjedetaljene for kostnad.

Beregning av lønnsomhet konverter beløpet på tilbudslinjendetaljene for kostnader og salg til standardvalutaen for miljøet for å rapportere den totale beregnede marginen i tilbudet.

Dette kan føre til valutaavrundingsfeil og endrede marginger på grunn av manglende valutakurser for gjeldende dato. Bruk disse beregningene bare på prosjekttilbud som estimater og ikke faktiske lovpålagte eller annen rapportering som krever høyere presisjon ved avrunding, og vær oppmerksomm på gyldig dato for valutakurser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]