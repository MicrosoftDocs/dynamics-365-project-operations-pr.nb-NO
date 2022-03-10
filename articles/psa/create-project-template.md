---
title: Opprette en prosjektmal
description: Slik oppretter du en prosjektmal i Project Service
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
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1423dfedccfdc471662581707b4441c9ed477f7c0811ccf3905af8c59f774f77
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990868"
---
# <a name="create-a-project-template-project-service"></a>Opprette en prosjektmal (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Prosjektmaler spare tid hvis firmaet jevnlig byr på lignende typer prosjekter. De utgjør et standardsett med roller og estimert timer for en type prosjekt. Ledere for forretningsforbindelser og prosjektledere kan opprette prosjekter basert på en prosjektmal, eller de kan kopiere malen og lage en egen mal.  
  
## <a name="components-of-project-template"></a>Komponenter i prosjektmal
 En prosjektmal består av tre komponenter:  
  
- **Arbeidsnedbrytningsstruktur**: En arbeidsnedbrytningsstruktur i en prosjektmal har det samme settet med elementer som i prosjektet. Du kan opprette et oppgavehierarki, tilordne roller til oppgaven, definere attributter for tidsplan, angi avhengigheter og vise alle dataene i Gantt-diagrammet. Arbeidsnedbrytningsstrukturen i prosjektmaler støtter også aktivitetsmodi for hver aktivitet. Det er ingen forskjell mellom en prosjektmal og et prosjekt når du oppretter arbeidsplanen.  
  
- **Prosjektestimater**:Prosjektestimater i maler fungerer på samme måte som de gjør i prosjekter, bortsett fra at prislister for tilbakestilling av kostnadene og salgsprisene alltid er standardkostnader og salgsprislister definert i [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-parameterne. Resten av funksjonaliteten er den samme som i et prosjekt.  
  
- **Sette sammen prosjektteam**: Når du setter sammen et prosjektteam for en prosjektmal, kan du bestille en navngitt ressurs i en mal. Du kan bruke **Genererer prosjektteam** i arbeidsnedbrytningsstrukturen til å generere et sett med generelle ressurser. Du kan også angi nødvendige ferdigheter og kompetanser for generelle ressurser. Du kan ikke erstatte en generell ressurs med en bestillbar ressurs i prosjektmaler.  
  
## <a name="create-a-project-from-a-template"></a>Opprette et prosjekt fra en mal  
 Du kan opprette et prosjekt fra en mal på disse måtene:  
  
-   Når du oppretter et prosjekt fra en forespørsel, kan du velge en prosjektmal i hurtigopprettingsskjemaet for prosjektet.  
  
-   Når du oppretter et prosjekt ved å klikke **Nytt prosjekt**, vises prosjektskjemaet før du lagrer posten. Herfra kan du klikke **Velg en mal**-feltet for å velge fra listen over forhåndsdefinerte prosjektmaler i organisasjonen.  
  
-   Klikk **Opprett prosjekt fra en mal** på **Prosjektmal**-siden for å opprette et prosjekt fra malen.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Kopiere komponenter i en mal til et prosjekt  
 Når du kopierer komponenter i en mal til et prosjekt, er det et par ting du bør vite om.  
  
 **Kopiere en arbeidsnedbrytningsstruktur**: Når du kopierer arbeidsnedbrytningsstrukturen fra en prosjektmal, hvis prosjektet har en annen prosjektkalender enn malen, brukes arbeidstimene fra prosjektkalenderen på tidsplanen for oppgavene. Dette justerer tidsplanen til reserveprosjektkalenderen. På samme måte tar den første oppgaven i arbeidsnedbrytningsstrukturen prosjektets startdato, slik at resten av tidsplanen for oppgavehierarkiet oppdateres basert på varigheten og avhengighetene som er angitt i malens arbeidsnedbrytningsstruktur.  
  
 **Kopiere prosjektestimater**: Når du kopierer på tvers av prosjektestimatlinjer, oppdateres prislister basert på eierenheten i prosjektet for kostprislisten og kunden for salgsprislisten. Enhetskosten og salgsprisene bestemmes fra disse prislistene på prosjekter som er knyttet til en salgsenhet.  
  
 **Kopiere et prosjektteam**: Når du kopierer prosjektteamet fra malen til et prosjekt, kopieres de generelle ressursene på tvers, sammen med ferdighetene og kompetansene som er definert i malen. Tildeling av generelle ressurser blir også vedlikeholdt i prosjektmalen.  
  
### <a name="see-also"></a>Se også  
 [Prosjektlederhåndbok](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]