---
title: Nyheter april 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Dette emnet inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i april 2021-versjonen av Project Operations for scenarioer basert på ressurer / ikke-lagerførte enheter
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dbce86e88f8315ac4a4957c1128b5619d5328bdbbe27793e161f8f2691899481
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008148"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter april 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gjelder for følgende Dynamics 365 Project Operations-komponenter og versjoner:

- Project Operations på Dataverse-miljø versjon 4.9.0.221
- Prosjektstyring og regnskap i Dynamics 365 Finance-miljø versjon 10.0.17

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- Ikke-lagerført materiell for prosjekter. Viktige funksjoner omfatter følgende:
  - Estimering og prising av ikke-lagerført materiell i salgssyklusen for et prosjekt. For mer informasjon, se [Konfigurere kostnads- og salgspriser for katalogprodukter – Lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sporing av bruken av ikke-lagerført materiell under prosjektlevering. For mer informasjon, se [Registrer materialbruk på prosjekter og prosjektoppgaver](../material/material-usage-log.md).
  - Fakturering av kostnader for ikke-lagerført materiell som er brukt. For mer informasjon, se [Administrere faktureringsrestansen](../proforma-invoicing/manage-billing-backlog.md).
  - Hvis du vil ha mer informasjon om hvordan du konfigurerer denne funksjonen, kan du se [Konfigurere ikke-lagerførte materialer og ventende leverandørfakturaer](../procurement/configure-materials-nonstocked.md)
- Oppgavebasert fakturering: Lagt til muligheten til å knytte prosjektoppgaver til prosjektkontraktslinjer, og dermed utsette dem for samme faktureringsmetode, fakturahyppighet og kunder som prosjektoppgavene på kontraktlinjen. Denne tilknytningen sikrer nøyaktig fakturering, regnskapsføring, omsetningsberegning og anerkjennelse for å arbeide i samsvar med dette oppsettet på prosjektoppgaver.
- Nye API-er i Dynamics 365 Dataverse tillater oppretting, oppdatering og sletting med **planleggingsenheter**. For mere informasjon, se [Bruke API-er for tidsplan til å utføre operasjoner med planleggingsenheter](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Listen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i Project Operations april 2021-versjonen.

| **Enhetstilordning** | **Oppdatert versjon** | **Kommentarer** |
| --- | --- | --- |
| Faktiske verdier for Project Operations-integrering (msdyn\_actuals) | 1.0.0.14 | Tilordning endret for å synkronisere faktiske data for materielle prosjekter. |
| Enhet for utgiftsestimater for Project Operations-integrering (msdyn\_estimateslines) | 1.0.0.2 | Lagt til synkronisering av prosjektkontraktlinje i Finance and Operations-apper for oppgavebasert faktureringsstøtte. |
| Enhet for timesestimater for Project Operations-integrering (msdyn\_resourceassignments) | 1.0.0.5 | Lagt til synkronisering av prosjektkontraktlinje i Finance and Operations-apper for oppgavebasert faktureringsstøtte. |
| Project Operations-integreingstabell for materialestimater (msdyn\_estimatelines) | 1.0.0.0 | Ny tabelltilordning for å synkronisere materialestimater fra Dataverse til Finance and Operations-apper. |
| Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn\_projectvendorinvoices) | 1.0.0.0 | Ny tabelltilordning for å synkronisere leverandørfakturahoder fra Finance and Operations-apper til Dataverse. |
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Ny tabelltilordning for å synkronisere leverandørfakturalinjer fra Finance and Operations-apper til Dataverse. |

Du bør alltid kjøre den nyeste versjonen av tilordningen i miljøet og aktivere alle relaterte tabelltilordninger når du oppdaterer Project Operations Dataverse-løsningen og Finance and Operations-løsningsversjonen. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du får problemer med å starte tilordningen, følger du instruksjonene i delen [Problem med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledning for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations i Dynamics 365 Dataverse

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2124532 | Knappen **Rett opp faktura** vises på en proformafaktura når honorarbeløpet eller det brukte honorarbeløpet vises på den opprinnelige fakturaen. Knappen vises bare for miljøer med Finance versjon 10.0.19 eller høyere. |
| Fakturering og prising | 2224568 | Lagt til logikk for å aktivere tilpassinger som involverer aktivering av plugin-modulen for fakturabekreftelse. |
| Fakturering og prising | 2101098 | Forbedret logikken for standardfelt til proformafaktura: **Fakturaadresse**, **Fakturanavn** og **Betalingsbetingelser** angis nå som standard fra den tilsvarende kundeoppføringen i prosjektkontrakten. |
| Fakturering og prising | 2021413 | Oppdaterte feltene **Faktisk kostnad** og **Salg** i **Oppgave**-enheten for å inkludere salgsverdier fra ufakturerte og fakturerte utgifter for oppgaver. |
| Fakturering og prising | 2182110 | Når du kopierer en prosjektkontrakt, genereres kontraktlinje-ID-en på nytt i målprosjektkontrakten for å sikre at den er unik. |
| Administrasjon av salgsmulighet | 2186741 | Valideringer som er lagt til for å sikre at **Opprinnelse**-feltet og **Transaksjonstype** ikke kan oppdateres for eksisterende tilbudslinjedetaljer. |
| Administrasjon av salgsmulighet | 2191353 | Milepæler kan ikke opprettes på en kontraktlinje for tid og materialer. |
| Administrasjon av salgsmulighet | 2216956 | Løste problemer med **Oppdater priser**. |
| Planlegging og sporing | 2182979 | Forbedret prosjektkopieringsfunksjonen for å sikre at utgiftsestimatlinjene kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184144 | Forbedret prosjektkopieringsfunksjonen for å sikre at navnet på ressursposisjonen kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184799 | Prosjektkopiering: Strammet inn kontrollen for å sikre at den estimerte startdatoen ikke kan endres under kopiering. |
| Planlegging og sporing | 2185134 | Prosjektkopiering: Estimert startdato for målprosjektet er satt til dagens dato. |
| Planlegging og sporing | 2196373 | Prosjektkopiering: Kontroller at prosjektleder- og teammedlemsoppføringer ikke dupliseres i prosjektteamet. |
| Planlegging og sporing | 2211833 | Prosjektkopiering: Ressurstilordninger kopieres fra kildeprosjektoppgaven til målprosjektet. |
| Planlegging og sporing | 2186541 | Løste problemer i **Estimater**-rutenettet ved gruppering etter ressurs. |
| Planlegging og sporing | 2166906 | Transaksjonskategorien fra en oppgave må kopieres til enheten **Ressurstilordning**. |
| Ressursbehandling | 2125362 | Løste problemer med oppretting av et generelt teammedlem ved hjelp av en timesbasert tildelingsmetode. |
| Tid og utgift | 2113603 | Løste det tilpassingsrelaterte problemet med å fjerne attributter fra **Tidsregistrering**-siden. Systemet kontrollerer nå om attributtet finnes på siden før det får tilgang til dem ved hjelp av et skript. |
| Tid og utgift | 2204377 | Kopierte timeregistreringer må vises automatisk når du velger **Kopier uke** i tidsoppføringen. |
| Tid og utgift | 2209059 | **Status**-feltet kan redigeres for tidsoppføringer i Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Prosjektstyring og regnskap | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminering av omvendt estimat fungerer ikke i delen **Periodisk**.  |
| Prosjektstyring og regnskap | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funksjonen **Regnskapsjustering** oppretter et problem med finanskontoer der **Ikke tillat manuell oppføring** er valgt. |
| Prosjektstyring og regnskap | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Lagt til forretningslogikk for å behandle korrigeringsfakturaer inkludert honorarbeløp eller brukt honorarbeløp. |
| Prosjektstyring og regnskap | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | VIA-salgsverdipostering i konsernintern prosjektfakturering velger en uventet konto. |
| Prosjektstyring og regnskap | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Når du arbeider med beholdere i Project Operations, fører endring av standardprosjektet på en kontrakt etter at forskuddsbetalingene er fakturert, problemer med innkommende fradrag. |
| Prosjektstyring og regnskap | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Hvis du fjerner et prosjekt fra en kontrakt i Project Operations, må du om nødvendig tilbakestille standardprosjektet for kontrakten. |
| Prosjektstyring og regnskap | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | I Project Operations vises feil utgiftslinjer i listen **Legg til linje** på den konserninterne fakturaen. |
| Prosjektstyring og regnskap | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | I Project Operations vises ikke siden **Innkjøpsavtale** i juridiske enheter i Finance som er integrert med Project Operations. |
| Prosjektstyring og regnskap | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | På grunn av en Dataverse-integreringsfeil kan du ikke konvertere et tilbud til vunnet i Project Operations. |
| Prosjektstyring og regnskap | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** kan angi fakturaadressen for finansieringskilde fra en annen kunde.  |
| Prosjektstyring og regnskap | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | I Project Operations velges ingen dimensjoner når du oppretter en posteringsfaktura for en transaksjon. |
| Reiser og utgifter | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Forskuddssaldoen oppdateres ikke for en utgiftsrapport hvis den er godkjent og lagt inn linje for linje. |
| Reise og utgift | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Avgifter for angitte, konserninterne utgiftsrapporter beregnes ikke på riktig måte. |
| Reise og utgift | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Flere felter relatert til prosjekter vises på den nye siden **Konserninterne utgiftsrapporter**. |
| Reise og utgift | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Det vises en uriktig feilmelding i overskriftsbekreftelsene for utgiftsrapporter. |
| Reise og utgift | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | En utgiftsrapport posteres feil i et konserninternt scenario hvis merverdiavgiften posteres til den juridiske enheten for målet. |
| Reise og utgift | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Innsendingsdatoer for rapporter skrives ikke ut på godkjente utgiftsrapporter. |
| Reise og utgift | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Feltene **Godkjenningsdato** og **Avvisningsdato** fylles ikke ut etter at en utgift er godkjent. |
| Reise og utgift | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | En reiserekvisisjon som er opprettet for én arbeider, kan brukes for en annen arbeiders reiseregning. |
| Reise og utgift | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Utgiftskategorier låses når du legger til en ny utgiftslinje. |
| Reise og utgift | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Hvis du deler opp linjene i en allerede oppdelt utgiftsrapport, fører dette til ufullstendig postering av bilaget i Leverandørgjeld\Finans, og bryter regnskapskildeutforskeren fordi **TRVEXPTRANS.SOURCEDOCUMENTLINE** dupliseres. |
| Reise og utgift | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Reiserekvisisjonspolicyen fungerer ikke som forventet. |
| Reise og utgift | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Navnet på leverandørkontoen vises ikke for posterte prosjekttransaksjoner for utgiftsrapporter. |
| Reise og utgift | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | I Project Operations kan du ikke godkjenne tid med en oppgave for et konserninternt prosjekt. |
| Reise og utgift | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategorien for retur av kontantforskudd oppdaterer ikke forskuddssaldoer når de publiseres. |
| Reise og utgift | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Salgsprisen beregnes feil på utgiftsrapporter som ble opprettet i en fremmed valuta ved hjelp av importerte kredittkorttransaksjoner, og er knyttet til et prosjekt. |
| Reise og utgift | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Rullet tilbake **TrvRequisitionLine**-dataenheten og den tilknyttede unike indeksen. |
| Reise og utgift | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | La til instrumentering i **SOURCEDOCUMENTLINE**-genereringen. |
| Reise og utgift | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Feil underbilag i hovedboken vises i et konserninternt scenario hvis merverdiavgiften posteres til den juridiske enheten for målet. |
| Reise og utgift | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | I Project Operations slettes ikke utgiftsestimater fra Finance når de slettes fra Dataverse. |
| Reise og utgift | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Når en utgiftskategori er en ikke-prosjektkategori, kopieres ikke de finansielle dimensjonene som er valgt på **Utgift**-siden, til utgiftsrapporten. |
