---
title: Administrere flere kunder på prosjektkontrakter – Lite
description: Dette emnet gir informasjon om behandling av flere kunder på prosjektkontrakter.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 015e407b1b9e464edec1e57ce6b5132f21f5ae6d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593072"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Administrere flere kunder på prosjektkontrakter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektkontrakter i Dynamics 365 Project Operations støtter scenariet der en kontraktstmessig avtale innebærer flere kunder som er finansiering for en avtale. Kategorien **Sammendrag** på siden **Prosjektkontrakt** inkluderer feltet **Kunde**. Dette feltet identifiserer hovedkunden for avtalen. Andre kunder for avtalen kan konfigureres i kategorien **Kunder** på siden **Prosjektkontrakt**.

Alle kontraktkunder som er oppført i prosjektkontrakten er som standard kontraktlinjekunder på eventuelle nye prosjektbaserte kontraktlinjer som opprettes for prosjektkontrakten. Eksisterende prosjektbaserte kontraktlinjer arver ikke nye kontraktkunder fordi nye oppføringer opprettes.

Produktbaserte kontraktlinjer knyttes automatisk til den primære kunden.

Kontraktkunder og kontraktlinjekunder kan legges til, oppdateres eller slettes når som helst før kontrakten blir vunnet.

## <a name="primary-customer"></a>Primær kunde

Kunden som er oppført i kategorien **Sammendrag** for prosjektkontrakten som den potensielle kunden, er den primære kunden for kontrakten. Når du prøver å slette den primære kunden fra kundelisten i kontrakten, får du en feilmelding om at en primær kundeoppføring på en kontrakt ikke kan slettes.

Den primære kunden kan ikke oppdateres fra listen over kontraktkunder. I stedet endrer du den potensielle kunden i kategorien **Sammendrag** for kontrakten. Når dette feltet oppdateres på siden **Kontraktsammendrag**, blir den nye kunden lagt til som en ny kontraktkunde med flagget **Primær** angitt. Den forrige primære kunden vil fremdeles være en kunde i kontrakten.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Opprette, oppdatere eller slette en oppføring for kontraktkunde

En kontraktkunde kan opprettes, oppdateres eller slettes fra kategorien **Kunder** på siden **Prosjektkontrakt**. Feltene i tabellen nedenfor er i kontraktkundeoppføringen for en prosjektkontrakt og bør beholdes når du arbeider med kontrakten.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Forretningsforbindelse** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde. | Viser alle de aktive kontoene. Dette feltet er låst etter at oppføringen er opprettet. Hvis du vil oppdatere kontoen, sletter du oppføringen og oppretter den på nytt. Hvis du har registrert faktiske verdier, eller hvis kontraktkundeoppføringen er en primær kunde, kan du ikke slette oppføringen. | Kontraktkunder kopieres over som kontraktlinjekunder når det opprettes en kontraktlinje. |
| **Delingsprosent for fakturering** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde. | Representerer prosentandelen av hver ikke-fakturerte salgstransaksjon som skal skrives til denne kontraktkunden. | Kopieres over til nye kontraktlinjer og prosjektkontraktlinjekunder på nye prosjektkontraktlinjer. |
| **Navn på kontakt for fakturering** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde. | Dette tekstfeltet bør brukes til å identifisere fakturakontaktpersonen for denne kunden. Dette feltet bruker den relaterte forretningsforbindelsesoppføringen som standard. | Kopieres til feltet **Faktureres til kontraktnavn** i fakturaen som genereres for denne kunden. |
| **Fakturanavn** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde | Dette tekstfeltet bør brukes til å identifisere fakturakontaktpersonen for denne kunden. Dette feltet bruker den relaterte forretningsforbindelsesoppføringen som standard. | Kopieres til feltet **Faktureres til kontraktnavn** i fakturaen som genereres for denne kunden. |
| **Betalingsbetingelser** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde. | Verdiene bruker den relaterte forretningsforbindelsesoppføringen som standard. | Kopieres til feltet **Faktureres til kontraktnavn** i fakturaen som genereres for denne kunden. |
| **Er avrunding** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde. | Angir om denne kunden er en standard avrundingskunde for denne avtalen. Det kan bare være én kunde for avrunding på en prosjektkontrakt. | Når kostnader og ufakturerte salg deles på antall potensielle kunder til en avrundingsdifferanse, gjelder denne differansen for den faktiske verdien som er knyttet til denne kunden. |
| **Må ikke overskrides-grense** | Rutenettet kan redigeres i kategorien **Kontraktlinjekunder** og skjemaene **Hoved** og **Hurtigoppretting** for en kontraktkunde | Angir om det er en forhandlet avgrensning eller øvre grense for totalt beløp som blir fakturert til kunden for dette engasjementet. | Oppsettet for **Må ikke overskrides-grense** på kontraktkundenivå evalueres på **Ufakturerte faktiske verdier** som refererer til denne kontraktkunden. |

## <a name="edit-billing-split-percentages"></a>Rediger delingsprosenter for fakturering

Delingsprosent for fakturering kan redigeres i rutenettet. Når delingsprosentene for fakturering ikke er totalt 100 prosent, oppstår det en feil. Når du har redigert delingsprosentene for fakturering, oppdaterer du siden for å lukke feilen.

Du kan også velge **Fordel jevnt** i rutenettet **Kontraktkunder** for å fordele fakturadelingene jevnt til alle kontraktkunder. Hvis det finnes en avrundingsfaktor, blir den lagt til i avrundingskunden. En av kontraktskundene blir alltid merket som kunde for **avrunding**, noe som betyr at avrundingsflagget er satt til **Ja** i kontraktkundeoppføringen. Dette er vanligvis hovedkunden til kontrakten, men den kan også endres.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]