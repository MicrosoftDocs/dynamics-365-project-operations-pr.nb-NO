---
title: Opprette en arbeidsnedbrytningsstruktur
description: Dette emnet forklarer hvordan du oppretter en WBS-avtale om arbeidsplass for de grunnleggende kontrollene i det nye planleggingsgrensesnittet.
author: ruhercul
ms.date: 01/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ac3facacd95e5e677635cb037d0d3458da612410
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005713"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Opprette en arbeidsnedbrytningsstruktur (WBS)

En prosjektplan kommuniserer hvilke oppgaver som må fullføres, hvilke ressurser som skal utføre arbeidet, og tidsrammen som arbeidet må fullføres i. Planen gjenspeiler alt arbeidet som er forbundet med å levere prosjektet i tide. I Dynamics 365 Project Operations oppretter du en prosjektplan basert på følgende:

  - Oppdeling av arbeidet i håndterbare oppgaver.
  - Beregning av tiden som kreves for å utføre hver oppgave.
  - Angivelse av oppgaveavhengigheter.
  - Angivelse av oppgavevarigheter.
  - Beregning av de generelle ressursene som skal utføre oppgavene. 

Prosjektplanen opprettes i kategorien **Plan** på siden **Prosjekt**.

## <a name="tasks"></a>Oppgaver

Det første trinnet i prosessen med å opprette en prosjektplan er å dele opp arbeidet i håndterbare deler. Tidsplanen i Project Operations støtter følgende funksjoner:

- Hovedaktiviteter eller beholderoppgaver
- Bladnodeoppgaver

### <a name="summary-tasks"></a>Sammendragsoppgaver

Sammendragsoppgaver kan lagre andre sammendragsoppgaver eller bladnodeoppgaver. De har ingen arbeidsinnsats eller kostnad alene. I stedet er arbeidsinnsatsen og kostnaden en beregning av arbeidsinnsatsen og kostnadene for de tilhørende beholderoppgavene. Startdatoen for hovedoppgaven er startdatoen for beholderoppgavene, og sluttdatoen er sluttdatoen for beholderoppgavene. Navnet på en hovedoppgave kan redigeres, men planleggingsegenskaper, inkludert innsats, datoer og varighet, kan ikke redigeres. Hvis du sletter en hovedoppgave, slettes også alle beholderoppgavene.

### <a name="leaf-node-tasks"></a>Bladnodeoppgaver

Bladnodeoppgaver representerer det mest detaljerte arbeidet på prosjektet. De har en beregnet arbeidsinnsats, ressurser, planlagte start- og sluttdatoer og en varighet.

## <a name="create-a-task-hierarchy"></a>Opprette et oppgavehierarki

### <a name="add-a-task"></a>Legge til oppgaver

Du legger til én eller flere oppgaver ved å fullføre følgende trinn.

1. Gå til **Prosjekter** og velg og åpne prosjektoppføringen du vil opprette en tidsplan for. 
2. Velg kategorien **Oppgaver**. 
3. Velg **Legg til ny oppgave**, angi et navn på oppgaven, og trykk deretter på ENTER.
2. Skriv inn et nytt oppgavenavn, og trykk på ENTER på nytt til du har en fullstendig oppgaveliste.

### <a name="manage-hierarchy-of-a-task"></a>Administrere hierarki for en oppgave

Når en oppgave er rykket inn, blir den underordnet oppgaven som er rett over den. Tidsplan-ID-en for oppgaven beregnes deretter på nytt, slik at den er basert på tidsplan-ID-en til den nye overordnede oppgaven, og følger disposisjonsnummereringen. Den overordnede oppgaven er nå et sammendragsoppgave. Det blir derfor en fremheving av de underordnede oppgavene. Når en oppgave blir forfremmet, er den ikke lenger en underordnet oppgave som var dens overordnede. Tidsplan-ID-en beregnes deretter på nytt slik at den gjenspeiler den oppdaterte dybden og posisjonen for oppgaven i hierarkiet. Innsats, kostnader og datoer for den forrige overordnede oppgaven beregnes på nytt, slik at de ikke inneholder denne oppgaven.

Du rykker inn eller forfremmer en oppgave ved å fullføre følgende trinn.

1. På siden **Prosjekt** i kategorien **Oppgaver** velger du de tre vertikale prikkene basert på oppgavenavn under **Sammendragsoppgaver**, og deretter velger du **Lag deloppgave**. 
2. Velg oppgaven du vil rykke inn eller forfremme. Hvis du vil velge mer enn én oppgave, velger du en oppgave, trykker på og holder nede Ctrl, og deretter velger du flere oppgaver.
2. Velg **Rykk inn** eller **Forfrem deloppgave** for å flytte oppgaver under eller ut fra under sammendragsoppgavene.

### <a name="move-tasks-up-and-down"></a>Flytte oppgaver opp og ned

