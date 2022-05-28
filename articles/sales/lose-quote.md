---
title: Kopier prosjektbaserte tilbud
description: Dette emnet gir informasjon om hvordan du kopierer prosjektbaserte tilbud i Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1e8611f34a23d6d87317cc785148c1a3f9c26dca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588058"
---
# <a name="copy-project-based-quotes"></a>Kopier prosjektbaserte tilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan enkelt opprette et nytt prosjekttilbud ved å kopiere et eksisterende. 

- Hvis du vil kopiere et prosjekttilbud, går du til listesiden **Prosjekttilbud** eller detaljsiden **Prosjekttilbud**, velger prosjekttilbudet du vil kopiere, og velger deretter **Kopier**.

Dette åpner en dialogside der du kan angi parameterne for kopien. Den følgende tabellen lister opp feltene som er inkludert på dialogsiden. Kopieringsprosessen kan endres avhengig av verdiene du velger.

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Emne | Angi relevant emne, eller navn, for måltilbudet. Når dialogboksen åpnes, setter systemet den til emnet for kildetilbudet med **-kopi** lagt til. | |
| Potensiell kunde | Referanse til kundens firma- eller forretningsforbindelsesoppføring. Når dialogboksen åpnes, setter systemet den til kontoen i kildetilbudet. | Dette feltet er den primære kunden i tilbudet. |
| Kontraktsenhet | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen.
Når dialogboksen åpnes, setter systemet den til kontraktenheten i kildetilbudet. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver enkelt kontraktenhet har en valuta. Valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under kjøringen av prosjektet. |
| Valuta | Dette er valutaen som avtaletransaksjonene utføres i. Når dialogboksen åpnes, setter systemet den til valutaen i kildetilbudet. Dette kan endres, og hvis det endres, er feltet **Kopier pris** alltid satt til **Nei**. Dette skyldes at prislistene i kildetilbudet ikke lenger er relevante. | Valuta brukes til å angi en prisliste som standard, til å bygge et økonomisk estimat på tilbudet og til slutt til å fakturere kunden når avtalen er vunnet. |
| Ønsket leveringsdato | Dette er leveringsdatoen som kunden har bedt om. | Dette brukes som sluttdato når du oppretter faktureringsdatoer langs en bestemt frekvens. |
| Kopier pris | En Ja/nei-verdi angir om prissettingen i tilbudet skal kopieres fra kildetilbudet. | Hvis du velger **Ja**, kopieres prosjektprisliste- og produktprislistereferansene fra kildetilbudet til måltilbudet. Hvis du velger **Nei**, blir prislistene standard på nytt basert på de siste prislistene som ble definert i konto- eller prosjektparameterne. |

Når du velger **OK** på dialogsiden, oppretter systemet en kopi av prosjekttilbudet basert på parameterne som er valgt i dialogen. Det nye prosjekttilbudet åpnes. 

> [!NOTE]
> Følgende informasjon kopieres ikke fra kildetilbudet til måltilbudet:
>
> - Fakturaplaner
> - Tilbud og tilbudslinjekunder
> - Prosjektreferanse på prosjektbaserte tilbudslinjer – informasjon om kundebudsjett
>
>Ettersom denne informasjonen er svært spesifikk for hvert tilbud, kopieres ikke disse feltene og oppføringene. Tilbudslinjer for prosjekter og produkter, estimater på tilbudslinjedetaljer og verdier på tilbudsnivå som ikke må overskrides, kopieres. Standarder for pris og kostnadssats avhenger av alternativet **Kopier pris** som er valgt på dialogsiden **Kopier parametere**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]