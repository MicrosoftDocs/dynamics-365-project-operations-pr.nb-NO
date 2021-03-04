---
title: Konfigurere regnskap for fakturerbare prosjekter
description: Dette emnet gir informasjon om regnskapsalternativene for fakturerbare prosjekter.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131985"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurere regnskap for fakturerbare prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dynamics 365 Project Operations støtter forskjellige regnskapsalternativer for fakturerbare prosjekter som omfatter tid og materiale og transaksjoner med fast pris.

- **Tids- og materialtransaksjoner**: Disse transaksjonene faktureres etter hvert som arbeidet pågår, basert på forbruket av timer, utgifter, varer eller gebyrer på prosjektet. Disse transaksjonskostnadene kan sammenlignes med omsetningen for hver transaksjon, og prosjektet faktureres etter hvert som arbeidet pågår. Prosjektomsetningen kan også avsettes når transaksjonen inntreffer. Under fakturering gjenkjennes omsetningen, og påløpte inntekter tilbakeføres hvis aktuelt.
- **Fastpristransaksjoner**: Disse transaksjonene blir fakturert i henhold til en faktureringsplan som er basert på prosjektkontrakten. Omsetning for fastpristransaksjoner kan gjenkjennes ved fakturering, eller de kan beregnes og posteres regelmessig, i henhold til metodene **Fullført kontrakt** eller **Fullførte prosentandel**.

Et prosjekt anses som fakturerbart når det er knyttet til én eller flere kontraktlinjer. En prosjektkontraktlinje definerer for seg selv hvilke faktureringsmetoder og transaksjonstyper som er tillatt.

Som eksempel har Fabrikam Robotics vunnet en prosjektkontrakt med Adatum Corporation for å optimalisere utstyr. Adatum betaler et fast beløp på 10 000 USD for å dekke påløpte prosjektutgifter. Dette er en faktureringsmetode for fastpris. Prosjekttid og -avgifter blir fakturert per bruk. Dette er en faktureringsmetode for tid og material. Alt arbeid spores under ett prosjekt med navnet Adatum utstyrsoptimalisering.

Et prosjektteammedlem sender inn åtte timer arbeid på prosjektet Adatum utstyrsoptimalisering. Når prosjektlederen godkjenner denne tiden, bruker systemet faktureringsmetoden for tid og materiale til å opprette transaksjoner med faktiske verdier, en faktura og en konto. Denne transaksjonen tas ikke med i beregningen av fastprisomsetning.

Et annet prosjektteammedlem sender en reiseregning på 2000 USD mot prosjektet Adatum utstyrsoptimalisering. Når prosjektlederen godkjenner denne innsendelsen, bruker systemet en faktureringsmetode for fastpris til å opprette transaksjoner med faktiske verdier og en konto for denne prosjektutgiften. Kunden blir ikke fakturert basert på denne transaksjonen. I stedet faktureres de ved å bruke hver av de separat konfigurerte faktureringsmilepælene. Denne utgiftstransaksjonen, sammen med utgiftsestimatene, tas med i beregningen av fastprisomsetning.

Regnskapsprinsipper for prosjekttransaksjoner er definert i prosjektkostnads- og omsetningsprofiler. For hver prosjekttransaksjon fastsetter systemet riktig prosjektkostnads- og omsetningsprofil ved å bruke reglene for prosjektkostnads o g omsetningsprofiler som er konfigurert.

## <a name="define-project-cost-and-revenue-profiles"></a>Definere prosjektkostnads- og omsetningsprofiler 

Prosjektkostnads- og omsetningsprofiler fastsetter regnskapsreglene for prosjekttransaksjoner. Disse profilene konfigureres i prosjektledelsen og -regnskapet. 

Fullfør fremgangsmåten nedenfor for å opprette en ny prosjektkostnads- og omsetningsprofil. 

1. Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Bokføring** > **Prosjektkostnads- og omsetningsprofiler**. 
2. Velg **Ny** for å opprette en ny prosjektkostnads- og omsetningsprofil.
3. I **Navn**-feltet skriver du inn navnet og en kort beskrivelse av profilen.
4. I feltet **Faktureringsmetode** velger du **Tid og materiale** eller **Fast pris**.
5. Utvid hurtigfanen **Finans**. Feltene på denne fanen definerer regnskapsprinsippene som brukes når prosjekttransaksjoner blir journalført ved hjelp av Project Operations-integreringsjournalen, og som deretter faktureres via prosjektfakturaforslaget.
6. Velg den relevante informasjonen i følgende felt på hurtigfanen **Finans**:

    - **Poster kostnader – time**:

       - *Ingen hovedbok*: Kostnaden for tidstransaksjoner posteres ikke til hovedboken når Project Operations-integreringsjournalen posteres. Regnskapsføreren kan imidlertid bokføre kostnader ved hjelp av funksjonen Poster kostnader senere.
       - **Saldo**: Kostnaden for tidstransaksjonene debiteres til hovedbokkontotypen *VIA – kostverdi* og krediteres til *lønnstildelingskontoen* i posteringsoppsettet for hovedbok. Regnskapsføreren bruker funksjonen Poster kostnader til å flytte denne kostnaden fra en saldokonto til en konto for fortjeneste og tap regelmessig.
       - **Resultat**: Når det posteres til Project Operations-integreringsjournalen, debiteres kostnaden for tidstransaksjonen til kontotypen *Kostnad* i hovedboken og krediteres til *lønnstildelingskontoen* definert på **Kostnad**-fanen på siden **Finansposteringsoppsett** (**Prosjektstyring og regnskap** \> **Oppsett** \> **Bokføring** \> **Finansposteringsoppsett**). Dette er det vanligste oppsettet for tids- og materialtransaksjoner.
        - *Aldri hovedbok*: Kostnaden for tidstransaksjoner blir aldri postert til hovedboken.

    - **Poster kostnader – utgift**:

         - **Saldo**: Ved postering av Project Operations-integreringsjournalen debiteres kostnaden for utgiftstransaksjonen til kontotypen *VIA – kostverdi* i hovedboken, slik det er definert på **Kostnad**-fanen på siden **Finansposteringsoppsett**, og den krediteres mot forskyvningskontoen på journallinjen. Standard forskyvningskontoer for utgifter er definert under **Prosjektstyring og regnskap** > **Oppsett** \> **Bokføring** \> **Standard forskyvningskonto for utgifter**. Regnskapsføreren bruker funksjonen **Poster kostnader** til å flytte denne kostnaden fra denne saldokontoen til resultatkontoen regelmessig.
        - **Resultat**: Ved postering av Project Operations-integreringsjournalen debiteres kostnaden for utgiftstransaksjonen til kontotypen *Kostnad* i hovedboken, slik det er definert på **Kostnad**-fanen på siden **Finansposteringsoppsett**, og den krediteres mot forskyvningskontoen på journallinjen. Standard forskyvningskontoer for utgifter er definert under **Prosjektstyring og regnskap** \> **Oppsett** \> **Bokføring** \> **Standard forskyvningskonto for utgifter**.
       
    - **A konto fakturering**:

        - **Saldo**: Ved postering av prosjektfakturaforslaget blir en a konto-transaksjon (faktureringsmilepæl) kreditert til finanskontotypen *VIA fakturert – a konto*, slik det er definert i kategorien **Omsetning** på siden **Finansposteringsoppsett**, og debitert til kundesaldokontoen.
         - **Resultat**: Ved postering av prosjektfakturaforslaget blir en a konto-transaksjon (faktureringsmilepæl) kreditert til finanskontotypen *Fakturert omsetning – a konto*, slik det er definert i kategorien **Omsetning** på siden **Finansposteringsoppsett**, og debitert til kundesaldokontoen. Kundesaldokontoer defineres i **Utestående fordringer** \> **Oppsett** \> **Kundebokføringsprofiler**.

   Når du definerer posteringsprofilene for faktureringsmetoder for tid og materiale, har du mulighet til å avsette omsetning per transaksjonstype (time, utgift og gebyr). Hvis alternativet **Avsett inntekt** er satt til **Ja**, registreres ikke-fakturerte salgstransaksjoner i Project Operations-integreringsjournalen til hovedboken. Salgsverdien debiteres til **VIA – salgsverdikonto** og krediteres til kontoen **Påløpte inntekter – salgsverdi** som ble konfigurert på siden **Finansposteringsoppsett**, i kategorien **Omsetning**. 
  
  > [!NOTE]
  > Alternativet **Avsett omsetning** er bare tilgjengelig når den tilsvarende kostnaden for transaksjonstypen **Kostnad** er postert til resultatkontoen.
    
