---
title: Opprette egendefinerte felt og enheter
description: Dette emnet forklarer hvordan du oppretter alternativsett og enheter i din egen løsning på Power Apps-plattformen.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754181"
---
# <a name="create-custom-fields-and-entities"></a>Opprette egendefinerte felt og enheter 

Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet på Power Apps-plattformen.  
Fremgangsmåtene i dette emnet bør fullføres ved hjelp av nettgrensesnittet i PSA (Project Service Automation).

> [!IMPORTANT]
> Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning. Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst. Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Opprette en egendefinert løsning for prisdimensjoner
1. I PSA klikker du **Innstillinger** > **Løsninger**, og deretter klikker du **Ny** for å opprette en ny løsning. 
2. Gi løsningen navnet **\<organisasjonsnavn> prisdimensjoner**, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Opprette en egendefinert løsning for prisdimensjoner](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon

En prisdimensjon kan være et alternativsett eller en enhet. Begge må opprettes i prisløsningen. Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.

### <a name="entity-based-dimensions"></a>Enhetsbaserte dimensjoner

1. I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**.
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.
3. Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**. Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Standard enhetsdefinisjon for tittel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Alternativsettbaserte dimensjoner 
Du kan opprette to alternativsettbaserte dimensjoner. Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet**, og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.


1. I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**. 
3. Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Opprette data for enhetsbaserte dimensjoner

Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel. Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**. Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.

1. Klikk **Avansert søk** i PSA. Velg enheten **Standardtittel**, og klikk deretter **Resultater**. Alle radene i enheten **Standardtittel** vises.
2. Klikk **Ny**. I **Navn**-feltet angir du "Systemingeniør" og klikker deretter **Lagre**.
3. Lukk skjemaet. 
4. Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".

> ![Eksempeldata for enheten Standardtittel ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Legg til alle nødvendige PSA-enheter og relaterte komponenter i prisdimensjonsløsningen
Du må legge til følgende Project Service-enheter i prisløsningen. Følg trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.

1. I PSA klikker du **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du **\<organisasjonsnavn> prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.
3. I dialogboksen **Løsningskomponenter** velger du følgende enheter:

- Faktisk
- Ressurs som kan reserveres
- Estimatlinje
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

4. Når du blir bedt om å inkludere avhengige enheter for enhetene som er valgt ovenfor, klikker du **Nei**.

> ![Ikke ta med alle relaterte komponenter](media/Do-not-include-required.png)


