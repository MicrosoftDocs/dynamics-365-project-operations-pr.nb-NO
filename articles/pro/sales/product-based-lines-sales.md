---
title: Produktbaserte salgsmulighetslinjer – Lite
description: Dette emnet gir informasjon om produktbaserte salgsmulighetslinjeelementer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764966"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="9cba0-103">Produktbaserte salgsmulighetslinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="9cba0-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="9cba0-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9cba0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9cba0-105">Produkterbaserte salgsmulighetslinjer er linjeelementer for salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="9cba0-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="9cba0-106">Disse distinkte linjeelementene finnes på den endelige fakturaen som leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="9cba0-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="9cba0-107">Fakturaen inkluderer ingen andre tilleggstjenester.</span><span class="sxs-lookup"><span data-stu-id="9cba0-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="9cba0-108">Tilknyttet forbruk spores ikke for oppgaver i relaterte prosjekter.</span><span class="sxs-lookup"><span data-stu-id="9cba0-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="9cba0-109">Produktbaserte linjer kan være katalogelementer eller produkter som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="9cba0-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="9cba0-110">Det meste av funksjonaliteten for produktbaserte linjer i en salgsmulighet følger funksjonaliteten fra Dynamics 365 Sales-programmet.</span><span class="sxs-lookup"><span data-stu-id="9cba0-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="9cba0-111">Du får mer informasjon om produktbaserte salgsmulighetslinjer ved se [Legge til produkter i en salgsmulighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="9cba0-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="9cba0-112">**Kundebudsjett** er et konsept som gjelder prosjektbaserte salgsmulighetslinjer.</span><span class="sxs-lookup"><span data-stu-id="9cba0-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="9cba0-113">Feltet **Kundebudsjett** sporer beløpet kunden er villig til å betale for varen.</span><span class="sxs-lookup"><span data-stu-id="9cba0-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="9cba0-114">Når omsetningsmetoden for salgsmulighetssammendraget er **Systemberegnet**, oppsummeres kundebudsjettverdiene på tvers av salgsmulighetslinjene for å beregne beregnet omsetning.</span><span class="sxs-lookup"><span data-stu-id="9cba0-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 

