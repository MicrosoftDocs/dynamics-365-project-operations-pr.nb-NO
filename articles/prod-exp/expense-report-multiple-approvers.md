---
title: Flere godkjennere av en reiseregning
description: Dette emnet gir informasjon om reiseregninger som krever godkjenning fra flere personer.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081776"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Flere godkjennere av en reiseregning

[!include [banner](../includes/banner.md)]

Det kan hende at mer enn én person må godkjenne en reiseregning som er sendt inn av en ansatt, avhengig av organisasjonens godkjenningspolicyer for utgifter. Når du konfigurerer arbeidsflytprosessen for godkjenning av reiseregninger, kan du legge til arbeidsflytelementer som inneholder oppgaver eller trinn for én eller flere godkjennere av reiseregninger. Du kan for eksempel angi at alle reiseregninger skal godkjennes først av lederen til den ansatte som sendte rapporten, og deretter av leverandørgjeld-koordinatoren.

Hvis du bestemmer deg for å kreve flere godkjennere av reiseregninger, kan du legge til arbeidsflytelementene på følgende måter:

- Legg til ett godkjenningselement som har ett trinn. Det kan for eksempel hende at trinnet krever at en reiseregning tilordnes en brukergruppe, og at den godkjennes av 50 prosent av brukergruppens medlemmer.
- Legg til ett godkjenningselement som har flere trinn. Godkjenningselementet kan for eksempel ha følgende trinn:

    1. Lederen av den ansatte som sendte reiseregningen, godkjenner den.
    2. Leverandørgjeld-assistenten verifiserer kvitteringene og reiseregningselementene.
    3. Budsjetteieren godkjenner reiseregningen.

- Legg til flere godkjenningselementer med ett trinn. Du kan for eksempel legge til et separat godkjenningselement for hvert av følgende trinn:

    1. Den ansattes overordnede godkjenner reiseregningen.
    2. Budsjetteieren godkjenner reiseregningen.