---
title: Vise belastbar utnyttelse for ressurser
description: Dette emnet gir informasjon om ressursutnyttelsesvisningen.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 6daa6cfa1c6a237d8a1685123f7c1a6926418bfe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081642"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="ea145-103">Vise belastbar utnyttelse for ressurser</span><span class="sxs-lookup"><span data-stu-id="ea145-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="ea145-104">I **Utnyttelse-visningen** på siden **Ressursutnyttelse i Project Service** vises den belastbare utnyttelsen for hver bestillbare ressurs.</span><span class="sxs-lookup"><span data-stu-id="ea145-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="ea145-105">Siden visningen er basert på planleggingstavlen, finner du mange av de samme funksjonene.</span><span class="sxs-lookup"><span data-stu-id="ea145-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Skjermbilde av visningen Utnyttelse](media/FAQ-utilization-1.png)
 

<span data-ttu-id="ea145-107">Beregningen av belastbar utnyttelse fungerer som følger:</span><span class="sxs-lookup"><span data-stu-id="ea145-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="ea145-108">Belastbar utnyttelse = (belastbare faktiske timer) / (ressurskapasitet).</span><span class="sxs-lookup"><span data-stu-id="ea145-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="ea145-109">Cellene representerer beregnet belastbar utnyttelse for den valgte perioden (dager uker eller måneder).</span><span class="sxs-lookup"><span data-stu-id="ea145-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="ea145-110">Fargene i hver celle viser belastbar utnyttelse for en ressurs sammenlignet med belastbar målutnyttelse.</span><span class="sxs-lookup"><span data-stu-id="ea145-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="ea145-111">Du kan angi målutnyttelse på ressursens standardrolle eller på den individuelle ressursen selv.</span><span class="sxs-lookup"><span data-stu-id="ea145-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="ea145-112">Beregningen ser på den individuelle for målet først, og deretter på ressursens standardrolle.</span><span class="sxs-lookup"><span data-stu-id="ea145-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="ea145-113">Angi mål for en ressurs</span><span class="sxs-lookup"><span data-stu-id="ea145-113">Set target on a resource</span></span>

