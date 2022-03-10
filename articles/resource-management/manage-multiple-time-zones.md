---
title: Administrere tidssoner
description: Når et prosjekt opprettes, er tidssonen basert på tidssonen som er definert i den brukte arbeidstidsmalen.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d3fc0453e3038839107a98c4179e6bd4aede95cf4a5fcfe2d52f823b83029485
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988708"
---
# <a name="manage-time-zones"></a>Administrere tidssoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


## <a name="projects"></a>Prosjekter

Når et prosjekt opprettes, er tidssonen basert på tidssonen som er definert i den brukte arbeidstidsmalen. I **prosjektet** er datoene alltid relative i forhold til tidssonen for brukeren som er logget på i hver kategori, med unntak av **Oppgave**-kategorien. Når du viser arbeidsnedbrytningsstrukturen, vises alltid datoene i tidssonen for prosjektet.

## <a name="tasks"></a>Oppgaver

Når du oppretter en oppgave, kontrolleres start- og sluttidspunktet og timene/dagen etter arbeidstiden til prosjektet. Hvis en oppgave for eksempel er opprettet med et prosjekt der tids sonen er -8 PST, og har følgende arbeidstid: 09:00 til 17:00 mandag til fredag, vil alle oppgaver som er opprettet uten en tilordning, respektere start- og sluttidspunktet for prosjektkalenderen.

## <a name="manage-resources-with-time-zones"></a>Administrere ressurser med tidssoner

For å få nøyaktige og forutsigbare resultater når du bruker **Utvid bestilling**, er det to viktige krav som må oppfylles:  

- Brukeren må konfigurere tidssonen for enheten slik at den samsvarer medtids sonen som er angitt i systemets **tilpassingsinnstillinger**.
 
  ![Tidssoneinnstillinger i Windows 10.](media/reconcile-assignments-03.png)

  ![Tidssoneinnstillinger i innstillinger for personalisering.](media/reconcile-assignments-04.png)
 
- Ressursen som kan bestilles, må ha minst ett minutt med arbeidstid som overlapper med konturene som brukes til å definere den ønskede utvidelsen. Eksempel: Følgende ressurser med arbeidstid som faller mellom 09:00 og 19:00. 

  ![Sammenligning av ressursomfang.](media/reconcile-assignments-05.png)

Følgende tabell viser:

- En prosjektkalendermal
- Ressurs A: Denne ressursen har samme kalender og er i samme tidssone som prosjektet. Starttidspunktet for bestillinger blir kl. 9:00.
- Ressurs B: Denne ressursen befinner seg i en annen tidssone enn prosjektet, og starter 07:00 i sin tidssone. Imidlertid vil bestillinger starte på 9:00 som det første starttidspunktet for tilordningsomfanget.
- Ressurs C og D: Ressursene befinner seg i andre tidssoner, begge forskjellige fra hverandre og prosjektet, og bestillinger startes ikke tidligere enn de respektive starttidspunktene som er tilgjengelige.

|Entity  |Kalender  |
|-|-|
|Prosjektkalendermal   | ![prosjektkalender.](media/reconcile-assignments-06.png) |
|Ressurs A  | ![Ressurs A-kalender.](media/reconcile-assignments-06.png) |
|Ressurs B  |  ![Ressurs B-kalender.](media/reconcile-assignments-07.png) |
|Ressurs C  |  ![Ressurs C-kalender.](media/reconcile-assignments-08.png) |
|Ressurs D  | ![Ressurs D-kalender.](media/reconcile-assignments-09.png)  |
 
Når du navigerer til **Avstemming**-visningen, vises ressurstilordningene og de tilknyttede bestillingsmanglene.

![Avstemmingsvisning før utvidelse.](media/reconcile-assignments-10.png)

Etter at du har brukt funksjonen for å forlenge bestillingen til hver ressurs, blir alle bestillinger utvidet for hver ressurs, fordi arbeidstiden til hver ressurs overlappet med konturene av mangelen.

![Avstemmingsvisning etter bestillingsutvidelse.](media/reconcile-assignments-11.png) 

Legg merke til at en nærmere kikk på detaljene i bestillingene viser forskjeller i starttidspunktet for bestillingene. Bestillingene starter tidligst på starttidspunktet til tilordningsprofilen, og ikke senere enn den tilgjengelige starttiden til ressursen.

![Nye bestillinger for ressursene på planleggingstavlen.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]