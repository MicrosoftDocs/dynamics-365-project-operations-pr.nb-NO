---
title: Prosjektfaser
description: Dette emnet gir informasjon om prosjektstadier som er tilgjengelige i Microsoft Dynamics Project Operations.
author: ruhercul
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
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127485"
---
# <a name="project-stages"></a><span data-ttu-id="39c84-103">Prosjektfaser</span><span class="sxs-lookup"><span data-stu-id="39c84-103">Project stages</span></span>

<span data-ttu-id="39c84-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="39c84-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="39c84-105">Prosjektfaser skal vise statusen til prosjektet etter hvert som det pågår.</span><span class="sxs-lookup"><span data-stu-id="39c84-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="39c84-106">Tilpassinger kan brukes til automatisk å oppdatere fasene med forretningsprosessflyter, Power Automate eller plugin-modulutvidelser.</span><span class="sxs-lookup"><span data-stu-id="39c84-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="39c84-107">Følgende faser er definert i standard forretningsprosessflyt:</span><span class="sxs-lookup"><span data-stu-id="39c84-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="39c84-108">Nye</span><span class="sxs-lookup"><span data-stu-id="39c84-108">New</span></span>
- <span data-ttu-id="39c84-109">Tilbud</span><span class="sxs-lookup"><span data-stu-id="39c84-109">Quote</span></span>
- <span data-ttu-id="39c84-110">Planlegg</span><span class="sxs-lookup"><span data-stu-id="39c84-110">Plan</span></span>
- <span data-ttu-id="39c84-111">Lever</span><span class="sxs-lookup"><span data-stu-id="39c84-111">Deliver</span></span>
- <span data-ttu-id="39c84-112">Fullført</span><span class="sxs-lookup"><span data-stu-id="39c84-112">Complete</span></span>
- <span data-ttu-id="39c84-113">Lukk</span><span class="sxs-lookup"><span data-stu-id="39c84-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="39c84-114">Nye</span><span class="sxs-lookup"><span data-stu-id="39c84-114">New</span></span>

<span data-ttu-id="39c84-115">Når du oppretter et prosjekt, er prosjektfasen satt til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="39c84-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="39c84-116">Hvis prosjektet ble opprettet fra en mal, kan det ha tidsplan-, estimat- og teamdata.</span><span class="sxs-lookup"><span data-stu-id="39c84-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="39c84-117">Ellers er det en disposisjon av prosjektet, og de resterende komponentene må registreres.</span><span class="sxs-lookup"><span data-stu-id="39c84-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="39c84-118">Tilbud</span><span class="sxs-lookup"><span data-stu-id="39c84-118">Quote</span></span>

<span data-ttu-id="39c84-119">Når du knytter et prosjekt til et tilbud, eller når du oppretter et prosjekt fra et tilbud, er prosjektfasen satt til **Tilbud**, og de estimerte start- og sluttdatoene oppdateres også.</span><span class="sxs-lookup"><span data-stu-id="39c84-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="39c84-120">Når prosjektet er i **Tilbud**-fasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjektenhet**-siden.</span><span class="sxs-lookup"><span data-stu-id="39c84-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="39c84-121">Plan</span><span class="sxs-lookup"><span data-stu-id="39c84-121">Plan</span></span>

<span data-ttu-id="39c84-122">Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til **Kontrakt**-fasen, oppdateres prosjektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="39c84-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="39c84-123">Når prosjektet er i **Plan**-fasen, vises detaljene for kontrakten på **Prosjektenhet**-siden.</span><span class="sxs-lookup"><span data-stu-id="39c84-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="39c84-124">Lever</span><span class="sxs-lookup"><span data-stu-id="39c84-124">Deliver</span></span>

<span data-ttu-id="39c84-125">Når prosjektplanen er fullført, og du er klar til å starte prosjektet, skal prosjektlederen oppdatere prosjektfasen til **Lever** for å vise at prosjektet har startet.</span><span class="sxs-lookup"><span data-stu-id="39c84-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="39c84-126">Fullstendig</span><span class="sxs-lookup"><span data-stu-id="39c84-126">Complete</span></span> 

<span data-ttu-id="39c84-127">Når arbeidet for prosjektet er fullført, kan prosjekt lederen oppdatere fasen til **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="39c84-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="39c84-128">Ved å oppdatere prosjektstadiet til **Fullfør** angir prosjektlederen at arbeidet er 100 prosent fullført, men at prosjektet holdes åpent slik at eventuelle ventende tids- eller utgiftsoppføringer kan registreres.</span><span class="sxs-lookup"><span data-stu-id="39c84-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="39c84-129">Lukk</span><span class="sxs-lookup"><span data-stu-id="39c84-129">Close</span></span>

<span data-ttu-id="39c84-130">Når alle transaksjoner er registrert for prosjektet, kan prosjektlederen oppdatere fasen til **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="39c84-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="39c84-131">På dette tidspunktet kan det ikke registreres noen transaksjoner, og prosjektet er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="39c84-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

