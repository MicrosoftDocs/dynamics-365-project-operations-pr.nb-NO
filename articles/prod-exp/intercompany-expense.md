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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960844"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="ffedb-103">Konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="ffedb-103">Intercompany expenses</span></span>

<span data-ttu-id="ffedb-104">En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="ffedb-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="ffedb-105">Du kan bruke konserninterne utgifter til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for.</span><span class="sxs-lookup"><span data-stu-id="ffedb-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="ffedb-106">Den juridiske enheten som bruker arbeideren, kalles den utlånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ffedb-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="ffedb-107">Den juridiske enheten som arbeideren påløper kostnader for, kalles den lånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ffedb-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="ffedb-108">Før en arbeider kan opprette og sende inn selskapets utgifter, må du aktivere linjer for selskapets utgifter.</span><span class="sxs-lookup"><span data-stu-id="ffedb-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="ffedb-109">I den juridiske enheten for utlån på siden **Parametere for utgiftshåndtering** velger du **Tillat linjer for konsernintern utgift**.</span><span class="sxs-lookup"><span data-stu-id="ffedb-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="ffedb-110">Avgiftspostering for konserninterne utgifter</span><span class="sxs-lookup"><span data-stu-id="ffedb-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffedb-111">Før du kan bruke avgiftsgrupper som er knyttet til den juridiske enheten for utlån (kilde) i stedet for den juridiske enheten (målet) i reiseregningen, må du aktivere funksjonaliteten i oppsettet av salgsavgift i økonomimodulen.</span><span class="sxs-lookup"><span data-stu-id="ffedb-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="ffedb-112">Når parameteren **Juridisk enhet for konsernintern avgiftsbokføring** er satt til **Kilde** og **Bruk avgiftsregler for mva** er satt til **Nei**, brukes avgiftskombinasjonen for den juridisk enheten for utlån.</span><span class="sxs-lookup"><span data-stu-id="ffedb-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="ffedb-113">Når den samme parameteren er satt til **Mål**, brukes avgiftskombinasjonen for den lånende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="ffedb-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="ffedb-114">Når det gjelder juridiske enheter i USA, når parameteren er angitt til **Kilde**, må feltet **Mva-fordringer** også konfigureres på den nye siden **Bokføringsgrupper i hovedbok**.</span><span class="sxs-lookup"><span data-stu-id="ffedb-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="ffedb-115">Regnskapsmotoren bruker informasjonen fra dette feltet for avgiftsrelatert regnskapsregistrering.</span><span class="sxs-lookup"><span data-stu-id="ffedb-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="ffedb-116">Funksjonaliteten er konsekvent for utgiftslinjer som er bokført med eller uten et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ffedb-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
