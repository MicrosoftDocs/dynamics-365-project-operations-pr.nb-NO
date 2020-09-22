---
title: Bruke tillegget Project Service til å planlegge arbeidet i Microsoft Project | MicrosoftDocs
description: Dette emnet gir informasjon om hvordan du legger til, konfigurerer og bruker Microsoft Project-tillegget for Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754079"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="bcc88-103">Bruke tillegget Project Service Automation til å planlegge arbeidet i Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="bcc88-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="bcc88-104">gjør det enklere for deg å utføre prosjektplanlegging og estimater.</span><span class="sxs-lookup"><span data-stu-id="bcc88-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="bcc88-105">Du kan definere arbeidet slik at kostnader, arbeid og salgsverdi er tydelig når det endelige forslaget sendes.</span><span class="sxs-lookup"><span data-stu-id="bcc88-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="bcc88-106">Nå kan du installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og utføre planleggingen i det kjente miljøet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="bcc88-107">Bruk de kraftige egenskapene for planlegging og administrasjon av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og oppdater deretter prosjektplanen i Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bcc88-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="bcc88-108">For å kunne bruke SharePoint-dokumentadministrasjon for å lagre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjekter må [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administratoren aktivere dokumentadministrasjon.</span><span class="sxs-lookup"><span data-stu-id="bcc88-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc88-109">[Aktivere dokumentbehandling i SharePoint for bestemte enheter](../admin/enable-sharepoint-document-management-specific-entities.md)</span><span class="sxs-lookup"><span data-stu-id="bcc88-109">[Enable SharePoint document management for specific entities](../admin/enable-sharepoint-document-management-specific-entities.md)</span></span>  
> - <span data-ttu-id="bcc88-110">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er bare kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="bcc88-110">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="bcc88-111">Last ned og installer tillegget</span><span class="sxs-lookup"><span data-stu-id="bcc88-111">Download and install the add-in</span></span>  
 <span data-ttu-id="bcc88-112">Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-påloggingsinformasjonen klar.</span><span class="sxs-lookup"><span data-stu-id="bcc88-112">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="bcc88-113">Du trenger denne informasjonen for å koble fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-113">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="bcc88-114">Fra nedlastingssenteret kan du laste ned tillegget for den støttede versjonen av Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="bcc88-114">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="bcc88-115">Klikk nedlastingskoblingen.</span><span class="sxs-lookup"><span data-stu-id="bcc88-115">Click the download link.</span></span>  

3.  <span data-ttu-id="bcc88-116">Når nedlastingen er fullført, klikker du **Ja** for å installere tillegget.</span><span class="sxs-lookup"><span data-stu-id="bcc88-116">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="bcc88-117">Konfigurere tillegget</span><span class="sxs-lookup"><span data-stu-id="bcc88-117">Configure the add-in</span></span>  

1. <span data-ttu-id="bcc88-118">Åpne [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og klikk kategorien **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-118">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="bcc88-119">Klikk **Koble til**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-119">Click **Connect**.</span></span>  

3. <span data-ttu-id="bcc88-120">Skriv inn påloggingsinformasjonen din, og klikk deretter **Logg på**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-120">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="bcc88-121">Nå kan du begynne å bruke tillegget.</span><span class="sxs-lookup"><span data-stu-id="bcc88-121">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="bcc88-122">Lese fra en mal</span><span class="sxs-lookup"><span data-stu-id="bcc88-122">Read from a template</span></span>  
 <span data-ttu-id="bcc88-123">Les fra en mal du har opprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopiert til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for å starte prosjektplanleggingen.</span><span class="sxs-lookup"><span data-stu-id="bcc88-123">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc88-124">[Opprett en prosjektmal (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="bcc88-124">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1.  <span data-ttu-id="bcc88-125">Fra kategorien **Project Service** klikker du **Lese** > **Prosjektmal for Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-125">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="bcc88-126">Velg en prosjektmal fra listen, og klikk deretter **Åpne**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-126">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="bcc88-127">Oppgaver som er overført fra malen til Project, settes som standard som manuelt planlagt.</span><span class="sxs-lookup"><span data-stu-id="bcc88-127">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="bcc88-128">Tilordne [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="bcc88-128">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="bcc88-129">Åpne et prosjekt, og klikk på **Oppgave**-båndet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-129">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="bcc88-130">Klikk på **Gantt-diagram**-menyen, og velg deretter **Ressursliste**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-130">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="bcc88-131">I ressurslisten klikker du rullegardinmenyen **Rolle for Project Service-ressurs** og velger en Project Service Automation-rolle.</span><span class="sxs-lookup"><span data-stu-id="bcc88-131">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="bcc88-132">Bemanne prosjektet med ressurser</span><span class="sxs-lookup"><span data-stu-id="bcc88-132">Staff your project with resources</span></span>  

1.  <span data-ttu-id="bcc88-133">Merk en rad fra kategorien Project Service, og klikk **Finn ressurser**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-133">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="bcc88-134">På **Bestill ressurs**-skjermen merker du ressursen du vil bruke for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-134">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="bcc88-135">Klikk **Bestill**, og klikk deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-135">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="bcc88-136">Publisere prosjektet</span><span class="sxs-lookup"><span data-stu-id="bcc88-136">Publish your project</span></span>  
<span data-ttu-id="bcc88-137">Når prosjektplanleggingen er fullført, er det neste trinnet å importere og publisere prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-137">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="bcc88-138">Prosjektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-138">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="bcc88-139">Prosessen for prising og teamgenerering brukes.</span><span class="sxs-lookup"><span data-stu-id="bcc88-139">The pricing and team generation process are applied.</span></span> <span data-ttu-id="bcc88-140">Åpne prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å se at teamet, prosjektestimater og arbeidsnedbrytningsstruktur er generert.</span><span class="sxs-lookup"><span data-stu-id="bcc88-140">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="bcc88-141">Tabellen nedenfor viser hvor du finner resultatene:</span><span class="sxs-lookup"><span data-stu-id="bcc88-141">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="bcc88-142">**Gantt-diagram**</span><span class="sxs-lookup"><span data-stu-id="bcc88-142">**Gantt Chart**</span></span>   | <span data-ttu-id="bcc88-143">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbeidsnedbrytningsstruktur**-skjermen.</span><span class="sxs-lookup"><span data-stu-id="bcc88-143">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="bcc88-144">**Ressursliste**</span><span class="sxs-lookup"><span data-stu-id="bcc88-144">**Resource Sheet**</span></span> |   <span data-ttu-id="bcc88-145">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektteammedlemmer**-skjermen.</span><span class="sxs-lookup"><span data-stu-id="bcc88-145">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="bcc88-146">**Bruk av bruk**</span><span class="sxs-lookup"><span data-stu-id="bcc88-146">**Use Usage**</span></span>    |    <span data-ttu-id="bcc88-147">Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektestimater**-skjermen.</span><span class="sxs-lookup"><span data-stu-id="bcc88-147">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="bcc88-148">**Importere og publisere prosjektet**</span><span class="sxs-lookup"><span data-stu-id="bcc88-148">**To import and publish your project**</span></span>  
1. <span data-ttu-id="bcc88-149">Fra kategorien **Project Service** klikker du **Publiser** > **Nytt Project Service Automation-prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-149">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="bcc88-150">I dialogboksen **Publiser til et nytt prosjekt i Project Service** skriver du inn **prosjektnavnet** og velger **kunden**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-150">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="bcc88-151">Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble planprosjektfilen til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="bcc88-151">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="bcc88-152">Klikk **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-152">Click **Publish**.</span></span>  

   <span data-ttu-id="bcc88-153">Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-153">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="bcc88-154">Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-154">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="bcc88-155">Redigere et prosjekt som er importert</span><span class="sxs-lookup"><span data-stu-id="bcc88-155">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="bcc88-156">Hvis du vil gjøre endringer i en prosjektplan som er importert til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to alternativer:</span><span class="sxs-lookup"><span data-stu-id="bcc88-156">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="bcc88-157">Åpne hovedfilen og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-157">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="bcc88-158">Fjern kobling for filen og rediger den direkte i Project Service.</span><span class="sxs-lookup"><span data-stu-id="bcc88-158">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="bcc88-159">Som standard er et prosjekt som er lastet opp fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan bare redigeres i Project.</span><span class="sxs-lookup"><span data-stu-id="bcc88-159">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="bcc88-160">Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], må koblingen for filen fjernes.</span><span class="sxs-lookup"><span data-stu-id="bcc88-160">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="bcc88-161">Redigere i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="bcc88-161">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="bcc88-162">Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-162">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="bcc88-163">Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-163">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="bcc88-164">Klikk **Åpne i MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-164">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="bcc88-165">Dette åpner den koblede hovedfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-165">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="bcc88-166">Fjerne kobling for en fil og redigere den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="bcc88-166">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="bcc88-167">Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-167">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="bcc88-168">Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-168">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="bcc88-169">Klikk **Koble fra MS Project** fra båndet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-169">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="bcc88-170">Laste opp en prosjektfil til SharePoint eller Office-grupper</span><span class="sxs-lookup"><span data-stu-id="bcc88-170">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="bcc88-171">Du kan laste opp en prosjektfil til SharePoint og finne den under dokumentene som er knyttet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-171">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="bcc88-172">Du må få administratoren til å konfigurere SharePoint-dokumentbehandling for å slå den på for Project-enheten.</span><span class="sxs-lookup"><span data-stu-id="bcc88-172">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc88-173">[Sette opp SharePoint-integrasjon](../admin/set-up-sharepoint-integration.md)</span><span class="sxs-lookup"><span data-stu-id="bcc88-173">[Set up SharePoint integration](../admin/set-up-sharepoint-integration.md)</span></span>  

 <span data-ttu-id="bcc88-174">Du kan også laste opp prosjektfilen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hvis du har definert Office-grupper.</span><span class="sxs-lookup"><span data-stu-id="bcc88-174">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc88-175">[Samarbeide med kollegaene ved hjelp av Office 365-grupper](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span><span class="sxs-lookup"><span data-stu-id="bcc88-175">[Collaborate with your colleagues using Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)</span></span>  

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="bcc88-176">Laste opp en fil for SharePoint</span><span class="sxs-lookup"><span data-stu-id="bcc88-176">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="bcc88-177">Fra hovedmenyen klikker du **Project Service** > **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-177">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="bcc88-178">Velg **Til prosjektdokumenter i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-178">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="bcc88-179">I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, velger du **Ja** eller **Nei**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-179">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="bcc88-180">Hvis du klikker **Ja**, er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="bcc88-180">If you click **Yes**, you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="bcc88-181">Hvis du klikker **Nei**, virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-181">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="bcc88-182">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-182">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="bcc88-183">Laste opp en fil for Office-grupper</span><span class="sxs-lookup"><span data-stu-id="bcc88-183">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="bcc88-184">Fra hovedmenyen klikker du **Project Service** > **Last opp**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-184">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="bcc88-185">Velg **Til prosjektdokumenter i Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-185">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="bcc88-186">I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, velger du **Ja** eller **Nei**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-186">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="bcc88-187">Hvis du klikker **Ja**, er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="bcc88-187">If you click **Yes**, you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="bcc88-188">Hvis du klikker **Nei**, virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-188">If you click **No**, the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="bcc88-189">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-189">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="bcc88-190">Publisere prosjektet som en mal</span><span class="sxs-lookup"><span data-stu-id="bcc88-190">Publish  your project as a template</span></span>  
 <span data-ttu-id="bcc88-191">Du kan lagre prosjektet og bruke det på nytt ved å lagre det som en prosjektmal i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-191">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="bcc88-192">Prosjektmaler er gjenbrukbare prosjektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-192">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="bcc88-193">[Opprett en prosjektmal (Project Service Automation)](../project-service/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="bcc88-193">[Create a project template (Project Service Automation)](../project-service/create-project-template.md)</span></span>  

1. <span data-ttu-id="bcc88-194">Fra kategorien **Project Service** klikker du **Publiser** > **Ny mal for Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-194">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="bcc88-195">I dialogboksen **Publiser til et nytt prosjekt i Project Service-malen** skriver du inn **prosjektmalnavnet**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-195">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="bcc88-196">Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble prosjektfilen til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-196">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="bcc88-197">Klikk **Publiser**.</span><span class="sxs-lookup"><span data-stu-id="bcc88-197">Click **Publish**.</span></span>  

<span data-ttu-id="bcc88-198">Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-malen til skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="bcc88-198">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="bcc88-199">Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="bcc88-199">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="bcc88-200">Se også</span><span class="sxs-lookup"><span data-stu-id="bcc88-200">See Also</span></span>  
 [<span data-ttu-id="bcc88-201">Prosjektlederhåndbok</span><span class="sxs-lookup"><span data-stu-id="bcc88-201">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
