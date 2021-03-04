---
title: Opprette fakturaplaner på en prosjektbasert kontraktlinje – Lite
description: Dette emnet gir informasjon om hvordan du oppretter fakturatidsplaner og milepæler.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180339"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Opprette fakturaplaner på en prosjektbasert kontraktlinje – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Du kan legge ved en fakturaplan på en prosjektbasert kontraktlinje. Fakturering er bare tillatt etter at kontrakten er vunnet for å opprette en prosjektkontrakt. Fakturaplaner gjør det mulig å opprette utkast til fakturaer for en prosjektbasert kontraktlinje automatisk. Hvis du har tenkt å alltid opprette fakturaer manuelt, kan du hoppe over opprettelse av fakturaplaner på en prosjektbasert kontraktlinje eller en kontraktlinje.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Opprette en tid og material-fakturafakturaplan for en prosjektbasert kontraktlinje

Når en prosjektbasert kontraktlinje har en faktureringsmetode for tid og materialer, kan du opprette en datobasert fakturaplan. Fullfør fremgangsmåten nedenfor for å generere en datobasert fakturaplan automatisk.

1. Gå til **Innstillinger** > **Fakturafrekvenser** for å definere fakturafrekvens.
2. Åpne prosjektkontrakten, og angi ønsket leveringsdato i kategorien **Sammendrag**.
3. Åpne tid og material-kontraktlinjen du vil opprette en datobasert fakturaplan for. 
4. I kategorien **Fakturaplan** velger du en startdato for fakturering og fakturahyppigheten. 
5. I delrutenettet velger du **Generer fakturaplan**.

    Systemet genererer fakturaplanen med følgende feltinformasjon:

    - **Dato for fakturakjøring** er satt til datoen basert på fakturahyppigheten.
    - **Transaksjonsfrist** er angitt til dagen før **Dato for fakturakjøring**.
    - **Kjørestatus** angis automatisk til **Ikke kjørt**. Når den automatiske fakturaopprettingsjobben kjører for en bestemt **Dato for fakturakjøring**, oppdateres dette feltet automatisk til **Kjøringen var vellykket** eller **Kjøring mislyktes**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Opprette en fakturaplan med fast pris for en prosjektbasert kontraktlinje

Når en prosjektbasert kontraktlinje har en faktureringsmetode for fast pris, kan du opprette en milepælbasert fakturaplan. Fullfør fremgangsmåten nedenfor for automatisk å generere en milepælbasert fakturaplan for et fast sett med milepæler som fordeles likt for kalenderperioden.

1. Gå til **Innstillinger** > **Fakturafrekvenser** for å definere fakturafrekvens.
2. Åpne prosjektkontrakten, og angi ønsket leveringsdato i kategorien **Sammendrag**.
3. Åpne kontraktlinjen for fast pris der du må opprette en tidsplan for milepælen. 
4. I kategorien **Fakturaplan** (faktureringsmilepæler) velger du en startdato for fakturering og fakturahyppigheten. 
5. I delrutenettet velger du **Generer periodiske milepæler**.

    Systemet genererer fakturaplanen med følgende milepælinformasjon.

    - **Navn på milepæl** er satt til datoen som er diktert basert på fakturafrekvensen.
    - **Milepældato** er satt til datoen som er diktert basert på fakturafrekvensen.
    - **Milepælbeløp** beregnes ved å dele kontraktsbeløpet på den prosjektbaserte kontraktlinjen med antall milepæler i henhold til hyppighet, startdato og ønskede leveringsdatoer.
    - Hvis kontraktlinjen har en verdi i feltet **Estimert avgiftsbeløp**, blir dette feltet også likt fordelt på hver milepæl ved generering av periodiske milepæler.

Faktureringsmilepæler skal være lik den avtalte verdien for den prosjektbaserte kontraktlinjen. Hvis de ikke er like, oppstår det en feil. Du kan rette denne feilen ved å kontrollere at faktureringsmilepælene legger sammen den avtalte verdien av linjen ved å opprette, redigere eller slette milepæler. Oppdater siden etter at endringene er utført.

### <a name="manually-create-milestones"></a>Opprette milepæler manuelt

Faste prismilepæler kan genereres manuelt når de ikke deles periodisk. Følg fremgangsmåten nedenfor for å opprette en milepæl manuelt.

1. Åpne kontraktlinjen for fast pris der du vil opprette en milepæl. 
2. I kategorien **Fakturaplan**, i delrutenettet, velger du **+ Opprett ny milepæl for kontraktlinje**.
3. I skjemaet for **milepæloppretting** angir du obligatorisk informasjon basert på tabellen nedenfor. 

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Navn på milepæl | Hurtigoppretting | Tekstfelt for navnet på milepælen. | Dette feltet er inkludert på milepælen for prosjektkontraktlinjen og fakturaen. |
| Prosjektoppgave | Hurtigoppretting | Hvis milepælen er knyttet til en prosjektoppgave, bruker du denne referansen til å legge til egendefinert logikk og angi statusen for milepælen basert på oppgavestatusen. | Det er ingen nedstrøms påvirkning på denne referansen til en oppgave. |
| Milepældato | Hurtigoppretting | Datoen når opprettingsprosessen for automatisk faktura skal se etter statusen for denne milepælen for fakturering. | Dette er inkludert på milepælen for prosjektkontraktlinjen og fakturaen. |
| Fakturastatus | Hurtigoppretting | Når milepælen opprettes, er denne statusen alltid satt til **Ikke klar for fakturering** eller **Ikke startet**. | Dette er inkludert på milepælen for prosjektkontraktlinjen og fakturaen. |
| Linjebeløp | Hurtigoppretting | Beløpet eller verdien av milepælen som skal faktureres til kunden. | Dette feltet er inkludert på milepælen for prosjektkontraktlinjen og fakturaen. |
| Avgift | Hurtigoppretting | Avgiftsbeløpet som brukes på milepælen. | Dette er inkludert på milepælen for prosjektkontraktlinjen og fakturaen. |

4. Velg **Lagre og lukk**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]