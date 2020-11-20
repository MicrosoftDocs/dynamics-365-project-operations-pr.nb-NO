---
title: Hensyn ved oppgradering – Microsoft Dynamics 365 Project Service Automation versjon 2.x eller 1.x til versjon 3
description: Dette emnet gir informasjon om hensyn du må ta når du oppgraderer fra Project Service Automation versjon 2.x eller 1.x til versjon 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3c51726f71cfd0d4be98982d6a02268d64a70b91
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121725"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Hensyn ved oppgradering – PSA-versjon 2.x eller 1.x til versjon 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation og Field Service
Både Dynamics 365 Project Service Automation og Dynamics 365 Field Service bruker løsningen Universal Resourcing Scheduling (URS) for ressursplanlegging. Hvis du har både Project Service Automation and Field Service i forekomsten, må du planlegge å oppgradere begge løsningene til den nyeste versjonen (versjon 3.x for Project Service Automation, versjon 8.x for Field Service). Oppgradering av Project Service Automation eller Field Service installerer den nyeste versjonen av URS, noe som betyr at inkonsekvent funksjonalitet er mulig hvis både Project Service Automation- og Field Service-løsningen i samme forekomst ikke oppgraderes til nyeste versjon.

## <a name="resource-assignments"></a>Ressurstilordninger
I Project Service Automation versjon 2 og versjon 1 ble oppgavetilordninger lagret som underordnede oppgaver (også kalt linjeoppgaver) i **Oppgaveenhet** og var indirekte relatert til **Ressurstilordning**-enheten. Linjeoppgaven var synlig i popup-vinduet for tilordningen i arbeidsnedbrytningsstrukturen (WBS).

![Linjeaktiviteter i WBS i Project Service Automation versjon 2 og versjon 1](media/upgrade-line-task-01.png)

I versjon 3 av Project Service Automation er det underliggende skjemaet for tilordning av bestillbare ressurser til oppgaver endret. Linjeoppgaven er avskrevet, og det er en direkte 1:1-relasjon mellom oppgaven i **Oppgaveenhet** og teammedlemmet i enheten **Ressurstilordning**. Oppgaver som er tilordnet til et prosjektteammedlem, er nå lagret direkte i ressurstilordningsenheten.  

Disse endringene påvirker oppgraderingen av eventuelle eksisterende prosjekter som har ressurstilordninger for navngitte reserverbare ressurser og generelle ressurser i et prosjektteam. Dette emnet gir deg vurderingene du må ta hensyn til for prosjektene dine når du oppgraderer til versjon 3. 

### <a name="tasks-assigned-to-named-resources"></a>Oppgaver tilordnet til navngitte ressurser
Ved hjelp av den underliggende oppgaveenheten kunne teammedlemmer ved hjelp av oppgaver i versjon 2 og versjon 1 ha en annen rolle enn standardrollen som er definert. For eksempel kunne Sigrid Hammeren, som var tilordnet rollen som Programbehandler som standard, tilordnes en oppgave med rollen utvikler. I versjon 3 er rollen for et navngitt teammedlem alltid standard, slik at alle oppgaver som Sigrid Hammeren er tilordnet, bruker standardrollen som Programbehandler.

Hvis du har tilordnet en ressurs til en aktivitet utenfor standardrollen i versjon 2 og versjon 1, tilordnes den navngitte ressursen til standardrollen for alle oppgavetilordninger når du oppgraderer, uavhengig av rolletilordning i versjon 2. Dette vil føre til forskjeller i de beregnede beregningene fra versjon 2 eller versjon 1 til versjon 3, fordi estimater beregnes basert på rollen til ressursen og ikke tilordning av linjeoppgaver. I versjon 2 er eksempelvis to oppgaver tilordnet til Aurora Tharaldsen. Rollen på linjeoppgaven for oppgave 1 er Utvikler og Programbehandler for oppgave 2. Aurora Tharaldsen har standardrollen som Programbehandler.

![Flere roller som er tilordnet én ressurs](media/upgrade-multiple-roles-02.png)

I og med at rollene som Utvikler og Programbehandler er forskjellige, er kostnads- og salgsberegningene som følger:

![Kostnadsestimater for ressursroller](media/upggrade-cost-estimates-03.png)

![Salgsestimater for ressursroller](media/upgrade-sales-estimates-04.png)

Når du oppgraderer til versjon 3, blir linjeoppgaver erstattet med ressurstilordninger for oppgaven for ressursteammedlemmet som kan bestilles. Tilordningen bruker standardrollen ressursen som kan reserveres. I grafikken nedenfor har Aurora Tharaldsen rollen som Programbehandler i ressursen.

![Ressurstilordninger](media/resource-assignment-v2-05.png)

I og med at estimatene er basert på standardrollen for ressursen, kan det hende at salgs- og kostnadsberegningene endres. Vær oppmerksom på at du ikke lenger kan se rollen **Utvikler** i grafikken nedenfor, fordi rollen nå hentes fra den bestillbare ressursens standardrolle.

![Kostnadsestimater for standardroller](media/resource-assignment-cost-estimate-06.png)
![Salgsestimater for standardroller](media/resource-assignment-sales-estimate-07.png)

Når oppgraderingen er fullført, kan du redigere rollen til et teammedlem til noen annet enn den tilordnede standarden. Hvis du imidlertid endrer teammedlemmers rolle, blir den endret på alle de tilordnede oppgavene, fordi teammedlemmer ikke lenger kan tilordnes flere roller i versjon 3.

