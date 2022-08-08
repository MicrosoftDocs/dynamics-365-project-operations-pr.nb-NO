---
title: Funksjoner som er fjernet eller avskrevet i Dynamics 365 Project Operations
description: Denne artikkelen beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028341"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funksjoner som er fjernet eller avskrevet i Dynamics 365 Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering, og Project Operations for lagerførte/produksjonsbaserte scenarioer_

Denne artikkelen beskriver funksjoner som er fjernet eller som er planlagt for fjerning fra Dynamics 365 Project Operations.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling, og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å ta hensyn til disse fjerningene og avskrivningene for din egen planlegging.

> [!NOTE]
> Detaljert informasjon om objekter i økonomi- og driftsapper finnes i [**Tekniske referanserapporter**](/dynamics/s-e/global/axtechrefrep_61). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av økonomi- og driftsapper.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Fjernede eller avskrevne funksjoner i Project Operations mars 2022-utgivelse

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parameteren "Opprett alltid justeringstransaksjon" i Prosjektstyring og regnskap

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsaken til avskriving/fjerning** | Justeringstransaksjoner kreves for revisjonsformål. Etter avskrivning blir denne parameteren skjult. Systemet oppretter alltid justeringstransaksjoner, akkurat som det for øyeblikket gjør når parameteren er satt til **Ja**. |
| **Erstattet av en annen funksjon?** | No |
| **Berørte produktområder** | App |
| **Distribusjonsalternativ** | Project Operations for produksjons-/lagerførte scenarioer |
| **Status** | Avskrevet: Innen 1. mars 2023 vil vi skjule parameteren og endre systemfunksjonaliteten, slik at justeringstransaksjoner alltid opprettes. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parameteren "Bruk justeringsdato som ny prosjektdato" i Prosjektstyring og regnskap

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsaken til avskriving/fjerning** | Denne parameteren ble opprinnelig brukt til å tillate justeringer når en regnskapsperiode lukkes. Den er imidlertid ikke lenger nødvendig fordi regnskapsdatoen for transaksjonen kan endres til den første datoen i den åpne perioden, hvis dette er konfigurert. Prosjektdatoen må ikke endres fordi den representerer datoen da transaksjonen ble inntraff. |
| **Erstattet av en annen funksjon?** | No |
| **Berørte produktområder** | App |
| **Distribusjonsalternativ** | Project Operations for produksjons-/lagerførte scenarioer |
| **Status** | Avskrevet: Innen 1. mars 2023 vil vi skjule parameteren og endre systemfunksjonaliteten, slik at prosjektdatoen aldri endres i justeringer. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Arbeidsflyten for ressursforespørsel i Project Operations for lagerførte/produksjonsbaserte scenarioer

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsaken til avskriving/fjerning** | Avskrevet på grunn av lav bruk og begrensninger i transaksjonsvolum. |
| **Erstattet av en annen funksjon?** | No |
| **Berørte produktområder** | App |
| **Distribusjonsalternativ** | Project Operations for produksjons-/lagerførte scenarioer |
| **Status** | Avskrevet: Innen 1. mars 2023 deaktiveres alternativet for å be om ressurser for prosjektet ved hjelp av arbeidsflyten. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Siden Prosjektfakturaforslag uten overskrifts- og linjevisninger

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsaken til avskriving/fjerning** | Avskrevet på grunn av forbedringer på siden som ble innført sammen med funksjonsnøkkelen **Bruk prosjektfakturaforslag og fakturajournalskjemaene med hode- og linjevisning**. |
| **Erstattet av en annen funksjon?** | Ja |
| **Berørte produktområder** | App |
| **Distribusjonsalternativ** | Project Operations for produksjons-/lagerførte scenarioer, Project Operations for ressursbaserte/ikke-lagerførte scenarioer |
| **Status** | Avskrevet: Innen 1. mars 2023 vil vi deaktivere den tidligere (eldre) siden og aktivere funksjonsnøkkelen **Bruk prosjektfakturaforslag og fakturajournalskjemaene med hode- og linjevisning** som standard. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Fjernede eller avskrevne funksjoner i Project Operations desember 2021-utgivelse

### <a name="collaboration-workspaces"></a>Samarbeidsarbeidsområder

[Opprette eller koble til et arbeidsområde for samarbeid (Project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Årsaken til avskriving/fjerning** | Avskrevet på grunn av lav bruk. Kunder som bruker Project Operations for ressurs-/ikke lagerførte scenarioer, kan bruke [Samarbeid med Office Groups](../project-management/collaboration-groups.md). |
| **Erstattet av en annen funksjon?** | No |
| **Berørte produktområder** | App  |
| **Distribusjonsalternativ** | Project Operations for produksjons-/lagerførte scenarioer |
| **Status** | Avskrevet: Innen 1. desember 2022 planlegger vi ikke lenger å støtte arbeidsområder for samarbeid. |
