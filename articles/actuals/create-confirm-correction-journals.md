---
title: Opprette og bekrefte korrigeringsjournaler
description: Denne artikkelen inneholder informasjon om hvordan du oppretter og bekrefter en korrigeringsjournal.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928076"
---
# <a name="create-and-confirm-correction-journals"></a>Opprette og bekrefte korrigeringsjournaler

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Fra tid til annen kan det hende at en tids- eller utgiftsoppføring angis feil. En konsulent kan for eksempel velge feil dato når de oppretter en tidsoppføring, eller de kan velge feil prosjekt når de oppgir en utgift. Hvis en konsulent ikke kan oppdatere de sendte oppføringene, kan en administrator i bakgrunnen korrigere de faktiske beløpene for et prosjekt direkte.

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

7. Når du har bekreftet korreksjonsjournalen, går du tilbake til prosjektet eller prosjektene du har oppdatert, for å vise endringene.

8. På prosjektsiden, på fanen **Faktiske verdier**, går du gjennom listen **Tilknyttet visning for faktiske data**. De opprinnelige oppføringene og de korrigerte oppføringene vises.


## <a name="correct-approved-material-usage-logs"></a>Korriger godkjente logger for materialbruk

Fullfør fremgangsmåten nedenfor for å korrigere én eller flere loggoppføringer for materialbruk.

1. I **Salgs**-området, i den venstre navigasjonsruten, under **Transaksjoner**, velger du **Faktiske verdier**.

2. I listen **Faktiske verdier** bruker du kolonnefiltre til å velge **Materiale**-transaksjonsklassen, slik at bare de faktiske verdiene for materialene vises. Bruk andre kolonnefiltre til ytterligere å begrense de faktiske beløpene som vises. Når du kan finne det ønskede settet med faktiske verdier, velger du de faktiske verdiene, og deretter velger du **Korriger oppføringer**. En ny korreksjonsjournal opprettes automatisk, og typen **Materialkorrigering** tilordnes.

3. På siden **Ny journal**, i **Beskrivelse**-feltet, skriver du inn en beskrivelse for korreksjonen. På fanen **Materialkorriger**, i delen **Nye verdier for materialer**, velger du deretter datafeltene som skal korrigeres for de valgte materiallinjene. Du kan for eksempel tilordne materialet til et annet prosjekt, eller korrigere produktet, materialdatoen eller underkontrakten.

4. Velg **Forhåndsvisning**. Velg deretter **OK** i dialogboksen.

5. Kontroller korrigeringene på fanen **Journallinjer**. Du kan vise en liste over de opprinnelige faktiske verdiene som er relatert til de valgte materialoppføringene som er reversert, og de korrigerte tilsvarende linjene som er opprettet.

6. Hvis de korrigerte verdiene er som forventet, velger du **Bekreft**. Velg deretter **OK** i dialogboksen. Hvis verdiene ikke er som forventet, velger du **Avbryt** for å gå tilbake til listen **Faktiske verdier**. Gjenta deretter trinn 2 til 5.

7. Når du har bekreftet korreksjonsjournalen, går du tilbake til prosjektet eller prosjektene du har oppdatert, for å vise endringene.

8. På prosjektsiden, på fanen **Faktiske verdier**, går du gjennom listen **Tilknyttet visning for faktiske data**. De opprinnelige oppføringene og de korrigerte oppføringene vises.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
