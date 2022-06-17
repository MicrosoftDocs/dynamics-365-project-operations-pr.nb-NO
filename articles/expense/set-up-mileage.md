---
title: Angi reisegodtgjørelse ved hjelp av kjørelengdenivåer
description: Denne artikkelen inneholder informasjon om kilometersatser og reisegodtgjørelsesnivåer.
author: suvaidya
ms.date: 05/20/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 03ca18c8fef6228f2ba553ebe50447beda5a857c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930146"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
