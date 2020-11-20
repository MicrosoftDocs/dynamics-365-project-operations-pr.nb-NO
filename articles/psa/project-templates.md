---
title: Prosjektmaler
description: Dette emnet gir informasjon om hvordan du bruker prosjektmaler for et raskt prosjektoppsett.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123038"
---
# <a name="project-templates"></a><span data-ttu-id="882ae-103">Prosjektmaler</span><span class="sxs-lookup"><span data-stu-id="882ae-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="882ae-104">En prosjektmal er et forhåndsdefinert rammeverk som hjelper deg med å starte et prosjekt raskt og enkelt.</span><span class="sxs-lookup"><span data-stu-id="882ae-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="882ae-105">Du kan bruke en forhåndsdefinert mal til å opprette et nytt prosjekt med ett klikk.</span><span class="sxs-lookup"><span data-stu-id="882ae-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="882ae-106">Som for prosjekter må du definere forhåndskravene for prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="882ae-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="882ae-107">Du må definere en prosjektkalender for hver prosjektmal, og roller og prislister må være forhåndsdefinert i organisasjonen, slik at komponentene i malen har nyttige data.</span><span class="sxs-lookup"><span data-stu-id="882ae-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="882ae-108">En prosjektmal består av tre komponenter: en tidsplan, prosjektestimater og prosjektteammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="882ae-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="882ae-109">Tidsplan</span><span class="sxs-lookup"><span data-stu-id="882ae-109">Schedule</span></span>

<span data-ttu-id="882ae-110">En tidsplan i en prosjektmal har samme sett elementer som en tidsplan i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="882ae-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="882ae-111">Du kan opprette et oppgavehierarki, tilordne roller til oppgaver, definere attributter for tidsplan og angi avhengigheter.</span><span class="sxs-lookup"><span data-stu-id="882ae-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="882ae-112">En tidsplan i en prosjektmal støtter også oppgavemoduser for hver oppgave.</span><span class="sxs-lookup"><span data-stu-id="882ae-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="882ae-113">Den støtter derfor planleggingsmotoren.</span><span class="sxs-lookup"><span data-stu-id="882ae-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="882ae-114">Du må knytte en prosjektkalender til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="882ae-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="882ae-115">Når du oppretter en arbeidsplan, er det ingen forskjell mellom en prosjektmal og et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="882ae-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="882ae-116">Prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="882ae-116">Project estimates</span></span>

<span data-ttu-id="882ae-117">Prosjektestimater i en prosjektmal fungerer på samme måte som prosjektestimater i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="882ae-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="882ae-118">Kostnads- og salgsprisene trekkes imidlertid fra standard kostnads- og salgsprislistene som er definert i parameterne.</span><span class="sxs-lookup"><span data-stu-id="882ae-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="882ae-119">Opprette et prosjekt fra en mal</span><span class="sxs-lookup"><span data-stu-id="882ae-119">Creating a project from a template</span></span>
 
<span data-ttu-id="882ae-120">Det finnes flere måter å opprette et prosjekt på fra en prosjektmal:</span><span class="sxs-lookup"><span data-stu-id="882ae-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="882ae-121">Når du oppretter et prosjekt fra et tilbud, kan du velge en prosjektmal i dialogboksen **Hurtigoppretting: Prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="882ae-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialogboksen Hurtigoppretting: Prosjekt](media/project-11.png)

- <span data-ttu-id="882ae-123">Når du oppretter et prosjekt ved å velge **Nytt prosjekt**, vises **Prosjekt**-siden før oppføringen lagres.</span><span class="sxs-lookup"><span data-stu-id="882ae-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="882ae-124">I feltet **Velg en mal** velger du en av de forhåndsdefinerte prosjektmalene i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="882ae-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="882ae-125">Bruk **Opprett prosjekt fra mal** på siden **Malenhet**.</span><span class="sxs-lookup"><span data-stu-id="882ae-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="882ae-126">Kopiere komponenter i en mal til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="882ae-126">Copying components of template to project</span></span>

<span data-ttu-id="882ae-127">Når du kopierer komponentene i en prosjektmal til et prosjekt, kan det oppstå noen overstyringer, avhengig av innstillingene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="882ae-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="882ae-128">Kopiere tidsplanen</span><span class="sxs-lookup"><span data-stu-id="882ae-128">Copying the schedule</span></span>

<span data-ttu-id="882ae-129">Når du kopierer tidsplanen fra en prosjektmal, hvis prosjektet har en annen prosjektkalender enn malen, brukes arbeidstimene fra prosjektkalenderen på tidsplanen for oppgavene.</span><span class="sxs-lookup"><span data-stu-id="882ae-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="882ae-130">Dette justerer tidsplanen til reserveprosjektkalenderen.</span><span class="sxs-lookup"><span data-stu-id="882ae-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="882ae-131">På samme måte tar den første oppgaven i tidspnalen prosjektets startdato, og tidsplanen for resten av oppgavehierarkiet oppdateres basert på varigheten og avhengighetene som er angitt i malen.</span><span class="sxs-lookup"><span data-stu-id="882ae-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="882ae-132">Kopiere prosjektestimater</span><span class="sxs-lookup"><span data-stu-id="882ae-132">Copying project estimates</span></span> 

<span data-ttu-id="882ae-133">Når du kopierer på tvers av prosjektestimatlinjer, oppdateres prislistene.</span><span class="sxs-lookup"><span data-stu-id="882ae-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="882ae-134">For kostnadsprislisten er disse oppdateringene basert på den eiende enheten til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="882ae-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="882ae-135">For salgsprislisten er de basert på kunden.</span><span class="sxs-lookup"><span data-stu-id="882ae-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="882ae-136">For prosjekter som er knyttet til en salgsenhet, bestemmes enhetskosten og salgsprisene basert på disse prislistene.</span><span class="sxs-lookup"><span data-stu-id="882ae-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="882ae-137">Kopiere et prosjektteam</span><span class="sxs-lookup"><span data-stu-id="882ae-137">Copying a project team</span></span>

<span data-ttu-id="882ae-138">Når et prosjektteam kopieres fra en prosjektmal til et prosjekt, kopieres de generelle ressursene, sammen med ferdighetene og kompetansene som er definert i malen.</span><span class="sxs-lookup"><span data-stu-id="882ae-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="882ae-139">Tildeling av generelle ressurser blir også vedlikeholdt slik som i prosjektmalen.</span><span class="sxs-lookup"><span data-stu-id="882ae-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="882ae-140">Navngitte ressurser støttes ikke i prosjektmaler.</span><span class="sxs-lookup"><span data-stu-id="882ae-140">Named resources aren't supported in project templates.</span></span>
