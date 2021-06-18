---
title: Hvorfor settes pris som standard til null i faktiske utgiftskostnader?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktiske utgiftskostnader.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 03c958635dec66b0f243872dfb929eba6a20119b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5992798"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>Hvorfor settes pris som standard til null i faktiske utgiftskostnader

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse vanlige spørsmålene gjelder for faktiske utgifter der transaksjonsklassen er satt til Utgift og transaksjonstypen er Kostnad.

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>Feilsøke kostnadssatser i faktiske utgiftskostnader

Gå til oppføringen for relaterte utgifter, og kontroller at det er et beløp i feltet utgiftsoppføring. Hvis den opprinnelige utgiftsoppføringen ikke har fylt ut beløpsfeltet, har du identifisert problemet.
 
Hvis du vil løse dette problemet, oppretter du utgiftsposten på nytt med et gyldig beløp og godkjenner det.


[!INCLUDE[footer-include](../includes/footer-banner.md)]