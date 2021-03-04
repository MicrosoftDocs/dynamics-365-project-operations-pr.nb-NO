---
title: Planlegge arbeidet ditte i Microsoft Project med Project Service-tillegget
description: Dette emnet gir informasjon om hvordan du bruker Microsoft Project-tillegget for Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145955"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planlegge arbeidet ditte i Microsoft Project med Project Service-tillegget

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjør det enklere for deg å utføre prosjektplanlegging og estimater. Du kan definere arbeidet slik at kostnader, arbeid og salgsverdi er tydelig når det endelige forslaget sendes.  

Du kan installere [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] og utføre planleggingen i det kjente miljøet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Bruk de kraftige egenskapene for planlegging og administrasjon av [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], og oppdater deretter prosjektplanen i Project Service Automation.  

> [!IMPORTANT]
> - For å kunne bruke SharePoint-dokumentadministrasjon for å lagre [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filer for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjekter må [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-administratoren aktivere dokumentadministrasjon. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] er bare kompatibelt med [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Last ned og installer tillegget  
 Ha [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-påloggingsinformasjonen klar. Du trenger denne informasjonen for å koble fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Fra nedlastingssenteret kan du laste ned tillegget for den støttede versjonen av Project Service, enten [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) eller [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Velg nedlastingskoblingen.  

3.  Når nedlastingen er fullført, velger du **Ja** for å installere tillegget.  

## <a name="configure-the-add-in"></a>Konfigurere tillegget  

1. Åpne [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og velg kategorien **Project Service**.  

2. Velg **Koble til**.  

3. Skriv inn påloggingsinformasjonen din, og velg deretter **Logg på**.  

   Nå kan du begynne å bruke tillegget.  

## <a name="read-from-a-template"></a>Lese fra en mal  
 Les fra en mal du har opprettet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] og kopiert til [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], for å starte prosjektplanleggingen. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Opprett en prosjektmal (Project Service Automation)](../psa/create-project-template.md)  

1.  Fra kategorien **Project Service** velger du **Lese** > **Prosjektmal for Project Service Automation**.  

2.  Velg en prosjektmal fra listen, og velg deretter **Åpne**.  

    > [!NOTE]
    >  Oppgaver som er overført fra malen til Project, settes som standard som manuelt planlagt.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Tilordne [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-roller til prosjektressurser  

1.  Åpne et prosjekt, og velg på **Oppgave**-båndet.  

2. Velg på **Gantt-diagram**-menyen, og velg deretter **Ressursliste**.  

3. I ressurslisten velger du rullegardinmenyen **Rolle for Project Service-ressurs** og velger en Project Service Automation-rolle.  

## <a name="staff-your-project-with-resources"></a>Bemanne prosjektet med ressurser  

1.  Merk en rad fra kategorien Project Service, og velg **Finn ressurser**.  

2.  På **Bestill ressurs**-skjermen merker du ressursen du vil bruke for prosjektet.  

3.  Velg **Bestill** og deretter **OK**.  

## <a name="publish-your-project"></a>Publisere prosjektet  
Når prosjektplanleggingen er fullført, er det neste trinnet å importere og publisere prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Prosjektet importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Prosessen for prising og teamgenerering brukes. Åpne prosjektet i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] for å se at teamet, prosjektestimater og arbeidsnedbrytningsstruktur er generert. Tabellen nedenfor viser hvor du finner resultatene.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-diagram**   | Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Arbeidsnedbrytningsstruktur**-skjermen. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ressursliste** |   Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektteammedlemmer**-skjermen.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Bruk av bruk**    |    Importeres til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Prosjektestimater**-skjermen.     |

**Importere og publisere prosjektet**  
1. I kategorien **Project Service** går du til **Publiser** > **Nytt Project Service Automation-prosjekt**.  

2. I dialogboksen **Publiser til et nytt prosjekt i Project Service** skriver du inn **prosjektnavnet** og velger **kunden**.  

3. Du kan også velge **Koble prosjektplan til Project Service Automation** for å koble planprosjektfilen til Project Service Automation.  

4. Velg **Publiser**.  

   Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] til skrivebeskyttet.  Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Redigere et prosjekt som er importert  
 Hvis du vil gjøre endringer i en prosjektplan som er importert til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], har du to alternativer:  

- Åpne hovedfilen og rediger den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Fjern kobling for filen og rediger den direkte i Project Service. Som standard er et prosjekt som er lastet opp fra [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], låst og kan bare redigeres i Project. Hvis du vil redigere filen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], må koblingen for filen fjernes.  

### <a name="edit-in-pn_microsoft_project"></a>Rediger i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. På hovedmenyen går du til **Project Service** > **Prosjekter**.  

2. Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Velg **Åpne i MS Project** fra båndet. Dette åpner den koblede hovedfilen i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Fjerne kobling for en fil og redigere den i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. På hovedmenyen går du til **Project Service** > **Prosjekter**.  

2. Fra listen over prosjekter åpner du det du opprettet i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Velg **Koble fra MS Project** fra båndet.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Laste opp en prosjektfil til SharePoint eller Office-grupper  
 Du kan laste opp en prosjektfil til SharePoint og finne den under dokumentene som er knyttet til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  Du må få administratoren til å konfigurere SharePoint-dokumentbehandling for å slå den på for Project-enheten. 

 Du kan også laste opp prosjektfilen til [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] hvis du har definert Office-grupper.

### <a name="upload-a-file-for-sharepoint"></a>Laste opp en fil for SharePoint  

1. På hovedmenyen går du til **Project Service** > **Last opp**.  

2. Velg **Til prosjektdokumenter i Project Service Automation**.  

3. I dialogboksen **Aktiver Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** velger du **Ja** eller **Nei**.  

   - Hvis du velger **Ja**, er det mulig å velge **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.  

   - Hvis du velger **Nei**, fungerer ikke koblingen for **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  

