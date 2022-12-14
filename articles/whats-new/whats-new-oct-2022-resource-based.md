---
title: Nyheter oktober 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra oktober 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806630"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter oktober 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.57.0.176
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.30

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

| Funksjonsområdet | Funksjonsnavn | Mer informasjon |
| --- | --- | --- |
| Prosjektplanlegging og sporing | **Ekstern planlegging i Project Operations**<br>Med modusen for ekstern planlegging kan kunder opprette, oppdatere og slette enheter som er knyttet til arbeidsnedbrytningsstrukturer (WBS-er) ved å bruke de opprinnelige API-ene for Dataverse uten gjeldende grenser som håndheves av Project for the Web. | [Ekstern planlegging](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribusjon og konfigurasjon | <p>**La kunder velge distribusjonstypen**<br>Produktdrevne oppdateringer (PDU-er) i Project Operations brukes til å installere Project Operations-løsningen for dobbel skriving automatisk når kjerneløsningen for dobbel skriving og iverksettingsløsningen er installert i miljøet.</p><p>Denne funksjonen innfører den nye parameteren **Virkemåte for løsningsoppgradering** i prosjektparametere. Når **Bare Lite** er angitt for denne parameteren installerer ikke lenger PDU-er løsningen for dobbel skriving i Project Operations, selv om kjerneløsningen for dobbel skriving og iverksettingsløsningen er installert i miljøet. Denne funksjonaliteten er til nytte for kunder som planlegger å bruke løsninger for dobbel skriving til å integrere salgsordrer i økonomi- og driftsapper, men vil bruke Project Operations i en Lite-modus (det vil si uten integrering i økonomi- og driftsapper).</p> | |
| Fakturering og prising | <p>**Valutakonvertering for ufakturert salgstransaksjon for utgift i integrerte miljøer**<br>Når det gjelder kunder som bruker Project Operations integrert med økonomi- og driftsapper (det vil si i den ressursbaserte/ikke-lagerførte distribusjonstypen), behandles valutakursene vanligvis i økonomi- og driftsapper. Hvis en utgiftskategori imidlertid skal få pris ved hjelp av prisberegningsmetoden Kostpris eller Påslag over kostnad når kunden faktureres, bruker valutakursen som brukes til å beregne salgsbeløpet, valutakursene i Dataverse, ikke valutakurser fra økonomi- og driftsapper.</p><p>Denne funksjonen innfører den nye parameteren **Valutakonverteringsfunksjonalitet** i prosjektparametere. Når denne parameteren er satt til **Utvidet med tilbakefall**, beregnes ufakturerte salgsbeløp i utgiftstransaksjoner ved hjelp av valutakursene fra økonomi- og driftsapper.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen. Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2316317 | Systemet tillater at fakturaer opprettes uten belastbare transaksjoner. |
| Fakturering og prising | 2737300 | Valider at **Kunde**-feltet er tilgjengelig før skjemaet åpnes. |
| Fakturering og prising | 2744948 | Legg til en nullkontroll for Faktureringsmetode. |
| Fakturering og prising | 2763515 | Referanse for nullreferansefeil når salgskontrakten for fakturaen mangler. |
| Fakturering og prising | 2844301 | Opprettelse av bunkefaktura mislykkes på grunn av en feil. |
| Fakturering og prising | 2845869 | Feil lagring for Organisasjonstjeneste. |
| Fakturering og prising | 2853729 | Rolle- og prisdetaljer oppdateres når faktureringstypen endres. |
| Fakturering og prising | 2940350 | Når faktiske verdier får pris, skal bare aktive prislister registreres automatisk. |
| Distribusjon og konfigurasjon | 3001206 | Enheten msdyn\_replaylogheader gjør at kundeorganisasjoner ikke kan oppgraderes. |
| Administrasjon av salgsmulighet | 2755582 | Referanse for nullreferanseunntak i hjelper for regel for delt fakturering. |
| Administrasjon av salgsmulighet | 2761477 | Når du bruker delt fakturering, blir milepæler frittstående ved sletting av en milepæl (topptekst). |
| Administrasjon av salgsmulighet | 2767595 | Når en oppføring for materialbruk åpnes i hovedskjemaet, endres Ressurs som kan reserves for oppføringen, til den påloggede brukeren. |
| Prosjektplanlegging og sporing | 2790384 | Tidsavbruddet for ventende OperationSet er for kort. |
| Prosjektplanlegging og sporing | 2957840 | Oppgaver kan ikke lagres, og kolonner kan ikke legges til på **Oppgaver**-siden i Project Operations som er integrert. |
| Ressursbehandling | 2751560 | Inkonsekvente foretrukne organisasjonsenheter i ressurskrav. |
| Utsetting | 2853245 | Samsvar for faktiske verdier på leverandørfakturalinje oppdaterer ikke verifiseringsstatusen hvis en kontraktlinje allerede er koblet til leverandørfakturalinjen. |
| Utsetting | 2907231 | Prosessfasen for leverandørfakturaer kan ikke gå videre. |
| Tid og utgift | 2867363 | Oppføringer forlater ikke visningen Fravær/ferier for godkjenning når de er i kø for godkjenning. |
| Tid og utgift | 2894405 | TESA: Den ubrukte katalogen for konseptgodkjenning fører til problemer med forskriftssamsvar. |

### <a name="project-management-and-accounting-in-finance"></a>Oversikt over prosjektstyring og regnskap i Finans

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du deg på Microsoft Dynamics Lifecycle Services og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
