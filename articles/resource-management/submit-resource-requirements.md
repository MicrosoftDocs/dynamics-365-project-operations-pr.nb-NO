---
title: Sende en ressursforespørsel
description: Du kan sende et generert ressurskrav som en ressursforespørsel. Forespørselen sendes deretter til en ressurslederen for fullføring.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081514"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="c725e-104">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="c725e-104">Submit a resource request</span></span>

<span data-ttu-id="c725e-105">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="c725e-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c725e-106">Du kan sende et generert ressurskrav som en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="c725e-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="c725e-107">Forespørselen sendes deretter til en ressurslederen for fullføring.</span><span class="sxs-lookup"><span data-stu-id="c725e-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="c725e-108">I Dynamics 365 Project Operations, på **Prosjekter** -siden, velger du **Team** -fanen for å vise en liste over bestillbare ressurser.</span><span class="sxs-lookup"><span data-stu-id="c725e-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="c725e-109">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="c725e-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="c725e-110">Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="c725e-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="c725e-111">Når forespørselen er utført, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen ved å bestille en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="c725e-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="c725e-112">Ellers, hvis ressurslederen har foreslått en navngitt ressurs, blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="c725e-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
