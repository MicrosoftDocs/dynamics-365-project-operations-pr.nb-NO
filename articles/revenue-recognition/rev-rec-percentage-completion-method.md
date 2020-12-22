---
title: Inntektsestimat for fastprisprosjekter
description: Dette emnet gir informasjon om fastprisinntekt i prosjekter.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531510"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="a8590-103">Inntektsestimat for fastprisprosjekter</span><span class="sxs-lookup"><span data-stu-id="a8590-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="a8590-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_</span><span class="sxs-lookup"><span data-stu-id="a8590-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a8590-105">Når du oppretter en prosjektkontraktlinje med følgende attributter i Dynamics 365 Project Operations på Microsoft Dataverse, oppretter systemet automatisk et inntektsestimat for fastprisprosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8590-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="a8590-106">Informasjonen i dette prosjektet er basert på følgende:</span><span class="sxs-lookup"><span data-stu-id="a8590-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="a8590-107">En faktureringsmåte med fast pris.</span><span class="sxs-lookup"><span data-stu-id="a8590-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="a8590-108">Et tilknyttet prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a8590-108">An associated project.</span></span>
  - <span data-ttu-id="a8590-109">Minst én milepæl som er definert i kategorien **Fakturaplan** på **Prosjektkontraktlinje**-siden.</span><span class="sxs-lookup"><span data-stu-id="a8590-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="a8590-110">Gjennomgå inntektsestimater for fastprisprosjekter</span><span class="sxs-lookup"><span data-stu-id="a8590-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="a8590-111">Følg fremgangsmåten nedenfor for å gjennomgå inntektsestimater for fastprisprosjekter:</span><span class="sxs-lookup"><span data-stu-id="a8590-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="a8590-112">I Dynamics 365 Finance-miljøet går du til **Prosjektstyring og regnskap** > **Prosjekter** > **Inntektsestimat for fastprisprosjekter**.</span><span class="sxs-lookup"><span data-stu-id="a8590-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="a8590-113">Velg prosjektet du vil vise, og dobbeltklikk på **Estimatprosjekt-ID** for å åpne oppføringen og gjennomgå detaljene for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a8590-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="a8590-114">Utvid **Prosjekt**-fanen. Du vil se ett prosjekt i **Valgte prosjekter**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a8590-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="a8590-115">Systemet bruker dette som standardprosjektet fordi det er prosjektet som er knyttet til prosjektkontraktlinjen.</span><span class="sxs-lookup"><span data-stu-id="a8590-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="a8590-116">Hvis du vil endre tilknytningen, velger du flere prosjekter og legger dem til i **Valgte prosjekter**-rutenettet.</span><span class="sxs-lookup"><span data-stu-id="a8590-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="a8590-117">Hvis flere prosjekter er valgt i dette rutenettet, blir prosjektets prosentfullføring og inntektsestimater beregnet sammen for alle de valgte prosjektene.</span><span class="sxs-lookup"><span data-stu-id="a8590-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="a8590-118">Prosjektkostnad, inntektsprofil, kostnadsmal og periodekode kan angis manuelt.</span><span class="sxs-lookup"><span data-stu-id="a8590-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="a8590-119">Hvis de ikke angis manuelt, blir verdiene som angitt som standard i den første estimatberegningen for prosjektet ved hjelp av reglene som er konfigurert for prosjektkostnad og inntektsprofiler.</span><span class="sxs-lookup"><span data-stu-id="a8590-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>