7. Utvid hurtigfanen **Estimat**. Feltene i denne kategorien definerer beregningsinnstillingene for estimater for fastprisomsetning. Feltene i denne kategorien gjelder bare for prosjektkostnads- og omsetningsprofiler med faktureringsmetoden **Fast pris**.
8. Velg den relevante informasjonen i følgende felt på hurtigfanen **Estimat**:

    - **Prinsippet som brukes til beregning av prosjektfullførelse**:

        - **Fullført kontrakt**: Kostnadssamsvar og inntektsføring skjer ikke før etter at prosjektet er fullført. Kostnader gjenspeies som VIA i saldoen til prosjektet er fullført.
        - **Fullførte prosentandel**: Påløpte inntekter blir beregnet og postert til hovedboken hver periode basert på fullføringsprosenten for prosjektet. Det finnes flere metoder som er tilgjengelige for å beregne fullføringsprosent. Disse metodene kan være automatiske, basert på konfigurasjonen, eller manuelle.
        - **Ingen VIA**: Dette oppsettet brukes til fastprisprosjekter med et kort tidsrom og der fakturaen og kostnadene forekommer i samme periode. I dette tilfellet settes verdien i feltet **A konto fakturering** på hurtigfanen **Hovedbok** automatisk til **Resultat** for å sikre at inntekt føres ved fakturering. Prosessen for beregning av omsetningen brukes ikke for denne prosjektkostnads- og omsetningsprofilen.

    - **Samsvarsprinsipp**: Dette feltet angir hvordan den beregnede salgsverdien (påløpte inntekter) skal posteres i hovedboken.

        - Ved hjelp av **Salgsverdi**-prinsippet beregner systemet salgsverdien ved å sammenligne kostnader og omsetning, og deretter bokføre den som et enkelt beløp.
        - Ved hjelp av prinsippet **Produksjon og fortjeneste** deler systemet opp salgsverdien i realiserte kostnader og beregnet fortjeneste. Disse posteres separat.

    - **Kostnadsmaler**: Tillat at prosjekttransaksjoner grupperes basert på transaksjonstype og prosjektkategori, og definer beregningsregler for fullføringsprosent for disse gruppene.
    - **Periodekoder**: Definer hyppigheten for beregning av omsetning for en bestemt prosjektkostnads- og omsetningsprofil.
    - **Kategorier for estimat**: Brukes for bokføring av salgsverdi (påløpt omsetning) til prosjekttransaksjoner. Først konfigurerer du den dedikerte prosjektkategorien for en **Gebyr**-transaksjonstype, og deretter angir du flagget **Estimat** for denne prosjektkategorien. Deretter, avhengig av valgt samsvarsprinsipp, velger du denne prosjektkategorien i feltet **Salgsverdi** eller **Fortjeneste** i prosjektkostnads- og omsetningsprofilen.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Eksempelkonfigurasjoner for prosjektkostnads- og omsetningsprofiler

Tid og materialer – ingen VIA

