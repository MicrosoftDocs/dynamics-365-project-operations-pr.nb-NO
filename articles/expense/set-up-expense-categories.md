---
title: Konfigurere utgiftskategorier
description: Dette emnet gir informasjon om hvordan du setter opp utgiftskategorier og delte kategorier for reiseregninger.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896698"
---
# <a name="set-up-expense-categories"></a>Konfigurere utgiftskategorier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når ansatte oppretter reiseregninger, må hver utgift som de registrerer, tilknyttes en utgiftskategori. Utgiftskategorier er avledet fra delte kategorier som kan deles på tvers av de juridiske enhetene i organisasjonen. Disse utgiftskategoriene kan også deles i andre områder, avhengig av hvordan organisasjonen er definert. Basert på definisjonen av organisasjonen og veiledning fra implementeringsteamet må du bestemme om kategoriene som brukes i utgiftshåndtering, bare skal brukes i utgiftshåndtering, eller om de skal deles i andre områder.

> [!NOTE]
> Disse kategoriene kan deles mellom prosjektstyring og regnskaps- og utgiftshåndtering, eller mellom prosjektledelsen og regnskap og produksjon. De kan imidlertid ikke deles mellom utgiftshåndtering og produksjon.

Før du kan starte oppsettsprosessen, må følgende avgjørelser tas for hver utgiftskategori:

- Hva er utgiftskategorien? Eksempler inkluderer kategorier for flyreiser, hotell eller kjørelengde.
- Kan utgiftskategorien også brukes til prosjektstyring og regnskap? I så fall må du også ta følgende beslutninger:

    - Hvilke kostnadskontoer skal brukes til følgende utgifter?

        - Kostnad
        - Lønnstildeling
        - VIA – kostverdi
        - Kostnadselement
        - VIA-kostnadsverdielement
        - Påløpt tap
        - VIA – påløpt tap

    - Hvilke omsetningskontoer skal brukes for følgende omsetningskilder?

        - Fakturert omsetning
        - Påløpt omsetning – Salgsverdi
        - VIA – Salgsverdi
        - Påløpt omsetning – produksjon
        - VIA – produksjon
        - Påløpt omsetning – fortjeneste
        - VIA – fortjeneste
        - Påløpt omsetning – abonnement
        - VIA – abonnement

- Hva er utgiftstypen?
- Hva er standard betalingsmetode for utgiftskategorien?
- Må utgifter i utgiftskategorien være spesifiserte?
- Hva er standard hovedkonto for utgiftskategorien?
- Hva er standard mva-gruppe for varesalg for utgiftskategorien?
- Er det tillatt med flere betalingsmetoder for utgiftskategorien? I så fall, hvilke?
- Finnes det underkategorier i utgiftskategorien? Hvis det finnes underkategorier, må du også ta følgende beslutninger:

    - Er noen av underkategoriene utelukket fra avgiftsfradrag?
    - Hva er mva-gruppen for varesalg for underkategoriene?
