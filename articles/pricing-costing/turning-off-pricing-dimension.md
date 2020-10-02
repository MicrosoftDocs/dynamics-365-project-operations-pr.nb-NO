---
title: Deaktivere en prisdimensjon
description: Dette emnet gir informasjon om hvordan du deaktiverer prisdimensjoner.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 54e02726138f7306481ca50d5204ee29a3b68549
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896518"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="24830-103">Deaktivere en prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="24830-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="24830-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="24830-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="24830-105">Det kan hende du må se gjennom og oppdatere prisstrategien med noen års mellomrom.</span><span class="sxs-lookup"><span data-stu-id="24830-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="24830-106">Eventuelle oppdateringer du gjør, krever kanskje at du slår av en eksisterende prisdimensjon og oppretter en ny.</span><span class="sxs-lookup"><span data-stu-id="24830-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="24830-107">Du kan for eksempel tidligere ha priset etter **Rolle**, men du har nå bestemt deg for å prise etter **Arbeidserfaring**.</span><span class="sxs-lookup"><span data-stu-id="24830-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="24830-108">Dette kan kreve at du deaktiverer **Rolle** som en prissettingsdimensjon og oppretter **Arbeidserfaring** som en ny prissetingsdimensjon.</span><span class="sxs-lookup"><span data-stu-id="24830-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="24830-109">Hvis du slår av en prisingsmodell, uavhengig av om den er standard eller egendefinert, kan det utføres ved å sette feltene **Gjelder kostnad** og **Gjelder salg** for prisingsdimensjonen til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="24830-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="24830-110">Når du gjør dette, kan det imidlertid hende at du får en feilmelding om at **prisdimensjonen ikke kan oppdateres eller slettes hvis det finnes tilknyttede prisoppføringer.**</span><span class="sxs-lookup"><span data-stu-id="24830-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

<span data-ttu-id="24830-111">Denne feilmeldingen angir at det finnes prisoppføringer som tidligere ble angitt for dimensjonen, som blir deaktivert.</span><span class="sxs-lookup"><span data-stu-id="24830-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="24830-112">Alle **Rollepris**- og **Rolleprispåslag**-oppføringer som refererer til en dimensjon, må slettes før dimensjonens bruk kan settes til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="24830-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="24830-113">Denne regelen gjelder både for standard prisdimensjoner og egendefinerte prisdimensjoner som du kan ha opprettet.</span><span class="sxs-lookup"><span data-stu-id="24830-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="24830-114">Årsaken til denne valideringen er at hver **Rollepris**-oppføring må ha en unik kombinasjon av dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="24830-114">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="24830-115">For eksempel, på en prisliste som kalles **Amerikanske kostsatser 2018**, har du følgende **Rollepris**-rader.</span><span class="sxs-lookup"><span data-stu-id="24830-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="24830-116">Standardtittel</span><span class="sxs-lookup"><span data-stu-id="24830-116">Standard Title</span></span>         | <span data-ttu-id="24830-117">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="24830-117">Org Unit</span></span>    |<span data-ttu-id="24830-118">Enhet</span><span class="sxs-lookup"><span data-stu-id="24830-118">Unit</span></span>   |<span data-ttu-id="24830-119">Pris</span><span class="sxs-lookup"><span data-stu-id="24830-119">Price</span></span>  |<span data-ttu-id="24830-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="24830-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="24830-121">Systemingeniør</span><span class="sxs-lookup"><span data-stu-id="24830-121">Systems Engineer</span></span>|<span data-ttu-id="24830-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="24830-122">Contoso US</span></span>|<span data-ttu-id="24830-123">Hour</span><span class="sxs-lookup"><span data-stu-id="24830-123">Hour</span></span>| <span data-ttu-id="24830-124">100</span><span class="sxs-lookup"><span data-stu-id="24830-124">100</span></span>|<span data-ttu-id="24830-125">USD</span><span class="sxs-lookup"><span data-stu-id="24830-125">USD</span></span>|
| <span data-ttu-id="24830-126">Senior systemingeniør</span><span class="sxs-lookup"><span data-stu-id="24830-126">Senior Systems Engineer</span></span>|<span data-ttu-id="24830-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="24830-127">Contoso US</span></span>|<span data-ttu-id="24830-128">Hour</span><span class="sxs-lookup"><span data-stu-id="24830-128">Hour</span></span>| <span data-ttu-id="24830-129">150</span><span class="sxs-lookup"><span data-stu-id="24830-129">150</span></span>| <span data-ttu-id="24830-130">USD</span><span class="sxs-lookup"><span data-stu-id="24830-130">USD</span></span>|


<span data-ttu-id="24830-131">Når du deaktiverer **Standardtittel** som prisdimensjon, og prismotoren søker etter en pris, vil den bare bruke verdien **Organisasjonsenhet** fra inndatakonteksten.</span><span class="sxs-lookup"><span data-stu-id="24830-131">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="24830-132">Hvis **Organisasjonsenhet** i inndatakonteksten er "Ekeli USA", vil resultatet være ikke-deterministisk, fordi begge radene samsvarer.</span><span class="sxs-lookup"><span data-stu-id="24830-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="24830-133">For å unngi dette scenarioet, validerer systemet at kombinasjonen av dimensjoner er unik når du oppretter **Rollepris**.</span><span class="sxs-lookup"><span data-stu-id="24830-133">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="24830-134">Hvis dimensjonen er deaktivert etter at **Rollepris**-oppføringene er opprettet, kan denne begrensningen brytes.</span><span class="sxs-lookup"><span data-stu-id="24830-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="24830-135">Derfor kreves det at du sletter alle **Rollepris**- og **Rolleprispåslag**-rader som har denne dimensjonsverdien fylt ut, før du slår av dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="24830-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
