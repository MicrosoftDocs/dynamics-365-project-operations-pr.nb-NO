---
title: Opprette egendefinerte løsninger for prisdimensjoner
description: Dette emnet forklarer hvordan du oppretter en egendefinert løsning når du oppretter egendefinerte prisdimensjoner.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081629"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Opprette egendefinerte løsninger for prisdimensjoner

> [!IMPORTANT]
> Alle egendefinerte endringer i prisdimensjonen må være i en egen løsning. Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst. Når du har gjort de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.

1. Velg **Innstillinger** > **Løsninger** , og velg deretter **Ny**. 
2. Gi løsningen navnet **\<your organization name>-prisdimensjoner** , angi den gjenstående nødvendige informasjonen, og velg deretter **Lagre**.

> ![Opprette en egendefinert løsning for prisdimensjoner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen
Du må legge til følgende Project Service-enheter i prisløsningen. Fullfør trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.

1. Velg **Innstillinger** > **Løsninger** , og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.
3. I dialogboksen **Løsningskomponenter** velger du følgende enheter:

- Faktisk
- Ressurs som kan reserveres
- Estimatlinje
- Prosjektoppgave
- Fakturalinjedetalj
- Journallinje
- Detalj for prosjektkontraktlinjer
- Prosjektteammedlem
- Tilbudslinjedetalj
- Rolleprispåslag
- Rollepris 
- Tidsoppføring 

> ![Legg til eksisterende enheter i prisdimensjonsløsningen](media/Existing-entities-to-PD-solution.png)

> ![Velg løsningskomponenter](media/Dimension-Components.png)

> [!NOTE]
> Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.

4. Når du blir bedt om å inkludere avhengige enheter for de valgte enhetene, klikker du **Nei**.

> ![Ikke ta med alle relaterte komponenter](media/Do-not-include-required.png)


