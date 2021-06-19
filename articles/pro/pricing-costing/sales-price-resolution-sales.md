---
title: Løs salgspriser for prosjektestimater og faktiske verdier
description: Dette emnet inneholder informasjon om løsing av salgspriser i prosjektestimater og faktiske verdier.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8ac7b8ca7dfc5679b0acb1a984bb7663552d66b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004349"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Løs salgspriser for prosjektestimater og faktiske verdier

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Når salgspriser på estimater og faktiske beløp løses i Dynamics 365 Project Operations, bruker systemet først datoen og valutaen for det relaterte prosjekttilbudet eller kontrakten til å løse salgsprislisten. Når salgsprislisten er løst, løser systemet salgs- eller fakturasatsen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Løse salgssatser på faktiske og estimerte linjer for tid

I Project Operations brukes estimatlinjer til å angi tilbudslinje- og kontraktlinjedetaljene for tids- og ressurstilordningene for prosjektet.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi fakturasatsen som standard.

1. Ssystemet bruker feltene **Rolle** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i den løste prislisten. Dette samsvaret forutsetter at standard prisdimensjoner for fakturasatser brukes. Hvis du har konfigurert prising basert på andre felter i stedet for, eller i tillegg til **Rolle** og **Ressursenhet**, er det denne kombinasjonen som brukes til å hente en samsvarende rolleprislinje.
2. Hvis systemet finner en rolleprislinje som har en fakturasats for kombinasjonen av feltene **Rolle** og **Ressursenhet**, brukes denne fakturasatsen som standard.
3. Hvis systemet ikke kan samsvare feltverdiene for **Rolle** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når systemet har funnet en samsvarende rolleprisoppføring, blir fakturasatsen fra denne oppføringen standardsatsen. Dette samsvaret forutsetter en standardkonfigurasjon for den relative prioriteten for **Rolle** i forhold til **Ressursenhet** som en salgsprisdimensjon.

> [!NOTE]
> Hvis du har konfigurert en annen prioritering av **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringene med samsvarende verdier for hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Løse salgssatser på faktiske og estimerte linjer for utgift

I Project Operations brukes estimatlinjer for utgift til å angi tilbudslinje- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene for prosjektet.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi enhetssalgsprisen som standard.

1. Systemet bruker kombinasjonen av feltene **Kategori** og **Enhet** på estimatlinjen for utgift til å samsvare mot kategoriprislinjene i prislisten som er løst.
2. Hvis systemet finner en kategoriprislinje som har en salgssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes denne salgssatsen som standard.
3. Hvis systemet finner en samsvarende kategoriprislinje, kan prismodellen brukes til å angi salgsprisen som standard. Tabellen nedenfor viser standard virkemåte for utgiftspris i Project Operations.

    | Kontekst | Prismodell | Pris brukt som standard |
    | --- | --- | --- |
    | Estimat | Pris per enhet | Basert på kategoriprislinjen |
    | &nbsp; | Kostpris | 0.00 |
    | &nbsp; | Påslag over kostnad | 0.00 |
    | Faktisk | Pris per enhet | Basert på kategoriprislinjen |
    | &nbsp; | Kostpris | Basert på de relaterte faktiske kostnadene |
    | &nbsp; | Påslag over kostnad | Bruk en markering som definert av kategoriprislinjen for enhetskostnadssasten for den relaterte faktiske kostnadenn |

4. Hvis systemet ikke kan samsvare verdiene i feltene **Kategori** og **Enhet**, settes salgssatsen til null (0) som standard.

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Løse salgssatser på linjer med faktiske verdier og estimatlinjer for materialer

I Project Operations brukes estimatlinjer for materialer til å angi tilbuds- og kontraktlinjedetaljer for materialer og materialestimatlinjene i et prosjekt.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi enhetssalgsprisen som standard.

1. Systemet bruker feltkombinasjonen **Produkt** og **Enhet** på estimatlinjen for materiale for samsvar med prislisteelementlinjene i prislisten som ble løst.
2. Hvis systemet finner en prislisteelementlinje som har en salgssats for feltkombinasjonen **Produkt** og **Enhet** og prismetoden er **Valutabeløp**, brukes salgsprisen som er angitt på prislinjen.
3. Hvis verdiene i feltene **Produkt** og **Enhet** ikke samsvarer, blir salgssatsen null som standard.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
