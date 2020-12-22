---
title: Opprette konserninterne transaksjoner
description: Dette emnet gir informasjon om hvordan du oppretter konserninterne transaksjoner.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a9d34d69ff59f0cb470bb852d8a80ecaedf6544
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595525"
---
# <a name="create-intercompany-transactions"></a>Opprette konserninterne transaksjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Konserninterne transaksjoner er tid- og utgiftstransaksjoner fra en prosjektkontrakt som tilhører et firma eller en organisasjonsenhet, mens ressursene på prosjektkontrakten er en del av et annet firma eller en annen organisasjonsenhet.

Når en konsernintern transaksjon godkjennes, opprettes de følgende faktiske transaksjonene

| **Transaksjonstype** | **Anvendt prisliste** | **Transaksjonsvaluta** |
| --- | --- | --- |
| Kostnad | Prisliste for kontraktens produksjonspris per enhet | Valuta på prislinjen |
| Ufakturerte salg. Disse opprettes bare for faktiske verdier som er knyttet til en kontraktlinje med faktureringstype, klokkeslett og materiell. | Salgsprisliste for kontraktprosjekt | Kontraktvaluta |
| Kostnad for ressursenhet | Kostprisliste for ressursenhet | Valuta på prislinjen |
| Salg mellom organisasjonsenheter | Prisliste for kontraktens produksjonspris per enhet | Valuta på prislinjen |

Kostnader, ressursens enhetskostnad og enhetssalgtransaksjonspriser og valuta mellom organisasjoner styres av **Organisasjonsenhet**. Dette er viktig å huske når du bestemmer deg for hvordan du vil strukturere selskaper og organisasjonsenheter i implementeringen.

Når du oppretter salgsmulighets-, tilbuds-, prosjektkontrakt- og prosjektoppføringer, kontrollerer systemet at valutaen for kontraktenheten samsvarer med kontraktfirmaets regnskapsvaluta. Når de ikke er de samme, kan ikke disse oppføringene opprettes. Valutaen for organisasjonsenheten defineres i Dynamics 365 Project Operations ved å gå til **Dataverse** > **Innstillinger** > **Organisasjonsenheter**. Regnskapsvalutaen for et firma defineres i Dynamics 365 Finance ved å gå til **Økonomimodul** > **Finansoppsett** > **Finans**. Valutaen synkroniseres i Dataverse-miljøet ved hjelp av dobbel skriving-tilordning i finans.

Systemet oppretter leverandørenhetskostnader og faktiske verdier for organisasjons enhetssalg i følgende situasjoner:

  - Når ressursenheten er forskjellig fra kontraktenheten
  - Når ressursfirmaet er forskjellig fra kontraktfirmaet

Bare transaksjoner som har et annet ressursfirma enn kontraktfirmaet, blir imidlertid overført til Dynamics 365 Finance-miljøet for ytterligere regnskapsføring.

Regnskap for faktiske verdier for prosjekter registreres i Project Operations-integreringsjournalen i Finance. Systemet oppretter følgende journallinjer:

| **Transaksjonstype** | **Juridisk enhet** | **Oppretter prosjekttransaksjon ved postering** | **Standardverdier for finansdimensjoner fra** | **Standard Mva-gruppe for fakturering og Mva-gruppe for faktureringselement** |
| --- | --- | --- | --- | --- |
| Kostnad | Blir ikke lagt til i integreringsjournalen | Ikke tilgjengelig | Ikke tilgjengelig | Ikke tilgjengelig |
| Ufakturert salg | Integreringsjournal for den juridiske enheten som låner | Ja | Project | **Mva-gruppe for fakturering**: Basert på **kontraktkunden** <br/> **Mva-gruppe for faktureringselement**: Fra prosjektkategorien for den gjeldende juridiske enheten på journallinjen |
| Kostnad for ressursenhet | Integreringsjournal for den juridiske enheten som låner ut | No | Konsernintern kunde | **Mva-gruppe for fakturering**: Basert på den **konserninterne kunden** <br/> **Mva-gruppe for faktureringselement**: Fra prosjektkategorien for den gjeldende juridiske enheten på journallinjen |
| Salg mellom organisasjoner | Integreringsjournal for den juridiske enheten som låner ut | No | Konsernintern kunde | **Mva-gruppe for fakturering**: Basert på den **konserninterne kunden** <br/> **Mva-gruppe for faktureringselement**: Fra prosjektkategorien for den gjeldende juridiske enheten på journallinjen |

### <a name="example-intercompany-transactions"></a>Eksempel: konserninterne transaksjoner

Anna Pilskog, en utvikler som er ansatt i GBPM, fører opp 10 timer med arbeid mot et USPM Brusefoss industrier-prosjekt, som er godkjent av prosjektlederen. Utviklerkostnad i GBPM er 88 GBP per time. GBPM vil fakturere USPM 120 USD per utviklertime. USPM vil fakturere kunden, Brusefoss industrier, 200 USD for arbeid som er gjort av GBPM-ressursen. Hvis du vil ha mer informasjon, kan du se [Konfigurere konsernintern fakturering](configure-intercompany-invoicing.md).

