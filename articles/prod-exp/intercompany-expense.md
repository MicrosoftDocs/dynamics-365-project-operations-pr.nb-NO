---
title: Konserninterne utgifter
description: Dette emnet inneholder informasjon om hvordan du bruker selskapets utgifter til å tilordne en arbeiders utgifter til den juridiske enheten som arbeidet ble utført for.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271545"
---
# <a name="intercompany-expenses"></a>Konserninterne utgifter

En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen. Du kan bruke konserninterne utgifter til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for. Den juridiske enheten som bruker arbeideren, kalles den utlånende juridiske enheten. Den juridiske enheten som arbeideren påløper kostnader for, kalles den lånende juridiske enheten. 

Før en arbeider kan opprette og sende inn selskapets utgifter, må du aktivere linjer for selskapets utgifter. I den juridiske enheten for utlån på siden **Parametere for utgiftshåndtering** velger du **Tillat linjer for konsernintern utgift**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Avgiftspostering for konserninterne utgifter

[!include [banner](../includes/banner.md)]

Før du kan bruke avgiftsgrupper som er knyttet til den juridiske enheten for utlån (kilde) i stedet for den juridiske enheten (målet) i reiseregningen, må du aktivere funksjonaliteten i oppsettet av salgsavgift i økonomimodulen. Når parameteren **Juridisk enhet for konsernintern avgiftsbokføring** er satt til **Kilde** og **Bruk avgiftsregler for mva** er satt til **Nei**, brukes avgiftskombinasjonen for den juridisk enheten for utlån. Når den samme parameteren er satt til **Mål**, brukes avgiftskombinasjonen for den lånende juridiske enheten. Når det gjelder juridiske enheter i USA, når parameteren er angitt til **Kilde**, må feltet **Mva-fordringer** også konfigureres på den nye siden **Bokføringsgrupper i hovedbok**. Regnskapsmotoren bruker informasjonen fra dette feltet for avgiftsrelatert regnskapsregistrering.   
Funksjonaliteten er konsekvent for utgiftslinjer som er bokført med eller uten et prosjekt.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]