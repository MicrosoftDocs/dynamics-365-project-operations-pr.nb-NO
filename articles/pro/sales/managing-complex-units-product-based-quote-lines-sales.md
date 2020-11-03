---
title: Administrasjon av komplekse enheter, for eksempel per bruker, per måned for produktbaserte tilbudslinjer
description: Dette emnet gir informasjon om administrasjon av komplekse enheter for produktbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081552"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="993f8-103">Administrasjon av komplekse enheter, for eksempel per bruker, per måned for produktbaserte tilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="993f8-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="993f8-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="993f8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="993f8-105">Dynamics 365 Project Operations bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter.</span><span class="sxs-lookup"><span data-stu-id="993f8-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="993f8-106">Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på tilbuds- eller prosjektkontraktlinjen som antall brukermåneder.</span><span class="sxs-lookup"><span data-stu-id="993f8-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="993f8-107">Vanligvis lagres prisen på abonnementsprogramvaren i katalogen som prisen per bruker per måned.</span><span class="sxs-lookup"><span data-stu-id="993f8-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="993f8-108">I løpet av salgsprosessen er prisen på tilbudslinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av IT-salgsrepresentanten.</span><span class="sxs-lookup"><span data-stu-id="993f8-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="993f8-109">Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="993f8-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="993f8-110">Antallet som brukes til å beregne tilbudslinjen, er et produkt av antall brukere og antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="993f8-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="993f8-111">Project Operations har innført konseptet antallsfaktorer for å støtte denne typen salg.</span><span class="sxs-lookup"><span data-stu-id="993f8-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="993f8-112">Antallsfaktorer er avhengig av produktattributter i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="993f8-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="993f8-113">Når du konfigurerer bestemte egenskaper for et produkt, kan du bruke Project Operations til å flagge et delsett av, eller alle egenskapene, som antall faktorer.</span><span class="sxs-lookup"><span data-stu-id="993f8-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="993f8-114">Project Operations validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="993f8-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="993f8-115">Når du legger til et produkt med antallsfaktorer i en tilbudslinje, **Antall** -feltet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="993f8-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="993f8-116">Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner Project Operations antallet på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="993f8-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="993f8-117">Dynamics 365 Sales kan for eksempel ha følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="993f8-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="993f8-118">**Antall brukere** : Antall brukere</span><span class="sxs-lookup"><span data-stu-id="993f8-118">**No of users** : The number of users</span></span>
- <span data-ttu-id="993f8-119">**Antall måneder** : Antall abonnementsmåneder</span><span class="sxs-lookup"><span data-stu-id="993f8-119">**No of Months** : The number of subscription months</span></span>
- <span data-ttu-id="993f8-120">**Produkt-SKU**</span><span class="sxs-lookup"><span data-stu-id="993f8-120">**Product SKU**</span></span>

<span data-ttu-id="993f8-121">Du kan flagge egenskapene **Antall brukere** og **Antall måneder** som antallsfaktorer ved å redigere egenskapene for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="993f8-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="993f8-122">Følg denne fremgangsmåten for å opprette antallsfaktorer fra produktegenskaper:</span><span class="sxs-lookup"><span data-stu-id="993f8-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="993f8-123">I den venstre navigasjonsruten i Project Operations går du til **Salg** > **Produkter**.</span><span class="sxs-lookup"><span data-stu-id="993f8-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="993f8-124">Åpne produktet du må konfigurere antallsfaktorer for.</span><span class="sxs-lookup"><span data-stu-id="993f8-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="993f8-125">Kontroller at produktet har egenskaper som allerede er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="993f8-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="993f8-126">På siden **Prosjektinformasjon** for produktet velger du kategorien **Antallsfaktorer**.</span><span class="sxs-lookup"><span data-stu-id="993f8-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="993f8-127">I delrutenettet velger du **+ Ny feltberegning**.</span><span class="sxs-lookup"><span data-stu-id="993f8-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="993f8-128">Angi navnet på antallsfaktoren, og velg egenskapsverdien som tilordnes feltberegningen.</span><span class="sxs-lookup"><span data-stu-id="993f8-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="993f8-129">Lagre og lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="993f8-129">Save and close the form.</span></span> <span data-ttu-id="993f8-130">Gjenta disse trinnene for alle egenskaper som skal brukes til å beregne antallet for den produktbaserte tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="993f8-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="993f8-131">Når du oppretter en produktbasert tilbudslinje for et produkt, blir antallet på tilbudslinjen låst.</span><span class="sxs-lookup"><span data-stu-id="993f8-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="993f8-132">Antallet beregnes som et produkt av egenskapsverdiene som du har lagt inn for tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="993f8-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>
