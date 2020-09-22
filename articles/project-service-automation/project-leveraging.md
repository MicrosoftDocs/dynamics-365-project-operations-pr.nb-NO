---
title: Salgsestimater og prosjekter
description: Dette emnet gir informasjon om hvordan du kan dra nytte av tidsplanen og estimatene i salgsprosessen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754094"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="4b8b0-103">Salgsestimater og prosjekter</span><span class="sxs-lookup"><span data-stu-id="4b8b0-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4b8b0-104">I løpet av salgsprosessen kan du opprette salgsestimater ved å koble et prosjekt til et tilbud.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="4b8b0-105">På denne måten kan deterministisk estimering utføres i løpet av salgsprosessen for å dra nytte av prosjektplanleggings- og estimeringsfunksjoner.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="4b8b0-106">Hvis salget går gjennom, kan tidsplanen som ble brukt til salgsestimeringen, brukes som grunnlag for videre beregning av prosjektplanen.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="4b8b0-107">Koble et prosjekt til en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="4b8b0-107">Linking a project to a quote line</span></span>

<span data-ttu-id="4b8b0-108">Når du oppretter en prosjektbasert tilbudslinje, kan du opprette et nytt prosjekt eller knytte til et eksisterende prosjekt på **Tilbudslinje**-siden.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Tilbudslinje-skjemaet](media/project-8.png)
 
<span data-ttu-id="4b8b0-110">Når du oppretter et nytt prosjekt fra tilbudslinjedetaljene, kan du dra nytte av prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="4b8b0-111">Prosjektmaler er modellprosjekter som representerer standard prosjektplaner og økonomiske estimater som er typiske i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="4b8b0-112">De kan også representere kopier av prosjektplaner og estimater fra tidligere prosjekter.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Tilbudslinjedetaljer](media/project-9.png)
  
<span data-ttu-id="4b8b0-114">Når du oppretter prosjektet fra tilbudet er prosjektet automatisk knyttet til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="4b8b0-115">Estimatkomponenter i et prosjekt</span><span class="sxs-lookup"><span data-stu-id="4b8b0-115">Components of estimates in a project</span></span>

<span data-ttu-id="4b8b0-116">Ved hjelp av en tidsplan kan du dele arbeid inn i oppgaver, vedlikeholde et hierarki med oppgaver, bestemme hvilke ressurser som kreves for å fullføre en oppgave, og tilordne et estimat over innsatsen som kreves for å fullføre en oppgave.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="4b8b0-117">Du kan definere arbeidsinnsatsen og tidsplanestimatene ved hjelp av feltene i kategorien **Tidsplan** på **Prosjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="4b8b0-118">Siden en prisliste er knyttet til prosjektet, beregnes økonomiske estimater ved hjelp av kostnader og salgspriser som er definert i prislisten.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="4b8b0-119">Importere estimater fra et prosjekt til et tilbud</span><span class="sxs-lookup"><span data-stu-id="4b8b0-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="4b8b0-120">Når du har definert prosjektestimater, kan du importere dem til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="4b8b0-121">På siden **Tilbudslinjedetaljer** velger du **Importer fra estimater** på båndet for å oppsummere prosjektestimater etter transaksjonstype, rolle eller oppgavenivå.</span><span class="sxs-lookup"><span data-stu-id="4b8b0-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
