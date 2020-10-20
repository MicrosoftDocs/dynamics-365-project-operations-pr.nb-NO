---
title: Produktbaserte salgsmulighetslinjer
description: Dette emnet gir informasjon om produktbaserte salgsmulighetslinjeelementer i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896248"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="fa929-103">Produktbaserte salgsmulighetslinjer</span><span class="sxs-lookup"><span data-stu-id="fa929-103">Product-based opportunity lines</span></span>

<span data-ttu-id="fa929-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="fa929-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fa929-105">Produkterbaserte salgsmulighetslinjer er linjeelementer for salgsmuligheten.</span><span class="sxs-lookup"><span data-stu-id="fa929-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="fa929-106">Disse linjene leveres til kunden som distinkte linjeelementer på den eventuelle fakturaen, uten andre verdiøkende tjenester.</span><span class="sxs-lookup"><span data-stu-id="fa929-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="fa929-107">Tilknyttet forbruk spores ikke for oppgaver i relaterte prosjekter.</span><span class="sxs-lookup"><span data-stu-id="fa929-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="fa929-108">Produktbaserte linjer kan være katalogelementer eller produkter som ikke er i produktkatalogen.</span><span class="sxs-lookup"><span data-stu-id="fa929-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="fa929-109">Det meste av funksjonaliteten for produktbaserte linjer i en salgsmulighet følger funksjonaliteten fra Dynamics 365 Sales-programmet.</span><span class="sxs-lookup"><span data-stu-id="fa929-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="fa929-110">Du får mer informasjon om produktbaserte salgsmulighetslinjer ved se [Legge til produkter i en salgsmulighet](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="fa929-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="fa929-111">Ett konsept om produktbaserte salgsmulighetslinjer som er spesifikt for prosjektrelaterte salgsmuligheter, er **Kundebudsjett**.</span><span class="sxs-lookup"><span data-stu-id="fa929-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="fa929-112">Bruk dette feltet til å spore beløpet som kunden er villig til å betale for linjeelementet.</span><span class="sxs-lookup"><span data-stu-id="fa929-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="fa929-113">Hvis omsetningsmetoden for salgsmulighetssammendraget er satt til **Systemberegnet**, summeres kundebudsjettverdiene på tvers av produkt- og prosjektbaserte linjer for å beregne estimert omsetning.</span><span class="sxs-lookup"><span data-stu-id="fa929-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
