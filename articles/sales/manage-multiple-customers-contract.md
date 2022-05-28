---
title: Administrere flere kunder på prosjektkontrakter
description: Dette emnet gir informasjon om hvordan du administrerer flere kunder på en prosjektkontrakt.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bf8b0d313b2b07924d730fe8923b05559bbcc244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591324"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administrere flere kunder på prosjektkontrakter

Dette emnet gir informasjon om hvordan du administrerer flere kunder på en prosjektkontrakt. Du kan bruke en prosjektkontrakt når en kontraktavtale for flere kunder er nødvendig for å finansiere en avtale. På **Prosjektkontrakt**-siden, inneholder **Sammendrag**-fanen informasjon om den primære kunden for en avtale. Andre kunder som deltar i avtalen, kan legges til i **Kunder**-fanen.

Alle kontraktkunder i **Kunder**-fanen i prosjektkontrakten er som standard kontraktlinjekunder på eventuelle nye prosjektbaserte kontraktlinjer som opprettes for prosjektkontrakten. Eksisterende prosjektbaserte kontraktlinjer arver ikke nye kontraktkunderoppføringer som opprettes på et senere tidspunkt.

Du kan legge til, oppdatere eller slette kontraktkunder og kontraktlinjekunder når som helst før kontrakten blir vunnet. En kunde i prosjektkontrakten må defineres som en kunde i det eiende firmaet eller juridisk enhet på **Kunder**-siden. Juridiske enheter konfigureres i **Prosjektstyring og regnskaps**-modulen for Dynamics 365 Project Operations, og de er tilgjengelige som firmaer i **Prosjektsalg**- og **Levering**-modulene i Project Operations.

## <a name="primary-customers"></a>Primære kunder

Den potensielle kunden på **Sammendrag**-fanen for prosjektkontrakten er den primære kunden for kontrakten. Den primære kunden kan ikke oppdateres fra listen over kontraktkunder. Hvis du prøver å slette den primære kunden fra en kundeliste i kontrakten, får du en feilmelding om at en primær kundeoppføring på en kontrakt ikke kan slettes. I stedet endrer du kunden på **Potensiell kunde**-feltet på **Sammendrag**-fanen på prosjektkontrakten. Når du oppdaterer dette feltet, blir den nylig valgte kunden lagt til som en ny kontraktkunde med **Primær**-flagget angitt til **Ja**. Den forrige primære kunden er fremdeles en kunde i kontrakten, men er ikke lenger den primære kunden.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Opprette, oppdatere eller slette en oppføring for kontraktkunde

Du kan opprette, oppdatere eller slette en kontraktkunde fra **Kontraktkunder**-feltet på **Kontrakt**-siden. Følgende felt er inkludert på kontraktkundeoppføringen på en prosjektkontrakt.

| **Felt** | **Plassering** | **Beskrivelse** | 
| --- | --- | --- | 
| Konto | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Viser alle de aktive kontoene. Dette feltet er låst etter at oppføringen er opprettet. Hvis du vil oppdatere oppføringen, sletter du oppføringen og oppretter den på nytt. Hvis du har registrert faktiske verdier, eller hvis kontraktkundeoppføringen er en primær kunde, kan du ikke slette oppføringen. Kontraktkunder kopieres over som kontraktlinjekunder når det opprettes en kontraktlinje. |
| Delingsprosent for fakturering | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Representerer prosentandelen av hver ufakturerte salgstransaksjon som er tilordnet denne kontraktkunden. Når nye prosjektkontraktlinjer opprettes, kopieres faktureringsdelprosenten til nye kontraktlinjer som er opprettet og for kontraktlinjekunder i prosjektet. |
| Navn på kontakt for fakturering | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Dette tekstfeltet skal brukes til å identifisere fakturaens kontaktperson for kunden. Verdiene kommer fra den relaterte forretningsforbindelsesoppføringen som standard. Kontaktnavnet kopieres til **Fakturakontraktnavn** på fakturaen som genereres for kunden. |
| Fakturanavn | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Bruk dette feltet til å identifisere fakturaens kontaktperson for kunden. Verdiene kommer fra den relaterte forretningsforbindelsesoppføringen som standard. Navnet kopieres til **Fakturakontraktnavn**-feltet på fakturaen som genereres for kunden. |
| Betalingsbetingelser | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Verdiene kommer fra den relaterte forretningsforbindelsesoppføringen som standard. Betingelsene kopieres til **Fakturakontraktnavn** på fakturaen som genereres for kunden. |
| Eiende firma | Redigerbart rutenett på **Prosjektkontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en prosjektkontraktkunde. | Den juridiske enheten hvor kunden er satt opp i **Prosjektstyring og regnskap**-modulen. Dette feltet er skrivebeskyttet og er satt til det eiende firmaet i prosjektkontrakten.</br>Listen over kunder som skal legges til i **Forretningsforbindelse**-feltet, er allerede filtrert til listen fra det eiende firmaet i modulen **Prosjektstyring og regnskap** i Project Operations. Det eiende firmaet er identisk med den juridiske enheten i **Prosjektstyring og regnskap**-modulen i Project Operations. Alle kostnader og inntekter som belastes fra prosjektet, er gjort rede for i økonomimodulen i det eiende firmaet. |
| Er avrunding | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Angir om kunden er en standard avrundingskunde for avtalen. Det kan bare være én kunde for avrunding på en prosjektkontrakt. Når kostnader og ufakturerte salg deles på antall og leder til en avrundingsdifferanse, gjelder denne differansen for den faktiske verdien som er knyttet til kunden. |
| Må ikke overskrides-grense | Redigerbart rutenett på **Kontraktkunder**-fanen samt hoved- og hurtigopprettingssider for en kontraktkunde. | Angir om det er en forhandlet avgrensning eller øvre grense for totalt beløp som blir fakturert til kunden for engasjementet. Må ikke overskrides-grenseoppsettet på kontraktkundenivå evalueres basert på ufakturerte faktiske salg som refererer til kontraktkunden. |

## <a name="edit-billing-split-percentages"></a>Rediger delingsprosenter for fakturering

Du kan redigere delingsprosent for fakturering i rutenettet. Når delingsprosentene for fakturering ikke er totalt 100 prosent, oppstår det en feil. Når du har redigert en delingsprosent for fakturering, oppdaterer du **Prosjektkontrakt**-siden for å fjerne feilen.

Du kan også velge **Fordel jevnt** på delrutenettetet for kontraktlinjekundene. Faktureringsdelinger tildeles jevnt til alle kundene på prosjektkontrakten. Hvis det finnes en avrundingsfaktor, blir den lagt til avrundingskunden. En av kontraktkundene har alltid **Avrunding**-flagget angitt til **Ja**. Den kunden er avrundingskunden. En avrundingskunde er vanligvis den primære kunden i kontrakten, men det er ikke obligatorisk.


[!INCLUDE[footer-include](../includes/footer-banner.md)]