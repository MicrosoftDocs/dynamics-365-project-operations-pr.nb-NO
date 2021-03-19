---
title: Bestillinger for et prosjekt
description: Denne artikkelen beskriver de forskjellige metodene du kan bruke til å opprette bestillinger for et prosjekt. Metoden du bruker, er avhengig av formålet med bestillingen, og når de innkjøpte varene forbrukes og belastes på et prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289201"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="4cda8-104">Bestillinger for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="4cda8-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cda8-105">Denne artikkelen beskriver de forskjellige metodene du kan bruke til å opprette bestillinger for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="4cda8-106">Metoden du bruker, er avhengig av formålet med bestillingen, og når de innkjøpte varene forbrukes og belastes på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="4cda8-107">Metoder for å opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="4cda8-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="4cda8-108">Du kan bruke én av følgende metoder til å opprette en bestilling i Prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="4cda8-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="4cda8-109">Formålet med bestillingen avgjør når bestillingen skal forbrukes, og derfor når varer skal belastes til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4cda8-110">Metode</span><span class="sxs-lookup"><span data-stu-id="4cda8-110">Method</span></span></th>
<th><span data-ttu-id="4cda8-111">Formål</span><span class="sxs-lookup"><span data-stu-id="4cda8-111">Purpose</span></span></th>
<th><span data-ttu-id="4cda8-112">Forbruk av varer</span><span class="sxs-lookup"><span data-stu-id="4cda8-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4cda8-113">Opprette en bestilling direkte fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="4cda8-114">Bruk denne metoden for å kjøpe varer fra en ekstern leverandør for forbruk på et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="4cda8-115">Du kan opprette bestillingen på følgende to måter:</span><span class="sxs-lookup"><span data-stu-id="4cda8-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="4cda8-116">Fra selve prosjektet.</span><span class="sxs-lookup"><span data-stu-id="4cda8-116">From the project itself.</span></span> <span data-ttu-id="4cda8-117">I dette tilfellet er prosjektet allerede definert for bestillingen.</span><span class="sxs-lookup"><span data-stu-id="4cda8-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="4cda8-118">Ved å navigere til prosjektbestillingen.</span><span class="sxs-lookup"><span data-stu-id="4cda8-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="4cda8-119">Du må velge både leverandøren og prosjektet som bestillingen skal opprettes for.</span><span class="sxs-lookup"><span data-stu-id="4cda8-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="4cda8-120">Varene forbrukes når leverandørfakturaen oppdateres.</span><span class="sxs-lookup"><span data-stu-id="4cda8-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4cda8-121">Opprett en bestilling fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4cda8-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="4cda8-122">Bruk denne metoden for å kjøpe varer når du oppretter en salgsordre fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="4cda8-123">Varene forbrukes når salgsordren faktureres til kunden.</span><span class="sxs-lookup"><span data-stu-id="4cda8-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4cda8-124">Opprett en bestilling fra et varebehov.</span><span class="sxs-lookup"><span data-stu-id="4cda8-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="4cda8-125">Bruk denne metoden for å kjøpe varer når du oppretter et varebehov fra et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="4cda8-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="4cda8-126">Varer forbrukes når følgeseddelen for varebehovet er oppdatert.</span><span class="sxs-lookup"><span data-stu-id="4cda8-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="4cda8-127">Når du oppdaterer leverandørfakturaen eller følgeseddelen, blir du bedt om å oppdatere følgeseddelen på varebehovet.</span><span class="sxs-lookup"><span data-stu-id="4cda8-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="4cda8-128">Hvis du vil ha mer informasjon, kan du se [Motta varer på bestilling fra varebehov](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="4cda8-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]