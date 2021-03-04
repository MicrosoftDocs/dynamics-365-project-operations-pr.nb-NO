---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764569"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="542b3-103">Konfigurere kostnads- og salgspriser for katalogprodukter – Lite</span><span class="sxs-lookup"><span data-stu-id="542b3-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="542b3-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="542b3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="542b3-105">Definisjon av priser for produktkatalogelementer i Dynamics 365 Project Operations er det samme som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="542b3-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="542b3-106">I Project Operations kan ikke produkter beregnes eller brukes på prosjekter, så produktkatalogpriser behøver ikke angis i prosjektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="542b3-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="542b3-107">Bruk feltet **Produktpris** i et tilbud, en kontrakt eller en konto til å angi produktkatalogpriser.</span><span class="sxs-lookup"><span data-stu-id="542b3-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="542b3-108">Ikke definer produktkatalogpriser i prosjektprislistene.</span><span class="sxs-lookup"><span data-stu-id="542b3-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="542b3-109">Prosjektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="542b3-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="542b3-110">Appspesifikk forretningslogikk kopierer prislistene fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="542b3-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="542b3-111">Resultatet er en kontraktsspesifikk prosjektprisliste.</span><span class="sxs-lookup"><span data-stu-id="542b3-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="542b3-112">Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor.</span><span class="sxs-lookup"><span data-stu-id="542b3-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="542b3-113">Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter.</span><span class="sxs-lookup"><span data-stu-id="542b3-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="542b3-114">Ettersom ingen kopiering er involvert, påvirkes ikke ytelsen til tilbudsprosessen.</span><span class="sxs-lookup"><span data-stu-id="542b3-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
