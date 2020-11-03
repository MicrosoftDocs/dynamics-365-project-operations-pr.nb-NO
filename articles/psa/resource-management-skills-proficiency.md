---
title: Ferdighets- og kunnskapsmodeller
description: Dette emnet gir informasjon om hvordan du bruker ferdighets- og kunnskapsmodeller.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081840"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="997a1-103">Ferdighets- og kunnskapsmodeller</span><span class="sxs-lookup"><span data-stu-id="997a1-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="997a1-104">Ferdigheter er ressursegenskaper som deles mellom Dynamics 365 Project Service Automation og eventuelt Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="997a1-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="997a1-105">Hvis du vil vedlikeholde ferdighetsrepositoriet i Project Service Automation, kan du gå til **Ressurser** \> **Ressursferdigheter**.</span><span class="sxs-lookup"><span data-stu-id="997a1-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Ressursferdigheter](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="997a1-107">Bruke kompetansemodeller til å vurdere ressurser</span><span class="sxs-lookup"><span data-stu-id="997a1-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="997a1-108">Ferdigheter for ressurser er rangert av kompetansemodeller.</span><span class="sxs-lookup"><span data-stu-id="997a1-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="997a1-109">De enkelte klassifiseringene finnes i en kompetansemodell.</span><span class="sxs-lookup"><span data-stu-id="997a1-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="997a1-110">Hvis du vil opprette en kompetansemodell, går du til **Ressurser** \> **Kompetansemodeller** og velger **Ny**.</span><span class="sxs-lookup"><span data-stu-id="997a1-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="997a1-111">I den nye vurderingsmodellen angir du minimumsverdien for vurdering, maksimumsverdien for vurdering og enheten som skal vurderes.</span><span class="sxs-lookup"><span data-stu-id="997a1-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="997a1-112">I delrutenettet **Rangeringsverdier** kan du definere de ulike vurderingsverdiene, fra minimum til maksimum.</span><span class="sxs-lookup"><span data-stu-id="997a1-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimums- og maksimumsvurderinger er definert](media/Resource-Management-image85.png)

<span data-ttu-id="997a1-114">Disse vurderingsverdiene vises på filtrene **Ressurskrav** , **Planleggingstavle** og **Planleggingsassistent**.</span><span class="sxs-lookup"><span data-stu-id="997a1-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>
