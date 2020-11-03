---
title: Tilordne generelt bestillbare ressurser til en oppgave og et prosjektteam
description: Dette emnet gir informasjon om bestilling av generelle ressurser for aktiviteter og prosjektteam.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081635"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tilordne generelt bestillbare ressurser til en oppgave og generere ressurskrav 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I tillegg til å bestille og tilordne navngitte eller faktiske ressurser i prosjektet kan du tilordne generelle ressurser til prosjektoppgaver. Disse ressursene kan fungere som plassholdere for navngitte ressurser til du er klar til å bemanne prosjektet med navngitte ressurser. 

1. I Project Service Automation (PSA) åpner du **Prosjekt** -siden, og i kategorien **Tidsplan** angir du posisjonsnavnet til den generelle ressursen i **Ressurs** -cellen i tidsplanen. Du kan også klikke **Ressurs** -ikonet i cellen for å åpne ressursvelgeren og deretter skrive inn navnet på den generelle ressursen du vil opprette.

![Opprette og tilordne et generelt teammedlem](media/RM-how-to-9.png)

Dette åpner panelet **Hurtigoppretting: Prosjektteammedlem**. 

2. Angi rollen og organisasjonsenheten for det generelle ressursteammedlemmet, og klikk deretter **Lagre**.

![Hurtigoppretting av generelt teammedlem](media/RM-how-to-10.png)

3. Når du har opprettet det nye medlemmet i det generelle ressursteamet, blir det tilordnet til oppgaven. Du kan fortsette å tilordne den generelle ressursen til andre oppgaver i oppgavetidsplanen.

![Tilordne eksisterende generelle teammedlemmer til oppgaver](media/RM-how-to-11.png)

4. Når du har tilordnet den generelle ressursen, kan du generere et ressurskrav og fullføre det ved å bestille eller sende en ressursforespørsel til en ressursleder direkte.

![Generere et krav for et generelt teammedlem](media/RM-how-to-12.png)

I rutenettet for teammedlemmer, i tillegg til å kunne bruke ressursvelgeren som nevnt ovenfor, kan du legge til generelle ressurser direkte. Ressursene legges til med et ressurskrav som er basert på start- og sluttdatoene og fordelingsmetoden som er angitt i panelet **Hurtigoppretting: Prosjektteammedlem**.

Du kan se en forskjell hvis du legger til det generelle teammedlemmet direkte og deretter tildeler flere oppgaver til den generelle ressursen enn antallet det er nødvendig å dekke. Klikk **Generer krav** for å generere kravet på nytt for å balansere de nødvendige timene mot tildelinger.

Du kan også klikke **Ressurskrav** -koblingen i rutenettet for teamet for å åpne kravet og legge til kvalifikasjoner, foretrukne ressurser og så videre.

![Ressurskrav](media/RM-how-to-13.png)
