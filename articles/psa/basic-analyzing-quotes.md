---
title: Analyse av prosjekttilbud
description: Dette emnet gir informasjon om analyse av prosjekttilbud.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 0d9cefafcce33297146cae81d9ba7e68ab79aeb6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081736"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="06aeb-103">Analyse av prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="06aeb-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="06aeb-104">Dynamics 365 Project Service Automation analyserer prosjekttilbud for å beregne lønnsomhet.</span><span class="sxs-lookup"><span data-stu-id="06aeb-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="06aeb-105">Det analyseres også hvor godt tilbudet er justert mot kundens forventninger om leveringsdato eller fullføringsdato, og om budsjettbegrensningene.</span><span class="sxs-lookup"><span data-stu-id="06aeb-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="06aeb-106">Lønnsomhetsanalyse</span><span class="sxs-lookup"><span data-stu-id="06aeb-106">Profitability analysis</span></span>

<span data-ttu-id="06aeb-107">Project Service Automation analyserer lønnsomhet ved å bruke bruttofortjenesten og den justerte bruttofortjenesten.</span><span class="sxs-lookup"><span data-stu-id="06aeb-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="06aeb-108">Bruttofortjeneste beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="06aeb-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="06aeb-109">Den justerte bruttofortjenesten beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="06aeb-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="06aeb-110">Hvis verdiene for bruttofortjeneste og justert bruttofortjeneste varierer med en stor margin, blir mye av arbeidet i tilbudet klassifisert som ikke-belastbart.</span><span class="sxs-lookup"><span data-stu-id="06aeb-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="06aeb-111">Analyse av kundeforventninger</span><span class="sxs-lookup"><span data-stu-id="06aeb-111">Analysis of customer expectations</span></span>

<span data-ttu-id="06aeb-112">Du kan analysere tilbud og generere diagrammer for kundeforventninger om tidsplanen og budsjettet hvis du angir verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="06aeb-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="06aeb-113">**Ønsket leveringsdato** -feltet i tilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="06aeb-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="06aeb-114">**Kundebudsjett** -feltet for hver tilbudslinje (for prosjektrelaterte linjer og produktbaserte linjer).</span><span class="sxs-lookup"><span data-stu-id="06aeb-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="06aeb-115">Analyse av kundeforventninger om tidsplanen utføres ved å sammenligne den siste sluttdatoen for tilbudslinjedetaljene med den ønskede leveringsdatoen i alle tilbudslinjene i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="06aeb-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="06aeb-116">Analyse av kundeforventninger til budsjettet gjøres ved å sammenligne summen av det totale kundebudsjettet med det tilbudte beløpet på tvers av alle tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="06aeb-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
