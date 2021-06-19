---
title: Motta varer på bestilling fra varebehov
description: Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011698"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="54ba0-103">Motta varer på bestilling fra varebehov</span><span class="sxs-lookup"><span data-stu-id="54ba0-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="54ba0-104">Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="54ba0-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="54ba0-105">Ved å bruke et varebehov i stedet for en varetransaksjon kan du planlegge levering rett før varen faktisk brukes, opprette en bestilling, inkludere varen i handelsavtalestrukturen og inkludere varebehovet i produksjonsplanlegging.</span><span class="sxs-lookup"><span data-stu-id="54ba0-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="54ba0-106">Denne oppgaven bruker USSI-datasett.</span><span class="sxs-lookup"><span data-stu-id="54ba0-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="54ba0-107">I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="54ba0-108">I listen velger du koblingen i den ønskede raden.</span><span class="sxs-lookup"><span data-stu-id="54ba0-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="54ba0-109">Velg **Plan** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="54ba0-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="54ba0-110">Velg **Elementkrav**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="54ba0-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-111">Select **New**.</span></span>
6. <span data-ttu-id="54ba0-112">Skriv inn eller velg en verdi i feltet **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="54ba0-113">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54ba0-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="54ba0-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-114">Select **Save**.</span></span>
9. <span data-ttu-id="54ba0-115">Velg **Behandle** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="54ba0-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="54ba0-116">Velg **Funksjoner**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-116">Select **Functions**.</span></span>
11. <span data-ttu-id="54ba0-117">Velg **Opprett bestilling**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="54ba0-118">Merk av for **Inkluder alle**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="54ba0-119">Skriv inn eller velg en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="54ba0-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="54ba0-120">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-120">Select **OK**.</span></span>
15. <span data-ttu-id="54ba0-121">I navigasjonsruten går du til **Moduler > Leverandørgjeld > Bestillinger > Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="54ba0-122">I listen velger du koblingen i den ønskede raden.</span><span class="sxs-lookup"><span data-stu-id="54ba0-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="54ba0-123">Velg **Kjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="54ba0-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="54ba0-124">Velg **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="54ba0-125">Velg **Motta** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="54ba0-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="54ba0-126">Velg **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="54ba0-127">Skriv inn en verdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="54ba0-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="54ba0-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]