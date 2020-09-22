---
title: Produktbaserte tilbudslinjer
description: Dette emnet inneholder informasjon om produktbasere tilbudslinjer.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 76b90c95-1b3a-4704-a13f-9d7099b83f4c
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: d8bb36fbfe8d01aa26faf5515ca218ad836126b7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754096"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="4a8dc-103">Produktbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="4a8dc-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="4a8dc-104">Du kan opprette produktbaserte tilbudslinjer i Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="4a8dc-105">Produktbaserte tilbudslinjer kan være "innskrevne" linjer, eller de kan være elementer fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4a8dc-106">Produktkatalog</span><span class="sxs-lookup"><span data-stu-id="4a8dc-106">Product catalog</span></span>

<span data-ttu-id="4a8dc-107">Produktene i en Dynamics 365-produktkatalog har en standardenhet og enhetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="4a8dc-108">Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som også har disse attributtene.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="4a8dc-109">Alle produktene i en produktserie arver samme attributtsett.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="4a8dc-110">Et selskap selger for eksempel abonnementslisenser for en rekke typer programvare.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="4a8dc-111">All abonnementsprogramvare har følgende to attributter:</span><span class="sxs-lookup"><span data-stu-id="4a8dc-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4a8dc-112">Antall brukere</span><span class="sxs-lookup"><span data-stu-id="4a8dc-112">Number of users</span></span> 
- <span data-ttu-id="4a8dc-113">Abonnementsvarighet (i måneder)</span><span class="sxs-lookup"><span data-stu-id="4a8dc-113">Subscription duration (in months)</span></span>

<span data-ttu-id="4a8dc-114">En god måte å opprettholde denne typen katalog på, er å opprette en produktserie kalt **Abonnementsprogramvare**, og som har **Antall brukere** og **Abonnementsvarighet** som attributter.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="4a8dc-115">Du kan deretter legge til enkeltprodukter, for eksempel **Dynamics 365 Sales** eller **Dynamics 365 Field Service** i produktserien **Abonnementsprogramvare**.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4a8dc-116">Legge til produktkatalogvarer i et prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="4a8dc-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="4a8dc-117">Sider med prosjekttilbud og prosjektkontrakter har deler for to linjetyper: prosjektbaserte linjer og produktbaserte linjer.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="4a8dc-118">For produktbaserte linjer brukes Dynamics 365 til å legge til varer fra en produktkatalog i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="4a8dc-119">Rullegardinlisten på tilbudslinjen eller prosjektkontraktlinjen inkluderer alle produkter og enheter i produktprislisten som er knyttet til tilbudet eller prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="4a8dc-120">Du kan også legge til produkter som ikke er del av tilbudets produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="4a8dc-121">Du kan også velge produkter fra andre prislister, eller du kan velge produkter direkte fra produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="4a8dc-122">Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet til å hente produktets salgspris.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4a8dc-123">Hvis det ikke er angitt en standardprisliste, settes prisen til 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4a8dc-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="4a8dc-124">Hvis en tilbudslinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4a8dc-125">Vær oppmerksom på at en tilbudslinje i Dynamics 365 har et **Prising**-felt.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="4a8dc-126">To verdier er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="4a8dc-126">Two values are available:</span></span>

- <span data-ttu-id="4a8dc-127">Overstyr pris</span><span class="sxs-lookup"><span data-stu-id="4a8dc-127">Override pricing</span></span>  
- <span data-ttu-id="4a8dc-128">Bruk standard</span><span class="sxs-lookup"><span data-stu-id="4a8dc-128">Use default</span></span>

<span data-ttu-id="4a8dc-129">Hvis du angir dette feltet til **Overstyr pris**, angir ikke Dynamics 365 en standardpris.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="4a8dc-130">Du må angi en pris for produktet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4a8dc-131">Hvis du angir dette feltet til **Bruk standard**, bruker Dynamics 365 standard salgspris og låser feltet for å forhindre redigering.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="4a8dc-132">Når du har installert PSA, angis det standard salgspriser på de produktbasert linjene i et tilbud.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="4a8dc-133">**Pris**-feltet angis deretter til **Overstyr pris**, slik at du kan redigere standardprisen på tilbudslinjene.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Angi Overstyr pris](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="4a8dc-135">Antallsfaktorer for produkter</span><span class="sxs-lookup"><span data-stu-id="4a8dc-135">Quantity factors for products</span></span>

<span data-ttu-id="4a8dc-136">PSA bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="4a8dc-137">Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på tilbuds- eller prosjektkontraktlinjen som antall brukermåneder.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="4a8dc-138">Vanligvis lagres prisen på abonnementsprogramvaren i katalogen som prisen per bruker per måned.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="4a8dc-139">Du kan imidlertid bruke andre tidsbeskrivelser i stedet.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="4a8dc-140">I løpet av salgsprosessen er prisen på tilbudslinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av IT-salgsrepresentanten.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="4a8dc-141">Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="4a8dc-142">Antallet som brukes til å beregne beløpet for tilbudslinjen, er et produkt av antall brukere og antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="4a8dc-143">PSA har innført konseptet antallsfaktorer for å støtte denne typen salg.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="4a8dc-144">Antallsfaktorer er avhengig av produktattributter i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="4a8dc-145">Når du konfigurerer bestemte egenskaper for et produkt, kan du bruke PSA til å flagge et delsett av disse egenskapene, eller alle egenskapene, som antall faktorer.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="4a8dc-146">PSA validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="4a8dc-147">Når et produkt som antallsfaktorer er konfigurert for, blir lagt til på en tilbudslinje, blir **Antall**-feltet på tilbuds linjen et skrivebeskyttet felt.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="4a8dc-148">Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner PSA antallet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="4a8dc-149">Dynamics 365 kan for eksempel ha følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="4a8dc-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="4a8dc-150">**Antall brukere** – antall brukere</span><span class="sxs-lookup"><span data-stu-id="4a8dc-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="4a8dc-151">**Antall måneder** – antall abonnementsmåneder</span><span class="sxs-lookup"><span data-stu-id="4a8dc-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="4a8dc-152">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="4a8dc-152">**Product SKU**</span></span> 

<span data-ttu-id="4a8dc-153">Egenskapene **Antall brukere** og **Antall måneder** kan flagges som antallsfaktorer ved å redigere egenskapene for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="4a8dc-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Flagge Antall brukere og Antall måneder som kvalitetsfaktorer](media/basic-guide-11.png)
 
