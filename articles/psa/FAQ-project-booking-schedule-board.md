---
title: Opprette en prosjektbestilling fra planleggingstavlen
description: Dette emnet gir informasjon om hvordan du oppretter en prosjektestilling fra planleggingstavlen.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146540"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Opprette en prosjektbestilling fra planleggingstavlen

[!include [banner](../includes/psa-now-project-operations.md)]

Du kan reservere en ressurs til et prosjekt direkte fra kategorien **Team** i prosjektet eller ved å generere et ressurskrav fra en generell teammedlemstilordning og deretter oppfylle det genererte kravet med et prosjektteammedlem.

Du kan også bestille en ressurs til et prosjekt direkte fra planleggingstavlen. Du kan gjøre dette på tre måter:

- **Bestille fra et generert ressurskrav:** Du kan generere et ressurskrav etter at du har opprettet en generisk ressurs og tilordnet oppgaver i et prosjekt.

- **Bestille fra det primære kravet:** De primære kravene vises på planleggingstavlen i kategorien **Prosjekt**. 

- **Bestille fra et nytt ressurskrav:** Du kan opprette et ressurskrav fra grunnen av og knytte det til et prosjekt. På planleggingstavlen vises ressurskravet i **Åpne krav**-kategorien.

## <a name="book-from-a-generated-resource-requirement"></a>Bestille fra et generert ressurskrav

Du kan opprette en generell ressurs og tilordne den til én oppgave eller flere oppgaver i et prosjekt. Deretter kan du generere et ressurskrav fra det generelle teammedlemmet. 

1.  På planleggingstavlen vises denne ressursen i **Åpne krav**-kategorien. Du må kanskje bruke kolonnefiltre i rutenettet hvis du har mange åpne krav. 

    ![Kategorien Åpne krav på planleggingstavlen](media/FAQ-Project-Booking-Schedule-Board-1.png "Skjermbilde av tabell med bestillinger og tilordninger")

2. Velg kravet. **Søk etter tilgjengelighet**-kategorien vises øverst i den valgte raden.
 
3. Når du velger kategorien, åpnes modusen Planleggingsassistent på planleggingstavlen og filtrerer de tilgjengelige ressursene som oppfyller ressurskravet. Deretter kan du bestille en ressurs.

4. Du kan også dra og slippe valgt rad fra bunnen av planleggingstavlen til en ressurscelle i rutenettet ovenfor. Når du slipper det, åpner **Opprett ressursbestilling**-panelet til høyre.

    Valg av **Bestill** bestiller ressursen til prosjektteamet.

![Panel for å opprette ressursbestilling](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Bestille fra det primære kravet

Når du oppretter et prosjekt i Project Service, opprettes automatisk et ressurskrav kalt primærkrav. Dette er et tomt krav som brukes til å bestille raskt en ressurs med planleggingstavlen uten å generere et krav eller opprette ett helt forfra. Fordi kravet er tomt, må du angi datoer samt tildelingsmetode og timer hvis det er aktuelt. 

1. Hvis du vil bestille en ressurs med primærkravet, velger du **Prosjekt**-kategorien på planleggingstavlen. Det kan hende du må bruke kolonnefilteret i **Prosjekt**-kolonnen hvis du har mange prosjekter.

   ![Kolonnefiltre på planleggingstavlen](media/FAQ-Project-Booking-Schedule-Board-2.png "Skjermbilde av tabell med bestillinger og tilordninger")

2. Velg kravet som bare har prosjektnavnet som navn, og som har en varighet på null (0).

3. Velg **Søk etter tilgjengelighet**-kategorien som vises i raden. Dette setter planleggingstavlen i modusen Planleggingsassistent og viser tilgjengelige ressurser som kan bestilles på prosjektet.

4. Siden et **primærkrav** er et tomt krav med null (0) varighet, må du angi varigheten i **Opprett ressursbestilling**-panelet når du velger og bestiller en ressurs.

5. Du kan også velge **primærkravet for prosjektet** nederst på planleggingstavlen og dra og slippe det på en ressurs for å bestille den.
 
    Siden **primærkravet** er et tomt krav med null (0) varighet, må du angi varigheten i **Opprett ressursbestilling**-panelet når du velger og bestiller en ressurs.
 
    Når du bestiller en ressurs gjennom **primærkravet på planleggingstavlen**, kan du legge den til prosjektteamet uten tilordninger.
 
## <a name="book-from-a-new-resource-requirement"></a>Bestille fra et nytt ressurskrav
Fullfør fremgangsmåten nedenfor for å bestille fra et nytt ressurskrav. 

1. Gå til **Ressurskrav** og velg deretter **Ny** for å opprette et nytt ressurskrav.

2. Velg et prosjekt i kategorien **Prosjekt** for å knytte behovet til prosjektet.
 
    På planleggingstavlen vises dette nylig opprettede kravet som et **åpent krav** som du kan fullføre.

3. Bestill ressursen for å legge den til i prosjektteamet.

4. Nå som ressursen er bestilt, må du tilordne oppgaver manuelt.

