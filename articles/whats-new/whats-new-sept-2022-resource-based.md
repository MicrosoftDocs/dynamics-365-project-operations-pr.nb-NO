---
title: Nyheter september 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra september 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634818"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter september 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.46.0.60
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.29

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

| Funksjonsområdet | Funksjonsnavn | Mer informasjon |
| --- | --- | --- |
| Administrasjon av salgsmulighet | **Revisjon og aktivering av tilbud**<br>Project Operations har fullstendig støtte for salgsprosessen. Prosjekttilbud kan aktiveres for å representere en tilstand der tilbudet er skrivebeskyttet og blir gjennomgått. Aktiverte tilbud kan revideres for å opprette nye tilbud som har et trinnvis revisjonsnummer. Aktiverte prosjekttilbud eller tilbudsrevisjoner kan lukkes som vunnet eller tapt. | [Aktiver og revider et prosjekttilbud](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturering og prising | **Tidssoneagnostisk prisstandard**<br>Project Operations har innført konseptet med en tidssoneagnostisk dato for alle faktiske verdier for prosjekt. Et nytt felt, **Transaksjonsdato**, er nå tilgjengelig på journallinjer og faktiske verdier og brukes til å lagre datoen da transaksjonen forekom, men uten å konvertere denne datoen til Coordinated Universal Time. Denne datoen brukes til nedstrømsprosesser, for eksempel prisstandard og opprettelse av faktura. | <p>[Fastslå kostnadssatser for prosjektbaserte estimater og faktiske verdier](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Fastslå salgspriser for prosjektbaserte estimater og faktiske verdier](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturering og prising | **Datoeffektive prisoverstyringer i Project Operations**<br>Datoeffektive prisoverstyringer gjør at du kan overstyre eller endre bestemte priser i prislisten. | [Datoeffektive prisoverstyringer](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Utsetting | **Utsetting og avstemming av leverandørfakturaer**<br>Denne funksjonen gjør at kunder kan opprette underkontrakter for å kjøpe ressurstid, utgiftskategorier og materialer som brukes til prosjektarbeid. Den gjør også at kunder kan registrere leverandørfakturaer som blir tilgjengelige for prosjektledere for verifisering i Dataverse, i økonomi- og driftsapper. | <p>[Administrasjon av underkontrakt](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Opprett leverandørfakturaer](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Tid og utgift | **Global godkjenner**<br>Denne funksjonen aktiverer uavhengige programvareleverandører (ISV) og sentralisert godkjenning, uavhengig av statusen for prosjekt- eller teammedlem i prosjektet. | [Sikkerhet og godkjenninger](/dynamics365/project-operations/approvals/approvals-security) |
| Utgiftshåndtering | **Mulighet til å postere utgiftsansvar i leverandørvaluta**<br>Denne funksjonen gjør at utgiftsrapporter kan posteres i en leverandørvaluta for betalingsmetoden for kontanter. | [Mulighet til å postere utgiftsansvar i leverandørvaluta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Prosjektinnkjøp | **Betal når betalt-leverandørbetalinger**<br>Denne funksjonen gjør at funksjonen Betal når betalt (PWP) kan brukes med ikke-lagerføringsmiljøer i Project Operations. Den gjør at leverandørbetalingene kan blokkeres/beholdes basert på tilbakeholdelsesbetingelser frem til betalingen er mottatt fra kunden. | [Betal når betalt-leverandørbetalinger](/dynamics365/project-operations/procurement/pay-when-paid) |
| Prosjektinnkjøp | **Innkjøpsrekvisisjoner for prosjekt**<br>Denne funksjonen gjør at brukere kan opprette prosjektrelaterte bestillinger i juridiske enheter der Project Operations i Dynamics 365 Customer Engagement-integrering er aktivert. Prosjektbestillinger kan brukes til å registrere innkjøp av ikke-lagerført materiale mot prosjektet av identiteten Innkjøpsavdeling. Prosjektbestillinger synkroniseres ikke med Dataverse. Du kan imidlertid bruke en virtuell enhet til å vise prosjektbestillingslinjer i Dataverse for informasjon om prosjektledere. Prosjektrelatert leverandørfakturakostnad integreres med enheten Faktiske verdier for prosjekt i Dataverse. Prosjektkostnad registreres i prosjektunderfinans ved hjelp av journalen for Project Operations-integrering. | |
|Prosjektplanlegging og sporing|**Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter** </br> </br>API-en for redigering av ressurstilordninger gjør det mulig for utviklere å programmatisk angi en oppgavetilordningspersons innsats i alle støttede datointervaller for mer detaljert planlegging av faser i tid.|[Bruk API-er for prosjektplan til å utføre operasjoner med planleggingsenheter](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Tabellen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i september 2022-versjonen av Project Operations.

| Enhetstilordning | Oppdatert versjon | Kommentarer |
| -------------- | ------------------- | ------------|
| Faktiske verdier for Project Operations-integrering (msdyn_actuals) | 1.0.0.15 | Denne tilordningen støtter behandling av faktiske verdier i underkontrakter med Project Operations for ressursbaserte scenarioer. |
| Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn_projectvendorinvoices) | 1.0.0.2 | Denne tilordningen støtter behandling av faktiske verdier i underkontrakter med Project Operations for ressursbaserte scenarioer. |
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Denne tilordningen støtter behandling av faktiske verdier i underkontrakter med Project Operations for ressursbaserte scenarioer. |

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2754422 | Materiale- og utgiftsestimater flyter ikke til Finance når prosjekter kopieres i Dataverse. |
| Tid og utgift | 2787409 | En ugyldig godkjenner kan godkjenne en tidsoppføring som ikke er knyttet til et prosjekt. |
| Administrasjon av salgsmulighet | 2788907 | Oppdatert feilmelding om unikhetsvalidering for ordrelinjer som inneholder flagg. |
| Tid og utgift | 2842253 | Håndtering av nullunntak for tidsgodkjenning. |
| Fakturering og prising | 2844181 | Mislykket forsøk på å hente korrelasjons-ID-en blokkerer fakturaopprettelse. |
| Fakturering og prising | 2876628 | QLD, CLD – Løsningen for estimering av prisliste skal bruke eldre felter for datointervall i prislisten. |
| Utsetting | 2893222 | Hvis ingen rolle er angitt for en underkontraktlinje, må det gå an å velge denne linjen på et teammedlem for enhver rolle. |

### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du deg på Microsoft Dynamics Lifecycle Services og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funksjoner som er aktivert som standard i den neste versjonen

Denne tabellen viser funksjonene som er aktivert som standard i versjon 10.0.30. De fleste funksjoner som er aktivert automatisk, kan slås av i [Funksjonsbehandling](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). I fremtiden kan det hende at enkelte funksjoner som har blitt slått på automatisk, blir fjernet fra Funksjonsbehandling og blir obligatoriske. Denne endringen sikrer at kunder bruker gjeldende funksjonalitet, slik at forbedringer kan bygge på den gjeldende funksjonaliteten etter hvert som de legges til. Funksjoner aktiveres aldri automatisk på mindre enn ett år hvis de ikke er avgjørende.

| Funksjonsnavn | Aktiveringsdato | Funksjon lagt til | Funksjonstilstand | Modul |
| --- | --- | --- |--- |--- |
| Aktiver den asynkrone operasjonen når brukeren må bytte mellom synkrone og asynkrone operasjoner | 21. oktober 2022 | 9. april 2021 | Aktivert som standard | Utgiftshåndtering |
| Evaluering av utgiftspolicy kreves for kvitteringer | 21. oktober 2022 | 20. desember 2021 | Aktivert som standard | Utgiftshåndtering |
| Listevisning for utgiftsrapporter opprettet ved å delegere arbeidere | 21. oktober 2022 | 19. februar 2020 | Aktivert som standard | Utgiftshåndtering |
| Beregning av reisegodtgjørelse totalt etter regnskapsår | 21. oktober 2022 | 10. mai 2022 | Aktivert som standard | Utgiftshåndtering |
