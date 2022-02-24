---
title: Løse kostpriser for estimater og faktiske verdier
description: Dette emnet gir informasjon om hvordan kostpriser for estimater og faktiske beløp løses.
author: rumant
manager: Annbe
ms.date: 04/09/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 13903acc22e765ddc5bc1b87428ef3565f2b0a44
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877324"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Løse kostpriser for estimater og faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

For å løse kostpriser og kostprislisten for estimater og faktiske verdier bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktenhet** i det relaterte prosjektet. Når kostprislisten er løst, løser programmet kostnadssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Løse kostnadssatser på faktiske og estimerte linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjedetaljene for tids- og ressurstilordninger i et prosjekt.

Når en kostprisliste er løst, bruker systemet feltene **Rolle**, **Ressursstyringsfirma** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prisdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare felter i stedet for, eller i tillegg til **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje. Hvis programmet finner en rolleprislinje som har en kostfor kombinasjonen av **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, det vil si standard kostpris. Hvis programmet ikke nøyaktig kan samsvare kombinasjonen av verdiene for **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolleverdi, men med nullverdier for **Ressursenhet** og **Ressursstyringsfirma**. Etter at en samsvarende rolleprisoppføring med samsvarende rolleprisverdi er funnet, brukes standardkostnadssatsen som standard fra denne oppføringen. 

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringer med verdier som samsvarer med hver av prissettingsdimensjonsverdiene i prioritetsrekkefølgen med rader som har nullverdier for de dimensjonene som kommer sist i prioritetsrekkefølgen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Løse kostnadssatser på faktiske og estimerte linjer for utgift

Estimatlinjer for utgift refererer til tilbuds- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene i et prosjekt.

Når en kostprisliste er løst, bruker systemet en kombinasjon av feltene **Kategori** og **Enhet** på estimatlinjen for en utgift til å samsvare mot **Kategoripris**-linjene i den løste prislisten. Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes kostnadssatsen som standard. Hvis systemet ikke kan samsvare verdiene for **Kategori** og **Enhet**, eller hvis det kan finne en samsvarende kategoriprislinje, men prismodellen ikke er **Pris per enhet**, settes kostnadssatsen som standard til null (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Løse kostnadssatser på linjer med faktiske verdier og estimatlinjer for materialer

Estimatlinjer for materialer refererer til tilbuds- og kontraktlinjedetaljer for materialer og materialestimatlinjene i et prosjekt.

Når en kostnadsprisliste er løst, bruker systemet en kombinasjon av feltene **Produkt** og **Enhet** på estimatlinjen for at et materialestimat skal samsvare mot **Prislisteelementer**-linjene i den løste prislisten. Hvis systemet finner en produktprislinje som har en kostnadssats for feltkombinasjonen **Produkt** og **Enhet**, brukes standardkostnadssatsen. Hvis systemet ikke kan samsvare verdiene for **Produkt** og **Enhet**, blir enhetskostnaden null som standard. Denne standardverdien brukes også hvis det finnes en samsvarende linje for prislisteelement, men prismodellen er basert på en standardkostnad eller gjeldende kostnad som ikke er definert i produktet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
