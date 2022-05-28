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
ms.reviewer: johnmichalak
ms.openlocfilehash: cf51333179d2d972af84de7adb4b718b6e17d038
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598914"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Administrere prosjekter og bestillinger i kalenderen (Project Service)

> [!Note]
> AVSKREVET: Denne funksjonen er avskrevet og er ikke lenger tilgjengelig.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Vis personlige avtaler, prosjektarbeidsbestillinger og arbeidsordretilordninger for Field Service ved hjelp av [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.  
  
 Med alt på ett sted er det enkelt å administrere hverdagen. Møter, avtaler, bestillinger og oppgaver er alle tilgjengelige i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen.  
  
 Hvis du bruker [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], kan du også angi personlige avtaler i tidsoppføringsvisningen for Project Service. Dette gjør at prosjekt- og ressursansvarlige vet tilgjengeligheten din for prosjekter. Du sparer også tid fordi du slipper å skrive inn informasjon om dine personlige avtaler to ganger. Du kan ganske enkelt importere personlige avtaler fra kalenderen til tidsoppføringsvisning for Project Service.  
  
 Kalenderen synkroniserer prosjekt- og arbeidsordrebestillinger fra i dag til de kommende fire uker. Denne innstillingen kan ikke endres.  
  
 Synkronisering støttes bare én vei, fra PSA til [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen. Du kan synkronisere i motsatt rekkefølge. 
  
 Hvis du vil lære hvordan du bruker [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, kan du se [Outlook-kalenderen på Internett for bedrifter](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Konfigurere  
 Før du kan vise og behandle dine bestillinger i [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalenderen, må du definere et par ting.  
  
- Du må ha legitimasjon for global administrator eller systemansvarlig for [!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- Administratoren må konfigurere e-postserverprofilen, og hver bruker må konfigurere postboksen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Angi e-postbehandling via synkronisering på serversiden](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Slå på synkronisering for organisasjonen (administrasjonsoppgave)  
  
1.  Fra hovedmenyen klikker du **Innstillinger** > **Administrasjon**.  
  
2.  Klikk **Systeminnstillinger**.  
  
3.  Klikk kategorien **Synkronisering**.  
  
4.  Under **Velg om du vil aktivere synkronisering av ressursbestilling med** merker du av for **Synkroniser ressursbestilling med Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Slå på synkronisering for brukerprofilen (brukeroppgave)  
  
1.  Klikk **Innstillinger**-knappen øverst til høyre på skjermen.  
  
2.  Klikk **Alternativer**.  
  
3.  Klikk kategorien **Synkronisering**.  
  
4.  Under **Synkronisering av ressursbestilling med Outlook** merker du av for **Ressursbestilling for synkronisering med Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importere personlige avtaler (brukeroppgave)  
 Du kan importere personlige avtaler fra kalenderen til tidsoppføringsvisning for Project Service Automation .  
  
1. Åpne [!INCLUDE[pn_office_365](../includes/pn-office-365.md)]-kalender, og klikk **Importer data**.  
  
2. I skjermbildet Filtre velger du **Avtaler fra Exchange** og klikker **Bruk**.  
  
3. Systemet drar avtaler til tidsoppføringsvisningen som foreslåtte oppføringer fra den gjeldende uken. Hvis du vil legge til oppføringer for en annen uke, klikker du **Forrige** eller **Neste**.  
  
4. Merk avtalen du vil legge til i tidsoppføringsvisningen for Project Service Automation.  
  
5. På **Tidsoppføring**-hurtigmenyen velger du de riktige alternativene for å konvertere avtalen til en tidsoppføringsvisning for Project Service Automation.  
  
6. Klikk **Lagre**.  
  
### <a name="see-also"></a>Se også  
 [Håndbok for tid, utgifter og samarbeid](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
