---
title: Koble faktiske verdier til opprinnelige oppføringer
description: Dette emnet forklarer hvordan du kobler faktiske verdier til opprinnelige oppføringer, for eksempel tidsregistrering, utgiftsregistrering eller logger for materialbruk.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852601"
---
# <a name="link-actuals-to-original-records"></a>Koble faktiske verdier til opprinnelige oppføringer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


I Dynamics 365 Project Operations er en *forretningstransaksjon* et abstrakt konsept som ikke representeres av en enhet. Noen felles felt og prosesser på enheter er imidlertid utformet for å bruke konseptet forretnings transaksjoner. Følgende enheter bruker dette konseptet:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Journallinjer
- Faktisk

Av disse enhetene er **tilbudslinjedetaljer**, **kontraktlinjedetaljer** og **estimatlinjer** tilordnet til estimatfasen i prosjektets livssyklus. Enhetene **Journallinjer** og **Faktiske enheter** tilordnes til utførelsesfasen i prosjektets livssyklus.

Project Operations gjenkjenner oppføringer i disse fem enhetene som forretningstransaksjoner. Den eneste forskjellen er at oppføringer i enhetene som er tilordnet til estimatfasen, betraktes som finansielle prognoser, mens oppføringer i enheter som er tilordnet til utførelsesfasen, betraktes som økonomiske fakta som allerede har forekommet.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsepter som er unike for forretningstransaksjoner
Følgende konsepter er unike for forretningstransaksjoner:

- Transaksjonstype
- Transaksjonsklasse
- Transaksjonsopprinnelse
- Transaksjonstilkobling

### <a name="transaction-type"></a>Transaksjonstype

Transaksjonstype representerer tidsberegningen og konteksten for den finansielle innvirkningen på et prosjekt. Dette representeres av et alternativsett som har følgende støttede verdier i Project Operations:

  - Kostnad
  - Prosjektkontrakt
  - Ufakturert salg
  - Fakturert salg
  - Salg mellom organisasjoner
  - Kostnad for ressursenhet

### <a name="transaction-class"></a>Transaksjonsklasse

Transaksjonsklasse representerer de forskjellige kostnadstypene som er påløpt for prosjekter. Dette representeres av et alternativsett som har følgende støttede verdier i Project Operations:

  - Tid
  - Utgift
  - Materiale
  - Gebyr
  - Milepæl
  - Avgift

**Milepæl** brukes vanligvis av forretningslogikken for fakturering med fast pris i Project Operations.

### <a name="transaction-origin"></a>Transaksjonsopprinnelse

**Transaksjonsopprinnelse** er en enhet som lagrer opprinnelsen til hver forretningstransaksjon. Etter hvert som et prosjekt kommer i gang, vil hver forretningstransaksjon forårsake en annen forretningstransaksjon, som i sin tur oppretter en ny og så videre. Enheten for transaksjonsopprinnelse er utformet for å lagre data om opprinnelsen til hver transaksjon for å bidra til rapportering og sporbarhet. 

### <a name="transaction-connection"></a>Transaksjonstilkobling

**Transaksjonstilkobling** er en enhet som lagrer relasjonen mellom to lignende forretningstransaksjoner, for eksempel kostnader og relaterte faktiske verdier for salg, eller transaksjonsannulleringer som utløses av faktureringsaktiviteter, for eksempel fakturabekreftelse eller fakturakorreksjoner.

Sammen hjelper **Transaksjonsopprinnelse** og **Transaksjonstilkobling** deg med å spore relasjoner mellom forretningstransaksjoner og handlinger som førte til en bestemt forretningstransaksjon.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Eksempel: slik fungerer transaksjonsopprinnelse sammen med transaksjonstilkobling

Følgende eksempel viser den typiske behandlingen av tidsoppføringer i en Project Operations-prosjektlivssyklus.

> ![Behandling av tidsoppføringer i Project Service-livssyklus](media/basic-guide-17.png)
 
1. Innsending av en tidsoppføring oppretter to journallinjer: én linje for kostnad og én linje for ufakturert salg.
2. Eventuell godkjenning av tidsoppføringen oppretter to faktiske verdier: én for kostnad og én for ufakturert salg.
3. Når en ny prosjektfaktura blir opprettet, opprettes fakturalinjetransaksjonen ved hjelp av data fra det faktiske salget som ikke er fakturert. 
4. Når fakturaen er bekreftet, opprettes det to nye faktiske verdier: en tilbakeføring av en ufakturert faktisk verdi og et faktisk fakturert salg.

Hver av disse hendelsene oppretter en oppføring i enhetene **Transaksjonsopprinnelse** og **Transaksjonstilkobling**. Disse nye oppføringene bidrar til å bygge en logg over relasjoner mellom oppføringene som opprettes mellom tidsoppføringene, journallinjen, faktiske verdier og fakturalinjedetaljer.

Tabellen nedenfor viser oppføringene i **Transaksjonsopprinnelse**-enheten for arbeidsflyten.

