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
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Bruke tillegget Project Service Automation til å planlegge arbeidet i Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjør det enklere for deg å utføre prosjektplanlegging og estimater. Du kan definere arbeidet slik at kostnader, arbeid og salgsverdi er tydelig når det endelige forslaget sendes.  

 Nå kan du installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og utføre planleggingen i det kjente miljøet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Bruk de kraftige egenskapene for planlegging og administrasjon av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og oppdater deretter prosjektplanen i Project Service Automation.  

> [!IMPORTANT]
> - For å kunne bruke SharePoint-dokumentadministrasjon for å lagre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjekter må [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administratoren aktivere dokumentadministrasjon. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er bare kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Last ned og installer tillegget  
 Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-påloggingsinformasjonen klar. Du trenger denne informasjonen for å koble fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Fra nedlastingssenteret kan du laste ned tillegget for den støttede versjonen av Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Klikk nedlastingskoblingen.  

3.  Når nedlastingen er fullført, klikker du **Ja** for å installere tillegget.  

## <a name="configure-the-add-in"></a>Konfigurere tillegget  

1. Åpne [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og klikk kategorien **Project Service**.  

2. Klikk **Koble til**.  

3. Skriv inn påloggingsinformasjonen din, og klikk deretter **Logg på**.  

   Nå kan du begynne å bruke tillegget.  

## <a name="read-from-a-template"></a>Lese fra en mal  
 Les fra en mal du har opprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopiert til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for å starte prosjektplanleggingen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Opprett en prosjektmal (Project Service Automation)](../psa/create-project-template.md)  

1.  Fra kategorien **Project Service** klikker du **Lese** > **Prosjektmal for Project Service Automation**.  

2.  Velg en prosjektmal fra listen, og klikk deretter **Åpne**.  

    > [!NOTE]
    >  Oppgaver som er overført fra malen til Project, settes som standard som manuelt planlagt.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Tilordne [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til prosjektressurser  

1.  Åpne et prosjekt, og klikk på **Oppgave** -båndet.  

2.  Klikk på **Gantt-diagram** -menyen, og velg deretter **Ressursliste**.  

3.  I ressurslisten klikker du rullegardinmenyen **Rolle for Project Service-ressurs** og velger en Project Service Automation-rolle.  

## <a name="staff-your-project-with-resources"></a>Bemanne prosjektet med ressurser  

1.  Merk en rad fra kategorien Project Service, og klikk **Finn ressurser**.  

2.  På **Bestill ressurs** -skjermen merker du ressursen du vil bruke for prosjektet.  

3.  Klikk **Bestill** , og klikk deretter **OK**.  

## <a name="publish-your-project"></a>Publisere prosjektet  
Når prosjektplanleggingen er fullført, er det neste trinnet å importere og publisere prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Prosjektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Prosessen for prising og teamgenerering brukes. Åpne prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å se at teamet, prosjektestimater og arbeidsnedbrytningsstruktur er generert. Tabellen nedenfor viser hvor du finner resultatene:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-diagram**   | Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbeidsnedbrytningsstruktur** -skjermen. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressursliste** |   Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektteammedlemmer** -skjermen.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Bruk av bruk**    |    Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektestimater** -skjermen.     |

**Importere og publisere prosjektet**  
1. Fra kategorien **Project Service** klikker du **Publiser** > **Nytt Project Service Automation-prosjekt**.  

2. I dialogboksen **Publiser til et nytt prosjekt i Project Service** skriver du inn **prosjektnavnet** og velger **kunden**.  

3. Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble planprosjektfilen til Project Service Automation.  

4. Klikk **Publiser**.  

   Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.  Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Redigere et prosjekt som er importert  
 Hvis du vil gjøre endringer i en prosjektplan som er importert til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to alternativer:  

- Åpne hovedfilen og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Fjern kobling for filen og rediger den direkte i Project Service. Som standard er et prosjekt som er lastet opp fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan bare redigeres i Project. Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], må koblingen for filen fjernes.  

### <a name="edit-in-pn_microsoft_project"></a>Redigere i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.  

2. Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klikk **Åpne i MS Project** fra båndet. Dette åpner den koblede hovedfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Fjerne kobling for en fil og redigere den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Fra hovedmenyen klikker du **Project Service** > **Prosjekter**.  

2. Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Klikk **Koble fra MS Project** fra båndet.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Laste opp en prosjektfil til SharePoint eller Office-grupper  
 Du kan laste opp en prosjektfil til SharePoint og finne den under dokumentene som er knyttet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  Du må få administratoren til å konfigurere SharePoint-dokumentbehandling for å slå den på for Project-enheten. 

 Du kan også laste opp prosjektfilen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hvis du har definert Office-grupper.

### <a name="upload-a-file-for-sharepoint"></a>Laste opp en fil for SharePoint  

1. Fra hovedmenyen klikker du **Project Service** > **Last opp**.  

2. Velg **Til prosjektdokumenter i Project Service Automation**.  

3. I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , velger du **Ja** eller **Nei**.  

   - Hvis du klikker **Ja** , er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.  

   - Hvis du klikker **Nei** , virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  

### <a name="upload-a-file-for-office-groups"></a>Laste opp en fil for Office-grupper  

1. Fra hovedmenyen klikker du **Project Service** > **Last opp**.  

2. Velg **Til prosjektdokumenter i Project Service Automation**.  

3. I dialogboksen **Aktiver Åpne i dialogboksen [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , velger du **Ja** eller **Nei**.  

   - Hvis du klikker **Ja** , er det mulig å velge knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.  

   - Hvis du klikker **Nei** , virker ikke koblingen for knappen **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  

## <a name="publish--your-project-as-a-template"></a>Publisere prosjektet som en mal  
 Du kan lagre prosjektet og bruke det på nytt ved å lagre det som en prosjektmal i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Prosjektmaler er gjenbrukbare prosjektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Opprett en prosjektmal (Project Service Automation)](../psa/create-project-template.md)  

1. Fra kategorien **Project Service** klikker du **Publiser** > **Ny mal for Project Service Automation**.  

2. I dialogboksen **Publiser til et nytt prosjekt i Project Service-malen** skriver du inn **prosjektmalnavnet**.  

3. Du kan også merke av for **Koble prosjektplan til Project Service Automation** for å koble prosjektfilen til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Klikk **Publiser**.  

Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-malen til skrivebeskyttet.  Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Se også  
 [Prosjektlederhåndbok](../psa/project-manager-guide.md)