Oppgaver kan flyttes til et hvilket som helst nivå i strukturen for arbeidsstruktur på én av to måter:

- Velg én oppgave til, og dra dem til ønsket plassering.
- Velg en eller flere oppgaver, høyreklikk og velg **Klipp ut**, velg målcellen i tidsplanen, høyreklikk og velg deretter **Lim inn**.

## <a name="task-attributes"></a>Oppgaveattributter

Et oppgavenavn beskriver arbeidet som må fullføres. I Project Operations er attributtene som er knyttet til en oppgave, en beskrivelse av tidsplanen til oppgaven og krav til bemanning.

## <a name="schedule-attributes"></a>Planlegge attributter

Attributtene **Innsats**, **Startdato**, **Sluttdato** og **Varighet** definerer tidsplanen for oppgaven.

Tabellen nedenfor viser flere tidsplanattributter.

| **Endelig visningsnavn** | **Endelig beskrivelse** |
| --- | --- |
| Innsats fullført (timer) | Fullført arbeid for oppgaven i timer. |
| Varighet | Viser varigheten for oppgaven i dager. |
| Total innsats | Totalt arbeid for oppgaven i timer. |
| Overflate | Sluttdato og -tidspunkt. |
| % fullført | Prosentandelen av oppgaven som er fullført. |
| Prosjektsamling | Oppgavetavlen kan grupperes etter samling, slik at hver samling har sin egen kolonne. |
| Gjenværende innsats (timer) | Gjenstående arbeid for oppgaven i timer. |
| Starter | Startdato og -tidspunkt. |
| Navn | Navnet på oppgaven. |
| ID | ID-en for oppgaven i arbeidsnedbrytningsstrukturen. |

Som en administrator kan du definere egendefinerte felter for oppgaveenheten. Feltene kan imidlertid ikke vises i tidsplanrutenettet. Hvis du vil vise de egendefinerte feltene, legger du dem til på detaljsiden for **Prosjektoppgave**.

## <a name="staffing-attributes"></a>Bemanningsattributter

Du får tilgang til attributter for bemanning via **Ressurser**-feltet i tidsplanen. Du kan søke etter en eksisterende ressurs, eller velge **Opprett** og legge til et prosjektteammedlem som en ny ressurs i **Hurtigoppretting**-ruten.

Feltene **Rolle**, **Ressursenhet** og **Stillingsnavn** brukes til å beskrive bemanningskravene for oppgaven. Disse bemanningsattributtene sammen med oppgaveplanen brukes til å finne tilgjengelige ressurser for denne oppgaven.

   - **Rolle**: Angi ressurstypen som kreves for å utføre oppgaven.
   - **Ressursenhet**: Angi enheten som ressursene for oppgaven skal tilordnes fra. Dette attributtet har innvirkning på kostnads- og salgsberegningen for oppgaven hvis kostnads- og fakturasatsen for ressursen er angitt basert på ressursenheter.
   - **Stillingsnavn**: Angi et navn for den generelle ressursen som fungerer som en plassholder for ressursen som til syvende og sist kommer til å utføre arbeidet.

**Ressurser**-feltet inneholder stillingsnavnet til den generelle ressursen eller den navngitte ressursen når en slik finnes.

**Kategori**-feltet inneholder verdier som angir en bredere arbeidstype som oppgaven kan grupperes i. Dette feltet har ikke innvirkning på planlegging eller bemanning. Feltet brukes i stedet bare til rapportering.

## <a name="task-dependencies"></a>Oppgaveavhengigheter

Du kan bruke tidsplanen i Project Operations til å opprette foregående relasjoner mellom aktiviteter. Feltet **Foregående** bruker én eller flere verdier til å angi oppgavene som en oppgave avhenger av. Når foregående verdier tilordnes til en oppgave, kan oppgaven bare starte etter at alle de foregående oppgavene er fullført. På grunn av avhengigheten tilbakestilles planlagt startdato for oppgaven til datoen når de foregående oppgavene er fullført.

Oppgavemodusen har ingen innvirkning på oppdateringer som utføres på start- og sluttdatoene for foregående/avhengige oppgaver.

## <a name="accessibility-and-keyboard-shortcuts"></a>Tilgjengelighet og hurtigtaster

Rutenettet **Tidsplan** er fullt tilgjengelig og kan brukes med skjermlesere, for eksempel Narrator, JAWS eller NVDA. Du kan bla gjennom rutenettområdet ved hjelp av piltastene (som i Microsoft Excel), du kan bruke TAB-tasten til å gå gjennom de interaktive brukergrensesnittelementene, og du kan bruke pil ned-tasten, ENTER-tasten eller mellomromstasten til å velge og åpne rullegardinmenyene.


[!INCLUDE[footer-include](../includes/footer-banner.md)]