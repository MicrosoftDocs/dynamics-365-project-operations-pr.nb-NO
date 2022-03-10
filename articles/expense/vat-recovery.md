---
title: Mva-fradrag i utgiftshåndtering
description: Dette emnet forklarer hvordan du mottar refusjoner for kvalifiserte mva-transaksjoner.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 64e9f4091fdf40cc702e83a165fe0a5be5043359348210bbe4afcd8a18055133
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999373"
---
# <a name="vat-recovery-in-expense-management"></a>Mva-fradrag i utgiftshåndtering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

For å motta refusjoner fra berettigede mva-transaksjoner må et firma eller en organisasjon identifisere, samle inn, kontrollere og sende inn nøyaktig informasjon. Denne prosessen inkluderer flere oppgaver og, avhengig av størrelsen på firmaet, kan inkludere flere ansatte eller roller.

For å oppnå mva-fradrag i modulen **Utgiftshåndtering** må følgende forhåndskrav være oppfylt:

- Mva-koder må være opprettet for land/områder som er tilordnet til utgiftskategorier.
- En mva-gruppe må være opprettet for hver avgiftskode.
- En mva-kode for varesalg må være opprettet for mva-gruppe.

Når forhåndskravene er oppfylt, må trinnene nedenfor fullføres for å be om refusjoner av mva-transaksjoner.

1. I en reiseregning angir du avgiftsinformasjon om kredittkorttransaksjoner for å identifisere kvalifiserte mva-refusjoner.
2. Kontroller at all avgiftsinformasjon er utfylt, og bokfør deretter reiseregningen.
3. Behandle utgifter som er berettiget til internasjonalt mva-fradrag.
4. Send data om VAT-fradrag til tredjepartsleverandøren for å søke om internasjonale fradragsreturer.
5. Behandle utgifter for innenlands mva-fradrag.

Avsnittene nedenfor inneholder eksempler som viser hvordan Contoso-ansatte fullfører hvert trinn.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Angi avgiftsinformasjon om kredittkorttransaksjoner for å identifisere kvalifiserte mva-refusjoner.

Gjertrud, en Contoso-salgsrepresentant som er basert i USA, returnerte nylig fra en salgsreise til Storbritannia. I løpet av turen påløpte det noen personlige kredittkortutgifter for måltider for Gjertrud. Gjertrud må nå opprette en reiseregning for å avstemme utgiftene.

Når Gjertrud angir informasjon i reiseregningen, velger hun **Storbritannia** i feltet **Land/område** på siden **Rediger reiseregning**. Listen over mva-grupper filtreres, slik at den bare viser gruppene som gjelder for Storbritannia. Gjertrud velger mva-gruppen **Storbritannia 001** og velger deretter mva-gruppen **Måltider**. Deretter legger Gjertrud til en ny transaksjon for overnatting. Fordi det bare er én mva-gruppe og én mva-gruppe for varesalg for overnatting i Storbritannia, fylles denne informasjonen automatisk ut i Gjertruds reiseregning.

Alle utgifter må ha en samsvarende kvittering per Contoso-policy. Når Gjertrud lagrer reiseregningen, mottar hun derfor en melding om at hun må legge ved en kvittering for hver transaksjon som hun har oppført i reiseregningen. Gjertrud bekrefter at hun har lagt ved et digitalt bilde av hver transaksjonskvittering i reiseregningen, og sender deretter rapporten til godkjenning. Deretter sender hun papirkvitteringene til behandlingsavdelingen på kontoret. Dette teamet sender dataene for mva-gjenoppretting til tredjepartsleverandøren som arkiverer internasjonale mva-gjenopprettingsreturer for Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Kontroller avgiftsinformasjon og poster en reiseregning

Før april kan koordinatoren for leverandørgjeld for Contoso postere en utgiftsrapport må hun angi avgiftsinformasjon som mangler. Hun åpner siden **Detaljer for reiseregning** og ser Gjertruds godkjente reiseregning. Anne åpner deretter reiseregningen for å vise detaljer om transaksjonene. Hun ser at Gjertrud ikke har angitt en mva-gruppe for en vare for én av transaksjonene. I og med at denne informasjonen ikke er oppgitt, kan ikke Anne postere reiseregningen. Hun ser derfor på siden **Avgiftskonfigurasjoner** i Utgiftshåndtering og finner riktig mva-gruppe for varen for landet/området og transaksjons typen. Anne kan nå postere reiseregningen til hovedboken.

Når Anne posterer reiseregningen, opprettes det et arbeidselement som er mva-fradragsberettiget. Dette arbeidselementet tilordnes til et medlem i behandlingsavdelingen på kontoret. Anne mottar en melding som bekrefter at bokføringen var vellykket. Denne meldingen viser også antall mva-transaksjoner som ble identifisert for fradrag.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Behandle utgifter som er berettiget til internasjonalt mva-fradrag

Arne, som er medlem av back office-behandlingsteamet hos Contoso, er ansvarlig for å bekrefte at all nødvendig informasjon om gjenfinning av merverdiavgift er inkludert i utgiftsrapporter. Han åpner siden **Avgiftsfradrag for utgifter** og velger reiseregningen som Gjertrud har sendt. Arne kontrollerer deretter at alle nødvendige kvitteringer er vedlagt, og at riktig mva-gruppe og mva-koder for varen er angitt.

Når Arni mottar papirkvitteringer fra Gjertrud, verifiserer han dem mot de digitale kvitteringene og endrer deretter statusen for reiseregningen til **Klar til fradrag**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Send data for mva-fradrag til tredjepartsleverandøren

Når Arne er klar til å sende reiseregningsdataene til tredjepartsleverandøren som vil arkivere mva-fradragsreturene, åpner han siden **Avgiftsfradrag for utgifter**. Han filtrerer siden slik at den bare viser reiseregningene som er merket som **Klar til fradrag**. Arne velger deretter **Fil** &gt; **Eksporter til Excel**. Mva-informasjonen fra reiseregningene eksporteres til et Microsoft Excel-regneark. Arne sender dette regnearket til tredjepartsleverandøren og inkluderer en melding som angir at papirkvitteringene er sendt via et transportbyrå.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Behandle utgifter for innenlands mva-fradrag

Arne må kontrollere at reiseregningstransaksjonene er kvalifisert for mva-fradrag, og at de digitale kvitteringene er vedlagt rapportene. For å begynne å behandle berettigede utgifter for innenlands fradrag åpner Arne siden **Avgiftsfradrag for utgifter** og velger reiseregningen som krever verifisering. Han verifiserer at kvitteringene står i navnet på firmaet i stedet for den ansatte. (For mva-fradrag må kvitteringer være i firmaets navn.) Arne kontrollerer deretter at riktig mva-gruppe og mva-koder for varen er angitt.

Når Arne mottar papirkvitteringene, endrer han statusen for reiseregningen til **Klar til fradrag**. Han kan deretter arkivere returen med de aktuelle skattemyndighetene. I dette tilfellet er de aktuelle skattemyndighetene i Norge Altinn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]