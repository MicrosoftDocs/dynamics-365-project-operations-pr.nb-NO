---
title: Gi arbeidsestimater for et prosjekt under salgsprosessen
description: Slik gir du arbeidsestimater for et prosjekt under salgsprosessen i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754173"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="462aa-103">Gi arbeidsestimater for et prosjekt under salgsprosessen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="462aa-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="462aa-104">Under salgsprosessen, kan du arbeide ut salgsestimater fra grunnen med tilbudslinjene.</span><span class="sxs-lookup"><span data-stu-id="462aa-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]<span data-ttu-id="462aa-105">-funksjoner i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] gir en mer vitenskapelig og deterministisk måte å komme opp med salgsestimater på ved å bryte ned arbeidselementer og knytte sammen relevante attributter, som bidrar til estimater for prosjektet i arbeidsnedbrytningsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="462aa-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="462aa-106">Når du vinner salget, kan du bruke den tilknyttede arbeidsnedbrytningsstrukturen i prosjektplanen og forbedre den etter behov for vellykket fullføring av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="462aa-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="462aa-107">Koble et prosjekt til en tilbudslinje</span><span class="sxs-lookup"><span data-stu-id="462aa-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="462aa-108">Når du oppretter en prosjektbasert tilbudslinje, kan du opprette et nytt prosjekt fra tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="462aa-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="462aa-109">Deretter kan du bruke prosjektmaler som er forhåndskonfigurerte standard prosjektplaner og økonomiske estimater som er felles for organisasjonen, eller en kopi av en prosjektplan og estimater fra et tidligere prosjekt.</span><span class="sxs-lookup"><span data-stu-id="462aa-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="462aa-110">Når du oppretter et prosjekt, velge en prosjektmal gir grunnlag for å finjustere planen, estimater og rollekravene.</span><span class="sxs-lookup"><span data-stu-id="462aa-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="462aa-111">Ved å opprette prosjektet fra tilbudet er prosjektet automatisk knyttet til tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="462aa-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="462aa-112">Komponenter for prosjektestimat</span><span class="sxs-lookup"><span data-stu-id="462aa-112">Project estimate components</span></span>  
 <span data-ttu-id="462aa-113">Arbeidsnedbrytningsstrukturen i et prosjekt er en måte å dele opp arbeidet i aktiviteter, opprettholde et hierarki av aktiviteter og tilordne et overslag over innsats som kreves for å fullføre hver aktivitet.</span><span class="sxs-lookup"><span data-stu-id="462aa-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="462aa-114">Du kan også knytte roller til en aktivitet for å angi et estimat av typen ressurs som kreves for å fullføre en aktivitet og en tidsplan.</span><span class="sxs-lookup"><span data-stu-id="462aa-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="462aa-115">Arbeidsnedbrytningsstrukturen hjelper deg med å bestemme arbeidsinnsats- og tidsplanestimater.</span><span class="sxs-lookup"><span data-stu-id="462aa-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="462aa-116">Som standard bruker prosjektet standard prislister du definerte tidligere.</span><span class="sxs-lookup"><span data-stu-id="462aa-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="462aa-117">Kostnadene og salgsprisene som er definert i prislistene, hjelper med å bestemme økonomiske estimater for prosjektets arbeidsnedbryting.</span><span class="sxs-lookup"><span data-stu-id="462aa-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="462aa-118">Hvis prosjektet er knyttet til et tilbud, og tilbudet har en annen prisliste enn standard, brukes tilbudets prisliste for økonomiske beregninger.</span><span class="sxs-lookup"><span data-stu-id="462aa-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="462aa-119">Importere estimater fra et prosjekt til et tilbud</span><span class="sxs-lookup"><span data-stu-id="462aa-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="462aa-120">Når du har prosjektestimater i prosjektet, kan du importere disse estimatene til tilbudslinjen:</span><span class="sxs-lookup"><span data-stu-id="462aa-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="462aa-121">I **Tilbudslinjedetaljer** klikker du **Importer fra estimater**.</span><span class="sxs-lookup"><span data-stu-id="462aa-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="462aa-122">Velg om du vil importere prosjektestimater summert etter nodenivået transaksjonstype, rolle eller arbeidsnedbrytingsstruktur.</span><span class="sxs-lookup"><span data-stu-id="462aa-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="462aa-123">Se også</span><span class="sxs-lookup"><span data-stu-id="462aa-123">See Also</span></span>  
 [<span data-ttu-id="462aa-124">Prosjektlederhåndbok</span><span class="sxs-lookup"><span data-stu-id="462aa-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
