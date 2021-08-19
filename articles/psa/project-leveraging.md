---
title: Salgsestimater og prosjekter
description: Dette emnet gir informasjon om hvordan du kan dra nytte av tidsplanen og estimatene i salgsprosessen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1dac342ead487c50d14f3b2fa39e60314d13b0047b77fe6df8f32dee29b09422
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995188"
---
# <a name="sales-estimates-and-projects"></a>Salgsestimater og prosjekter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I løpet av salgsprosessen kan du opprette salgsestimater ved å koble et prosjekt til et tilbud. På denne måten kan deterministisk estimering utføres i løpet av salgsprosessen for å dra nytte av prosjektplanleggings- og estimeringsfunksjoner. Hvis salget går gjennom, kan tidsplanen som ble brukt til salgsestimeringen, brukes som grunnlag for videre beregning av prosjektplanen.

## <a name="linking-a-project-to-a-quote-line"></a>Koble et prosjekt til en tilbudslinje

Når du oppretter en prosjektbasert tilbudslinje, kan du opprette et nytt prosjekt eller knytte til et eksisterende prosjekt på **Tilbudslinje**-siden. 

> ![Tilbudslinje-skjemaet.](media/project-8.png)
 
Når du oppretter et nytt prosjekt fra tilbudslinjedetaljene, kan du dra nytte av prosjektmaler. Prosjektmaler er modellprosjekter som representerer standard prosjektplaner og økonomiske estimater som er typiske i en organisasjon. De kan også representere kopier av prosjektplaner og estimater fra tidligere prosjekter.

> ![Tilbudslinjedetaljer.](media/project-9.png)
  
Når du oppretter prosjektet fra tilbudet er prosjektet automatisk knyttet til tilbudslinjen.

## <a name="components-of-estimates-in-a-project"></a>Estimatkomponenter i et prosjekt

Ved hjelp av en tidsplan kan du dele arbeid inn i oppgaver, vedlikeholde et hierarki med oppgaver, bestemme hvilke ressurser som kreves for å fullføre en oppgave, og tilordne et estimat over innsatsen som kreves for å fullføre en oppgave.

Du kan definere arbeidsinnsatsen og tidsplanestimatene ved hjelp av feltene i kategorien **Tidsplan** på **Prosjekt**-siden. Siden en prisliste er knyttet til prosjektet, beregnes økonomiske estimater ved hjelp av kostnader og salgspriser som er definert i prislisten.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Importere estimater fra et prosjekt til et tilbud

Når du har definert prosjektestimater, kan du importere dem til tilbudslinjen. På siden **Tilbudslinjedetaljer** velger du **Importer fra estimater** på båndet for å oppsummere prosjektestimater etter transaksjonstype, rolle eller oppgavenivå.


[!INCLUDE[footer-include](../includes/footer-banner.md)]