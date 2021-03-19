---
title: Analyse av prosjekttilbud
description: Dette emnet gir informasjon om analyse av prosjekttilbud.
author: rumant
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291271"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="48839-103">Analyse av prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="48839-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="48839-104">Dynamics 365 Project Service Automation analyserer prosjekttilbud for å beregne lønnsomhet.</span><span class="sxs-lookup"><span data-stu-id="48839-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="48839-105">Det analyseres også hvor godt tilbudet er justert mot kundens forventninger om leveringsdato eller fullføringsdato, og om budsjettbegrensningene.</span><span class="sxs-lookup"><span data-stu-id="48839-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="48839-106">Lønnsomhetsanalyse</span><span class="sxs-lookup"><span data-stu-id="48839-106">Profitability analysis</span></span>

<span data-ttu-id="48839-107">Project Service Automation analyserer lønnsomhet ved å bruke bruttofortjenesten og den justerte bruttofortjenesten.</span><span class="sxs-lookup"><span data-stu-id="48839-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="48839-108">Bruttofortjeneste beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="48839-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="48839-109">Den justerte bruttofortjenesten beregnes ved å bruke følgende formel:</span><span class="sxs-lookup"><span data-stu-id="48839-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="48839-110">Hvis verdiene for bruttofortjeneste og justert bruttofortjeneste varierer med en stor margin, blir mye av arbeidet i tilbudet klassifisert som ikke-belastbart.</span><span class="sxs-lookup"><span data-stu-id="48839-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="48839-111">Analyse av kundeforventninger</span><span class="sxs-lookup"><span data-stu-id="48839-111">Analysis of customer expectations</span></span>

<span data-ttu-id="48839-112">Du kan analysere tilbud og generere diagrammer for kundeforventninger om tidsplanen og budsjettet hvis du angir verdier for følgende felt:</span><span class="sxs-lookup"><span data-stu-id="48839-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="48839-113">**Ønsket leveringsdato**-feltet i tilbudshodet.</span><span class="sxs-lookup"><span data-stu-id="48839-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="48839-114">**Kundebudsjett**-feltet for hver tilbudslinje (for prosjektrelaterte linjer og produktbaserte linjer).</span><span class="sxs-lookup"><span data-stu-id="48839-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="48839-115">Analyse av kundeforventninger om tidsplanen utføres ved å sammenligne den siste sluttdatoen for tilbudslinjedetaljene med den ønskede leveringsdatoen i alle tilbudslinjene i tilbudet.</span><span class="sxs-lookup"><span data-stu-id="48839-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="48839-116">Analyse av kundeforventninger til budsjettet gjøres ved å sammenligne summen av det totale kundebudsjettet med det tilbudte beløpet på tvers av alle tilbudslinjer.</span><span class="sxs-lookup"><span data-stu-id="48839-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]