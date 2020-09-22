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
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754192"
---
# <a name="skills-and-proficiency-models"></a>Ferdighets- og kunnskapsmodeller

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Ferdigheter er ressursegenskaper som deles mellom Dynamics 365 Project Service Automation og eventuelt Dynamics 365 Field Service. 

Hvis du vil vedlikeholde ferdighetsrepositoriet i Project Service Automation, kan du gå til **Ressurser** \> **Ressursferdigheter**. 

> ![Ressursferdigheter](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>Bruke kompetansemodeller til å vurdere ressurser

Ferdigheter for ressurser er rangert av kompetansemodeller. De enkelte klassifiseringene finnes i en kompetansemodell. 

1. Hvis du vil opprette en kompetansemodell, går du til **Ressurser** \> **Kompetansemodeller** og velger **Ny**.
2. I den nye vurderingsmodellen angir du minimumsverdien for vurdering, maksimumsverdien for vurdering og enheten som skal vurderes.
3. I delrutenettet **Rangeringsverdier** kan du definere de ulike vurderingsverdiene, fra minimum til maksimum.

> ![Minimums- og maksimumsvurderinger er definert](media/Resource-Management-image85.png)

Disse vurderingsverdiene vises på filtrene **Ressurskrav**, **Planleggingstavle** og **Planleggingsassistent**.
