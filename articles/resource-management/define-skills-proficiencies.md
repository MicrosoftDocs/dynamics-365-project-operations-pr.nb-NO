---
title: Definere ferdigheter og kompetanser
description: Dette emnet gir informasjon om hvordan du konfigurerer kunnskapsmodeller for å vurdere ressurser.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015343"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="9593a-103">Definere ferdigheter og kompetanser</span><span class="sxs-lookup"><span data-stu-id="9593a-103">Define skills and proficiencies</span></span>

<span data-ttu-id="9593a-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="9593a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9593a-105">Ferdigheter er ressursegenskaper som deles mellom Dynamics 365 Project Operations og eventuelt Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="9593a-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="9593a-106">Hvis du vil vedlikeholde ferdighetsrepositoriet i Project Operations, kan du gå til **Ressurser** \> **Ressursferdigheter**.</span><span class="sxs-lookup"><span data-stu-id="9593a-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="9593a-107">Bruke kompetansemodeller til å vurdere ressurser</span><span class="sxs-lookup"><span data-stu-id="9593a-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="9593a-108">Ferdigheter for ressurser er rangert av kompetansemodeller.</span><span class="sxs-lookup"><span data-stu-id="9593a-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="9593a-109">De enkelte klassifiseringene finnes i en kompetansemodell.</span><span class="sxs-lookup"><span data-stu-id="9593a-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="9593a-110">Hvis du vil opprette en kompetansemodell, går du til **Ressurser** \> **Kompetansemodeller** og velger **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9593a-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="9593a-111">I den nye vurderingsmodellen angir du minimumsverdien for vurdering, maksimumsverdien for vurdering og enheten som skal vurderes.</span><span class="sxs-lookup"><span data-stu-id="9593a-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="9593a-112">I delrutenettet **Rangeringsverdier** kan du definere de ulike vurderingsverdiene, fra minimum til maksimum.</span><span class="sxs-lookup"><span data-stu-id="9593a-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="9593a-113">Disse vurderingsverdiene vises på filtrene **Ressurskrav**, **Planleggingstavle** og **Planleggingsassistent**.</span><span class="sxs-lookup"><span data-stu-id="9593a-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]