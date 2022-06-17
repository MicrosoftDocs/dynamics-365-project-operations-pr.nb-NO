---
title: Tilordningsversjoner av dobbel skriving for Project Operations
description: Denne artikkelen inneholder listen over tilordninger med dobbel skriving som kreves for Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee0b6a1722405e6a50c42db6bd2a25b872c6118c
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959448"
---
# <a name="project-operations-dual-write-map-versions"></a>Tilordningsversjoner av dobbel skriving for Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Bruk av Dynamics 365 Project Operations for ressurs/ikke-lagerførte scenarioer krever et sett med tilordninger for dobbeltskriving for å kjøre i miljøet. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Nødvendige tilordninger: ordningsløsning for dobbel skriving

Følgende tilordninger kreves for Project Operations-løsningen: Sørg for at du kjører tilordningene i tabellen nedenfor og relaterte tabelltilordninger i miljøet.

| Tabelltilordning | Første synkronisering |
| --- | --- |
| Finans (msdyn_ledgers) | Krever første synkronisering for tabelltilordningen og alle forhåndskrav. Masteren for første synkronisering er økonomi- og driftsapper. |
| Juridiske enheter (cdm_companies) | Ikke obligatorisk. Systemet fyller ut denne enheten automatisk ut når miljøer kobles ved hjelp av dobbeltskriving. |
| Kunder V3 (kontoer) | Ikke nødvendig for klargjøring. |
| Leverandør V2 (msdyn_vendors) | Ikke nødvendig for klargjøring. |

1. Fra listen over tilordninger velger du tilordningen Finans **(msdyn\_ledgers)** med alle dens krav, og deretter merker du av for **Første synkronisering**. I feltet **Hovedoppføring for første synkronisering** velger du **Økonomi- og driftsapper** for både hovedboktilordningen og alle forutsetningstilordninger. Velg **Kjør**.

![Synkronisering av finanstilordning.](media/DW6.png)

2. Følg de samme trinnene for alle gjenværende tabelltilordninger som er oppført i tabellen ovenfor. Ikke merk av for **Første synkronisering** når du kjører disse tilordningene.

## <a name="project-operations-dual-write-maps"></a>Tilordninger for dobbel skriving for Project Operations

Følgende tilordninger kreves for en Project Operations-løsning. Tilordningsversjoner av dobbel skriving vises med oppdateringen mai 2021 for Project Operations, versjon 4.10.0.186.

| Enhetstilordning | Nyeste versjon | Første synkronisering | Nødvendig Dynamics 365 Finance-versjon |
| --- | --- | --- | --- |
| Integreringsenhet for prosjekttransaksjonsrelasjoner (msdyn\_transactionconnections) | 1.0.0.0 | Ikke nødvendig for klargjøring. ||
| Prosjektkontrakthoder (salgsordrer) | 1.0.0.1 | Ikke nødvendig for klargjøring. ||
| Prosjektkontraktlinjer (salgsordredetaljer) | 1.0.0.0 | Ikke nødvendig for klargjøring. ||
| Prosjektfinansieringskilde (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Ikke nødvendig for klargjøring. ||
| Project Operations-integreingstabell for materialestimater (msdyn\_estimatelines) | 1.0.0.0 | Ikke nødvendig for klargjøring. ||
| Prosjektfakturaforslag V2 (fakturaer) | 1.0.0.3 | Ikke nødvendig for klargjøring. ||
| Faktiske verdier for Project Operations-integrering (msdyn_actuals) | 1.0.0.14 | Ikke nødvendig for klargjøring. ||
| Milepæler for prosjektkontraktlinje for Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Ikke nødvendig for klargjøring. ||
| Integreringsenhet for kostnadsestimater for Project Operations (msdyn_estimatelines) | 1.0.0.2 | Ikke nødvendig for klargjøring. ||
| Enhet for timesestimater for Project Operations-integrering (msdyn_resourceassignments) | 1.0.0.5 | Ikke nødvendig for klargjøring. ||
| Eksportenhet for prosjektutgiftskategorier for Project Operations-integrering (msdyn_expensecategories) | 1.0.0.1 | Ikke nødvendig for klargjøring. ||
| Eksportenhet for prosjektutgifter for Project Operations-integrering (msdyn_expenses) | 1.0.0.3 | Ikke nødvendig for klargjøring. ||
| Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn_projectvendorinvoices) | 1.0.0.1 | Ikke nødvendig for klargjøring. |10.0.26 eller senere|
| Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Ikke nødvendig for klargjøring. | 10.0.26 eller senere |
| Prosjektressursroller for alle selskaper (bookableresourcecategories) | 1.0.0.1 | Krever en første synkronisering for tabelltilordningen for å synkronisere ressursrollene for prosjektleder og teammedlem som fylles ut i Dynamics 365 Dataverse-miljøet under klargjøring. Dataverse er hovedkilden for den første synkroniseringen. ||
| Prosjektoppgaver (msdyn_projecttasks) | 1.0.0.4 | Ikke nødvendig for klargjøring. ||
| Prosjekttransaksjonskategorier (msdyn_transactioncategories) | 1.0.0.0 | Ikke nødvendig for klargjøring. ||
| Prosjekter V2 (msdyn_projects) | 1.0.0.2 | Ikke nødvendig for klargjøring. ||

Fullfør fremgangsmåten nedenfor for å kjøre de oppførte tilordningene.

1. Aktiver prosjektressursrollene for **alle firmaer (bookableresourcecategories)**-tabelltilordningen siden denne tilordningen krever den første synkroniseringen. I feltet **Hovedoppføring for første synkronisering** velger du **Common Data Service**. 

 ![Synkronisering av tabelltilordning for ressursrolle.](media/6ResourceInitialSync.jpg)

 Vent til statusen for tilordningen **kjører** før du går til neste trinn.

2. Velg alle de resterende obligatoriske tilordningene. Du kan filtrere dem i listen over tilordninger med dobbel skriving ved hjelp av nøkkelordet **Prosjekt** i søk i øvre høyre hjørne. Du kan velge alle tilordninger og deretter kjøre. Hvis du vil ha mer informasjon, kan du se [Behandle flere tabelltilordninger](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Sørg for at du også aktiverer og kjører relaterte enhetstilordninger.

### <a name="project-operations-dual-write-map-versions"></a>Tilordningsversjoner av dobbel skriving for Project Operations

Kjør alltid den nyeste versjonen av tilordningen i miljøet. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis noen av følgende betingelser finnes:

- En tilordning er ikke aktivert.
- Den nyeste versjonen av tilordningen er ikke aktivert. 
- Relaterte tabelltilordninger er ikke aktivert.

Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjoner**, velge den siste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