1. Gå til **Ressurser** i Project Operations og velg **Anna Pilskog** fra listen. På **Planlegging**-fanen i **Bedrift**-feltet selger du **GBPM**.
2. Gå til **Salg** > **Kunder** og velg **Ny** for å opprette en ny kundeoppføring for Brusefoss industrier.
    1. Angi firma til **USPM**.
    2. Angi **Relasjonstype** til **Kunde**.
    3. Velg **Kundegruppe 10 – innenlands**.
    4. Angi valuta til **USD**.
    5. Lagre oppføringen.
3. Gå til **Salg** > **Prosjektkontrakter** og opprett en ny prosjektkontrakt for Brusefoss industrier.
    1. Angi eierfirmaet til **USPM** og kontraktsenheten til **Contoso Robotics US**.
    2. Velg Brusefoss industrier som kunden.
    3. Velg en produktprisliste, og lagre oppføringen.
    4. På **Kontraktlinjer**-fanen oppretter du en ny kontraktlinje. Angi hvilket som helst navn, og velg **Tid og materialer** som faktureringsmetoden.
    5. Opprett et nytt prosjekt, og knytt det til denne kontraktlinjen.
4. Logg på som ressursen **Anna Pilskog**. Gå til **Prosjekter** > **Tidsoppføringer**, og opprett en tidsoppføring for Brusefoss industrier-prosjektet.
5. Logg på som prosjektlederen. Gå til **Prosjekter** > **Godkjenninger**, og godkjenn tidsoppføringstransaksjonen som ble logget av Anna Pilskog.
6. Naviger til Brusefoss industri-prosjektet, og velg **Relaterte** > **Faktiske data**. De faktiske transaksjonene som vises nedenfor, blir opprettet.

| **Transaksjonstype** | **Pris** | **Transaksjonsvaluta** | **Beløp** |
| --- | --- | --- | --- |
| Kostnad | 120 | USD | 1200 |
| Ufakturert salg | 200 | USD | 2000 |
| Kostnad for ressursenhet | 88 | GBP | 880 |
| Salgsenheter mellom organisasjoner | 120 | USD | 1200 |

7. Logg på som en USPM-regnskapsfører. Åpne Finance-forekomsten av Project Operations, og velg firmaet **USPM**. 
8. Gå til **Prosjektstying og regnskap** > **Periodisk** > **Project Operations på Customer Engagement** > **Importer fra oppsamling**, og velg for å kjøre den periodiske prosessen. Denne periodiske prosessen fyller inn integreringsjournal for Project Operations.
9. Gå til **Prosjektstyring og regnskap** > **Journaler** > **Integreringsjournal for Project Operations** og gjennomgå journallinjene. Systemet oppretter følgende linje:

    | **Transaksjonstype** | **Pris** | **Transaksjonsvaluta** | **Beløp** |
    | --- | --- | --- | --- |
    | Ufakturert salg | 200 | USD | 2000 |

    Hvis systemet er konfigurert til å avsette inntekt for dette prosjektet, blir følgende postert:

    - Debet: Prosjekt – VIA-salgsverdi 200 USD
    - Kredit: Prosjekt – påløpte inntekter 200 USD

    Dette ufakturerte salget er nå klart for fakturering. Fakturaen for kunden Brusefoss industrier kan bokføres finansielt når det er nødvendig.

10. Logg på som **GBPM**-regnskapsføreren. Åpne Finance-forekomsten av Project Operations, og åpne firmaet **GBPM**. 
11. Gå til **Prosjektstying og regnskap** > **Periodisk** > **Project Operations på Customer Engagement** > **Importer fra oppsamling**, og kjør den periodiske prosessen for å fylle inn integreringsjournalen for Project Operations.
12. Gå til **Prosjektstyring og regnskap** > **Journaler** > **Integreringsjournal for Project Operations** og gjennomgå linjene. Systemet oppretter følgende linjer.

    | **Transaksjonstype** | **Pris** | **Transaksjonsvaluta** | **Beløp** |
    | --- | --- | --- | --- |
    | Kostnad for ressursenhet | 88 | GBP | 880 |
    | Salgsenheter mellom organisasjoner | 120 | USD | 1200 |

    Hvis du posterer disse oppføringene, fører dette til følgende bilagstransaksjoner:

    - Debet: Prosjektkostnad 88 GBP
    - Kredit: lønnsfordeling 88 GBP

    Hvis systemet er konfigurert til å avsette konserninterne inntekter, blir følgende postert:

    - Debet: Prosjekt – VIA-salgsverdi 120 USD
    - Kredit: Prosjekt – påløpte inntekter 120 USD

    Systemet er nå klart til å opprette en konsernintern kundefaktura.
