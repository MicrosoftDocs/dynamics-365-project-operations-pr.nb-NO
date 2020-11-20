---
title: Tilordne en ressurs til en oppgave
description: Dette emnet gir informasjon om hvordan du tilordner ressurser til oppgaver.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: b7aef799ec4b90d602a6f3641cbac06264664f00
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125145"
---
# <a name="assign-a-resource-to-a-task"></a>Tilordne en ressurs til en oppgave

Det er tre måter å tilordne en ressurs til en oppgave på i Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reserver en ressurs som et teammedlem og tilordne deretter ressursen til en oppgave

Du kan legge til en ressurs i prosjektteamet og deretter tilordne ressursen til oppgaver i prosjektplanen.

1. Legg til et nytt teammedlem ved å velge **Ny** i kategorien **Teammedlem**. 

2. Panelet for **hurtigoppretting av teammedlem** åpnes, der du kan velge navnet på ressursen som kan bestilles, og angi en rolle. 

    Velg én av følgende tildelingsmetoder for bestilling av ressursen:

    - **Full kapasitet** bestiller ressursens fulle kapasitet for de angitte fra- og til-datoene.
    - **Kapasitet i prosent** bestiller ressursen med en prosent av ressursens kapasitet for de angitte fra- og til-datoene.
    - **Etter timer - distribuer jevnt** bestiller ressursen for et bestemt antall timer og distribuerer dem jevnt per dag over de angitte fra-/til-datoene.
    - **Etter timer - frontbelast** bestiller ressursen for et bestemt antall timer og frontbelaster timene per dag over de angitte fra- og til-datoene.
    - **Ingen** legger til ressursen i teamet, men oppretter ikke en bestilling som absorberer kapasiteten deres.

3. I rutenettet **Planlegg** for en oppgave velger du **Ressurs**-ikonet i ressurscellen, og velger deretter teammedlemmet du akkurat la til, under **Teammedlemmer**. 

> [!NOTE]
> I kategorien **Teammedlem** og **Avstemming** viser ressursen bestilte timer og tilordnede timer. Timene børl være like, men behøver ikke være det ettersom bestillinger og tilordninger ikke er tett sammenknyttet. Kategorien **Avstemming** gir informasjon når de er forskjellige, for eksempel når du tilordner en ressurs flere timer enn du har bestilt. Om nødvendig kan du korrigere informasjonen ved å utvide ressursens bestillinger eller endre tilordningen.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Opprette et generelt teammedlem gjennom oppgavetilordning

Når du oppretter et generelt teammedlem via oppgavetildeling, oppretter du en plassholder eller en generell ressurs som beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene. Deretter genererer du et krav (eller sender en forespørsel ved hjelp av kravet) som brukes til å søke etter og reservere den navngitte ressursen.

1. I rutenettet **Planlegg** for en oppgave velger du **ressursikonet** i ressurscellen.

2. Skriv inn et navn som fungerer som plassholder for ressursens navn. For eksempel "Programleder".

3. Velg **Opprett**, og angi rollen for den generelle ressursen i feltet for **hurtigoppretting av prosjektteammedlem**.

4. Du kan fortsette å tilordne oppgaver til denne plassholderessursen ved å velge ressursen i **ressursvelgeren** for oppgaven. De er oppført under **Teammedlemmer**.

5. Når du er ferdig med å tilordne den generelle ressursen, velger du den generelle ressursen i kategorien **Team** og velger deretter **Generer krav** for å opprette et ressurskrav for den generelle ressursen.

6. Velg **Bestill** for den generelle ressursen. Du kan deretter bruke planleggingstavlen for å finne og bestille en virkelig ressurs. Du kan også sende kravet for fullføring av en ressursleder.

7. Når den generelle ressursen er fullført med en navngitt ressurs, fjernes den generelle ressursen fra teamet og oppgavetilordningene for den generelle ressursen tilordnes til den navngitte ressursen som fullførte ressurskravet for den generelle ressursen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilordne en navngitt ressurs fra listen over alle ressurser som kan reserveres

Du kan bruke søkeboksen i **ressursvelgeren** for å søke i alle ressursene som kan reserveres, og tilordne dem til en oppgave.

Ressurser som er tilordnet på denne måten, blir lagt til i teamet uten bestillinger. Dette ligner på å legge til et teammedlem og velge Ingen som tildelingsmetode. Ressursen vises i kategorien **Team** og kategorien **Avstemming** som ressurser med bare tilordninger og et bestillingsunderskudd. Reserver dem hvis du vil bruke tilgjengeligheten deres.

1. I rutenettet **Planlegg** for en oppgave velger du **ressursikonet** i ressurscellen.

2. Begynn å skrive inn et navn. Søkeresultater for navnet vises i **ressursvelgeren** under **Andre ressurser**.

3. Velg ressursen som du vil tilordne til oppgaven.

