---
title: Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver
description: Dette emnet gir informasjon om hvordan du bestiller navngitte ressurser for prosjektteam og tilordner dem til oppgaver.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: cdbcd84d2277ba1c8e68270d5b1f8ca45c17f05e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575362"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Bestille navngitte bestillbare ressurser til et prosjektteam og tilordne oppgaver 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan legge til en navngitt ressurs i prosjektteamet ved å reservere den direkte til teamet. Det gjør du ved å følge denne fremgangsmåten:

1. Gå til **Prosjekter** i Project Service Automation, og velg det åpne prosjektet du bestiller for.
2. På **Prosjekt**-siden i **Team**-kategorien klikker du **Ny**. 

![Legge til et teammedlem fra fanen Team.](media/RM-how-to-1.png)

3. Velg den bestillbare ressursen i dialogboksen **Hurtigoppretting: Prosjektteammedlem**. **Rolle**-feltet fylles ut med ressursens standardrolle hvis en rolle er tilordnet. Du kan endre rollen etter behov. 
4. Velg fra- og til-datoene som ressursen trenger, og velg fordelingsmetoden for ressursens kapasitet. 
5. Hvis du vil at teammedlemmet skal være en prosjektgodkjenner, velger du **Ja** i feltet **Prosjektgodkjenner**. Dette betyr at teammedlemmet kan godkjenne sendte tids- og utgiftsoppføringer for dette prosjektet. 
6. Klikk **Lagre**.

![Legge til et team medlem i hurtigopprettingsskjemaet.](media/RM-how-to-2.png)


Nå kan du tilordne den bestilte ressursen til oppgaver i prosjektet. På **Prosjekt**-siden klikker du kategorien **Tidsplan** for å tilordne oppgaver til den nye ressursen. Ressursvelgeren som startes fra **Ressurser**-feltet i oppgaverutenettet, viser teammedlemmene som du kan velge.

![Tilordne et teammedlem til en oppgave i fanen Tidsplan.](media/RM-how-to-3.png)

I versjon 3 for Project Service automation (PSA) er ressursbestillinger og oppgavetildelinger ikke tett forbundet. Dette betyr at når du bruker ressursvelgeren i tidsplanen, kan du tilordne oppgaver til teammedlemmer for flere timer enn ordrene dekker på prosjektet.
Du kan se forskjellene mellom bestillinger og tildelinger for teammedlemmer i kategorien **Team** eller i kategorien **Ressursavstemming** . Du kan også avstemme forskjellene mellom bestillinger og tildelinger for ressurser på et mer detaljert nivå.

![Fanen Ressursavstemming.](media/RM-how-to-4.png)

Du kan også bruke ressursvelgeren i kategorien **Tidsplan** til å søke etter og velge bestillbare ressurser som ikke allerede er en del av prosjektteamet. Disse vises i ressursvelgeren som **Andre ressurser**.

![Tilordne en ressurs som ikke er medlem av et team, til en oppgave.](media/RM-how-to-5.png)

Når du gjør dette, legges ressursen til i prosjektteamet og tildeles oppgaven, men det genereres ingen bestillinger.

![Teammedlemmer med tilordninger og ingen bestillinger.](media/RM-how-to-6.png)

Du kan bruke funksjonen for å utvide bestillingen i kategorien **Avstemming** eller **planleggingstavlen** til å reservere ressursens kapasitet til prosjektet.

![Utvide bestillinger for et teammedlem i fanen Ressursavstemming.](media/RM-how-to-7.png)

Når et teammedlem er bestilt i prosjektet, kan du bruke vedlikehold av bestillinger, eller du kan bruke planleggingstavlen direkte til å behandle bestillingene.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
