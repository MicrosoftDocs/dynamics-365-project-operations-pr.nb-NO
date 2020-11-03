---
title: Personlige utgifter i en utgiftsrapport
description: Dette emnet forklarer de to metodene for håndtering av en arbeiders personlige utgifter i Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081769"
---
# <a name="personal-expenses-on-an-expense-report"></a>Personlige utgifter i en utgiftsrapport

[!include [banner](../includes/banner.md)]

I løpet av en forretningsreise kan arbeidere noen ganger bli belastet for personlige utgifter på firmaets kredittkort. Hvis du ikke definerer en prosess for håndtering av personlige utgifter, kan det hende at godkjennings prosessen for reiseregninger blir forstyrret når de ansatte sender inn de spesifiserte reiseregningene. 

Det finnes to metoder for håndtering av en arbeiders personlige utgifter:

- **Betalt av ansatt** – Organisasjonen betaler ikke personlige utgifter som vises på fakturaen for firmaets kredittkort. I stedet opprettes det en rapport som viser personlige utgifter sammen med firmautgiftene som ble belastet firmaets kredittkort.
- **Betalt av firma** – organisasjonen din betaler hele regningen for firmaets kredittkort, og debiterer deretter arbeiderens konto for de personlige utgiftene.

Du kan velge metoden organisasjonen bruker, på siden **Parametere for utgiftshåndtering**.
