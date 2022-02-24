---
title: Estimere en prosjekttilbudslinje
description: Dette emnet inneholder informasjon om hvordan du oppretter et estimat på en prosjekttilbudslinje.
author: rumant
manager: Annbe
ms.date: 04/01/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b941511f842a81764ddd1c05a437578b9fd902ce
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858800"
---
# <a name="estimate-a-project-quote-line"></a>Estimere en prosjekttilbudslinje

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

En prosjektbasert tilbudslinje inneholder detaljer som bidrar til beregning av kostnader og potensiell omsetning på arbeidet som er involvert i å levere tilbudslinjen.

Hvis du vil estimere en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj** på tilbudslinjen. Du kan opprette et estimat på en prosjektbasert tilbudslinje på to måter:

   - Opprett estimatet manuelt direkte på tilbudslinjen ved hjelp av tilbudslinjedetaljer. 
   - Opprett et prosjekt og en prosjektplan, og knytt deretter prosjektet og oppgavene i prosjektet til tilbudslinjen. Fremgangsmåten for import av beregningene for prosjektplanen til tilbudslinjen basert på informasjonen du har angitt, blir aktivert.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Opprette estimater direkte på en prosjektbasert tilbudslinje

Gjør følgende for å opprette følgende estimater direkte på en prosjektbasert kontraktlinje:

1. Hvis du vil opprette et estimat på en prosjektbasert tilbudslinje, velger du kategorien **Tilbudslinjedetalj**. Linjeelementet du oppretter i denne kategorien, oppsummerer den tilbudte verdien for denne tilbudslinjen. 
2. Hvis du vil opprette tilbudslinjedetaljer, velger du **Ny tilbudslinjedetalj** i delrutenettet **Tilbudslinjedetaljer**. En glidebryter for hurtigoppretting åpner. Følgende felt på **Tilbudslinje**-siden:

| **Felt** | **Sted** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Beskrivelse | Hurtigoppretting | En beskrivelse av det spesifikke estimatet. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Transaksjonsklasse | Hurtigoppretting | Denne rullegardinlisten inneholder transaksjonsklassene som er inkludert i kategorien **Generelt** for den prosjektbaserte tilbudslinjen.  | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Velg produkt | Hurtigoppretting | Gjelder når transaksjonsklassen er **Materiale**. Du kan velge å angi at denne estimatlinjen gjelder et **eksisterende** produkt (i produktkatalogen) eller et produkt som **ikke er** i produktkatalogen. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Produkt | Hurtigoppretting | ID-en for produktet fra produktkatalogen. Dette feltet aktiveres bare når du velger **Eksisterende** i **Velg produkt**-feltet. ID-en brukes til å hente salgsprisen fra prosjektprislisten i tilbudet. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Produkt ikke i produktkatalog | Hurtigoppretting | En tekstboks for å skrive inn produktnavnet. Dette feltet aktiveres bare når du velger **Ikke i produktkatalog** i **Velg produkt**-feltet.| Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Rolle | Hurtigoppretting | Rollen til personen som skal utføre dette arbeidet, eller som pådrar seg denne utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Kategori | Hurtigoppretting | Kategorien for arbeidet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Startdato | Hurtigoppretting | Arbeidets startdato. | Dette feltet settes som standard til tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Sluttdato | Hurtigoppretting | Arbeidets sluttdato. | Dette feltet settes som standard til tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Ressursstyringsfirma | Hurtigoppretting | Ressursfirmaet eller den juridiske enheten som pådrar seg denne kostnaden, gir ressursen mulighet til å arbeide med den. | Verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk, og som brukes ved henting av kostpris. |
| Ressursenhet | Hurtigoppretting | Ressursenheten som pådrar seg denne kostnaden, og som sørger for ressursen for å arbeide med den. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk, og som brukes ved henting av kostpris. |
| Tidsplan for enhet | Hurtigoppretting | Enhetsgruppen for arbeidet, produktet eller utgiften. Enhetene tilhører en enhetsplan eller en gruppe enheter. Eksempelvis er mil og kilometer enheter som tilhører en gruppe enheter som beskriver avstand. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Enhet | Hurtigoppretting | Enheten for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Antall | Hurtigoppretting | Antallet for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte tilbudslinjedetaljen for kostnaden som opprettes automatisk. |
| Enhetspris | Hurtigoppretting |Fakturasatsen for rollen som utfører arbeidet, enhetsprisen for produktet eller salgsprisen for produktet eller utgiftskategorien. Standardverdien for **Tid** er basert på kombinasjonen av prisdimensjonsverdier på rolleprislinjen i prosjektprislisten som gjelder for startdatoen. For **utgifter** er standarden fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, finnes det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien for dette feltet basert på **Prislisteelement**-linjen i prosjektprislisten som gjelder for startdatoen.| Kostnadssatsen for rollen som utfører arbeidet, kostnaden per enhet i utgiftskategorien eller enhetskostnaden for produktet. Standarden for **Tid** er basert på kombinasjonen av prisdimensjonsverdier på kostprislinjen vedlagt kontraktenheten som gjelder for startdatoen. For utgifter er standarden basert på kategoriprislinjen i kostnadsprislisten vedlagt kontraktenheten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, er det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien for dette feltet basert på **Prislisteelement**-linjen i kostnadsprislisten vedlagt kontraktenheten som gjelder for startdatoen.|
| Beregnet mva | Hurtigoppretting | Du kan angi beregnet avgift eller utgift for dette arbeidet manuelt. | Dette feltet har ingen nedstrøms påvirkning. |
| Mengde | Hurtigoppretting | Du kan angi informasjon manuelt i dette feltet hvis feltene **Antall** og **Pris** står tomme. Hvis disse feltene ikke er tomme, blir dette feltet skrivebeskyttet og beregnet som (antall \* enhetspris) + avgift. | Dette feltet har ingen nedstrøms påvirkning. |

