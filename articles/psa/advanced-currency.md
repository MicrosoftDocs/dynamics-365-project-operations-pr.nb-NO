---
title: Scenarioer for flere valutaer (versjon 3.x)
description: Dette emnet inneholder informasjon om scenarioer med flere valutaer.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 33e44297dc80801c3e4416cd9fc3bedae5f3c4ba
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291721"
---
# <a name="multiple-currency-scenarios"></a>Scenarioer for flere valutaer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 har to valutakonsepter:

- **Transaksjonsvaluta** – valutaen som en transaksjon utføres i. 
- **Standard valuta** – valutaen for Dynamics 365-forekomsten. Denne valutaen konfigureres når en Dynamics 365-forekomst klargjøres. Dette kan ikke endres.

Ekeli solgte for eksempel 100 T-skjorter til en kunde i Storbritannia for 15 pund (GBP) per stykk. Tabellen nedenfor viser hvordan denne transaksjonen registreres i Ordreprodukt-enheten.

| Produkt | Antall | Pris per enhet | Valuta | Beløp | Valutakurs | Grunnpris per enhet| Beløp (st.valuta)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| T-skjorte | 100      | 15             | GBP      | 1500   | 0.94          | USD 17,25               | USD 1,725       |

**Valuta**-kolonnen viser transaksjonsvalutaen, som er valutaen som salget forekom i. **Valutakurs**-kolonnen er valutakursen mellom transaksjonsvalutaen og basisvalutaen. Basisvalutaen er amerikanske dollar (USD). Denne basisvalutaen ble konfigurert da Dynamics 365-forekomsten ble klargjort.
Som tabellen viser, registreres hver transaksjon både i transaksjonsvalutaen og basisvalutaen. Dynamics 365 bruker valutakursen til å beregne basisvalutabeløpene.

## <a name="project-service-automation-extensions"></a>Project Service Automation-utvidelser

Dynamics 365 Project Service Automation påvirker transaksjonsvalutaen, fordi forretningstransaksjoner vanligvis har to aspekter: kostnad og salg.

Følgende enheter anses som forretningstransaksjoner:

- Tilbudslinjedetalj
- Detalj for prosjektkontraktlinjer
- Estimatlinje
- Journallinje
- Fakturalinjedetalj
- Faktisk

I hver av disse enhetene finnes det en oppføring som representerer kostnadsbeløpet eller salgsbeløpet. På samme måte som for alle Dynamics 365-enheter som har et **Beløp**-felt, inneholder hver oppføring beløp både i transaksjonsvalutaen og basisvalutaen. 

PSA utvider konseptet med transaksjonsvaluta for kostnaden og salget på følgende måter:

- Kostnadstransaksjonsvalutaen for tidstransaksjoner kommer alltid fra valutaen til organisasjonsenheten som eier eller administrerer prosjektet. Denne organisasjons enheten kalles en kontraktsenhet.
- Salgstransaksjonsvalutaen for tids- og utgiftstransaksjoner kommer alltid fra valutaen til prosjektkontrakten.
- Kostnadstransaksjonsvalutaen for utgifter kommer fra valutaen som utgiftsoppføringen ble opprettet i.

## <a name="multiple-currency-scenario"></a>Scenario for flere valutaer

Denne delen beskriver et eksempel på et prosjekt som har fått navnet Fabrikam, Japan. Slik er scenarioet satt opp:

1. GBP og japanske yen (JPY) er angitt under **Innstillinger** \> **Forretningsbehandling** \> **Valutaer**. 
2. En kundekonto med navnet **Fabrikam - Japan** er satt opp, og JPY er valgt som valuta for forretningsforbindelsen.
3. En organisasjonsenhet kalt **Ekeli UK** er konfigurert, og GBP er valgt som valuta.
4. En prosjektkontrakt opprettes, der **Ekeli UK** er angitt som kontraktsenheten, og **Fabrikam – Japan** er angitt som kunden.
5. Prosjektkontraktlinjer opprettes basert på faktureringsarrangementer for de forskjellige transaksjonsklassene i prosjektet, for eksempel fakturering av tid kontra fakturering av utgifter.
6. Det opprettes et prosjekt der **Ekeli UK** er angitt som kontraktsenheten. Dette prosjektet opprettes og tilordnes til prosjektkontraktslinjene.


Under forhåndsberegning som bruker tilbudslinjedetaljene, detaljene for prosjektkontraktslinjen eller på estimatlinjen for tidsplanen, opprettes det alltid to oppføringer i enheten. Den ene oppføringen gjelder kostnad, og den andre oppføringen er for salg.

- Som standard er transaksjonsvalutaen i kostnadsoppføringen satt til valutaen i prosjektets kontraktsenhet. I dette eksemplet er valutaen GBP.
- Som standard er transaksjonsvalutaen i salgsoppføringen satt til valutaen i prosjektkontrakten. I dette eksemplet er valutaen JPY.

Når faktiske verdier opprettes for tid ved hjelp av tidsoppføringen eller journallinjen, skjer følgende:

- Som standard er transaksjonsvalutaen i kostnadsoppføringen satt til valutaen i prosjektets kontraktsenhet.
- Som standard er transaksjonsvalutaen i salgsoppføringen satt til valutaen i prosjektkontrakten.

Når faktiske verdier opprettes for utgifter tid ved hjelp av utgiftsoppføringen eller journallinjen, skjer følgende:

- Du kan registrere utgiftsbeløpet i en hvilken som helst valuta. Velg valutaen ved hjelp av valutavelgeren på siden **Utgiftsoppføring** eller på siden **Journallinje**. Som standard er transaksjonsvalutaen for kostnadsoppføringen satt til valutaen i utgiftsoppføringen. 
- Som standard er transaksjonsvalutaen for salgsoppføringen valutaen i prosjektkontrakten. Hvis du vil angi denne valutaen, konverterer systemet først transaksjonsbeløpet i valutaen som brukeren angav, til basisvalutaen. Beløpet konverteres deretter til valutaen i prosjektkontrakten. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Beregne verdier når faktiske verdier for prosjekter registreres i flere transaksjonsvalutaer

Dynamics 365 håndterer automatisk verdier i forskjellige valutaer. Her er et eksempel.

| Transaksjonsklasse | Transaksjonstype| Date   | Ressurs | Transaksjonskategori | Antall | Enhetspris | Beløp      | Valutakurs | Beløp i basis |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Ufakturert salg   | 14. juni | Noah  |                      | 8 timer    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Time              | Ufakturert salg   | 15. juni | Noah  |                      | 8 timer    | 20 000 JPY    | 160 000 JPY | 123           | 1300,81 USD    |
| Utgift           | Ufakturert salg   | 16. juni | Noah  | Hotell                | 1 per stk.     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Utgift           | Ufakturert salg   | 17. juni | Noah  | Leiebil           | 1 per stk.     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Hvis du vil beregne den totale verdien for ufakturert salg i prosjektet, kan du opprette et verdifelt felt for **Beløp**-feltet i alle de relaterte, ufakturerte salgsbeløpene. Verdifeltet er en konstruksjon i Dynamics 365, som gjør det mulig å bruke hurtigformler på relaterte oppføringer.


[!INCLUDE[footer-include](../includes/footer-banner.md)]