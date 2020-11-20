---
title: Prosjektinnstillinger
description: Denne emnet gir informasjon om innstillinger for prosjektstyring.
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123120"
---
# <a name="project-settings"></a><span data-ttu-id="fce12-103">Prosjektinnstillinger</span><span class="sxs-lookup"><span data-stu-id="fce12-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fce12-104">Bruk følgende innstillinger for å få tilgang til funksjonene for prosjektplanlegging.</span><span class="sxs-lookup"><span data-stu-id="fce12-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="fce12-105">Arbeidsmal</span><span class="sxs-lookup"><span data-stu-id="fce12-105">Work template</span></span>

<span data-ttu-id="fce12-106">Hvis du vil opprette en prosjektplan, må du opprette en prosjektkalendermal som definerer antallet arbeidstimer for hver dag i tidsplanen og eventuelle tidspunkt selskapet holder stengt.</span><span class="sxs-lookup"><span data-stu-id="fce12-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="fce12-107">Hvis du vil opprette en prosjektkalendermal, kan du knytte en arbeidsmal til **Kalendermal**-feltet for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="fce12-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="fce12-108">Følg denne fremgangsmåten for å opprette en arbeidsmal.</span><span class="sxs-lookup"><span data-stu-id="fce12-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="fce12-109">I PSA, den venstre navigasjonsruten, klikker du **Ressurser**.</span><span class="sxs-lookup"><span data-stu-id="fce12-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="fce12-110">På **Ressurser**-listesiden åpner du en brukeroppføring og velger deretter **Vis arbeidstimer**.</span><span class="sxs-lookup"><span data-stu-id="fce12-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fce12-111">Sørg for at du tillater popup-vinduer på nettlesersiden.</span><span class="sxs-lookup"><span data-stu-id="fce12-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="fce12-112">På denne måten kan du se arbeidstimene som er angitt for ressursen.</span><span class="sxs-lookup"><span data-stu-id="fce12-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="fce12-113">I kategorien **Måndsvisning** klikker du **Konfigurer**.</span><span class="sxs-lookup"><span data-stu-id="fce12-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="fce12-114">En liste med tre alternativer vises:</span><span class="sxs-lookup"><span data-stu-id="fce12-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="fce12-115">Ny ukeplan</span><span class="sxs-lookup"><span data-stu-id="fce12-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="fce12-116">Arbeidstidsplan for én dag</span><span class="sxs-lookup"><span data-stu-id="fce12-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="fce12-117">Fritid</span><span class="sxs-lookup"><span data-stu-id="fce12-117">Time Off</span></span>

> ![Konfigurere salternativer](media/project-13.png)

4. <span data-ttu-id="fce12-119">Velg **Ny ukeplan**, og angi deretter alternativene for denne ressursplanen.</span><span class="sxs-lookup"><span data-stu-id="fce12-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="fce12-120">Du kan angi en regelmessig ukeplan, daglige timeparametere, selskapet holder stengt, og så videre.</span><span class="sxs-lookup"><span data-stu-id="fce12-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="fce12-121">Angi datointervallet, velg **Lagre**, og klikk deretter **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="fce12-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="fce12-122">Gå tilbake til **Ressurser**-listesiden, og velg ressursen du angir arbeidstimer for.</span><span class="sxs-lookup"><span data-stu-id="fce12-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="fce12-123">Velg **Angi kalender som** for å angi arbeidsmalen.</span><span class="sxs-lookup"><span data-stu-id="fce12-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="fce12-124">Skriv inn et navn på arbeidsmalen i dialogboksen **Arbeidsmal**, og velg deretter **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="fce12-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="fce12-125">Du kan nå knytte arbeidsmalen til en prosjektkKalendermal.</span><span class="sxs-lookup"><span data-stu-id="fce12-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="fce12-126">Ressursroller</span><span class="sxs-lookup"><span data-stu-id="fce12-126">Resource roles</span></span>

<span data-ttu-id="fce12-127">Begrepet *ressursrolle* viser til en rekke ferdigheter, kompetanser og sertifiseringer som en person må ha for å utføre et bestemt sett med oppgaver i et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="fce12-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="fce12-128">Med PSA kan du angi kostnader for og fakturere tiden til en ressurs basert på rollen som ressursen er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="fce12-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="fce12-129">Alle organisasjoner må konfigurere disse rollene ved å bruke det venstre navigasjonsfeltet på **Project Service**-menyen.</span><span class="sxs-lookup"><span data-stu-id="fce12-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="fce12-130">Alle organisasjoner må konfigurere disse rollene på siden **Aktive ressurskategorier**.</span><span class="sxs-lookup"><span data-stu-id="fce12-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="fce12-131">Hvis du vil åpne denne siden, velger du **Ressursroller** i den venstre navigasjonsruten.</span><span class="sxs-lookup"><span data-stu-id="fce12-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="fce12-132">Prislister</span><span class="sxs-lookup"><span data-stu-id="fce12-132">Price lists</span></span>

<span data-ttu-id="fce12-133">Med prislister kan du angi kostpriser og salgspriser for ressursroller, utgiftskategorier, produkter og andre elementer i en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="fce12-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="fce12-134">Før du angir økonomiske estimater for arbeid som må leveres for et prosjekt, bør du opprette en støttekostnads- og salgsprisliste.</span><span class="sxs-lookup"><span data-stu-id="fce12-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="fce12-135">I Parametere-delen bør du også konfigurere en standard kostnads- og salgsprisliste som gjelder for alle prosjekter som opprettes i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="fce12-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="fce12-136">På siden **Aktive prosjektparametere** sørger du for at du angir en standard kostnads- og salgsprisliste.</span><span class="sxs-lookup"><span data-stu-id="fce12-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
