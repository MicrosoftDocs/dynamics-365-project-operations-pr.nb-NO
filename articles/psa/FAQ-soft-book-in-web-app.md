---
title: Hvordan kan jeg foreta en ikke-forpliktende bestilling av ressurser i appversjon 2.x?
description: Denne artikkelen beskriver hvordan du kan foreta en ikke-forpliktende bestilling av prosjektteammedlemmer med Project Service.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9e5d1c91f8ea98117583996552c2f2834be9c537
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081643"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Hvordan kan jeg foreta en ikke-forpliktende bestilling av ressurser i webappen (Project Service-appen v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Du kan planlegge foreløpig eller foreta en ikke-forpliktende bestilling av en ressurs til et prosjektteam for å vise at du har planer om å tilordne ressursen til et prosjekt. Ikke-forpliktende bestillinger bruker ikke ressursens tilgjengelige kapasitet. Ikke-forpliktende bestilte teammedlemmer kan ikke tilordnes til prosjektoppgaver. Bare ressurser med statusen Forpliktende bestilling og utførelsestypen Dedikert kan tilordnes til oppgaver (forutsatt at de har nok timer for forpliktende bestilling som dekker tilordningsinnsatsen).

Ikke-forpliktende bestilte prosjektteammedlemmer vises i rutenettet Teammedlem der de ikke-forpliktende timene vises i kolonnen Ikke-forpliktende bestilling. De vises også på planleggingstavlen. Igjen så angir de ikke forbruk av kapasitet ettersom ikke-forpliktende bestilling ikke bruker kapasiteten til en ressurs.

Det finnes tre måter å foreta en ikke-forpliktende bestilling av et teammedlem til et prosjekt med Project Service versjon 2.x. Du kan foreta en ikke-forpliktende bestilling med planleggingstavlen,ved hjelp av funksjonen Vedlikehold bestillinger eller ved å opprette en generell ressurs. Disse metodene er beskrevet nedenfor.

## <a name="soft-book-with-the-schedule-board"></a>Foreta en ikke-forpliktende bestilling med planleggingstavlen

Hvis du skal foreta en ikke-forpliktende bestilling med planleggingstavlen, følger du denne fremgangsmåten: 
1. Åpne planleggingstavlen.
2. Velg kategorien Prosjekt nederst i Bestillingskrav-panelet på planleggingstavlen.
3. Finn prosjektet du vil foreta en ikke-forpliktende bestilling av en ressurs i. Hvis du har mange prosjekter, klikker du på kolonneoverskriften Prosjekt og bruker filteret for å finne prosjektet.
4. Klikk på prosjektet, og deretter drar og slipper du det på ressursens tidsrutenett.
5. Dette åpner Opprett ressursbestilling-panelet til høyre. Juster start- og sluttdatoen, velg bestillingsstatus som Ikke-forpliktende, og angi timene. 
6. Klikk på Bestill.
7. Tilbake i prosjektet vises nå ressursen som et teammedlem med timene med ikke-forpliktende bestilling i kolonnen Ikke-forpliktende bestilling.

Vær oppmerksom på at du ikke kan tilordne dem til oppgaver i arbeidsnedbrytningsstrukturen (WBS) ettersom ressurser må ha forpliktende bestilling i et team for å kunne tilordnes.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Forpliktende bestilling ved hjelp av funksjonen Vedlikehold bestillinger

Hvis du skal foreta en ikke-forpliktende bestilling med Vedlikehold bestillinger, følger du denne fremgangsmåten:
1. Klikk på Ny fra teammedlemsrutenettet.
2. Velg ressursen som kan reserveres, rolle, fra/til.
3. Velg en annen tildelingsmetode enn Ingen:
- Full kapasitet
- Kapasitet i prosent
- Etter timer - distribuer jevnt
- Etter timer - frontbelast
4. Klikk Lagre. Du kan se ressursen i teamrutenettet og timene deres angis som Forpliktende.
5. Vedlikehold ressursens bestillinger ved å klikke på Vedlikehold bestillinger.
6. Utvid ressursen når planleggingstavlen åpnes for å vise bestillingene. Du kan se bestillingen angitt som Forpliktende.
7. Høyreklikk på bestillingen og velg Ikke-forpliktende bestilling under Endre status, og deretter Ikke-forpliktende. Bestillingsstatusen er nå Ikke-forpliktende.
8. Når du har lukket planleggingstavlen, ser du at timene for ressursen er endret fra Forpliktende til Ikke-forpliktende i teammedlemsrutenettet.
Merk at hvis du foretar en forpliktende bestilling av en ressurs til teamet, og deretter tilordner dem oppgaver i WBS, når du bruker vedlikehold bestillinger til å endre status fra Forpliktende til Ikke-forpliktende, fjernes tilordningene fra oppgavene for denne ressursen ettersom bare ressurser med forpliktende bestilling kan tilordnes til oppgaver.

## <a name="soft-book-by-creating-a-generic-resource"></a>Foreta ikke-forpliktende bestilling ved å opprette en generell ressurs

Du kan opprette en ikke-forpliktende bestilling ved å generere et generelt ressursteammedlem, fullføre med planleggingstavlen eller ressursforespørselen og endre typen under bestillingen.
Bruk denne fremgangsmåten for å gjøre dette:

1. Tilordne roller til oppgavene du vil generere generiske teammedlemmer for, i prosjektets WBS.
2. Klikk på Generer prosjektteam.
3. I rutenettet for prosjektteammedlem velger du den generelle ressursen, og klikker på Bestill.
4. Velg ressursen du ønsker å reservere, på planleggingstavlen.
5. I Opprett ressursbestilling-panelet på planleggingstavlen endrer du bestillingsstatusen til Ikke-forpliktende.
6. Klikk på Bestill eller Bestill og avslutt.

Når du har lukket planleggingstavlen, ser du den valgte ressursen er lagt til teamet med timer med ikke-forpliktende bestillinger og tilordnede timer. Du kan også se at den generelle ressursen fortsatt er på teamet, som er en indikator på at oppgavene er tilordnet til et teammedlem med ikke-forpliktende bestilling.

Når du er klar til å endre en teammedlemsressurs med ikke-forpliktende bestilling til et teammedlem med forpliktende bestilling slik at du kan tilordne dem til oppgaver, gjør du følgende:

1. Velg ressursen, og klikk på Vedlikehold bestillinger.
2. Utvid ressursen når planleggingstavlen åpnes for å vise bestillingene. Du kan se bestillingen merket som Ikke-forpliktende.
3. Høyreklikk på bestillingen og velg Forpliktende bestilling under Endre status, og deretter Forpliktende. Bestillingsstatusen er nå Forpliktende.
4. Når du har lukket planleggingstavlen, ser du at timene for ressursen er endret fra Ikke-forpliktende til Forpliktende i teammedlemsrutenettet. Du kan nå tilordne ressursen til oppgaver (forutsatt at det er samsvar mellom timene med forpliktende bestilling og innsatstimene for oppgaven for tilordningen). Vær oppmerksom på at hvis du fulgte fremgangsmåten for generell ressursfullføring i nr. 3 ovenfor, og du endrer statusen for ressursen som kan bestilles med ikke-forpliktende bestilling, til forpliktende, fjernes det generelle teammedlemmet fra teamet.
