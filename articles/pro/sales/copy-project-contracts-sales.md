---
title: Kopiere prosjektkontrakter
description: Dette emnet gir informasjon om kopiering av prosjektkontrakter i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6da8e3ba8e062f3e06dc7f440caebdd93e496c65
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081525"
---
# <a name="copying-project-contracts"></a>Kopiere prosjektkontrakter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Du kan enkelt opprette nye prosjektkontrakter ved å ta kopier av eksisterende kontrakter på én av to måter: 

  - Velg en prosjektkontrakt på listesiden **Prosjektkontrakter** , og velg deretter **Kopier**.
  - På detaljsiden **Prosjektkontrakt** velger du **Kopier**.

En dialogside åpnes, der du kan velge parameterne for den kopierte kontrakten. Følgende felt er inkludert i dialogboksen. Kopieringsprosessen kan endres avhengig av verdiene du velger i denne dialogen.

| **Felt** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
| --- | --- | --- |
| Emne | Skriv inn emnet for målkontrakten. Når dialogsiden åpnes, setter systemet dette feltet til navnet på kildekontrakten med **-kopi** lagt til. | Dette feltet har ingen nedstrøms påvirkning. |
| Kunde | Referanse til kundens firma- eller forretningsforbindelsesoppføring. Når dialogboksen åpnes, setter systemet dette feltet til kontoen i kildekontrakten. | Dette feltet er den primære kunden i kontrakten. |
| Kontraktsenhet | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne avtalen. Når dialogsiden åpnes, setter systemet den til kontraktenheten for kildekontrakten. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver enkelt kontraktenhet har en valuta. Denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |
| Valuta | Dette er valutaen som avtaletransaksjonene utføres i. Når dialogsiden åpnes, setter systemet dette feltet til valutaen for kildekontrakten. Du kan ikke endre valutaen. I så fall settes feltet **Kopier pris** alltid til **Nei** fordi prislistene på kildekontrakten ikke lenger er relevante. | Valuta brukes til å standardisere prislister, til å bygge økonomiske estimater i kontrakten og til å fakturere kunden når avtalen er vunnet. |
| Ønsket leveringsdato | Leveringsdatoen som er forespurt av kunden. | Denne datoen brukes som sluttdato når du oppretter faktureringsdatoer langs en bestemt frekvens. |
| Kopier pris | Angir om prissettingen i kontrakten skal kopieres fra kildekontrakten. | Hvis dette feltet er satt til **Ja** , kopieres prosjekt- og produktprislistereferansene fra kildetilbudet til målkontrakten. Hvis du velger **Nei** , blir prislistene standard basert på de siste prislistene i konto- eller prosjektparameterne. |

Når du velger **OK** på dialogsiden, oppretter systemet en kopi av kontrakten basert på parameterne som er valgt. Den nye kontrakten åpnes.

Følgende informasjon kopieres ikke fra **kilde** - til **målkontrakten** :

  - Fakturaplaner
  - Kontrakt og kontraktlinjekunder
  - Prosjektreferanse på prosjektbaserte kontraktlinjer
  - Kundebudsjettinformasjon

Ettersom denne informasjonen er spesifikk for hver kontrakt, kopieres ikke disse feltene og oppføringene. Kontraktlinjer for prosjekter og produkter, estimater på kontraktlinjedetaljer og verdier på kontraktnivå som ikke må overskrides, kopieres. Standarder for pris og kostnadssats avhenger av valget i feltet **Kopier pris** på dialogsiden **Kopier parametere**.