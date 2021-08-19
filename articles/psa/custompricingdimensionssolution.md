---
title: Opprette egendefinerte løsninger for prisdimensjoner
description: Dette emnet forklarer hvordan du oppretter en egendefinert løsning når du oppretter egendefinerte prisdimensjoner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995278"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Opprette egendefinerte løsninger for prisdimensjoner

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Alle egendefinerte endringer i prisdimensjonen må være i en egen løsning. Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst. Når du har gjort de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.

1. Velg **Innstillinger** > **Løsninger**, og velg deretter **Ny**. 
2. Gi løsningen navnet **\<your organization name>-prisdimensjoner**, angi den gjenstående nødvendige informasjonen, og velg deretter **Lagre**.

> ![Opprette en egendefinert løsning for prisdimensjoner.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen
Du må legge til følgende Project Service-enheter i prisløsningen. Fullfør trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.

1. Velg **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**. 
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

> ![Legg til eksisterende enheter i prisdimensjonsløsningen.](media/Existing-entities-to-PD-solution.png)

> ![Velg løsningskomponenter.](media/Dimension-Components.png)

> [!NOTE]
> Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.

4. Når du blir bedt om å inkludere avhengige enheter for de valgte enhetene, klikker du **Nei**.

> ![Ikke ta med alle relaterte komponenter.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]