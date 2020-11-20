---
title: Opprette et adhoc-forskudd på en kontrakt – Lite
description: Dette emnet gir informasjon om hvordan du oppretter et forskudd på en kontrakt etter behov.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181374"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Opprette et adhoc-forskudd på en kontrakt – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Microsoft Dynamics 365 Project Operations støtter faktureringsscenarioer som omfatter forskuddsbetaling. Prosessen for å bruke **Forskudd** i **Project Operations** ligner på **Honorar**-kontrakter. 

Fullfør fremgangsmåten nedenfor for å fakturere kunden for et forskudd.

1. Gå til **Prosjektkontrakt**-siden, og velg deretter kategorien **Forskudd og honorarer**.
2. I delrutenettet som viser alle tidligere registrerte forskuddsbetalinger, velger du **+ Nytt Prosjektkontrakthonorar**. 

    **Hurtigoppretting**-skjemaet åpner for registrering av en forskuddsbetaling.
    
3. Tabellen nedenfor viser feltene for registrering av et forskudd og hva du må huske på når du oppretter nye:

    | Felt | Beskrivelse | Nedstrøms påvirkning |
    | --- | --- | --- |
    | **Prosjektkontraktkunde** | Dette feltet angir hvilken kunde på kontrakten som skal faktureres for dette forskuddet. | Hvis du har flere kunder i kontrakten og vil fakturere hver av dem for et bestemt honorar eller forskudd, oppretter du et forskudd for hver kunde individuelt. |
    | **Beskrivelse** | Beskrivelsen av formålet med eller tidsberegningen for forskuddet for å identifisere dette forskuddet. | Denne beskrivelsen vises på fakturalinjen for dette forskuddet. |
    | **Beløp** | Beløpet for forskuddsbetalingen. | Dette beløpet vises på fakturalinjen for dette forskuddet. |
    | **Fakturadato** | Datoen da forskuddet faktureres til kunden. | Dette er datoen for prosessen for automatisk fakturaopprettelse for å opprette en fakturalinje for dette forskuddet. |
    | **Fakturastatus** | Dette er en alternativ innstilling som angir om dette forskuddet blir lagt til i en kladdefaktura for denne kunden. Mulige verdier er:</br>- **Ikke klar for fakturering**</br>- **Klar for fakturering** | Når en forskuddsbetaling er merket som **Klar til fakturering**, legges den til som en linjetid på en kladdefaktura. Bare et fullt fakturert forskudd kan brukes til å avstemme mot prosjektkostnader for den neste fakturaperioden. |

4. Velg **Lagre og lukk** i dialogboksen hurtigoppretting for å registrere forhåndsbetaling eller forskudd.
