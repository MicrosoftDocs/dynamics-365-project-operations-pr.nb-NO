---
title: Navigasjon i brukergrensesnittet
description: Dette emnet gir informasjon om prosjektledelse i Dynamics 365 Project-operasjoner.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ff624a13ec88ae64dba18715fbe9b94353b070e8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081538"
---
# <a name="navigating-the-user-interface"></a>Navigasjon i brukergrensesnittet

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

## <a name="overview"></a>Oversikt

Hovedprosjektskjemaet er delt inn i flere kategorier. Hver kategori representerer et forskjellig detaljnivå i prosjektet.

- **Sammendrag** : Gir en beskrivelse av prosjektet og aggregerer både planlagt og faktisk prosjekt ytelse.

    ![Kategorien Sammendrag og felt](media/navigation7.png)

- **Oppgaver** : Gir detaljer om arbeidsnedbrytningsstrukturen representert av en rutenettvisning, en tavlevisning og et Gantt-diagram.

    ![Kategorien Oppgave og felt](media/navigation8.png)

- **Team** : Inneholder detaljer om prosjektdeltakerne. Den tilordnede innsatsen for hvert teammedlem blir også oppsummert i denne visningen.

    ![Kategorien Team og felt](media/navigation9.png)

- **Ressurstilordninger** : Gir en tidsinndelt visning av innsatsen for hver ressurs i et prosjekt.

    ![Kategorien Ressurstilordninger og felt](media/navigation10.png)

- **Ressursavstemming** : Gir en tidsinndelt visning av forskjellene mellom tilordningene til hver navngitt ressurs og deres bestillinger.

    ![Kategorien Ressursavstemming og felt](media/navigation11.png)

- **Estimater** : Gir en tidsinndelt visning av kostnads- og salgsestimatene for et prosjekt.

    ![Kategorien Estimater og felt](media/navigation12.png)

- **Sporing** : Gir en visning som viser fremdriften for oppgaver i arbeidsnedbrytingsstrukturen for innsats, kostnad og salg.

    ![Kategorien Sporing og felt](media/navigation13.png)

- **Salg** : Inneholder dypkoblinger til tilbud og kontrakter som er knyttet til prosjektet.

- **Utgiftsestimater** : Gir et rutenett som definerer prosjektutgifter basert på organisatoriske utgiftskategorier.

    ![Kategorien Utgiftsestimater og felt](media/navigation14.png)

## <a name="grid-controls"></a>Rutenettkontroller

Nedenfor vises en kort oversikt over vanlige kontroller som finnes på de forskjellige prosjektplanleggingsfanene.

### <a name="refresh"></a>Refresh

**Oppdater** : Henter de nyeste dataene fra serveren hvis det har oppstått endringer etter at rutenettet ble lastet inn.

![Oppdater-knapp](media/navigation7.png)

### <a name="group-by"></a>Grupper etter

**Grupper etter** : Oppdaterer grupperingen av radene i rutenettet for å gjenspeile enten ressurser, roller eller kategorier basert på brukerens behov.

![Grupper etter-knappen](media/navigation6.png)

### <a name="previousnext"></a>Forrige/Neste

**Forrige**/**Neste** : Oppdater de synlige tidsperiodene i de tidsinndelte rutenettene.

![Knappene Forrige og Neste](media/navigation2.png)

### <a name="timescale"></a>Tidsskala

**Tidsskala** : Endre aggregasjonen til tidsinndelte data mellom dager, uker, måneder og år.

![Tidsskala-knappen](media/navigation3.png)

### <a name="expand"></a>Utvid

**Utvid** : Gjengir det synlige rutenettet i fullskjermmodus, og gir mer mulighet til å se flere roller.

![Utvid-knappen](media/navigation4.png)

### <a name="time-phase-by"></a>Tidsfase etter

**Tidsfase etter** : Oppdater grupperingen av radene i rutenettet for å gjenspeile kostnadsestimater for salgsestimater. Denne kontrollen gjelder også for estimatskriptet og rutenettet for sporing.

![Tidsfase etter-knappen](media/navigation0.png)

### <a name="add-column"></a>Legg til kolonne

**Legg til kolonne** : Gjør det mulig for brukeren å definere de synlige kolonnene i rutenettet. Bare medfølgende kolonner kan legges til i rutenettet på skjemaet **Prosjektplanlegging**.

![Legg til kolonne-knappen](media/navigation5.png)
