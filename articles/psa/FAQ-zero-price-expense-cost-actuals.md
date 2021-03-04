---
title: Hvorfor settes pris som standard til null i faktiske utgiftskostnader?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktiske utgiftskostnader.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146360"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="08424-103">Hvorfor settes pris som standard til null i faktiske utgiftskostnader</span><span class="sxs-lookup"><span data-stu-id="08424-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="08424-104">Disse vanlige spørsmålene gjelder for faktiske utgifter der transaksjonsklassen er satt til Utgift og transaksjonstypen er Kostnad.</span><span class="sxs-lookup"><span data-stu-id="08424-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="08424-105">Feilsøke kostnadssatser i faktiske utgiftskostnader</span><span class="sxs-lookup"><span data-stu-id="08424-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="08424-106">Gå til oppføringen for relaterte utgifter, og kontroller at det er et beløp i feltet utgiftsoppføring.</span><span class="sxs-lookup"><span data-stu-id="08424-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="08424-107">Hvis den opprinnelige utgiftsoppføringen ikke har fylt ut beløpsfeltet, har du identifisert problemet.</span><span class="sxs-lookup"><span data-stu-id="08424-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="08424-108">Hvis du vil løse dette problemet, oppretter du utgiftsposten på nytt med et gyldig beløp og godkjenner det.</span><span class="sxs-lookup"><span data-stu-id="08424-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
