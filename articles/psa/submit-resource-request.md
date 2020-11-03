---
title: Sende en ressursforespørsel
description: Dette emnet gir informasjon om å sende en forespørsel for en prosjektressurs.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081713"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="3703e-103">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="3703e-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3703e-104">Du kan sende et generert ressurskrav som en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="3703e-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="3703e-105">Forespørselen sendes deretter til en ressurslederen for fullføring.</span><span class="sxs-lookup"><span data-stu-id="3703e-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="3703e-106">Klikk kategorien **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="3703e-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="3703e-107">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="3703e-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Sende en ressursforespørsel](media/RM-how-to-18.png)

<span data-ttu-id="3703e-109">Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="3703e-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="3703e-110">Når forespørselen er utført av ressurslederen, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen med bestilling av en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="3703e-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="3703e-111">Ellers blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås** hvis ressurslederen har foreslått en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="3703e-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
