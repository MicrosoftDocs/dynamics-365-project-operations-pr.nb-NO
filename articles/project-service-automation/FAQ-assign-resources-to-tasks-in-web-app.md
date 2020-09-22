---
title: Hvordan tilordner jeg en ressurs som kan reserveres, til en oppgave i nettappen
description: En oversikt over måtene du kan tilordne bestillbare ressurser på.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754212"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Hvordan tilordner jeg en ressurs som kan reserveres, til en oppgave i webappen (Project Service-appen v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Det er to måter å tilordne en ressurs til en oppgave på i Project Service. Du kan reservere en ressurs som et teammedlem og deretter tilordne den til en oppgave. Eller du kan opprette et generelt teammedlem gjennom rolletilordning i oppgaver, generere et team, og deretter oppfylle reservekravene med en navngitt ressurs.

Vær oppmerksom på at hvis du vil tilordne en ressurs som kan bestilles, til en oppgave, må ressursteammedlemmet som kan bestilles, ha nok tilgjengelige bestillinger. Statusen for bestillingen må være utførelsestypen Forpliktende bestilling og status Dedikert. Hvis det ikke er nok bestillinger for ressursen, fjerner Project Service tilordningen og viser følgende feilmelding:

*Kan ikke tilordne ressurs til oppgave - Følgende ressurs(er) har ikke tilstrekkelig antall timer reservert for dette prosjektet*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reserver en ressurs som et teammedlem og tilordne deretter ressursen til en oppgave

Med denne metoden kan du legge til en ressurs i prosjektteamet og deretter tilordne oppgaver til ressursen i prosjektplanen. Slik gjør du dette:
1.  Legg til et nytt teammedlem ved å velge **Ny** i teammedlemsrutenettet.
2.  Velg navnet på ressursen som kan bestilles, og angi en rolle i skjermbildet for hurtigoppretting av teammedlem.
3.  Velg **Fra**- og **Til**-datoer.

    > [!div class="mx-imgBorder"] 
    > ![Skjermbilde av å legge til teammedlem](media/FAQ-Resources-to-Tasks2-1.png "Skjermbilde av å legge til teammedlem")
 
4.  Velg én av følgende tildelingsmetoder for bestilling av ressursen:
    - **Full kapasitet** bestiller ressursens fulle kapasitet for de angitte fra- og til-datoene.
    - **Kapasitet i prosent** bestiller ressursen med en prosent av ressursens kapasitet for de angitte fra- og til-datoene.
    - **Etter timer - distribuer jevnt** bestiller ressursen for et bestemt antall timer og distribuerer dem jevnt per dag over de angitte fra- og til-datoene.
    - **Etter timer - frontbelast** bestiller ressursen for et bestemt antall timer og frontbelaster timene per dag over de angitte fra- og til-datoene.

    Ikke velg **Ingen** fordi den legger til ressursen i teamet, men oppretter ikke en bestilling som absorberer ressursens kapasitet.
5.  Velg **Lagre**.

    Vær oppmerksom på at timene i bestillingen må være nok til å dekke innsatstimene og datoområdene til oppgavene som du tilordner denne ressursen til. Hvis de ikke står i forhold til hverandre, kan du ikke tilordne ressursen til oppgaven.

6.  I arbeidsnedbrytningsstrukturen (WBS) for oppgaven klikker du rullegardinlisten for ressurscellen. Deretter: 

    1. Velg **Legg til**.
    2. Velg rullegardinlisten under **Ressurser**, og velg teammedlemmet du la til ovenfor.
    3. Velg **OK**. Teammedlemmet tilordnes nå til oppgaven.

    > [!div class="mx-imgBorder"] 
    > ![Skjermbilde av å legge til ressurser med WBS](media/FAQ-Resources-to-Tasks2-2.png "Skjermbilde av å legge til ressurser med WBS")
 
Du kan se aggregatet av ressursens tilordnede timer under Tilordnede timer i teammedlemsrutenettet Det blir mindre enn eller lik de bestilte timene for ressursen. 

> [!div class="mx-imgBorder"] 
> ![Skjermbilde av tilordnede timer for en ressurs](media/FAQ-Resources-to-Tasks2-3.png "Skjermbilde av tilordnede timer for en ressurs")
 
