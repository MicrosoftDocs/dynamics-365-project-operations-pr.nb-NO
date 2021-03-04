---
title: Arbeidsflyt for utgiftshåndtering
description: Dette emnet forklarer hvordan du kan bruke arbeidsflytsystemet i Microsoft Dynamics 365 Finance til å konfigurere en gjennomgangsprosess for reiseregninger i Utgiftshåndtering.
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
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960574"
---
# <a name="expense-management-workflow"></a>Arbeidsflyt for utgiftshåndtering

Du kan bruke arbeidsflytsystemet til å konfigurere en gjennomgangsprosess for reiseregninger i Utgiftshåndtering. Du kan konfigurere en arbeidsflyt som bruker følgende vilkår for å avgjøre hvem som godkjenner reiseregninger:

- Rapporteringshierarkiet for ansatte og forhåndsdefinerte godkjenningsbegrensninger
- Godkjenning på flere nivåer som støtter midlertidige godkjennere og en endelig godkjenner
- Finansdimensjoner og prosjektansvar
- Tilordning til bestemte brukere eller brukergrupper

Arbeidsflytgodkjenninger kan opprettes for reiseregninger, reiserekvisisjoner, forskudd og tilbakebetaling av MVA.

**Eksempel**

Fremgangsmåten nedenfor er et eksempel på arbeidsflyten for en reiseregning i Utgiftshåndtering.

1. En ansatt oppretter og lagrer en reiseregning.
2. Den ansattes sender inn reiseregningen for godkjenning. Godkjenneren identifiseres basert på reglene som ble definert da arbeidsflyten ble konfigurert.
3. Godkjenneren mottar en melding om at en reiseregning er klar til godkjenning. Godkjenneren ser gjennom reiseregningen og kontrollerer at følgende betingelser er oppfylt:

    - Utgiftene bryter ikke utgiftspolicyer. Hvis en utgiftspolicy brytes, kontrollerer godkjenneren at reiseregningen inkluderer en gyldig forretningsmessig begrunnelse.
    - Elektroniske kvitteringer knyttes til reiseregningen.

4. Godkjenneren godkjenner reiseregningen.
5. Reiseregning tilordnes til koordinatoren for leverandørgjeld for postering.
6. Ett av følgende trinn inntreffer, avhengig av om automatisk postering er konfigurert:

    - Hvis automatisk postering er konfigurert, blir reiseregningen behandlet for betaling, og statusen for reiseregningen oppdateres.
    - Hvis automatisk postering ikke er konfigurert, kontrollerer koordinatoren for leverandørgjeld at alle originalkvitteringer er sendt, og at kvitteringene er i samsvar med utgiftene i reiseregningen. Alle avgiftskoder som angis i reiseregningen, må også verifiseres som riktige.

Når disse kravene er bekreftet oppfylt, blir reiseregningen postert.

Når reiseregningen er postert, blir betalingen godkjent for reiseregningen, og den ansatte blir refundert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]