![Oppdatere en ressursrolle](media/resource-role-assignment-08.png)

Dette gjelder også for linjeaktiviteter som er tilordnet navngitte ressurser når du endrer ressursens organisasjonsenhet fra standard til en annen organisasjonsenhet. Når oppgraderingen av versjon 3 er fullført, bruker tilordningen ressursens standard organisasjonsenhet i stedet for den som er angitt i linjeoppgaven.

### <a name="tasks-assigned-to-generic-resources"></a>Oppgaver som er tilordnet generelle ressurser
I versjon 2 og versjon 1 kan du angi rolle og organisasjonsenhet for en oppgave og deretter bruke funksjonen **Generer team** til å generere generelle ressurser basert på attributtene som er angitt for oppgaven. I versjon 3 oppretter du generelle teammedlemmer med rolle- og organisasjonsenheten, og deretter tilordner du teammedlemmene til oppgaver.

I versjon 2 og versjon 1 kan prosjekter med generelle ressurser ha to tilstander eller en kombinasjon av begge på aktivitetsnivå. Du har for eksempel følgende scenarioer:

- Oppgaver med angitte roller og organisasjonssett, men ingen tilknyttede ressurstilordning er generert.
- Oppgaver med ressurstilordninger for generelle gruppemedlemmer som ble tilordnet ved å opprette generelle ressurser med funksjonen **Generer team**.

Før du starter oppgraderingen, anbefaler vi at du genererer teamet på nytt for hvert prosjekt som har aktiviteter som er tilordnet til generelle ressurser, eller som teamprosessen fremdeles ikke er kjørt på.

For oppgaver som er tilordnet til generelle teammedlemmer som ble generert med **Generer team**, vil oppgraderingen beholde den generelle ressursen i teamet og beholde tilordningen til det generelle teammedlemmet. Vi anbefaler at du genererer ressurskravet for det generelle teammedlemmet etter oppgraderingen, men før du bestiller eller sender en ressursforespørsel. Dette bevarer eventuelle organisasjonsenhetstilordninger for de generelle teammedlemmene som er forskjellige fra prosjektets kontraktsorganisasjonsenhet.

I Prosjekt Z-prosjektet er for eksempel kontraktorganisasjonsenheten Ekeli USA. I prosjektplanen er testing av oppgaver i implementeringsfasen blitt tilordnet rollen Teknisk konsulent, og den tilordnede organisasjonsenheten er Ekeli India.

![Organisasjonstilordning for implementeringsfasen](media/org-unit-assignment-09.png)

Etter implementeringsfasen tilordnes integreringstestoppgaven til den tekniske konsulenten, men organisasjonen er satt til Ekeli USA.  

![Organisasjonstilordning for integreringstestoppgave](media/org-unit-generate-team-10.png)

Når du genererer et team for prosjektet, opprettes det to generiske teammedlemmer på grunn av de forskjellige organisasjonsenhetene i oppgavene. Teknisk konsulent 1 blir tilordnet Ekeli India-oppgaver, og Teknisk konsulent 2 får Ekeli USA-oppgavene.  

![Genererte generelle teammedlemmer](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> I Project Service Automation versjon 2 og versjon 1 inneholder ikke teammedlemmet organisasjonsenheten som vedlikeholdes på linjeoppgaven.

![Linjeoppgaver i versjon 2 og versjon 1 i Project Service Automation](media/line-tasks-12.png)

Du kan vise organisasjonsenheten i beregningsvisningen. 

![Estimater for organisasjonsenheter](media/org-unit-estimates-view-13.png)
 
Når oppgraderingen er fullført, blir organisasjonsenheten i linjeoppgaven som tilsvarer det generelle teammedlemmet, lagt til det generelle teammedlemmet, og linjeoppgaven blir fjernet. På grunn av dette anbefaler vi at før du oppgraderer, genererer eller genererer teamet på nytt for hvert prosjekt som inneholder generelle ressurser.

For oppgaver som er tilordnet til en rolle med en organisasjonsenhet som er forskjellig fra organisasjonsenheten for kontraktprosjektet, og et team ikke er generert, oppretter oppdateringen et generelt team for rollen, men vil bruke kontraktenheten for prosjektet for teammedlemmets organisasjonsenhet. Ved å se på eksemplet med Prosjekt Z betyr dette at kontraktorganisasjonsenheten Ekeli USA og prosjektplanen som tester oppgaver i implementeringsfasen, er tilordnet rollen som Teknisk konsulent med organisasjonsenheten tilordnet til Ekeli India. Integrasjonstestoppgaven som fullføres etter implementeringsfasen, er tilordnet til rollen Teknisk konsulent. Organisasjonsenheten er Ekeli USA, og et team har ikke blitt generert. Oppgraderingen oppretter ett generisk teammedlem, en teknisk konsulent som har de tildelte timene for alle tre oppgaver og organisasjonsenheten Ekeli, prosjektets kontraktorganisasjonsenhet.   
 
Endring av standarden for de ulike ressursorganisasjonsenhetene på ikke-genererte teammedlemmer er årsaken til at vi anbefaler at du genererer eller genererer teamet på nytt for hvert prosjekt som inneholder generelle ressurser, før oppgraderingen, slik at organisasjonsenhetstilordningene ikke går tapt.

