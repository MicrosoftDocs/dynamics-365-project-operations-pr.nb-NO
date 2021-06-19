---
title: Planlegge et prosjekt med en arbeidsnedbrytningsstruktur
description: Slik planlegger du et prosjekt med en arbeidsnedbrytningsstruktur i Project Service
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
ms.openlocfilehash: 027bcbc8995ed39af78c7ff9b1028f401c3b0d4d
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008593"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Planlegge et prosjekt med en arbeidsnedbrytningsstruktur (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

En prosjektplan kommuniserer hvilke oppgaver som må utføres, hvilke ressurser som skal utføre arbeidet, og tidsrammen som arbeidet må fullføres i. Prosjektplanen gjenspeiler alt arbeidet som er forbundet med å levere prosjektet i tide. Et av de første trinnene i startfasen av prosjektet er å komme opp med en prosjektplan. Hvis du vil opprette en prosjektplan, må du opprette en arbeidsnedbrytningsstruktur.  
  
 Opprett en prosjektstruktur med en arbeidsnedbrytningsstruktur, som hjelper deg å:  
  
- Dele opp arbeidet i håndterbare oppgaver  
  
- Beregne tiden som kreves for å fullføre en oppgave  
  
- Angi oppgaveavhengigheter og oppgavevarighet  
  
- Fastslå rollene som kreves for å fullføre hver oppgave  
  
  Prosjektplanen i arbeidsnedbrytningsstrukturen har et velkjent utseende, komplett med et interaktivt Gantt-diagram.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Opprette en arbeidsnedbrytningsstruktur for et prosjekt  
 Opprett en arbeidsnedbrytningsstruktur for å representere sekvensen av oppgavene i et prosjekt. Arbeidsnedbrytningsstrukturen omfatter oppgaver, krav for hver oppgave og informasjon om inntekter og kostnader. I en arbeidsnedbrytningsstruktur kan du legge til:  
  
-   Rekkefølgen for oppgvaer i et hierarki  
  
-   Andre oppgaver, om noen, som må fullføres før du kan starte en oppgave  
  
-   Startdato, sluttdato og varighet for en oppave  
  
-   Antall timer som kreves for en oppgave  
  
-   Eventuelle nødvendige arbeiderferdigheter og -utdanning  
  
-   Arbeiderne som er tildelt en oppgave  
  
-   Beregnet omsetning og kostnader  
  
## <a name="task-types"></a>Oppgavetyper  
Når du oppretter en arbeidsnedbrytningsstruktur, skal du bruke følgende typer oppgaver:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Rotnode for prosjektet** | Hovedaktiviteten på øverste nivå for prosjektet. Alle andre prosjektoppgaver opprettes under den. Navnet på rotoppgaven er navnet på prosjektet. Innsats, datoer og varighet for rotnoden er basert på verdiene i hierarkiet under den. Du kan ikke redigere egenskaper for rotnoden eller slette rotnoden. | 
| **Hovedaktiviteter eller beholderoppgaver** | En hovedaktivitet er en oppgave som har deloppgaver under seg. En hovedaktivitet har ikke arbeidsinnsats eller kostnader selv. Arbeidsinnsatsen og kostnadene er en beregnet verdi av deloppgavene. Du kan endre navnet på en hovedaktivitet, men du kan ikke endre innsats, datoer eller varighet, fordi de blir automatisk beregnet. Hvis du sletter en hovedaktivitet, slettes oppgaven og alle deloppgavene.|  
| **Bladnodeoppgaver** | En bladnodeoppgave representerer det mest detaljerte arbeidet på prosjektet. Den har en beregnet arbeidsinnsats, et planlagt antall ressurser, planlagte start- og sluttdatoer og en varighet.|

  
## <a name="task-hierarchy"></a>Oppgavehierarki  
 Du har følgende alternativer når du oppretter et oppgavehierarki:  
  
- **Legg til oppgave**.   Du kan legge til en oppgave i en posisjon du velger i oppgavehierarkiet. Hvis du ikke velger en posisjon, vises den nye oppgaven på slutten.  
  
- **Rykk inn aktivitet**.   Rykke inn en aktivitet for å gjøre den til en underordnet aktivitet direkte ovenfor.  
  
- **Reduser innrykk for aktivitet**.   Reduser innrykk for en aktivitet, slik at den ikke lenger en underordnet aktivitet for den opprinnelige overordnede aktiviteten.  
  
- **Flytt opp og Flytt ned**.   Flytt aktiviteter opp eller ned i hierarkiet for den overordnede aktiviteten. Hvis du flytter en aktivitet opp eller ned, har dette ingen innvirkning på arbeid, kostnader, datoer eller varighet.  
  
## <a name="task-attributes"></a>Oppgaveattributter  
 Et oppgavenavn beskriver arbeidet som må fullføres. Du kan bruke forskjellige oppgaveattributter til å beskrive tidsplanen og bemanningsbehovene for oppgaven.  
  
### <a name="schedule-attributes"></a>Planlegge attributter

 - Tilordne verdier til **Innsatstimer**, **Antall ressurser**, **Startdato**, **Sluttdato** og **Varighet** for å bestemme tidsplanen for oppgaven. 
 - **Innsats** er et estimat for timene det tar å fullføre oppgaven.
 - **Antall ressurser** er et estimat som prosjektlederen legger inn i oppgaven, for å komme opp med den beste mulige tidsplanen. 
 - **Varighet** (i dager) angir hvor mange arbeidsdager det vil ta å fullføre oppgaven.  
  
