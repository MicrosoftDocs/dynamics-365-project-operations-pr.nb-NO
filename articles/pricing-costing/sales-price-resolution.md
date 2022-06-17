---
title: Løse salgspriser for estimater og faktiske verdier
description: Denne artikkelen inneholder informasjon om hvordan du løser salgssatser for estimater og faktiske verdier.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee750b93a5be7be09ed76942c7c235f8c811e8bb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911838"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Løse salgspriser for estimater og faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når salgspriser på estimater og faktiske beløp løses i Dynamics 365 Project Operations, bruker systemet først datoen og valutaen for det relaterte prosjekttilbudet eller kontrakten til å løse salgsprislisten. Når salgsprislisten er løst, løser systemet salgs- eller fakturasatsen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Løse salgssatser på faktiske og estimerte linjer for tid

I Project Operations brukes estimatlinjer til å angi tilbudslinje- og kontraktlinjedetaljene for tids- og ressurstilordningene for prosjektet.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi fakturasatsen som standard.

1. Ssystemet bruker feltene **Rolle**, **Ressursstyringsfirma** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i den løste prislisten. Dette samsvaret forutsetter at standard prisdimensjoner for fakturasatser brukes. Hvis du har konfigurert prising basert på andre felter i stedet for, eller i tillegg til **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, er det denne kombinasjonen som brukes til å hente en samsvarende rolleprislinje.
2. Hvis systemet finner en rolleprislinje som har en fakturasats for kombinasjonen av feltene **Rolle**, **Ressurstyringsfirma** og **Ressursenhet**, brukes denne fakturasatsen som standard.
3. Hvis systemet ikke kan samsvare feltverdiene for **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når systemet har funnet en samsvarende rolleprisoppføring, blir fakturasatsen fra denne oppføringen standardsatsen. Dette samsvaret forutsetter en standardkonfigurasjon for den relative prioriteten for **Rolle** i forhold til **Ressursenhet** som en salgsprisdimensjon.

> [!NOTE]
> Hvis du konfigurerte en annen prioritering av **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringene med samsvarende verdier for hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

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
    | &nbsp; | Påslag over kostnad | Ved å bruke en markering som definert av kategoriprislinjen for enhetskostnadssasten for den relaterte faktiske kostnaden |

4. Hvis systemet ikke kan samsvare verdiene i feltene **Kategori** og **Enhet**, settes salgssatsen til null (0) som standard.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Løs salgssatser på linjer med faktiske verdier og estimatlinjer for materialer

I Project Operations brukes estimatlinjer for materialer til å angi tilbuds- og kontraktlinjedetaljer for materialer og materialestimatlinjene i et prosjekt.

Når en prisliste for salg er løst, fullfører systemet følgende trinn for angi enhetssalgsprisen som standard.

1. Systemet bruker feltkombinasjonen **Produkt** og **Enhet** på estimatlinjen for materiale for samsvar med prislisteelementlinjene i prislisten som ble løst.
2. Hvis systemet finner en prislisteelementlinje som har en salgssats for feltkombinasjonen **Produkt** og **Enhet** og prismetoden er **Valutabeløp**, brukes salgsprisen som er angitt på prislinjen.
3. Hvis verdiene i feltene **Produkt** og **Enhet** ikke samsvarer, blir salgssatsen null som standard.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
