---
title: Prosjektteammedlemmer
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med informasjon, attributter og planlegging for prosjektteammedlemmer.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3465688fb267f3ab785fcb0d252e8616ac1aa1c8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929318"
---
# <a name="project-team-members"></a>Prosjektteammedlemmer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjektteammedlemmer er prosjektdeltakerne som fullfører arbeidet på et prosjekt. Formålet til rutenettet for teammedlemmer er å gi en liste over navngitte ressurser som er forpliktet til engasjementet, og generelle teammedlemmer som er plassholderressurser, og som vil bli bemannet senere.

Fra rutenettet for teammedlemmer har prosjektlederen og de andre prosjektdeltakerne mulighet til å se hvem som er med i prosjektet. De kan også vise et sammendrag av deres bestillinger, planlagt innsats og individuelle ressurstilordninger. Rutenettet for teammedlemmer gjør det mulig for prosjektledere å definere ressurskrav for generelle teammedlemmer og administrere bestillinger av eksisterende teammedlemmer.

Tabellen nedenfor viser de viktigste attributtene for et prosjektteammedlem.

| Feltnavn          | Beskrivelse                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tilordningsmetode        | Tildelingsmetoden som brukes til å bestille ressurser i prosjektet.                                                                         |
| Faktureringstype             | Velg om teammedlemmet er klassifisert som fakturerbart.                                                                                                                                       |
| Ressurs som kan reserveres        | Den reserverbare ressursen som er valgt for å erstatte den generelle ressursen.                                                                                                                   |
| Slettestatus            | Slettestatusen for teammedlemmet for å spore om det er sendt en sletteforespørsel til PSS, og om PSS sender tilbake svar og innen det forventede tidsrommet. |
| Total innsats (timer)     | Summen av teammedlemmets innsats i tilordningene.                                                                                                                         |
| Innsats fullført (timer) | En sporing av innsatsen som teammedlemmet har gjort i tilordningene.                                                                                           |
| Gjenværende innsats (timer) | En sporing av innsatsen som ennå ikke er fullført av teammedlemmet i tilordningene.                                                                                    |
| Overflate                   | Sluttdatoen for teammedlemskapet for ressursen.                                                                                                                                            |
| Timer med forpliktende bestillinger        | De faste, forpliktende timene til teammedlemmet.                                                                                                                                                                |
| Stillingsnavn            | Navnet som brukes til å identifisere den generelle ressursen.                                                                                                                                   |
| Ressursenhet          | Organisasjonsenheten for ressursen som utfører arbeidet.                                                                                                                      |
| Prosjektgodkjenner         | Velg om teammedlemmet kan godkjenne tid og utgifter.                                                                                                                     |
| Nødvendige timer           | De nødvendige timene for teammedlemmet fra teammedlemskrav.                                                                                                                       |
| Rolle                     | Rollen som teammedlemmet fyller i dette teamet.                                                                                                                                |
| Stillingsbeskrivelse     | Skriv inn en beskrivelse av rollen for dette teammedlemmet.                                                                                                                             |
| Timer med ikke-forpliktende bestillinger        | Timene med ikke-forpliktende bestillinger for teammedlemmet.                                                                                                                                                                 |
| Start                    | Startdatoen for teammedlemskapet for ressursen.                                                                                                                                          |

Følgende handlinger kan utføres fra rutenettet for teammedlemmer:

- **Bestill**: For organisasjoner som bruker hybride bestillinger, vil Bestill-handlingen gi brukerne mulighet til å bestille en navngitt ressurs basert på behovskravene som genereres fra det generelle teammedlemmet.
- **Generer krav**: Denne handlingen genererer kravet.
- **Angi mønster**: Gjør det mulig for prosjektledere å justere profiler for ressurskrav på et detaljert nivå. Prosjektledere kan justere de spesifikke behovene til prosjektet i tilfeller der standarddistribusjonen ikke passer inn.
- **Send forespørsel**: For organisasjoner som bruker metoden for sentrale bestillinger.
- **Rediger**: Attributter for teammedlemmer kan redigeres, blant annet organisasjonsenheten, rollen og stillingsnavnet.
- **Vedlikehold bestillinger**: Når ressursbestillinger må oppdateres, gjør vedlikehold av bestillinger at prosjektlederen kan justere følgende:

    - Start
    - Slutt
    - Fordeling av total innsats

- **Ny**: I tillegg til å legge til ressurser direkte fra tidsplanen kan prosjektledere legge til nye eller generelle teammedlemmer fra rutenettet for teammedlemmer.
- **Slett**: Ved å velge ett eller mange teammedlemmer kan prosjektlederen slette ressurser som ikke lenger skal være med i prosjektet. Ved sletting av et teammedlem slettes også alle tilknyttede ressurstildelinger, og alle eksisterende bestillinger blir annullert.


[!INCLUDE[footer-include](../includes/footer-banner.md)]