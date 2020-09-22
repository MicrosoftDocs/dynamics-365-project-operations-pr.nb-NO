---
title: Hvorfor settes pris som standard til null i faktiske utgiftskostnader?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktiske utgiftskostnader.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754108"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor settes pris som standard til null i faktiske utgiftskostnader?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse vanlige spørsmålene gjelder for faktiske utgifter der transaksjonsklassen er satt til Utgift og transaksjonstypen er Kostnad.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Feilsøke kostnadssatser i faktiske utgiftskostnader

Gå til oppføringen for relaterte utgifter, og kontroller at det er et beløp i feltet utgiftsoppføring. Hvis den opprinnelige utgiftsoppføringen ikke har fylt ut beløpsfeltet, har du identifisert problemet.
 
Hvis du vil løse dette problemet, oppretter du utgiftsposten på nytt med et gyldig beløp og godkjenner det.
