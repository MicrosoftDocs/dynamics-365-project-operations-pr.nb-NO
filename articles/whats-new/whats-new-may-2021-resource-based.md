---
title: Nyheter mai 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra mai 2021.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030001"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter mai 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

- Project Operations i Dynamics 365 Dataverse-miljøversjon 4.10.0.186
- Prosjektstyring og regnskap i økonomi- og driftsapper, versjon 10.0.18

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- [Planleggingsmoduser](../project-management/scheduling-modes.md): Prosjektledere kan nå definere om et prosjekt skal administreres ved hjelp av planleggingsmodus med den faste varigheten, fast arbeid eller faste enheter.
- [Definere kjørelengde ved hjelp av nivåene for kjørelengdesats](../expense/set-up-mileage.md): Oppdater kjørelengdenivå for utgiftsrapporter for ansatte.

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Listen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i Project Operations mai 2021-versjonen.

| Enhetstilordning | Oppdatert versjon | Kommentarer |
| --- | --- | --- |
| Prosjektfinansieringskilde (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synkroniser betalingsbetingelser for prosjektkontraktkunde. |
| Prosjektfakturaforslag V2 (fakturaer) | 1.0.0.3 | Synkroniser betalingsbetingelser for proformafaktura. |
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kvalitetsoppdateringer |
| Prosjekter V2 (msdyn\_projects) | 1.0.0.2 | Kvalitetsoppdateringer |

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og løsningen for økonomi- og driftsapper. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis du får problemer med å starte tilordningen, følger du instruksjonene i delen [Problem med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledning for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2227635 | Verdiene i feltene **Enhetsgruppe** og **Enhet** kommer som standard fra produktet i rutenettet **Materialestimater**. |
| Fakturering og prising | 2234127 | **Oppgave-ID**-feltet integreres nå riktig med faktiske Dataverse-prosjektverdier når en leverandørfaktura legges ut. |
| Fakturering og prising | 2235564 | Når du lagrer en journallinje, sikrer du at valutaen som vises i journallinjeoppføringen, samsvarer med standardvalutaen til linjen etter lagring. |
| Fakturering og prising | 2246671 | Hvis du gjør en transaksjon ikke-belastbar under fakturering, reverseres den opprinnelige ikke-fakturerte salgsoppføringen, og det opprettes en ny ikke-fakturert salgsoppføring som ikke-belastbar. |
| Fakturering og prising | 2264042 | Gyldig fakturakorrigering må ikke blokkeres hvis det finnes en fakturakorrigeringsdetalj som ikke er gyldig i miljøet. |
| Fakturering og prising | 2146367 | Tilordning av dobbeltskriving i prosjektfakturahode utvides til å inkludere betalingsbetingelser. |
|   Administrasjon av salgsmuligheter | 2086888 | Ikke legg til roller og kategorier som er deaktivert, før du kopierer et tilbud til belastbare roller og kategorier for et nylig kopiert tilbud. |
|   Administrasjon av salgsmuligheter | 2234376 | Skrivebeskyttede felt er nedtonet i rutenettet **Materialestimater**. |
|   Administrasjon av salgsmuligheter | 2238337 | Et tilbud basert på en kontakt kan lagres selv om det ikke er knyttet til en prosjektprisliste. |
|   Administrasjon av salgsmuligheter | 2239810 | Hvis du lukker et tilbud som tapt, lukkes også det tilknyttede prosjektet, og eventuelle bestillinger kanselleres. |
| Prosjektplanlegging og sporing | 2099559 | Det ble lagt til flere valideringer for systemtilstanden før rutenettet for **Prosjektoppgaver** åpnes. |
| Prosjektplanlegging og sporing | 2178987 | Rettet en midlertidig feil som oppstår når du velger **Neste fase** på **Prosjekt**-siden. |
| Ressursbehandling | 2224817 | Funksjonaliteten for å utvide standardbestillinger til riktig bestillingsstatus. |
| Tidsoppføring | 2202476 | Siden **Tidsregistrering** bruker nå kontrollen for rutenettreaksjon og løser problemer som feiljustering av rutenett. |
| Tidsoppføring | 2223377 | Tidsoppføringen skjules fra **Relatert**-delen på siden **Ressurs som kan reserveres** for å unngå forvirring med anvendeligheten. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Prosjektstyring og regnskap | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Kan ikke konvertere et tilbud til vunnet i Project Operations for ressursbaserte scenarioer på grunn av en integrasjonsfeil. |
| Prosjektstyring og regnskap | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: En feil vises når du prøver å knytte en kontraktlinje til en prosjekt-ID på grunn av kontrollen av overlappende kontraktlinjer og transaksjonstyper. |
| Prosjektstyring og regnskap | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** angir fakturaadressen for finansieringskilden fra en annen kunde. |
| Reise og utgift | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Det kan oppstå en posteringsfeil knyttet til kjørelengdeoppsett. |
| Reise og utgift | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funksjonaliteten **Deling til personlig** fungerer ikke for utgiftstransaksjoner i utenlandsk valuta. |
| Reise og utgift | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Rullegardinverdier for utgiftskategori viser feil kategorier for representanteruansett om de er en ressurs. |
| Reise og utgift | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Du kan ikke lagre en konsernintern reiseregning på grunn av en **Ressurs-/kategorivalidering**-feil. |
| Reise og utgift | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Feil kilometersatsberegning i utgiftsrapportpostering har delte linjer. |
| Reise og utgift | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Du kan ikke postere en konsernintern reiseregning når merverdiavgiften er inkludert og motkontotypen på betalingsmåten er **Arbeider**. |
| Reise og utgift | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Tilbakerulling av **TrvRequisitionLine**-dataenheten og den unike indeksen er tilknyttet. |
| Reise og utgift | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Utgiftsrapport støtter oppretting og oppdatering av kildedokumentlinje. |
| Reise og utgift | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Feil underbilag i hovedboken vises i et konserninternt scenario hvis merverdiavgiften posteres til den juridiske enheten for målet. |
| Reise og utgift | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: Utgiftsestimatet slettes ikke fra Finance når det slettes fra Dataverse. |
| Reise og utgift | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Når utgiftskategorien er en ikke-prosjektkategori, kopieres ikke de finansielle dimensjonene som er valgt på **Utgifter**-siden, til utgiftsrapporten. |