### <a name="staffing-attributes"></a>Bemanningsattributter

 - **Rolle**, **Organisasjonsenhet for ressurs**, **Antall ressurser** og **Ressurser** beskriver bemanningsbehovene for oppgaven. 
 - **Rolle** beskriver hvilken type ressurs som kreves for å utføre oppgaven. 
 - **Organisasjonsenhet for ressurs** angir organisasjonsenheten der ressursene skal bemannes for denne oppgaven. Dette også påvirker kostnader og salgsestimat for oppgaven, siden dette er gjort rede for når det skal avgjøres enhetssalgspris for ressursen. 
 - **Ressurser** inneholder en generell ressurs eller en navngitt ressurs når noe blir funnet.  
  
## <a name="task-dependencies"></a>Oppgaveavhengigheter  
 Du kan opprette avhengigheter mellom én eller flere oppgaver for foregående oppgave i arbeidsnedbrytningsstrukturen. Du kan angi én eller flere verdier for feltet for foregående oppgaver for å angi hvilke oppgaver det skal være avhengig av. Når du tilordner en verdi for foregående oppgave til en oppgave, kan oppgaven bare starte når alle de foregående oppgavene er fullført. Sette denne avhengigheten på en oppgave fører til ny beregning av den planlagte startdatoen for oppgaven som siste slutten av alle de foregående oppgavene. Foregåenderelaterte innvirkninger på en tidsplan er ikke begrenset til oppgavemodus definert på oppgaven.  
  
## <a name="task-mode"></a>Oppgavemodus  
 Oppgavemodus er en av de viktige faktorene som bestemmer planlegging av bladnodeoppgaver. Det finnes to oppgavemoduser for hver oppgave: automatisk planleggingsmodus og manuell planleggingsmodus.  
  
-   **Automatisk planlegging**.   Når du angir oppgavemodusen til automatisk planlagt, bruker oppgaveplanleggingsmotoren planleggingsreglene på følgende oppgaveattributter for å bestemme tidsplanen for oppgaven:  
  
    -   Foregående oppgaver  
  
    -   Innsats  
  
    -   Antall ressurser  
  
    -   Start- og sluttdatoer  
  
-   **Planleggingsregler**.   Startdatoen for en bladnodeoppgave som ikke har standard foregående oppgaver, settes som standard til planlagt startdato for prosjektet. Varigheten av en bladnodeoppgave er alltid beregnet som antall arbeidsdager mellom start- og sluttdatoen. Når en oppgave planlegges automatisk, vil planleggingsmotoren følge reglene nedenfor:  
  
    -   Start- og sluttdatoer for en oppgave må alltid være virkedager i henhold til prosjektets planleggingskalender  
  
    -   Startdatoen for en oppgave som har foregående oppgaver, settes som standard til den seneste sluttdatoen for foregående oppgaver  
  
    -   Innsats = antall personer * varighet * timer i en standard arbeidsdag i prosjektkalenderen  
  
-   **Manuell planlegging**.   I noen tilfeller vil du kanskje avvike fra disse reglene. I slike tilfeller kan du angi oppgavemodusen for oppgaven som skal planlegges manuelt. Dette stopper planleggingsmotoren fra å beregne verdier for andre planleggingsattributter. Angi foregående oppgaver påvirker alltid startdatoen for den avhengige oppgaven.  
  
## <a name="create-a-work-breakdown-structure"></a>Opprette en arbeidsnedbrytningsstruktur  
  
1.  Gå til **Project Service > Prosjekter**.  
  
2.  Klikk prosjektet du vil arbeide på.  
  
3.  Velg pil ned ved siden av prosjektnavnet i feltet øverst på skjermen, og klikk deretter Arbeidsnedbrytningsstruktur.  
  
4.  Hvis du vil legge til en oppgave, klikker du **Legg til oppgave**. Fyll ut feltene for oppgaven, og klikk deretter **Lagre**.  
  
5.  Fortsett å legge til oppgaver til arbeidsnedbrytningsstrukturen er fullført. Når du oppretter en arbeidsnedbrytningsstruktur, kan du gjøre følgende for å organisere oppgavene:  
  
    -   Velg en oppgave, og klikk **Innrykk** for å flytte den under en annen oppgave, eller klikk Reduser innrykk for å flytte den ut et nivå.  
  
    -   Velg en oppgave, og klikk **Flytt opp** eller **Flytt ned** for å flytte den opp eller ned i listen.  
  
    -   Klikk **Skjul Gantt-diagram** for å skjule Gantt-diagrammet, og klikk **Vis Gantt-diagram** for å vise det på nytt.  
  
    -   Velg en annen tidsperiode for Gantt-diagrammet i **Tidsskala**.  
  
6.  Hvis du vil legge til roller som du har angitt i arbeidsnedbrytningsstrukturen, for teammedlemmer i prosjektet, klikker du **Generer prosjektteam**.  
  
7.  Klikk **Lagre** nederst til høyre på skjermen når du er ferdig med endringene.  
  
### <a name="see-also"></a>Se også  
 [Prosjektlederveiledning](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]