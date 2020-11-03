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
# <a name="intercompany-expenses"></a><span data-ttu-id="ee8e8-104">Konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="ee8e8-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee8e8-105">En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="ee8e8-106">I slike tilfeller kan du bruke funksjonen for konsernintern utgift til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="ee8e8-107">Den juridiske enheten som bruker arbeideren, kalles den utlånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="ee8e8-108">Den juridiske enheten som arbeideren påløper kostnader for, kalles den lånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="ee8e8-109">Før en arbeider kan opprette og sende utgifter for arbeid som er utført for en annen juridisk enhet, må du gå til siden **Parametere for utgiftshåndtering** og velge **Tillat konserninterne utgiftslinjer**.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="ee8e8-110">Avgiftspostering for konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="ee8e8-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee8e8-111">Hvis du vil bruke avgiftsgrupper som er knyttet til den utlånende juridiske enheten (kilden) i stedet for den lånende juridiske enheten lånes (målet) i reiseregningen, må du konfigurere dette i mva-oppsett i hovedboken.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="ee8e8-112">Når parameteren **Juridisk enhet for bokføring av konsernintern mva** i hovedboken er angitt til **Kilde** og **Bruk skatteregler for mva** er angitt til **Nei** , brukes avgiftskombinasjonen for den utlånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="ee8e8-113">Når den samme parameteren er satt til **Mål** , brukes avgiftskombinasjonen for den lånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="ee8e8-114">Når det gjelder juridiske enheter i USA, når parameteren er angitt til **Kilde** , må feltet **Mva-fordringer** også konfigureres på den nye siden **Bokføringsgrupper i hovedbok**.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="ee8e8-115">Regnskapsmotoren bruker informasjonen fra dette feltet for avgiftsrelatert regnskapsregistrering.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="ee8e8-116">Funksjonaliteten er konsekvent for utgiftslinjer som er bokført med eller uten et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ee8e8-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
