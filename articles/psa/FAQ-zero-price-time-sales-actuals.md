---
title: Hvorfor settes pris som standard til null i faktisk tidssalg?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktisk tidssalg.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2df4ce2d6391e70fea8e8f15c1b5774c9a9bfbe5f5ef2e6d8da8668afd34d4c9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992578"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Hvorfor settes pris som standard til null i faktisk tidssalg?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse vanlige spørsmålene gjelder for faktiske verdier der transaksjonsklassen er satt til Tid og transaksjonstypen er Ufakturert salg. Følgende tre kontroller hjelper deg med å feilsøke hvorfor prisen (fakturasatsen) settes som standard til 0 i faktisk tidssalg.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontroll 1: Identifiser salgsprislisten for prosjektet

Finn prosjektet fra prosjektfeltet for de faktiske verdiene og gå til prosjektsiden. Gå deretter til kategorien Salg. Klikk på koblingen i feltet Prosjektkontrakt i rutenettet Prosjektkontraktlinjer. Prosjektkontrakt-siden åpnes. På prosjektkontraktssiden går du til kategorien Prosjektprislister. Kontroller om det finnes minst én prisliste tilknyttet her. Hvis det er ingen prisliste vedlagt i rutenettet Prosjektprislister for prosjektkontrakten, har du fastslått problemet. Legg ved en prisliste i Prosjektprislister-rutenettet. Prislistene som kan tilknyttes her, må ha kontekstfeltet satt til Salg og valutafeltet i prislisten må samsvare med valutafeltet i prosjektkontrakten. Når du har gjort de nødvendige korrigeringene, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at ufakturerte faktiske verdier for salg viser en gyldig pris. 

Hvis du har én eller flere prislister som er vedlagt i rutenettet Prosjektprislister i prosjektkontrakten, går du videre til neste kontroll i dokumentet.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontroll 2: Er noen av prislistene som er identifisert ovenfor, gyldige for den bestemte datoen til det faktiske tidssalget?

For at Project Service skal vurdere en prisliste for standardpris, må denne prislisten være gjeldende for datoen på det faktiske tidssalget. Kontroller følgende for å se om prislisten(e) identifisert ovenfor er gjeldende:
- Kontroller om start- og sluttdatoer i kategorien Generelt for prislistene som er tilknyttet, ikke er tomme. Hvis start- og sluttdatoene i prislistene identifisert ovenfor er tomme, vil du ha fastslått problemet. 
- Noter startdatofeltet for det faktiske tidssalget og kontroller om noen av prislistene som er identifisert, er gjeldende for denne datoen. For eksempel bør datoen for faktisk tidssalg være innenfor startdatoen og sluttdatoen i prislisten. 
    - Hvis det ikke er en prisliste som omfatter denne datoen i det faktiske tidssalget, har du fastslått problemet. Endre start- og sluttdatoer for prislisten for å sikre at prislisten dekker datoen for faktisk tidssalg. 
    - Hvis det er mer enn én prisliste som omfatter datoen i det faktiske tidssalget, har du fastslått problemet. Du kan løse dette ved å redigere start- og sluttdatoene i prislisten(e) slik at det bare er én prisliste som omfatter datoen for det faktiske tidssalget. 
    - Hvis det er bare én prisliste som omfatter datoen for det faktiske tidssalget, går du til kontroll 3.
Når du har gjort de nødvendige korrigeringene, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at det faktiske tidssalget viser en gyldig pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontroll 3: Finnes det en pris i prislisten for prisdimensjonene i det faktiske tidssalget?

Hvis du har fullført kontroll 1 og 2, skal du nå ha bare én prisliste som gjelder for datoen for det faktiske tidssalget. Åpne prislisten og gå til kategorien Rollepriser. Kontroller at det er en rad i rutenettet for prisdimensjonene i det faktiske tidssalget.

Hvis det ikke er noen rad i rutenettet Rollepriser for prisdimensjonene i det faktiske tidssalget, har du fastslått problemet. Opprett en rad i rutenettet Rollepriser for prisdimensjonene i det faktiske tidssalget. Når du har gjort dette, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at det faktiske tidssalget viser en gyldig pris.

Hvis du fremdeles ikke ser en gyldig pris i det faktiske tidssalget når du har gjort de tre kontrollene ovenfor, logger du en støtteforespørsel. 



[!INCLUDE[footer-include](../includes/footer-banner.md)]