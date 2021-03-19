---
title: Løse kostpriser for estimater og faktiske verdier
description: Dette emnet gir informasjon om hvordan kostpriser for estimater og faktiske beløp løses.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c2fe2a15d38ab5a1f2a93c6db4ed6b7eb9bbd33d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275685"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Løse kostpriser for estimater og faktiske verdier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

For å løse kostpriser og kostprislisten for estimater og faktiske verdier bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktenhet** i det relaterte prosjektet. Når kostprislisten er løst, løser programmet kostnadssatsen.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Løse kostnadssatser på faktiske og estimerte linjer for tid

Estimatlinjer for tid refererer til tilbuds- og kontraktlinjedetaljene for tids- og ressurstilordninger i et prosjekt.

Når en kostprisliste er løst, bruker systemet feltene **Rolle**, **Ressursstyringsfirma** og **Ressursenhet** på estimatlinjen for tid til å samsvare mot rolleprislinjene i prislisten. Dette samsvaret forutsetter at du bruker standard prisdimensjoner for arbeidskostnad. Hvis du har konfigurert systemet til å samsvare felter i stedet for, eller i tillegg til **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje. Hvis programmet finner en rolleprislinje som har en kostfor kombinasjonen av **Rolle**, **Ressursstyringsfirma** og **Ressursenhet**, det vil si standard kostpris. Hvis programmet ikke kan samsvare verdiene for **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**. Når det har hentet en samsvarende rolleprisoppføring, blir kostnadssatsen som standard fra denne oppføringen. 

> [!NOTE]
> Hvis du konfigurerer en annen prioritering av **Rolle**, **Ressursutstyringsfirma** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette. Systemet henter rolleprisoppføringer med verdier som samsvarer med hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Løse kostnadssatser på faktiske og estimerte linjer for utgift

Estimatlinjer for utgift refererer til tilbuds- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene i et prosjekt.

Når en kostprisliste er løst, bruker systemet en kombinasjon av feltene **Kategori** og **Enhet** på estimatlinjen for en utgift til å samsvare mot **Kategoripris**-linjene i den løste prislisten. Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes kostnadssatsen som standard. Hvis systemet ikke kan samsvare verdiene for **Kategori** og **Enhet**, eller hvis det kan finne en samsvarende kategoriprislinje, men prismodellen ikke er **Pris per enhet**, settes kostnadssatsen som standard til null (0).


[!INCLUDE[footer-include](../includes/footer-banner.md)]