## <a name="update-prices-on-quote-line-details"></a>Oppdatere priser på tilbudslinjedetaljer

Hvis du har endret priser på prosjektprislisten som er knyttet til tilbudet, eller på kostnadsprislisten for kontraktenheten, kan du velge **Beregn på nytt** på **Tilbud**-siden for å oppdatere prisene i de enkelte tilbudslinjedetaljene for å gjenspeile denne endringen. Når du velger **Beregn på nytt**, vises det en advarsel som informerer deg om at prisene på tilbudslinjedetaljene for alle tilbudslinjene i dette tilbudet tilbakestilles. Velg **Ja** for å oppdatere priser for både salgs- og kostnadstilbudslinjedetaljer.

## <a name="access-quote-line-details-for-cost"></a>Få tilgang til tilbudslinjedetaljer for kostnad

Følg denne fremgangsmåten for å få tilgang til tilbudslinjedetaljer for kostnader:

1. Velg en rad i rutenettet i kategorien **Tilbudslinjedetaljer** for å aktivere handlinger på verktøylinjen i delrutenettet. 
2. Velg **Åpne kostnadsdetaljer** for å vise den beslektede kostnadssatsen og beløpet for denne tilbuds linjen.

> [!NOTE]
> Endring av ressursenhetenhet, antall, dato, rolle eller kategoriverdier på tilbudslinjedetaljene for kostnad, endrer de tilsvarende verdiene i tilbudslinjedetaljene for salg.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Valuta på tilbudslinjedetaljer for kostnad og salg

Valutaen i tilbudslinjedetaljene for salg hentes som standard fra prosjektprislisten som gjelder for startdatoen for tilbudslinjedetaljene.

Valutaen i tilbudslinjedetaljene for kostnad hentes som standard fra prislisten for kontraktenheten i tilbudet som gjelder for startdatoen for tilbudslinjedetaljene for kostnaden.

> [!NOTE]
> Beregning av lønnsomhet konverter beløpet på tilbudslinjendetaljene for kostnader og salg til standardvalutaen for miljøet for å rapportere den totale beregnede marginen i tilbudet. Det kan oppstå valutaavrundingsfeil og endrede marginer på grunn av manglende datoeffektivitet for vekslingskurs. Bruk bare disse beregningene i prosjekttilbud, da dette er tilnærminger og ikke gjelder faktiske lovpålagte eller annen rapportering som krever høyere presisjon for avrunding og bevissthet om datoeffektivitet for valutakurser.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
