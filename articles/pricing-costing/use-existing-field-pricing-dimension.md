---
title: Project Operations-felt som prisdimensjoner
description: Dette emnet gir informasjon ved å bruke felter som prisdimensjoner i Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004498"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="0496f-103">Project Operations-felter som prisdimensjoner</span><span class="sxs-lookup"><span data-stu-id="0496f-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="0496f-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="0496f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0496f-105">**Faktiske verdier**-enheten har mange felt som kan brukes som prisdimensjoner for ressursbasert prissetting.</span><span class="sxs-lookup"><span data-stu-id="0496f-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="0496f-106">Ett felles felt er for eksempel **Ressurs som kan bestilles**.</span><span class="sxs-lookup"><span data-stu-id="0496f-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="0496f-107">Mindre selskaper som har færre enn 20–30 fakturerbare ressurser, kan oppdage at det å ha spesifikke fakturerings- og kostnadssatser for hver ressurs, er en enklere måte.</span><span class="sxs-lookup"><span data-stu-id="0496f-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="0496f-108">Men etter hvert som den fakturerbare arbeidsstyrken vokser, kan imidlertid ressursspesifikke priser bli urealistisk å vedlikeholde.</span><span class="sxs-lookup"><span data-stu-id="0496f-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="0496f-109">Ressurskostnader og fakturasatser begynner å variere etter hvert som ressursene blir forfremmet, får mer erfaring eller oppnår et ulikt sett med ferdigheter.</span><span class="sxs-lookup"><span data-stu-id="0496f-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="0496f-110">Et annet eksempel er en transaksjonskategori.</span><span class="sxs-lookup"><span data-stu-id="0496f-110">Another example is that of transaction category.</span></span> <span data-ttu-id="0496f-111">Kunder og implementerere har brukt transaksjonskategorien til å klassifisere arbeid og bruke feltet til pris og kostnad basert på arbeidskategorien.</span><span class="sxs-lookup"><span data-stu-id="0496f-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]