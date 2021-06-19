---
title: Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver
description: Dette emnet gir informasjon om hvordan du bestiller navngitte ressurser for prosjektteam og tilordner dem til oppgaver.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: e0f3957936e699fb2a9f570b9789924c55e12cc2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009358"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="eb893-103">Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver</span><span class="sxs-lookup"><span data-stu-id="eb893-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="eb893-104">Du kan legge til en navngitt ressurs i prosjektteamet ved å reservere den direkte til teamet.</span><span class="sxs-lookup"><span data-stu-id="eb893-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="eb893-105">Det gjør du ved å følge denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="eb893-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="eb893-106">Gå til **Prosjekter** i Project Service Automation, og velg det åpne prosjektet du bestiller for.</span><span class="sxs-lookup"><span data-stu-id="eb893-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="eb893-107">På **Prosjekt**-siden i **Team**-kategorien klikker du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="eb893-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Legge til et teammedlem fra kategorien Team](media/RM-how-to-1.png)

3. <span data-ttu-id="eb893-109">Velg den bestillbare ressursen i dialogboksen **Hurtigoppretting: Prosjektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="eb893-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="eb893-110">**Rolle**-feltet fylles ut med ressursens standardrolle hvis en rolle er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="eb893-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="eb893-111">Du kan endre rollen etter behov.</span><span class="sxs-lookup"><span data-stu-id="eb893-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="eb893-112">Velg fra- og til-datoene som ressursen trenger, og velg fordelingsmetoden for ressursens kapasitet.</span><span class="sxs-lookup"><span data-stu-id="eb893-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="eb893-113">Hvis du vil at teammedlemmet skal være en prosjektgodkjenner, velger du **Ja** i feltet **Prosjektgodkjenner**.</span><span class="sxs-lookup"><span data-stu-id="eb893-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="eb893-114">Dette betyr at teammedlemmet kan godkjenne sendte tids- og utgiftsoppføringer for dette prosjektet.</span><span class="sxs-lookup"><span data-stu-id="eb893-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="eb893-115">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="eb893-115">Click **Save**.</span></span>

![Legge til et team medlem i hurtigopprettingsskjemaet](media/RM-how-to-2.png)


<span data-ttu-id="eb893-117">Nå kan du tilordne den bestilte ressursen til oppgaver i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="eb893-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="eb893-118">På **Prosjekt**-siden klikker du kategorien **Tidsplan** for å tilordne oppgaver til den nye ressursen.</span><span class="sxs-lookup"><span data-stu-id="eb893-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="eb893-119">Ressursvelgeren som startes fra **Ressurser**-feltet i oppgaverutenettet, viser teammedlemmene som du kan velge.</span><span class="sxs-lookup"><span data-stu-id="eb893-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Tilordne et teammedlem til en oppgave i kategorien Tidsplan](media/RM-how-to-3.png)

<span data-ttu-id="eb893-121">I versjon 3 for Project Service automation (PSA) er ressursbestillinger og oppgavetildelinger ikke tett forbundet.</span><span class="sxs-lookup"><span data-stu-id="eb893-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="eb893-122">Dette betyr at når du bruker ressursvelgeren i tidsplanen, kan du tilordne oppgaver til teammedlemmer for flere timer enn ordrene dekker på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="eb893-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="eb893-123">Du kan se forskjellene mellom bestillinger og tildelinger for teammedlemmer i kategorien **Team** eller i kategorien **Ressursavstemming** . Du kan også avstemme forskjellene mellom bestillinger og tildelinger for ressurser på et mer detaljert nivå.</span><span class="sxs-lookup"><span data-stu-id="eb893-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Kategorien Ressursavstemming](media/RM-how-to-4.png)

<span data-ttu-id="eb893-125">Du kan også bruke ressursvelgeren i kategorien **Tidsplan** til å søke etter og velge bestillbare ressurser som ikke allerede er en del av prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="eb893-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="eb893-126">Disse vises i ressursvelgeren som **Andre ressurser**.</span><span class="sxs-lookup"><span data-stu-id="eb893-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Tilordne en ressurs som ikke er medlem av et team, til en oppgave](media/RM-how-to-5.png)

<span data-ttu-id="eb893-128">Når du gjør dette, legges ressursen til i prosjektteamet og tildeles oppgaven, men det genereres ingen bestillinger.</span><span class="sxs-lookup"><span data-stu-id="eb893-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Teammedlemmer med tilordninger og ingen bestillinger](media/RM-how-to-6.png)

<span data-ttu-id="eb893-130">Du kan bruke funksjonen for å utvide bestillingen i kategorien **Avstemming** eller **planleggingstavlen** til å reservere ressursens kapasitet til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="eb893-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Utvide bestillinger for et teammedlem i kategorien Ressursavstemming](media/RM-how-to-7.png)

<span data-ttu-id="eb893-132">Når et teammedlem er bestilt i prosjektet, kan du bruke vedlikehold av bestillinger, eller du kan bruke planleggingstavlen direkte til å behandle bestillingene.</span><span class="sxs-lookup"><span data-stu-id="eb893-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]