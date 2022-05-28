---
title: Estimere en prosjektbasert kontraktlinje – Lite
description: Dette emnet inneholder informasjon om estimering av en prosjektbasert kontraktlinje.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 179994a2515686bce2370964121cbdca08a9d085
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597350"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimere en prosjektbasert kontraktlinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations inneholder en prosjektbasert kontraktlinje detaljer som hjelper deg med å estimere kostnaden og potensiell omsetning på arbeidet som er involvert i å levere kontraktlinjen.

For å beregne en prosjektbasert kontraktlinje går du til kategorien **Kontraktlinjedetalj** på den prosjektbaserte **Kontraktlinje**.  Det er to måter å opprette et estimat på en prosjektbasert kontraktlinje på:

   - Opprett et estimat direkte på kontraktlinjen ved å legge til kontraktlinjedetaljer manuelt.
   - Opprett et prosjekt og en prosjektplan, og knytt deretter prosjektet og aktivitetene til kontraktlinjen i prosjektet. Dette gjør at du kan importere prosjektplananslaget til kontraktlinjen basert på komponentene som er inkludert på kontraktlinjen.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Opprette et estimat direkte på en prosjektbasert kontraktlinje

Gjør følgende for å opprette et estimat direkte på en prosjektbasert kontraktlinje:

1. Gå til kontraktlinjen, og velg kategorien **Kontraktlinjedetaljer**. Linjene du oppretter i denne kategorien, oppsummeres og vises som **Kontraktverdi** for denne **Kontraktlinjen**. 
2. I underrutenettet **Kontraktlinjedetaljer** velger du **Ny kontraktlinjedetalj**. Det åpnes en glidebryter for hurtigopprettelse. Følgende felter er tilgjengelige på siden **Kontraktlinjedetaljer**.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Beskrivelse** | **Hurtigoppretting** | En beskrivelse av det spesifikke estimatet. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Transaksjonsklasse** | **Hurtigoppretting** | Dette er en liste over transaksjonsklasser som er inkludert i kategorien **Generelt** for den prosjektbaserte kontraktlinjen. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Velg produkt** | **Hurtigoppretting** | Gjelder når transaksjonsklassen er **Materiale**. Du kan angi om denne estimatlinjen gjelder et **eksisterende** produkt (i produktkatalogen) eller et produkt som **ikke er** i produktkatalogen. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Produkt** | **Hurtigoppretting** | ID-en for produktet fra produktkatalogen. Dette feltet aktiveres bare når du velger **Eksisterende produkt** i **Velg produkt**-feltet. ID-en brukes til å hente salgsprisen fra prosjektprislisten i kontrakten. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Produkt ikke i produktkatalog** | **Hurtigoppretting** | Et tekstfelt der du kan skrive inn produktnavnet. Dette feltet aktiveres bare når du velger **Ikke i produktkatalog** i **Velg produkt**-feltet.| Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Rolle** | **Hurtigoppretting** | Rollen til personen som utfører dette arbeidet eller oppretter utgiften. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk.|
| **Kategori** | **Hurtigoppretting** | Kategorien for arbeidet eller utgiften. |Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk.|
| **Startdato** | **Hurtigoppretting** | Arbeidets startdato. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Sluttdato** | **Hurtigoppretting** | Arbeidets sluttdato. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Ressursenhet** | **Hurtigoppretting** | Ressursenheten som pådrar seg denne kostnaden, og som sørger for ressursen for å arbeide med den. |Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk, og som brukes ved henting av kostpris. |
| **Tidsplan for enhet** | **Hurtigoppretting** | Enhetsgruppen for arbeidet, produktet eller utgiften. Enhetene tilhører en enhetsplan eller en gruppe enheter. Eksempelvis er *Mil* og *Kilometer (kms)* enheter som tilhører en gruppe enheter som beskriver avstand. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Enhet** | **Hurtigoppretting** | Enheten for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Antall** | **Hurtigoppretting** | Antallet for arbeidet, produktet eller utgiften. | Denne verdien settes som standard til den relaterte kontraktlinjedetaljen for kostnaden som opprettes automatisk. |
| **Enhetspris** | **Hurtigoppretting** | Fakturasatsen for rollen som utfører arbeidet, enhetsprisen for produktet eller salgsprisen for produktet eller utgiftskategorien. Dette feltet brukes som standard for **Tid** basert på kombinasjonen av prisdimensjonsverdier på rolleprislinjen i prosjektprislisten som gjelder for startdatoen. For **utgifter** er dette feltets standard fra prisoppsettet for transaksjonskategorien i prosjektprislisten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er **pris per enhet**, finnes det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien for dette feltet basert på **Prislisteelement**-linjen i prosjektprislisten som gjelder for startdatoen.| Kostnadssatsen for rollen som utfører arbeidet, eller kostnaden per enhet i utgiftskategorien eller enhetskostnaden for produktet. Dette feltet brukes som standard for **Tid** basert på kombinasjonen av prisdimensjonsverdier på kostprislinjen vedlagt kontraktenheten som gjelder for startdatoen. For utgifter er dette feltets standard basert på kategoriprislinjen for kostprislisten som er knyttet til kontraktenheten som gjelder for startdatoen. Hvis prismodellen for transaksjonskategorien ikke er pris per enhet, finnes det ingen standard, og dette feltet blir stående tomt. For produkter er standardverdien for dette feltet basert på **Prislisteelement**-linjen i kostnadsprislisten vedlagt kontraktenheten som gjelder for startdatoen.|
| **Beregnet mva** | **Hurtigoppretting** | Estimert avgift for dette arbeidet eller denne utgiften. | Estimert avgift for dette arbeidet eller denne utgiften. |
| **Mengde** | **Hurtigoppretting** | Du kan legge til verdien i dette feltet hvis feltene **Antall** og **Pris** er tomme. Hvis **Antall** og **Pris** er utfylt, er feltet **Mengde** skrivebeskyttet, og det beregnes som **(Antall \*Enhetspris) + avgift**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Oppdatere priser på kontraktlinjedetaljer

