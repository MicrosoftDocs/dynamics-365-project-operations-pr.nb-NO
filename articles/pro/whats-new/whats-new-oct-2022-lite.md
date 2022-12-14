---
title: Nyheter oktober 2022 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations Lite-distribusjon fra oktober 2022.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806643"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Nyheter oktober 2022 – Project Operations Lite-distribusjon

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.57.0.176

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

| Funksjonsområdet | Funksjonsnavn | Mer informasjon |
| --- | --- | --- |
| Prosjektplanlegging og sporing | **Ekstern planlegging i Project Operations**<br>Med modusen for ekstern planlegging kan kunder opprette, oppdatere og slette enheter som er knyttet til arbeidsnedbrytningsstrukturer (WBS-er) ved å bruke de opprinnelige API-ene for Dataverse uten gjeldende grenser som håndheves av Project for the Web. | [Ekstern planlegging](/dynamics365/project-operations/project-management/external-scheduling) |
| Distribusjon og konfigurasjon | <p>**La kunder velge distribusjonstypen**<br>Produktdrevne oppdateringer (PDU-er) i Project Operations brukes til å installere Project Operations-løsningen for dobbel skriving automatisk når kjerneløsningen for dobbel skriving og iverksettingsløsningen er installert i miljøet.</p><p>Denne funksjonen innfører den nye parameteren **Virkemåte for løsningsoppgradering** i prosjektparametere. Når **Bare Lite** er angitt for denne parameteren installerer ikke lenger PDU-er løsningen for dobbel skriving i Project Operations, selv om kjerneløsningen for dobbel skriving og iverksettingsløsningen er installert i miljøet. Denne funksjonaliteten er til nytte for kunder som planlegger å bruke løsninger for dobbel skriving til å integrere salgsordrer i økonomi- og driftsapper, men vil bruke Project Operations i en Lite-modus (det vil si uten integrering i økonomi- og driftsapper).</p> | |

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Fakturering og prising | 2316317 | Systemet tillater at fakturaer opprettes uten belastbare transaksjoner. |
| Fakturering og prising | 2737300 | Valider at Kunde-feltet er tilgjengelig før skjemaet åpnes. |
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
| Ressursbehandling | 2751560 | Inkonsekvente foretrukne organisasjonsenheter i ressurskrav. |
| Utsetting | 2907231 | Prosessfasen for leverandørfakturaer kan ikke gå videre. |
| Tid og utgift | 2867363 | Oppføringer forlater ikke visningen Fravær/ferier for godkjenning når de er i kø for godkjenning. |
| Tid og utgift | 2894405 | TESA: Den ubrukte katalogen for konseptgodkjenning fører til problemer med forskriftssamsvar. |
