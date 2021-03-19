---
title: Administrere flere kunder på prosjektbaserte tilbudslinjer – Lite
description: Dette emnet beskriver hvordan du administrerer flere kunder på prosjektbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0fde833ad6b13fc12b733d1aa9f3bba0cfd95b2b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273099"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines---lite"></a>Administrere flere kunder på prosjektbaserte tilbudslinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektbaserte tilbudslinjer støtter scenarioer der hver tilbudslinje har en liste over kunder som betaler for den. Denne listen over kunder på den prosjektbaserte tilbudslinjen kan være den samme som listen over kunder i tilbudet. Du kan også endre listen over kunder slik at de kan være forskjellige. Når et prosjekttilbud blir vunnet, kopieres kundelisten på den prosjektbaserte tilbudslinjen til den tilsvarende prosjektbaserte kontraktlinjen for å opprette den eventuelle prosjektkontrakten. Kunder i det prosjektbaserte tilbudet kopieres til prosjektkontrakten.

Når du fakturerer den eventuelle prosjektkontrakten, prioriteres kundelisten på den prosjektbaserte kontraktlinjen over listen på prosjektkontrakten. Kundelisten på prosjektkontrakten brukes bare for standardverdier på nye prosjektkontraktlinjer.

Alle tilbudskunder i kategorien **Kunder** i prosjekttilbudet blir som standard tilbudslinjekunder på nye prosjektbaserte tilbudslinjer som er opprettet for prosjekttilbudet. Ingen eksisterende prosjektbaserte tilbudslinjer arver nye tilbudskundeoppføringer som er opprettet etter dem.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Opprette, oppdatere eller slette en oppføring av en tilbudslinjekunde

Du kan opprette, oppdatere eller slette en tilbudslinjekunde i kategorien **Kunder for tilbudslinje** på siden **Prosjektbasert tilbudslinje**. Når du legger til en ny kunde på den prosjektbaserte tilbudslinjen, blir kunden også lagt til i det totale tilbudet som en tilbudskunde, med en standard faktureringsandelsprosent på 0 % av det totale tilbudet. Faktureringsadelsprosenten i det totale tilbudet kopieres til nye tilbudslinjer og til den eventuelle prosjektkontrakten. Når du fakturerer fra kontrakten, brukes imidlertid faktureringsandelsprosenten på tilbudslinjenivået, ikke faktureringsandelsprosenten på det totale kontraktnivået. 

Tabellen nedenfor viser feltene på oppføringen av en tilbudslinjekunde for en prosjektbasert tilbudslinje.

| Felt | Sted | Beskrivelse og veiledning | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Forretningsforbindelse** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Viser alle aktive kontoer. Dette feltet er låst etter at oppføringen er opprettet. Hvis du må oppdatere feltet, sletter du oppføringen og oppretter den på nytt. Hvis du har registrert faktiske verdier, kan du ikke slette oppføringen. | Når du velger en forretningsforbindelse fra hovedlisten over forretningsforbindelser som skal legges til, blir tilbudslinjekunden også lagt til som en tilbudskunde når du lagre den. Når et tilbud blir vunnet, kopieres tilbudslinjekunder til kunder på prosjektkontraktlinjen. |
| **Delingsprosent for fakturering** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Representerer prosentandelen av hver ikke-fakturerte salgstransaksjon som skal tilskrives denne tilbudslinjekunden. | Kopiert over til kunder for prosjektkontraktlinje. |
| **Må ikke overskrides-grense** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Angir om det finnes en avtalt grense eller et tak på totalbeløp som blir fakturert til denne kunden for denne tilbudslinjen. | Kopiert over til kunder for prosjektkontraktlinje når et tilbud er vunnet. |
| **Er avrunding** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Angir om denne kunden er en kunde med standard avrunding for denne prosjektbaserte tilbudslinjen. | Kopiert over til kunder i prosjektkontrakten når et tilbud er vunnet. |

## <a name="edit-billing-split-percentages"></a>Rediger delingsprosenter for fakturering

Du kan redigere delingsprosenter for fakturering på linjen. Hvis delingsprosentandelen for fakturering ikke er totalt 100 %, oppstår det en feil. Når du har redigert delingsprosentene for fakturering, oppdaterer du tilbudslinjesiden for å fjerne feilen.

Bruk handlingen for jevn fordeling i delrutenettet for tilbudslinjekunder til å fordele fakturingsandeler på alle tilbudslinjekunder. Hvis det finnes en avrundingsfaktor, blir denne lagt til for avrundingskunden. Én av tilbudslinjekundene er alltid merket som avrundingskunde, som betyr at oppføringen av tilbudslinjekunden har avrundingsflagget angitt til **Ja**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]