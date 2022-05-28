---
title: Opprette egendefinerte felt og enheter som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter egendefinerte alternativsett eller enheter.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 4912087d7a19f5f342beff94723acd6131ce2dd8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580698"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Opprette egendefinerte felt og enheter som prisdimensjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Fullfør fremgangsmåten nedenfor når du vil opprette et egendefinert alternativsett eller enhet for å bruke det/den som en prisdimensjon. Hvis du vil ha mer informasjon, kan du se [Overskikt over prisdimensjoner](pricing-dimensions-overview.md).  

> [!IMPORTANT]
> Vi anbefaler at du gjør alle egendefinerte endringer i prisdimensjonen i en separat løsning. Denne anbefalte fremgangsmåten gir deg fleksibilitet i fremtiden for å oppdatere eller fjerne endringer etter behov. Dette hjelper deg også med å bruke arbeidet på nytt og gjør det enklere å overføre disse endringene til en annen forekomst etter at du har gjort alle de nødvendige endringene, eksportere denne løsningen som en **Administrert løsning** og importere den til andre forekomster for å bruke prisoppsettet på nytt.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Opprette egendefinerte felt og alternativsett i løsningen for prisdimensjon

En prisdimensjon kan være et alternativsett eller en enhet. Begge må opprettes i prisløsningen. Fremgangsmåten i denne prosedyren forklarer hvordan du oppretter enhetsbaserte dimensjoner og alternativsettbaserte dimensjoner.

### <a name="entity-based-dimensions"></a>Enhetsbaserte dimensjoner
Følg denne fremgangsmåten for å opprette enhetsbaserte dimensjoner:

1. Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter**.
3. Klikk **Ny** for å opprette en ny enhet kalt **Standardtittel**. 
4. Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Standard enhetsdefinisjon for tittel.](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Alternativsettbaserte dimensjoner 
Du kan opprette to alternativsettbaserte dimensjoner. 

- Bruk **Arbeidssted for ressurs** til å spore prisen på **Hjem**-lokasjonsarbeid og **På stedet**-arbeid. 
- Bruke **Arbeidstimer for ressurs** med verdiene **Vanlig** og **Overtid** for å bruke et påslag når arbeidet er ferdig.

Følgende grafikk gir en visning av **Arbeidssted for ressurs**-dimensjonen. 

> ![Alternativsettbasert prisdimensjon kalt Arbeidssted for ressurs.](media/Option-set-PD-called-Resource-Work-Location.png)

Følgende grafikk gir en visning av **Arbeidstimer for ressurs**-dimensjonen. 

> ![Alternativsettbasert prisdimensjon kalt Arbeidstimer for ressurs.](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Gå til **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Alternativsett**. 
3. Klikk **Ny** for å opprette et nytt alternativsett, angi den gjenstående nødvendige informasjonen, og klikk deretter **Lagre**.

## <a name="create-data-for-entity-based-dimensions"></a>Opprette data for enhetsbaserte dimensjoner

Du kan opprette data for en enhetsbasert dimensjon manuelt eller ved å bruke import- eller servicekall i Microsoft Excel. Følg trinnene i denne prosedyren for å opprette to standardtitler, **systemingeniør** og **overordnet systemingeniør**, fra den enhetsbaserte dimensjonen **Standardtittel**. Hvis dataene du vil opprette, er små, som i følgende eksempel, kan du bruke et standardskjema.

1. Velg **Avansert søk**.
2. Velg enheten **Standardtittel**, og velg deretter **Resultater**. Alle radene i enheten **Standardtittel** vises.
3. Velg **Ny**, angi "Systemingeniør" i **Navn**-feltet og velg deretter **Lagre**.
4. Lukk siden. 
5. Gjenta trinn 1-3 for å opprette en ny standardtittel for "Overordnet systemingeniør".

> ![Eksempeldata for enheten Standardtittel.](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]