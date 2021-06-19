---
title: Opprette et adhoc-forskudd på en kontrakt
description: Dette emnet gir informasjon om hvordan du oppretter et forskudd på en kontrakt etter behov.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 51e3b0ac8e111be70fe6ad0f9c162dfaec3339ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003508"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Opprette et adhoc-forskudd på en kontrakt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]