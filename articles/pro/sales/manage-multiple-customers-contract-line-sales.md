---
title: Administrere flere kunder på prosjektbaserte kontraktlinjer – Lite
description: Dette emnet gir informasjon om behandling av flere kunder på prosjektbaserte kontraktlinjer.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9dfaa766f3d6064bb84dcd1b032e0e279b1b9cdf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273255"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Administrere flere kunder på prosjektbaserte kontraktlinjer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektbaserte kontraktlinjer kan inneholde en liste over kunder som er ansvarlig for betalingen. Denne listen over kunder på den prosjektbaserte kontraktlinjen kan være den samme som listen over kunder i kontrakten, men det kreves ikke. Når et prosjekttilbud blir vunnet, og det opprettes en prosjektkontrakt, kopieres kundelisten på tilbudslinjen til den tilsvarende kontraktlinjen. Kunder i tilbudet kopieres til kontrakten.

Når prosjektkontrakten er fakturert, prioriteres kundelisten på den prosjektbaserte kontraktlinjen over kundelisten på kontrakten. Kundelisten på prosjektkontrakten brukes bare som standard for nye kontraktlinjer.

Alle kontraktkunder i kategorien **Kunder** i prosjektkontrakten er som standard kontraktlinjekunder på eventuelle nye kontraktlinjer som opprettes for prosjektkontrakten. Eventuelle eksisterende kontraktlinjer arver ikke de nye kontraktkundeoppføringene som opprettes etterpå.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Opprette, oppdatere eller slette en oppføring for kontraktlinjekunde

Du kan opprette, oppdatere eller slette en kontraktlinjekunde fra kategorien Kontraktlinjekunder på siden Prosjektbaserte kontraktlinjer. Når en ny kunde legges til på den prosjektbaserte kontraktlinjen, blir de også lagt til i den totale kontrakten som en kontraktkunde med en standard delingsprosent for fakturering på null prosent. Delingsprosent for fakturering for den totale kontrakten kopieres til nye kontraktlinjer og til den endelige prosjektkontrakten. Ved fakturering fra kontrakten er det imidlertid delingsprosenten for fakturering på kontraktlinjenivået som brukes, og ikke delingsprosent for fakturering på det samlede kontraktnivået.

Nedenfor vises feltene på **Kontrakt**-linjekundeoppføringen for en prosjektbasert kontraktlinje som må huskes når du arbeider med den:

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Forretningsforbindelse** | Redigerbart rutenett i kategorien **Kontraktkunder** og **Hoved**- og **Hurtigoppretting**-skjemaer for en kontraktkunde. | Alle aktive forretningsforbindelser. Dette feltet er låst etter at oppføringen er opprettet. Hvis du vil oppdatere feltet, sletter du oppføringen og oppretter en ny oppføring. Hvis du har registrert faktiske verdier, kan du ikke slette oppføringen. Du kan imidlertid merke av for delingsprosent for fakturering som null for forretningsforbindelsen. Når oppføringen er merket som null, berøres eventuelle fremtidige faktiske kostnader og inntekter som er knyttet til eller delt med denne kunden. | Når du velger en forretningsforbindelse fra hovedlisten over forretningsforbindelser som skal legges til og lagres, blir kontraktlinjekunden også lagt til som en kontraktkunde. Kontraktlinjekunder brukes ved generering av fakturaer. |
| **Delingsprosent for fakturering** | Redigerbart rutenett i kategorien **Kontraktkunder** og **Hoved**- og **Hurtigoppretting**-skjemaer for en kontraktkunde. | Dette feltet viser prosentandelen av hver ikke-fakturerte salgstransaksjon som skal skrives til denne kontraktlinjekunden. | Kontraktlinjekunder og delingsprosent for fakturering brukes når faktiske verdier opprettes etter godkjenning, og når fakturaen er generert. |
| **Må ikke overskrides-grense** | Redigerbart rutenett i kategorien **Kontraktkunder** og **Hoved**- og **Hurtigoppretting**-skjemaer for en kontraktkunde. | Angir om det er en forhandlet avgrensning eller øvre grense for totalt beløp som blir fakturert til denne kunden for kontraktlinjen. | Må ikke overskrides-grensen for kontraktlinjekunden brukes når faktiske verdier opprettes og fakturaene genereres. |
| **Er avrunding** | Redigerbart rutenett i kategorien **Kontraktkunder** og **Hoved**- og **Hurtigoppretting**-skjemaer for en kontraktkunde. | Dette feltet angir om kunden er en standard avrundingskunde for denne prosjektbaserte kontraktlinjen. | Når du genererer en faktisk verdi i henhold til delingsprosent for fakturering, kan det oppstå avrundingsdifferanser. Denne kunden får avrundingsdifferansene i dette tilfellet. |

## <a name="edit-billing-split-percentages"></a>Rediger delingsprosenter for fakturering

Delingsprosent for fakturering kan redigeres i rutenettet. Når delingsprosentene for fakturering ikke er totalt 100 prosent, oppstår det en feil. Når du har redigert delingsprosentene for fakturering, oppdaterer du siden for å fjerne feilen.

Du kan også velge **Fordel jevnt** i delrutenettetet for kontraktlinjekunde. Denne handlingen fordeler faktureringsdelingene til alle kontraktlinjekunder. Hvis det finnes en avrundingsfaktor, blir den lagt til i avrundingskunden. Én kontraktlinjekunde er alltid merket som **Avrunding**-kunden med **Avrunding**-flagget satt til **Ja**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]