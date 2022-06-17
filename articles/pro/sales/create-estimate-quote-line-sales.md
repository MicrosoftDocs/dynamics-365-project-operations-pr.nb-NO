---
title: Estimere en prosjektbasert tilbudslinje
description: Denne artikkelen inneholder informasjon om hvordan du oppretter et estimat på en prosjektbasert tilbudslinje.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2a8aa2971431cd1f2082c8fc80db1438be185f5b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914368"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimere en prosjektbasert tilbudslinje

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En prosjektbasert tilbudslinje inneholder detaljer som bidrar til beregning av kostnader og potensiell omsetning på arbeidet som er involvert i å levere tilbudslinjen.

Hvis du vil beregne en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj** på den prosjektbasert tilbudslinjen. Det er to måter å opprette et estimat på en prosjektbasert tilbudslinje på:

- Opprett estimatet manuelt direkte på tilbudslinjen ved hjelp av tilbudslinjedetaljer. 
- Opprett et prosjekt og en prosjektplan, og knytt deretter prosjektet og oppgavene i prosjektet til tilbudslinjen. Fremgangsmåten for import av beregningene for prosjektplanen til tilbudslinjen basert på informasjonen du har angitt, blir aktivert.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opprette estimater direkte på en prosjektbasert tilbudslinje

Hvis du vil opprette et estimat på en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj**. Linjeelementet du oppretter i denne kategorien, oppsummerer den tilbudte verdien for denne tilbudslinjen. 

Hvis du vil opprette tilbudslinjedetaljer, velger du **Ny tilbudslinjedetalj** i delrutenettet **Tilbudslinjedetaljer**. En glidebryter for hurtigoppretting åpner. Tabellen nedenfor viser detaljer om feltene på siden **Tilbudslinjedetalj** og hvordan verdiene har innvirkning påfunksjonaliteten.

| **Felt** | **Sted** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtigoppretting | En beskrivelse av det spesifikke estimatet. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Transaksjonsklasse | Hurtigoppretting | Denne rullegardinlisten inneholder transaksjonsklassene som er inkludert i kategorien **Generelt** for den prosjektbaserte tilbudslinjen.  | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Velg produkt | Hurtigoppretting | Gjelder når transaksjonsklassen er **Materiale**. Du kan velge å angi at denne estimatlinjen gjelder et **eksisterende** produkt (i produktkatalogen) eller et produkt som **ikke er** i produktkatalogen. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Produkt | Hurtigoppretting | ID-en for produktet fra produktkatalogen. Dette feltet aktiveres bare hvis du velger **Eksisterende** i **Velg produkt**-feltet. ID-en brukes til å hente salgsprisen fra prosjektprislisten i tilbudet. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Produkt ikke i produktkatalog | Hurtigoppretting | En tekstboks for å skrive inn navnet på produktet. Dette feltet aktiveres bare hvis du velger **Ikke i produktkatalog** i **Velg produkt**-feltet.| Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Rolle | Hurtigoppretting | Rollen til personen som skal utføre dette arbeidet, eller som pådrar seg denne utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Kategori | Hurtigoppretting | Kategorien for arbeidet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Startdato | Hurtigoppretting | Arbeidets startdato. | Dette feltet settes som standard til tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Sluttdato | Hurtigoppretting | Arbeidets sluttdato. | Dette feltet settes som standard til tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Ressursenhet | Hurtigoppretting | Ressursenheten som pådrar seg denne kostnaden, og som sørger for ressursen for å arbeide med den. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk, og som brukes ved henting av kostpris. |
| Tidsplan for enhet | Hurtigoppretting | Enhetsgruppen for arbeidet, produktet eller utgiften. Enhetene tilhører en enhetsplan eller en gruppe enheter. Eksempelvis er mil og kilometer enheter som tilhører en gruppe enheter som beskriver avstand. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Enhet | Hurtigoppretting | Enheten for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Antall | Hurtigoppretting | Antallet for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Enhetspris | Hurtigoppretting |Fakturasatsen for rollen som utfører arbeidet, enhetsprisen for produktet eller salgsprisen for produktet eller utgiftskategorien. Standardverdien i dette feltet er **Tid** basert på kombinasjonen av prisdimensjonsverdiene på rolleprislinjen i prosjektprislisten som gjelder for startdatoen. For **utgifter** er standarden fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, er det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien basert på **Prislisteelement**-linjen i prosjektprislisten som gjelder for startdatoen.| Kostnadssatsen for rollen som utfører arbeidet, kostnaden per enhet i utgiftskategorien eller enhetskostnaden for produktet. Standardverdien i dette feltet er **Tid** basert på kombinasjonen av prisdimensjonsverdiene på rolleprislinjen i prosjektprislisten som gjelder for startdatoen. For **utgifter** er standarden fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, er det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien basert på **Prislisteelement**-linjen i prosjektprislisten som gjelder for startdatoen.|
| Beregnet mva | Hurtigoppretting | Du kan angi beregnet avgift eller utgift for dette arbeidet manuelt. | Dette feltet har ingen nedstrøms påvirkning. |
| Mengde | Hurtigoppretting | Du kan angi informasjon manuelt i dette feltet hvis feltene **Antall** og **Pris** står tomme. Hvis disse feltene ikke er tomme, blir dette feltet skrivebeskyttet og beregnet som (antall \* enhetspris) + avgift. | Dette feltet har ingen nedstrøms påvirkning. |


