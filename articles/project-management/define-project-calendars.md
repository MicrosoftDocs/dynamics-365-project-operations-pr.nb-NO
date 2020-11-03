---
title: Definere prosjektkalendere
description: Dette emnet gir informasjon om hvordan du bruker en prosjektkalender til å spore prosjektplanen.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081794"
---
# <a name="define-project-calendars"></a><span data-ttu-id="3f532-103">Definere prosjektkalendere</span><span class="sxs-lookup"><span data-stu-id="3f532-103">Define project calendars</span></span>

<span data-ttu-id="3f532-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="3f532-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3f532-105">Hvis du vil opprette en prosjektplan, må du opprette en prosjektkalendermal som definerer antallet arbeidstimer for hver dag i tidsplanen og eventuelle tidspunkt selskapet holder stengt.</span><span class="sxs-lookup"><span data-stu-id="3f532-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="3f532-106">Hvis du vil opprette en prosjektkalendermal, kan du knytte en arbeidsmal til **Kalendermal** -feltet for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f532-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="3f532-107">Følg denne fremgangsmåten for å opprette en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="3f532-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="3f532-108">Velg **Ressurser** i venstre navigasjonsrute.</span><span class="sxs-lookup"><span data-stu-id="3f532-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="3f532-109">På **Ressurser** -listesiden åpner du en brukeroppføring og velger deretter **Vis arbeidstimer**.</span><span class="sxs-lookup"><span data-stu-id="3f532-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="3f532-110">Sørg for at du tillater popup-vinduer på nettlesersiden.</span><span class="sxs-lookup"><span data-stu-id="3f532-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="3f532-111">På denne måten kan du se arbeidstimene som er angitt for ressursen.</span><span class="sxs-lookup"><span data-stu-id="3f532-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="3f532-112">I kategorien **Måndsvisning** klikker du **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="3f532-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="3f532-113">En liste med tre alternativer vises:</span><span class="sxs-lookup"><span data-stu-id="3f532-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="3f532-114">Ny ukeplan</span><span class="sxs-lookup"><span data-stu-id="3f532-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="3f532-115">Arbeidstidsplan for én dag</span><span class="sxs-lookup"><span data-stu-id="3f532-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="3f532-116">Fritid</span><span class="sxs-lookup"><span data-stu-id="3f532-116">Time Off</span></span>

4. <span data-ttu-id="3f532-117">Velg **Ny ukeplan** , og angi deretter alternativene for denne ressursplanen.</span><span class="sxs-lookup"><span data-stu-id="3f532-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="3f532-118">Du kan angi en regelmessig ukeplan, daglige timeparametere, selskapet holder stengt, og så videre.</span><span class="sxs-lookup"><span data-stu-id="3f532-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="3f532-119">Angi datointervallet, velg **Lagre** , og klikk deretter **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="3f532-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="3f532-120">Gå tilbake til **Ressurser** -listesiden, og velg ressursen du angir arbeidstimer for.</span><span class="sxs-lookup"><span data-stu-id="3f532-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="3f532-121">Velg **Angi kalender som** for å angi arbeidsmalen.</span><span class="sxs-lookup"><span data-stu-id="3f532-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="3f532-122">Skriv inn et navn på arbeidsmalen i dialogboksen **Arbeidsmal** , og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="3f532-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="3f532-123">Du kan nå knytte arbeidsmalen til en prosjektkKalendermal.</span><span class="sxs-lookup"><span data-stu-id="3f532-123">You can now associate the work template with a project calendar template.</span></span>