Hvis oppgaven du prøver å tilordne til ressursen, starter etter sluttdatoen for ressursbestillingene, vises ikke ressursen i rullegardinlisten.

Vær oppmerksom på at du kan tilordne en ressurs til flere timer enn de bestilte timene hvis ressursen har igjen noe ikke-tilordnet kapasitet. I dette tilfellet blir ressursen bare delvis tilordnet opptil bestillingene. Du kan se disse gjenværende ikke-tilordnede oppgavetimene ved å legge til kolonnen Timer uten bemanning i arbeidsnedbrytningsstrukturen.

Hvis ressurser tilordnes til deres bestilte timer (bestilte timer er lik tilordnede timer), ser du følgende feilmelding når du prøver å tilordne dem ytterligere oppgaver:

*Kan ikke tilordne ressurs til oppgave - Følgende ressurs(er) har ikke tilstrekkelig antall timer reservert for dette prosjektet.*

I tillegg legges standard teammedlem for prosjektleder som legges til teamet når du oppretter prosjektet, til uten noen bestillinger og kan ikke tilordnes til en oppgave. De vises ikke i ressursrullegardinlisten for oppgaver.

Hvis du vil tilordne denne ressursen, må du fjerne dem fra teamet, og deretter legge dem til på nytt med en annen tildelingsmetode enn Ingen. Årsaken til at de legges til teamet når prosjektet opprettes, er at et prosjekt har minst én prosjektgodkjenner som standard.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Opprette et generelt teammedlem gjennom rolletilordning på oppgaver

Denne metoden sikrer at ressursene har nok bestillinger for oppgaver. Først oppretter du en plassholder eller en generell ressurs som beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene, ved å generere et team etter at rollene er tilordnet til oppgavene. Slik gjør du dette:

1. Velg en oppgave i arbeidsnedbrytningsstrukturen.
2. Velg **Tilordnet rolle**-rullegardinlisteikonet i ressurscellen.
3. Velg **Rolle**-rullegardinlisten, og velg rollen for den generelle ressursen.
4. Velg **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Skjermbilde av å bruke WBS for å legge til ressurs](media/FAQ-Resources-to-Tasks2-4.png "Skjermbilde av å bruke WBS for å legge til ressurs")
 
Når du er ferdig med å tilordne roller til oppgavene i WBS, velger du **Generer prosjektteam**. Project Service oppretter minimum antall generelle teammedlemmer basert på rollene, ressursorganisasjonsenhetene og prosjektkalenderen ved å aggregere oppgavetilordningene.

> [!div class="mx-imgBorder"] 
> ![Skjermbilde av å generere prosjektteam](media/FAQ-Resources-to-Tasks2-5.png "Skjermbilde av å generere prosjektteam")
 
Du kan se ressurser av typen generell ressurs med rolle og stillingsnavn i Teammedlem-rutenettet. Hvis to ressurser kreves for en rolle for å fullføre arbeidet, oppretter funksjonen Generer team to teammedlemmer og bruker stillingsnavnet for å skille dem.

> [!div class="mx-imgBorder"] 
> ![Skjermbilde av å legge til to generelle ressurser](media/FAQ-Resources-to-Tasks2-6.png "Skjermbilde av å legge til to generelle ressurser")
 
Du kan åpne støtteressurskravet for det generelle teammedlemmet ved å velge koblingen under Ressurskrav.

> [!div class="mx-imgBorder"] 
> ![Skjermbilde av å åpne støtteressurskrav](media/FAQ-Resources-to-Tasks2-7.png "Skjermbilde av å åpne støtteressurskrav")

Velg **Bestill** for den generelle ressursen, og deretter kan du bruke planleggingstavlen for å finne og bestille en virkelige ressurs. Du kan også sende kravet for fullføring av en ressursleder ved å velge **Send forespørsel**.

Når den generelle ressursen er fullført med en navngitt ressurs, fjernes den generelle ressursen fra teamet og oppgavetilordningene for den generelle ressursen tilordnes til den navngitte ressursen som fullførte ressurskravet for den generelle ressursen.
 

