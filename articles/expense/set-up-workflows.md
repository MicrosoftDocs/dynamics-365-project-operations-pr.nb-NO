---
title: Konfigurere arbeidsflyter for reiseregning og utlegg
description: Du kan sette opp en arbeidsflytprosess som brukes til å gjennomgå og godkjenne reise- og utgiftsdokumenter.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081647"
---
# <a name="set-up-workflows-for-expense-management"></a>Konfigurere arbeidsflyter for reiseregning og utlegg

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan sette opp en arbeidsflytprosess for å gjennomgå og godkjenne reise- og utgiftsdokumenter. Du kan definere arbeidsflyter for reiseregninger, reiserekvisisjoner og forespørsler om forskudd.

En arbeidsflyt representerer en forretningsprosess og definerer hvordan et dokument flyter gjennom systemet. Arbeidsflyten angir også hvem som må fullføre en oppgave eller godkjenne et dokument. Det er flere fordeler ved å bruke arbeidsflytsystemet i organisasjonen:

- **Konsistente prosesser** : Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter. Ved å bruke arbeidsflytsystemet bidrar du til å sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.
- **Prosess-synlighet** : Du kan spore måledata for status, logg og ytelse for en bestemt arbeidsflytforekomst. Dette gjør det mulig for deg å fastsette om endringer skal utføres i arbeidsflyten for å forbedre effektiviteten.
- **Sentralisert arbeidsliste** : Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og godkjenningene som er tilordnet dem. 

## <a name="workflow-types"></a>Arbeidsflyttyper

Tabellen nedenfor viser hvilke typer arbeidsflyter du kan opprette i **Reiseregning og utlegg**.


|              <strong>Type</strong>              |                   <strong>Bruk denne typen til å</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatisk goodkjenning av reiseregninger</strong> |            Opprette arbeidsflyter for godkjenning av reiseregninger.             |
|  <strong>Automatisk bokføring av reiseregning</strong>   |        Opprette arbeidsflyter for automatisk bokføring av reiseregninger.        |
|       <strong>Utgiftslinjeelement</strong>        |     Opprette arbeidsflyter for godkjenning av linjeelementer i reiseregninger.      |
| <strong>Automatisk postering av utgiftslinjeelement</strong> | Opprette arbeidsflyter for automatisk postering av linjeelementer i reiseregninger. |
|       <strong>Reiserekvisisjon</strong>       |          Opprette arbeidsflyter for godkjenning av reiserekvisisjoner.           |
|      <strong>Forespørsel om kontantforskudd</strong>      |         Opprette arbeidsflyter for godkjenning av forespørsler om kontantforskudd.          |
|        <strong>Mva-fradrag</strong>        | Opprette arbeidsflyter for godkjenning av Mva-fradrag.  |
