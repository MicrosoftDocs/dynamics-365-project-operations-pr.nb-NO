---
title: Konfigurere kostnads- og salgspriser for utgifter
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for transaksjons- og utgiftskategoriene.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b518c9eda00bef4d342dd66677344af516012749
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180294"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Konfigurere kostnads- og salgspriser for utgifter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan sette opp kostnads- og salgspriser for transaksjonskategorier i Dynamics 365 Project Operations. Fordi kostnads- og salgspriser er utformet for utgifter, må hver transaksjonskategori som inkluderer disse, også være definert som en utgiftskategori. Dette oppsettet sørger for nøyaktigheten i funksjonaliteten nedstrøms. Kost- og salgspriser for transaksjonskategorier kan bare vises i én valuta, som må være valutaen i prislistehodet.

Følg fremgangsmåten nedenfor for å konfigurere kost- og salgspriser for transaksjonskategorier. 

1. Opprett en prisliste basert på prislistehodet. 
2. I **Kategoripriser**, på delrutenettmenyen, velger du **+ Ny kategoripris**. 
3. Angi transaksjonskategorien og enheten du oppretter den nye prisen for, på **Hurtigopprett**-siden.

Tabellen nedenfor viser feltene i kategorien **Generelt** og på **Hurtigopprett**-siden for en kategoriprislinje som du bør huske på når du oppretter kategoripriser i en salgs- eller kostprisliste.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Transaksjonskategori | Sidene **Generelt** og **Hurtigoppretting** | Velg transaksjonskategorien du oppretter en salgs- eller kostpris for. | Transaksjonskategorien i det innkommende estimatet eller den faktiske verdien for utgift samsvares mot denne linjen for å angi standard kost- eller salgssats for transaksjonskategorien. |
| Tidsplan for enhet | Sidene **Generelt** og **Hurtigoppretting** | Enhetsplanen kommer som standard fra enhetsplanen til transaksjonskategorien. | Dette feltet har ingen nedstrøms påvirkning. |
| Enhet | Sidene **Generelt** og **Hurtigoppretting** | Velg enheten som satsene opprettes for. | Enheten i det innkommende estimatet eller den faktiske verdien samsvares mot enheten på denne linjen for å standardisere satsen for utgiftsestimatet eller den faktiske verdien. |
| Prismodell | Sidene **Generelt** og **Hurtigoppretting** | Mulige verdier i feltet **Prismodell** er **Pris per enhet**, **Kostpris** og **Påslag over kostnad**. | Under prisoppsettet låser **Pris per enhet** feltet **Prosent** på kategoriprislinjen. Hvis **Kostpris** er valgt, er feltene **Pris** og **Prosent** låst i salgsprislisten. Hvis du velger **Påslag over kostnad**, låses **Pris**-feltet i salgsprislisten. På en innkommende faktisk linje for utgift fører prismodellen **Kostpris** og **Påslag over kostnad** til at den tilsvarende, ikke-fakturerte salgslinjen blir tilordnet en pris som er lik den faktiske kostprisen, eller som beregnes som påslag over prisen. |
| Pris | Sidene **Generelt** og **Hurtigoppretting** | Angi en sats per enhet for transaksjonskategorien og enhetskombinasjonen. Satsen for kjøregodtgjørelse er for eksempel 10 USD per mile og 8 USD per kilometer. | Kjøregodtgjørelsen er satsen som angis soom standard for pris eller kostnad per enhet for det innkommende estimatet eller den faktiske linjen for en utgiftstransaksjonsklasse.|
| Prosent | Sidene **Generelt** og **Hurtigoppretting** | Angi en prosent over kostnad for transaksjonskategorien og enhetskombinasjonen. Salgsprisen for flybilletter kan for eksempel merkes som 10 prosent av kostnaden av den påløpte flyreiseutgiften. | Denne prosenten over kostnad er bare relevant i en salgsprisliste når den valgte prismetoden er **Påslag over kostnad**. |
| Valuta | Sidene **Generelt** og **Hurtigoppretting** | Som standard kommer denne verdien fra valutaen i hodet i i prislisten. For transaksjonskategoripriser kan ikke valutaen overstyres. | Denne valutaen settes som standard på prisen per enhet på den innkommende faktiske linjen i utgiftstransaksjonsklassen for kostnader og salg. |

## <a name="pricing-methods-for-expenses"></a>Prismodeller for utgifter

Når du definerer kategoripriser som bare er relevante i forbindelse med utgiftsprising, kan du bruke én av følgende tre prismodeller:

- **Pris per enhet**
- **Kostpris**
- **Påslag over kostnad**

### <a name="price-per-unit"></a>Pris per enhet
Når denne prismodellen er valgt på en kategoriprislinje som er koblet til en salgsprisliste, blir prisen som standard angitt for kategori- og enhetskombinasjonen både i estimatet og den faktiske verdien. Estimat refererer til prosjektestimatlinjene for utgifter, tilbudslinjedetaljene og kontraktlinjedetaljene for utgifter .

### <a name="at-cost"></a>Kostpris
Når denne prismodellen er valgt på kategoriprislinjen som er koblet til en salgsprisliste, blir prisen som standard angitt for kategori- og enhetskombinasjonen bare for den faktiske utgiften. Det kan for eksempel være ikke-fakturerte salgsverdier for utgiftstransaksjonsklassen. Enhetsprisen angis på ikke-fakturert salgsverdi fra enhetsprisen på faktisk kostnad for den aktuelle utgiften. Prisstandarden basert på kostnad utføres ikke på prosjektestimater for utgifter eller tilbudslinje- og kontraktlinjedetaljene for utgifter.

### <a name="markup-over-cost"></a>Påslag over kostnad
Når denne prismodellen er valgt på kategoriprislinjen som er koblet til en salgsprisliste, blir prisen som standard angitt for kategori- og enhetskombinasjonen bare for en faktisk utgift. Det kan for eksempel være ikke-fakturerte salgsverdier for utgiftstransaksjonsklassen. Denne enhetsprisen er satt til den ikke-fakturerte salgsverdien til en beregnet verdi fra enhetsprisen på den faktiske kostnaden for den aktuelle utgiften etter at den definerte påslagsprosenten er brukt. Prisstandarden basert på kostnad utføres ikke i prosjektestimater for utgifter eller tilbudslinje- og kontraktlinjedetaljer for utgifter.
