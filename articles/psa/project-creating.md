---
title: Prosjektplaner
description: Dette emnet gir informasjon om hvordan du oppretter en tidsplan.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284009"
---
# <a name="project-schedules"></a>Prosjektplaner 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En prosjektplan kommuniserer hvilke oppgaver som må fullføres, hvilke ressurser som skal utføre arbeidet, og tidsrammen som arbeidet må fullføres i. Den gjenspeiler alt arbeidet som er forbundet med å levere prosjektet i tide. I Dynamics 365 Project Service Automation oppretter du en prosjektplan ved å dele opp arbeidet i håndterbare oppgaver, anslå hvor lang tid som kreves for å utføre hver enkelt oppgave, angi oppgaveavhengigheter, angi oppgavevarigheter og beregne de generelle ressursene som vil utføre oppgavene. Prosjektplanen opprettes i kategorien **Tidsplan** på prosjektsiden.
 
## <a name="tasks"></a>Oppgaver

Det første trinnet i prosessen med å opprette en prosjektplan er å dele opp arbeidet i håndterbare deler. Tidsplanen i PSA støtter følgende funksjoner:

- Rotnode for prosjektet
- Hovedaktiviteter eller beholderoppgaver
- Bladnodeoppgaver

### <a name="project-root-node"></a>Rotnode for prosjektet

Prosjektrotnoden er hovedoppgaven på øverste nivå for prosjektet. Alle andre prosjektoppgaver opprettes under den. Navnet på rotnoden er alltid angitt til navnet på prosjektet. Innsats, datoer og varighet for rotnoden er oppsummert basert på verdiene i hierarkiet under den. Du kan ikke redigere egenskapene for rotnoden. Du kan heller ikke slette rotnoden.

### <a name="summary-or-container-tasks"></a>Hovedaktiviteter eller beholderoppgaver 

Hovedoppgaver har deloppgaver eller beholderoppgaver under seg. De har ingen arbeidsinnsats eller kostnad alene. I stedet er arbeidsinnsatsen og kostnaden en beregning av arbeidsinnsatsen og kostnadene for de tilhørende beholderoppgavene. Startdatoen for hovedoppgaven er startdatoen for beholderoppgavene, og sluttdatoen er sluttdatoen for beholderoppgavene. Navnet på en hovedoppgave kan redigeres, men planleggingsegenskaper (innsats, datoer og varighet) kan ikke redigeres. Hvis du sletter en hovedoppgave, slettes også alle beholderoppgavene.

### <a name="leaf-node-tasks"></a>Bladnodeoppgaver

Bladnodeoppgaver representerer det mest detaljerte arbeidet på prosjektet. De har en beregnet arbeidsinnsats, ressurser, planlagte start- og sluttdatoer og en varighet.
 
## <a name="creating-a-task-hierarchy"></a>Opprette et oppgavehierarki

Du kan opprette et oppgavehierarki ved å bruke følgende alternativer:

- **Legg til oppgave**-knappen
- **Rykk inn aktivitet**-knappen
- **Reduser innrykk for aktivitet**-knappen
- Knappene **Flytt opp** og **Flytt ned**
- Tilgjengelighet og hurtigtaster

### <a name="add-task"></a>Legg til oppgave

Med knappen **Legg til oppgave** kan du opprette en ny oppgave i hierarkiet. Hvis du ikke velger en posisjon, settes oppgaven inn på slutten. 

En tidsplan-ID tilordnes hver enkelt oppgave. Tidspnal-ID-en representerer oppgavens dybde og posisjon i hierarkiet. Den bruker disposisjonsnummerering. For oppgaver på det første nivået under prosjektrotnoden brukes det et nummereringssett på 1, 2, 3 og så videre. For oppgaver under det første nivået brukes det et nummereringssett på 1.1, 1.2, 1.3 og så videre.

### <a name="indent-task"></a>Rykk inn aktivitet

Når en oppgave er rykket inn, blir den underordnet oppgaven som er rett over den. Tidsplan-ID-en for oppgaven beregnes deretter på nytt, slik at den er basert på tidsplan-ID-en til den nye overordnede oppgaven, og følger disposisjonsnummereringen. Den overordnede oppgaven er nå en hovedoppgave eller en beholderoppgave. Det blir derfor en fremheving av de underordnede oppgavene.

### <a name="outdent-task"></a>Reduser innrykk for aktivitet 

Når innrykket for en oppgave reduseres, er den ikke lenger en underordnet oppgaven som var overordnet. Tidsplan-ID-en beregnes deretter på nytt slik at den gjenspeiler den oppdaterte dybden og posisjonen for oppgaven i hierarkiet. Innsats, kostnader og datoer for den forrige overordnede oppgaven beregnes på nytt, slik at de ikke inneholder denne oppgaven.

### <a name="move-up-and-move-down"></a>Flytt opp og Flytt ned 

Knappene **Flytt opp** og **Flytt ned** endrer plasseringen av en oppgave i det overordnede hierarkiet. Endringer av denne typen påvirker ikke oppgavens innsats, kostnader, datoer eller varighet. Bare oppgavens tidsplan-ID berøres. Tidsplan-ID-en beregnes deretter på nytt slik at den gjenspeiler oppgavens nye posisjon i den overordnede oppgavens liste over underordnede oppgaver.

### <a name="accessibility-and-keyboard-shortcuts"></a>Tilgjengelighet og hurtigtaster

