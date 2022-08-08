---
title: Angi reisegodtgjørelse ved hjelp av kjørelengdenivåer
description: Denne artikkelen inneholder informasjon om kilometersatser og reisegodtgjørelsesnivåer.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9689bbaf4c4f88ad9f746c3f98676f97e634ab6c
ms.sourcegitcommit: 5e1f549a2e55a87351b2979e3aff402ed35487e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9064290"
---
# <a name="set-up-mileage-using-mileage-rate-tiers"></a>Angi reisegodtgjørelse ved hjelp av kjørelengdenivåer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når en utgift rapporteres og den valgte utgiftskategorien er **Reisegodtgjørelse**, beregnes beløpet for utgiftslinjen i henhold til beløpet *sats per reisegodtgjørelse*. Dette beløpet fastsettes ved hjelp av definerte reisegodtgjørelsesnivåer eller, hvis ingen reisegodtgjørelsesnivå er definert, ved å følge standard reisegodtgjørelsesats. 

Reisegodtgjørelsesnivåer kan konfigureres ved å gå til **Utgiftshåndtering** > **Oppsett** > **Generelt** > **Utgiftskategorier** > **Reisegodtgjørelse** > **Kategorioppsett**.

Når du har oppgradert til 10.0.18, og organisasjonen bruker utgiftskategorien for reisegodtgjørelse, bør du vurdere å aktivere reisegodtgjørelsefunksjonen etter å ha sett gjennom utformingsendringene nedenfor. 

Den nye utformingen for reisegodtgjørelsesnivåer har innvirkning på hvordan verdien i **Antall**-feltet behandles. Før utgivelsen av 10.0.18 ble verdien i **Antall**-feltet betraktet som den nedre grensen. Da akkumulering krysset denne verdien, ble den tilsvarende satsen brukt.  Fra og med 10.0.18 regnes verdien i **Antall**-feltet som øvre grense. Tilsvarende sats brukes når akkumulering av reisegodtgjørelse er mindre enn verdien i **Antall**-feltet.  Den nye modellen for reisegodtgjørelse bidrar med konsekvens på tvers av reisegodtgjørelsesnivå og bedre brukervennlighet.   

Alle godkjente utgiftsrapporter beregnes på nytt under postering i henhold til den nye utformingen.

## <a name="example"></a>Eksempel
 
### <a name="before-version-10018"></a>Før versjon 10.0.18
Med to reisegodtgjørelsesnivåer representerer **Antall**-feltet på hvert nivå den nedre reisegodtgjørelsesgrensen. For øyeblikket har nivå én verdien null (0) og en sats på 0,45, og nivå to har en verdi på 1 000 og en sats på 0,25. Hvis akkumulerte mil eller kilometer krysser verdien i feltet, brukes den relaterte satsen. Hvis det ikke finnes noen linje med null-antall, bruker systemet reisegodtgjørelsen som er definert i Utgiftsbehandling. 
 
Hvis en ansatt sender en utgiftsrapport på 1 500 engelske mil, vil de to reisegodtgjørelseslinjene i den posterte utgiftsrapporten være: 1000 (sats 0,45) + 500 (sats 0,25) = 575,00.

### <a name="after-version-10018"></a>Etter versjon 10.0.18
I 10.0.18 representerer **Antall**-feltet i hvert lag nivå den øvre grensen for nivået. For øyeblikket har nivå én verdien 999 og en sats på 0,45, og nivå to har en verdi på 999.999.999,00 og en sats på 0,25. Hvis akkumulerte mil eller kilometer krysser verdien i **Antall**-feltet, brukes den relaterte satsen. Hvis alle øvre grense overstiges, bruker systemet reisegodtgjørelsen som er definert i Utgiftsbehandling. 
 
For at samme scenario skal kunne beregnes riktig, må nivåoppsett endres. **Antall**-feltet på nivå én har verdien 999.00 og en verdi på 999,999,999.00 på nivå to. Hvis en ansatt overskrider det totale antallet mil eller kilometer på nivå 1, bruker systemet reisegodtgjørelsessatsen som er definert i Utgiftsbehandling. 
  
Hvis en ansatt sender en utgiftsrapport på 1 500 engelske mil, vil de to reisegodtgjørelseslinjene i den posterte utgiftsrapporten være: 1000 (sats 0,45) + 500 (sats 0,25) = 575

## <a name="enable-the-mileage-amount-calculation-for-multiple-mileage-tiers-with-same-rate-feature"></a>Aktivere funkjonen for beregningen av reisegodtgjørelsesbeløp for flere reisegodtgjørelsesnivåer med samme sats

Funksjonen for **beregningen av reisegodtgjørelsesbeløp for flere reisegodtgjørelsesnivåer med samme sats** forbedrer beregningen av reisegodtgjørelsessatsen. Fullfør fremgangsmåten nedenfor for å aktivere denne funksjonen.

1. Gå til **Arbeidsområder** > **Funksjonsbehandling**. 
2. Finn og velg **beregningen av reisegodtgjørelsesbeløp for flere reisegodtgjørelsesnivåer med samme sats**, og velg deretter **Aktiver nå**.

Når du har aktivert funksjonen, tilbakestiller du reisegodtgjørelsesnivåene, slik at de gjenspeiler verdien i **Antall**-feltet på riktig måte. 

## <a name="enable-the-mileage-totals-calculation-by-fiscal-year-feature"></a>Aktivere totalberegningen for reisegodtgjørelse med regnskapsårfunksjonen

Funksjonen for **totalberegning av reisegodtgjørelse etter regnskapsår** gir en ny innstilling i parametere for administrasjon av utgifter som utfører totalberegninger for kilometer per regnskapsår i stedet for kalenderåret. Fullfør fremgangsmåten nedenfor for å aktivere denne funksjonen.

1. Gå til **Arbeidsområder** > **Funksjonsbehandling**.
1. Finn og velg funksjonen for **totalberegning av av reisegodtgjørelse etter regnskapsår**, og velg deretter **Aktiver nå**.
1. Gå til **Utgiftshåndtering** > **Oppsett** > **Generelt** > **Parametere for utgiftshåndtering**.
1. På siden **Parametere for utgiftshåndtering** finner og aktiverere du **Bruk regnskapsår for totalberegning av av reisegodtgjørelse**.

Når du har aktivert **Bruk regnskapsår for totalberegning av av reisegodtgjørelse** kalkuleres kilometerlengde av regnskapsår.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
