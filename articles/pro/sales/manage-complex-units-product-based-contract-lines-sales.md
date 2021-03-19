---
title: Administrere komplekse enheter for produktbaserte kontraktlinjer – Lite
description: Dette emnet inneholder informasjon om hvordan du kan støtte salg av abonnementsbaserte produkter.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 029d2aa4fd20fc036a34ae6136fe12454f3b7703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273345"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="71364-103">Administrere komplekse enheter for produktbaserte kontraktlinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="71364-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="71364-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="71364-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71364-105">Dynamics 365 Project Operations bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter.</span><span class="sxs-lookup"><span data-stu-id="71364-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="71364-106">Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på kontrakt- eller prosjektkontraktlinjen som antall brukermåneder.</span><span class="sxs-lookup"><span data-stu-id="71364-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="71364-107">Prisen på abonnementsprogramvaren lagres i katalogen som prisen per bruker per måned.</span><span class="sxs-lookup"><span data-stu-id="71364-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="71364-108">I løpet av salgsprosessen er prisen på kontraktlinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av salgsrepresentanten.</span><span class="sxs-lookup"><span data-stu-id="71364-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="71364-109">Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="71364-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="71364-110">Antallet som brukes til å beregne beløpet for kontraktlinjen, er et produkt av antall brukere og antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="71364-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="71364-111">Project Operations støtter konseptet *antallsfaktorer* for å støtte denne typen salg.</span><span class="sxs-lookup"><span data-stu-id="71364-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="71364-112">Antallsfaktorer er avhengig av produktattributter.</span><span class="sxs-lookup"><span data-stu-id="71364-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="71364-113">Når du konfigurerer bestemte egenskaper for et produkt, kan du flagge et delsett av disse egenskapene, eller alle egenskapene, som antall faktorer.</span><span class="sxs-lookup"><span data-stu-id="71364-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="71364-114">Project Operations validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer.</span><span class="sxs-lookup"><span data-stu-id="71364-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="71364-115">Når det legges til et produkt med konfigurerte antallsfaktorer på en kontraktlinje, blir **Antall**-feltet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="71364-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="71364-116">Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner Project Operations antallet på kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="71364-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="71364-117">Dynamics 365 Sales kan for eksempel ha følgende egenskaper:</span><span class="sxs-lookup"><span data-stu-id="71364-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="71364-118">**Antall brukere**: Antall brukere.</span><span class="sxs-lookup"><span data-stu-id="71364-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="71364-119">**Antall måneder**: Antall abonnementsmåneder.</span><span class="sxs-lookup"><span data-stu-id="71364-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="71364-120">**Produkt-SKU** Vareopptellingsenheter (Stock Keeping Unit – SKU) for produktet.</span><span class="sxs-lookup"><span data-stu-id="71364-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="71364-121">Egenskapene **Antall brukere** og **Antall måneder** kan flagges som antallsfaktorer ved å redigere egenskapene for produktlinjen.</span><span class="sxs-lookup"><span data-stu-id="71364-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="71364-122">Følg fremgangsmåten nedenfor for å opprette antallsfaktorer fra produktegenskaper.</span><span class="sxs-lookup"><span data-stu-id="71364-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="71364-123">Velg **Salg-Produkter** i **Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="71364-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="71364-124">Åpne produktet du vil definere antallsfaktorer for.</span><span class="sxs-lookup"><span data-stu-id="71364-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="71364-125">Kontroller at produktet allerede har konfigurert egenskaper.</span><span class="sxs-lookup"><span data-stu-id="71364-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="71364-126">På **Prosjektinformasjon**-siden velger du kategorien **Antallsfaktorer**.</span><span class="sxs-lookup"><span data-stu-id="71364-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="71364-127">I delrutenettet velger du **+ Ny feltberegning**.</span><span class="sxs-lookup"><span data-stu-id="71364-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="71364-128">Angi navnet på **Antallsfaktor**, og velg egenskapsverdien som tilordnes feltberegningen.</span><span class="sxs-lookup"><span data-stu-id="71364-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="71364-129">Lagre og lukk skjemaet.</span><span class="sxs-lookup"><span data-stu-id="71364-129">Save and close the form.</span></span>
7. <span data-ttu-id="71364-130">Gjenta trinn 2-6 for alle egenskapene som samlet utgjør antallet for den produktbaserte kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="71364-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="71364-131">Når antallsfaktorer er konfigurert og brukeren oppretter en kontraktlinje for dette produktet, blir antallet for kontraktlinjen låst.</span><span class="sxs-lookup"><span data-stu-id="71364-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="71364-132">Antallet beregnes deretter som et produkt av egenskapsverdiene for denne kontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="71364-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]