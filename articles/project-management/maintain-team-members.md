---
title: Opprettholde teammedlemmer
description: Dette emnet gir informasjon om bestilling av navngitte ressurser for prosjektteam og tilordne dem til oppgaver.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131535"
---
# <a name="maintain-team-members"></a>Opprettholde teammedlemmer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan legge til en navngitt ressurs i prosjektteamet ved å reservere den direkte til teamet.

1. I Dynamics 365 Project Operations går du til **Prosjekter**, og velg det åpne prosjektet du bestiller for.
2. På **Prosjekt**-siden i **Team**-kategorien velger du **Ny**. 
3. Velg den bestillbare ressursen i dialogboksen **Hurtigoppretting: Prosjektteammedlem**. **Rolle**-feltet fylles ut med ressursens standardrolle hvis en rolle er tilordnet. Du kan endre rollen. 
4. Velg fra- og til-datoene som ressursen trenger, og velg fordelingsmetoden for ressursens kapasitet. 
5. I feltet **Prosjektgodkjenner** velger du **Ja** hvis du vil at teammedlemmet skal være prosjektgodkjenner. Teammedlemmet kan godkjenne sendte tids- og utgiftsoppføringer for dette prosjektet. 
6. Velg **Lagre**.

Nå kan du tilordne den bestilte ressursen til oppgaver i prosjektet. På **Prosjekt**-siden, i kategorien **Tidsplan**, tilordner du oppgaver til den nye ressursen. Ressursvelgeren som startes fra **Ressurser**-feltet i oppgaverutenettet, viser teammedlemmene som du kan velge.


I Project Operations er ikke ressursbestillinger og oppgavetilordninger tett koblet sammen. Når du bruker ressursvelgeren i tidsplanen, kan du tilordne oppgaver til teammedlemmer for flere timer enn ordrene dekker på prosjektet.

Forskjellene mellom bestillinger og tildelinger for teammedlemmer vises i kategoriene **Team** og **Ressursavstemming**. Du kan også avstemme forskjellene mellom bestillinger og tildelinger for ressurser på et mer detaljert nivå.

Bruk ressursvelgeren i kategorien **Tidsplan** til å søke etter og velge bestillbare ressurser som ikke allerede er en del av prosjektteamet. Disse ressursene vises i ressursvelgeren som **Andre ressurser**.

Når du tar et valg, legges ressursen til i prosjektteamet og tildeles oppgaven, men det genereres ingen bestillinger.

Du kan bruke funksjonen for å utvide bestillingen i kategorien **Avstemming** eller **planleggingstavlen** til å reservere ressursens kapasitet til prosjektet.

Når et teammedlem er bestilt i prosjektet, kan du bruke **Vedlikehold bestillinger**, eller du kan bruke **planleggingstavlen** direkte til å behandle bestillingene.


[!INCLUDE[footer-include](../includes/footer-banner.md)]