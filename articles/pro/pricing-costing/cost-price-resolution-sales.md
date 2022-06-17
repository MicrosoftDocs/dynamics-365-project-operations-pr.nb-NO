---
title: Løse kostpriser for estimater og faktiske verdier i et prosjekt
description: Denne artikkelen inneholder informasjon om hvordan kostpriser i prosjektestimater og faktiske verdier løses.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c278d8994389145c6dbee7574d2354724d985722
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917542"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Løse kostpriser for estimater og faktiske verdier i et prosjekt 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

For å løse kostpriser og kostprislisten for estimater og faktiske verdier bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktenhet** i det relaterte prosjektet. Når kostprislisten er løst, løser programmet kostnadssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Løse kostnadssatser på faktiske og estimerte linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjedetaljene for tids- og ressurstilordninger i et prosjekt.

Etter at en kostprisliste er løst, blir feltene **Rolle** og **Ressursenhet** på estimatlinjen for Tid samsvart mot rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prissettingsdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare felter i stedet for, eller i tillegg til **Rolle** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje. Hvis programmet finner en rolleprislinje som har en kostfor kombinasjonen av **Rolle** og **Ressursenhet**, det vil si standard kostpris. Hvis programmet ikke kan samsvare verdiene for **Rolle** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når det har hentet en samsvarende rolleprisoppføring, blir kostnadssatsen som standard fra denne oppføringen. 

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringer med verdier som samsvarer med hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Løse kostnadssatser på faktiske og estimerte linjer for utgift

Estimatlinjer for utgift refererer til tilbuds- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene i et prosjekt.

Når en kostprisliste er løst, bruker systemet en kombinasjon av feltene **Kategori** og **Enhet** på utgiftsestimatlinjen til å samsvare mot linjene for **Kategoripris** i den løste prislisten. Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes kostnadssatsen som standard. Hvis systemet ikke kan samsvare verdiene for **Kategori** og **Enhet**, eller hvis systemet finner en samsvarende kategoriprislinje, men prissettingsmetoden ikke er **Pris per enhet**, brukes som standard en kostnadssats på null(0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Løse kostnadssatser på linjer med faktiske verdier og estimatlinjer for materialer

Estimatlinjer for materialer refererer til tilbuds- og kontraktlinjedetaljer for materialer og materialestimatlinjene i et prosjekt.

Når en kostnadsprisliste er løst, bruker systemet en kombinasjon av feltene **Produkt** og **Enhet** på estimatlinjen for at et materialestimat skal samsvare mot **Prislisteelementer**-linjene i den løste prislisten. Hvis systemet finner en produktprislinje som har en kostnadssats for feltkombinasjonen **Produkt** og **Enhet**, brukes standardkostnadssatsen. Hvis systemet ikke samsvarer med verdiene for **Produkt** og **Enhet**, eller hvis det finner en samsvarende prislisteelementlinje, men prismodellen er basert på standardkostnad eller gjeldende kostnad, og ingen av dem er definert på produktet, angis enhetskostnaden som null.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
