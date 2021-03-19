---
title: Spore status for et prosjekt
description: Slik sporer du status for et prosjekt i Project Service
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
ms.openlocfilehash: d57f33cdf240db4cae1f33fe962173790fe0fe7f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281940"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="f373b-103">Spore status for et prosjekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f373b-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f373b-104">Bruk [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] til å spore fremdriften for prosjektet til en klient.</span><span class="sxs-lookup"><span data-stu-id="f373b-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="f373b-105">Senere i engasjementet oppdateres prosjektfasene for å gjenspeile fasen i engasjementet:</span><span class="sxs-lookup"><span data-stu-id="f373b-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="f373b-106">**Ny**</span><span class="sxs-lookup"><span data-stu-id="f373b-106">**New**</span></span>    | <span data-ttu-id="f373b-107">Når du oppretter et prosjekt, er fasen satt til **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f373b-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="f373b-108">Hvis du opprettet prosjektet fra en mal, kan prosjektet i denne fasen ha en tidsplan, estimater og teamdata.</span><span class="sxs-lookup"><span data-stu-id="f373b-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="f373b-109">Ellers vil det være disposisjonen for prosjektet, og du må manuelt angi resten av prosjektkomponentene.</span><span class="sxs-lookup"><span data-stu-id="f373b-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="f373b-110">**Tilbud**</span><span class="sxs-lookup"><span data-stu-id="f373b-110">**Quote**</span></span>   |      <span data-ttu-id="f373b-111">Når du knytter et prosjekt til et tilbud eller oppretter det fra et tilbud, er prosjektfasen satt til **Tilbud**, og de estimerte start- og sluttdatoene oppdateres også.</span><span class="sxs-lookup"><span data-stu-id="f373b-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="f373b-112">Når prosjektet er i tilbudsfasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="f373b-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="f373b-113">**Plan**</span><span class="sxs-lookup"><span data-stu-id="f373b-113">**Plan**</span></span>   |                                     <span data-ttu-id="f373b-114">Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til kontraktfasen, oppdateres prosjektfasen til **Plan**.</span><span class="sxs-lookup"><span data-stu-id="f373b-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="f373b-115">Kontraktdetaljene vises i kategorien **Salg** på **Prosjekt**-siden.</span><span class="sxs-lookup"><span data-stu-id="f373b-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="f373b-116">**Fullfør**</span><span class="sxs-lookup"><span data-stu-id="f373b-116">**Complete**</span></span> |                    <span data-ttu-id="f373b-117">Når prosjektarbeidet er fullført, kan du bytte fase til **Fullført**.</span><span class="sxs-lookup"><span data-stu-id="f373b-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="f373b-118">Når prosjektfasen er satt til Fullført, er det forstått at arbeidet er 100 % fullført, men prosjektet holdes åpent for alle ventende tids- eller utgiftsposter som skal registreres.</span><span class="sxs-lookup"><span data-stu-id="f373b-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="f373b-119">**Lukk**</span><span class="sxs-lookup"><span data-stu-id="f373b-119">**Close**</span></span>   |           <span data-ttu-id="f373b-120">Når alle transaksjoner er registrert i prosjektet og du ikke forventer at flere skal loggføres, kan du manuelt sette fasen til **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="f373b-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="f373b-121">Når prosjektet er satt til **Lukk**, kan du ikke loggføre flere transaksjoner i prosjektet, og prosjektet vil være skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="f373b-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="f373b-122">Slik sporer du status for et prosjekt</span><span class="sxs-lookup"><span data-stu-id="f373b-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="f373b-123">Gå til **Project Service > Prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="f373b-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="f373b-124">Klikk prosjektet du vil arbeide på.</span><span class="sxs-lookup"><span data-stu-id="f373b-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="f373b-125">Velg pil ned ved siden av prosjektnavnet i feltet øverst på skjermen, og klikk deretter **Prosjektsporing**.</span><span class="sxs-lookup"><span data-stu-id="f373b-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="f373b-126">Velg **Innsatssporing** eller **Kostnadssporing** i rullegardinlisten over oppgavelisten.</span><span class="sxs-lookup"><span data-stu-id="f373b-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="f373b-127">Dobbeltklikk en hvilken som helst oppgave for å redigere den.</span><span class="sxs-lookup"><span data-stu-id="f373b-127">Double-click any task to edit it.</span></span> <span data-ttu-id="f373b-128">Du kan også flytte eller endre størrelse på stolpene i Gantt-diagrammet for å endre klokkeslett og fremdriften for en oppgave.</span><span class="sxs-lookup"><span data-stu-id="f373b-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="f373b-129">Se også</span><span class="sxs-lookup"><span data-stu-id="f373b-129">See Also</span></span>  
 [<span data-ttu-id="f373b-130">Prosjektlederhåndbok</span><span class="sxs-lookup"><span data-stu-id="f373b-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]