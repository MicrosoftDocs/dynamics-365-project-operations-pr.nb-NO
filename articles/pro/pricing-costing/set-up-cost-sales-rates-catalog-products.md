---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176713"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="98b99-103">Konfigurere kostnads- og salgspriser for katalogprodukter – Lite</span><span class="sxs-lookup"><span data-stu-id="98b99-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="98b99-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="98b99-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="98b99-105">Konfigurering av priser for produktkatalogvarer i Dynamics 365 Project Operations er likt som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="98b99-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="98b99-106">Siden produkter ikke kan estimeres eller brukes i prosjekter i Project Operations, er det ikke nødvendig å angi produktkatalogpriser i prosjektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="98b99-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="98b99-107">Produktkatalogpriser bør konfigureres i **Produktpris**-feltet for et tilbud, en kontrakt eller en forretningsforbindelse.</span><span class="sxs-lookup"><span data-stu-id="98b99-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="98b99-108">Ikke konfigurer produktkatalogpriser i prosjektprislistene for disse enhetene.</span><span class="sxs-lookup"><span data-stu-id="98b99-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="98b99-109">Prosjektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="98b99-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="98b99-110">Det finnes programspesifikk forretningslogikk som kopierer prislistene fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="98b99-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="98b99-111">Resultatet er en kontraktsspesifikk prosjektprisliste.</span><span class="sxs-lookup"><span data-stu-id="98b99-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="98b99-112">Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor.</span><span class="sxs-lookup"><span data-stu-id="98b99-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="98b99-113">Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter.</span><span class="sxs-lookup"><span data-stu-id="98b99-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="98b99-114">Dette betyr at produktprislister ikke påvirker ytelsen til prosessen ved å vinne tilbudet.</span><span class="sxs-lookup"><span data-stu-id="98b99-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
