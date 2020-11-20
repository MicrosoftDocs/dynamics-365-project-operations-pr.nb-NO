---
title: Løse kostpriser for estimater og faktiske verdier – Lite
description: Dette emnet gir informasjon om hvordan kostpriser for estimater og faktiske beløp løses.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3fedf7b577e2372fb10ea85ea1e3caa9bf2f5ad0
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176803"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Løse kostpriser for estimater og faktiske verdier – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

For å løse kostpriser og kostprislisten for estimater og faktiske verdier bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktenhet** i det relaterte prosjektet. Når kostprislisten er løst, løser programmet kostnadssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Løse kostnadssatser på faktiske og estimerte linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjedetaljene for tids- og ressurstilordninger i et prosjekt.

Når en kostprisliste er løst, bruker systemet feltene **Rolle** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prisdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare felter i stedet for, eller i tillegg til **Rolle** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje. Hvis programmet finner en rolleprislinje som har en kostfor kombinasjonen av **Rolle** og **Ressursenhet**, det vil si standard kostpris. Hvis programmet ikke kan samsvare verdiene for **Rolle** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når det har hentet en samsvarende rolleprisoppføring, blir kostnadssatsen som standard fra denne oppføringen. 

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringer med verdier som samsvarer med hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Løse kostnadssatser på faktiske og estimerte linjer for utgift

Estimatlinjer for utgift refererer til tilbuds- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene i et prosjekt.

Når en kostprisliste er løst, bruker systemet en kombinasjon av feltene **Kategori** og **Enhet** på estimatlinjen for en utgift til å samsvare mot **Kategoripris**-linjene i den løste prislisten. Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes kostnadssatsen som standard. Hvis systemet ikke kan samsvare verdiene for **Kategori** og **Enhet**, eller hvis det kan finne en samsvarende kategoriprislinje, men prismodellen ikke er **Pris per enhet**, settes kostnadssatsen som standard til null (0).
