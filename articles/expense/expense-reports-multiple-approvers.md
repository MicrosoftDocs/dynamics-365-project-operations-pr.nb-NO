---
title: Utgiftsrapporter og flere godkjennere
description: Dette emnet gir informasjon om reiseregninger som krever at flere enn én person må godkjennes.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897103"
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
