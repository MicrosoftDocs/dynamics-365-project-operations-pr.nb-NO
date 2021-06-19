---
title: Startsiden for oppgradering
description: Dette emnet viser hvor du finner viktig informasjon om nye og endrede funksjoner i Dynamics 365 Project Service Automation, og prosessen med å oppgradere til nyeste versjon.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012373"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="237e7-103">Startsiden for oppgradering</span><span class="sxs-lookup"><span data-stu-id="237e7-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="237e7-104">Oppgradere fra PSA-versjon 2.x eller 1.x til versjon 3.x</span><span class="sxs-lookup"><span data-stu-id="237e7-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="237e7-105">Nye forekomster</span><span class="sxs-lookup"><span data-stu-id="237e7-105">New instances</span></span>

<span data-ttu-id="237e7-106">Fra og med 17. mai 2019, når Project Service Automation velges under klargjøring av en ny forekomst, installeres versjon 3. x som standard.</span><span class="sxs-lookup"><span data-stu-id="237e7-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="237e7-107">Eksisterende forekomster</span><span class="sxs-lookup"><span data-stu-id="237e7-107">Existing instances</span></span>

<span data-ttu-id="237e7-108">Tidligere måtte kunder som hadde en forekomst av PSA versjon 2.x og som måtte oppgradere til versjon 3.x, som er UCI-versjonen (Unified Client Interfaced-based) av PSA, kontakte Microsofts kundestøtte og oppgi detaljene for sin versjon slik at kundestøtten kunne aktivere versjonen for oppgradering til versjon 3.x.</span><span class="sxs-lookup"><span data-stu-id="237e7-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="237e7-109">Fra og med 1. mars 2020 kan kunder som har en forekomst av PSA versjon 2.x og som må oppgradere til versjon 3.x, oppgradere sine versjoner direkte fra administrasjonsportalen uten å måtte kontakte Microsofts kundestøtte.</span><span class="sxs-lookup"><span data-stu-id="237e7-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="237e7-110">PSA versjon 3. x inneholder omfattende endringer.</span><span class="sxs-lookup"><span data-stu-id="237e7-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="237e7-111">Den er bygd på Enhetlig grensesnitt-rammeverket for å hjelpe deg med å gi en forbedret brukeropplevelse.</span><span class="sxs-lookup"><span data-stu-id="237e7-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="237e7-112">Den nyutviklede appen leverer et ensartet og gjennomført brukergrensesnitt som følger responsive utformingsprinsipper på best mulig måte for optimal visning på alle skjermstørrelser og enheter.</span><span class="sxs-lookup"><span data-stu-id="237e7-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="237e7-113">Det har vært andre endringer i hele programmet.</span><span class="sxs-lookup"><span data-stu-id="237e7-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="237e7-114">Noen av områdene som er endret, er priser, bestilling og tilordning av ressurser, tid, utgifter og godkjenninger.</span><span class="sxs-lookup"><span data-stu-id="237e7-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="237e7-115">Før du begynner oppgraderingsprosessen, anbefaler vi at du fullfører følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="237e7-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="237e7-116">Kontroller om både Dynamics 365 Field Service og Project Service Automation er installert på den identifiserte forekomsten.</span><span class="sxs-lookup"><span data-stu-id="237e7-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="237e7-117">Hvis begge løsningene er installert, må du planlegge å oppgradere begge før du gjenopptar vanlig bruk av forekomsten.</span><span class="sxs-lookup"><span data-stu-id="237e7-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="237e7-118">Se nøye gjennom følgende emner.</span><span class="sxs-lookup"><span data-stu-id="237e7-118">Carefully review the following topics.</span></span> <span data-ttu-id="237e7-119">Bevissthet og forståelse rundt endringene mellom versjonene hjelper deg med oppgraderingsprosessen.</span><span class="sxs-lookup"><span data-stu-id="237e7-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="237e7-120">Disse emnene inneholder informasjon om de viktigste endringene i PSA, sammen med hensyn og anbefalinger for planlegging av oppgraderingen til versjon 3. x.</span><span class="sxs-lookup"><span data-stu-id="237e7-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="237e7-121">Hva er nytt eller endret i Project Service Automation versjon 3</span><span class="sxs-lookup"><span data-stu-id="237e7-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="237e7-122">Hensyn ved oppgradering – Project Service Automation versjon 2.x eller 1.x til versjon 3.x</span><span class="sxs-lookup"><span data-stu-id="237e7-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="237e7-123">Oppgrader sandkasseforekomsten din for å evaluere endringene i implementeringen før du oppgraderer produksjonsforekomsten din.</span><span class="sxs-lookup"><span data-stu-id="237e7-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="237e7-124">Når du har sett gjennom emnene som ble nevnt tidligere, og er klar til å oppgradere til PSA versjon 3. x eller den UCI-baserte versjonen, sender du en forespørsel til Microsoft kundestøtte for å gjøre oppgraderingen tilgjengelig fra administrasjonssenteret.</span><span class="sxs-lookup"><span data-stu-id="237e7-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="237e7-125">Angi detaljene for forekomsten i forespørselen.</span><span class="sxs-lookup"><span data-stu-id="237e7-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="237e7-126">Eldre versjoner av PSA (PSA version 2. x) i en nyopprettet forekomst</span><span class="sxs-lookup"><span data-stu-id="237e7-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="237e7-127">Fra og med 17. mai 2019 vil alle nye forekomster ha UCI som standardklient.</span><span class="sxs-lookup"><span data-stu-id="237e7-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="237e7-128">Når det gjelder justering til denne endringen, blir PSA-versjon 3. x og Field Service versjon 8.x klargjort som standard, fordi disse versjonene er utformet for å fungere med UCI-klienten.</span><span class="sxs-lookup"><span data-stu-id="237e7-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="237e7-129">Fra og med 1. mars 2020 kan ikke Dynamics PSA-kunder lenger opprette et nytt miljø med eldre versjoner av PSA, for eksempel PSA versjon 2.x eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="237e7-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="237e7-130">Alle nye miljøer vil bare få versjon 3.x av PSA.</span><span class="sxs-lookup"><span data-stu-id="237e7-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="237e7-131">For å få best mulig utbytte når du bruker eldre versjoner av Field Service og PSA, går du til siden **Systeminnstillinger**, og for feltet **Bruk bare det nye enhetlige grensesnittet (anbefales)** velger du **Nei**, fordi disse versjonene ikke er utformet for å lastes inn på riktig måte i UCI.</span><span class="sxs-lookup"><span data-stu-id="237e7-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="237e7-132">Når du har deaktivert UCI, kan du åpne og kjøre disse versjonene av Field Service og PSA ved å bruke den gamle webklienten.</span><span class="sxs-lookup"><span data-stu-id="237e7-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]