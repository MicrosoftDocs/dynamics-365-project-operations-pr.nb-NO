---
title: Deaktivere en prisdimensjon
description: Dette emnet viser hvordan du konfigurerer prisdimensjoner i Project Service- løsningen.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da8615fa147838d9088c639039d5a2534e662e82
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014308"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="8db88-103">Deaktivere en prisdimensjon</span><span class="sxs-lookup"><span data-stu-id="8db88-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8db88-104">Det kan hende du må se gjennom og oppdatere prisstrategien med noen års mellomrom.</span><span class="sxs-lookup"><span data-stu-id="8db88-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="8db88-105">Eventuelle oppdateringer du gjør, krever kanskje at du slår av en eksisterende prisdimensjon og oppretter en ny.</span><span class="sxs-lookup"><span data-stu-id="8db88-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="8db88-106">Du kan for eksempel tidligere ha priset etter **Rolle**, men du har nå bestemt deg for å prise etter **Arbeidserfaring**.</span><span class="sxs-lookup"><span data-stu-id="8db88-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="8db88-107">Dette kan kreve at du deaktiverer **Rolle** som en prissettingsdimensjon og oppretter **Arbeidserfaring** som en ny prissetingsdimensjon.</span><span class="sxs-lookup"><span data-stu-id="8db88-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="8db88-108">Hvis du slår av en prisingsmodell, uavhengig av om den er standard eller egendefinert, kan det utføres ved å sette feltene **Gjelder kostnad** og **Gjelder salg** for prisingsdimensjonen til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8db88-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="8db88-109">Når du gjør dette, kan du imidlertid få følgende feilmelding:</span><span class="sxs-lookup"><span data-stu-id="8db88-109">However, when you do this, you might receive the following error message.</span></span>

![Feil ved forretningsprosess er sannsynlig når du slår av en prissettingssdimensjon](media/Business-Process-Error.png)


<span data-ttu-id="8db88-111">Denne feilmeldingen angir at det finnes prisoppføringer som tidligere ble angitt for dimensjonen, som blir deaktivert.</span><span class="sxs-lookup"><span data-stu-id="8db88-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="8db88-112">Alle **Rollepris**- og **Rolleprispåslag**-oppføringer som refererer til en dimensjon, må slettes før dimensjonens bruk kan settes til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="8db88-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="8db88-113">Denne regelen gjelder både for standard prisdimensjoner og egendefinerte prisdimensjoner som du kan ha opprettet.</span><span class="sxs-lookup"><span data-stu-id="8db88-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="8db88-114">Årsaken til denne valideringen er at Project Service har en begrensning om at hver **Rollepris**-oppføring må ha en unik kombinasjon av dimensjoner.</span><span class="sxs-lookup"><span data-stu-id="8db88-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="8db88-115">For eksempel, på en prisliste som kalles **Amerikanske kostsatser 2018**, har du følgende **Rollepris**-rader.</span><span class="sxs-lookup"><span data-stu-id="8db88-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="8db88-116">Standardtittel</span><span class="sxs-lookup"><span data-stu-id="8db88-116">Standard Title</span></span>         | <span data-ttu-id="8db88-117">Organisasjonsenhet</span><span class="sxs-lookup"><span data-stu-id="8db88-117">Org Unit</span></span>    |<span data-ttu-id="8db88-118">Enhet</span><span class="sxs-lookup"><span data-stu-id="8db88-118">Unit</span></span>   |<span data-ttu-id="8db88-119">Pris</span><span class="sxs-lookup"><span data-stu-id="8db88-119">Price</span></span>  |<span data-ttu-id="8db88-120">Valuta</span><span class="sxs-lookup"><span data-stu-id="8db88-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="8db88-121">Systemingeniør</span><span class="sxs-lookup"><span data-stu-id="8db88-121">Systems Engineer</span></span>|<span data-ttu-id="8db88-122">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="8db88-122">Contoso US</span></span>|<span data-ttu-id="8db88-123">Time</span><span class="sxs-lookup"><span data-stu-id="8db88-123">Hour</span></span>| <span data-ttu-id="8db88-124">100</span><span class="sxs-lookup"><span data-stu-id="8db88-124">100</span></span>|<span data-ttu-id="8db88-125">USD</span><span class="sxs-lookup"><span data-stu-id="8db88-125">USD</span></span>|
| <span data-ttu-id="8db88-126">Senior systemingeniør</span><span class="sxs-lookup"><span data-stu-id="8db88-126">Senior Systems Engineer</span></span>|<span data-ttu-id="8db88-127">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="8db88-127">Contoso US</span></span>|<span data-ttu-id="8db88-128">Time</span><span class="sxs-lookup"><span data-stu-id="8db88-128">Hour</span></span>| <span data-ttu-id="8db88-129">150</span><span class="sxs-lookup"><span data-stu-id="8db88-129">150</span></span>| <span data-ttu-id="8db88-130">USD</span><span class="sxs-lookup"><span data-stu-id="8db88-130">USD</span></span>|


<span data-ttu-id="8db88-131">Når du deaktiverer **Standardtittel** som prisdimensjon, og Project Service-prismotoren søker etter en pris, vil den bare bruke verdien **Organisasjonsenhet** fra inndatakonteksten.</span><span class="sxs-lookup"><span data-stu-id="8db88-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="8db88-132">Hvis **Organisasjonsenhet** i inndatakonteksten er "Contoso USA", vil resultatet være ikke-deterministisk, fordi begge radene samsvarer.</span><span class="sxs-lookup"><span data-stu-id="8db88-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="8db88-133">For å unngi dette scenarioet, validerer Project Service at kombinasjonen av dimensjoner er unik når du oppretter **Rollepris**.</span><span class="sxs-lookup"><span data-stu-id="8db88-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="8db88-134">Hvis dimensjonen er deaktivert etter at **Rollepris**-oppføringene er opprettet, kan denne begrensningen brytes.</span><span class="sxs-lookup"><span data-stu-id="8db88-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="8db88-135">Derfor kreves det at du sletter alle **Rollepris**- og **Rolleprispåslag**-rader som har denne dimensjonsverdien fylt ut, før du slår av dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="8db88-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]