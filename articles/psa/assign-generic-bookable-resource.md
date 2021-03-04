---
title: Tilordne generelt bestillbare ressurser til en oppgave og et prosjektteam
description: Dette emnet gir informasjon om bestilling av generelle ressurser for aktiviteter og prosjektteam.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: 684167f0a68872ef871fbaa06c5161e78045c9a5
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145415"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="2e981-103">Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav</span><span class="sxs-lookup"><span data-stu-id="2e981-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="2e981-104">I tillegg til å bestille og tilordne navngitte eller faktiske ressurser i prosjektet kan du tilordne generelle ressurser til prosjektoppgaver.</span><span class="sxs-lookup"><span data-stu-id="2e981-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="2e981-105">Disse ressursene kan fungere som plassholdere for navngitte ressurser til du er klar til å bemanne prosjektet med navngitte ressurser.</span><span class="sxs-lookup"><span data-stu-id="2e981-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="2e981-106">I Project Service Automation (PSA) åpner du **Prosjekt**-siden, og i kategorien **Tidsplan** angir du posisjonsnavnet til den generelle ressursen i **Ressurs**-cellen i tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="2e981-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="2e981-107">Du kan også klikke **Ressurs**-ikonet i cellen for å åpne ressursvelgeren og deretter skrive inn navnet på den generelle ressursen du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="2e981-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Opprette og tilordne et generelt teammedlem](media/RM-how-to-9.png)

<span data-ttu-id="2e981-109">Dette åpner panelet **Hurtigoppretting: Prosjektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="2e981-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="2e981-110">Angi rollen og organisasjonsenheten for det generelle ressursteammedlemmet, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="2e981-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Hurtigoppretting av generelt teammedlem](media/RM-how-to-10.png)

3. <span data-ttu-id="2e981-112">Når du har opprettet det nye medlemmet i det generelle ressursteamet, blir det tilordnet til oppgaven.</span><span class="sxs-lookup"><span data-stu-id="2e981-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="2e981-113">Du kan fortsette å tilordne den generelle ressursen til andre oppgaver i oppgavetidsplanen.</span><span class="sxs-lookup"><span data-stu-id="2e981-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Tilordne eksisterende generelle teammedlemmer til oppgaver](media/RM-how-to-11.png)

4. <span data-ttu-id="2e981-115">Når du har tilordnet den generelle ressursen, kan du generere et ressurskrav og fullføre det ved å bestille eller sende en ressursforespørsel til en ressursleder direkte.</span><span class="sxs-lookup"><span data-stu-id="2e981-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generere et krav for et generelt teammedlem](media/RM-how-to-12.png)

<span data-ttu-id="2e981-117">I rutenettet for teammedlemmer, i tillegg til å kunne bruke ressursvelgeren som nevnt ovenfor, kan du legge til generelle ressurser direkte.</span><span class="sxs-lookup"><span data-stu-id="2e981-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="2e981-118">Ressursene legges til med et ressurskrav som er basert på start- og sluttdatoene og fordelingsmetoden som er angitt i panelet **Hurtigoppretting: Prosjektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="2e981-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="2e981-119">Du kan se en forskjell hvis du legger til det generelle teammedlemmet direkte og deretter tildeler flere oppgaver til den generelle ressursen enn antallet det er nødvendig å dekke.</span><span class="sxs-lookup"><span data-stu-id="2e981-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="2e981-120">Klikk **Generer krav** for å generere kravet på nytt for å balansere de nødvendige timene mot tildelinger.</span><span class="sxs-lookup"><span data-stu-id="2e981-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="2e981-121">Du kan også klikke **Ressurskrav**-koblingen i rutenettet for teamet for å åpne kravet og legge til kvalifikasjoner, foretrukne ressurser og så videre.</span><span class="sxs-lookup"><span data-stu-id="2e981-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Ressurskrav](media/RM-how-to-13.png)

