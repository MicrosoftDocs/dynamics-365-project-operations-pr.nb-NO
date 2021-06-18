---
title: Administrere prosjekter og bestillinger i Office 365-kalenderen
description: Slik administrerer du prosjekter og bestillinger i Office 365-kalenderen
author: ruhercul
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 575f3c94f886d12717496445d0e6357fdc01246b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000403"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="9a001-103">Administrere prosjekter og bestillinger i kalenderen (Project Service)</span><span class="sxs-lookup"><span data-stu-id="9a001-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="9a001-104">AVSKREVET: Denne funksjonen er avskrevet og er ikke lenger tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="9a001-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="9a001-105">Vis personlige avtaler, prosjektarbeidsbestillinger og arbeidsordretilordninger for Field Service ved hjelp av [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.</span><span class="sxs-lookup"><span data-stu-id="9a001-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="9a001-106">Med alt på ett sted er det enkelt å administrere hverdagen.</span><span class="sxs-lookup"><span data-stu-id="9a001-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="9a001-107">Møter, avtaler, bestillinger og oppgaver er alle tilgjengelige i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.</span><span class="sxs-lookup"><span data-stu-id="9a001-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="9a001-108">Hvis du bruker [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kan du også angi personlige avtaler i tidsoppføringsvisningen for Project Service.</span><span class="sxs-lookup"><span data-stu-id="9a001-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="9a001-109">Dette gjør at prosjekt- og ressursansvarlige vet tilgjengeligheten din for prosjekter.</span><span class="sxs-lookup"><span data-stu-id="9a001-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="9a001-110">Du sparer også tid fordi du slipper å skrive inn informasjon om dine personlige avtaler to ganger.</span><span class="sxs-lookup"><span data-stu-id="9a001-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="9a001-111">Du kan ganske enkelt importere personlige avtaler fra kalenderen til tidsoppføringsvisning for Project Service.</span><span class="sxs-lookup"><span data-stu-id="9a001-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="9a001-112">Kalenderen synkroniserer prosjekt- og arbeidsordrebestillinger fra i dag til de kommende fire uker.</span><span class="sxs-lookup"><span data-stu-id="9a001-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="9a001-113">Denne innstillingen kan ikke endres.</span><span class="sxs-lookup"><span data-stu-id="9a001-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="9a001-114">Synkronisering støttes bare én vei, fra PSA til [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.</span><span class="sxs-lookup"><span data-stu-id="9a001-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="9a001-115">Du kan synkronisere i motsatt rekkefølge.</span><span class="sxs-lookup"><span data-stu-id="9a001-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="9a001-116">Hvis du vil lære hvordan du bruker [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, kan du se [Outlook-kalenderen på Internett for bedrifter](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span><span class="sxs-lookup"><span data-stu-id="9a001-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="9a001-117">Konfigurere</span><span class="sxs-lookup"><span data-stu-id="9a001-117">Setup</span></span>  
 <span data-ttu-id="9a001-118">Før du kan vise og behandle dine bestillinger i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, må du definere et par ting.</span><span class="sxs-lookup"><span data-stu-id="9a001-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="9a001-119">Du må ha legitimasjon for global administrator eller systemansvarlig for [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].</span><span class="sxs-lookup"><span data-stu-id="9a001-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="9a001-120">Administratoren må konfigurere e-postserverprofilen, og hver bruker må konfigurere postboksen.</span><span class="sxs-lookup"><span data-stu-id="9a001-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="9a001-121">[Angi e-postbehandling via synkronisering på serversiden](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="9a001-121">[Set up email processing through server-side synchronization](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="9a001-122">Slå på synkronisering for organisasjonen (administrasjonsoppgave)</span><span class="sxs-lookup"><span data-stu-id="9a001-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="9a001-123">Fra hovedmenyen klikker du **Innstillinger** > **Administrasjon**.</span><span class="sxs-lookup"><span data-stu-id="9a001-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="9a001-124">Klikk **Systeminnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="9a001-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="9a001-125">Klikk kategorien **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="9a001-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="9a001-126">Under **Velg om du vil aktivere synkronisering av ressursbestilling med** merker du av for **Synkroniser ressursbestilling med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9a001-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="9a001-127">Slå på synkronisering for brukerprofilen (brukeroppgave)</span><span class="sxs-lookup"><span data-stu-id="9a001-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="9a001-128">Klikk **Innstillinger**-knappen øverst til høyre på skjermen.</span><span class="sxs-lookup"><span data-stu-id="9a001-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="9a001-129">Klikk **Alternativer**.</span><span class="sxs-lookup"><span data-stu-id="9a001-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="9a001-130">Klikk kategorien **Synkronisering**.</span><span class="sxs-lookup"><span data-stu-id="9a001-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="9a001-131">Under **Synkronisering av ressursbestilling med Outlook** merker du av for **Ressursbestilling for synkronisering med Outlook**.</span><span class="sxs-lookup"><span data-stu-id="9a001-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="9a001-132">Importere personlige avtaler (brukeroppgave)</span><span class="sxs-lookup"><span data-stu-id="9a001-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="9a001-133">Du kan importere personlige avtaler fra kalenderen til tidsoppføringsvisning for Project Service Automation .</span><span class="sxs-lookup"><span data-stu-id="9a001-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="9a001-134">Åpne [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, og klikk **Importer data**.</span><span class="sxs-lookup"><span data-stu-id="9a001-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="9a001-135">I skjermbildet Filtre velger du **Avtaler fra Exchange** og klikker **Bruk**.</span><span class="sxs-lookup"><span data-stu-id="9a001-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="9a001-136">Systemet drar avtaler til tidsoppføringsvisningen som foreslåtte oppføringer fra den gjeldende uken.</span><span class="sxs-lookup"><span data-stu-id="9a001-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="9a001-137">Hvis du vil legge til oppføringer for en annen uke, klikker du **Forrige** eller **Neste**.</span><span class="sxs-lookup"><span data-stu-id="9a001-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="9a001-138">Merk avtalen du vil legge til i tidsoppføringsvisningen for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a001-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="9a001-139">På **Tidsoppføring**-hurtigmenyen velger du de riktige alternativene for å konvertere avtalen til en tidsoppføringsvisning for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="9a001-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="9a001-140">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9a001-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9a001-141">Se også</span><span class="sxs-lookup"><span data-stu-id="9a001-141">See Also</span></span>  
 [<span data-ttu-id="9a001-142">Håndbok for tid, utgifter og samarbeid</span><span class="sxs-lookup"><span data-stu-id="9a001-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]