---
title: Produktbaserte salgsmulighetslinjer – Lite
description: Dette emnet gir informasjon om produktbaserte salgsmulighetslinjeelementer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176350"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="2de47-103">Produktbaserte salgsmulighetslinjer – Lite</span><span class="sxs-lookup"><span data-stu-id="2de47-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="2de47-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="2de47-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2de47-105">Produkterbaserte salgsmulighetslinjer er linjeelementer for salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="2de47-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="2de47-106">Disse linjene leveres til kunden som distinkte linjeelementer på den eventuelle fakturaen, uten andre verdiøkende tjenester.</span><span class="sxs-lookup"><span data-stu-id="2de47-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="2de47-107">Tilknyttet forbruk spores ikke for oppgaver i relaterte prosjekter.</span><span class="sxs-lookup"><span data-stu-id="2de47-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="2de47-108">Produktbaserte linjer kan være katalogelementer eller produkter som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="2de47-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="2de47-109">Det meste av funksjonaliteten for produktbaserte linjer i en salgsmulighet følger funksjonaliteten fra Dynamics 365 Sales-programmet.</span><span class="sxs-lookup"><span data-stu-id="2de47-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="2de47-110">Du får mer informasjon om produktbaserte salgsmulighetslinjer ved se [Legge til produkter i en salgsmulighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="2de47-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="2de47-111">Ett konsept om produktbaserte salgsmulighetslinjer som er spesifikt for prosjektrelaterte salgsmuligheter, er **Kundebudsjett**.</span><span class="sxs-lookup"><span data-stu-id="2de47-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="2de47-112">Bruk dette feltet til å spore beløpet som kunden er villig til å betale for linjeelementet.</span><span class="sxs-lookup"><span data-stu-id="2de47-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="2de47-113">Hvis omsetningsmetoden for salgsmulighetssammendraget er satt til **Systemberegnet**, summeres kundebudsjettverdiene på tvers av produkt- og prosjektbaserte linjer for å beregne estimert omsetning.</span><span class="sxs-lookup"><span data-stu-id="2de47-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
