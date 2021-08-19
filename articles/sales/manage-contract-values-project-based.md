---
title: Arbeide med prosjektbaserte kontraktlinjer
description: Dette emnet inneholder informasjon om prosjektbaserte kontraktlinjer.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990058"
---
# <a name="work-with-projectbased-contract-lines"></a>Arbeide med prosjektbaserte kontraktlinjer

Prosjektbaserte kontraktlinjer i Dynamics 365 Project Operations er utformet for å inneholde estimat- og faktureringsavtaler for bestemte komponenter av prosjektarbeid for et engasjement. Strukturen til en prosjektbasert kontraktlinje utvides for prosjektestimater og faktureringsscenarioer med følgende konsepter:

- Faktureringsmetode
- Prosjekt- og oppgavetilordning
- Inkluderte transaksjonsklasser
- Må ikke overskrides-grense
- Belastbarhets-oppsett
- Estimater ved hjelp av kontraktlinjedetaljer
- Kontraktlinjekunder

Følgende felt er inkludert i **Generelt**-kategorien i prosjektbaserte kontraktlinjer. Disse feltene hjelper deg med å definere grunnlaget for et detaljert estimat fra grunnen av og faktureringsordninger for prosjektbasert arbeid.

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| **Navn** | Navnet på kontraktlinjen som identifiserer den separate komponenten i kontrakten som blir estimert. For en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra en tilsvarende verdi av den prosjektbaserte tilbudslinjen. | Denne feltverdien kopieres til prosjektfakturalinjen som opprettes fra denne kontraktlinjen når fakturaen opprettes. |
| **Faktureringsmetode** | På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen. Dette er et alternativsett som representerer de to hovedkontraktmodellene som støttes av Project Operations:</br>- **Fast pris**</br>- **Tid og materiale** | Basert på faktureringsmetoden for den refererte kontraktlinjen blir den faktiske transaksjonen behandlet. Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for tid og materialer, opprettes det en post for kostnader og ufakturert faktisk salgsverdi. Hvis kontraktlinjen som den faktiske verdien refererer til, har en faktureringsmetode for fast pris, blir bare en faktisk kostnad opprettet. |
| **Project** | Bruk dette feltet til å identifisere prosjektet som skal brukes til å levere arbeidet på dette engasjementet. | Verdien i dette feltet brukes sammen med feltene **Inkluderte oppgaver** og **Inkluderte transaksjonsklasser** for å løse kontraktlinjereferansen på en faktisk eller beregnet linjeoppføring. |
| **Inkluder tid** | Et flagg angir om tidstransaksjoner eller arbeidskraftkostnader på det valgte prosjektet er inkludert på denne kontraktlinjen. En **Nei**-verdi angir at tidstransaksjonene eller arbeidskostnadene ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at de tas med. | Denne feltverdien brukes sammen med prosjektet for å løse kontraktlinjereferansen på en faktisk eller beregnet linjeoppføring. |
| **Inkluder utgift** | Et flagg angir om utgiftskostnadene på det valgte prosjektet inkluderes på denne kontraktlinjen. En **Nei**-verdi angir at utgiftskostnaden ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at den tas med. | Denne feltverdien brukes sammen med prosjektet for å løse kontraktlinjereferansen på en faktisk eller beregnet linjeoppføring. |
| **Inkluder gebyr** | Et flagg angir om avgiftene på det valgte prosjektet inkluderes på denne kontraktlinjen. En **Nei**-verdi angir at avgiftene ikke skal tas med på denne kontraktlinjen. En **Ja**-verdi angir at de tas med. | Denne feltverdien brukes sammen med prosjektet for å løse kontraktlinjereferansen på en faktisk eller beregnet linjeoppføring. |
| **Avtalt beløp** | På en kontraktlinje med fast pris er dette den avtalte verdien som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen. På en kontraktlinje for tid og materialer er dette beløpet en estimert verdi av hva som skal faktureres til kunden for alle arbeidskomponentene som er tilknyttet denne kontraktlinjen. På en prosjektkontrakt som opprettes fra et tilbud, kopieres denne verdien fra det tilsvarende feltet på tilbudslinjen. Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra beløpet på kontraktlinjedetaljene. | Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre beløpene i linjedetaljene. På en fastpriskontraktlinje brukes denne verdien til å generere beløpet før avgift på periodiske faktureringsmilepæler. |
| **Beregnet mva** | Brukeren kan redigere dette feltet for å angi det estimerte avgiftsbeløpet på kontraktlinjen. Når en prosjektbasert kontraktlinje har linjedetaljer, er dette feltet låst for redigering og oppsummeres fra avgiftsbeløpet på kontraktlinjedetaljene. | Når kontraktlinjen har linjedetaljer, kan denne verdien endres ved å endre avgiftsbeløpene i linjedetaljene. På en fastpriskontraktlinje brukes denne verdien til å generere avgift på periodiske faktureringsmilepæler. |
| **Avtalt beløp etter mva** | Kontraktlinjebeløpet etter mva. Dette feltet er skrivebeskyttet og beregnes som **Avtalt beløp + avgift**. | På en fastpriskontraktlinje brukes denne verdien til å generere periodiske faktureringsmilepæler. |
| **Må ikke overskrides-grense** | Brukeren kan redigere dette feltet, og det er bare tilgjengelig i prosjektbaserte kontraktlinjer som har faktureringsmetode for tid og materialer. | Brukeren kan redigere dette feltet. Når en faktisk verdi for tid og utgifter refererer til denne kontraktlinjen for tid og materiale, evalueres beløpet på den faktiske verdien mot grensen som ikke må overskrides, på denne kontraktlinjen, etter at det er tatt høyde for de allerede brukte og forpliktede beløpene. |
| **Kundebudsjett** | Dette feltet er redigerbart og kopieres fra det tilsvarende feltet på tilbudslinjen, hvis kontrakten ble opprettet fra et tilbud. | Dette feltet brukes bare til informasjon og har ikke noen nedstrøms signifikans. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Valideringsregel for alternativene i kategorien Generelt for prosjektbaserte kontraktlinjer

