---
title: Sende en ressursforespørsel
description: Du kan sende et generert ressurskrav som en ressursforespørsel. Forespørselen sendes deretter til en ressurslederen for fullføring.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014038"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="b922e-104">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="b922e-104">Submit a resource request</span></span>

<span data-ttu-id="b922e-105">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="b922e-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b922e-106">Du kan sende et generert ressurskrav som en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="b922e-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="b922e-107">Forespørselen sendes deretter til en ressurslederen for fullføring.</span><span class="sxs-lookup"><span data-stu-id="b922e-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="b922e-108">Klikk fanen **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b922e-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="b922e-109">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="b922e-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="b922e-110">Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="b922e-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="b922e-111">Når forespørselen er utført, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen ved å bestille en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="b922e-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="b922e-112">Ellers, hvis ressurslederen har foreslått en navngitt ressurs, blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="b922e-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]