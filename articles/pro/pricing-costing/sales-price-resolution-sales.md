---
title: Løse salgspriser for estimater og faktiske verdier
description: Dette emnet gir informasjon om løsing av salgspriser for estimater og faktiske verdier.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c8972bd7710735e9acdbf951079f2da24a00bd7f
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088034"
---
# <a name="resolving-sales-prices-for-estimates-and-actuals"></a>Løse salgspriser for estimater og faktiske verdier

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Når salgspriser for estimater og faktiske verdier løses i Dynamics 365 Project operations, bruker systemet først datoen og valutaen for det relaterte prosjekttilbudet eller kontrakten til å løse salgsprislisten. Når salgsprislisten er løst, løser systemet salgs- eller fakturasatsen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Løse salgssatser på faktiske og estimerte linjer for tid

I Project Operations brukes estimatlinjer til å angi tilbudslinje- og kontraktlinjedetaljene for tids- og ressurstilordningene for prosjektet.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi fakturasatsen som standard.

1. Ssystemet bruker feltene **Rolle** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i den løste prislisten. Dette samsvaret forutsetter at standard prisdimensjoner for fakturasatser brukes. Hvis du har konfigurert prising basert på andre felter i stedet for, eller i tillegg til **Rolle** og **Ressursenhet** , er det denne kombinasjonen som brukes til å hente en samsvarende rolleprislinje.
2. Hvis systemet finner en rolleprislinje som har en fakturasats for kombinasjonen av feltene **Rolle** og **Ressursenhet** , brukes denne fakturasatsen som standard.
3. Hvis systemet ikke kan samsvare feltverdiene for **Rolle** og **Ressursenhet** , henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når systemet har funnet en samsvarende rolleprisoppføring, blir fakturasatsen fra denne oppføringen standardsatsen. Dette samsvaret forutsetter en standardkonfigurasjon for den relative prioriteten for **Rolle** i forhold til **Ressursenhet** som en salgsprisdimensjon.

> [!NOTE]
> Hvis du har konfigurert en annen prioritering av **Rolle** og **Ressursenhet** , eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringene med samsvarende verdier for hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Løse salgssatser på faktiske og estimerte linjer for utgift

I Project Operations brukes estimatlinjer for utgift til å angi tilbudslinje- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene for prosjektet.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi enhetssalgsprisen som standard.

1. Systemet bruker kombinasjonen av feltene **Kategori** og **Enhet** på estimatlinjen for utgift til å samsvare mot kategoriprislinjene i prislisten som er løst.
2. Hvis systemet finner en kategoriprislinje som har en salgssats for kombinasjonen av feltene **Kategori** og **Enhet** , brukes denne salgssatsen som standard.
3. Hvis systemet finner en samsvarende kategoriprislinje, kan prismodellen brukes til å angi salgsprisen som standard. Tabellen nedenfor viser standard virkemåte for utgiftspris i Project Operations.

    | Kontekst | Prismodell | Pris brukt som standard |
    | --- | --- | --- |
    | Estimat | Pris per enhet | Basert på kategoriprislinjen |
    | &nbsp; | Kostpris | 0.00 |
    | &nbsp; | Påslag over kostnad | 0.00 |
    | Faktisk | Pris per enhet | Basert på kategoriprislinjen |
    | &nbsp; | Kostpris | Basert på de relaterte faktiske kostnadene |
    | &nbsp; | Påslag over kostnad | Bruk en markering som definert av kategoriprislinjen for enhetskostnadssasten for den relaterte faktiske kostnadenn |

4. Hvis systemet ikke kan samsvare verdiene i feltene **Kategori** og **Enhet** , settes salgssatsen til null (0) som standard.
