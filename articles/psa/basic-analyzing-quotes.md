---
title: Analyse av prosjekttilbud
description: Dette emnet gir informasjon om analyse av prosjekttilbud.
author: rumant
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
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012463"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="67520-103">Analyse av prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="67520-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="67520-104">Dynamics 365 Project Service Automation analyserer prosjekttilbud for å beregne lønnsomhet.</span><span class="sxs-lookup"><span data-stu-id="67520-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="67520-105">Det analyseres også hvor godt tilbudet er justert mot kundens forventninger om leveringsdato eller fullføringsdato, og om budsjettbegrensningene.</span><span class="sxs-lookup"><span data-stu-id="67520-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="67520-106">Lønnsomhetsanalyse</span><span class="sxs-lookup"><span data-stu-id="67520-106">Profitability analysis</span></span>

<span data-ttu-id="67520-107">Project Service Automation analyserer lønnsomhet ved å bruke bruttofortjenesten og den justerte bruttofortjenesten.</span><span class="sxs-lookup"><span data-stu-id="67520-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="67520-108">Bruttofortjeneste beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="67520-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="67520-109">Den justerte bruttofortjenesten beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="67520-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="67520-110">Hvis verdiene for bruttofortjeneste og justert bruttofortjeneste varierer med en stor margin, blir mye av arbeidet i tilbudet klassifisert som ikke-belastbart.</span><span class="sxs-lookup"><span data-stu-id="67520-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="67520-111">Analyse av kundeforventninger</span><span class="sxs-lookup"><span data-stu-id="67520-111">Analysis of customer expectations</span></span>

<span data-ttu-id="67520-112">Du kan analysere tilbud og generere diagrammer for kundeforventninger om tidsplanen og budsjettet hvis du angir verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="67520-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="67520-113">**Ønsket leveringsdato**-feltet i tilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="67520-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="67520-114">**Kundebudsjett**-feltet for hver tilbudslinje (for prosjektrelaterte linjer og produktbaserte linjer).</span><span class="sxs-lookup"><span data-stu-id="67520-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="67520-115">Analyse av kundeforventninger om tidsplanen utføres ved å sammenligne den siste sluttdatoen for tilbudslinjedetaljene med den ønskede leveringsdatoen i alle tilbudslinjene i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="67520-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="67520-116">Analyse av kundeforventninger til budsjettet gjøres ved å sammenligne summen av det totale kundebudsjettet med det tilbudte beløpet på tvers av alle tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="67520-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]