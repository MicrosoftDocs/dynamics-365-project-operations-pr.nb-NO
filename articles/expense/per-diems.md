---
title: Kostgodtgjørelser
description: Dette emnet gir informasjon om reglene for kostgodtgjørelse som brukes i Utgiftshåndtering.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908432"
---
# <a name="per-diems"></a><span data-ttu-id="67616-103">Kostgodtgjørelser</span><span class="sxs-lookup"><span data-stu-id="67616-103">Per diems</span></span>

<span data-ttu-id="67616-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="67616-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="67616-105">En kostgodtgjørelse er en godtgjørelse som betales til en arbeider som er på arbeidsreise.</span><span class="sxs-lookup"><span data-stu-id="67616-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="67616-106">I Utgiftshåndtering kan du opprette regler for kostgodtgjørelse for forskjellige reisesituasjoner.</span><span class="sxs-lookup"><span data-stu-id="67616-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="67616-107">Kostgodtgjørelsessatser kan baseres på tiden på året, reisestedet eller begge deler.</span><span class="sxs-lookup"><span data-stu-id="67616-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="67616-108">Når du oppretter en kostgodtgjørelsesregel, kan du angi at en prosentsats av kostgodtgjørelsessatsen skal tilbakeholdes hvis en arbeider mottar gratis måltider eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="67616-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="67616-109">Du kan også angi et minimum og maksimum antall timer som kostgodtgjørelsessatsen kan gjelde for en arbeiders reise.</span><span class="sxs-lookup"><span data-stu-id="67616-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="67616-110">Konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="67616-110">Configuration</span></span> 

1. <span data-ttu-id="67616-111">Hvis du vil legge til kostgodtgjørelser, går du til **Oppsett** > **Beregninger og koder** > **Steder for kostgodtgjørelse**.</span><span class="sxs-lookup"><span data-stu-id="67616-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="67616-112">For hvert av stedene som er lagt til over, velger du en kostgodtgjørelse og en valuta som er gyldig mellom en bestemt start- og sluttdato, for hotell, måltider og andre utgifter.</span><span class="sxs-lookup"><span data-stu-id="67616-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="67616-113">Kostgodtgjørelsessatser og valutaer konfigureres under **Oppsett** > **Beregninger og koder** > **Kostgodtgjørelser**.</span><span class="sxs-lookup"><span data-stu-id="67616-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="67616-114">På siden **Steder for kostgodtgjørelse** konfigurerer du kostgodtgjørelsesnivåene.</span><span class="sxs-lookup"><span data-stu-id="67616-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="67616-115">Kostgodtgjørelsesnivåer gir deg mulighet til å definere prosentandelen av en daglig grense for hotell, måltid og andre utgifter.</span><span class="sxs-lookup"><span data-stu-id="67616-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="67616-116">Hvis du vil angi måltidsprosentreduksjonen for frokost, lunsj eller middag, må du oppdatere feltene på siden **Parametere for utgiftshåndtering** i kategorien **Kostgodtgjørelse**.</span><span class="sxs-lookup"><span data-stu-id="67616-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="67616-117">Sende utgifter med kostgodtgjørelse</span><span class="sxs-lookup"><span data-stu-id="67616-117">Submit expenses using per diem</span></span>
<span data-ttu-id="67616-118">Hvis du vil sende utgifter ved hjelp av kostgodtgjørelse, bruker du utgiftskategorien **Kostgodtgjørelse** når du oppretter en reiseregning.</span><span class="sxs-lookup"><span data-stu-id="67616-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="67616-119">Angi **Kostgodtgjørelse fra dato**, **Kostgodtgjørelse til dato** og **Sted for kostgodtgjørelse**.</span><span class="sxs-lookup"><span data-stu-id="67616-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="67616-120">Beløpet beregnes basert på kostgodtgjørelsessatsene for den valgte lokasjonen, og måltidsreduksjonen beregnes basert på kostgodtgjørelsesnivåene.</span><span class="sxs-lookup"><span data-stu-id="67616-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
