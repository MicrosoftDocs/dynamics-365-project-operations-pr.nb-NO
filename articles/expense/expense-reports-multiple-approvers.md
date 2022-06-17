---
title: Utgiftsrapporter og flere godkjennere
description: Denne artikkelen inneholder informasjon om reiseregninger som må godkjennes av flere personer.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 88f42535e4826d1f618bd542eec3b26a6fde1a97
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914470"
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