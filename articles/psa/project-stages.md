---
title: Prosjektfasetyper
description: Denne emnet gir informasjon om prosjektfaser.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: aa423979a794b07a8bd27440f47a29480b74b518
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123074"
---
# <a name="project-stage-types"></a><span data-ttu-id="4c4d2-103">Prosjektfasetyper</span><span class="sxs-lookup"><span data-stu-id="4c4d2-103">Project stage types</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4c4d2-104">Prosjektfaser skal vise statusen til prosjektet etter hvert som det pågår.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="4c4d2-105">Tilpassinger kan brukes til automatisk å oppdatere fasene med forretningsprosessflyter, Power Automate eller plugin-modulutvidelser.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="4c4d2-106">Følgende faser er definert i standard BPF:</span><span class="sxs-lookup"><span data-stu-id="4c4d2-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="4c4d2-107">Nytt</span><span class="sxs-lookup"><span data-stu-id="4c4d2-107">New</span></span>
- <span data-ttu-id="4c4d2-108">Tilbud</span><span class="sxs-lookup"><span data-stu-id="4c4d2-108">Quote</span></span>
- <span data-ttu-id="4c4d2-109">Plan</span><span class="sxs-lookup"><span data-stu-id="4c4d2-109">Plan</span></span>
- <span data-ttu-id="4c4d2-110">Lever</span><span class="sxs-lookup"><span data-stu-id="4c4d2-110">Deliver</span></span>
- <span data-ttu-id="4c4d2-111">Fullstendig</span><span class="sxs-lookup"><span data-stu-id="4c4d2-111">Complete</span></span>
- <span data-ttu-id="4c4d2-112">Lukk</span><span class="sxs-lookup"><span data-stu-id="4c4d2-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="4c4d2-113">Ny</span><span class="sxs-lookup"><span data-stu-id="4c4d2-113">New</span></span>

<span data-ttu-id="4c4d2-114">Når du oppretter et prosjekt, er prosjektfasen satt til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="4c4d2-115">Hvis prosjektet ble opprettet fra en mal, kan det ha tidsplan-, estimat- og teamdata.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="4c4d2-116">Ellers er det bare en disposisjon av prosjektet, og de resterende komponentene må registreres.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="4c4d2-117">Tilbud</span><span class="sxs-lookup"><span data-stu-id="4c4d2-117">Quote</span></span>

<span data-ttu-id="4c4d2-118">Når du knytter et prosjekt til et tilbud, eller når du oppretter et prosjekt fra et tilbud, er prosjektfasen satt til **Tilbud**, og de estimerte start- og sluttdatoene oppdateres også.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="4c4d2-119">Når prosjektet er i **Tilbud**-fasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjektenhet**-siden.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="4c4d2-120">Plan</span><span class="sxs-lookup"><span data-stu-id="4c4d2-120">Plan</span></span>

<span data-ttu-id="4c4d2-121">Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til **Kontrakt**-fasen, oppdateres prosjektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="4c4d2-122">Når prosjektet er i **Plan**-fasen, vises detaljene for kontrakten på **Prosjektenhet**-siden.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="4c4d2-123">Lever</span><span class="sxs-lookup"><span data-stu-id="4c4d2-123">Deliver</span></span>

<span data-ttu-id="4c4d2-124">Når prosjektplanen er fullført, og du er klar til å starte prosjektet, skal prosjektlederen oppdatere prosjektfasen til **Lever** for å vise at prosjektet har startet.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="4c4d2-125">Fullstendig</span><span class="sxs-lookup"><span data-stu-id="4c4d2-125">Complete</span></span> 

<span data-ttu-id="4c4d2-126">Når arbeidet for prosjektet er fullført, kan prosjekt lederen oppdatere fasen til **Fullfør**.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="4c4d2-127">Ved å oppdatere prosjektstadiet til **Fullfør** angir prosjektlederen at arbeidet er 100 prosent fullført, men at prosjektet holdes åpent slik at eventuelle ventende tids- eller utgiftsoppføringer kan registreres.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="4c4d2-128">Lukk</span><span class="sxs-lookup"><span data-stu-id="4c4d2-128">Close</span></span>

<span data-ttu-id="4c4d2-129">Når alle transaksjoner er registrert for prosjektet, kan prosjektlederen oppdatere fasen til **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="4c4d2-130">På dette tidspunktet kan det ikke registreres noen transaksjoner, og prosjektet er skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="4c4d2-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
