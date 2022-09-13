---
title: Kopier prosjektbaserte kontrakter
description: Denne artikkelen inneholder informasjon om kopiering av prosjektkontrakter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410336"
---
# <a name="copy-project-based-contracts"></a>Kopier prosjektbaserte kontrakter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Du kan enkelt opprette nye prosjektkontrakter ved å kopiere eksisterende kontrakter på én av to måter:

- Velg en prosjektkontrakt på listesiden **Prosjektkontrakter**, og velg deretter **Kopier**.
- På detaljsiden **Prosjektkontrakt** velger du **Kopier**.

I begge tilfeller vises en dialogboks, der du kan angi parameterne for den kopierte kontrakten. Dialogboksen omfatter følgende felter. Kopieringsprosessen kan endres avhengig av verdiene du velger.

| Felt | Bekrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| Emne | Skriv inn emnet for målkontrakten. Når dialogboksen åpnes, setter systemet feltet til navnet på kildekontrakten, men ordet «kopi» føyes til. | Dette feltet har ingen nedstrøms påvirkning. |
| Kunde | En referanse til kundens firma- eller forretningsforbindelsesoppføring. Når dialogboksen åpnes, setter systemet feltet til kontoen i kildekontrakten. | Dette feltet er den primære kunden i kontrakten. |
| Eiende firma | Firmaet som er ansvarlig for levering av prosjektene som er knyttet til denne avtalen. Når dialogboksen åpnes, setter systemet feltet til det eiende firmaet i kildekontrakten. | Det eiende firmaet er den juridiske enheten som skal gjennomføre prosjektet etter at avtalen er gjort. Valutaen til det eiende firmaet må samsvare med valutaen til kontraktsenheten. |
| Kontraktsenhet | Organisasjonsenheten som er ansvarlig for levering av prosjektene som er knyttet til denne avtalen. Når dialogboksen åpnes, setter systemet feltet til kontraktsenheten i kildekontrakten. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene etter at avtalen er lukket. Hver enkelt kontraktenhet har en valuta. Denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløper under prosjektet. |
| Valuta | Dette er valutaen som avtaletransaksjonene utføres i. Når dialogsiden åpnes, setter systemet feltet til valutaen for kildekontrakten. Du kan ikke endre valutaen. I så fall settes feltet **Kopier pris** alltid til **Nei** fordi prislistene i kildekontrakten ikke lenger er relevante. | Denne valutaen brukes for standard prislister til å generere økonomiske estimater i kontrakten og til å fakturere kunden når avtalen er vunnet. |
| Ønsket leveringsdato | Leveringsdatoen som er forespurt av kunden. | Denne datoen brukes som sluttdato når du oppretter faktureringsdatoer med en bestemt frekvens. |
| Kopier pris | En verdi som angir om prissettingen i kontrakten skal kopieres fra kildekontrakten. | Hvis dette feltet er satt til **Ja**, kopieres prosjekt- og produktprislistereferansene fra kildekontrakten til målkontrakten. Hvis det er satt til **Nei**, brukes standard prislister basert på de siste prislistene i konto- eller prosjektparameterne. |

Når du velger **OK** i dialogboksen, oppretter systemet en kopi av kontrakten basert på parameterverdiene du angir. Deretter åpnes den nye kontrakten.

Følgende informasjon kopieres **ikke** fra kildekontrakten til målkontrakten fordi den er spesifikk for hver kontrakt:

- Fakturaplaner
- Kontrakt og kontraktlinjekunder
- Prosjektreferanse på prosjektbaserte kontraktlinjer
- Kundebudsjettinformasjon

Kontraktlinjer for prosjekter og produkter, estimater i kontraktlinjedetaljer og verdier på kontraktnivå som ikke må overskrides, kopieres. Oppføring av standardpriser og kostnadssatser avhenger av valget i feltet **Kopier pris** i dialogboksen **Kopier parametere**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
