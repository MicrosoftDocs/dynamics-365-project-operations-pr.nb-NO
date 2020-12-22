---
title: Deaktivere en prisdimensjon
description: Dette emnet gir informasjon om hvordan du deaktiverer prisdimensjoner.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650061"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="f0835-103">Deaktivere en prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="f0835-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="f0835-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="f0835-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0835-105">Det kan hende du må se gjennom og oppdatere prisstrategien med noen års mellomrom.</span><span class="sxs-lookup"><span data-stu-id="f0835-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="f0835-106">Eventuelle oppdateringer du gjør, krever kanskje at du slår av en eksisterende prisdimensjon og oppretter en ny.</span><span class="sxs-lookup"><span data-stu-id="f0835-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="f0835-107">Du kan for eksempel tidligere ha priset etter **Rolle**, men du har nå bestemt deg for å prise etter **Arbeidserfaring**.</span><span class="sxs-lookup"><span data-stu-id="f0835-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="f0835-108">Dette kan kreve at du deaktiverer **Rolle** som en prissettingsdimensjon og oppretter **Arbeidserfaring** som en ny prissetingsdimensjon.</span><span class="sxs-lookup"><span data-stu-id="f0835-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="f0835-109">Hvis du slår av en prisingsmodell, uavhengig av om den er standard eller egendefinert, kan det utføres ved å sette feltene **Gjelder kostnad** og **Gjelder salg** for prisingsdimensjonen til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="f0835-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="f0835-110">Når du gjør dette, kan det imidlertid hende at du får en feilmelding om at **prisdimensjonen ikke kan oppdateres eller slettes hvis det finnes tilknyttede prisoppføringer.**</span><span class="sxs-lookup"><span data-stu-id="f0835-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Feil ved forretningsprosess er sannsynlig når du slår av en prissettingssdimensjon](media/Business-Process-Error.png)

<span data-ttu-id="f0835-112">Denne feilmeldingen angir at det finnes prisoppføringer som tidligere ble angitt for dimensjonen, som blir deaktivert.</span><span class="sxs-lookup"><span data-stu-id="f0835-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="f0835-113">Alle **Rollepris**- og **Rolleprispåslag**-oppføringer som refererer til en dimensjon, må slettes før dimensjonens bruk kan settes til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="f0835-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="f0835-114">Denne regelen gjelder både for standard prisdimensjoner og egendefinerte prisdimensjoner som du kan ha opprettet.</span><span class="sxs-lookup"><span data-stu-id="f0835-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="f0835-115">Årsaken til denne valideringen er at hver **Rollepris**-oppføring må ha en unik kombinasjon av dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f0835-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="f0835-116">For eksempel, på en prisliste som kalles **Amerikanske kostsatser 2018**, har du følgende **Rollepris**-rader.</span><span class="sxs-lookup"><span data-stu-id="f0835-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="f0835-117">Standardtittel</span><span class="sxs-lookup"><span data-stu-id="f0835-117">Standard Title</span></span>         | <span data-ttu-id="f0835-118">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="f0835-118">Org Unit</span></span>    |<span data-ttu-id="f0835-119">Enhet</span><span class="sxs-lookup"><span data-stu-id="f0835-119">Unit</span></span>   |<span data-ttu-id="f0835-120">Pris</span><span class="sxs-lookup"><span data-stu-id="f0835-120">Price</span></span>  |<span data-ttu-id="f0835-121">Valuta</span><span class="sxs-lookup"><span data-stu-id="f0835-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="f0835-122">Systemingeniør</span><span class="sxs-lookup"><span data-stu-id="f0835-122">Systems Engineer</span></span>|<span data-ttu-id="f0835-123">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f0835-123">Contoso US</span></span>|<span data-ttu-id="f0835-124">Hour</span><span class="sxs-lookup"><span data-stu-id="f0835-124">Hour</span></span>| <span data-ttu-id="f0835-125">100</span><span class="sxs-lookup"><span data-stu-id="f0835-125">100</span></span>|<span data-ttu-id="f0835-126">USD</span><span class="sxs-lookup"><span data-stu-id="f0835-126">USD</span></span>|
| <span data-ttu-id="f0835-127">Senior systemingeniør</span><span class="sxs-lookup"><span data-stu-id="f0835-127">Senior Systems Engineer</span></span>|<span data-ttu-id="f0835-128">Contoso US</span><span class="sxs-lookup"><span data-stu-id="f0835-128">Contoso US</span></span>|<span data-ttu-id="f0835-129">Hour</span><span class="sxs-lookup"><span data-stu-id="f0835-129">Hour</span></span>| <span data-ttu-id="f0835-130">150</span><span class="sxs-lookup"><span data-stu-id="f0835-130">150</span></span>| <span data-ttu-id="f0835-131">USD</span><span class="sxs-lookup"><span data-stu-id="f0835-131">USD</span></span>|


<span data-ttu-id="f0835-132">Når du deaktiverer **Standardtittel** som prisdimensjon, og prismotoren søker etter en pris, vil den bare bruke verdien **Organisasjonsenhet** fra inndatakonteksten.</span><span class="sxs-lookup"><span data-stu-id="f0835-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="f0835-133">Hvis **Organisasjonsenhet** i inndatakonteksten er "Ekeli USA", vil resultatet være ikke-deterministisk, fordi begge radene samsvarer.</span><span class="sxs-lookup"><span data-stu-id="f0835-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="f0835-134">For å unngi dette scenarioet, validerer systemet at kombinasjonen av dimensjoner er unik når du oppretter **Rollepris**.</span><span class="sxs-lookup"><span data-stu-id="f0835-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="f0835-135">Hvis dimensjonen er deaktivert etter at **Rollepris**-oppføringene er opprettet, kan denne begrensningen brytes.</span><span class="sxs-lookup"><span data-stu-id="f0835-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="f0835-136">Derfor kreves det at du sletter alle **Rollepris**- og **Rolleprispåslag**-rader som har denne dimensjonsverdien fylt ut, før du slår av dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="f0835-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>
