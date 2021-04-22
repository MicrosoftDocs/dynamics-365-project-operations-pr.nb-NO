---
title: Produktprislister
description: Dette emnet gir informasjon om prislistene i katalogprising som brukes for prosjekttilbud og kontrakter.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877502"
---
# <a name="product-price-lists"></a><span data-ttu-id="3aa26-103">Produktprislister</span><span class="sxs-lookup"><span data-stu-id="3aa26-103">Product price lists</span></span>

<span data-ttu-id="3aa26-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3aa26-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="3aa26-105">I Project Operations støtter **Produktprislister** og relaterte prislisteelementenheter funksjonalitet for prising av produkter på produktbaserte tilbuds- og kontraktlinjer.</span><span class="sxs-lookup"><span data-stu-id="3aa26-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="3aa26-106">For produkter som brukes i prosjekter, brukes prislisteelementoppføringene for prosjektprislister.</span><span class="sxs-lookup"><span data-stu-id="3aa26-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="3aa26-107">Produkter bør settes opp slik at de har standard kostnads- og prislister i produkt katalogen.</span><span class="sxs-lookup"><span data-stu-id="3aa26-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="3aa26-108">Bruk listeprisen, standardkostnaden og gjeldende kostnad for å konfigurere standard kostnader og listepriser.</span><span class="sxs-lookup"><span data-stu-id="3aa26-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="3aa26-109">Standard listeprisene brukes på en tilbudslinje eller en prosjektkontraktlinje når systemet ikke finner en prislistelinje for produktet i produktprislisten for tilbudet eller prosjektkontrakten.</span><span class="sxs-lookup"><span data-stu-id="3aa26-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="3aa26-110">Kostprisen for produktkataloglinjer kan endres mellom tilbud.</span><span class="sxs-lookup"><span data-stu-id="3aa26-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="3aa26-111">Denne funksjonen er viktig fordi hvis du ikke kan spore kostnader nøyaktig, kan du ikke fastsette driftsfortjeneste på prosjektforhandlinger.</span><span class="sxs-lookup"><span data-stu-id="3aa26-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="3aa26-112">Som standard er standardkostnaden for produktet brukt som kostprisen.</span><span class="sxs-lookup"><span data-stu-id="3aa26-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="3aa26-113">Standard kostpris kan imidlertid oppdateres i tilbudslinjen hvis det er en annen kostnadspris for det aktuelle tilbudet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="3aa26-114">Prislisteelementer</span><span class="sxs-lookup"><span data-stu-id="3aa26-114">Price list items</span></span>

<span data-ttu-id="3aa26-115">Du kan legge til produkter fra en produktkatalog i forskjellige prislister.</span><span class="sxs-lookup"><span data-stu-id="3aa26-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="3aa26-116">Prislistelinjer for produkter refererer alltid til en bestemt enhet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="3aa26-117">Priser for et produkt i prislisteelementer kan konfigureres som et valutabeløp.</span><span class="sxs-lookup"><span data-stu-id="3aa26-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="3aa26-118">De kan også konfigureres som en funksjon av listepris, løpende kostnad eller standardkostnad.</span><span class="sxs-lookup"><span data-stu-id="3aa26-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="3aa26-119">Prisingsfunksjonalitet støtter ulike avrundingsalternativer når produktpriser konfigureres som en funksjon av listepris, standardkostnad eller løpende kostnad.</span><span class="sxs-lookup"><span data-stu-id="3aa26-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="3aa26-120">I tillegg til å dra nytte av flere prisingsmetoder og avrundingsalternativer kan du knytte rabattlister til prislisteelementer.</span><span class="sxs-lookup"><span data-stu-id="3aa26-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="3aa26-121">Standard produktprisliste</span><span class="sxs-lookup"><span data-stu-id="3aa26-121">Default product price list</span></span>
<span data-ttu-id="3aa26-122">Hver kundeoppføring har et **Standard prisliste**-felt der du kan angi en prisliste som samsvarer med kundens valuta.</span><span class="sxs-lookup"><span data-stu-id="3aa26-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="3aa26-123">Det blir ikke automatisk lagt inn en standardverdi i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="3aa26-124">Når en egendefinert prisavtale med en bestemt kunde finnes, kan du bruke dette feltet til å knytte en prisliste til den aktuelle kunden.</span><span class="sxs-lookup"><span data-stu-id="3aa26-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="3aa26-125">Enhetene Salgsmulighet, Tilbud og Prosjektkontrakt bruker følgende rekkefølge til å angi standard prislister for produkter.</span><span class="sxs-lookup"><span data-stu-id="3aa26-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="3aa26-126">Den samme rekkefølgen brukes for prosjektprislister.</span><span class="sxs-lookup"><span data-stu-id="3aa26-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="3aa26-127">Tilbud</span><span class="sxs-lookup"><span data-stu-id="3aa26-127">Quote</span></span>
2.  <span data-ttu-id="3aa26-128">Salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="3aa26-128">Opportunity</span></span>
3.  <span data-ttu-id="3aa26-129">Kunde</span><span class="sxs-lookup"><span data-stu-id="3aa26-129">Customer</span></span>
4.  <span data-ttu-id="3aa26-130">Globale innstillinger</span><span class="sxs-lookup"><span data-stu-id="3aa26-130">Global settings</span></span> 

<span data-ttu-id="3aa26-131">**Produkt**-feltet på tilbudslinjen viser som standard alle de aktive produktene i produktprislisten for tilbudet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="3aa26-132">Hvis et produkt er deaktivert, eller det er et utkastprodukt, vises det ikke, selv om det er i prislisten.</span><span class="sxs-lookup"><span data-stu-id="3aa26-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="3aa26-133">Produktkataloglinjer legges til som fakturalinjer på den første fakturaen som opprettes for en prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="3aa26-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="3aa26-134">Disse fakturalinjene kan slettes på et fakturautkast.</span><span class="sxs-lookup"><span data-stu-id="3aa26-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="3aa26-135">I slike tilfeller vil linjene vises på en etterfølgende faktura til de faktureres eller til fakturaen sendes til kunden.</span><span class="sxs-lookup"><span data-stu-id="3aa26-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="3aa26-136">Du kan ikke fakturere et delvist antall av en produktfakturalinje.</span><span class="sxs-lookup"><span data-stu-id="3aa26-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="3aa26-137">Når produktlinjene fra prosjektkontrakten faktureres, opprettes faktiske verdier.</span><span class="sxs-lookup"><span data-stu-id="3aa26-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="3aa26-138">De faktiske verdiene blir imidlertid ikke koblet til den relaterte prosjektenheten.</span><span class="sxs-lookup"><span data-stu-id="3aa26-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="3aa26-139">Med andre ord er produktbaserte prosjektkontraktlinjer uavhengige av prosjektbasert forbruk.</span><span class="sxs-lookup"><span data-stu-id="3aa26-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
