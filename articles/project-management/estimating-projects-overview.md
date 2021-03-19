---
title: Oversikt over estimatprosjekter
description: Dette emnet inneholder informasjon om estimater i Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4ff73c6efd5b21b91a7772c3733734d8008e00a3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286890"
---
# <a name="estimate-projects-overview"></a>Oversikt over estimatprosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I et prosjektbasert tilbud kan du bruke enheten for **tilbudslinjedetalj** til å estimere arbeidet som kreves for å levere et prosjekt. Deretter kan du dele dette estimatet med kunden.

Prosjektbaserte tilbudslinjer kan ha fra null til mange tilbudslinjedetaljer. Tilbudslinjedetaljer brukes til å beregne tid, utgifter eller gebyrer. Microsoft Dynamics 365 Project Operations tillater ikke materialestimater i tilbudslinjedetaljer. Disse kalles transaksjonsklasser. Estimerte avgiftsbeløp kan også angis i en transaksjonsklasse.

I tillegg til transaksjonsklasser har tilbudslinjedetaljer en transaksjonstype. To transaksjonstyper støttes for tilbudslinjedetaljer: **Kostnad** og **Prosjektkontrakt**.

## <a name="estimate-by-using-a-contract"></a>Beregne ved hjelp av en kontrakt

Hvis du brukte et tilbud da du opprettet en prosjektbasert kontrakt, kopieres estimatet du har utført for hver tilbudslinje i tilbudet, til prosjektkontrakten. Strukturen i en prosjektkontrakt er lik strukturen i prosjekttilbudet som har linjer, linjedetaljer og fakturaplaner.

Estimater kan utføres direkte i en prosjektkontrakt, som i et prosjekttilbud. For et prosjekttilbud utføres estimatet ved hjelp av kontraktlinjer og kontraktlinjedetaljer. Kontraktlinjedetaljer kan også genereres fra en prosjektplan som ble opprettet ved hjelp estimatmetoden nedenfra og opp.

Kontraktslinjedetaljer kan brukes til å beregne tid, utgifter eller gebyrer. Estimerte avgiftsbeløp kan også angis i en kontraktslinjedetalj.

Materialestimater tillates ikke i kontraktslinjedetaljer.

Prosessene som støttes i en prosjektkontrakt, er fakturaopprettelse og -bekreftelse. Fakturaopprettelse oppretter et utkast av en prosjektbasert faktura som inkluderer alle faktiske beløp for fakturaer som ikke er fakturert, frem til gjeldende dato.

Bekreftelsen gjør kontrakten skrivebeskyttet og endrer statusen fra **Utkast** til **Bekreftet**. Når du har utført denne handlingen, kan du ikke angre den. Ettersom denne handlingen er permanent, er det best å holde kontrakten i en **Utkast**-status.

De eneste forskjellene mellom kontraktutkast og bekreftede kontrakter er statusen og det faktum at kontraktutkast kan redigeres, mens bekreftede kontrakter ikke kan dette. Du kan utføre både fakturaopprettelse og sporing av faktiske verdier både i kontraktutkast og bekreftede kontrakter.

Project Operations støtter ikke endringsordrer i kontrakter eller prosjekter.

## <a name="estimating-projects"></a>Estimere prosjekter

Du kan estimere tid og utgifter på prosjekter. Project Operations tillater ikke estimater av materialer eller gebyrer på prosjekter.

Tidsestimater genereres når du oppretter en oppgave og identifiserer attributtene for en generisk ressurs som kreves for å utføre oppgaven. Tidsestimater genereres fra planlagte oppgaver. Tidsestimater opprettes ikke hvis du oppretter generiske teammedlemmer utenfor konteksten i tidsplanen.

Utgiftsestimater angis i rutenettet på **Estimater**-siden.

## <a name="understanding-estimation"></a>Forstå estimering

Bruk tabellen nedenfor som veiledning for å forstå forretningslogikken i estimeringsfasen.

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