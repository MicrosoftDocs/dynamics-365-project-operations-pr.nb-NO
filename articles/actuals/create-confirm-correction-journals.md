---
title: Opprette og bekrefte korrigeringsjournaler
description: Dette emnet gir informasjon om hvordan du oppretter og bekrefter en korrigeringsjournal.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127775"
---
# <a name="create-and-confirm-correction-journals"></a>Opprette og bekrefte korrigeringsjournaler

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Noen ganger kan en tids- eller utgiftsoppføring være angitt feil. En konsulent kan for eksempel velge feil dato ved oppretting av en tidsoppføring, eller de kan transponere tallene ved angivelse av en utgift. Hvis en konsulent ikke kan gjøre oppdateringene til de sendte oppføringene, kan en administrator direkte korrigere oppføringen for et prosjekt.

Hvis du vil fullføre fremgangsmåtene i dette emnet, må du ha administratortillatelser.

## <a name="correct-approved-time-entries"></a>Korrigere godkjente tidsoppføringer     

Fullfør fremgangsmåten nedenfor for å rette én eller flere tidsoppføringer for et prosjekt.

1. I **Salg**-området velger du **Transaksjoner** og velger deretter **Godkjent tid**. 

2. I listen **Godkjent tid** finner og velger du én eller flere godkjente tidsoppføringer som skal korrigeres. Du kan bruke filteret til å finne relaterte oppføringer. Du kan for eksempel filtrere på en prosjekt-ID og velge alle godkjente tidsoppføringer med denne prosjekt-ID-en.

3. Velg **Korriger oppføringer**. En ny korrigeringsjournal opprettes automatisk med den angitte typen **Tidskorrigering**. Oppføringene du har valgt, blir lagt til i journalen. 

4. På siden **Ny journal** angir du en **beskrivelse** for korrigeringsjournalen, og deretter velger du kategorien **Korrigeringer for tidsoppføring**.  

5. I delen **Nye verdier for tidsoppføringer** oppdaterer du feltene med riktig informasjon etter behov. Du kan for eksempel endre det tilordnede prosjektet eller en ressurs som kan reserveres.

6. Velg **Forhåndsvisning**. Velg **OK** i dialogboksen. I kategorien **Journallinjer** kan du vise en liste over de opprinnelige faktiske verdiene som er relatert til de valgte tidsoppføringene som er tilbakeført, og de korrigerte tilsvarende linjene som er blitt opprettet. Hvis det skal utføres flere rettelser, gjentar du trinn 5 og 6. 

> [!NOTE]
> Alle de korrigerte faktiske verdiene vil ha samme verdier som du har valgt i delen **Nye verdier for tidsoppføringer**.

7. Hvis korrigeringene vises som forventet, velger du **Bekreft**. Velg **OK** i dialogboksen.

8. Gå tilbake til **Salg**-området, velg **Prosjekter**, og åpne deretter prosjektet som du akkurat oppdaterte tidsoppføringene for. 

9. På **Prosjekter**-siden i kategorien **Faktiske verdier** kan du vise endringene du har utført. 

> [!NOTE]
> Hvis kategorien **Faktiske verdier** ikke vises, velger du **Relatert** > **Faktiske verdier**.  

10. I listen **Tilknyttet visning for faktiske data** kan du se at de opprinnelige tidsoppføringene som er tilbakeført, fremdeles er oppført, og dette gjelder også for de tilsvarende korrigerte tidsoppføringene. 

I følgende grafikk er det for eksempel to linjeelementer med et antall på 8,00 som har debiteringer oppført i Beløp-kolonnen. I tillegg finnes det to linjeelementer med et antall på -8,00 som viser krediterte beløp i Beløp-kolonnen. Disse korrigeringene får antallet til å bli null.

 
## <a name="correct-approved-expense-entries"></a>Korrigere godkjente utgiftsoppføringer

Fullfør fremgangsmåten nedenfor for å korrigere én eller flere utgiftsoppføringer. 

1. I **Salg**-området, i den venstre navigasjonsruten, under **Transaksjoner**, velger du **Godkjente utgifter**.

2. I listen **Godkjente utgifter** velger du prosjektet du vil korrigere, og deretter velger du **Korriger oppføringer**. En ny korrigeringsjournal opprettes automatisk med den angitte typen **Utgiftskorrigering**. 

3. På siden **Ny journal** skriver du en **beskrivelse** for korrigeringen, og i kategorien **Utgiftskorrigering**, i delen **Nye verdier for utgifter** velger du datafeltene du vil korrigere for de valgte utgiftslinjene. Du kan for eksempel tilordne utgiften til et annet **prosjekt** eller korrigere verdiene for **Utgiftskategori**, **Utgiftsdato** eller **Ressurs som kan reserveres**.

4. Velg **Forhåndsvisning**. Velg **OK** i dialogboksen. 

5. Verifiser korrigeringene i kategorien **Journallinjer**. Du kan vise en liste over de opprinnelige faktiske verdiene som er relatert til de valgte utgiftsoppføringene som er tilbakeført, og de korrigerte tilsvarende linjene som er blitt opprettet.

6. Hvis de korrigerte verdiene er som forventet, velger du **Bekreft**. Velg **OK** i dialogboksen. Hvis verdiene ikke vises som forventet, velger du **Avbryt** for å gå tilbake til listen **Godkjente utgifter**. Gjenta trinn 2 til 5. 

> [!NOTE]
> De korrigerte faktiske verdiene vil ha samme verdier som du har valgt i delen **Nye verdier for utgifter**.

7. Etter at du har bekreftet korrigeringsjournalen, navigerer du tilbake til prosjektet eller prosjektene du oppdaterte, for å vise endringene.  

8. På prosjektsiden, i kategorien **Faktiske verdier**, går du gjennom **Tilknyttet visning for faktiske data**. De opprinnelige oppføringene og de korrigerte oppføringene vises. Følgende grafikk viser opprinnelige utgiftsoppføringsbeløp og tilhørende korrigerte utgiftsoppføringsbeløp. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]