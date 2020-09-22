---
title: Konfigurere ressursroller
description: Slik konfigurerer du ressursroller i Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0a180069-17d9-40fd-b4af-9b8d50f373ea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 6a32ec4380e847b897931b6691fa8f9784d0cee7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754080"
---
# <a name="configure-resource-roles-project-service"></a><span data-ttu-id="18915-103">Konfigurere ressursroller (Project Service)</span><span class="sxs-lookup"><span data-stu-id="18915-103">Configure resource roles (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="18915-104">Roller spiller er en viktig del av prosjektplanleggingen når ressurskrav og kostnadene for et prosjekt skal fastsettes.</span><span class="sxs-lookup"><span data-stu-id="18915-104">Roles play an important part in project planning, when determining resource requirements or costs of a project.</span></span> <span data-ttu-id="18915-105">For hver rolle prosjektene krever, må du opprette en ressursrolle og knytte ferdigheter og kompetanser til denne rollen.</span><span class="sxs-lookup"><span data-stu-id="18915-105">For each role your projects require, you need to create a resource role and associate skills and proficiencies to that role.</span></span> <span data-ttu-id="18915-106">Du vil for eksempel opprette en rolle for utvikler, prosjektleder eller spilltester.</span><span class="sxs-lookup"><span data-stu-id="18915-106">For example, you might want to create roles for developer, project manager, or game tester.</span></span> <span data-ttu-id="18915-107">Du må også angi ferdighetene og kunnskapsnivåene som er nødvendig for rollen.</span><span class="sxs-lookup"><span data-stu-id="18915-107">You’ll also set the skills and proficiency levels required for the role.</span></span>  
  
 <span data-ttu-id="18915-108">Konfigurer ressursroller for å sikre effektiv prosjektberegning for organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="18915-108">Configure resource roles to ensure effective project estimation for your organization.</span></span>  <span data-ttu-id="18915-109">Pass også på at du angir faktureringstypen nøyaktig.</span><span class="sxs-lookup"><span data-stu-id="18915-109">Also make sure you accurately set the billing type.</span></span> <span data-ttu-id="18915-110">Et element som er angitt med en ikke-belastbar faktureringstype vises ikke på kontrakten eller tilbudslinjene.</span><span class="sxs-lookup"><span data-stu-id="18915-110">An item set with a non-chargeable billing type doesn’t show up on contract or quote lines.</span></span>  
  
 <span data-ttu-id="18915-111">Når du har konfigurert ressursrollene, kan du definere kostpriser og salgspriser med en prisliste.</span><span class="sxs-lookup"><span data-stu-id="18915-111">Once you’ve set up resource roles, you can set up cost and sales prices with a price list.</span></span>  
  
 <span data-ttu-id="18915-112">For hver rolle du vil legge til, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="18915-112">For each role you want to add, do the following:</span></span>  
  
1.  <span data-ttu-id="18915-113">Gå til **Project Service > Ressursroller**.</span><span class="sxs-lookup"><span data-stu-id="18915-113">Go to **Project Service > Resource Roles**.</span></span>  
  
2.  <span data-ttu-id="18915-114">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="18915-114">Click **New**.</span></span>  
  
3.  <span data-ttu-id="18915-115">I **Generelt**-området angir du et navn for rollen i **Navn**, og fyller deretter ut de andre feltene etter behov.</span><span class="sxs-lookup"><span data-stu-id="18915-115">In the **General** area, enter a name for the role in **Name**, and then fill in the other fields as necessary.</span></span>  
  
4.  <span data-ttu-id="18915-116">Klikk **Lagre** for å opprette oppføringen slik at du kan fortsette å redigere den.</span><span class="sxs-lookup"><span data-stu-id="18915-116">Click **Save** to create the record so you can continue editing it.</span></span>  
  
5.  <span data-ttu-id="18915-117">Hvis du vil legge til en ny ferdighet, klikker du **+** i **Ferdigheter**-området.</span><span class="sxs-lookup"><span data-stu-id="18915-117">In the **Skills** area, click **+** to add a skill.</span></span>  
  
6.  <span data-ttu-id="18915-118">I ruten **Rollekompetansekrav** klikker du i **Ferdighet**-feltet, og klikker **Søk**-knappen, og velger deretter en ferdighet.</span><span class="sxs-lookup"><span data-stu-id="18915-118">In the **Role competency requirement** pane, click in the **Skill** field, click the **Search** button, and then select a skill.</span></span>  
  
7.  <span data-ttu-id="18915-119">Velg et kompetansenivå for ferdigheten, og klikk deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="18915-119">Select a proficiency for that skill, and then click **Save**.</span></span>  
  
8.  <span data-ttu-id="18915-120">Fortsett å legge til ferdigheter etter behov.</span><span class="sxs-lookup"><span data-stu-id="18915-120">Continue adding skills as necessary.</span></span> <span data-ttu-id="18915-121">Når du er ferdig, klikker du **Lagre** nederst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="18915-121">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
9. <span data-ttu-id="18915-122">Klikk **Aktiver** for å gjøre denne ressursrollen tilgjengelig for bruk i prosjekter.</span><span class="sxs-lookup"><span data-stu-id="18915-122">To make this resource role available for projects to use, click **Activate**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="18915-123">Se også</span><span class="sxs-lookup"><span data-stu-id="18915-123">See Also</span></span>  
 [<span data-ttu-id="18915-124">Definere ressurser</span><span class="sxs-lookup"><span data-stu-id="18915-124">Set up resources</span></span>](../project-service/set-up-resources.md)
