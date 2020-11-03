---
title: Konfigurere kostnads- og salgspriser for katalogprodukter
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081687"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="05477-103">Konfigurere kostnads- og salgspriser for katalogprodukter</span><span class="sxs-lookup"><span data-stu-id="05477-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="05477-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="05477-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="05477-105">Konfigurering av priser for produktkatalogvarer i Dynamics 365 Project Operations er likt som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="05477-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="05477-106">Siden produkter ikke kan estimeres eller brukes i prosjekter i Project Operations, er det ikke nødvendig å angi produktkatalogpriser i prosjektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="05477-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="05477-107">Produktkatalogpriser bør konfigureres i **Produktpris** -feltet for et tilbud, en kontrakt eller en forretningsforbindelse.</span><span class="sxs-lookup"><span data-stu-id="05477-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="05477-108">Ikke konfigurer produktkatalogpriser i prosjektprislistene for disse enhetene.</span><span class="sxs-lookup"><span data-stu-id="05477-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="05477-109">Prosjektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="05477-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="05477-110">Det finnes programspesifikk forretningslogikk som kopierer prislistene fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="05477-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="05477-111">Resultatet er en kontraktsspesifikk prosjektprisliste.</span><span class="sxs-lookup"><span data-stu-id="05477-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="05477-112">Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor.</span><span class="sxs-lookup"><span data-stu-id="05477-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="05477-113">Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter.</span><span class="sxs-lookup"><span data-stu-id="05477-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="05477-114">Dette betyr at produktprislister ikke påvirker ytelsen til prosessen ved å vinne tilbudet.</span><span class="sxs-lookup"><span data-stu-id="05477-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
