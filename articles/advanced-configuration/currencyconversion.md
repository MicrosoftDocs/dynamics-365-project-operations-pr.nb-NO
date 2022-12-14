---
title: Konfigurer valutakonvertering for å beregne salgspriser fra kostnadssatser
description: Denne artikkelen forklarer hvordan du konfigurerer funksjonaliteten for valutakonvertering som skal brukes i Microsoft Dynamics 365 Project Operations når salgstransaksjoner genereres fra kostnadstransaksjoner.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816673"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Konfigurer valutakonvertering for å beregne salgspriser fra kostnadssatser

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

I Microsoft Dynamics 365 Project Operations kan salgspriser for utgiftskategorier konfigureres som numeriske verdier, eller de kan konfigureres slik at de beregnes basert på kostnaden som påløper.

Når de konfigureres slik at de beregnes basert på den påløpte kostnaden, er følgende alternativer tilgjengelige:

- Kostpris
- Påslagsprosent over kostnad

I scenarioer der utgiftskostnadene påløper i en annen valuta enn salgsvalutaen for prosjektkontrakten, kreves valutakonvertering for å beregne salgsprisen basert på kostnaden.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valutakonverteringsfunksjonalitet som bruker opprinnelige Dataverse-valutakurser

Project Operations bruker som standard valutakursene som er lagret i Valuta-tabellen i Dataverse. Følg denne fremgangsmåten for å konfigurere Project Operations slik at det bruker opprinnelige valutakurser til å beregne salgsprisen fra kostnader.

1. Gå til **Project Operations \> Innstillinger \> Parametere**.
1. Åpne detaljsiden **Prosjektparameter**.
1. Angi en tom verdi i feltet **Valutakonverteringslogikk**.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valutakonverteringsfunksjonalitet som bruker valutakurser fra økonomi- og driftsapper

Vekslingskursene i Valuta-tabellen som er opprinnelig tilgjengelige i Dataverse, er ikke datoeffektive. Det kan derfor hende at de ikke alltid skaleres til kravene du har for beregning av salgspriser fra kostnadssatser.

Du kan bruke valutakurser fra økonomi- og driftsmiljøet til å beregne salgsprisen i salgsvalutaen fra en kostnadssats i kostnadsvalutaen. Følg denne fremgangsmåten for å konfigurere denne valutakonverteringsfunksjonaliteten.

1. Legg til feltet **Valutakonverteringslogikk** på siden **Prosjektparametere**. Lagre og publiser deretter tilpassingen.
1. Gå til **Project Operations \> Innstillinger \> Parametere**.
1. Åpne detaljsiden **Prosjektparameter**. 
1. Sett feltet **Valutakonverteringsfunksjonalitet** til **Utvidet med tilbakefall til standard**.
1. Gi sikkerhetsrollen **Appbruker med dobbel skriving** tillatelsen **Global leser** til følgende tabeller:

    - msdyn\_currencyexchangerates
    - msdyn\_currencyexchangeratepairs
    - msdyn\_exchangeratetypes

1. I økonomi- og driftsmiljøet kjører du følgende tilordninger med dobbel skriving ved første synkronisering:

    - Valutakurstype (msdyn\_exchangeratetypes)
    - Valutapar for valutakurs (msdyn\_currencyexchangeratepairs)
    - Valutakurser for CDS (msdyn\_currencyexchangerates)

Etter at disse endringene er fullført, gjør dobbel skriving at valutakursene fra økonomi- og driftsmiljøet blir tilgjengelige i Dataverse. Project Operations bruker deretter disse valutakursene til å konvertere kostnadssatser til kontraktens salgsvaluta.

> [!NOTE]
> Denne valutakonverteringsfunksjonaliteten gjelder bare for beregning av salgspriser fra kostnadssatser. Den brukes ikke til generell beregning av standardvalutaverdier. Standardvalutaverdier bruker alltid opprinnelige Dataverse-valutakurser, uavhengig av om du fullfører denne fremgangsmåten.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
