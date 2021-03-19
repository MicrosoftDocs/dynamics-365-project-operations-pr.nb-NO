---
title: Løse kostpriser for estimater og faktiske verdier – Lite
description: Dette emnet gir informasjon om hvordan kostpriser for estimater og faktiske beløp løses.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274561"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a><span data-ttu-id="6c7b0-103">Løse kostpriser for estimater og faktiske verdier – Lite</span><span class="sxs-lookup"><span data-stu-id="6c7b0-103">Resolve cost prices on estimates and actuals - lite</span></span>

<span data-ttu-id="6c7b0-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6c7b0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c7b0-105">For å løse kostpriser og kostprislisten for estimater og faktiske verdier bruker systemet informasjonen i feltene **Dato**, **Valuta** og **Kontraktenhet** i det relaterte prosjektet.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="6c7b0-106">Når kostprislisten er løst, løser programmet kostnadssatsen.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="6c7b0-107">Løse kostnadssatser på faktiske og estimerte linjer for tid</span><span class="sxs-lookup"><span data-stu-id="6c7b0-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="6c7b0-108">Estimatlinjer for tid refererer til tilbuds- og kontraktlinjedetaljene for tids- og ressurstilordninger i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="6c7b0-109">Etter at en kostprisliste er løst, blir feltene **Rolle** og **Ressursenhet** på estimatlinjen for Tid samsvart mot rolleprislinjene i prislisten.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="6c7b0-110">Dette samsvaret forutsetter at du bruker standard prissettingsdimensjoner for arbeidskostnad.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="6c7b0-111">Hvis du har konfigurert systemet til å samsvare felter i stedet for, eller i tillegg til **Rolle** og **Ressursenhet**, brukes en annen kombinasjon til å hente en samsvarende rolleprislinje.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="6c7b0-112">Hvis programmet finner en rolleprislinje som har en kostfor kombinasjonen av **Rolle** og **Ressursenhet**, det vil si standard kostpris.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="6c7b0-113">Hvis programmet ikke kan samsvare verdiene for **Rolle** og **Ressursenhet**, henter det rolleprislinjer med en samsvarende rolle, men nullverdier for **Ressursenhet**.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="6c7b0-114">Når det har hentet en samsvarende rolleprisoppføring, blir kostnadssatsen som standard fra denne oppføringen.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="6c7b0-115">Hvis du konfigurerer en annen prioritering av **Rolle** og **Ressursenhet**, eller hvis du har andre dimensjoner som har høyere prioritet, endres denne virkemåten i henhold til dette.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="6c7b0-116">Systemet henter rolleprisoppføringer med verdier som samsvarer med hver av prisdimensjonsverdiene i prioritetsrekkefølgen, med rader som har nullverdier for de dimensjonene som kommer sist.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="6c7b0-117">Løse kostnadssatser på faktiske og estimerte linjer for utgift</span><span class="sxs-lookup"><span data-stu-id="6c7b0-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="6c7b0-118">Estimatlinjer for utgift refererer til tilbuds- og kontraktlinjedetaljene for utgifter og utgiftsestimatlinjene i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="6c7b0-119">Når en kostprisliste er løst, bruker systemet en kombinasjon av feltene **Kategori** og **Enhet** på utgiftsestimatlinjen til å samsvare mot linjene for **Kategoripris** i den løste prislisten.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="6c7b0-120">Hvis systemet finner en kategoriprislinje som har en kostnadssats for kombinasjonen av feltene **Kategori** og **Enhet**, brukes kostnadssatsen som standard.</span><span class="sxs-lookup"><span data-stu-id="6c7b0-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="6c7b0-121">Hvis systemet ikke kan samsvare verdiene for **Kategori** og **Enhet**, eller hvis systemet finner en samsvarende kategoriprislinje, men prissettingsmetoden ikke er **Pris per enhet**, brukes som standard en kostnadssats på null(0).</span><span class="sxs-lookup"><span data-stu-id="6c7b0-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]