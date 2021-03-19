---
title: Administrere prosjekttilbud
description: Denne emnet gir informasjon om prosjekttilbud.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87921221ea210e67a3ddc53bd124f292de80de99
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272940"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="6a9be-103">Administrere prosjekttilbud</span><span class="sxs-lookup"><span data-stu-id="6a9be-103">Manage project quotes</span></span>

<span data-ttu-id="6a9be-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="6a9be-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a9be-105">I Dynamics 365 Project Operations er prosjekttilbud utformet for bidra til å bygge forslag til prosjektarbeid.</span><span class="sxs-lookup"><span data-stu-id="6a9be-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="6a9be-106">Strukturen i et prosjekt tilbud i Project Operations er strukturert for prosjektforslag med følgende komponenter:</span><span class="sxs-lookup"><span data-stu-id="6a9be-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="6a9be-107">Tilbudslinjer som identifiserer de separate komponentene for arbeid som skal presenteres som komponenter på høyt nivå.</span><span class="sxs-lookup"><span data-stu-id="6a9be-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="6a9be-108">Tilbudslinjedetaljer som identifiserer og beregner arbeidet for hver komponent eller tilbudslinje på høyt nivå.</span><span class="sxs-lookup"><span data-stu-id="6a9be-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="6a9be-109">Tidsplan- eller datoestimater og økonomiaspekter ved arbeidet er knyttet til denne tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="6a9be-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="6a9be-110">Kontraktmodeller og belastbare komponenter konfigureres for hver tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="6a9be-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="6a9be-111">Dette oppsettet hjelper deg med å beregne spredningen av inntekter, forbruk og lønnsomhet for hver tilbudslinje og det totale tilbudet.</span><span class="sxs-lookup"><span data-stu-id="6a9be-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="6a9be-112">Vise alle prosjektbaserte tilbud</span><span class="sxs-lookup"><span data-stu-id="6a9be-112">View all project-based quotes</span></span>

<span data-ttu-id="6a9be-113">En liste over alle prosjekttilbud kan ses på listesiden **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="6a9be-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="6a9be-114">Gå til **Salg** > **Tilbud**.</span><span class="sxs-lookup"><span data-stu-id="6a9be-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="6a9be-115">Det vises en liste over alle prosjekttilbudene i systemet.</span><span class="sxs-lookup"><span data-stu-id="6a9be-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="6a9be-116">Bruk **Vis bryter** til å velge andre filtrerte visninger av tilbudene.</span><span class="sxs-lookup"><span data-stu-id="6a9be-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="6a9be-117">Ved hjelp av egendefinerte filtervilkår kan du konfigurere dine egne visninger og navigasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="6a9be-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="6a9be-118">Tilbud kan opprettes eller slettes fra denne listesiden eller detaljsider.</span><span class="sxs-lookup"><span data-stu-id="6a9be-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]