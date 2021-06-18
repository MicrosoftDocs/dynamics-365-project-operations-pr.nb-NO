---
title: Opprette en prosjektmal
description: Slik oppretter du en prosjektmal i Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 148bf1d42b640ff7b58b13bb0c30c7e583d803c8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997253"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="3f581-103">Opprette en prosjektmal (Project Service)</span><span class="sxs-lookup"><span data-stu-id="3f581-103">Create a project template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="3f581-104">Prosjektmaler spare tid hvis firmaet jevnlig byr på lignende typer prosjekter.</span><span class="sxs-lookup"><span data-stu-id="3f581-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="3f581-105">De utgjør et standardsett med roller og estimert timer for en type prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3f581-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="3f581-106">Ledere for forretningsforbindelser og prosjektledere kan opprette prosjekter basert på en prosjektmal, eller de kan kopiere malen og lage en egen mal.</span><span class="sxs-lookup"><span data-stu-id="3f581-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="3f581-107">Komponenter i prosjektmal</span><span class="sxs-lookup"><span data-stu-id="3f581-107">Components of project template</span></span>
 <span data-ttu-id="3f581-108">En prosjektmal består av tre komponenter:</span><span class="sxs-lookup"><span data-stu-id="3f581-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="3f581-109">**Arbeidsnedbrytningsstruktur**: En arbeidsnedbrytningsstruktur i en prosjektmal har det samme settet med elementer som i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f581-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="3f581-110">Du kan opprette et oppgavehierarki, tilordne roller til oppgaven, definere attributter for tidsplan, angi avhengigheter og vise alle dataene i Gantt-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="3f581-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="3f581-111">Arbeidsnedbrytningsstrukturen i prosjektmaler støtter også aktivitetsmodi for hver aktivitet.</span><span class="sxs-lookup"><span data-stu-id="3f581-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="3f581-112">Det er ingen forskjell mellom en prosjektmal og et prosjekt når du oppretter arbeidsplanen.</span><span class="sxs-lookup"><span data-stu-id="3f581-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="3f581-113">**Prosjektestimater**:Prosjektestimater i maler fungerer på samme måte som de gjør i prosjekter, bortsett fra at prislister for tilbakestilling av kostnadene og salgsprisene alltid er standardkostnader og salgsprislister definert i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parameterne.</span><span class="sxs-lookup"><span data-stu-id="3f581-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="3f581-114">Resten av funksjonaliteten er den samme som i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3f581-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="3f581-115">**Sette sammen prosjektteam**: Når du setter sammen et prosjektteam for en prosjektmal, kan du bestille en navngitt ressurs i en mal.</span><span class="sxs-lookup"><span data-stu-id="3f581-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="3f581-116">Du kan bruke **Genererer prosjektteam** i arbeidsnedbrytningsstrukturen til å generere et sett med generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="3f581-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="3f581-117">Du kan også angi nødvendige ferdigheter og kompetanser for generelle ressurser.</span><span class="sxs-lookup"><span data-stu-id="3f581-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="3f581-118">Du kan ikke erstatte en generell ressurs med en bestillbar ressurs i prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="3f581-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="3f581-119">Opprette et prosjekt fra en mal</span><span class="sxs-lookup"><span data-stu-id="3f581-119">Create a project from a template</span></span>  
 <span data-ttu-id="3f581-120">Du kan opprette et prosjekt fra en mal på disse måtene:</span><span class="sxs-lookup"><span data-stu-id="3f581-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="3f581-121">Når du oppretter et prosjekt fra en forespørsel, kan du velge en prosjektmal i hurtigopprettingsskjemaet for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3f581-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="3f581-122">Når du oppretter et prosjekt ved å klikke **Nytt prosjekt**, vises prosjektskjemaet før du lagrer posten.</span><span class="sxs-lookup"><span data-stu-id="3f581-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="3f581-123">Herfra kan du klikke **Velg en mal**-feltet for å velge fra listen over forhåndsdefinerte prosjektmaler i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="3f581-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="3f581-124">Klikk **Opprett prosjekt fra en mal** på **Prosjektmal**-siden for å opprette et prosjekt fra malen.</span><span class="sxs-lookup"><span data-stu-id="3f581-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="3f581-125">Kopiere komponenter i en mal til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="3f581-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="3f581-126">Når du kopierer komponenter i en mal til et prosjekt, er det et par ting du bør vite om.</span><span class="sxs-lookup"><span data-stu-id="3f581-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="3f581-127">**Kopiere en arbeidsnedbrytningsstruktur**: Når du kopierer arbeidsnedbrytningsstrukturen fra en prosjektmal, hvis prosjektet har en annen prosjektkalender enn malen, brukes arbeidstimene fra prosjektkalenderen på tidsplanen for oppgavene.</span><span class="sxs-lookup"><span data-stu-id="3f581-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="3f581-128">Dette justerer tidsplanen til reserveprosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="3f581-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="3f581-129">På samme måte tar den første oppgaven i arbeidsnedbrytningsstrukturen prosjektets startdato, slik at resten av tidsplanen for oppgavehierarkiet oppdateres basert på varigheten og avhengighetene som er angitt i malens arbeidsnedbrytningsstruktur.</span><span class="sxs-lookup"><span data-stu-id="3f581-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="3f581-130">**Kopiere prosjektestimater**: Når du kopierer på tvers av prosjektestimatlinjer, oppdateres prislister basert på eierenheten i prosjektet for kostprislisten og kunden for salgsprislisten.</span><span class="sxs-lookup"><span data-stu-id="3f581-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="3f581-131">Enhetskosten og salgsprisene bestemmes fra disse prislistene på prosjekter som er knyttet til en salgsenhet.</span><span class="sxs-lookup"><span data-stu-id="3f581-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="3f581-132">**Kopiere et prosjektteam**: Når du kopierer prosjektteamet fra malen til et prosjekt, kopieres de generelle ressursene på tvers, sammen med ferdighetene og kompetansene som er definert i malen.</span><span class="sxs-lookup"><span data-stu-id="3f581-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="3f581-133">Tildeling av generelle ressurser blir også vedlikeholdt i prosjektmalen.</span><span class="sxs-lookup"><span data-stu-id="3f581-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3f581-134">Se også</span><span class="sxs-lookup"><span data-stu-id="3f581-134">See Also</span></span>  
 [<span data-ttu-id="3f581-135">Prosjektlederhåndbok</span><span class="sxs-lookup"><span data-stu-id="3f581-135">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]