---
title: Massekorrigeringer av faktiske verdier som er opprettet av godkjente tids- og utgiftsoppføringer
description: Denne artikkelen forklarer hvordan en administrator kan foreta enkeltkorrigeringer eller massekorrigeringer av tidligere godkjente tids- eller utgiftsoppføringer hvis faktureringen ikke er fullført.
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 82c9b38e4c79511fe3b6abfcb973fff8b56f1522
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916301"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Massekorrigeringer av faktiske verdier som er opprettet av godkjente tids- og utgiftsoppføringer

[!include [banner](../includes/psa-now-project-operations.md)]

Noen ganger kan en tids- eller utgiftsoppføring være angitt feil. En konsulent kan for eksempel velge feil dato ved oppretting av en tidsoppføring, eller de kan transponere tallene ved angivelse av en utgift. Hvis en konsulent ikke kan gjøre oppdateringene til de sendte oppføringene, kan en administrator direkte korrigere oppføringen for et prosjekt.

For å kunne fullføre fremgangsmåtene i denne artikkelen må du ha administratortillatelser.

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
