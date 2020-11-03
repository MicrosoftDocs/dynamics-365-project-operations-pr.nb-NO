---
title: Opprette egendefinerte felt og enheter
description: Dette emnet forklarer hvordan du oppretter alternativsett og enheter i din egen løsning på Power Apps-plattformen.
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
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081689"
---
# <a name="create-custom-fields-and-entities"></a>Opprette egendefinerte felt og enheter 

Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet på Power Apps-plattformen.  
Fremgangsmåtene i dette emnet bør fullføres ved hjelp av nettgrensesnittet i PSA (Project Service Automation).

> [!IMPORTANT]
> Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning. Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst. Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon

En prisdimensjon kan være et alternativsett eller en enhet. Begge må opprettes i prisløsningen. Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.

### <a name="entity-based-dimensions"></a>Enhetsbaserte dimensjoner

1. I PSA klikker du på **Innstillinger** > **Løsninger** og dobbeltklikker deretter på **\<your organization name>-prisdimensjoner**.
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.
3. Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**. Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Standard enhetsdefinisjon for tittel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Alternativsettbaserte dimensjoner 
Du kan opprette to alternativsettbaserte dimensjoner. Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet** , og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.


1. I PSA klikker du på **Innstillinger** > **Løsninger** og dobbeltklikker deretter på **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**. 
3. Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Opprette data for enhetsbaserte dimensjoner

Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel. Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør** , fra den enhetsbaserte dimensjonen **Standardtittel**. Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.

1. Klikk **Avansert søk** i PSA. Velg enheten **Standardtittel** , og klikk deretter **Resultater**. Alle radene i enheten **Standardtittel** vises.
2. Klikk **Ny**. I **Navn** -feltet angir du "Systemingeniør" og klikker deretter **Lagre**.
3. Lukk skjemaet. 
4. Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".

> ![Eksempeldata for enheten Standardtittel ](media/ST-data.png)