## <a name="update-prices-on-quote-line-details"></a>Oppdatere priser på tilbudslinjedetaljer

Hvis du har endret prisene i prosjektprislisten som er knyttet til tilbudet, eller i kostnadsprislisten for kontraktenheten, kan du velge **Beregn på nytt** på **Tilbud**-siden for å oppdatere prisene på de individuelle tilbudslinjedetaljene for å gjenspeile denne endringen. Når du velger **Beregn på nytt**, vises det en advarsel som informerer deg om at prisene på tilbudslinjedetaljene for alle tilbudslinjene i dette tilbudet tilbakestilles. Velg **Ja** for å oppdatere priser for både salgs- og kostnadstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få tilgang til tilbudslinjedetaljer for kostnad

I kategorien **Tilbudslinjedetaljer** velger du en rad i rutenettet for å aktivere noen handlinger på verktøylinjen i delrutenettet. Den første handlingen på verktøylinjen i rutenettet når en tilbudslinjedetalj er valgt, er **Åpne kostnadsdetaljer**. Velg **Åpne kostnadsdetaljer** for å vise den beslektede kostnadssatsen og beløpet for denne tilbuds linjen.

> [!NOTE]
> Endring av ressursenhetenhet, antall, dato, rolle eller kategoriverdier på tilbudslinjedetaljene for kostnad, endrer de tilsvarende verdiene i tilbudslinjedetaljene for salg.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta på tilbudslinjedetaljer for kostnad og salg

Valuta på tilbudslinjedetaljene for salg kommer som standard fra prosjektprislisten som er effektiv, for startdatoen for tilbudslinjedetaljene.

Valuta på tilbudslinjedetaljene for kostnad kommer som standard fra kontraktenheten for tilbudet som er effektiv, for startdatoen for tilbudslinjedetaljene for kostnad.

Beregning av lønnsomhet konverter beløpet på tilbudslinjendetaljene for kostnader og salg til standardvalutaen for miljøet for å rapportere den totale beregnede marginen i tilbudet.

> [!MERK
> > Det kan oppstå valutaavrundingsfeil og endrede marginer på grunn av manglende datoeffektivitet for vekslingskurs. Bruk bare disse beregningene på prosjektkontrakter, da dette er tilnærminger og ikke gjelder faktiske lovpålagte eller annen rapportering som krever høyere presisjon for avrunding og bevissthet om datoeffektivitet for valutakurser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
