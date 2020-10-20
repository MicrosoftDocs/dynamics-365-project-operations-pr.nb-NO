---
title: Administrere flere kunder på prosjektbaserte tilbudslinjer
description: Dette emnet gir informasjon om hvordan du administrerer flere kunder på prosjektbaserte tilbudslinjer.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffb89a954b8af9d726c64cceeafca638c3393130
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965850"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Administrere flere kunder på prosjektbaserte tilbudslinjer

Prosjektbaserte tilbudslinjer støtter scenarioer der hver tilbudslinje har en liste over kunder som betaler for den. Denne listen over kunder på den prosjektbaserte tilbudslinjen kan være den samme som listen over kunder i tilbudet. Du kan også endre listen over kunder slik at de kan være forskjellige. Hvis du vil opprette den eventuelle prosjektkontrakten når et prosjekttilbud blir vunnet, kopieres kundelisten på den prosjektbaserte tilbudslinjen til den tilsvarende prosjektbaserte kontraktlinjen. Kunder i det prosjektbaserte tilbudet kopieres til prosjektkontrakten.

Når du fakturerer den eventuelle prosjektkontrakten, prioriteres kundelisten på den prosjektbaserte kontraktlinjen over listen på prosjektkontrakten. Kundelisten på prosjektkontrakten brukes bare til å sette nye prosjektkontraktlinjer som standard.

Alle tilbudskunder i kategorien **Kunder** i prosjekttilbudet blir som standard tilbudslinjekunder på nye prosjektbaserte tilbudslinjer som er opprettet for prosjekttilbudet. Ingen eksisterende prosjektbaserte tilbudslinjer arver nye tilbudskundeoppføringer som er opprettet etter dem.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Opprette, oppdatere eller slette en oppføring av en tilbudslinjekunde

Du kan opprette, oppdatere eller slette en tilbudslinjekunde i kategorien **Kunder for tilbudslinje** på siden **Prosjektbasert tilbudslinje**. Når du legger til en ny kunde på den prosjektbaserte tilbudslinjen, blir kunden også lagt til i det totale tilbudet som en tilbudskunde, med en standard faktureringsandelsprosent på 0 % av det totale tilbudet. Faktureringsadelsprosenten i det totale tilbudet kopieres til nye tilbudslinjer og til den eventuelle prosjektkontrakten. Når du fakturerer fra kontrakten, brukes imidlertid faktureringsandelsprosenten på tilbudslinjenivået, ikke faktureringsandelsprosenten på det totale kontraktnivået. 

Tabellen nedenfor viser feltene på oppføringen av en tilbudslinjekunde for en prosjektbasert tilbudslinje.

| Felt | Sted | Beskrivelse og veiledning | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Forretningsforbindelse** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Viser alle aktive kontoer. Dette feltet er låst etter at oppføringen er opprettet. Hvis du må oppdatere feltet, sletter du oppføringen og oppretter den på nytt. Hvis du har registrert faktiske verdier, kan du ikke slette oppføringen. | Når du velger en forretningsforbindelse fra hovedlisten over forretningsforbindelser som skal legges til, blir tilbudslinjekunden også lagt til som en tilbudskunde. Tilbudslinjekunder kopieres til kunder på prosjektkontraktlinjen når et tilbud blir vunnet. |
| **Delingsprosent for fakturering** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Representerer prosentandelen av hver ikke-fakturerte salgstransaksjon som skal tilskrives denne tilbudslinjekunden. | Kopiert over til kunder for prosjektkontraktlinje. |
| **Må ikke overskrides-grense** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Angir om det finnes en avtalt grense eller et tak på totalbeløp som blir fakturert til denne kunden for denne tilbudslinjen. | Kopiert over til kunder for prosjektkontraktlinje når et tilbud er vunnet. |
| **Eiende firma** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Den juridiske enheten som denne kunden er konfigurert for, i modulen **Prosjektstyring og regnskap**. Dette feltet er skrivebeskyttet og er satt til eiende firma for selve tilbudet. Listen over kunder som skal legges til i **Forretningsforbindelse**-feltet, er allerede filtrert til listen fra det eiende firmaet i modulen **Prosjektstyring og regnskap** i Project Operations. | Det eiende firmaet tilsvarer konseptet juridisk enhet. Alle kostnader og inntekter som er påløpt fra dette prosjektet, blir regnskapsført i hovedboken til det eiende firmaet. |
| **Er avrunding** | Et redigerbart rutenett i kategorien **Kunder for tilbudslinje**, hovedskjemaet og hurtigopprettingsskjemaet for en tilbudslinjekunde. | Angir om denne kunden er en kunde med standard avrunding for denne prosjektbaserte tilbudslinjen. | Kopiert over til kunder i prosjektkontrakten når et tilbud er vunnet. |

## <a name="edit-billing-split-percentages"></a>Rediger delingsprosenter for fakturering

Du kan redigere delingsprosenter for fakturering på linjen. Hvis delingsprosentandelen for fakturering ikke er totalt 100 %, oppstår det en feil. Når du har redigert delingsprosentene for fakturering, oppdaterer du tilbudslinjesiden for å fjerne feilen.

Bruk handlingen for jevn fordeling i delrutenettet for tilbudslinjekunder til å fordele fakturingsandeler på alle tilbudslinjekunder. Hvis det finnes en avrundingsfaktor, blir denne lagt til for avrundingskunden. Én av tilbudslinjekundene er alltid merket som avrundingskunde, som betyr at oppføringen av tilbudslinjekunden har avrundingsflagget angitt til **Ja**. 
