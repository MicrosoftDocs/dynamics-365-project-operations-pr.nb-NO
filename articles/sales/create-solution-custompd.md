---
title: Opprette en løsning for egendefinerte prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppretter løsninger for egendefinerte prisdimensjoner.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992218"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Opprette en løsning for egendefinerte prisdimensjoner

 _**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_ 

>[!IMPORTANT]
>Alle egendefinerte endringer i prisdimensjonen må være i en egen løsning. Denne anbefalte fremgangsmåten gir deg fleksibiliteten å oppdatere eller fjerne endringer etter behov, hjelper deg med å bruke arbeidet ditt om igjen, og gjør det enklere å overføre til andre forekomster. Når du har gjort alle de nødvendige endringene, eksporterer du denne løsningen som en **Administrert** løsning, og deretter importerer du den til andre forekomster for gjenbruk.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Opprette en løsning for egendefinerte prisdimensjoner

1.  Velg **Innstillinger** > **Løsninger**, og velg deretter **Ny**.
2.  Gi løsningen navnet *<your organization name>-prisdimensjonener*.
3. Angi resten av den nødvendige informasjonen, og klikk deretter **Lagre**.

  ![Opprette egendefinert prisdimensjonsløsninger.](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Legg til alle nødvendige enheter og relaterte komponenter i prisdimensjonsløsningen

Legg til følgende Project Service-enheter i prisløsningen for å gjøre viktige skjemaendringer i prisløsningen. Når du har fullført denne prosedyren, gjenkjenner enhetene de nye prisdimensjonene.

1.  Velg **Innstillinger** > **Løsninger**, og deretter dobbeltklikker du på **<*ditt organisasjonsnavn*> prisdimensjoner**.
2.  I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Legg til eksisterende** > **Enheter**.
3.  I dialogboksen **Løsningskomponenter** velger du følgende enheter:
 
   - **Faktisk**
   - **Ressurs som kan reserveres**
   - **Estimatlinje**
   - **Prosjektoppgave**
   - **Fakturalinjedetalj**
   - **Journallinje**
   - **Detalj for prosjektkontraktlinjer**
   - **Prosjektteammedlem**
   - **Tilbudslinjedetalj**
   - **Rolleprispåslag**
   - **Rollepris**
   - **Tidsoppføring**
 
   ![Legg til eksisterende egendefinerte løsninger for prisdimensjoner.](./media/Existing-entities-to-PD-solution.png)
 
 4. Du kan gjennomgå komponentene for hver enhet som blir lagt til, og den endelige listen over enhetsverdier for hver enhet. 

   >[!NOTE]
   > Inkluder alle skjemaer og visninger for hver av enhetene som er valgt.

  ![Enheter lagt til.](./media/solution-component-selection.png)


5.  Når du blir bedt om å inkludere avhengige enheter for de valgte enhetene, velger du **Nei, ikke ta med nødvendige komponenter.**

    ![Inkludere avhengige enheter.](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]