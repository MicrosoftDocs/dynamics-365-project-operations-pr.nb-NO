---
title: Kopiere prosjektkontrakter
description: Denne artikkelen inneholder informasjon om kopiering av prosjektkontrakter i Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8fa17bbd5738e4bc6330c728a3418a2be6828eef
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410081"
---
# <a name="copy-project-contracts"></a>Kopiere prosjektkontrakter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Du kan enkelt opprette nye prosjektkontrakter ved å ta kopier av eksisterende kontrakter på én av to måter: 

  - Velg en prosjektkontrakt på listesiden **Prosjektkontrakter**, og velg deretter **Kopier**.
  - På detaljsiden **Prosjektkontrakt** velger du **Kopier**.

En dialogside åpnes, der du kan velge parameterne for den kopierte kontrakten. Følgende felt er inkludert i dialogboksen. Kopieringsprosessen kan endres avhengig av verdiene du velger i denne dialogen.

| **Felt** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Emne | Skriv inn emnet for målkontrakten. Når dialogsiden åpnes, setter systemet dette feltet til navnet på kildekontrakten med **-kopi** lagt til. | Dette feltet har ingen nedstrøms påvirkning. |
| Kunde | Referanse til kundens firma- eller forretningsforbindelsesoppføring. Når dialogboksen åpnes, setter systemet dette feltet til kontoen i kildekontrakten. | Dette feltet er den primære kunden i kontrakten. |
| Kontraktsenhet | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. Når dialogsiden åpnes, setter systemet den til kontraktenheten for kildekontrakten. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver enkelt kontraktenhet har en valuta. Denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |
| Valuta | Dette er valutaen som avtaletransaksjonene utføres i. Når dialogsiden åpnes, setter systemet dette feltet til valutaen for kildekontrakten. Du kan ikke endre valutaen. I så fall settes feltet **Kopier pris** alltid til **Nei** fordi prislistene på kildekontrakten ikke lenger er relevante. | Valuta brukes til å standardisere prislister, til å bygge økonomiske estimater i kontrakten og til å fakturere kunden når avtalen er vunnet. |
| Ønsket leveringsdato | Leveringsdatoen som er forespurt av kunden. | Denne datoen brukes som sluttdato når du oppretter faktureringsdatoer langs en bestemt frekvens. |
| Kopier pris | Angir om prissettingen i kontrakten skal kopieres fra kildekontrakten. | Hvis dette feltet er satt til **Ja**, kopieres prosjekt- og produktprislistereferansene fra kildetilbudet til målkontrakten. Hvis du velger **Nei**, blir prislistene standard basert på de siste prislistene i konto- eller prosjektparameterne. |

Når du velger **OK** på dialogsiden, oppretter systemet en kopi av kontrakten basert på parameterne som er valgt. Den nye kontrakten åpnes.

Følgende informasjon kopieres ikke fra **kilde**- til **målkontrakten**:

  - Fakturaplaner
  - Kontrakt og kontraktlinjekunder
  - Prosjektreferanse på prosjektbaserte kontraktlinjer
  - Kundebudsjettinformasjon

Ettersom denne informasjonen er spesifikk for hver kontrakt, kopieres ikke disse feltene og oppføringene. Kontraktlinjer for prosjekter og produkter, estimater på kontraktlinjedetaljer og verdier på kontraktnivå som ikke må overskrides, kopieres. Standarder for pris og kostnadssats avhenger av valget i feltet **Kopier pris** på dialogsiden **Kopier parametere**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
