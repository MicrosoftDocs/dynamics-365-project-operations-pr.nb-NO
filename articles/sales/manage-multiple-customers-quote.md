---
title: Administrere flere kunder i prosjekttilbud
description: Dette emnet inneholder informasjon om å arbeide med tilbud som involverer flere kunder som vil finansiere prosjektet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908434"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Administrere flere kunder i prosjekttilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjekttilbud støtter scenarioet der forslaget omfatter flere kunder som vil finansiere avtalen. Kategorien **Sammendrag** for tilbudet har feltet **Potensiell kunde** som identifiserer den primære kunden for avtalen. Andre kunder for avtalen kan konfigureres i kategorien **Kunder** i prosjekttilbudet.

Alle tilbudskunder i kategorien **Kunder** i prosjekttilbudet blir som standard tilbudslinjekunder på **nye** prosjektbaserte tilbudslinjer som er opprettet for tilbudet. Eksisterende prosjektbaserte tilbudslinjer arver ikke nye tilbudskundeoppføringer som er opprettet etter dem.

Tilbudskunder og tilbudslinjekunder kan når som helst legges til, oppdateres eller slettes før tilbudet er vunnet. En gyldig kunde i tilbudet må være definert som en kunde i det eiende firmaet eller den juridiske enheten på **Kunder**-siden. Juridiske enheter konfigureres i modulen **Prosjektstyring og regnskap** i Dynamics 365 Project Operations og blir gjort tilgjengelig som firmaer i modulen **Prosjektsalg og levering** i Project Operations.

## <a name="concept-of-a-primary-customer"></a>Konseptet primær kunde

Kunden som er oppført i kategorien **Sammendrag** for prosjekttilbudet som potensiell kunde, er den primære kunden i tilbudet. Hvis du prøver å slette den primære kunden fra kundelisten i tilbudet, får du en feilmelding om at en primær kundeoppføring i et tilbud ikke kan slettes.

Den primære kunden bør ikke oppdateres fra kundelisten i tilbudet. Du kan imidlertid påvirke den primære kunden ved å endre den potensielle kunden i kategorien **Sammendrag** for tilbudet. Når dette feltet oppdateres i **tilbudssammendraget**, blir den nylig valgte potensielle kunden lagt til som en ny tilbudskunde med flagget **Primær** angitt. Den gamle potensielle kunden vil fremdeles være en kunde i tilbudet.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Opprette, oppdatere eller slette en oppføring av en tilbudskunde

En tilbuds kundekan opprettes, oppdateres eller slettes fra kategorien **Tilbudskunder** på **Tilbud**-siden. Feltene i tabellen nedenfor er på oppføringen av en tilbudskunde for et prosjekttilbud.

| **Felt** | **Plassering** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Konto | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Viser alle de aktive kontoene. Dette feltet er låst etter at oppføringen er opprettet. Hvis du vil oppdatere det, sletter du oppføringen og oppretter den på nytt. Hvis du har registrert faktiske verdier, eller hvis tilbudskundeoppføringen er en primær kunde, kan du slette oppføringen. | Tilbudskunder kopieres over som tilbudslinjekunder når en tilbudslinje opprettes. Tilbudskunder kopieres også over til prosjektkontraktkundene når et tilbud blir vunnet. |
| Delingsprosent for fakturering | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Representerer prosentandelen av hver ikke-fakturerte salgstransaksjon som skal tilskrives denne tilbudskunden. | Kopiert over til nye tilbudslinjer som er opprettet, og til prosjektkontraktkunder. |
| Navn på kontakt for fakturering | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Dette er et tekstfelt og bør brukes til å identifisere fakturakontaktpersonen for denne kunden. Disse hentes som standard fra oppføringen for den relaterte forretningsforbindelsen | Kopieres til prosjektkontraktkunder når et tilbud blir vunnet og i sin tur til slutt til navnefeltet Faktura til kontrakt på fakturaen som er generert for denne kunden. |
| Fakturanavn | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Dette tekstfeltet bør brukes til å identifisere fakturakontaktpersonen for denne kunden. | Kopieres til prosjektkontraktkunden når et tilbud blir vunnet og i sin tur til til slutt til feltet **Faktura til kontraktnavn** på fakturaen som er generert for denne kunden. |
| Betalingsbetingelser | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Dette er et alternativsett med verdier som er standard fra oppføringen for den relaterte forretningsforbindelsen. | Kopieres til prosjektkontraktkunden når et tilbud blir vunnet og i sin tur til til slutt til feltet **Faktura til kontraktnavn** på fakturaen som er generert for denne kunden. |
| Er avrunding | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Angir om denne kunden er en standard avrundingskunde for denne avtalen. | Kopiert til kundene i prosjektkontrakten når et tilbud er vunnet. |
| Eiende firma | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Den juridiske enheten som denne kunden er konfigurert med, i modulen **Prosjektstyring og regnskap**. Dette feltet er skrivebeskyttet og er satt til eiende firma for selve tilbudet. Listen over kunder som skal legges til i **Forretningsforbindelse**-feltet, er allerede filtrert til listen fra dette eiende firmaet i modulen **Prosjektstyring og regnskap** i Project Operations. | Det eiende firmaet tilsvarer konseptet juridisk enhet i modulen **Prosjektstyring og regnskap** i Project Operations. Alle kostnader og inntekter som påløper fra dette prosjektet, blir regnskapsført i hovedboken til det eiende firmaet. |
| Må ikke overskrides-grense | Redigerbart rutenett i kategorien **Tilbudskunder** og skjemaene **Hoved** og **Hurtigoppretting** for en tilbudskunde. | Angir om det finnes en avtalt grense eller et tak på totalbeløp som blir fakturert til denne kunden for dette engasjementet. | Kopiert til kundene i prosjektkontrakten når et tilbud er vunnet. |

## <a name="editing-billing-split-percentages"></a>Redigere delingsprosenter for fakturering

Du kan redigere delingsprosentene for fakturering ved hjelp av den innebygde redigeringsopplevelsen i rutenettet. Hvis delingsprosentandelen for fakturering ikke er totalt 100 %, oppstår det en feil. Når du har oppdatert delingsprosentene for fakturering, oppdaterer siden for å fjerne feilen.

Du kan også prøve å velge **Fordel jevnt** i delrutenettet for tilbudskunden. Denne handlingen fordeler fakturadelinger til alle tilbudskunder. Hvis det finnes en avrundingsfaktor, blir denne lagt til for avrundingskunden. Én av tilbudskundene blir alltid merket som avrundingskunden. Dette betyr at oppføringen av tilbudskunden har flagget **Avrunding** satt til **Ja**. Dette er vanligvis den primære kunden i tilbudet, men dette kan endres.