1. <span data-ttu-id="ea145-114">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="ea145-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ea145-115">Velg en ressurs for å åpne oppføringen.</span><span class="sxs-lookup"><span data-stu-id="ea145-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="ea145-116">I kategorien **Project Service** kan du angi ressursens målutnyttelse.</span><span class="sxs-lookup"><span data-stu-id="ea145-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Skjermbilde av kategorien Project Service for å angi målutnyttelse](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="ea145-118">Angi målutnyttelse for en rolle</span><span class="sxs-lookup"><span data-stu-id="ea145-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="ea145-119">Gå til **Ressurser** \> **Ressursroller**.</span><span class="sxs-lookup"><span data-stu-id="ea145-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="ea145-120">Velg en rolle, og åpne oppføringen.</span><span class="sxs-lookup"><span data-stu-id="ea145-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="ea145-121">Angi målutnyttelsen for rollen.</span><span class="sxs-lookup"><span data-stu-id="ea145-121">Set the target utilization for the role.</span></span>

> ![Skjermbilde av bruk av ressursroller for å angi målutnyttelse](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="ea145-123">Beregne belastbar utnyttelse for en ressurs</span><span class="sxs-lookup"><span data-stu-id="ea145-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="ea145-124">Du må oppfylle noen forhåmndskrav for å beregne belastbar utnyttelse for en ressurs.</span><span class="sxs-lookup"><span data-stu-id="ea145-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="ea145-125">Angi standardrolle for individuell ressurs</span><span class="sxs-lookup"><span data-stu-id="ea145-125">Set default role for individual resource</span></span>

<span data-ttu-id="ea145-126">Du må angi målutnyttelse først på enten den individuelle ressursen eller på ressursroller.</span><span class="sxs-lookup"><span data-stu-id="ea145-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="ea145-127">Hvis du bruker ressursroller for mål, må hver enkelt ressurs ha en standardrolle.</span><span class="sxs-lookup"><span data-stu-id="ea145-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="ea145-128">Du angir dette ved å gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="ea145-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ea145-129">Velg en ressurs, åpne oppføringen, og velg deretter kategorien **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="ea145-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="ea145-130">I rutenettet **Ressursrolle** kontrollerer du at det finnes én rolle for ressursen, og at **Er standard** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ea145-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="ea145-131">Endre faktureringstype for ressursrolle</span><span class="sxs-lookup"><span data-stu-id="ea145-131">Change billing type for resource role</span></span>

<span data-ttu-id="ea145-132">Ressursrollene må angis slik at de har faktureringstypen **Belastbar**.</span><span class="sxs-lookup"><span data-stu-id="ea145-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="ea145-133">Gå til **Ressurser** \> **Ressursroller**.</span><span class="sxs-lookup"><span data-stu-id="ea145-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="ea145-134">Åpne oppføringen du vil oppdatere, og angi deretter faktureringstypen standard til **Belastbar**.</span><span class="sxs-lookup"><span data-stu-id="ea145-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="ea145-135">Angi arbeidstimer for ressursrolle</span><span class="sxs-lookup"><span data-stu-id="ea145-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="ea145-136">Ressursen må ha arbeidstimer for beregning av kapasitet.</span><span class="sxs-lookup"><span data-stu-id="ea145-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="ea145-137">Gå til **Ressurser** \> **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="ea145-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="ea145-138">Velg en ressurs for å åpne oppføringen, og velg deretter **Vis arbeidstimer**.</span><span class="sxs-lookup"><span data-stu-id="ea145-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="ea145-139">Du kan masseoppdatere listen over ressurser ved å bruke en **mal for arbeidstimer** i **ressurslistevisningen**.</span><span class="sxs-lookup"><span data-stu-id="ea145-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="ea145-140">Feilsøke belastbare faktiske timer</span><span class="sxs-lookup"><span data-stu-id="ea145-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="ea145-141">De belastbare faktiske timene hentes fra enheten **Faktiske verdier**.</span><span class="sxs-lookup"><span data-stu-id="ea145-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="ea145-142">Faktiske verdier med faktureringstypen **Belastbar** er med i beregningen, og derfor må du ha prosjekter der de faktiske verdiene er belastbare.</span><span class="sxs-lookup"><span data-stu-id="ea145-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="ea145-143">Hvis du ikke ser belastbar utnyttelse, er det noen ting du kan kontrollere:</span><span class="sxs-lookup"><span data-stu-id="ea145-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="ea145-144">Ressursen har arbeidstimer definert for kapasitet.</span><span class="sxs-lookup"><span data-stu-id="ea145-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="ea145-145">Ressursen har enten et individuelt definert utnyttelsesmål, eller har en standardrolle tilordnet til den.</span><span class="sxs-lookup"><span data-stu-id="ea145-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="ea145-146">Rollen har et utnyttelsesmål definert for den.</span><span class="sxs-lookup"><span data-stu-id="ea145-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="ea145-147">Faktiske verdier har faktureringstypen **Belastbar** for perioden du forventer en utnyttelsesberegning for.</span><span class="sxs-lookup"><span data-stu-id="ea145-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="ea145-148">Sjekk følgende hvis du ser faktiske verdier med andre faktureringstyper enn belastbar:</span><span class="sxs-lookup"><span data-stu-id="ea145-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="ea145-149">Rollen som brukes på de faktiske verdiene, har en annen standard faktureringstype enn belastbar.</span><span class="sxs-lookup"><span data-stu-id="ea145-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="ea145-150">Rollen på prosjektkontraktlinjen som støtter prosjektet, er satt til ikke-belastbar.</span><span class="sxs-lookup"><span data-stu-id="ea145-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="ea145-151">Prosjektet har ingen tilknyttet kontraktlinje.</span><span class="sxs-lookup"><span data-stu-id="ea145-151">The project does not have an associated contract line.</span></span>

