---
title: Send en ressursforespørsel
description: Dette emnet gir informasjon om å sende en forespørsel for en prosjektressurs.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754161"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="78c6d-103">Send en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="78c6d-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78c6d-104">Du kan sende et generert ressurskrav som en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="78c6d-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="78c6d-105">Forespørselen sendes deretter til en ressurslederen for fullføring.</span><span class="sxs-lookup"><span data-stu-id="78c6d-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="78c6d-106">Klikk kategorien **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="78c6d-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="78c6d-107">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="78c6d-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Sende en ressursforespørsel](media/RM-how-to-18.png)

<span data-ttu-id="78c6d-109">Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="78c6d-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="78c6d-110">Når forespørselen er utført av ressurslederen, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen med bestilling av en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="78c6d-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="78c6d-111">Ellers blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås** hvis ressurslederen har foreslått en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="78c6d-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
