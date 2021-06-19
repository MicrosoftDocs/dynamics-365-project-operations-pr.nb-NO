---
title: Konsepter for økonomisk estimat
description: Dette emnet inneholder informasjon om økonomisk estimat for prosjekter i Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 488b61ee1e81aac47fa92fff141f17b023e4f1c0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002608"
---
# <a name="financial-estimation-concepts"></a>Konsepter for økonomisk estimat

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations kan du økonomisk estimere prosjektene i to faser: 
1. I fasen før salg før avtalen blir vunnet. 
2. Under utførelsesfasen etter at prosjektkontrakten er opprettet. 

Du kan opprette et økonomisk estimat for prosjektbasert arbeid på følgende tre sider:
- **Tilbudslinje**-siden, ved å bruke tilbudslinjedetaljene.  
- **Prosjektkontraktlinje**-siden, ved å bruke kontraktlinjedetaljene. 
- **Prosjekt**-siden, ved å bruke fanene **Oppgaver** eller **Utgiftsestimater**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Bruk et prosjekttilbud til å opprette et estimat
I et prosjektbasert tilbud kan du bruke enheten for **tilbudslinjedetalj** til å estimere arbeidet som kreves for å levere et prosjekt. Deretter kan du dele dette estimatet med kunden.

Prosjektbaserte tilbudslinjer kan ha fra null til mange tilbudslinjedetaljer. Tilbudslinjedetaljer brukes til å beregne tid, utgifter eller gebyrer. Microsoft Dynamics 365 Project Operations tillater ikke materialestimater i tilbudslinjedetaljer. Disse kalles transaksjonsklasser. Estimerte avgiftsbeløp kan også angis i en transaksjonsklasse.

I tillegg til transaksjonsklasser har tilbudslinjedetaljer en transaksjonstype. To transaksjonstyper støttes for tilbudslinjedetaljer: **Kostnad** og **Prosjektkontrakt**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Bruk et kontrakttilbud til å opprette et estimat

Hvis du brukte et tilbud da du opprettet en prosjektbasert kontrakt, kopieres estimatet du har utført for hver tilbudslinje i tilbudet, til prosjektkontrakten. Strukturen i en prosjektkontrakt er lik strukturen i prosjekttilbudet som har linjer, linjedetaljer og fakturaplaner.

Estimater kan utføres direkte i en prosjektkontrakt, som i et prosjekttilbud. For et prosjekttilbud utføres estimatet ved hjelp av kontraktlinjer og kontraktlinjedetaljer. Kontraktlinjedetaljer kan også genereres fra en prosjektplan som ble opprettet ved hjelp estimatmetoden nedenfra og opp.

Kontraktslinjedetaljer kan brukes til å beregne tid, utgifter eller gebyrer. Estimerte avgiftsbeløp kan også angis i en kontraktslinjedetalj.

Materialestimater tillates ikke i kontraktslinjedetaljer.

## <a name="use-a-project-to-create-an-estimate"></a>Bruk et prosjekt til å opprette et estimat 

Du kan estimere tid og utgifter på prosjekter. Project Operations støtter ikke estimater av materiell eller gebyrer for prosjekter.

Tidsestimater genereres når du oppretter en oppgave og identifiserer attributtene for en generisk ressurs som kreves for å utføre oppgaven. Tidsestimater genereres fra planlagte oppgaver. Tidsestimater opprettes ikke hvis du oppretter generiske teammedlemmer utenfor konteksten i tidsplanen.

Utgiftsestimater angis i rutenettet på **Utgiftsestimater**-siden.

Det å opprette et estimat for et prosjekt anses som en god fremgangsmåte, fordi du kan bygge detaljerte estimater for arbeid eller tid og utgifter for hver oppgave i prosjektplanen. Du kan deretter bruke dette detaljerte estimatet til å opprette estimater for hver tilbudslinje og bygge et mer troverdig tilbud for kunden. Når du importerer eller oppretter et detaljert estimat på tilbudslinjen ved hjelp av prosjektplanen, importerer Project Operations salgsverdiene og kostnadsverdiene for disse estimatene. Etter importen kan du vise lønnsomhet, marginer og metrikkverdier for gjennomførbarhet i prosjekttilbudet.

## <a name="understanding-estimates"></a>Forstå estimater

