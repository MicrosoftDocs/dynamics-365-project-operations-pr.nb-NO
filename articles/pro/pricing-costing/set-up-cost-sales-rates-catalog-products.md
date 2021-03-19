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
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274470"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="a3e92-103">Konfigurere kostnads- og salgspriser for katalogprodukter – Lite</span><span class="sxs-lookup"><span data-stu-id="a3e92-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="a3e92-104">_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="a3e92-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a3e92-105">Definisjon av priser for produktkatalogelementer i Dynamics 365 Project Operations er det samme som i Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="a3e92-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="a3e92-106">I Project Operations kan ikke produkter beregnes eller brukes på prosjekter, så produktkatalogpriser behøver ikke angis i prosjektprislister for tilbud og kontrakter.</span><span class="sxs-lookup"><span data-stu-id="a3e92-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="a3e92-107">Bruk feltet **Produktpris** i et tilbud, en kontrakt eller en konto til å angi produktkatalogpriser.</span><span class="sxs-lookup"><span data-stu-id="a3e92-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="a3e92-108">Ikke definer produktkatalogpriser i prosjektprislistene.</span><span class="sxs-lookup"><span data-stu-id="a3e92-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="a3e92-109">Prosjektprislister er eksklusive for Project Operations.</span><span class="sxs-lookup"><span data-stu-id="a3e92-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="a3e92-110">Appspesifikk forretningslogikk kopierer prislistene fra et tilbud til en kontrakt.</span><span class="sxs-lookup"><span data-stu-id="a3e92-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="a3e92-111">Resultatet er en kontraktsspesifikk prosjektprisliste.</span><span class="sxs-lookup"><span data-stu-id="a3e92-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="a3e92-112">Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor.</span><span class="sxs-lookup"><span data-stu-id="a3e92-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="a3e92-113">Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter.</span><span class="sxs-lookup"><span data-stu-id="a3e92-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="a3e92-114">Ettersom ingen kopiering er involvert, påvirkes ikke ytelsen til tilbudsprosessen.</span><span class="sxs-lookup"><span data-stu-id="a3e92-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]