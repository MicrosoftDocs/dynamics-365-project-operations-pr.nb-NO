---
title: Nyheter desember 2020 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Dette emnet gir informasjon om kvalitetsoppdateringene som er tilgjengelige i desember 2020-versjonen av Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f5927a638fe8e454aecc9ce8dfc0871ed51d09f5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291946"
---
# <a name="whats-new-december-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter desember 2020 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

- Project Operations på Dataverse-miljø versjon 4.5.0.134
- Prosjektstyring og regnskap i Dynamics 365 Finance-miljø versjon 10.0.15

Hvis du vil ha mer informasjon om hvordan du oppdaterer denne utgivelsen, kan du se [Oppdatere Project Operations i Økonomi-miljøet](ur5-nonstocked-installation.md).

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen
Følgende funksjoner er inkludert i denne versjonen:

  - [Konsernintern fakturering](../project-accounting/intercompany-invoicing-overview.md) 
  - [Kundeforskudd og honorarer](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Oppdateringer til Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet                    | Referansenummer | Kvalitetsoppdatering                                                                                                                                               |
|---------------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fakturering og prising             | 1986009          | Manuelt opprettede journallinjer har inkonsekvent ytelse når bekreftet før prosjekter er koblet til eller koblet fra en kontraktlinje                     |
| Fakturering og prising             | 2028174          | Oppdateringer for fakturalinjedetaljer må følge logikken i korrigeringsjournalen                                                                                  |
| Fakturering og prising             | 2028315          | Rettinger av redigerbar nestet rutenettvirkemåte                                                                                                                        |
| Fakturering og prising             | 2031070          | Justering av korrektiv fakturalinjedetalj må følge logikken i korrigeringsjournalen                                                                              |
| Fakturering og prising             | 2034186          | Du må kunne oppdatere et prosjekt på en kontraktlinje                                                                                                        |
| Fakturering og prising             | 2034206          | Det må angis en justeringsstatus under faktisk tilbakeføring under oppheving av kobling til et prosjekt fra en kontraktlinje                                                        |
| Fakturering og prising             | 2040871          | Tillat oppdatering av enhet og enhetsgruppe i Utgiftsestimat-rutenettet                                                                                       |
| Fakturering og prising             | 2053754          | Faktiske verdier som opprettes fra fakturaredigeringer, er ikke merket med justeringsstatus og faktureringsstatus                                                                |
| Fakturering og prising             | 2057874          | Korriger transaksjonstilkobling opprettet under redigering av fakturalinjedetalj                                                                                     |
| Fakturering og prising             | 2057875          | Korriger transaksjonsopprinnelser opprettet under redigering av fakturalinjedetalj                                                                                        |
| Fakturering og prising           | 2057944          | Må-ikke-overstige-tilstand angitt som Dedikert for faktiske verdier som ikke er klare for fakturering fra en fakturakorreksjon                                             |
| Fakturering og prising           | 2066169          | Oppdater regnskapsdatoen for negativ ufakturert salgspost ved integrering ved hjelp av dobbel skriving                                                            |
| Fakturering og prising           | 2067622          | Behandlingsikonet bør vises under generering av milepæler                                                                                                |
| Fakturering og prising           | 2067624          | Avtalt beløp bør merkes som Anbefalt for selskapet ved generering av milepæler                                                                      |
| Fakturering og prising           | 2086880          | Skjul **Forslag**-knappen på båndet for prosjektbaserte tilbudslinjer                                                                                                |
| Fakturering og prising           | 2098140          | Vis **Rett opp faktura**-knappen for integrerte miljøer                                                                                             |
| Distribusjons og konfigurasjon  | 2101152          | Nytt miljø som opprettes ved hjelp av Project Operations-maler fra Power Platform-administrasjonssenteret, må ha alle posterings-installasjonsoperasjoner utført               |
| Styring av salgsmulighet        | 2086601          | Roller og kategorier som er deaktivert, bør ikke kopieres til lister over Belastbare roller og Belastbare kategorier på tilbudslinjer og kontraktlinjer |
| Prosjektplanlegging og sporing | 1949065          | Datasynlighet fungerer riktig på 200 % zoom                                                                                                                   |
| Prosjektplanlegging og sporing | 2046317          | Mulighet til å gi nytt navn til prosjektenheten i Project Operations                                                                                   |
| Prosjektplanlegging og sporing | 2057171          | Oppdatert feilmelding når **Prosjektets startdato**-feltet er tomt på **Prosjekt**-siden                                                           |
| Prosjektplanlegging og sporing | 2057197          | Støtter ikke beregning av linjekopi med oppgavereferanse                                                                                                     |
| Prosjektplanlegging og sporing | 2060687          | Tidssone-advarselen forsvinner nå etter en bestemt periode                                                                                                      |
| Ressursbehandling           | 1832887          | Standard Ressurskategori-ID må være statisk for å sikre at repeterende data lastes inn for Dataverse- og Finance-miljøer                                                 |
| Tid og utgift              | 2081793          | **Navn på utgiftskategori** må tilordnes et **Beskrivelse av utgiftskategori**-felt i Finance and Operations-apper                                                  |
| Tid og utgift              | 2034882          | **Ny**-knappen viser to ganger på kommandolinjen for tidsoppføringer når Dynamics 365 Field Service er installert                                          |
| Tid og utgift              | 2056028          | Oppdater **Rediger tid**-siden for å inkludere tidslinje                                                                                                              |
| Tid og utgift              | 1983747          | Diagrammet for tidsoppføring viser flere data                                                                                                                   |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet                        | Referansenummer | Kvalitetsoppdatering                                                                                                                                                                                                                                                   |
|-------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prosjektstyring og regnskap | [441680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441680)           | Justeringer blokkert for retur av varebehov                                                                                                                                                                                                        |
| Prosjektstyring og regnskap | [446498](https://fix.lcs.dynamics.com/Issue/Details/?bugId=446498)           | Skjemamerknader vises ikke på formaterte prosjektfakturaer                                                                                                                                                                                                          |
| Prosjektstyring og regnskap | [453407](https://fix.lcs.dynamics.com/Issue/Details/?bugId=453407)           | MEXICO CFDI 33 for prosjektfakturaer kan ikke oppdatere betalingsmåte fra fakturaforslag                                                                                                                                                           |
| Prosjektstyring og regnskap | [458149](https://fix.lcs.dynamics.com/Issue/Details/?bugId=458149)           | Parameter som automatisk angir regnskapsdatoen til en åpen periode, blir ikke respektert i **Integrering**-journalen                                                                                                                                                             |
| Prosjektstyring og regnskap | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Prognose-menyelementer vises ikke på **Prosjekter**-listesiden                                                                                                                                                                                                      |
| Prosjektstyring og regnskap | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Kan ikke åpne **Prosjektoppgave** > **Transaksjoner og prognose**                                                                                                                                                                                                      |
| Prosjektstyring og regnskap | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Når du fjerner og leser ressurstildeling, blir prosjektprognoseenheter i Finance doblet                                                                                                                                                                   |
| Prosjektstyring og regnskap | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468)           | Kan ikke opprette prosjektestimater i Dataverse uten kontraktlinje på prosjektet                                                                                                                                                                 |
| Prosjektstyring og regnskap | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Eliminering mislykkes på grunn av en feil ved utbalansering av bilag når firmavalutaen og transaksjonsvalutaen er forskjellig                                                                                                                                            |
| Prosjektstyring og regnskap | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382)           | Filter for fakturastatus i posterte prosjekttransaksjoner for fastprisprosjekter fungerer ikke                                                                                                                                                            |
| Prosjektstyring og regnskap | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Kan ikke oppdatere startdatoen for en oppgave i Dataverse                                                                                                                                                                                                                    |
| Prosjektstyring og regnskap | [507172](https://fix.lcs.dynamics.com/Issue/Details/?bugId=507172)           | Kunne slette fakturaforslagslinjer i integrert scenario i Project Operations                                                                                                                                                                                    |
| Prosjektstyring og regnskap | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989)           | Kunne slette fakturaforslagslinjer i integrert scenario i Project Operations                                                                                                                                                                                    |
| Prosjektstyring og regnskap | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Forhindre aktivering av flere kontraktlinjer-funksjon uten Dataverse-integrering                                                                                                                                                                                        |
| Prosjektstyring og regnskap | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527)           | Beregnet fakturert inntekt er null (0) når A konto-fakturering = Resultat                                                                                                                                                                          |
| Prosjektstyring og regnskap | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364)           | VIA – salgsverdipostering i konsernintern prosjektfakturering velger en uventet konto                                                                                                                                                                           |
| Prosjektstyring og regnskap | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799)           | Kan ikke utføre estimat-/inntektsføring med Project Operations aktivert                                                                                                                                                                         |
| Reise og utgift                | [378738](https://fix.lcs.dynamics.com/Issue/Details/?bugId=378738)           | Utgift som angis av en representant, returneres til utgiftsbrukeren og ikke representanten                                                                                                                                                                                           |
| Reise og utgift                | [409489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=409489)           | Arbeidsflyt for utgiftsrapport-representanten som sender inn arbeidsflyt er ikke identifisert som arbeidsflytavsender                                                                                                                                                             |
| Reise og utgift                | [464658](https://fix.lcs.dynamics.com/Issue/Details/?bugId=464658)           | Standard dimensjoner i overstyringer av juridisk enhet fungerer ikke på konserninterne utgiftsrapporter                                                                                                                                                                    |
| Reise og utgift                | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892)           | Problem med reduksjonsberegning av måltider for siste dagen for utgiftskategorien kostgodtgjørelse                                                                                                                                                                                    |
| Reise og utgift                | [473646](https://fix.lcs.dynamics.com/Issue/Details/?bugId=473646)           | **Beløp som skal avstemmes**-feltet på **Reiserekvisisjon**-siden oppdateres ikke etter at et utgiftslinjeelement er slettet fra utgiftsrapporten som er koblet til reiserekvisisjonen                                                                                                       |
| Reise og utgift                | [474396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=474396)           | Utgiftsrapport validerte policyen etter at den ble sendt til arbeidsflyten                                                                                                                                                                                           |
| Reise og utgift                | [475777](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475777)            | Reisekostnadskvitteringer vises ikke riktig for registreringsrepresentanten                                                                                                                                                                                            |
| Reise og utgift                | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714)            | Utgiftstype per ansatt viser ikke spesifiserte utgifter når brukerspråket er satt til es-MX                                                                                                                         |
| Reise og utgift                | [477831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477831)            | Utgiftsrapport gjør det mulig å angi feil underkategori for en utgiftskategori                                                                                                                                                                                       |
| Reise og utgift                | [478630](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478630)            | Avstemming av forskudd med utgiftsrapporten fungerer ikke som forventet når beløpet for utgiftsrapporten er høyere enn forskuddsbeløpet                                                                                                           |
| Reise og utgift                | [486680](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486680)            | Ytelsesproblemer med spørringer som er relatert til ProjProjectLookup. Kunden er blokkert fordi det tar lang tid å kjøre spørringen.                                                                                                                     |
| Reise og utgift                | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531)            | Utgiftsrapporter postert med **Tillat gruppering av transaksjoner basert på forskuddsbetalingskonto** og **Korrigering av regnskapsdato ved postering** aktivert viser at regnskapsdatoer ikke er gruppert i **Regnskapsdistribusjon**-tabellen, som har innvirkning på merverdiavgift-poster |
| Reise og utgift                | [491759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491759)            | Importerte kredittkorttransaksjoner med en utenlandsk valuta oppretter feil leverandørtransaksjoner hvis **Snudd avregning** brukes på utgiftsrapportlinjer                                                                                                                     |
| Reise og utgift                | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175)            | Konserninterne utgiftsrapporter kan ikke opprettes hvis Prosjekt-ID-en er lagt til på overskriftsnivået                                                                                                                                                                 |
| Reise og utgift                | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491)            | Problem med utgiftsbetaling når utgiftsbeløpet er høyere enn forskuddsbeløpet                                                                                                                                                                          |
| Reise og utgift                | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556)            | Prosjekt-ID-informasjon under en konsernintern utgiftsrapport er tom hvis brukerrollen er tilordnet en bestemt organisasjon                                                                                                                                           |
| Reise og utgift                | [513845](https://fix.lcs.dynamics.com/Issue/Details/?bugId=513845)            | Arbeidsflyten med automatisk postering av utgiftsrapport er fullført, men fakturaen er ikke postert                                                                                                                                                                                          |

### <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer
Hvis du vil ha informasjon om forskriftsmessige oppdateringer for Finance and Operations-apper, kan du se [Forskriftsmessige oppdateringer](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på LCS og vise de planlagte forskriftsmessige oppdateringene ved hjelp av verktøyet for problemsøk. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]