Bruk tabellen nedenfor som veiledning for å forstå forretningslogikken i estimatfasen.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Enhetsoppføring                                                                                                                                                                                                       | Transaksjonstype | Transaksjonsklasse | Tilleggsinformasjon                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Når du har behov for å beregne salgsverdien for tid i et tilbud                                                                                                                                                                                                                                                                                    | En oppføring for tilbudslinjedetalj opprettes                                                                                                                                                                               | Prosjektkontrakt | Time        | Transaksjonsopprinnelse-feltet på raden med tilbudslinjedetaljer på salgssiden refererer til raden med tilbudslinjedetaljer på kostnadssiden |
|                                                                                                                                                                                                                                                                                     | Systemet oppretter en andre oppføring av raden med tilbudslinjedetaljer for å lagre de tilsvarende kostnadsverdiene. Alle felt som ikke har pengeverdier, kopieres fra raden med tilbudslinjedetaljer for salg til kostnadsraden.                                                                                                                                                                               | Kostnad | Time        | Transaksjonsopprinnelse-feltet på raden med tilbudslinjedetaljer på salgssiden refererer til raden med tilbudslinjedetaljer på kostnadssiden |
| Når du har behov for å beregne salgsverdien for tid i en kontrakt                                                                                                                                                                                                                                                                                 | En oppføring for prosjektlinjedetalj (PLD) opprettes                                                                                                                                                                    | Prosjektkontrakt | Time        | Transaksjonsopprinnelse-feltet på PLD-raden på salgssiden refererer til PLD-raden på kostnadssiden      |
|                                                                                                                                                                                                                                                                                  | Systemet oppretter en andre PLD-oppføring for å lagre de tilsvarende kostnadsverdiene. Alle felt som ikke har pengeverdier, kopieres fra CLD-salgsraden til CLD-kostnadsraden.                                                                                                                                                                    | Kostnad | Time        | Transaksjonsopprinnelse-feltet på PLD-raden på salgssiden refererer til PLD-raden på kostnadssiden      |
| Når en bruker beskriver en ressurs i en prosjektoppgave                                                                                                                                                                                                                                                                                            | En estimatlinjeoppføring som viser salgsverdien for oppgaven, opprettes når en oppgave opprettes med alle obligatoriske prisdimensjoner. Rolle- og organisasjonsenheter er prisdimensjoner | Prosjektkontrakt | Tid        |                                                                                   |
|     | Estimatlinjeoppføringen som viser kostverdien for oppgaven, opprettes når en oppgave opprettes med alle obligatoriske prisdimensjoner. Alle felt som ikke har pengeverdier, kopieres fra salgsestimatlinjen til kostestimatlinjen. Rolle- og organisasjonsenheten er prisdimensjoner både for kostnads- og fakturasatser.                                                                                                                                                                                                                | Kostnad             | Tid           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Tilpasse enhetene for tilbudslinjedetaljer og kontraktlinjedetaljer

Hvis du har lagt til et egendefinert felt i tilbudslinjedetaljene og vil at systemet skal angi verdien i feltet som en standardverdi på den relaterte kostnadslinjen som opprettes, bruker du registreringsverktøyene **PreOperationContractLineDetailUpdate** og **PreOperationQuoteLineDetailUpdate**. Disse plugin-modulene må registreres på nytt etter at tilbudslinjedetaljene eller kontraktslinjedetaljene endres. Følg disse trinnene for å fullføre prosessen.

1. Åpne PluginRegistrationTool, og koble til forekomsten på nettet.
2. Velg **Søk**, og søk etter plugin-modulen for å oppdatere.
3. Velg plugin-modulen, og velg deretter **Velg** på hovedsiden.
4. Velg trinnet i plugin-modulen som skal oppdateres, høyreklikk, og velg deretter **Oppdater**.
5. I dialogboksen **Oppdater eksisterende trinn**, i feltet **Filtreringsattributter** velger du ellipseknappen (**...**):
6. I dialogboksen **Velg attributter** merker du av i boksene for egendefinerte attributter.
7. Velg **OK** for å lukke dialogboksen, og velg deretter **Oppdater trinn**.
8. Gjenta trinn 1 til 7 for den andre plugin-modulen.
9. Lukk **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