Rutenettet **Tidsplan** er fullt tilgjengelig og kan brukes med skjermlesere, for eksempel Narrator, JAWS eller NVDA. Du kan bla gjennom rutenettområdet ved hjelp av piltastene (som i Microsoft Excel), du kan bruke TAB-tasten til å gå gjennom de interaktive grensesnittelementene, og du kan bruke pil ned-tasten, ENTER-tasten eller mellomromstasten til å velge og aktivere rullegardinmenyene. Kolonneoverskriftene er også interaktive. Du kan skjule og vise kolonner, bruke TAB-tasten og piltastene til å bla gjennom kolonneoverskriftene, og bruke handlingsknappene på verktøylinjen. I tillegg kan du bruke følgende hurtigtaster:

- **Oppdater**: ALT+SKIFT+F5
- **Legg til**: ALT+SKIFT+INS
- **Slett**: ALT+SKIFT+Del
- **Flytt opp/ned**: ALT+SKIFT+Pil opp/ned
- **Rykk inn / Reduser innrykk**: ALT+SKIFT+Pil venstre/høyre
- **Vis/Skjul hierarkier**: ALT+SKIFT+pluss/minus

## <a name="task-attributes"></a>Oppgaveattributter

Et oppgavenavn beskriver arbeidet som må fullføres. I PSA er attributtene som er knyttet til en oppgave, en beskrivelse av tidsplanen til oppgaven og krav til bemanning.

> ![Oppgaveattributter](media/project-2.png)
 
### <a name="schedule-attributes"></a>Planlegge attributter

Attributtene **Innsats**, **Startdato**, **Sluttdato** og **Varighet** definerer tidsplanen for oppgaven.

Flere tidsplanattributter inkluderer:

- **Innsatstimer**: Skriv inn et estimat over timene som kreves for å fullføre oppgaven. 
- **Varighet**: Angi antall arbeidsdager som kreves for å fullføre oppgaven.
- **Tidsplan-ID**: Denne automatisk genererte ID-en brukes til å bestille oppgaver i hierarkiet. Avhengigheter mellom oppgavene styrer den faktiske rekkefølgen som oppgavene arbeides på.
 
### <a name="staffing-attributes"></a>Bemanningsattributter

Du får tilgang til attributter for bemanning via **Ressurser**-feltet i tidsplanen. Du kan søke etter en eksisterende ressurs, eller klikke **Opprett** og legge til et prosjektteammedlem som en ny ressurs i **Hurtigoppretting**-ruten.

Feltene **Rolle**, **Ressursenhet** og **Stillingsnavn** brukes til å beskrive bemanningskravene for oppgaven. Disse bemanningsattributtene sammen med oppgaveplanen brukes til å finne tilgjengelige ressurser for denne oppgaven.

**Rolle** – angi ressurstypen som kreves for å utføre oppgaven.

**Ressursenhet** – angi enheten som ressursene for oppgaven skal tilordnes fra. Dette attributtet har innvirkning på kostnads- og salgsberegningen for oppgaven hvis kostnads- og fakturasatsen for ressursen er angitt basert på ressursenheter.

**Stillingsnavn** – angi et egendefinert navn for den generelle ressursen som fungerer som en plassholder for ressursen som til syvende og sist kommer til å utføre arbeidet.

**Ressurser**-feltet inneholder stillingsnavnet til den generelle ressursen eller den navngitte ressursen når en slik finnes.

**Kategori**-feltet inneholder verdier som angir en bredere arbeidstype som oppgaven kan grupperes i. Dette feltet har ikke innvirkning på planlegging eller bemanning. Den brukes bare til rapportering.

### <a name="task-dependencies"></a>Oppgaveavhengigheter 

Du kan bruke tidsplanen i PSA til å opprette foregående relasjoner mellom aktiviteter. **Foregående**-feltet under **Oppgaver** bruker én eller flere verdier til å angi oppgavene som en oppgave avhenger av. Når foregående verdier tilordnes til en oppgave, kan oppgaven bare starte etter at alle de foregående oppgavene er fullført. På grunn av avhengigheten tilbakestilles planlagt startdato for oppgaven til datoen når de foregående oppgavene er fullført.

Oppgavemodusen har ingen innvirkning på oppdateringer som utføres på start- og sluttdatoene for foregående/avhengige oppgaver.

## <a name="task-mode"></a>Oppgavemodus 

Oppgavemodusen avgjør planleggingen av bladnodeoppgaver. PSA støtter to oppgavemoduser for hver oppgave: automatisk planlegging og manuell planlegging.

### <a name="auto-scheduling"></a>Automatisk planlegging 
 
Når oppgavemodusen angis til **Automatisk planlagt**, bruker oppgaveplanleggingsmotoren planleggingsreglene på følgende oppgaveattributter for å bestemme tidsplanen for oppgaven.

#### <a name="scheduling-rules"></a>Planleggingsregler

Hvis en bladnodeoppgave ikke har foregående oppgaver, settes startdatoen som standard til planlagt startdato for prosjektet. Varigheten av en bladnodeoppgave er alltid beregnet som antall arbeidsdager mellom start- og sluttdatoen. Når en oppgave planlegges automatisk, vil planleggingsmotoren følge disse reglene:

- Start- og sluttdatoene for oppgaven må alltid være virkedager i henhold til prosjektets planleggingskalender. 
- For enhver oppgave som har foregående oppgaver, settes som startdatoen automatisk til den seneste sluttdatoen for foregående oppgaver.
- Innsats beregnes ved hjelp av denne formelen: antall personer × varighet × timer i løpet av en standard arbeidsdag i prosjektkalenderen.

### <a name="manual-scheduling"></a>Manuell planlegging

Hvis reglene for automatisk planlegging ikke oppfyller kravene dine, kan du angi at oppgavemodusen skal være **Planlagt manuelt**. Denne innstillingen stopper planleggingsmotoren fra å beregne verdier for andre planleggingsattributter. Hvis du angir foregående oppgaver, vil du alltid ha bruk for den avhengige oppgavens startdato, uavhengig av oppgavemodusen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]