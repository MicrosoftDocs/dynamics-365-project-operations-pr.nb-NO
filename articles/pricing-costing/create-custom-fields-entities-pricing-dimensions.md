---
title: Opprette egendefinerte felt og enheter som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte alternativsett eller enheter.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081658"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Opprette egendefinerte felt og enheter som prisdimensjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet.

> [!IMPORTANT]
> Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning. Denne viktige fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov, den hjelper deg med å bruke arbeidet ditt, og det blir enklere å legge igjen disse endringene til en annen forekomst. Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **administrert løsning** og importerer den til andre forekomster for å bruke prisoppsettet på nytt.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Opprette en egendefinert løsning for prisdimensjoner
1. Gå til **Innstillinger** > **Løsninger** , og velg deretter du **Ny** for å opprette en ny løsning. 
2. Gi løsningen navnet **\<your organization name>-prisdimensjoner** , angi den gjenstående nødvendige informasjonen, og velg deretter **Lagre**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon

En prisdimensjon kan være et alternativsett eller en enhet. Begge må opprettes i prisløsningen. Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.

### <a name="entity-based-dimensions"></a>Enhetsbaserte dimensjoner

1. Gå til **Innstillinger** > **Løsninger** , og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.
3. Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**. 
4. Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.


### <a name="option-set-based-dimensions"></a>Alternativsettbaserte dimensjoner 
Du kan opprette to alternativsettbaserte dimensjoner. Bruk **Arbeidssted for ressurs** til å spore prisen på arbeid **hjemme** og **på stedet** , og bruk **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** til å bruke et påslag når arbeid er fullført.


1. Gå til **Innstillinger** > **Løsninger** , og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**. 
3. Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.

## <a name="create-data-for-entity-based-dimensions"></a>Opprette data for enhetsbaserte dimensjoner

Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel. Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør** , fra den enhetsbaserte dimensjonen **Standardtittel**. Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.

1. Velg **Avansert søk** , velg enheten **Standardtittel** , og velg deretter **Resultater**. Alle radene i enheten **Standardtittel** vises.
2. Velg **Ny** , angi "Systemingeniør" i **Navn** -feltet og velg deretter **Lagre**.
3. Lukk skjemaet. 
4. Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen
Du må legge til følgende enheter i prisløsningen. Følg trinnene i denne prosedyren for å gjøre noen viktige skjemaendringer i prisløsningen, slik at enhetene blir klar over de nye prisdimensjonene.

1. Velg **Innstillinger** > **Løsninger** , og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**. 
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


> [!NOTE]
> Pass på at du inkluderer alle skjemaer og visninger for hver av enhetene som er valgt.

4. Når du blir bedt om å inkludere avhengige enheter for enhetene som er valgt ovenfor, klikker du **Nei**.

