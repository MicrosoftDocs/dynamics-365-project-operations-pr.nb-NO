---
title: Opprettholde teammedlemmer
description: Dette emnet gir informasjon om bestilling av navngitte ressurser for prosjektteam og tilordne dem til oppgaver.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 60b6788d881518502d314e9ee5daf6bbc0ae8764
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286845"
---
# <a name="maintain-team-members"></a><span data-ttu-id="d14d7-103">Opprettholde teammedlemmer</span><span class="sxs-lookup"><span data-stu-id="d14d7-103">Maintain team members</span></span>

<span data-ttu-id="d14d7-104">_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_</span><span class="sxs-lookup"><span data-stu-id="d14d7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d14d7-105">Du kan legge til en navngitt ressurs i prosjektteamet ved å reservere den direkte til teamet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="d14d7-106">Gå til **Prosjekter** i Dynamics 365 Project Operations, og velg det åpne prosjektet du bestiller for.</span><span class="sxs-lookup"><span data-stu-id="d14d7-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="d14d7-107">På **Prosjekt**-siden i **Team**-kategorien velger du **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d14d7-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="d14d7-108">Velg den bestillbare ressursen i dialogboksen **Hurtigoppretting: Prosjektteammedlem**.</span><span class="sxs-lookup"><span data-stu-id="d14d7-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="d14d7-109">**Rolle**-feltet fylles ut med ressursens standardrolle hvis en rolle er tilordnet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="d14d7-110">Du kan endre rollen.</span><span class="sxs-lookup"><span data-stu-id="d14d7-110">You can change the role.</span></span> 
4. <span data-ttu-id="d14d7-111">Velg fra- og til-datoene som ressursen trenger, og velg fordelingsmetoden for ressursens kapasitet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="d14d7-112">I feltet **Prosjektgodkjenner** velger du **Ja** hvis du vil at teammedlemmet skal være prosjektgodkjenner.</span><span class="sxs-lookup"><span data-stu-id="d14d7-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="d14d7-113">Teammedlemmet kan godkjenne sendte tids- og utgiftsoppføringer for dette prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="d14d7-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d14d7-114">Select **Save**.</span></span>

<span data-ttu-id="d14d7-115">Nå kan du tilordne den bestilte ressursen til oppgaver i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="d14d7-116">På **Prosjekt**-siden, i kategorien **Tidsplan**, tilordner du oppgaver til den nye ressursen.</span><span class="sxs-lookup"><span data-stu-id="d14d7-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="d14d7-117">Ressursvelgeren som startes fra **Ressurser**-feltet i oppgaverutenettet, viser teammedlemmene som du kan velge.</span><span class="sxs-lookup"><span data-stu-id="d14d7-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="d14d7-118">I Project Operations er ikke ressursbestillinger og oppgavetilordninger tett koblet sammen.</span><span class="sxs-lookup"><span data-stu-id="d14d7-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="d14d7-119">Når du bruker ressursvelgeren i tidsplanen, kan du tilordne oppgaver til teammedlemmer for flere timer enn ordrene dekker på prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="d14d7-120">Forskjellene mellom bestillinger og tildelinger for teammedlemmer vises i kategoriene **Team** og **Ressursavstemming**.</span><span class="sxs-lookup"><span data-stu-id="d14d7-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="d14d7-121">Du kan også avstemme forskjellene mellom bestillinger og tildelinger for ressurser på et mer detaljert nivå.</span><span class="sxs-lookup"><span data-stu-id="d14d7-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="d14d7-122">Bruk ressursvelgeren i kategorien **Tidsplan** til å søke etter og velge bestillbare ressurser som ikke allerede er en del av prosjektteamet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="d14d7-123">Disse ressursene vises i ressursvelgeren som **Andre ressurser**.</span><span class="sxs-lookup"><span data-stu-id="d14d7-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="d14d7-124">Når du tar et valg, legges ressursen til i prosjektteamet og tildeles oppgaven, men det genereres ingen bestillinger.</span><span class="sxs-lookup"><span data-stu-id="d14d7-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="d14d7-125">Du kan bruke funksjonen for å utvide bestillingen i kategorien **Avstemming** eller **planleggingstavlen** til å reservere ressursens kapasitet til prosjektet.</span><span class="sxs-lookup"><span data-stu-id="d14d7-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="d14d7-126">Når et teammedlem er bestilt i prosjektet, kan du bruke **Vedlikehold bestillinger**, eller du kan bruke **planleggingstavlen** direkte til å behandle bestillingene.</span><span class="sxs-lookup"><span data-stu-id="d14d7-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]