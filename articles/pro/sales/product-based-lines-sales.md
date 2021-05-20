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
ms.openlocfilehash: f7dfabd068e180c7122ede0f79aaebfe220250a1
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949556"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="efb9b-103">Produktbaserte salgsmulighetslinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="efb9b-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="efb9b-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="efb9b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="efb9b-105">Produkterbaserte salgsmulighetslinjer er linjeelementer for salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="efb9b-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="efb9b-106">Disse distinkte linjeelementene finnes på den endelige fakturaen som leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="efb9b-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="efb9b-107">Fakturaen inkluderer ingen andre tilleggstjenester.</span><span class="sxs-lookup"><span data-stu-id="efb9b-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="efb9b-108">Tilknyttet forbruk spores ikke for oppgaver i relaterte prosjekter.</span><span class="sxs-lookup"><span data-stu-id="efb9b-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="efb9b-109">Produktbaserte linjer kan være katalogelementer eller produkter som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="efb9b-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="efb9b-110">Det meste av funksjonaliteten for produktbaserte linjer i en salgsmulighet følger funksjonaliteten fra Dynamics 365 Sales-programmet.</span><span class="sxs-lookup"><span data-stu-id="efb9b-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="efb9b-111">Du får mer informasjon om produktbaserte salgsmulighetslinjer ved se [Legge til produkter i en salgsmulighet](/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="efb9b-111">For more information about product-based opportunity lines, see [Add products to an opportunity](/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="efb9b-112">**Kundebudsjett** er et konsept som gjelder prosjektbaserte salgsmulighetslinjer.</span><span class="sxs-lookup"><span data-stu-id="efb9b-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="efb9b-113">Feltet **Kundebudsjett** sporer beløpet kunden er villig til å betale for varen.</span><span class="sxs-lookup"><span data-stu-id="efb9b-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="efb9b-114">Når omsetningsmetoden for salgsmulighetssammendraget er **Systemberegnet**, oppsummeres kundebudsjettverdiene på tvers av salgsmulighetslinjene for å beregne beregnet omsetning.</span><span class="sxs-lookup"><span data-stu-id="efb9b-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]