Hvis du endrer priser på prosjektprislisten som er knyttet til kontrakten eller kostnadsprislisten for kontraktsenheten, kan du oppdatere prisene i de enkelte kontraktlinjedetaljene for å gjenspeile endringen. På siden **Kontrakt** velger du **Omberegn**. Det vises en advarsel om at prisene for alle kontraktlinjene i denne kontrakten tilbakestilles. Velg **Ja** å oppdatere priser for både salgs- og kostnadskontraktlinjedetaljer.

## <a name="access-contract-line-details-for-cost"></a>Få tilgang til kontraktlinjedetaljer for kostnad

I kategorien **Kontraktlinjedetaljer** velger du en rad i rutenettet for å vise handlinger på verktøylinjen i delrutenettet. Den første handlingen på verktøylinjen for underrutenett er **Åpne kostnadsdetaljer**. Hvis du vil vise den beslektede kostnadssatsen og beløpet for denne kontraktlinjedetaljen, velger du **Åpne kostnadsdetaljer**. 

> [!NOTE]
> Hvis du endrer verdiene for ressursstyringsfirma, ressursstyringsenhet, mengde, datoer, rolle eller kategori på kontraktlinjedetaljene for **Kostnad**, endres også de tilsvarende verdiene på kontraktlinjedetaljen for **Salg**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Valuta på kontraktlinjedetaljer for kostnad og salg

Kontraktlinjedetaljene for **Salg** angir standardvalutaen fra prosjektprislisten som er gyldig for startdatoen for kontraktlinjedetaljene.

Kontraktlinjedetaljene for **Kostnad** angir standardvalutaen fra prislisten for kontraktenheten for kontrakten som er gyldig for startdatoen for kontraktlinjedetaljen for **Kostnad**.

Beregning av fortjeneste konverterer beløpene for kontraktlinjedetaljer for **Kostnad** og **Salg** til standardvalutaen for miljøet for å rapportere de samlede faktiske og beregnede marginene på kontrakten.

> [!NOTE]
> Det kan oppstå valutaavrundingsfeil og endrede marginer på grunn av manglende datoeffektivitet for vekslingskurs. Bruk bare disse beregningene på prosjektkontrakter, da dette er tilnærminger og ikke gjelder faktiske lovpålagte eller annen rapportering som krever høyere presisjon for avrunding og bevissthet om datoeffektivitet for valutakurser.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
