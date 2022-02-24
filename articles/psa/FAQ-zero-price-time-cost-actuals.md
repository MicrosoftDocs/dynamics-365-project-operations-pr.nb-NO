---
title: Hvorfor settes pris som standard til null i faktiske tidskostnader?
description: Feilsøke hvorfor en pris settes som standard til 0 i faktiske tidskostnader.
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
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993068"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Hvorfor settes pris som standard til null i faktiske tidskostnader?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse vanlige spørsmålene gjelder for faktiske verdier der transaksjonsklassen er satt til Tid og transaksjonstypen er Kostnad. Følgende tre kontroller hjelper deg med å feilsøke hvorfor prisen settes som standard til 0 i faktiske tidskostnader.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontroll 1: Identifiser kostnadsprislisten for prosjektet

Finn prosjektet fra prosjektfeltet for de faktiske verdiene og gå deretter til prosjektsiden. Klikk på koblingen for kontraktsenhet i feltet. På siden Kontraktsenhet kan du se om kontraktsenheten har en prisliste i rutenettet Kostprislister.

Hvis det er mer enn én prisliste, har du fastslått problemet. Project Service støtter bare én prisliste per organisasjonsenhet. Fjern alle prislister fra denne enheten til det er bare én prisliste vedlagt i rutenettet Kostprislister for organisasjonsenheten.

Hvis det ikke er noen prislister tilknyttet organisasjonsenheten, noter valutaen for organisasjonsenheten. Gå til Project Service og deretter Parametere, og åpne kategorien Prislister. Kontroller om det finnes prislister med kontekst satt til Kostnad og valuta som samsvarer med organisasjonsenhetens valuta.
 
Hvis det ikke finnes prislister som samsvarer med kriteriene, har du fastslått problemet. Kontroller at du har minst én prisliste der konteksten er satt til Kostnad og der valutaen samsvarer med organisasjonsenhetens valuta.

Hvis det er mer enn én prisliste som samsvarer med kriteriene, fortsetter du å lese dette dokumentet for å gjøre flere kontroller.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontroll 2: Er noen av prislistene som er identifisert ovenfor, gyldige for den bestemte datoen til de faktiske tidskostnadene?

For at Project Service skal vurdere en prisliste for standardpris, må denne prislisten være gjeldende for datoen på de faktiske tidskostnadene. Kontroller følgende for å se om prislisten(e) identifisert ovenfor er gjeldende:

- Kontroller om start- og sluttdatoer i kategorien Generelt for prislistene som er tilknyttet, ikke er tomme. Hvis start- og sluttdatoene i prislistene identifisert ovenfor er tomme, vil du ha fastslått problemet. 
- Noter startdatofeltet for de faktiske tidskostnadene og kontroller om noen av prislistene som er identifisert, er gjeldende for denne datoen. For eksempel bør datoen for faktiske tidskostnader være innenfor startdatoen og sluttdatoen i prislisten. 
    - Hvis det ikke er en prisliste som omfatter denne datoen i de faktiske tidskostnadene, har du fastslått problemet. Endre start- og sluttdatoer for prislisten for å sikre at prislisten dekker datoen for faktiske tidskostnader. 
    - Hvis det er mer enn én prisliste som omfatter datoen i de faktiske tidskostnadene, har du fastslått problemet. Du kan løse dette ved å redigere start- og sluttdatoene i prislisten(e) slik at det bare er én prisliste som omfatter datoen for de faktiske tidskostnadene. 
    - Hvis det er bare én prisliste som omfatter datoen for de faktiske tidskostnadene, kan du gå til neste kontroll i dokumentet.
Når du har gjort de nødvendige korrigeringene, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at de faktiske tidskostnadene viser en gyldig pris.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontroll 3: Finnes det en pris i prislisten for prisdimensjonene i de faktiske tidskostnadene?

Hvis du har fullført kontroll 1 og 2, skal du nå ha bare én prisliste som gjelder for datoen for de faktiske tidskostnadene. Åpne prislisten og gå til kategorien Rollepriser. Kontroller at det er en rad i rutenettet for prisdimensjonene i de faktiske tidskostnadene.

Hvis det ikke er noen rad i rutenettet Rollepriser for prisdimensjonene i de faktiske tidskostnadene, har du fastslått problemet. Opprett en rad i rutenettet Rollepriser for prisdimensjonene i de faktiske tidskostnadene. Når du har gjort dette, oppretter du en tidsoppføring på nytt, godkjenner den, og kontrollerer at de faktiske tidskostnadene viser en gyldig pris.
 
Hvis du fremdeles ikke ser en gyldig pris i de faktiske tidskostnadene når du har gjort de tre kontrollene ovenfor, logger du en støtteforespørsel.





[!INCLUDE[footer-include](../includes/footer-banner.md)]