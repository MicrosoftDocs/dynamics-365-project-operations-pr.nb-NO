---
title: Prosjektinnstillinger
description: Denne emnet gir informasjon om innstillinger for prosjektstyring.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: ca5fc63d56ddd84871949e38f421bcdfe38d478e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148160"
---
# <a name="project-settings"></a>Prosjektinnstillinger

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Bruk følgende innstillinger for å få tilgang til funksjonene for prosjektplanlegging.

## <a name="work-template"></a>Arbeidsmal

Hvis du vil opprette en prosjektplan, må du opprette en prosjektkalendermal som definerer antallet arbeidstimer for hver dag i tidsplanen og eventuelle tidspunkt selskapet holder stengt. Hvis du vil opprette en prosjektkalendermal, kan du knytte en arbeidsmal til **Kalendermal**-feltet for prosjektet. Følg denne fremgangsmåten for å opprette en arbeidsmal.

1. I PSA, den venstre navigasjonsruten, klikker du **Ressurser**. 
2. På **Ressurser**-listesiden åpner du en brukeroppføring og velger deretter **Vis arbeidstimer**.

  > [!NOTE]
  > Sørg for at du tillater popup-vinduer på nettlesersiden. På denne måten kan du se arbeidstimene som er angitt for ressursen.
  
3. I kategorien **Måndsvisning** klikker du **Konfigurer**. En liste med tre alternativer vises: 

  - Ny ukeplan
  - Arbeidstidsplan for én dag
  - Fritid

> ![Konfigurere salternativer](media/project-13.png)

4. Velg **Ny ukeplan**, og angi deretter alternativene for denne ressursplanen. Du kan angi en regelmessig ukeplan, daglige timeparametere, selskapet holder stengt, og så videre.
5. Angi datointervallet, velg **Lagre**, og klikk deretter **Lukk**. 
6. Gå tilbake til **Ressurser**-listesiden, og velg ressursen du angir arbeidstimer for. 
7. Velg **Angi kalender som** for å angi arbeidsmalen. 
8. Skriv inn et navn på arbeidsmalen i dialogboksen **Arbeidsmal**, og velg deretter **Bruk**. 

Du kan nå knytte arbeidsmalen til en prosjektkKalendermal.

## <a name="resource-roles"></a>Ressursroller

Begrepet *ressursrolle* viser til en rekke ferdigheter, kompetanser og sertifiseringer som en person må ha for å utføre et bestemt sett med oppgaver i et prosjekt. Med PSA kan du angi kostnader for og fakturere tiden til en ressurs basert på rollen som ressursen er tilknyttet. Alle organisasjoner må konfigurere disse rollene ved å bruke det venstre navigasjonsfeltet på **Project Service**-menyen.

Alle organisasjoner må konfigurere disse rollene på siden **Aktive ressurskategorier**. Hvis du vil åpne denne siden, velger du **Ressursroller** i den venstre navigasjonsruten.

## <a name="price-lists"></a>Prislister

Med prislister kan du angi kostpriser og salgspriser for ressursroller, utgiftskategorier, produkter og andre elementer i en organisasjon. Før du angir økonomiske estimater for arbeid som må leveres for et prosjekt, bør du opprette en støttekostnads- og salgsprisliste. I Parametere-delen bør du også konfigurere en standard kostnads- og salgsprisliste som gjelder for alle prosjekter som opprettes i organisasjonen. På siden **Aktive prosjektparametere** sørger du for at du angir en standard kostnads- og salgsprisliste.
