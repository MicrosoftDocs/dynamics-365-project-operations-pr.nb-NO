---
title: Konserninterne utgifter
description: En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen. I slike tilfeller kan du bruke funksjonen for konsernintern utgift til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081771"
---
# <a name="intercompany-expenses"></a>Konserninterne utgifter

[!include [banner](../includes/banner.md)]

En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen. I slike tilfeller kan du bruke funksjonen for konsernintern utgift til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for. Den juridiske enheten som bruker arbeideren, kalles den utlånende juridiske enheten. Den juridiske enheten som arbeideren påløper kostnader for, kalles den lånende juridiske enheten. 

Før en arbeider kan opprette og sende utgifter for arbeid som er utført for en annen juridisk enhet, må du gå til siden **Parametere for utgiftshåndtering** og velge **Tillat konserninterne utgiftslinjer**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Avgiftspostering for konserninterne utgifter

[!include [banner](../includes/banner.md)]

Hvis du vil bruke avgiftsgrupper som er knyttet til den utlånende juridiske enheten (kilden) i stedet for den lånende juridiske enheten lånes (målet) i reiseregningen, må du konfigurere dette i mva-oppsett i hovedboken. Når parameteren **Juridisk enhet for bokføring av konsernintern mva** i hovedboken er angitt til **Kilde** og **Bruk skatteregler for mva** er angitt til **Nei** , brukes avgiftskombinasjonen for den utlånende juridiske enheten. Når den samme parameteren er satt til **Mål** , brukes avgiftskombinasjonen for den lånende juridiske enheten. Når det gjelder juridiske enheter i USA, når parameteren er angitt til **Kilde** , må feltet **Mva-fordringer** også konfigureres på den nye siden **Bokføringsgrupper i hovedbok**. Regnskapsmotoren bruker informasjonen fra dette feltet for avgiftsrelatert regnskapsregistrering.   
Funksjonaliteten er konsekvent for utgiftslinjer som er bokført med eller uten et prosjekt.  
