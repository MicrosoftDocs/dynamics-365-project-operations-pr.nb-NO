---
title: Hvorfor settes pris som standard til null i faktiske salgsutgifter?
description: Følgende tre kontroller hjelper deg med å feilsøke hvorfor prisen settes som standard til 0 i faktiske salgsutgifter.
author: rumant
ms.prod: ''
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
ms.openlocfilehash: 92b507d8e5605c01f1a9235233b3cd2885070749
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993023"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Hvorfor settes pris som standard til null i faktiske salgsutgifter?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Disse vanlige spørsmålene gjelder for faktiske utgifter der transaksjonsklassen er satt til Utgift og transaksjonstypen er Ufakturert salg. Følgende tre kontroller hjelper deg med å feilsøke hvorfor prisen (fakturasatsen) settes som standard til 0 i faktiske salgsutgifter.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontroll 1: Identifiser salgsprislisten for prosjektet

Finn prosjektet fra prosjektfeltet for de faktiske verdiene og gå til prosjektsiden. Gå deretter til kategorien Salg. Klikk på koblingen i feltet Prosjektkontrakt i rutenettet Prosjektkontraktlinjer. Prosjektkontrakt-siden åpnes. På prosjektkontraktssiden går du til kategorien Prosjektprislister. Kontroller om det finnes minst én prisliste tilknyttet her.

Hvis ingen prisliste er vedlagt i rutenettet Prosjektprislister for prosjektkontrakten:

- Legg ved en prisliste i Prosjektprislister-rutenettet. Prislistene som kan tilknyttes her, må ha kontekstfeltet satt til Salg og valutafeltet i prislisten må samsvare med valutafeltet i prosjektkontrakten. Når du har gjort de nødvendige korrigeringene, oppretter du en utgiftsoppføring på nytt, godkjenner den, og kontrollerer at ufakturerte faktiske verdier for salg viser en gyldig pris.
- Hvis du har én eller flere prislister som er vedlagt i rutenettet Prosjektprislister i prosjektkontrakten, går du til kontroll 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontroll 2: Er noen av prislistene som er identifisert ovenfor, gyldige for den bestemte datoen til de faktiske utgiftene?

For at Project Service skal vurdere en prisliste for standardpris, må denne prislisten være gjeldende for datoen på de faktiske salgsutgiftene. Kontroller følgende for å se om prislisten(e) identifisert ovenfor er gjeldende:

- Start ved å kontrollere om start- og sluttdatoer i kategorien Generelt for prislistene som er tilknyttet, ikke er tomme. Hvis start- og sluttdatoene i prislistene identifisert ovenfor er tomme, vil du ha fastslått problemet. 
- Noter startdatofeltet for de faktiske salgsutgiftene og kontroller om noen av prislistene som er identifisert, er gjeldende for denne datoen. For eksempel bør datoen for faktiske utgifter være innenfor startdatoen og sluttdatoen i prislisten. 
    - Hvis det ikke er en prisliste som omfatter denne datoen i de faktiske salgsutgiftene, har du fastslått problemet. Endre start- og sluttdatoer for prislisten for å sikre at prislisten dekker datoen for faktiske utgifter. 
    - Hvis det er mer enn én prisliste som omfatter datoen i de faktiske salgsutgiftene, har du fastslått problemet. Rediger start- og sluttdatoene i prislisten(e) slik at det bare er én prisliste som omfatter datoen for de faktiske utgiftene. 
    - Hvis det er bare én prisliste som omfatter datoen for de faktiske utgiftene, kan du gå til kontroll 3.
Når du har gjort de nødvendige korrigeringene, oppretter du en utgiftsoppføring på nytt, godkjenner den, og kontrollerer at ufakturerte faktiske verdier for salg viser en gyldig pris.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontroll 3: Finnes det en gyldig pris for utgiftskategorien i gjeldende prosjektprisliste? 

Hvis du har fullført kontroll 1 og 2, skal du nå ha bare én prosjektprisliste som gjelder for datoen for de faktiske salgsutgiftene. Åpne prosjektprislisten og gå til kategorien Kategoripriser. Kontroller at det er en rad i rutenettet for den angitte utgiftskategorien i de faktiske utgiftene.
 
- Hvis det ikke er noen rad, har du fastslått problemet. Opprett en rad i Kategoripris-rutenettet for kategorien i de faktiske utgiftene. Opprett deretter en utgiftsoppføring på nytt, godkjenn den, og kontroller at ufakturerte faktiske verdier for salg viser en gyldig pris. 
- Hvis det er en rad for utgiftskategorien i rutenettet Kategoripriser, sjekker du om den har en gyldig pris.

For å forstå hva en gyldig pris er, bruker disse metodene:

- Hvis feltet Prismodell på Kategoripris-linjen er satt til Kostpris, blir enhetssatsen i de faktiske salgsutgiftene satt som standard til verdien i utgiftsoppføringen.
- Hvis feltet Prismodell på Kategoripris-linjen er satt til Påslagsprosent, kan du se om Prosent-feltet er satt til en gyldig verdi. Standard for enhetssatsen i de faktiske salgsutgiftene settes ved å bruke denne påslagsprosenten på prisen i utgiftsoppføringen.
- Hvis feltet Prismodell på Kategoripris-linjen er satt til Pris per enhet, kan du se om Pris-feltet er satt til en gyldig verdi. Enhetssatsen i de faktiske salgsutgiftene settes som standard til valutabeløpet som er angitt i Pris-feltet.

Hvis prisoppsettet for utgiftskategorien ikke er gyldig, har du fastslått problemet. Løsningen er å redigere kategoriprislinjen med en gyldig pris for utgiftskategorien i samsvar med reglene ovenfor. Når du har gjort dette, oppretter du en utgiftsoppføring på nytt, godkjenner den, og kontrollerer at ufakturerte faktiske verdier for salg får en gyldig pris.

Hvis du fremdeles ikke ser en gyldig pris i de faktiske salgsutgiftene når du har gjort de tre kontrollene ovenfor, logger du en støtteforespørsel.




[!INCLUDE[footer-include](../includes/footer-banner.md)]