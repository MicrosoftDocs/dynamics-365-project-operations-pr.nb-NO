---
title: Oversikt over produktbaserte kontraktlinjer – Lite
description: Dette emnet inneholder informasjon om produktbasere kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177883"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="55da9-103">Oversikt over produktbaserte kontraktlinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="55da9-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="55da9-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="55da9-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55da9-105">Du kan opprette produktbaserte kontraktlinjer i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="55da9-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="55da9-106">Produktbaserte kontraktlinjer kan være manuelt opprettede linjer, eller de kan være elementer fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="55da9-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="55da9-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="55da9-107">Product catalog</span></span>

<span data-ttu-id="55da9-108">Produktene i produktkatalogen har en standardenhet og enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="55da9-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="55da9-109">Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som også har disse attributtene.</span><span class="sxs-lookup"><span data-stu-id="55da9-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="55da9-110">Alle produktene i en produktserie arver samme attributtsett.</span><span class="sxs-lookup"><span data-stu-id="55da9-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="55da9-111">Et selskap selger for eksempel abonnementslisenser for en ulike typer programvare.</span><span class="sxs-lookup"><span data-stu-id="55da9-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="55da9-112">All abonnementsprogramvare har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="55da9-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="55da9-113">Antall brukere</span><span class="sxs-lookup"><span data-stu-id="55da9-113">Number of users</span></span>
- <span data-ttu-id="55da9-114">Abonnementsvarighet (i måneder)</span><span class="sxs-lookup"><span data-stu-id="55da9-114">Subscription duration (in months)</span></span>

<span data-ttu-id="55da9-115">Hvis du vil opprettholde denne typen katalog, oppretter du en produktfamilie med navnet **Abonnementsprogramvare**.</span><span class="sxs-lookup"><span data-stu-id="55da9-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="55da9-116">Legg til attributtene **Antall brukere** og **Abonnementsvarighet** i produktfamilien.</span><span class="sxs-lookup"><span data-stu-id="55da9-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="55da9-117">Deretter legger du til enkeltprodukter i produktfamilien **Abonnementsprogramvare**.</span><span class="sxs-lookup"><span data-stu-id="55da9-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="55da9-118">Legge til produktkatalogvarer i en prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="55da9-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="55da9-119">Prosjektkontrakter har deler for to linjetyper: prosjektbaserte linjer og produktbaserte linjer.</span><span class="sxs-lookup"><span data-stu-id="55da9-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="55da9-120">Produktbaserte linjer inkluderer alle produktene og enhetene i produktprislisten i kontrakten.</span><span class="sxs-lookup"><span data-stu-id="55da9-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="55da9-121">Produkter som ikke er en del av kontraktens produktprisliste, kan legges til.</span><span class="sxs-lookup"><span data-stu-id="55da9-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="55da9-122">Du kan velge produkter fra andre prislister eller direkte fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="55da9-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="55da9-123">Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet for produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="55da9-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="55da9-124">Hvis det ikke er angitt en standardprisliste, settes prisen til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="55da9-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="55da9-125">Hvis en kontraktlinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i linjen.</span><span class="sxs-lookup"><span data-stu-id="55da9-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="55da9-126">En kontraktlinje har **Priser**-feltet med de to verdiene:</span><span class="sxs-lookup"><span data-stu-id="55da9-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="55da9-127">**Overstyr pris**</span><span class="sxs-lookup"><span data-stu-id="55da9-127">**Override pricing**</span></span>
- <span data-ttu-id="55da9-128">**Bruk standard**</span><span class="sxs-lookup"><span data-stu-id="55da9-128">**Use default**</span></span>

<span data-ttu-id="55da9-129">Hvis du angir **Priser**-feltet til **Overstyr pris**, angis ikke standardprisen.</span><span class="sxs-lookup"><span data-stu-id="55da9-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="55da9-130">Angi en pris for produktet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="55da9-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="55da9-131">Hvis du setter feltet til **Bruk standard**, brukes standard salgspris, og feltet kan ikke redigeres.</span><span class="sxs-lookup"><span data-stu-id="55da9-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="55da9-132">Når du har installert Project Operations, blir standard salgspriser angitt på de produktbasert linjene i en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="55da9-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="55da9-133">**Priser**-feltet angis til **Overstyr pris**, slik at du kan redigere standardprisen på kontraktlinjene.</span><span class="sxs-lookup"><span data-stu-id="55da9-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="55da9-134">Dette er en spesifikk overstyring i Project Operations av virkemåten for produktbaserte linjer i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="55da9-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
