---
title: Nyheter i desember 2021 – Project Operations Lite-distribusjon
description: Dette emnet inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations Lite-distribusjon fra desember 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942989"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Nyheter i desember 2021 – Project Operations Lite-distribusjon

_Gjelder: Lite-distribusjon – avtale til proformafakturering_

Dette emnet gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

### <a name="subcontract-management"></a>Administrasjon av underkontrakt 

- [Underordnede prosjektteammedlemmer](../subcontracting/subcontracting-project-team-members.md): En prosjektleder kan opprette navngitte eller generiske teammedlemmer med underkontrakter og underkontraktslinjer for å påvirke bemanning og beregning.
- [Alternativer for underleverandør for prosjektteammedlemmer](../subcontracting/subcon-options.md): Når de tar bemanningsvalg for navngitte eller generiske prosjektteammedlemmer, kan prosjektlederen se gjennom eksisterende underkontrakter eller opprette nye underkontrakter for ett eller flere prosjektteammedlemmer. 
- [Kostnadsberegning av underkontrakterte ressurstilordninger](../subcontracting/costing-subcon-ra.md): Prosjektkostnadsberegning tar hensyn til underleverandørressurstilordninger og vil kostnadsbelegge dem ved hjelp av innkjøpsprislistene som er tilknyttet underkontraktene. 
- [Konfigurere planleggingstavlen for å vise kontraktarbeidere og underkontraktkapasitet](../subcontracting/configure-sb-subcon.md): Planleggingstavlen i Project Operations kan nå konfigureres til å søke etter og foreslå kontraktarbeidertype for reserverbare ressurser og underleverandørkapasitet sammen med ansatte. Denne konfigurasjonen kan brukes når du søker etter ressurser innenfor konteksten for bemanning etter et bestemt prosjektkrav, eller når du søker utenfor konteksten for et prosjektkrav.
- [Bemanning av et prosjekt med kontraktarbeidere og underkontraktkapasitet](../subcontracting/staffing-cw.md): Kontraktarbeidere kan nå bestilles på prosjekter som utnytter erfaringer fra planleggingstavler.
- [Registrering av tid, utgifter og materialbruk på prosjekter for underkontraktkomponenter](../subcontracting/recording-subcon-actuals.md): Kontraktarbeidere kan registrere tid og utgifter, og prosjektteammedlemmer kan også registrere bruk av materiell kjøpt ved hjelp av en underkontrakt på et prosjekt. Dette vil føre til at du registrerer nøyaktige kostnader på prosjekter som bruker kjøpt kapasitet eller materiell.
- [Tilstandsoverganger på en underkontrakt](../subcontracting/subcon-states.md): Underkontrakter kan bekreftes for å fullføre forhandlinger med leverandøren, lukkes for å indikere at leveringen er fullført, eller kanselleres for å angi at kontrakten skal avsluttes med leverandøren før leveringen er fullført.

### <a name="task-planning"></a>Oppgaveplanlegging
- Forbedret feilsøking for systemadministratorer. Når en bruker ikke kan åpne et prosjekt, kan administratoren se gjennom ikke-lisensrelaterte feil generert fra Project for the Web, i [Logger for prosjektplanlegging](../../project-management/schedule-api-logs.md).
- [Bruk sjekklister for oppgaver i Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). I Microsoft Project for the Web kan du legge til en sjekkliste for en oppgave for å holde oversikt over bestemte elementer.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Planlegging og sporing | 2392596 | API-er for tidsplan tillater nå oppdateringer av feltene **Gjenværende innsats**, **Fullført innsats** og **% fullført**. |
| Planlegging og sporing | 2478497 | Feltene **Aktivitetsnummer** og **Oppgave-ID** for API-er for tidsplan kan være tomme når de legges inn, fordi de fylles ut med automatisk nummerering.|
| Tid og utgift | 2468135 | Antall godkjenningssøk er redusert fra fem til tre. |
| Tid og utgift | 2468188 | Løste problemet med loggtekst som overskred maksimumslengden i **notetext**-attributtet for **merknad**-enheten. |
