---
title: Sende en ressursforespørsel
description: Du kan sende et generert ressurskrav som en ressursforespørsel. Forespørselen sendes deretter til en ressurslederen for fullføring.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279150"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="680dc-104">Sende en ressursforespørsel</span><span class="sxs-lookup"><span data-stu-id="680dc-104">Submit a resource request</span></span>

<span data-ttu-id="680dc-105">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="680dc-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="680dc-106">Du kan sende et generert ressurskrav som en ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="680dc-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="680dc-107">Forespørselen sendes deretter til en ressurslederen for fullføring.</span><span class="sxs-lookup"><span data-stu-id="680dc-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="680dc-108">Klikk fanen **Team** på siden **Prosjekter** for å vise en liste over bestillbare ressurser i Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="680dc-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="680dc-109">Velg den generelle ressursen som har et ressurskrav, fra listen, og klikk deretter **Send forespørsel**.</span><span class="sxs-lookup"><span data-stu-id="680dc-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="680dc-110">Forespørselsstatusen for det generelle teammedlemmet blir endret **Sendt**.</span><span class="sxs-lookup"><span data-stu-id="680dc-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="680dc-111">Når forespørselen er utført, erstattes den generelle ressursen av en navngitt ressurs hvis ressurslederen utfører forespørselen ved å bestille en navngitt ressurs.</span><span class="sxs-lookup"><span data-stu-id="680dc-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="680dc-112">Ellers, hvis ressurslederen har foreslått en navngitt ressurs, blir den generelle ressursen værende i teamet, og forespørselsstatusen endres til **Må gjennomgås**.</span><span class="sxs-lookup"><span data-stu-id="680dc-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]