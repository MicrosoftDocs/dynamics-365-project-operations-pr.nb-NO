---
title: Konfigurere en salgsprisliste
description: Dette emnet gir information om salgsprislister for prosjektpriser.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 05b1c13540e902975eee7379276cf394d9fc5743
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275460"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="0dab7-103">Konfigurere en salgsprisliste</span><span class="sxs-lookup"><span data-stu-id="0dab7-103">Set up a sales price list</span></span>

<span data-ttu-id="0dab7-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0dab7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0dab7-105">For prosjekttilbud og kontrakter har en prosjektprisliste et annet prisoverstyringsmønster enn en produktprisliste.</span><span class="sxs-lookup"><span data-stu-id="0dab7-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="0dab7-106">På en produktkatalogbasert tilbudslinje kan du overstyre prisen for roller og kategorier direkte på tilbudslinjen, fordi hver tilbudslinje peker på nøyaktig ett katalogelement.</span><span class="sxs-lookup"><span data-stu-id="0dab7-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="0dab7-107">På en prosjektbasert tilbudslinjen kan du imidlertid ikke overstyre prisen til roller og kategorier direkte på tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="0dab7-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="0dab7-108">Du kan bruke prosjektprislisten til å arbeide med de to spesifikke overstyringsmønstrene.</span><span class="sxs-lookup"><span data-stu-id="0dab7-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="0dab7-109">Vi anbefaler at du har en egen prisliste for prosjektressursene og katalogelementene på grunn av virkemåteforskjellene mellom de to når du overstyrer prisen.</span><span class="sxs-lookup"><span data-stu-id="0dab7-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="0dab7-110">Hver av de følgende enhetene kan ha én eller flere tilknyttede salgsprislister for prosjektprising:</span><span class="sxs-lookup"><span data-stu-id="0dab7-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="0dab7-111">Kunde (forretningsforbindelse)</span><span class="sxs-lookup"><span data-stu-id="0dab7-111">Customer (account)</span></span> 
- <span data-ttu-id="0dab7-112">Salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="0dab7-112">Opportunity</span></span> 
- <span data-ttu-id="0dab7-113">Tilbud</span><span class="sxs-lookup"><span data-stu-id="0dab7-113">Quote</span></span> 
- <span data-ttu-id="0dab7-114">Prosjektkontrakt</span><span class="sxs-lookup"><span data-stu-id="0dab7-114">Project Contract</span></span>

<span data-ttu-id="0dab7-115">Tilknytningen til disse enhetene og en prisliste angis av prosjektprislistene.</span><span class="sxs-lookup"><span data-stu-id="0dab7-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="0dab7-116">Du kan knytte én eller flere prislister til salgsenhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="0dab7-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="0dab7-117">Det registreres ikke automatisk en standard prosjektprisliste i en kundeoppføring.</span><span class="sxs-lookup"><span data-stu-id="0dab7-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="0dab7-118">Du kan imidlertid legge ved en prosjektprisliste manuelt i kundeoppføringen.</span><span class="sxs-lookup"><span data-stu-id="0dab7-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="0dab7-119">Likevel bør du likevel legge ved en prosjekt prisliste manuelt bare når du har en egen definert prisingsavtale med kunden.</span><span class="sxs-lookup"><span data-stu-id="0dab7-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="0dab7-120">Når en prosjektprisliste er knyttet til en salgsenhet, valideres følgende informasjon:</span><span class="sxs-lookup"><span data-stu-id="0dab7-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="0dab7-121">Prislisten som en kontekst for **Salg**.</span><span class="sxs-lookup"><span data-stu-id="0dab7-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="0dab7-122">Valutaen i prislisten samsvarer med kundevalutaen.</span><span class="sxs-lookup"><span data-stu-id="0dab7-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="0dab7-123">I en prosjektkontrakt brukes følgende prioritetsrekkefølge til automatisk å angi relaterte prosjektprislister:</span><span class="sxs-lookup"><span data-stu-id="0dab7-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="0dab7-124">Tilbud</span><span class="sxs-lookup"><span data-stu-id="0dab7-124">Quote</span></span>
2. <span data-ttu-id="0dab7-125">Salgsmulighet</span><span class="sxs-lookup"><span data-stu-id="0dab7-125">Opportunity</span></span>
3. <span data-ttu-id="0dab7-126">Kunde</span><span class="sxs-lookup"><span data-stu-id="0dab7-126">Customer</span></span> 
4. <span data-ttu-id="0dab7-127">Globale innstillinger</span><span class="sxs-lookup"><span data-stu-id="0dab7-127">Global settings</span></span> 

<span data-ttu-id="0dab7-128">Når en prosjektprisliste er angitt som standard, validerer systemet at valutaen samsvarer med kundens valuta, og at standardprislistene som er lagt inn, har en kontekst for **Salg**.</span><span class="sxs-lookup"><span data-stu-id="0dab7-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="0dab7-129">Du kan knytte flere prosjektprislister til enhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="0dab7-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="0dab7-130">Denne funksjonen støtter datospesifikke standardpriser for en langvarig prosjektkontrakt, der du kan trenge mer enn én prisliste for å ta hensyn til prisoppdateringer som inntreffer på grunn av inflasjonen.</span><span class="sxs-lookup"><span data-stu-id="0dab7-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="0dab7-131">Hvis prislistene som du knytter til enheten Kunde, Salgsmulighet, Tilbud eller Prosjektkontrakt, for eksempel har overlappende datogyldighet, kan standard prisene være feil.</span><span class="sxs-lookup"><span data-stu-id="0dab7-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="0dab7-132">Derfor bør du sørge for at prosjektprislister som har overlappende datogyldighet, ikke er tilknyttet disse enhetene.</span><span class="sxs-lookup"><span data-stu-id="0dab7-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]