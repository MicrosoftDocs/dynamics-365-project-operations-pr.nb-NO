---
title: Nyheter mai 2021 – Project Operations Lite-distribusjon
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations Lite-distribusjon fra mai 2021.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934194"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Nyheter mai 2021 – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

   - Project Operations på Dataverse-miljø versjon 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- [Planleggingsmoduser](../../project-management/scheduling-modes.md): Prosjektledere kan nå definere om et prosjekt skal administreres ved hjelp av planleggingsmodus med fast varighet, fast arbeid eller faste enheter.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2224568 | Lagt til logikk for å aktivere tilpassinger som involverer aktivering av programtillegget for fakturabekreftelse. |
| Fakturering og prising | 2101098 | Forbedret logikken i standardfelt for proformafaktura. Disse feltene omfatter **Fakturaadresse**, **Fakturanavn** og **Betalingsbetingelser**. Feltene er nå standard fra den tilsvarende kundeoppføringen for prosjektkontrakten. |
| Fakturering og prising | 2021413 | Oppdaterte feltene **Faktisk kostnad** og **Salg** i **Oppgave**-enheten for å inkludere salgsverdier fra ufakturerte og fakturerte utgifter for oppgaver. |
| Fakturering og prising | 2182110 | Når du kopierer en prosjektkontrakt, genereres kontraktlinje-ID-en på nytt i målprosjektkontrakten for å sikre at den er unik. |
| Administrasjon av salgsmulighet | 2186741 | Valideringer som er lagt til for å sikre at **Opprinnelse**-feltet og transaksjonstype ikke kan oppdateres for eksisterende tilbudslinjedetaljer. |
| Administrasjon av salgsmulighet | 2191353 | Milepælsoppretting kan ikke tillates på en kontraktlinje for tid og materialer. |
| Administrasjon av salgsmulighet | 2216956 | Løste problemer med **Oppdater priser**. |
| Planlegging og sporing | 2182979 | Forbedret prosjektkopieringsfunksjonen for å sikre at utgiftsestimatlinjene kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184144 | Forbedret prosjektkopieringsfunksjonen for å sikre at navnet på ressursposisjonen kopieres fra det opprinnelige prosjektet. |
| Planlegging og sporing | 2184799 | Strammet inn kontrollen ved kopiering av et prosjekt for å sikre at den estimerte startdatoen ikke kan endres under kopiering. |
| Planlegging og sporing | 2185134 | Under kopiering av et prosjekt er målprosjektets startdato satt til dagens dato. |
| Planlegging og sporing | 2196373 | Kontroller at prosjektleder- og teammedlemsoppføringer ikke dupliseres i prosjektteamet. under kopiering av et prosjekt. |
| Planlegging og sporing | 2211833 | Ressurstilordninger kopieres fra kildeprosjektoppgaven til målprosjektet. |
| Planlegging og sporing | 2186541 | Løste problemer i **Estimater**-rutenettet ved gruppering etter **Ressurs**. |
| Planlegging og sporing | 2166906 | Transaksjonskategorien fra en oppgave må kopieres til enheten **Ressurstilordning**. |
| Ressursbehandling | 2125362 | Løste problemer med oppretting av et generelt teammedlem ved hjelp av den timesbaserte tildelingsmetoden. |
| Tid og utgift | 2113603 | Løste det tilpassingsrelaterte problemet med å fjerne attributter fra **Tidsregistrering**-siden. Systemet kontrollerer om attributtet finnes på siden før det får tilgang til attributtet ved hjelp av et skript. |
| Tid og utgift | 2204377 | Kopierte timeregistreringer må vises automatisk når du velger **Kopier uke**. |
| Tid og utgift | 2209059 | **Status**-feltet kan redigeres for tidsoppføringer i Dynamics 365 Field Service. |