Regel: Et prosjekt og en bestemt transaksjonsklasse kan bare tas med på én prosjektbasert kontraktlinje i en kontrakt.

| Kontrakt | Kontraktlinje | Project | Inkluder tid | Inkluder utgift | Inkluder avgift | Gyldig / ikke gyldig | Årsak                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Bryter regelen. Tidspunkt, utgift og gebyrer på prosjekt P1 er inkludert i både kontraktlinjer, CL1 og CL2.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Bryter regelen. Tidspunkt, utgift og gebyrer på prosjekt P1 er inkludert i både kontraktlinjer, CL1 og CL2.                                                                                       |
| C1       | CL1           | P1      | Ja          | No              | Ja         | Ikke gyldig       | Bryter regelen. Tid og avgifter på prosjekt P1 er inkludert i både kontraktlinjer, CL1 og CL2.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Bryter regelen. Tid og avgifter på prosjekt P1 er inkludert i både kontraktlinjer, CL1 og CL2.                                                                                                   |
| C1       | CL1           | P1      | Ja          | No              | Ja         | Gyldig           | Tid og gebyrer på prosjekt P1 er inkludert på CL1. Utgift på prosjekt P1 er inkludert på CL2. </br>   Det er ingen overlapping i hva som inkluderes på hver enkelt kontraktlinje og derfor er gyldig.  |
| C1       | CL2           | P1      | No           | Ja             | No          | Gyldig           | Tid og gebyrer på prosjekt P1 er inkludert på CL1. Utgift på prosjekt P1 er inkludert på CL2. </br>   Det er ingen overlapping i hva som inkluderes på hver enkelt kontraktlinje og derfor er gyldig.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Bryter regelen. Tid, utgift og gebyrer på prosjekt P1 er inkludert på linjene for to kontrakter.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Ikke gyldig       | Bryter regelen. Tid, utgift og gebyrer på prosjekt P1 er inkludert på linjene for to kontrakter.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]