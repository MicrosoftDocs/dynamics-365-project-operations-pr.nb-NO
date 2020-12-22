---
title: Opprette en fakturaplan på en prosjektbasert kontraktlinje
description: Dette emnet gir informasjon om hvordan du oppretter fakturatidsplaner og milepæler på kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/17/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2fbec567c07d7567f1d133fa3512496039f16a1
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513936"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Opprette en fakturaplan på en prosjektbasert kontraktlinje 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Du kan opprette en fakturaplan på en prosjektbasert kontraktlinje. Fakturering er bare tillatt etter at kontrakten er vunnet, og når du oppretter en prosjektkontrakt. Ved hjelp av en fakturaplan kan du opprette fakturautkast for en prosjektbasert kontraktlinje automatisk. Hvis du imidlertid bare oppretter fakturaer manuelt, kan du hoppe over opprettelse av fakturaplaner på kontraktlinjer.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Opprette en fakturaplan for tid og materiale for en kontraktlinje

Når en prosjektbasert kontraktlinje har en faktureringsmetode for tid og materialer, kan du opprette en datobasert fakturaplan. Fullfør fremgangsmåten nedenfor for å generere en datobasert fakturaplan automatisk.

1. Gå til **Innstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. Gå til prosjektkontraktoppføringen, og på **Sammendrag**-fanen i feltet **Ønsket leveringsdato** velger du en dato.
3. Åpne kontraktlinjen **Tid og materiale** som du lager den datobaserte fakturaplanen for. 
4. I kategorien **Fakturaplan** velger du startdatoen for fakturering og fakturafrekvensen.
5. I delrutenettet velger du **Generer fakturaplan**. Fakturaplanen genereres med feltene **Dato for fakturakjøring**, **Transaksjonsfrist** og **Kjørestatus** angitt på følgende måte:

    - **Dato for fakturakjøring**: Denne datoen er diktert av fakturafrekvensen.
    - **Transaksjonsfrist**: Dagen før fakturakjøringen.
    - **Kjørestatus**: Angis automatisk til **Ikke kjørt**. Når den automatiske fakturaopprettingsjobben kjører for en bestemt fakturakjøringsdato, oppdateres dette feltet automatisk til **Kjøringen var vellykket** eller **Kjøring mislyktes**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Opprette en fakturaplan for fastpris for en kontraktlinje

Når kontraktlinjen har en fast faktureringsmetode, kan du opprette en milepælbasert fakturaplan. 

> [!NOTE]
> Milepæler kan ikke opprettes på en kontraktlinje hvis det ikke er tilordnet et prosjekt til kontraktlinjen.

Fullfør fremgangsmåten nedenfor for å generere en milepælbasert fakturaplan for et fast sett med milepæler som er likt distribuert for kalenderperioden.

1. Gå til **Innstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. Gå til prosjektkontraktoppføringen, og på **Sammendrag**-fanen i feltet **Ønsket leveringsdato** velger du en dato.
3. Åpne **Fast pris**-kontraktlinjen som du oppretter milepælplanen for. I kategorien **Faktureringsmilepæler** velger du startdatoen for fakturering og fakturafrekvensen. 
4. I delrutenettet velger du **Generer periodiske milepæler**. Fakturaplanen genereres med feltene **Navn på milepæl**, **Milepældato** og **Milepælbeløp** angitt som følger:

    - **Navn på milepæl**: Dette navnet bestemmes av fakturafrekvensen.
    - **Milepældato**: Denne datoen er diktert av fakturafrekvensen.
    - **Milepælbeløp**: Dette beløpet beregnes ved å dele kontraktbeløpet på kontraktlinjen etter antall milepæler som diktert etter frekfvensen og datoene for faktureringsstart og ønsket levering.

    Hvis kontraktlinjen har en verdi i feltet **Estimert mva-beløp**, er dette feltet også fordelt likt for hver milepælved generering av periodiske milepæler.

Faktureringsmilepæler skal være lik den avtalte verdien på kontraktlinjen. Hvis de ikke er det, vil det vises en feil på **Kontraktlinje**-siden. Du kan rette opp feilen ved å kontrollere at totalen for faktureringsmilepælene er lik den avtalte verdien for linjen, ved å opprette, redigere eller slette milepæler. Når du har gjort endringene, oppdaterer du siden for å fjerne feilen.

### <a name="manually-create-milestones"></a>Opprette milepæler manuelt

Du kan generere milepæler med fastpris manuelt når de ikke deles regelmessig. Fullfør fremgangsmåten nedenfor for å opprette en milepæl manuelt.

1. Åpne kontraktlinjen med fastpris som du oppretter en milepæl for, gå til **Fakturaplan**-fanen i delrutenettet og velg **+ Opprett ny milepæl for kontraktlinje**. 
2. På siden **Oppret milepæl** angir du den nødvendige informasjonen basert på tabellen nedenfor.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtigoppretting | Tekstfelt for navnet på milepælen. | Dette overføres til milepælen for prosjektkontraktlinjen og fakturaen. |
| Prosjektoppgave | Hurtigoppretting | Hvis milepælen er knyttet til en prosjektoppgave, kan du bruke denne referansen til å legge til et egendefinert logikksett for milepælstatusen basert på oppgavestatusen. | Programmet har ingen nedstrøms innvirkning på denne referansen til en oppgave. |
| Milepældato | Hurtigoppretting | Angi datoen når den automatiske fakturaopprettelsesprosessen skal lete etter statusen for denne milepælen, for å vurdere den for fakturering. | Dette overføres til milepælen for prosjektkontraktlinjen og fakturaen. |
| Fakturastatus | Hurtigoppretting | Når en milepæl opprettes, er denne statusen alltid satt til **Ikke klar for fakturering** eller **Ikke startet**. | Dette overføres til milepælen for prosjektkontraktlinjen og fakturaen. |
| Linjebeløp | Hurtigoppretting | Beløpet eller verdien for milepælen som skal faktureres til kunden. | Dette overføres til milepælen for prosjektkontraktlinjen og fakturaen. |
| Avgift | Hurtigoppretting | Avgiftsbeløpet som brukes på milepælen. | Dette overføres til milepælen for prosjektkontraktlinjen og fakturaen. |

3. Velg **Lagre og lukk**.
