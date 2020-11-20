---
title: Oversikt over produktbaserte tilbudslinjer – Lite
description: Dette emnet inneholder informasjon om arbeid med produktbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178200"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="78afd-103">Oversikt over produktbaserte tilbudslinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="78afd-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="78afd-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="78afd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="78afd-105">Du kan opprette produktbaserte tilbudslinjer i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="78afd-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="78afd-106">Produktbaserte tilbudslinjer kan være manuelt lagt til, eller de kan være elementer fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="78afd-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="78afd-107">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="78afd-107">Product catalog</span></span>

<span data-ttu-id="78afd-108">Hvert produkt i produktkatalogen har en standardenhet og enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="78afd-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="78afd-109">Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som deler disse attributtene.</span><span class="sxs-lookup"><span data-stu-id="78afd-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="78afd-110">Et selskap selger for eksempel abonnementslisenser for en ulike typer programvare.</span><span class="sxs-lookup"><span data-stu-id="78afd-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="78afd-111">All abonnementsprogramvare har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="78afd-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="78afd-112">Antall brukere</span><span class="sxs-lookup"><span data-stu-id="78afd-112">Number of users</span></span>
- <span data-ttu-id="78afd-113">En abonnementsvarighet målt i måneder</span><span class="sxs-lookup"><span data-stu-id="78afd-113">A subscription duration measured in months</span></span>

<span data-ttu-id="78afd-114">For å opprettholde denne typen katalog må du opprette en produktserie kalt **Abonnementsprogramvare** og legge til et antall brukere og abonnementsvarighet som attributter.</span><span class="sxs-lookup"><span data-stu-id="78afd-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="78afd-115">Deretter kan du legge til enkeltprodukter i **Abonnementsprogramvare**-produktserien.</span><span class="sxs-lookup"><span data-stu-id="78afd-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="78afd-116">Legge til produktkatalogvarer i et prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="78afd-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="78afd-117">Sidene **Prosjekttilbud** og **Prosjektkontrakt** har deler for prosjektbaserte linjer og produktbaserte linjer.</span><span class="sxs-lookup"><span data-stu-id="78afd-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="78afd-118">For produktbaserte linjer inkluderer rullegardinlisten på tilbudslinjen eller prosjektkontraktlinjen inkluderer alle produkter og enheter i produktprislisten.</span><span class="sxs-lookup"><span data-stu-id="78afd-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="78afd-119">Du kan også legge til produkter som ikke er del av produktprislisten.</span><span class="sxs-lookup"><span data-stu-id="78afd-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="78afd-120">Du kan også velge produkter fra andre prislister, eller direkte fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="78afd-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="78afd-121">Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet til å hente produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="78afd-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="78afd-122">Hvis det ikke er angitt en standardprisliste, settes prisen til null (0).</span><span class="sxs-lookup"><span data-stu-id="78afd-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="78afd-123">Når en tilbudslinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="78afd-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="78afd-124">En tilbudslinje i **Priser**-feltet med to tilgjengelige verdier:</span><span class="sxs-lookup"><span data-stu-id="78afd-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="78afd-125">**Overstyr pris**</span><span class="sxs-lookup"><span data-stu-id="78afd-125">**Override Pricing**</span></span>
- <span data-ttu-id="78afd-126">**Bruk standard**</span><span class="sxs-lookup"><span data-stu-id="78afd-126">**Use Default**</span></span>

<span data-ttu-id="78afd-127">Hvis du velger **Overstyr pris**, blir ikke standardprisen angitt.</span><span class="sxs-lookup"><span data-stu-id="78afd-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="78afd-128">I stedet må du angi en pris for produktet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="78afd-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="78afd-129">Hvis du velger **Bruk standard**, brukes standard salgspris, og feltet låses for redigering.</span><span class="sxs-lookup"><span data-stu-id="78afd-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="78afd-130">Standard salgspriser angis på de produktbasert linjene i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="78afd-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="78afd-131">**Pris**-feltet angis deretter til **Overstyr pris**, slik at du kan redigere standardprisen på tilbudslinjene.</span><span class="sxs-lookup"><span data-stu-id="78afd-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="78afd-132">Dette er en Project Operations-spesifikk overstyring til den produktbaserte linjefunksjonaliteten i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="78afd-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
