---
title: Beregne salg og kostnader for prosjekter når en ressurs som kan reserveres, fyller flere roller i et prosjekt
description: Dette emnet gir informasjon om hvordan prisdimensjoner kan brukes til å støtte prissetting og kostberegning for en ressurs som fyller flere roller i et prosjekt.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081672"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="20846-103">Beregne salg og kostnader for prosjekter når en ressurs som kan reserveres, fyller flere roller i et prosjekt</span><span class="sxs-lookup"><span data-stu-id="20846-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="20846-104">Prosjektrelaterte selskaper har ofte behov for at én ressurs utfører flere roller i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="20846-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="20846-105">Hver av disse rollene kan være priset og kalkulert på forskjellige måter, noe som betyr at den samme ressursens tid på prosjektet kan få et annet økonomisk estimat, avhengig av fakturerings- og kostnadssatser for hver av rollene.</span><span class="sxs-lookup"><span data-stu-id="20846-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="20846-106">Med Project Service Automation kan du konfigurere verdiene i teammedlemsoppføringen for den navngitte ressursen og tillate forskjellige overstyringer for hver av oppgavene som teammedlemmet er tilordnet til.</span><span class="sxs-lookup"><span data-stu-id="20846-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="20846-107">Eksemplet nedenfor forklarer hvordan den enkle overstyringen av denne verdien tillater at en ressurs har flere roller i et prosjekt med forskjellige kostnads- og faktureringssatser.</span><span class="sxs-lookup"><span data-stu-id="20846-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="20846-108">Opprett oppgaver</span><span class="sxs-lookup"><span data-stu-id="20846-108">Create tasks</span></span>
<span data-ttu-id="20846-109">Opprett to prosjektoppgaver på 40 timer hver, oppgave A og oppgave B. Velg oppgave A som forgjenger for oppgave B.</span><span class="sxs-lookup"><span data-stu-id="20846-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="20846-110">Konfigurere rolle og organisasjonsenhet for et generelt prosjektteammedlem</span><span class="sxs-lookup"><span data-stu-id="20846-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="20846-111">På siden **Planlegg** velger du **Oppgave** -raden for oppgave A.</span><span class="sxs-lookup"><span data-stu-id="20846-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="20846-112">I **Ressurser** -feltet velger du **Opprett** i rullegardinlisten.</span><span class="sxs-lookup"><span data-stu-id="20846-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="20846-113">På siden **Hurtigoppretting av teammedlem** angir du attributtene for det generelle teammedlemmet som kan utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="20846-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="20846-114">Velg riktig rolle og organisasjonsenhet, og velg deretter **Lagre og Lukk**.</span><span class="sxs-lookup"><span data-stu-id="20846-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="20846-115">Et generelt teammedlem blir opprettet og tilordnet til denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="20846-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="20846-116">Gjenta disse trinnene for oppgave B, og kontroller at rollen og organisasjonsenheten for det generelle teammedlemmet som er opprettet for oppgave B, er forskjellig fra oppgave A.</span><span class="sxs-lookup"><span data-stu-id="20846-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="20846-117">Konfigurere rolle og organisasjonsenhet for en prosjektoppgave</span><span class="sxs-lookup"><span data-stu-id="20846-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="20846-118">Når du har opprettet oppgave A, velger du oppgaven, og deretter velger du **Rediger oppgave**.</span><span class="sxs-lookup"><span data-stu-id="20846-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="20846-119">På siden **Oppgavedetaljer** finnre du feltene **Rolle** og **Organisasjonsenhet** , der du må legge til verdiene som kreves for en ressurs som skal utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="20846-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="20846-120">Hvis du utfører disse scenarioene ved hjelp av demonstrasjonsdata for Project Service Automation, velger du **Sjefskonsulent** for rollen og **Fabrikam US** som organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="20846-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="20846-121">Velg oppgave B, og velg deretter **Rediger oppgave**.</span><span class="sxs-lookup"><span data-stu-id="20846-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="20846-122">På siden **Oppgavedetaljer** finnre du feltene **Rolle** og **Organisasjonsenhet** , der du må legge til verdiene som kreves for en ressurs som skal utføre denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="20846-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="20846-123">Kontroller at verdiene i feltene **Rolle** og **Organisasjonsenhet** er forskjellige mellom oppgave B og oppgave A.</span><span class="sxs-lookup"><span data-stu-id="20846-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="20846-124">Hvis du utfører disse scenarioene ved hjelp av demonstrasjonsdata for Project Service Automation, velger du **Nettverkstekniker** for rollen og **Fabrikam US** som organisasjonsenhet.</span><span class="sxs-lookup"><span data-stu-id="20846-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="20846-125">Lagre og lukk siden **Oppgavedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="20846-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="20846-126">Virkemåte for teammedlemmer og estimater</span><span class="sxs-lookup"><span data-stu-id="20846-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="20846-127">På siden **Oppgavedetaljer** , under **Teammedlem** , velger du de to generelle teammedlemmene, og deretter velger du **Generer krav**.</span><span class="sxs-lookup"><span data-stu-id="20846-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="20846-128">Dette genererer ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="20846-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="20846-129">Velg gruppemedlemsraden for **Sjefskonsulent** , og velg deretter **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="20846-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="20846-130">Planleggingstavlen åpnes og bestiller en ressurs til dette kravet.</span><span class="sxs-lookup"><span data-stu-id="20846-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="20846-131">Velg gruppemedlemsraden for **Nettverkstekniker** , og velg deretter **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="20846-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="20846-132">Planleggingstavlen åpnes og bestiller den samme ressursen til dette kravet.</span><span class="sxs-lookup"><span data-stu-id="20846-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="20846-133">Rutenettet Teammedlem</span><span class="sxs-lookup"><span data-stu-id="20846-133">Team Member grid</span></span> 
<span data-ttu-id="20846-134">På rutenettet **Teammedlem** kan du legge merke til at oppføringene til de to generelle teammedlemmene er slettet, og at de har erstattet én ressurs.</span><span class="sxs-lookup"><span data-stu-id="20846-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="20846-135">Det finnes ett sett med verdier for denne ressusen som viser et standardsett med verdier for **Rolle** og **Organisasjonsenhet**.</span><span class="sxs-lookup"><span data-stu-id="20846-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="20846-136">Når du utvider raden for denne teammedlemsoppføringen, kan du se forskjellige tildelinger i teammedlemsoppføringen for begge disse oppgavene.</span><span class="sxs-lookup"><span data-stu-id="20846-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="20846-137">Hver tildelingsrad har oppgavespesifikke verdier for **Rolle** og **Organisasjonsenhet**.</span><span class="sxs-lookup"><span data-stu-id="20846-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="20846-138">Rutenett for estimater</span><span class="sxs-lookup"><span data-stu-id="20846-138">Estimates grid</span></span> 
<span data-ttu-id="20846-139">Når du navigerer til rutenettet **Estimater** , vil du legge merke til at begge tilordningene for den samme ressursen har forskjellig pris.</span><span class="sxs-lookup"><span data-stu-id="20846-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="20846-140">Tilordningen for ressursen i oppgave A er priset ved hjelp av **Rolle** -attributtverdien for **Sjefskonsulent**.</span><span class="sxs-lookup"><span data-stu-id="20846-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="20846-141">Tilordningen for den samme ressursen i oppgave B er priset ved hjelp av **Rolle** -attributtverdien for **Nettverkstekniker**.</span><span class="sxs-lookup"><span data-stu-id="20846-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





