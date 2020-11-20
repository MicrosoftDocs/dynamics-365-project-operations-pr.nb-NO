---
title: Planlegge ressurser for et prosjekt
description: Slik planlegger du ressurser for et prosjekt i Project Service
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132160"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="17f93-103">Planlegge ressurser for et prosjekt (Project Service)</span><span class="sxs-lookup"><span data-stu-id="17f93-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="17f93-104">Du kan sjekke ressurstilgjengeligheten for å få en oversikt over bestillingene, eller du kan filtrere visningen på ferdigheter, team, plassering og andre alternativer.</span><span class="sxs-lookup"><span data-stu-id="17f93-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="17f93-105">Planleggingstavlen viser liste over ressurser og deres tilgjengelighet.</span><span class="sxs-lookup"><span data-stu-id="17f93-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="17f93-106">Velg en visningsmodus for å vise tilgjengelighet etter **timer**, **dag**, **uke** eller **måned**.</span><span class="sxs-lookup"><span data-stu-id="17f93-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="17f93-107">Før du bruker planleggingstavlen, er det viktig å konfigurere den.</span><span class="sxs-lookup"><span data-stu-id="17f93-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="17f93-108">For mer informasjon, se [Konfigurere tidsplankortet (Field Service eller Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="17f93-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="17f93-109">Hvis du bruker en eldre versjon, kan du sjekke ressurstilgjengelighet under [Vise ressurstilgjengelighet](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="17f93-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="17f93-110">For å bruke bestillingsfunksjonen for planleggingstavle, geokoding og plasseringstjenester må du slå på kart.</span><span class="sxs-lookup"><span data-stu-id="17f93-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="17f93-111">På hovedmenyen, klikker du **Ressursplanlegging** > **Administrasjon**.</span><span class="sxs-lookup"><span data-stu-id="17f93-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="17f93-112">Klikk **Planleggingsparametre**.</span><span class="sxs-lookup"><span data-stu-id="17f93-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="17f93-113">Åpne oppføring og bla ned til delen **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="17f93-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="17f93-114">I feltet **Koble til kart** velger du **Ja**.</span><span class="sxs-lookup"><span data-stu-id="17f93-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="17f93-115">Godta vilkårene og lagre oppføringen.</span><span class="sxs-lookup"><span data-stu-id="17f93-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="17f93-116">På hovedmenyen velger du **Project Service** > **Planleggingstavle**.</span><span class="sxs-lookup"><span data-stu-id="17f93-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="17f93-117">Herfra er det flere måter å planlegge et bestillingskrav på manuelt.</span><span class="sxs-lookup"><span data-stu-id="17f93-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="17f93-118">Velg metoden som passer for deg.</span><span class="sxs-lookup"><span data-stu-id="17f93-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="17f93-119">Finne tilgjengelige ressurser</span><span class="sxs-lookup"><span data-stu-id="17f93-119">Find available resources</span></span>

1.  <span data-ttu-id="17f93-120">Fra **Bestillingskrav**-listen høyreklikker du på en ikke planlagt bestilling, og velger ett av følgende:</span><span class="sxs-lookup"><span data-stu-id="17f93-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="17f93-121">Velg **Finn tilgjengelighet – gjeldende ressurser** for å finne en tilgjengelig ressurs fra listen på planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="17f93-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="17f93-122">Velg **Finn tilgjengelighet – alle ressurser** for å finne en tilgjengelig ressurs fra ressurser i systemet</span><span class="sxs-lookup"><span data-stu-id="17f93-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="17f93-123">Når du gjør dette, viser filtrene alternativer for det valgte bestillingskravet.</span><span class="sxs-lookup"><span data-stu-id="17f93-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="17f93-124">Når du ser en ledig luke, høyreklikker du tidsluken på planleggingstavlen, og velger **Bestill her**.</span><span class="sxs-lookup"><span data-stu-id="17f93-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="17f93-125">Eller dra og slipp bestillingskravet til tilgjengelig tidsluke.</span><span class="sxs-lookup"><span data-stu-id="17f93-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="17f93-126">Bestill en ressurs ved hjelp av daglig visning og finn ut hvem som er underbestilt</span><span class="sxs-lookup"><span data-stu-id="17f93-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="17f93-127">På planleggingstavlen velger du **Visningsmodus** og velger **Dager**.</span><span class="sxs-lookup"><span data-stu-id="17f93-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="17f93-128">Dette viser en rutenettvisning av hvor mange timer en ressurs er bestilt per dag og hvilke dager som de er gratis.</span><span class="sxs-lookup"><span data-stu-id="17f93-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="17f93-129">Klikk navnet på ressursen som du vil reservere, og velg deretter **Bestill**.</span><span class="sxs-lookup"><span data-stu-id="17f93-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="17f93-130">I dialogboksen **Ressursbestilling (opprett)** velger du prosjektet som du vil reservere ressursen for, sammen med bestillingsmetoden og start- og sluttidspunkt.</span><span class="sxs-lookup"><span data-stu-id="17f93-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="17f93-131">Velg **Bestill** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="17f93-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="17f93-132">Vise planleggingstavlen</span><span class="sxs-lookup"><span data-stu-id="17f93-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="17f93-133">Velg et bestillingskrav som ikke er planlagt, fra listen nederst.</span><span class="sxs-lookup"><span data-stu-id="17f93-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="17f93-134">Dra bestillingskravet til en tilgjengelig ressurs-/tidsluke på planleggingstavlen.</span><span class="sxs-lookup"><span data-stu-id="17f93-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="17f93-135">Velg **Bestill** når du er ferdig.</span><span class="sxs-lookup"><span data-stu-id="17f93-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="17f93-136">Ytterligere ressurser</span><span class="sxs-lookup"><span data-stu-id="17f93-136">Additional resources</span></span>  
 [<span data-ttu-id="17f93-137">Veiledning for ressursansvarlig</span><span class="sxs-lookup"><span data-stu-id="17f93-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
