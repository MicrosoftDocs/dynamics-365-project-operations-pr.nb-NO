---
title: Konfigurere intern prosjektfakturering
description: Dette emnet viser hvordan du definerer prosjektfakturering mellom to selskaper i organisasjonen.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081679"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="c6e88-103">Konfigurere intern prosjektfakturering</span><span class="sxs-lookup"><span data-stu-id="c6e88-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6e88-104">Dette emnet viser hvordan du definerer prosjektfakturering mellom to selskaper i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="c6e88-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="c6e88-105">Denne oppgaven bruker USSI-datasett.</span><span class="sxs-lookup"><span data-stu-id="c6e88-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="c6e88-106">I navigasjonsruten går du til **Moduler > Leverandørgjelde > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c6e88-107">I listen **Alle leverandører** finner og velger du ønsket oppføring.</span><span class="sxs-lookup"><span data-stu-id="c6e88-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="c6e88-108">Velg **Generelt** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="c6e88-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="c6e88-109">Velg **Konsernintern**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="c6e88-110">Sett **Aktiv** til **Ja** for å aktivere konserninternt salg.</span><span class="sxs-lookup"><span data-stu-id="c6e88-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="c6e88-111">Skriv inn eller velg en verdi i **Kundefirma** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="c6e88-112">Skriv inn eller velg en verdi i **Min konto** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="c6e88-113">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-113">Select **Save**.</span></span>
9. <span data-ttu-id="c6e88-114">Lukk sidene for å gå tilbake til startsiden.</span><span class="sxs-lookup"><span data-stu-id="c6e88-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="c6e88-115">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="c6e88-116">Velg kategorien **Konsernintern**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="c6e88-117">Flytt glidebryteren til **Ja** for å aktivere planlegging og timelister for konsernintern ressurs.</span><span class="sxs-lookup"><span data-stu-id="c6e88-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="c6e88-118">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c6e88-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="c6e88-119">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-119">Select **New**.</span></span>
15. <span data-ttu-id="c6e88-120">Skriv inn eller velg en verdi i **Juridisk enhet som låner** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="c6e88-121">Merk av for **Avsett inntekt**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="c6e88-122">Skriv inn eller velg en verdi i **Standard timeregistreringskategori** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="c6e88-123">Skriv inn eller velg en verdi i **Standard utgiftskategori** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="c6e88-124">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-124">Select **Save**.</span></span>
20. <span data-ttu-id="c6e88-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c6e88-125">Close the page.</span></span>
21. <span data-ttu-id="c6e88-126">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Bokføring > Finansposteringsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="c6e88-127">I feltet **Finanskontotyper** velger du et alternativ.</span><span class="sxs-lookup"><span data-stu-id="c6e88-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="c6e88-128">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-128">Select **New**.</span></span>
24. <span data-ttu-id="c6e88-129">I feltet **Hovedkonto** i den nye raden angir du ønskede verdier.</span><span class="sxs-lookup"><span data-stu-id="c6e88-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="c6e88-130">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-130">Select **Save**.</span></span>
26. <span data-ttu-id="c6e88-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c6e88-131">Close the page.</span></span>
27. <span data-ttu-id="c6e88-132">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Overføringspris**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="c6e88-133">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-133">Select **New**.</span></span>
29. <span data-ttu-id="c6e88-134">Angi en dato i feltet **Effektiv dato**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="c6e88-135">Skriv inn eller velg en verdi i **Juridisk enhet som låner** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="c6e88-136">Velg et alternativ i feltet **Overføringsprismodell**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="c6e88-137">Angi et tall i **Priser** -feltet.</span><span class="sxs-lookup"><span data-stu-id="c6e88-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="c6e88-138">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c6e88-138">Select **Save**.</span></span>

