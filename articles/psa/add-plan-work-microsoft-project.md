---
title: Bruke tillegget Project Service til å planlegge arbeidet i Microsoft Project | MicrosoftDocs
description: Dette emnet gir informasjon om hvordan du legger til, konfigurerer og bruker Microsoft Project-tillegget for Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081750"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="a5629-103">Bruke tillegget Project Service Automation til å planlegge arbeidet i Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="a5629-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="a5629-104">gjør det enklere for deg å utføre prosjektplanlegging og estimater.</span><span class="sxs-lookup"><span data-stu-id="a5629-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="a5629-105">Du kan definere arbeidet slik at kostnader, arbeid og salgsverdi er tydelig når det endelige forslaget sendes.</span><span class="sxs-lookup"><span data-stu-id="a5629-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="a5629-106">Nå kan du installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og utføre planleggingen i det kjente miljøet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="a5629-107">Bruk de kraftige egenskapene for planlegging og administrasjon av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og oppdater deretter prosjektplanen i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a5629-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="a5629-108">For å kunne bruke SharePoint-dokumentadministrasjon for å lagre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjekter må [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administratoren aktivere dokumentadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="a5629-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="a5629-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er bare kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="a5629-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="a5629-110">Last ned og installer tillegget</span><span class="sxs-lookup"><span data-stu-id="a5629-110">Download and install the add-in</span></span>  
 <span data-ttu-id="a5629-111">Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-påloggingsinformasjonen klar.</span><span class="sxs-lookup"><span data-stu-id="a5629-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="a5629-112">Du trenger denne informasjonen for å koble fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="a5629-113">Fra nedlastingssenteret kan du laste ned tillegget for den støttede versjonen av Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="a5629-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="a5629-114">Klikk nedlastingskoblingen.</span><span class="sxs-lookup"><span data-stu-id="a5629-114">Click the download link.</span></span>  

3.  <span data-ttu-id="a5629-115">Når nedlastingen er fullført, klikker du **Ja** for å installere tillegget.</span><span class="sxs-lookup"><span data-stu-id="a5629-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="a5629-116">Konfigurere tillegget</span><span class="sxs-lookup"><span data-stu-id="a5629-116">Configure the add-in</span></span>  

1. <span data-ttu-id="a5629-117">Åpne [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og klikk kategorien **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="a5629-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="a5629-118">Klikk **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="a5629-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="a5629-119">Skriv inn påloggingsinformasjonen din, og klikk deretter **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="a5629-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="a5629-120">Nå kan du begynne å bruke tillegget.</span><span class="sxs-lookup"><span data-stu-id="a5629-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="a5629-121">Lese fra en mal</span><span class="sxs-lookup"><span data-stu-id="a5629-121">Read from a template</span></span>  
 <span data-ttu-id="a5629-122">Les fra en mal du har opprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopiert til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for å starte prosjektplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="a5629-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a5629-123">[Opprett en prosjektmal (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a5629-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="a5629-124">Fra kategorien **Project Service** klikker du **Lese** > **Prosjektmal for Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a5629-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="a5629-125">Velg en prosjektmal fra listen, og klikk deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="a5629-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="a5629-126">Oppgaver som er overført fra malen til Project, settes som standard som manuelt planlagt.</span><span class="sxs-lookup"><span data-stu-id="a5629-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="a5629-127">Tilordne [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="a5629-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="a5629-128">Åpne et prosjekt, og klikk på **Oppgave** -båndet.</span><span class="sxs-lookup"><span data-stu-id="a5629-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="a5629-129">Klikk på **Gantt-diagram** -menyen, og velg deretter **Ressursliste**.</span><span class="sxs-lookup"><span data-stu-id="a5629-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="a5629-130">I ressurslisten klikker du rullegardinmenyen **Rolle for Project Service-ressurs** og velger en Project Service Automation-rolle.</span><span class="sxs-lookup"><span data-stu-id="a5629-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="a5629-131">Bemanne prosjektet med ressurser</span><span class="sxs-lookup"><span data-stu-id="a5629-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="a5629-132">Merk en rad fra kategorien Project Service, og klikk **Finn ressurser**.</span><span class="sxs-lookup"><span data-stu-id="a5629-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="a5629-133">På **Bestill ressurs** -skjermen merker du ressursen du vil bruke for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a5629-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="a5629-134">Klikk **Bestill** , og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5629-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="a5629-135">Publisere prosjektet</span><span class="sxs-lookup"><span data-stu-id="a5629-135">Publish your project</span></span>  
<span data-ttu-id="a5629-136">Når prosjektplanleggingen er fullført, er det neste trinnet å importere og publisere prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="a5629-137">Prosjektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="a5629-138">Prosessen for prising og teamgenerering brukes.</span><span class="sxs-lookup"><span data-stu-id="a5629-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="a5629-139">Åpne prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å se at teamet, prosjektestimater og arbeidsnedbrytningsstruktur er generert.</span><span class="sxs-lookup"><span data-stu-id="a5629-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="a5629-140">Tabellen nedenfor viser hvor du finner resultatene:</span><span class="sxs-lookup"><span data-stu-id="a5629-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a5629-141">**Gantt-diagram**</span><span class="sxs-lookup"><span data-stu-id="a5629-141">**Gantt Chart**</span></span>   | <span data-ttu-id="a5629-142">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbeidsnedbrytningsstruktur** -skjermen.</span><span class="sxs-lookup"><span data-stu-id="a5629-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a5629-143">**Ressursliste**</span><span class="sxs-lookup"><span data-stu-id="a5629-143">**Resource Sheet**</span></span> |   <span data-ttu-id="a5629-144">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektteammedlemmer** -skjermen.</span><span class="sxs-lookup"><span data-stu-id="a5629-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="a5629-145">**Bruk av bruk**</span><span class="sxs-lookup"><span data-stu-id="a5629-145">**Use Usage**</span></span>    |    <span data-ttu-id="a5629-146">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektestimater** -skjermen.</span><span class="sxs-lookup"><span data-stu-id="a5629-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="a5629-147">**Importere og publisere prosjektet**</span><span class="sxs-lookup"><span data-stu-id="a5629-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="a5629-148">Fra kategorien **Project Service** klikker du **Publiser** > **Nytt Project Service Automation-prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="a5629-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="a5629-149">I dialogboksen **Publiser til et nytt prosjekt i Project Service** skriver du inn **prosjektnavnet** og velger **kunden**.</span><span class="sxs-lookup"><span data-stu-id="a5629-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="a5629-150">Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble planprosjektfilen til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a5629-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="a5629-151">Klikk **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="a5629-151">Click **Publish**.</span></span>  

   <span data-ttu-id="a5629-152">Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="a5629-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="a5629-153">Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="a5629-154">Redigere et prosjekt som er importert</span><span class="sxs-lookup"><span data-stu-id="a5629-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="a5629-155">Hvis du vil gjøre endringer i en prosjektplan som er importert til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to alternativer:</span><span class="sxs-lookup"><span data-stu-id="a5629-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="a5629-156">Åpne hovedfilen og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="a5629-157">Fjern kobling for filen og rediger den direkte i Project Service.</span><span class="sxs-lookup"><span data-stu-id="a5629-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="a5629-158">Som standard er et prosjekt som er lastet opp fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan bare redigeres i Project.</span><span class="sxs-lookup"><span data-stu-id="a5629-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="a5629-159">Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], må koblingen for filen fjernes.</span><span class="sxs-lookup"><span data-stu-id="a5629-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="a5629-160">Redigere i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="a5629-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="a5629-161">Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="a5629-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a5629-162">Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a5629-163">Klikk **Åpne i MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="a5629-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="a5629-164">Dette åpner den koblede hovedfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="a5629-165">Fjerne kobling for en fil og redigere den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="a5629-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="a5629-166">Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="a5629-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="a5629-167">Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="a5629-168">Klikk **Koble fra MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="a5629-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="a5629-169">Laste opp en prosjektfil til SharePoint eller Office-grupper</span><span class="sxs-lookup"><span data-stu-id="a5629-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="a5629-170">Du kan laste opp en prosjektfil til SharePoint og finne den under dokumentene som er knyttet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a5629-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="a5629-171">Du må få administratoren til å konfigurere SharePoint-dokumentbehandling for å slå den på for Project-enheten.</span><span class="sxs-lookup"><span data-stu-id="a5629-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="a5629-172">Du kan også laste opp prosjektfilen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hvis du har definert Office-grupper.</span><span class="sxs-lookup"><span data-stu-id="a5629-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="a5629-173">Laste opp en fil for SharePoint</span><span class="sxs-lookup"><span data-stu-id="a5629-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="a5629-174">Fra hovedmenyen klikker du **Project Service** > **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="a5629-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a5629-175">Velg **Til prosjektdokumenter i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a5629-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a5629-176">I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , velger du **Ja** eller **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a5629-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a5629-177">Hvis du klikker **Ja** , er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="a5629-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a5629-178">Hvis du klikker **Nei** , virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="a5629-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a5629-179">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a5629-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="a5629-180">Laste opp en fil for Office-grupper</span><span class="sxs-lookup"><span data-stu-id="a5629-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="a5629-181">Fra hovedmenyen klikker du **Project Service** > **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="a5629-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="a5629-182">Velg **Til prosjektdokumenter i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a5629-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="a5629-183">I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , velger du **Ja** eller **Nei**.</span><span class="sxs-lookup"><span data-stu-id="a5629-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="a5629-184">Hvis du klikker **Ja** , er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="a5629-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="a5629-185">Hvis du klikker **Nei** , virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="a5629-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="a5629-186">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="a5629-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="a5629-187">Publisere prosjektet som en mal</span><span class="sxs-lookup"><span data-stu-id="a5629-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="a5629-188">Du kan lagre prosjektet og bruke det på nytt ved å lagre det som en prosjektmal i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="a5629-189">Prosjektmaler er gjenbrukbare prosjektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="a5629-190">[Opprett en prosjektmal (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="a5629-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="a5629-191">Fra kategorien **Project Service** klikker du **Publiser** > **Ny mal for Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="a5629-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="a5629-192">I dialogboksen **Publiser til et nytt prosjekt i Project Service-malen** skriver du inn **prosjektmalnavnet**.</span><span class="sxs-lookup"><span data-stu-id="a5629-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="a5629-193">Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble prosjektfilen til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="a5629-194">Klikk **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="a5629-194">Click **Publish**.</span></span>  

<span data-ttu-id="a5629-195">Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-malen til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="a5629-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="a5629-196">Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="a5629-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="a5629-197">Se også</span><span class="sxs-lookup"><span data-stu-id="a5629-197">See Also</span></span>  
 [<span data-ttu-id="a5629-198">Prosjektlederhåndbok</span><span class="sxs-lookup"><span data-stu-id="a5629-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
