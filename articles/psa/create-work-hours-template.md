---
title: Opprette en mal for arbeidstimer
description: Slik oppretter du en mal for arbeidstimer i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 54d7385a2bb161c7dd02d882090790debaef3bdb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148790"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="7e9c1-103">Opprette en mal for arbeidstimer (Project Service)</span><span class="sxs-lookup"><span data-stu-id="7e9c1-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7e9c1-104">Før du kan opprette prosjekttidsplaner, må du sette opp en prosjektkalender som definerer antallet arbeidstimer for hver dag i tidsplanen og eventuelle tidspunkt selskapet holder stengt.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="7e9c1-105">Dette gjør du med en mal for arbeidstimer som inneholder detaljer om arbeidstimer per dag, fridager og andre tidspunkt selskapet holder stengt.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="7e9c1-106">Når du oppretter et prosjekt, kan du knytte en arbeidsmal til prosjektkalenderen for å bruke tidsplanen for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="7e9c1-107">Det er to måter du kan opprette en mal for arbeidstimer på:</span><span class="sxs-lookup"><span data-stu-id="7e9c1-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="7e9c1-108">Opprette en mal for arbeidstimer basert på en kalenderen til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="7e9c1-109">Opprette en ny mal for arbeidstimer.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="7e9c1-110">Slik oppretter du en mal for arbeidstimer basert på en kalenderen til en ressurs</span><span class="sxs-lookup"><span data-stu-id="7e9c1-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="7e9c1-111">Gå til **Project Service > Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="7e9c1-112">Velg ressursen du vil basere arbeidstimene på.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="7e9c1-113">Klikk **Lagre kalender som**, skriv inn et navn for malen for arbeidstimer, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="7e9c1-114">Når du er ferdig med å endre alternativer, klikker du **Lagre og lukk**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="7e9c1-115">Klikk **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="7e9c1-116">Slik oppretter du en ny mal for arbeidstimer</span><span class="sxs-lookup"><span data-stu-id="7e9c1-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="7e9c1-117">Gå til **Project Service > Arbeidstidsmal**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="7e9c1-118">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="7e9c1-119">Angi et navn for malen for arbeidstimer.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="7e9c1-120">Velg en ressurs å basere arbeidstiden på, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="7e9c1-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7e9c1-121">Se også</span><span class="sxs-lookup"><span data-stu-id="7e9c1-121">See Also</span></span>  
 [<span data-ttu-id="7e9c1-122">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="7e9c1-122">Set up resources</span></span>](../psa/set-up-resources.md)
