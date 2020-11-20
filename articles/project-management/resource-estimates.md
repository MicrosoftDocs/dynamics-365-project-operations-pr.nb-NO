---
title: Ressursestimater
description: Dette emnet gir informasjon om hvordan ressursestimater beregnes i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127384"
---
# <a name="resource-estimates"></a><span data-ttu-id="ac281-103">Ressursestimater</span><span class="sxs-lookup"><span data-stu-id="ac281-103">Resource estimates</span></span>

<span data-ttu-id="ac281-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="ac281-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ac281-105">Ressursestimater kommer fra tidsfaset innsats som er definert i arbeidsnedbrytningsstrukturen, sammen med aktuelle prisdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ac281-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="ac281-106">Beregningen er vanligvis **sats/time for hver rolle x timer.**</span><span class="sxs-lookup"><span data-stu-id="ac281-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="ac281-107">Den tidsfasede innsatsen for hver ressurs lagres i ressurstildelingsoppføringen.</span><span class="sxs-lookup"><span data-stu-id="ac281-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="ac281-108">Prissettingen er lagret i en forhåndsdefinert prisliste.</span><span class="sxs-lookup"><span data-stu-id="ac281-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="ac281-109">Enhetsomregning brukes basert på den aktuelle prislisten.</span><span class="sxs-lookup"><span data-stu-id="ac281-109">Unit conversion is applied based on the applicable price list.</span></span>

![Ressursestimater](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="ac281-111">Standard kostpris og kostnadsvaluta</span><span class="sxs-lookup"><span data-stu-id="ac281-111">Default cost price and cost currency</span></span>

<span data-ttu-id="ac281-112">Kostpriser hentes som standard fra organisasjonsenheten.</span><span class="sxs-lookup"><span data-stu-id="ac281-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="ac281-113">Standard fakturasats og salgsvaluta</span><span class="sxs-lookup"><span data-stu-id="ac281-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="ac281-114">Salgspriser brukes én gang per avtale.</span><span class="sxs-lookup"><span data-stu-id="ac281-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="ac281-115">Hierarkiet for salgsprisliste er som standard følgende:</span><span class="sxs-lookup"><span data-stu-id="ac281-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="ac281-116">Organisasjonen</span><span class="sxs-lookup"><span data-stu-id="ac281-116">Organization</span></span>
2. <span data-ttu-id="ac281-117">Kunde</span><span class="sxs-lookup"><span data-stu-id="ac281-117">Customer</span></span>
3. <span data-ttu-id="ac281-118">Tilbud/kontrakt</span><span class="sxs-lookup"><span data-stu-id="ac281-118">Quote/contract</span></span>
