---
title: Konfigurere standardkostnader for arbeid og utgifter
description: Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288346"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="9c218-103">Konfigurere standardkostnader for arbeid og utgifter</span><span class="sxs-lookup"><span data-stu-id="9c218-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c218-104">Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9c218-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="9c218-105">Denne oppgaven bruker USSI-datasett.</span><span class="sxs-lookup"><span data-stu-id="9c218-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9c218-106">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.</span><span class="sxs-lookup"><span data-stu-id="9c218-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="9c218-107">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c218-107">Select **New**.</span></span>
3. <span data-ttu-id="9c218-108">Angi en dato i feltet **Effektiv dato**.</span><span class="sxs-lookup"><span data-stu-id="9c218-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="9c218-109">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c218-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9c218-110">Du kan angi en standard kostpris for prosjektkategorien, eller du kan angi en kostpris basert på arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="9c218-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="9c218-111">Kostprisen som brukes, er kostprisen på det høyeste detaljnivået.</span><span class="sxs-lookup"><span data-stu-id="9c218-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="9c218-112">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c218-112">Select **Save**.</span></span>
6. <span data-ttu-id="9c218-113">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.</span><span class="sxs-lookup"><span data-stu-id="9c218-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="9c218-114">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c218-114">Select **New**.</span></span>
8. <span data-ttu-id="9c218-115">Angi en dato i feltet **Effektiv dato**.</span><span class="sxs-lookup"><span data-stu-id="9c218-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="9c218-116">Velt et alternativ i feltet **Gyldig for**.</span><span class="sxs-lookup"><span data-stu-id="9c218-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="9c218-117">Angi et tall i **Priser**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c218-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9c218-118">Du kan angi en standard salgspris for timetransaksjoner eller for en prosjektkategori.</span><span class="sxs-lookup"><span data-stu-id="9c218-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="9c218-119">Du kan også angi salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse.</span><span class="sxs-lookup"><span data-stu-id="9c218-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="9c218-120">Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="9c218-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9c218-121">Hvis det for eksempel er angitt både en generell salgspris og en arbeidsspesifikk salgspris, brukes den arbeidsspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="9c218-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="9c218-122">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c218-122">Select **Save**.</span></span>
12. <span data-ttu-id="9c218-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9c218-123">Close the page.</span></span>
13. <span data-ttu-id="9c218-124">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="9c218-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="9c218-125">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c218-125">Select **New**.</span></span>
15. <span data-ttu-id="9c218-126">Angi en dato i feltet **Effektiv dato**.</span><span class="sxs-lookup"><span data-stu-id="9c218-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="9c218-127">Angi et tall i **Kostpris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c218-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9c218-128">Flere felt kan fylles ut, men dette er minimum som kreves for å lagre oppføringen.</span><span class="sxs-lookup"><span data-stu-id="9c218-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="9c218-129">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c218-129">Select **Save**.</span></span>
18. <span data-ttu-id="9c218-130">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgpris (utgift)**.</span><span class="sxs-lookup"><span data-stu-id="9c218-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="9c218-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c218-131">Select **New**.</span></span>
20. <span data-ttu-id="9c218-132">Angi en dato i feltet **Effektiv dato**.</span><span class="sxs-lookup"><span data-stu-id="9c218-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="9c218-133">Velt et alternativ i feltet **Gyldig for**.</span><span class="sxs-lookup"><span data-stu-id="9c218-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="9c218-134">Angi et tall i **Priser**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c218-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9c218-135">Den faktiske salgsprisen, som brukes når en arbeider angir transaksjoner i en utgiftsjournalen, er salgsprisen med høyest detaljnivå.</span><span class="sxs-lookup"><span data-stu-id="9c218-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9c218-136">Hvis det for eksempel er angitt både en generell og en arbeidsspesifikk salgspris, brukes den arbeidsspesifikke salgsprisen.</span><span class="sxs-lookup"><span data-stu-id="9c218-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="9c218-137">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c218-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]