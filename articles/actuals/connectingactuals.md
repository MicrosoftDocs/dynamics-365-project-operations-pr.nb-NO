---
title: Transaksjonstilkoblinger – Koble faktiske data for forskjellige transaksjonstyper
description: Denne artikkelen forklarer hvordan en transaksjonstilkobling brukes til å koble faktiske data av forskjellige typer for å spore lønnsomhet, faktureringsrestanse og beregning av fakturert kontra ufakturert inntekt.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926098"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Transaksjonstilkoblinger – Koble faktiske data for forskjellige transaksjonstyper

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Oppføringer for transaksjonstilkoblinger opprettes for å koble faktiske data av forskjellige typer etter hvert som tids-, utgifts- eller materialbruk flyttes i livssyklusen fra tilbudet eller fasen før salg til kontraktfasen, godkjenninger og/eller tilbakekallinger, fakturering og potensielt kreditering eller korrigering av fakturering.

Følgende eksempel viser den typiske behandlingen av tidsoppføringer i en Project Operations-prosjektlivssyklus.

> ![Behandling av tidsoppføringer i Project Operations.](media/basic-guide-17.png)

Behandlingen av tidsoppføringer i en Project Operations-prosjektlivssyklus følger disse trinnene: 

1. Innsending av en tidsoppføring fører til at det opprettes to journallinjer: én for kostnad og én for ufakturert salg. 
2. Eventuell godkjenning av tidsoppføringen fører til at det opprettes to faktiske verdier: én for kostnad og én for ufakturert salg. Disse to faktiske verdiene er koblet sammen ved hjelp av transaksjonstilkoblinger.
3. Når brukeren oppretter en prosjektfaktura, opprettes fakturalinjetransaksjonen ved hjelp av data fra det faktiske salget som ikke er fakturert.
4. Når fakturaen er bekreftet, oppretter dette to nye faktiske verdier: en tilbakeføring av en ordre som er fakturert, og et faktisk fakturert salg. Den uredigerte tilbakeføringen av salg og det opprinnelige faktiske salget er tilkoblet ved hjelp av tilbakeføring av transaksjonstilkoblinger. Det fakturerte salget og de opprinnelige ufakturerte faktiske salgene er også tilkoblet for å vise koblingene mellom det som en gang var restanse eller WIP-inntekt (pågående arbeid), til det som nå er fakturert inntekt.   

Hver hendelse i behandlingsarbeidsflyten utløser oppretting av oppføringer i tabellen **Transaksjonstilkobling**. Dette bidrar til å bygge en sporing av relasjonene mellom oppføringene som opprettes mellom tidsoppføringen, den faktiske verdien og fakturalinjedetaljene.

Tabellen nedenfor viser oppføringene i **Transaksjonstilkobling**-enheten for den foregående arbeidsflyten.

|Hendelse                   |Transaksjon 1                 |Rolle for transaksjon 1 |Type for transaksjon 1       |Transaksjon 2          |Rolle for transaksjon 2 |Type for transaksjon 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Innsending av tidsoppføring   |GUID for journallinje (salg)     |Ufakturert salg |msdyn_journalline            |GUID for journallinje (kostnad)     |Kostnad            |msdyn_journalline  |
|Tidsgodkjenning           |GUID for ufakturert faktisk verdi (salg)  |Ufakturert salg |msdyn_actual                 |GUID for faktisk kostnadsverdi (kostnad)       |Kostnad            |msdyn_actual       |
|Oppretting av faktura        |GUID for fakturalinjedetalj      |Fakturert salg   |msdyn_invoicelinetransaction |GUID for ufakturert faktisk salg   |Ufakturert salg  |msdyn_actual       |
|Fakturabekreftelse    |GUID for tilbakeføring av faktisk verdi         |Tilbakeføring      |msdyn_actual                 |GUID for opprinnelig ufakturert salg |Opprinnelig        |msdyn_actual       |
|                        |GUID for fakturert salg             |Fakturert salg   |msdyn_actual                 |GUID for ufakturert faktisk salg   |Ufakturert salg  |msdyn_actual       |
|Korrigering av fakturautkast |GUID for fakturalinjetransaksjon|Erstatning      |msdyn_invoicelinetransaction |GUID for fakturert salg            |Opprinnelig        |msdyn_actual       |
|Bekreft fakturakorreksjon|GUID for tilbakeføring av fakturert salg  |Tilbakeføring      |msdyn_actual                 |GUID for fakturert salg            |Opprinnelig        |msdyn_actual       |
|                        |GUID for nytt ufakturert salg |Erstatning            |msdyn_actual                 |GUID for fakturert salg            |Opprinnelig        |msdyn_actual       |


Illustrasjonen nedenfor viser koblingene som opprettes mellom ulike typer faktiske data ved ulike hendelser ved hjelp av eksemplet med tidsoppføringer i Project Operations.

> ![Hvordan faktiske data av ulike typer er koblet til hverandre i Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
