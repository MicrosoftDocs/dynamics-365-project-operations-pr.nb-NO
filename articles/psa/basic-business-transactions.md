---
title: Forretningstransaksjoner
description: Dette emnet inneholder informasjon om forretningstransaksjoner.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987538"
---
# <a name="business-transactions"></a>Forretningstransaksjoner

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation er *forretningstransaksjon* et abstrakt konsept som ikke representeres av en enhet. Noen felles felt og prosesser på enheter er imidlertid utformet for å bruke konseptet forretnings transaksjoner. Følgende enheter bruker denne abstraksjonen:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Journallinjer
- Faktisk

Av disse entitetene tilordnes tilbudslinjedetaljer, kontraktlinjedetaljer og estimatlinjer til beregningsfasen i prosjektets livssyklus. Enhetene Journallinjer og Faktiske enheter tilordnes til utførelsesfasen i prosjektets livssyklus.

PSA behandler oppføringer i disse fem enhetene som forretningstransaksjoner. Den eneste forskjellen er at oppføringer i enheter som er tilordnet til beregningsfasen, betraktes som finansielle prognoser, mens oppføringer i enheter som er tilordnet til utførelsesfasen, betraktes som økonomiske fakta som allerede har forekommet.

Hvis du vil ha mer informasjon, se [Estimater](estimates.md) og [Faktiske verdier](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsepter som er unike for forretningstransaksjoner
Følgende konsepter er unike for forretningstransaksjoner:

- Transaksjonstype
- Transaksjonsklasse
- Transaksjonsopprinnelse
- Transaksjonstilkobling

### <a name="transaction-type"></a>Transaksjonstype

Transaksjonstype representerer tidsberegningen og konteksten for den finansielle innvirkningen på et prosjekt. Den representeres av et alternativsett som har følgende støttede verdier i PSA:
- Kostnad
- Prosjektkontrakt
- Ufakturert salg
- Fakturert salg
- Salg mellom organisasjoner
- Kostnad for ressursenhet

### <a name="transaction-class"></a>Transaksjonsklasse

Transaksjonsklasse representerer de forskjellige kostnadstypene som er påløpt for prosjekter. Den representeres av et alternativsett som har følgende støttede verdier i PSA:

- Time
- Utgift
- Materiale
- Gebyr
- Milepæl
- Avgift

**Milepæl**-verdien brukes vanligvis av forretningslogikken for fakturering med fast pris i PSA.

### <a name="transaction-origin"></a>Transaksjonsopprinnelse

Transaksjonsopprinnelse er en enhet som lagrer opprinnelsen til hver forretningstransaksjon. Etter hvert som prosjektutførelsen kommer i gang, gir hver forretningstransaksjon en økning for en annen forretningstransaksjon som i sin tur oppretter en ny, og så videre. Enheten for transaksjonsopprinnelse ble utformet for å lagre data om opprinnelsen til hver transaksjon, for å bidra til rapportering og sporing. 

### <a name="transaction-connection"></a>Transaksjonstilkobling

Transaksjonstilkobling er en enhet som lagrer relasjonen mellom to lignende forretningstransaksjoner, for eksempel kostnader og relaterte faktiske verdier for salg, eller transaksjonsannulleringer som utløses av faktureringsaktiviteter, for eksempel fakturabekreftelse eller fakturakorreksjoner.

Sammen hjelper transaksjonsopprinnelsen og transaksjonstilkoblingen deg med å holde oversikt over relasjoner mellom forretningstransaksjoner og handlinger som førte til oppretting av en bestemt forretningstransaksjon.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Eksempel: slik fungerer transaksjonsopprinnelse sammen med transaksjonstilkobling

Følgende eksempel viser den typiske behandlingen av tidsoppføringer i en PSA-prosjektlivssyklus.

> ![Behandling av tidsoppføringer i Project Service-livssyklus.](media/basic-guide-17.png)
 
1. Innsending av en tidsoppføring fører til at det opprettes to journallinjer: én for kostnad og én for ufakturert salg.
2. Eventiell godkjenning av tidsoppføringen fører til at det opprettes to faktiske verdier: én for kostnad og én for ufakturert salg.
3. Når brukeren oppretter en prosjektfaktura, opprettes fakturalinjetransaksjonen ved hjelp av data fra det faktiske salget som ikke er fakturert. 
4. Når fakturaen er bekreftet, opprettes det to nye faktiske verdier: en tilbakeføring av en ordre som er fakturert, og et faktisk fakturert salg.

Hver av disse hendelsene utløser opprettelsen av oppføringer i transaksjonsopprinnelsen og transaksjonstilkoblingen for å bidra til å bygge en sporing av relasjoner mellom disse oppføringene som opprettes på tvers av en tidsoppføringer, journallinjer, faktiske verdier og fakturalinjedetaljer.

Tabellen nedenfor viser oppføringene i Transaksjonsopprinnelse-enheten for den foregående arbeidsflyten.

| Hendelse                        | Opprinnelse                   | Opprinnelsestype                       | Transaksjon                       | Transaksjonstype         |
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

Tabellen nedenfor viser oppføringene i Transaksjonstilkobling-enheten for den foregående arbeidsflyten.

| Hendelse                          | Transaksjon 1                 | Rolle for transaksjon 1 | Type for transaksjon 1           | Transaksjon 2                | Rolle for transaksjon 2 | Type for transaksjon 2 |
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