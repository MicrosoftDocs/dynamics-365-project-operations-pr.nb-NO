---
title: Fakturaplaner på prosjektbaserte tilbudslinjer
description: Dette emnet gir informasjon om hvordan du oppretter fakturatidsplaner og milepæler for tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b69742915fe79ee59e7fdcf317000cea79c5929
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180834"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Fakturaplaner på prosjektbaserte tilbudslinjer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

En prosjektbasert tilbudslinje gir mulighet til å uttrykke en fakturaplan. Dette er valgfritt i løpet av tilbudsfasen fordi programmet ikke støtter fakturering av et prosjekt når det er knyttet til en tilbudslinje. Fakturering er bare tillatt etter at tilbudet er vunnet. Den eneste effekten ved å opprette en fakturaplan i løpet av tilbudsfasen er at denne fakturaplanen kopieres til den prosjektbaserte kontraktlinjen. Hvis du ikke oppretter en fakturaplan i løpet av tilbudsfasen, kan du gjøre dette på den prosjektbaserte kontraktlinjen.

Generelt sett er formålet med faktureringsplanen å tillate automatisk opprettelse av utkastfakturaer for en prosjektbasert kontraktlinje. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Opprette en fakturaplan for tid og materiale for en prosjektbasert tilbudslinje

Når faktureringsmetoden for en prosjektbasert tilbudslinje er tid og materiell, genererer systemet en datobasert fakturaplan. Fullfør fremgangsmåten nedenfor for å generere en datobasert fakturaplan automatisk.

1. Gå til **Innstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. På **Tilbud**-siden åpner du prosjekttilbudet, og på **Sammendrag**-fanen angir du ønsket leveringsdato.
3. Åpne tilbudslinjen for tid og materiell som du må opprette en datobasert fakturaplan for. 
4. I kategorien **Fakturaplan** velger du verdier i feltene **Fakturastart** og **Fakturafrekvens**. 
5. I delrutenettet velger du **Generer fakturaplan**.
6. Programmet genererer fakturaplanen med feltene **Dato for fakturakjøring**, **Transaksjonsfrist** og **Kjørestatus** angitt på følgende måte:

    - **Dato for fakturakjøring** er angitt til datoen som er diktert basert på fakturafrekvensen.
    - **Transaksjonsfrist** er angitt til dagen før **Dato for fakturakjøring**.
    - **Kjørestatus** angis automatisk til **Ikke kjørt**. Når den automatiske fakturaopprettingsjobben kjører for en bestemt fakturakjøringsdato, oppdateres dette feltet automatisk til **Kjøringen var vellykket** eller **Kjøring mislyktes**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Opprette en fakturaplan for fastpris for en prosjektbasert tilbudslinje

Når den prosjektbaserte tilbudslinjen har faktureringsmetoden **Fast**, oppretter systemet en milepælbasert fakturaplan. Fullfør fremgangsmåten nedenfor for automatisk å generere denne tidsplanen for et fast sett med milepæler som er likt distribuert for kalenderperioden.

1. Gå til **Innstillinger** > **Fakturafrekvenser**, og konfigurer en fakturafrekvens.
2. På **Tilbud**-siden åpner du prosjekttilbudet, og på **Sammendrag**-fanen angir du ønsket leveringsdato.
3. Åpne den tilbudslinjen for fastpris som du trenger for å opprette en milepælplan for. 
4. I kategorien **Fakturaplan** velger du verdier i feltene **Fakturastart** og **Fakturafrekvens**. 
5. I delrutenettet velger du **Generer periodiske milepæler**.
6. Programmet genererer fakturaplanen med navn på milepæl, dato og beløp.

    - Navnet på milepælen er angitt til datoen som er diktert basert på fakturafrekvensen.
    - Datoen for milepælen er angitt til datoen som er diktert basert på fakturafrekvensen.
    - Milepælbeløpet beregnes ved å dele tilbudsbeløpet på den prosjektbaserte tilbudslinjen etter antall milepæler som diktert etter frekvensen og datoene for faktureringsstart og ønsket levering.
    - Hvis tilbudslinjen også har et beregnet avgiftsbeløp, deles denne verdien mellom hver milepæl likt ved generering av periodiske milepæler.

### <a name="manually-create-milestones"></a>Opprette milepæler manuelt

Milepæler med fastpris kan også genereres manuelt når de ikke deles regelmessig. Slik oppretter du en milepæl manuelt:

Åpne tilbudslinjen for fastpris der du trenger for å opprette en milepæl. I kategorien **Fakturaplan**, i delrutenettet, velger du **+ Opprett ny tilbudslinjemilepæl**, og angi nødvendig informasjon basert på tabellen nedenfor.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtigoppretting | Navnet på milepælen. | Dette overføres til milepælen for prosjektkontraktlinjen og til fakturaen |
| Prosjektoppgave | Hurtigoppretting | Hvis milepælen er knyttet til en prosjektoppgave, kan du bruke denne referansen til å legge til et egendefinert logikksett for milepælstatusen basert på oppgavestatusen. | Programmet har ingen nedstrøms innvirkning på denne referansen til en oppgave. |
| Milepældato | Hurtigoppretting | Angi datoen når den automatiske fakturaopprettelsesprosessen skal lete etter statusen for denne milepælen, for å vurdere den for fakturering. | Dette overføres til milepælen for prosjektkontraktlinjen og til fakturaen. |
| Fakturastatus | Hurtigoppretting | Når en milepæl opprettes, er denne statusen alltid satt til **Ikke klar for fakturering**. | Dette overføres til milepælen for prosjektkontraktlinjen og til fakturaen. |
| Linjebeløp | Hurtigoppretting | Beløpet eller verdien for milepælen som skal faktureres til kunden. | Dette overføres til milepælen for prosjektkontraktlinjen og til fakturaen. |
| Avgift | Hurtigoppretting | Avgiftsbeløpet som skal brukes på milepælen. | Dette overføres til milepælen for prosjektkontraktlinjen og til fakturaen. |
