---
title: Nyheter april 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Dette emnet inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra april 2022.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613281"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter april 2022 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Project Operations i et Dataverse-miljø, versjon 4.41.0.45
- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.26

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Innkjøpskategorier kan ikke brukes i prosjektbestillinger og ventende leverandørfakturaer. For mer informasjon, se [Bruk innkjøpskategorier med prosjektbestillinger og ventende leverandørfakturaer](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Tabellen nedenfor viser tilordningene for dobbel skriving som er endret eller lagt til i mars 2022-versjonen av Project Operations.

| Enhetstilordning | Oppdatert versjon | Kommentarer |
| -------------- | ------------------- | ------------|
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet msdyn\_projectvendorinvoicelines | 1.0.0.4 | Denne tilordningen støtter bruken av innkjøpskategorier med bestillinger og ventende leverandørfakturaer. |

Kjør alltid den nyeste versjonen av tilordningen i miljøet, og aktiver alle relaterte tabelltilordninger når du oppdaterer versjonen av Project Operations Dataverse-løsningen og Finance-løsningen. Enkelte funksjoner fungerer kanskje ikke riktig hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en bruksklar tabelltilordning, bruker du endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem når du starter tilordningen, følger du instruksjonene i delen [Problemer med manglende tabellkolonner i tilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| ------------ | ---------------- | -------------- |
| Tid og utgifter | 2573900 | Funksjonen **Moderne godkjenning** må være aktivert som standard. |
| Fakturering og prising | 2603313 | Rettet en duplikatoppføringsfeil som forhindret at tilbuds- og kontraktlinjer som har et produkt, ble lagt til. |
| Distribusjon og konfigurasjon | 2611368 | Kunder må kunne legge til opptil fem egendefinerte enheter i løsningen ved hjelp av den moderne apputformingen. |
| Tid og utgifter | 2628285 | Løste et problem som påvirket muligheten til å angi riktig ressurskategori under import av tidsinnføring. |
|   Administrasjon av salgsmuligheter| 2628815 | Oppdater tegngrensen for beskrivelsen av tilbudslinjedetaljene slik at den samsvarer med tegngrensen for oppgaveemnet, slik at importen lykkes for oppgaver der emnet har mer enn 100 tegn. |
| Tid og utgifter| 2629547 | **Sendt av**-feltet for prosjektgodkjenninger må peke til brukeren som sendte oppføringen. |
| Tid og utgifter| 2629865 | **Kopier kategori**-feltet for oppgaver når prosjekter kopieres. |
| Tid og utgifter| 2636463 | Reparerte filtrene i godkjenninger i skjemaer for moderne godkjenninger. |
| Prosjektplanlegging og sporing | 2648300 | Løste et problem som hindrer at prosjekteieren blir endret. |
| Fakturering og prising | 2563000 | Journallinjer for et ufakturert salg der valutaen er forskjellig fra kontraktvalutaen, må ikke være tillatt. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

Hvis du vil ha informasjon om feilrettinger som er inkludert i denne oppdateringen, logger du på Microsoft Dynamics Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
