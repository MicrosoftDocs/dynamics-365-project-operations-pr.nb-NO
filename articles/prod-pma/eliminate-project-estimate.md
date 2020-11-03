---
title: Eliminere et prosjektestimat
description: Dette emnet gir informasjon om å eliminere et prosjektestimat etter at det er fullført.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081673"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="ee3f4-103">Eliminere et prosjektestimat</span><span class="sxs-lookup"><span data-stu-id="ee3f4-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee3f4-104">Prosjektestimater gir en økonomisk oversikt for arbeid som beregnet og planlagt for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="ee3f4-105">Hvis du vil arbeide med estimater for et prosjekt, må du legge ved prosjektet i et estimatprosjekt.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="ee3f4-106">Et estimatprosjekt er alltid basert på et eksisterende prosjekt, men flere prosjekter kan referere til et enkelt estimatprosjekt.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="ee3f4-107">Bare fastprisprosjekter og investeringsprosjekter kan knyttes til estimatprosjekter, og disse prosjektene må tilhøre samme prosjektgruppe som estimatprosjektet.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="ee3f4-108">Hvis du vil eliminere et estimatprosjekt, må det være fullført.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="ee3f4-109">Fremgangsmåten nedenfor forklarer hvordan du eliminerer et estimat.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="ee3f4-110">Gå til **Prosjektstyring og regnskap** > **Alle prosjekter** , og åpne prosjektet.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="ee3f4-111">På **Administrer** -fanen velger du **Estimatrs** , og på **Estimat** -siden velger du **Eliminer**.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="ee3f4-112">På siden **Eliminer estimat** , på **Generelt** -fanen angir du følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="ee3f4-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="ee3f4-113">**Periodekode** : Velg periodekoden for å velge de aktuelle estimatprosjektene.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="ee3f4-114">**Estimatdato** : Velg den aktuelle estimatdatoen for eliminering.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="ee3f4-115">**Eliminer med VIA-advarsler** : Aktiver dette alternativet for å gi beskjed når et estimat som er knyttet til pågående arbeid (VIA), blir eliminert.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="ee3f4-116">Når det ikke er merket av for dette alternativet, kan ikke eliminering fortsette hvis det ikke finnes noen ikke-estimerte transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="ee3f4-117">Dette alternativet er bare tilgjengelig når eliminering brukes på et estimatprosjekt.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="ee3f4-118">Det er ikke tilgjengelig hvis du bruker periodiske posteringer.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="ee3f4-119">Denne innstillingen fungerer med innstillingene på **Estimat** -fanen på siden **Prosjektparametere** i feltgruppen **Tillat eliminering når det finnes ikke-estimerte transaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="ee3f4-120">**Angi fase til fullført** : Aktiver dette alternativet for å angi estimatprosjektets fase til **Fullført** etter at du har kjørt elimineringen.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="ee3f4-121">**Skriv ut estimatliste** : Velg informasjonen som skal inkluderes når estimatlisten skrives ut.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="ee3f4-122">**Vis infologg** : Aktiver dette alternativet for å vise infologgen.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="ee3f4-123">**Bokføringsdato** : Velg bokføringsdatoen i hovedboken for estimatet.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="ee3f4-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-124">Select **OK**.</span></span>
5. <span data-ttu-id="ee3f4-125">Når elimineringsprosessen er fullført, vises det eliminerte estimatprosjektet med en negativ verdi.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="ee3f4-126">Hvis du ikke har tenkt å eliminere et estimat, kan du velge det eliminerte estimatet og velge **Gjør om eliminering**.</span><span class="sxs-lookup"><span data-stu-id="ee3f4-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
