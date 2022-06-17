---
title: Transaksjonsopprinnelse – Koble faktiske verdier til kilden
description: Denne artikkelen forklarer hvordan konseptet med transaksjonsopprinnelse brukes til å koble faktiske verdier til opprinnelige kildeoppføringer, for eksempel tidsoppføring, utgiftsoppføring eller logg over materialbruk.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921314"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Transaksjonsopprinnelse – Koble faktiske verdier til kilden

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Oppføringer for transaksjonsopprinnelse opprettes for å koble faktiske verdier til kilden, for eksempel tidsoppføringer, utgiftsoppføringer, logger for materialbruk og prosjektfakturaer.

Følgende eksempel viser den typiske behandlingen av tidsoppføringer i en Project Operations-prosjektlivssyklus.

> ![Behandling av tidsoppføringer i Project Operations.](media/basic-guide-17.png)
 
1. Innsending av en tidsoppføring fører til at det opprettes to journallinjer: én for kostnad og én for ufakturert salg.
2. Eventuell godkjenning av tidsoppføringen fører til at det opprettes to faktiske verdier: én for kostnad og én for ufakturert salg.
3. Når brukeren oppretter en prosjektfaktura, opprettes fakturalinjetransaksjonen ved hjelp av data fra det faktiske salget som ikke er fakturert.
4. Når fakturaen er bekreftet, opprettes det to nye faktiske verdier: en tilbakeføring av en ordre som er fakturert, og et faktisk fakturert salg.

Hver hendelse i denne behandlingsarbeidsflyten utløser opprettelsen av oppføringer i transaksjonsopprinnelsesenheten for å bidra til å bygge en sporing av relasjonene mellom disse oppføringene som opprettes på tvers av tidsoppføringer, journallinjer, faktiske verdier og fakturalinjedetaljer.

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


Illustrasjonen nedenfor viser koblingene som opprettes mellom faktiske verdier og deres kilder ved ulike hendelser ved hjelp av eksemplet med tidsoppføringer i Project Operations.

> ![Hvordan faktiske verdier er koblet til kildeoppføringer i Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