### <a name="upload-a-file-for-office-groups"></a>Laste opp en fil for Office-grupper  

1. På hovedmenyen går du til **Project Service** > **Last opp**.  

2. Velg **Til prosjektdokumenter i Project Service Automation**.  

3. I dialogboksen **Aktiver Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** velger du **Ja** eller **Nei**.  

   - Hvis du velger **Ja**, er det mulig å velge **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** i Project Service Automation og starte [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og laste inn prosjektfilen fra SharePoint-dokumentbiblioteket.  

   - Hvis du velger **Nei**, fungerer ikke koblingen for **Åpne i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**.  

4. [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-filen finnes i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Dokumenter** for det spesifikke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-prosjektet.  

## <a name="publish--your-project-as-a-template"></a>Publisere prosjektet som en mal  
 Du kan lagre prosjektet og bruke det på nytt ved å lagre det som en prosjektmal i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Prosjektmaler er gjenbrukbare prosjektplaner i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Hvis du vil ha mer informasjon, kan du se [Opprette en prosjektmal (Project Service Automation)](../psa/create-project-template.md). 

1. I kategorien **Project Service** går du til **Publiser** > **Ny Project Service Automation-prosjektmal**.  

2. I dialogboksen **Publiser til et nytt prosjekt i Project Service-malen** skriver du inn **prosjektmalnavnet**.  

3. Du kan også velge **Koble prosjektplan til Project Service Automation** for å koble Project-filen til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Velg **Publiser**.  

Når prosjektfilen kobles til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] gjøres den til hovedfilen og angir arbeidsnedbrytningsstrukturen i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-malen til skrivebeskyttet.  Hvis du vil gjøre endringer i prosjektplanen, må du gjøre dem i [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] og publisere dem som oppdateringer til [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Les en ressursrik tidsplan

Når du leser et prosjekt fra Project Service Automation, synkroniseres ikke ressursens kalender til skrivebordsklienten. Hvis det er forskjeller i oppgavevarighetene, innsatsen eller slutten, er det sannsynlig at ressursene og skrivebordsklienten ikke har samme malkalender for arbeidstid som brukes på prosjektet.


## <a name="data-synchronization"></a>Datasynkronisering
Tabellene i denne delen inneholder informasjon om synkronisering av enhetsdata mellom Project Service Automation og tilleggsprogrammet for stasjonær Microsoft Project.

### <a name="project-task-entity-table"></a>Tabell for prosjektoppgaveenhet
Tabellen nedenfor oppsummerer hvordan data for prosjektoppgaveenhet synkroniseres mellom Project Service Automation og Microsoft Project-tilleggsprogrammet.

| **Enhet** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Prosjektoppgave | Forfallsdato | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Beregnet innsats | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Klient-ID for MS Project | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Overordnet oppgave | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Project | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Prosjektoppgave | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Navn på prosjektoppgave | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Ressursenhet (avskrevet i versjon 3.0) | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Planlagt varighet | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | Startdato | Synkronisert | Ikke synkronisert |
| Prosjektoppgave | WBS-ID | Synkronisert | Ikke synkronisert |

### <a name="team-member-entity-table"></a>Enhetstabell for teammedlem
Tabellen nedenfor oppsummerer hvordan data for teammedlemsenhet synkroniseres mellom Project Service Automation og Micros

| **Enhet** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Teammedlem | Klient-ID for MS Project | Synkronisert | Ikke synkronisert |
| Teammedlem | Stillingsnavn | Synkronisert | Ikke synkronisert |
| Teammedlem | prosjekt | Synkronisert | Synkronisert |
| Teammedlem | Prosjektteam | Synkronisert | Synkronisert |
| Teammedlem | Ressursenhet | Ikke synkronisert | Synkronisert |
| Teammedlem | Rolle | Ikke synkronisert | Synkronisert |
| Teammedlem | Arbeidstid | Ikke synkronisert | Ikke synkronisert |

### <a name="resource-assignment-entity-table"></a>Tabell over ressurstilordningsentitet
Tabellen nedenfor oppsummerer hvordan data for ressurstilordningsenhet synkroniseres mellom Project Service Automation og Micros

| **Enhet** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Ressurstilordning | Fra dato | Synkronisert | Ikke synkronisert |
| Ressurstilordning | timer | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Klient-ID for MS Project | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Planlagt arbeid | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Project | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Prosjektteam | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Ressurstilordning | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Oppgave | Synkronisert | Ikke synkronisert |
| Ressurstilordning | Til dato | Synkronisert | Ikke synkronisert |

### <a name="project-task-dependencies-entity-table"></a>Tabell for enhet for prosjektoppgaveavhengigheter
Tabellen nedenfor oppsummerer hvordan data for enhet for prosjektoppgaveavhengigheter synkroniseres mellom Project Service Automation og Micros

| **Enhet** | **Felt** | **Microsoft Project til Project Service Automation** | **Project Service Automation til Microsoft Project** |
| --- | --- | --- | --- |
| Avhengigheter for prosjektoppgaver | Avhengighet for prosjektoppgaver | Synkronisert | Ikke synkronisert |
| Avhengigheter for prosjektoppgaver | Koblingstype | Synkronisert | Ikke synkronisert |
| Avhengigheter for prosjektoppgaver | Foregående oppgave | Synkronisert | Ikke synkronisert |
| Avhengigheter for prosjektoppgaver | Project | Synkronisert | Ikke synkronisert |
| Avhengigheter for prosjektoppgaver | Etterfølgende oppgave | Synkronisert | Ikke synkronisert |

### <a name="additional-resources"></a>Ytterligere ressurser
 [Prosjektlederhåndbok](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]