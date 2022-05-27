---
title: Foreta en ikke-forpliktende bestilling av en ressurs
description: Dette emnet inneholder informasjon om hvordan du kan planlegge løst eller foreta en uforpliktende bestilling av prosjektteammedlemmer.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7940409db69259785268778b6f6b0b67f4b2812d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577984"
---
# <a name="soft-book-a-resource"></a>Foreta en ikke-forpliktende bestilling av en ressurs

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Du kan planlegge foreløpig eller foreta en ikke-forpliktende bestilling av en ressurs til et prosjektteam for å vise at du har planer om å tilordne ressursen til prosjektet. Ikke-forpliktende bestillinger bruker ikke ressursens tilgjengelige kapasitet, og du kan tilordne ikke-forpliktende bestilte teammedlemmer til prosjektoppgaver. Fordi ikke-forpliktende bestillinger ikke bruker ressursens kapasitet, kan du fortsatt foreta forpliktende bestillinger av ressursen til andre oppgaver i samme periode. Ikke-forpliktende bestillinger kan ikke foretas på generelle ressurser. En ikke-forpliktende bestilling kan heller ikke fullføre en generell ressursforespørsel.

Ikke-forpliktende bestilte prosjektteammedlemmer vises i kategorien **Team** på **Prosjekt**-siden, der de ikke-forpliktende timene vises i kolonnen **Timer med ikke-forpliktende bestillinger** i visningen **Navngitte teammedlemmer**. Ikke-forpliktende bestilte prosjektteammedlemmer vises også på planleggingstavlen. Fordi de er bestilt uten forpliktelse, viser ikke planleggingstavlen noe forbruk av kapasitet for disse ressursene. Tid med ikke-forpliktende bestilling vises ikke i kategorien **Avstemming**, og vises heller ikke i feltet **Utvid bestillinger** i kategorien **Avstemming** på planleggingstavlen. 

Det er to måter å foreta en ikke-forpliktende bestilling av et teammedlem på til et prosjekt: direkte fra planleggingstavlen eller ved å legge til teammedlemmet i kategorien **Team**. 

## <a name="soft-book-from-the-schedule-board"></a>Foreta en ikke-forpliktende bestilling fra planleggingstavlen
Fullfør fremgangsmåten nedenfor for å foreta en ikke-forpliktende bestilling av en ressurs fra planleggingstavlen. 

1. Åpne planleggingstavlen, og gå deretter til panelet **Bestillingskrav** og velg kategorien **Prosjekt**.
2. Finn prosjektet der du vil foreta en ikke-forpliktende bestilling av en ressurs. Hvis det er et stort antall prosjekter i listen, velger du **Prosjekt**-kolonneoverskriften, og deretter bruker du filteret til å søke etter ett eller flere prosjekter.
3. Velg prosjektet, og deretter drar og slipper du det på ressursens tidsrutenett.
5. I panelet **Opprett ressursbestilling** justerer du start- og sluttdatoen, angir **bestillingsstatusen** til **Ikke-forpliktende** og angir deretter timene. 
6. Klikk på **Bestill**. Ressursen vises nå i **Team**-kategorien som en ressurs for prosjektet. Du kan se timene med ikke-forpliktende bestilling i kolonnen **Timer med ikke-forpliktende bestillinger** i visningen **Navngitte teammedlemmer**.

> [!NOTE]
> Du kan nå tilordne ikke-forpliktende bestillinger til oppgaver i kategorien **Plan**. I kategorien **Avstemming** viser ressursen et bestillingsunderskudd i forhold til oppgavetilordningen siden kategorien **Avstemming** bare vurderer forpliktende bestillinger. Du kan bruke funksjonen **Utvid bestillinger** for å foreta en forpliktende bestilling av ressursen for å unngå underskudd på forpliktende bestillinger mot ressurstilordningene. Du må avbryte manuelt den ikke-forpliktende bestillingen for ressursen ved hjelp av **Vedlikehold bestillinger**.

## <a name="soft-book-on-the-team-tab"></a>Foreta ikke-forpliktende bestilling i kategorien Team

Du kan legge til teammedlemmer direkte i kategorien **Team**, og endre deretter bestillingsstatusen fra **Forpliktende** til **Ikke-forpliktende** med **Vedlikehold bestillinger**. Når du legger til et teammedlem på denne måten, vil det alltid føre til en forpliktende bestilling hvis du ikke velger tildelingsmetoden **Ingen**.

Hvis du vil bruke denne metoden, må du utføre følgende trinn.

1. På **Prosjekt**-siden i **Team**-kategorien klikker du **Ny**.
2. Velg ressursen som kan reserveres, rollen og fra- og til-datoene.
3. Velg en annen tildelingsmetode enn **Ingen**.
4. Velg **Lagre**. Du kan se ressursen i rutenettet og timene deres i kolonnen **Timer med forpliktende bestillinger**.
5. Vedlikehold ressursens bestillinger ved å velge **Vedlikehold bestillinger**.
6. Utvid ressursen når planleggingstavlen åpnes for å vise bestillingene. Du kan se bestillingen angitt som **Forpliktende**.
7. Høyreklikk på bestillingen og under **Endre status** velger du **Ikke-forpliktende bestilling** \> **Ikke-forpliktende**. Bestillingsstatusen er nå **Ikke-forpliktende**.
8. Når du har lukket planleggingstavlen, ser du at timene for ressursen har flyttet fra kolonnen **Timer med forpliktende bestillinger** til **Timer med ikke-forpliktende bestillinger** i rutenettet **Team**, i visningen **Navngitte teammedlemmer**.

> [!NOTE]
> Når du bruker **Vedlikehold bestillinger** til å endre status fra **Forpliktende** til **Ikke-forpliktende**, og hvis du foretar en forpliktende bestilling av en ressurs til teamet, og deretter tilordner oppgaver til ressursen, beholdes oppgavetilordningene for denne ressursen. I kategorien **Avstemming** har ressursen imidlertid et bestillingsunderskudd ettersom bare forpliktende bestillinger vurderes ved avstemming av bestillinger kontra tilordninger. Du kan bruke funksjonen **Utvid bestillinger** i kategorien **Avstemming** for å foreta en forpliktende bestilling av ressursen for å unngå underskudd på forpliktende bestillinger mot ressurstilordningene. Du må avbryte den ikke-forpliktende bestillingen for ressursen ved hjelp av **Vedlikehold bestillinger**.

Når du er klar til å endre en teammedlemsressurs med ikke-forpliktende bestilling til et teammedlem med forpliktende bestilling, gjør du følgende:

1. Utvid ressursen på planleggingstavlen for å vise bestillingene. Du kan se bestillingen angitt som **Ikke-forpliktende**.
2. Høyreklikk på bestillingen og under **Endre status** velger du **Forpliktende bestilling** \> **Forpliktende**. Bestillingsstatusen er nå **Forpliktende**.
3. Når du har lukket planleggingstavlen og går tilbake til prosjektet og åpner kategorien **Team**, ser du at timene for ressursen har flyttet fra kolonnen **Timer med ikke-forpliktende bestillinger** til kolonnen **Timer med forpliktende bestillinger** i kategorien **Team**, i visningen **Navngitte teammedlemmer**. Hvis ressursen ble tilordnet til oppgaver, vil de ikke lenger vise et bestillingsunderskudd i kategorien **Avstemming** ettersom bestillingene nå er forpliktende.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
