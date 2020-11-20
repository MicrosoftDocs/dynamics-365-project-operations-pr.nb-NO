---
title: Veiledning for ressursansvarlig
description: En veiledning til ressursstyring i Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 04ee87e5b1a2cf96434f4862e07d2b85bad9eace
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124020"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="34b06-103">Veiledning til ressursansvarlig (Project Service)</span><span class="sxs-lookup"><span data-stu-id="34b06-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="34b06-104">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-funksjonene i [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] hjelper deg å finne de riktige ressursene til riktig tid for riktig prosjekt, og påse at alle ressurser brukes effektivt.</span><span class="sxs-lookup"><span data-stu-id="34b06-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="34b06-105">Distribuer firmaets konsulenter effektiv med [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="34b06-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="34b06-106">Disse gir deg verktøyene du trenger for å planlegge ressurser basert på kravene og tidsplanene for rådgivningsprosjekter og ferdighetene og tilgjengelighet til dine konsulenter.</span><span class="sxs-lookup"><span data-stu-id="34b06-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="34b06-107">Du kan raskt finne de mest kvalifiserte konsulentene som er tilgjengelige for å arbeide på et prosjekt, og du kan enkelt se hvordan du kan planlegge ressursbruken bedre under prosjektet.</span><span class="sxs-lookup"><span data-stu-id="34b06-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="34b06-108">Ressursplanlegging hjelper deg med å gjøre følgende:</span><span class="sxs-lookup"><span data-stu-id="34b06-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="34b06-109">Finn riktige ressurser til prosjekter, basert på hvor godt deres ferdigheter og kompetanse samsvarer med prosjektets ressurskrav.</span><span class="sxs-lookup"><span data-stu-id="34b06-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="34b06-110">Jamfør en ressurs' tidsplan med en prosjektkalender, basert på ressursens tilgjengelighet og planlagte fravær.</span><span class="sxs-lookup"><span data-stu-id="34b06-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="34b06-111">Den fargekodede kalenderen gir deg en visuell pekepinn på ressurstilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="34b06-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="34b06-112">Undersøk kapasiteten til hver konsulent og bestem hvordan denne kapasiteten brukes for øyeblikket.</span><span class="sxs-lookup"><span data-stu-id="34b06-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="34b06-113">Dette kan hjelpe deg å finne ut hvor en konsulent kan være over- eller underbelastet, eller om arbeidet er i tråd med vedkommendes kapasitet.</span><span class="sxs-lookup"><span data-stu-id="34b06-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="34b06-114">Tilordne en prosent eller et bestemt antall timer for en arbeiders kapasitet til et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="34b06-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="34b06-115">Foreta grupperessursbestillinger.</span><span class="sxs-lookup"><span data-stu-id="34b06-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="34b06-116">Foreta en ikke-forpliktende eller forpliktende bestilling av ressurser, og konverter ikke-forpliktende timer til forpliktende timer i ett trinn.</span><span class="sxs-lookup"><span data-stu-id="34b06-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="34b06-117">Dann en prosjektgruppe automatisk basert på ressurser som er definert i en arbeidsnedbrytningsstruktur for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="34b06-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="34b06-118">Fullfør ressursforespørsler (bestill, foreslå, finn erstatningsressurser).</span><span class="sxs-lookup"><span data-stu-id="34b06-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="34b06-119">Tildel ressurser i henhold til en sentral (ressursansvarlig tilordner) eller hybrid modell (ressursansvarlig og andre ledere kan tilordne).</span><span class="sxs-lookup"><span data-stu-id="34b06-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="34b06-120">Hvis du vil ha mer informasjon om hvordan du angir en sentral kontra hybrid ressursbehandlingsmodell, kan du se [Konfigurere innstillinger for flere parametere (Project Service)](../psa/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="34b06-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../psa/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="34b06-121">Du kan administrere ressurser effektivt på tvers av prosjekter og sikre at prosjekter er bemannet riktig.</span><span class="sxs-lookup"><span data-stu-id="34b06-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="34b06-122">Du må utføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="34b06-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="34b06-123">[Administrere ressursforespørsler](../psa/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="34b06-123">[Manage resource requests](../psa/manage-resource-requests.md).</span></span> <span data-ttu-id="34b06-124">Jamfør ferdighetene og kompetansen til konsulentene dine til riktige prosjekter.</span><span class="sxs-lookup"><span data-stu-id="34b06-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="34b06-125">[Vise ressurstilgjengelighet](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="34b06-125">[View resource availability](../psa/view-resource-availability.md).</span></span> <span data-ttu-id="34b06-126">Sjekk konsulentenes tilgjengelighet i en kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="34b06-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="34b06-127">[Vise ressursutnyttelse](../psa/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="34b06-127">[View resource utilization](../psa/view-resource-utilization.md).</span></span> <span data-ttu-id="34b06-128">Se tiden konsulentene er bestilt i prosent.</span><span class="sxs-lookup"><span data-stu-id="34b06-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="34b06-129">[Planlegge ressurser for et prosjekt](../psa/schedule-resources-project.md)</span><span class="sxs-lookup"><span data-stu-id="34b06-129">[Schedule resources for a project](../psa/schedule-resources-project.md).</span></span> <span data-ttu-id="34b06-130">Planlegge konsulenter for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="34b06-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="34b06-131">Hvis du vil ha mer informasjon om å sende forespørsler om ressurser for individuelle prosjekter, kan du se [Send ressursforespørsler](../psa/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="34b06-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../psa/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="34b06-132">Se også</span><span class="sxs-lookup"><span data-stu-id="34b06-132">See Also</span></span>  
 <span data-ttu-id="34b06-133">[Oversikt over Project Service](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="34b06-133">[Overview of Project Service](../psa/overview.md) </span></span>  
 <span data-ttu-id="34b06-134">[Administratorhåndbok](../psa/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="34b06-134">[Administrator Guide](../psa/admin-guide.md) </span></span>  
 <span data-ttu-id="34b06-135">[Veiledning for kontoadministrator](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="34b06-135">[Account Manager Guiden](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="34b06-136">[Prosjektlederhåndbok](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="34b06-136">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="34b06-137">Håndbok for tid, utgifter og samarbeid</span><span class="sxs-lookup"><span data-stu-id="34b06-137">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)
