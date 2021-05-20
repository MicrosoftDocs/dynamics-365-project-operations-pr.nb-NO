---
title: Nyheter januar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Dette emnet gir informasjon om kvalitetsoppdateringene som er tilgjengelige i januar 2021-versjonen av Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ece05f1f551b18a5b30610af57d68baa120948fb
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950996"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter januar 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_


Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

  - Project Operations på Dataverse-miljø versjon 4.6.0.154
  - Prosjektstyring og regnskap i Dynamics 365 Finance-miljø versjon 10.0.16

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområde** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| **Distribusjon og konfigurasjon** | 2106818 | Endret det nye navnet på webressursen som forårsaket problemer i forbindelse med tilpassing av en side. |
| **Fakturering og prising** | 2091908 | Løste synligheten for alternativene **Lås priser** og **Bruk gjeldende priser** på siden **Faktura** når Project Operations er installert sammen med Dynamics 365 Field Service. |
| **Fakturering og prising** | 2103058 | Oppdaterte **Prosjekttotaler** for å håndtere nullverdier for faktisk kostnad for en oppgave. |
| **Fakturering og prising** | 2116100 | Forbedrede feilmeldinger som brukes med funksjonaliteten **Rette oppføringer for faktiske data**. |
| **Fakturering og prising** | 2116129 | Forbedret synlighet for kostnadsestimater i kategorien **Estimater** på siden **Prosjekter**. |
| **Fakturering og prising** | 2119112 | Løste aggregering av faktisk salg og faktisk kostnad når ulike valutakurser brukes. |
| **Fakturering og prising** | 2134705 | Løste feilen Kan ikke lese egenskapen **getResourceString** for udefinert når siden **Faktura** er åpnet og Field Service er installert. |
| **Administrasjon av salgsmulighet** | 2022195 | Det oppgavebaserte faktureringsrutenettet på **Prosjekt**-siden inneholder et ikon som angir at det er en kontrakt eller tilbudslinje koblet til den oppgaven. |
| **Administrasjon av salgsmulighet** | 2029135 | Løste forretningsprosessfeilen som oppstår når en bruker prøver å åpne en fakturalinje på en bekreftet faktura som har et forskuddsbeløp fakturert. |
| **Administrasjon av salgsmulighet** | 2040713 | Løste skriptfeilen som oppstår når du oppretter en faktura fra en kontrakt, og Field Service er installert. |
| **Prosjektplanlegging og sporing** | 2090202 | Merket forretningsregler som ikke lenger brukes, som **Avskrevet**. |
| **Tid og utgift** | 2091249 | Innsnevret kontroller slik at brukere ikke kan endre oppgaven på en innsendt eller godkjent tidsoppføring. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| **Funksjonsområde** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| **Prosjektstyring og regnskap** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Feil kontraktbeløp på siden **Akonto** for et fast prisprosjekt med flere finansieringskilder. |
| **Prosjektstyring og regnskap** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Plassholderen **Invoiceproposal.PSAnfRefProjId** viser ikke prosjekt-ID-en for arbeidsflyten **Review project invoice proposals**. |
| **Prosjektstyring og regnskap** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Feil dato for kontantrabatt brukes ved innlegging av prosjektfakturaforslag. |
| **Prosjektstyring og regnskap** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Når du fjerner og leser ressurstilordninger i Project Operations, blir prosjektprognoseoppføringene i Økonomi doblet. |
| **Prosjektstyring og regnskap** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | I Project Operations kan du ikke opprette prosjektestimater i Dataverse uten å ha en kontraktlinje på prosjektet. |
| **Prosjektstyring og regnskap** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Finansdimensjonen i en prosjektutgiftstransaksjon synkroniseres ikke med den relaterte fordelingen og regnskapsdistribusjonen av utgiftsrapporten når kostnader posteres til Saldo. |
| **Prosjektstyring og regnskap** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filteret **Fakturastatus** i posterte prosjekttransaksjoner for fastprisprosjekter fungerer ikke. |
| **Prosjektstyring og regnskap** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminering av omvendt estimat fungerer ikke i delen **Periodisk**. |
| **Prosjektstyring og regnskap** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Fakturaforslagslinjer kan slettes i Project Operations når de er integrert med Dataverse. |
| **Prosjektstyring og regnskap** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Forhindre aktivering av funksjon for flere kontraktlinjer uten Dataverse-integrering. |
| **Prosjektstyring og regnskap** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Når akontofakturering er lik overskudd og tap, vises den fakturerte omsetningen som null på Estimater-siden. |
| **Prosjektstyring og regnskap** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Fakturarettelser fungerer ikke i integrerte miljøer. |
| **Prosjektstyring og regnskap** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Når du posterer VIA-salgsverdi i konsernintern prosjektfakturering, blir feil konto valgt. |
| **Prosjektstyring og regnskap** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | I Project Operations kan ikke avhengigheter for estimatoppgaver i Dataverse oppdateres. |
| **Prosjektstyring og regnskap** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Gjentatt sletting av journaler for Project Operations-integrering i Økonomi fører til tap av data. |
| **Prosjektstyring og regnskap** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Følgende feil oppstår under postering av et prosjektfakturaforslag: Transaksjonen balanserer ikke på rapporteringsvalutaen når forskuddsfakturaen som er trukket fra, legges til igjen". |
| **Prosjektstyring og regnskap** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Feil prosjekt-ID inkluderes ved fradrag etter at standard prosjektkontrakt er oppdatert i Project Operations. |
| **Prosjektstyring og regnskap** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Estimat- og omsetningsgjenkjenning kan ikke fullføres når Project Operations er aktivert. |
| **Prosjektstyring og regnskap** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Hvis du fjerner et prosjekt fra en kontrakt, tilbakestilles ikke standardprosjektet for kontrakten i Project Operations. |
| **Prosjektstyring og regnskap** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I Project Operations vises feil utgiftslinjer i listen **Legg til linje** på en konsernintern faktura. |
| **Reise og utgift** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Utgiftslinjer kan ikke posteres fordi det mangler timeoppsett på kontraktlinjen. |
| **Reise og utgift** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Når validering av prosjekt/kategori er obligatorisk, vises ikke utgiftskategorier som er tilknyttet prosjektet, i utgiftsrapporten. |
| **Reise og utgift** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Forskuddssaldoen oppdateres ikke når en utgiftsrapport legges inn etter linje. |
| **Reise og utgift** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Jobben **Oppdater betalingsinformasjon** mislykkes etter reversering av salgsbetingelser der en faktura ble inngått avtale med to eller flere betalingstransaksjoner. |
| **Reise og utgift** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Det er et problem med beregningen av måltidsreduksjonen for den siste dagen for utgiftskategorien Kostgodtgjørelse. |
| **Reise og utgift** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Rapporten **Utgiftstype per ansatt** viser ikke angitte utgifter hvis en brukers første tilkobling var på es-MX-språket. |
| **Reise og utgift** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Leverandørbetalingen for en utgiftsrapportfaktura bruker feil sammendragskonto for innlegg av regning. |
| **Reise og utgift** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Når en utgiftsrapport blir postert med alternativene **Tillat gruppering av transaksjoner basert på forskuddsbetalingskonto** og **Korrigering av regnskapsdato ved postering** aktivert, er ikke regnskapsdatoene gruppert i tabellen **Regnskapsdistribusjon**, noe som påvirker mva-postene. |
| **Reise og utgift** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Tilordning av underkategori for utgifter fjernes når det ikke er merket av for Bruk i utgift, og deretter velges på nytt. |
| **Reise og utgift** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | En konsernintern utgiftsrapport kan ikke opprettes hvis Prosjekt-ID-en legges til på overskriftsnivået. |
| **Reise og utgift** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Det er et problem med utgiftsbetalinger når utgiftsbeløpet er høyere enn forskuddsbeløpet. |
| **Reise og utgift** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Feltet **Prosjekt-ID** i en konsernintern utgiftsrapport er tom hvis brukerrollen er tilordnet en bestemt organisasjon. |
| **Reise og utgift** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Utgiftskategorien låses når du legger til en ny utgiftslinje. |
| **Reise og utgift** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Hvis du pålegger deg utgiftsrapportlinjer som allerede er delt, fører dette til en ufullstendig postert bilag i Leverandørgjeld\Finans. På grunn av dupliseringen av **TRVEXPTRANS.SOURCEDOCUMENTLINE**, er også regnskapskildeutforskeren brutt. |
| **Reise og utgift** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeksen som legges til i tabellen **TRVREQUISITIONLINE** som kunden har duplikater for, fører til en feil under oppgraderingen. |
| **Reise og utgift** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations kan ikke tid med konserninterne oppgaver i Dataverse opprettes eller godkjennes. |

## <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer

Hvis du vil ha informasjon om forskriftsmessige oppdateringer for Finance and Operations-apper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på LCS og vise de planlagte forskriftsmessige oppdateringene ved hjelp av verktøyet for problemsøk. Problemsøk lar deg søke etter land, type funksjon og utgave.


[!INCLUDE[footer-include](../includes/footer-banner.md)]