| Seminar/konferanse                        | Opprinnelse                   | Opprinnelsestype                       | Transaksjon                       | Transaksjonstype         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Innsending av tidsoppføring        | GUID for tidsoppføring   | Tidsoppføring                        | GUID for journallinjeoppføring (kostnad)   | Journallinje             |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for journallinjeoppføring (salg)  | Journallinje                      |                          |
| Tidsgodkjenning                | GUID for journallinjeoppføring | Journallinje                      | GUID for oppføring for ufakturert salg        | Faktisk                   |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for oppføring for ufakturert salg        | Faktisk                            |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for oppføring av faktisk kostnad           | Faktisk                            |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for oppføring av faktisk kostnad           | Faktisk                            |                          |
| Oppretting av faktura             | GUID for tidsoppføring   | Tidsoppføring                        | GUID for fakturalinjetransaksjon     | Fakturalinjetransaksjon |
| GUID for journallinjeoppføring     | Journallinje             | GUID for fakturalinjetransaksjon     | Fakturalinjetransaksjon          |                          |
| Fakturabekreftelse         | GUID for fakturalinje        | Fakturalinje                      | GUID for oppføring for fakturert salg          | Faktisk                   |
| GUID for faktura                 | Faktura                  | GUID for oppføring for fakturert salg          | Faktisk                            |                          |
| GUID for fakturalinjedetalj     | Fakturalinjedetalj      | GUID for oppføring for fakturert salg          | Faktisk                            |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for oppføring for fakturert salg          | Faktisk                            |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for oppføring for fakturert salg          | Faktisk                            |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for ufakturert salg omgjort      | Faktisk                            |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for ufakturert salg omgjort      | Faktisk                            |                          |
| Korrigering av fakturautkast     | Gammel ILD-GUID             | Fakturalinjetransaksjon          | GUID for korreksjons-ILD               | Fakturalinjetransaksjon |
| GUID for gammel IL                  | Fakturalinje             | GUID for korreksjons-ILD               | Fakturalinjetransaksjon          |                          |
| GUID for gammel faktura             | Faktura                  | GUID for korreksjons-ILD               | Fakturalinjetransaksjon          |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for korreksjons-ILD               | Fakturalinjetransaksjon          |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for korreksjons-ILD               | Fakturalinjetransaksjon          |                          |
| Bekreftet fakturakorreksjon | Gammel ILD-GUID             | Fakturalinjetransaksjon          | GUID for tilbakeført fakturert faktisk salg | Faktisk                   |
| GUID for gammel IL                  | Fakturalinje             | GUID for tilbakeført fakturert faktisk salg | Faktisk                            |                          |
| GUID for gammel faktura             | Faktura                  | GUID for tilbakeført fakturert faktisk salg | Faktisk                            |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for tilbakeført fakturert faktisk salg | Faktisk                            |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for tilbakeført fakturert faktisk salg | Faktisk                            |                          |
| Gammel ILD-GUID                 | Fakturalinjetransaksjon | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for gammel IL                  | Fakturalinje             | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for gammel faktura             | Faktura                  | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for tidsoppføring       | Tidsoppføring               | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for journallinjeoppføring     | Journallinje             | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for korreksjons-ILD          | Fakturalinjetransaksjon | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for korreksjons IL           | Fakturalinje             | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |
| GUID for fakturakorreksjon      | Faktura                  | GUID for nytt ufakturert faktisk salg    | Faktisk                            |                          |

Tabellen nedenfor viser oppføringene i **Transaksjonstilkobling**-enheten for arbeidsflyten.

| Seminar/konferanse                          | Transaksjon 1                 | Rolle for transaksjon 1 | Type for transaksjon 1           | Transaksjon 2                | Rolle for transaksjon 2 | Type for transaksjon 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Innsending av tidsoppføring          | GUID for journallinje (salg)     | Ufakturert salg     | msdyn_journalline            | GUID for journallinje (kostnad)     | Kostnad               | msdyn_journalline  |
| Tidsgodkjenning                  | GUID for ufakturert faktisk verdi (salg)  | Ufakturert salg     | msdyn_actual                 | GUID for faktisk kostnadsverdi (kostnad)       | Kostnad               | msdyn_actual       |
| Oppretting av faktura               | GUID for fakturalinjedetalj      | Fakturert salg       | msdyn_invoicelinetransaction | GUID for ufakturert faktisk salg   | Ufakturert salg     | msdyn_actual       |
| Fakturabekreftelse           | GUID for tilbakeføring av faktisk verdi         | Tilbakeføring          | msdyn_actual                 | GUID for opprinnelig ufakturert salg | Opprinnelig           | msdyn_actual       |
| GUID for fakturert salg              | Fakturert salg                  | msdyn_actual       | GUID for ufakturert faktisk salg   | Ufakturert salg               | msdyn_actual       |                    |
| Korrigering av fakturautkast       | GUID for fakturalinjetransaksjon | Erstatning          | msdyn_invoicelinetransaction | GUID for fakturert salg            | Opprinnelig           | msdyn_actual       |
| Bekreft fakturakorreksjon     | GUID for tilbakeføring av fakturert salg    | Tilbakeføring          | msdyn_actual                 | GUID for fakturert salg            | Opprinnelig           | msdyn_actual       |
| GUID for nytt ufakturert faktisk salg | Erstatning                     | msdyn_actual       | GUID for fakturert salg            | Opprinnelig                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
