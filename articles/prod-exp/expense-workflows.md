---
title: Konfigurere arbeidsflyter for utgiftshåndtering
description: Du kan sette opp en arbeidsflytprosess for å gjennomgå og godkjenne reise- og utgiftsdokumenter.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081774"
---
# <a name="set-up-expense-management-workflows"></a>Konfigurere arbeidsflyter for utgiftshåndtering

[!include [banner](../includes/banner.md)]

Du kan sette opp en arbeidsflytprosess som brukes til å gjennomgå og godkjenne reise- og utgiftsdokumenter. Dokumentene som arbeidsflyter kan defineres for, inkluderer reiseregninger, reiserekvisisjoner og forespørsler om forskudd.

En arbeidsflyt representerer en forretningsprosess. Den definerer hvordan et dokument flyter gjennom systemet, og viser hvem som må fullføre en oppgave eller godkjenne et dokument. Det er flere fordeler ved å bruke arbeidsflytsystemet i organisasjonen:

-   **Konsistente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter. Ved å bruke arbeidsflytsystemet bidrar du til å sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.

-   Prosess-synlighet – Du kan spore måledata for status, logg og ytelse for en bestemt arbeidsflytforekomst. Dette gjør det mulig for deg å fastsette om endringer skal utføres i arbeidsflyten for å forbedre effektiviteten.

-   Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og godkjenningene som er tilordnet dem. 

**Typene arbeidsflyter du kan opprette**

Tabellen nedenfor viser hvilke typer arbeidsflyter du kan opprette i **Utgift**.


|              <strong>Type</strong>              |                   <strong>Bruk denne typen til å</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Utgiftsrapport</strong>         |            Opprette arbeidsflyter for godkjenning av reiseregninger.             |
|  <strong>Automatisk bokføring av reiseregning</strong>   |        Opprette arbeidsflyter for automatisk bokføring av reiseregninger.        |
|       <strong>Utgiftslinjeelement</strong>        |     Opprette arbeidsflyter for godkjenning av linjeelementer i reiseregninger.      |
| <strong>Automatisk postering av utgiftslinjeelement</strong> | Opprette arbeidsflyter for automatisk postering av linjeelementer i reiseregninger. |
|       <strong>Reiserekvisisjon</strong>       |          Opprette arbeidsflyter for godkjenning av reiserekvisisjoner.           |
|      <strong>Forespørsel om kontantforskudd</strong>      |         Opprette arbeidsflyter for godkjenning av forespørsler om kontantforskudd.          |
|        <strong>Mva-fradrag</strong>        | Opprette arbeidsflyter for godkjenning av Mva-fradrag.  |
