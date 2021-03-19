---
title: Utgiftsrapporter og flere godkjennere
description: Dette emnet gir informasjon om reiseregninger som krever at flere enn én person må godkjennes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9b9826c89e9deb870adb053f82bd049906f56052
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276540"
---
# <a name="expense-reports-and-multiple-approvers"></a>Utgiftsrapporter og flere godkjennere

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Det kan hende at mer enn én person må godkjenne en sendt reiseregning, avhengig av organisasjonens godkjenningspolicyer for utgifter. Når du konfigurerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for én eller flere godkjennere av reiseregninger. Du kan for eksempel angi at alle reiseregninger skal godkjennes av to separate personer, lederen av den ansatte som sendte rapporten, og leverandørgjeld-koordinatoren.

Hvis du bestemmer deg for å kreve flere godkjennere av reiseregninger, kan du legge til arbeidsflytelementene på følgende måter:

- Legg til ett godkjenningselement som har ett trinn. Det kan for eksempel hende at trinnet krever at en reiseregning tilordnes en brukergruppe, og at den godkjennes av 50 prosent av brukergruppens medlemmer.
- Legg til ett godkjenningselement som har flere trinn. Godkjenningselementet kan for eksempel ha følgende trinn:

    1. Lederen av den ansatte som sendte reiseregningen, godkjenner den.
    2. Leverandørgjeld-assistenten verifiserer kvitteringene og reiseregningselementene.
    3. Budsjetteieren godkjenner reiseregningen.

- Legg til flere godkjenningselementer med ett trinn. Du kan for eksempel legge til et separat godkjenningselement for hvert av følgende trinn:

    1. Den ansattes overordnede godkjenner reiseregningen.
    2. Budsjetteieren godkjenner reiseregningen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]