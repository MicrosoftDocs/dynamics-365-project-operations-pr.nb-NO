---
title: Bruke et eksisterende felt i Project Service som en prisdimensjon
description: Dette emnet inneholder informasjon om hvordan du bruker eksisterende Project Service-felt som prisdimensjoner.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081698"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="366f9-103">Bruke et eksisterende felt i Project Service som en prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="366f9-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="366f9-104">Project Service Automation (PSA) har mange felt i enheten **Faktiske verdier** som kan brukes som prisdimensjoner for ressursbaserte priser i prosjektorganisasjoner.</span><span class="sxs-lookup"><span data-stu-id="366f9-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="366f9-105">Ett felles felt er for eksempel **Ressurs som kan bestilles**.</span><span class="sxs-lookup"><span data-stu-id="366f9-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="366f9-106">Mindre selskaper som har færre enn 20–30 fakturerbare ressurser, kan oppdage at det å ha spesifikke fakturerings- og kostnadssatser for hver ressurs, er en enklere måte.</span><span class="sxs-lookup"><span data-stu-id="366f9-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="366f9-107">Men etter hvert som den fakturerbar arbeidsstyrken vokser, kan dette imidlertid bli urealistisk å beholde når ressurskostnader og betalingssatser begynner å variere etter hvert som ressursene blir forfremmet, får mer erfaring eller oppnår forskjellige ferdighetssett.</span><span class="sxs-lookup"><span data-stu-id="366f9-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="366f9-108">Siden denne metoden fortsatt fungerer for selskaper av en bestemt størrelse, kan du se emnet [Bruke bestillbar ressurs som en prisingsdimensjon](bookable-resource-pricing-dimension.md) for å forstå hvordan et eksisterende Project Service-felt kan brukes som en prissettingsdimensjon.</span><span class="sxs-lookup"><span data-stu-id="366f9-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="366f9-109">Et annet eksempel er en transaksjonskategori.</span><span class="sxs-lookup"><span data-stu-id="366f9-109">Another example is that of transaction category.</span></span> <span data-ttu-id="366f9-110">Kunder og implementerere har brukt transaksjonskategorien i PSA til å klassifisere arbeid og bruke feltet til pris og kostnad basert på arbeidskategorien.</span><span class="sxs-lookup"><span data-stu-id="366f9-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="366f9-111">Hvis du vil ha mer informasjon, se [Bruke transaksjonskategori som prisdimensjon](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="366f9-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