![Kostnads- og omsetningsprofil: Tid og materialer – ingen VIA](media/time-material-no-wip.png)

Tid og materialer – VIA (omsetning)

![Kostnads- og omsetningsprofil: Tid og materialer – VIA](media/time-material-with-wip.png)

Fast pris – ingen VIA

![Kostnads- og omsetningsprofil: Fast pris – ingen VIA](media/fixed-price-no-wip.png)

Fast pris – fullført kontrakt

![Kostnads- og omsetningsprofil: Fast pris – fullført kontrakt](media/fixed-price-completed-contract.png)

Fast pris – fullføringsprosent

![Kostnads- og omsetningsprofil: Fast pris – fullføringsprosent](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Eksempler på regnskapshendelser for prosjektkostnads- og omsetningsprofiler.

| Regnskapshendelse                  | Tid og materiale – ingen VIA                       | Tid og materiale – VIA                                                                                           | Fast pris – ingen VIA                                            | Fast pris – fullført kontrakt                                                                            | Fast pris – fullføringsprosent                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Journalføre tidstransaksjoner    | Debet – kostnad <br>Kredit – lønnstildeling          | Debet – kostnad <br>Kredit – lønnstildeling <br>Debet – VIA-salgsverdi <br>Kredit – Salgsverdi for påløpt omsetning                | Debet – kostnad <br>Kredit – lønnstildeling                         | Debet – kostnad <br>Kredit – lønnstildeling                                                                    | Debet – kostnad <br>Kredit – lønnstildeling                       |
| Journalføre utgiftstransaksjoner | Debet – kostnad <br>Kredit – forskyvningskonto for utgift | Debet – kostnad <br>Kredit – forskyvningskonto for utgift <br>Debet – VIA-salgsverdi <br>Kredit – Salgsverdi for påløpt omsetning      | Debet – kostnad <br>Kredit – forskyvningskonto for utgift                 | Debet – kostnad<br> Kredit – forskyvningskonto for utgift                                                            | Debet – kostnad <br>Kredit – forskyvningskonto for utgift               |
| Fakturere kunde                | Debet – kundesaldo <br>Kredit – fakturert omsetning | Debet – kundesaldo <br>Kredit – fakturert omsetning <br>Kredit – debet for VIA-salgsverdi – Salgsverdi for påløpt omsetning | Debet – kundesaldo <br>Kredit – Fakturert omsetning – a konto | Debet – kundesaldo <br>Kredit – VIA – Fakturert a konto                                                  | Debet – kundesaldo <br>Kredit – VIA – Fakturert a konto    |
| Bokfør omsetningsestimat             | Ikke aktuelt                                   | Ikke aktuelt                                                                                                    | Ikke aktuelt                                                  | Debet – VIA-kostnadsverdi <br>Kredit – Kostnad                                                                         | Debet – VIA – Salgsverdi <br>Kredit – Salgsverdi for påløpt omsetning |
| Eliminere                         | Ikke aktuelt                                   | Ikke aktuelt                                                                                                    | Ikke aktuelt                                                  | Kredit – VIA-kostnadsverdi <br>Debet – kostnad <br>Kredit – Påløpt omsetning – Salgsverdi <br>Debet – VIA fakturert a konto | Debet – VIA – fakturert a konto <br>Kredit – VIA-salgsverdi     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurere regler for prosjektkostnads- og omsetningsprofil

Regler for prosjektkostnads- og omsetningsprofiler avgjør prosjektkostnads- og omsetningsprofilen som må brukes ved behandling av eventuelle fakturerbare prosjekttransaksjoner. Definer reglene ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Bokføring** \> **Regler for prosjektkostnads- og omsetningsprofiler**.

Regler kan defineres av prosjektkontrakten, prosjektgruppen eller etter et bestemt prosjekt. Systemet vil alltid velge regelen med høyeste detaljnivå først.


[!INCLUDE[footer-include](../includes/footer-banner.md)]