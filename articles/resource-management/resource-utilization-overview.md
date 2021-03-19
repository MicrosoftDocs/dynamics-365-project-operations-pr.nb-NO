---
title: Oversikt over ressursutnyttelse
description: Dette emnet gir informasjon om ressursutnyttelse i Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279330"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="e2b25-103">Oversikt over ressursutnyttelse</span><span class="sxs-lookup"><span data-stu-id="e2b25-103">Resource utilization overview</span></span>

<span data-ttu-id="e2b25-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="e2b25-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e2b25-105">Ressurser kan ha fakturerbar utnyttelse som mål.</span><span class="sxs-lookup"><span data-stu-id="e2b25-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="e2b25-106">Denne målutnyttelsen er definert som et attributt i standardrollen til en ressurs eller angitt i oppføringen for en enkelt bestillbar ressurs.</span><span class="sxs-lookup"><span data-stu-id="e2b25-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="e2b25-107">Utnyttelsesberegninger er basert på de faktiske timene ressursene har rapportert ved hjelp av godkjente tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="e2b25-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="e2b25-108">Følgende formler brukes til å beregne utnyttelse:</span><span class="sxs-lookup"><span data-stu-id="e2b25-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="e2b25-109">Fakturerbar utnyttelse = belastbare faktiske timer ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="e2b25-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="e2b25-110">Ikke-fakturerbar utnyttelse = faktisk tid med faktureringstype-ID = ikke-belastbar, komplementær eller ikke tilgjengelig ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="e2b25-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="e2b25-111">Intern = faktisk tid uten salgskontrakt ÷ ressurskapasitet</span><span class="sxs-lookup"><span data-stu-id="e2b25-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="e2b25-112">Ressurskapasitet = arbeidstimer for ressursen – fravær – ikke-arbeidsdager</span><span class="sxs-lookup"><span data-stu-id="e2b25-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="e2b25-113">Du kan finne visningen **Ressursutnyttelse** i **Ressurser**-ruten.</span><span class="sxs-lookup"><span data-stu-id="e2b25-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="e2b25-114">Hver celle i rutenettet representerer den fakturerbare utnyttelsesprosenten for ressursen i en periode, for eksempel en dag, uke eller måned.</span><span class="sxs-lookup"><span data-stu-id="e2b25-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="e2b25-115">Følgende formler brukes til å fargelegge cellene:</span><span class="sxs-lookup"><span data-stu-id="e2b25-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="e2b25-116">**Grønn**: Fakturerbar utnyttelse >= Ressursmålutnyttelse</span><span class="sxs-lookup"><span data-stu-id="e2b25-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="e2b25-117">**Gul**: Målutnyttelse – 20 <= Fakturerbar utnyttelse < Målutnyttelse</span><span class="sxs-lookup"><span data-stu-id="e2b25-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="e2b25-118">**Rød**: Fakturerbar utnyttelse < Målutnyttelse – 20</span><span class="sxs-lookup"><span data-stu-id="e2b25-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="e2b25-119">Siden visningen **Ressursutnyttelse** er basert på planleggingstavlen, kan du bruke filtreringsfunksjonene på planleggingstavlen til å filtrere resultatene.</span><span class="sxs-lookup"><span data-stu-id="e2b25-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="e2b25-120">Rutenettet krever at du angir en målutnyttelse for rollen eller den individuelle ressursen.</span><span class="sxs-lookup"><span data-stu-id="e2b25-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="e2b25-121">Du kan sette opp dette ved å gå til **Ressurser** > **Ressursroller**.</span><span class="sxs-lookup"><span data-stu-id="e2b25-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="e2b25-122">I tillegg må en standardrolle tilordnes til hver bestillbare ressurs.</span><span class="sxs-lookup"><span data-stu-id="e2b25-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="e2b25-123">Gå til **Ressurser** > **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="e2b25-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="e2b25-124">I kategorien **Project Service** kontrollerer du at det er definert en ressursrolle, og at **Er standard**-feltet er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e2b25-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="e2b25-125">Du kan legge til flere roller der **Er standard** = **Nei**.</span><span class="sxs-lookup"><span data-stu-id="e2b25-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="e2b25-126">Rollen der **Er standard** = **Ja** brukes til å evaluere ressursens utnyttelse mot målet for den aktuelle rollen.</span><span class="sxs-lookup"><span data-stu-id="e2b25-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="e2b25-127">I kategorien **Project Service** kan du også angi en individuell målutnyttelse for ressursen.</span><span class="sxs-lookup"><span data-stu-id="e2b25-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="e2b25-128">Beregningen av utnyttelsen bruker deretter denne målutnyttelsen til å evaluere ressursens mål i stedet for målet for standardrollen for ressursen.</span><span class="sxs-lookup"><span data-stu-id="e2b25-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="e2b25-129">Utnyttelse vises bare for en ressurs hvis ressursen har godkjent, belastbar tid i perioden som vises i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="e2b25-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]