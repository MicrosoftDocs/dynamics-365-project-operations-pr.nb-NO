---
title: Administrere flere kunder i et prosjekttilbud
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med tilbud som omfatter flere kunder som skal finansiere prosjektet.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 16cd07527fddd093748a18c1f7c900c8b32be85d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928214"
---
# <a name="manage-multiple-customers-on-a-project-quote"></a>Administrere flere kunder i et prosjekttilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjekttilbud støtter scenarioet der forslaget omfatter flere kunder som vil finansiere avtalen. Kategorien **Sammendrag** for tilbudet har feltet **Potensiell kunde** som identifiserer den primære kunden for avtalen. Andre kunder for avtalen kan konfigureres i kategorien **Kunder** i prosjekttilbudet.

Alle tilbudskunder i kategorien **Kunder** i prosjekttilbudet blir som standard tilbudslinjekunder på **nye** prosjektbaserte tilbudslinjer som er opprettet for tilbudet. Eksisterende prosjektbaserte tilbudslinjer arver ikke nye tilbudskundeoppføringer som er opprettet etter dem.

Tilbudskunder og tilbudslinjekunder kan når som helst legges til, oppdateres eller slettes før tilbudet er vunnet. En gyldig kunde i tilbudet må være definert som en kunde i det eiende firmaet eller den juridiske enheten på **Kunder**-siden. Juridiske enheter konfigureres i **Prosjektstyring og regnskaps**-modulen for Dynamics 365 Project Operations, og de er tilgjengelige som firmaer i **Prosjektsalg- og Levering**-modulene i Project Operations.

## <a name="concept-of-a-primary-customer"></a>Konseptet primær kunde

Kunden som er oppført i kategorien **Sammendrag** for prosjekttilbudet som potensiell kunde, er den primære kunden i tilbudet. Hvis du prøver å slette den primære kunden fra kundelisten i tilbudet, får du en feilmelding om at en primær kundeoppføring i et tilbud ikke kan slettes.

Den primære kunden bør ikke oppdateres fra kundelisten i tilbudet. Du kan imidlertid påvirke den primære kunden ved å endre den potensielle kunden i kategorien **Sammendrag** for tilbudet. Når dette feltet oppdateres i **tilbudssammendraget**, blir den nylig valgte potensielle kunden lagt til som en ny tilbudskunde med flagget **Primær** angitt. Den gamle potensielle kunden vil fremdeles være en kunde i tilbudet.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Opprette, oppdatere eller slette en oppføring av en tilbudskunde

En tilbuds kundekan opprettes, oppdateres eller slettes fra kategorien **Tilbudskunder** på **Tilbud**-siden. Feltene i tabellen nedenfor er på oppføringen av en tilbudskunde for et prosjekttilbud.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
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

Du kan også prøve å velge **Fordel jevnt** i delrutenettet til en tilbudskunde. Denne handlingen fordeler fakturadelinger til alle tilbudskunder. Hvis det finnes en avrundingsfaktor, blir denne lagt til for avrundingskunden. Én av tilbudskundene blir alltid merket som avrundingskunden. Dette betyr at oppføringen av tilbudskunden har flagget **Avrunding** satt til **Ja**. Dette er vanligvis den primære kunden i tilbudet, men dette kan endres.


[!INCLUDE[footer-include](../includes/footer-banner.md)]