---
title: Enhetsgrupper og enheter
description: Dette emnet inneholder informasjon om enhetsgrupper og enheter.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: 6620c99563394d1f3881d6bfdb72d01c1c4e8d6f
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145595"
---
# <a name="unit-groups-and-units"></a>Enhetsgrupper og enheter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Enhetsgrupper og enheter er basisenheter i Microsoft Dynamics 365. En enhet er en enkelt målenhet, og flere enheter kan grupperes i enhetsgrupper. En enhetsgruppe kalles noen ganger en enhetstidsplan i brukergrensesnittet for Dynamics 365. 

Her er noen eksempler på enheter og enhetsgrupper:
 
- **Enhetsgruppe**: Avstand 
    - **Enheter**: Mile, kilometer og så videre.
- **Enhetsgruppe**: Tid
    - **Enheter**: Time, dag, uke og så videre. 

Når du definerer flere enheter i en enhetsgruppe, må du også angi en konverteringsfaktor mellom dem ved å angi den første enheten som er angitt som standard- eller primærenhet for enhetsgruppen. 

For eksempel, i en **Tid**-enhetsgruppe, hvis du definerer **Time** som den første enheten, tilordner systemet **Time** som standardenhet. Hvis neste enhet du angir, er **Dag**, må du konfigurere en konverteringsfaktor for **Dag** til **Time**. Hvis du deretter legger til **Uke** som en tredje enhet, må du angi en konverteringsfaktor for **Uke** i form av **Dag** eller **Time**. 

Følgende bilde viser et eksempel på oppsett for **Dag**-enheten, der **Antall**-feltet viser antall timer i løpet av en dag, og i **Uke**, der **Antall**-feltet viser antall dager i uken.

> ![Enhetsgruppe: informasjonsside](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Bruke enheter og enhetsgrupper

Dynamics 365 Project Service Automation bruker enheter og enhetsgrupper til å behandle estimater og oppføringer for både utgifter og klokkeslett. 

For utgifter har hver utgiftskategori en standard enhetsgruppe og enhet. Disse verdiene angis som standardverdier for prislisteoppføringer for utgiftskategorier. 

Du har for eksempel en utgiftskategori som kalles **Reisegodtgjørelse**. Den har en enhetsgruppe som har navnet **Distanse** og en standardenhet med navnet **Mile**. Hvis du konfigurerer **Distanse**-enhetsgruppen slik at den har to enheter (**Mile** og **Kilometer**), kan du angi to priser for **Reisegodtgjørelse**-kategorien i én prisliste: pris per mile og pris per kilometer.

| Utgiftskategori  | Enhetsgruppe  | Enhet      | Prismodell  | Pris per enhet  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Reisegodtgjørelse           | Avstand      | Mile      | Pris per enhet    | 10 USD            |
| Reisegodtgjørelse           | Avstand      | Kilometer | Pris per enhet    |  6 USD            |

Når du angir en utgift i et prosjekt, bestemmer systemet prisen gjennom kombinasjonen av kategorien og enheten i utgiften. 

| Utgiftsbeskrivelse        | Utgiftskategori  | Enhet  | Antall  | Enhetspris   |
|----------------------------|---------------------|-------|-----------|----------------|
| Kjøring til klientsted | Reisegodtgjørelse             | Mile  | 10        | 10 USD         |

For tid har hvert prislistehode et **Standard tidsenhet**-felt. Verdien angis når du oppretter prislistehodet. Denne enheten brukes deretter til å angi alle rollebaserte priser i denne prislisten.

Estimatlinjer for feltet **Tid i tilbud** kan uttrykkes i en hvilken som helst enhet. Estimatlinjer på prosjekter og tidsoppføringer for prosjekter kan imidlertid bruke bare **Time**-enheten. Hvis enheten i tidsoppføringen eller på estimatlinjen ikke samsvarer med enheten på prislistelinjen for den aktuelle rollen, konverterer systemet prisen til enhetene som er definert i prosjektestimatet eller den faktiske transaksjonen for prosjektet.

Følgende eksempel viser hvordan PSA bruker enhetsgruppen, enhetene og konverteringsfaktorene.
- Enheter

   - **Enhetsgruppe**: Tid 
   - **Enheter**: Time 
    
    - **Dag** – omregningsfaktor: 8 timer       
    - **Uke** – omregningsfaktor: 40 timer  
        
- Prislisteoppsett for prosjekt A:

    - **Navn**: Salgspriser i UK 2016 
    - **Standard tidsenhet**: Dag 
    - **Valuta**: GBP

| Rolle      | Enhetsgruppe | Enhet | Organisasjonsenhet | Pris   |
|-----------|------------|------|---------------------|---------|
| Utvikler | Time       | Day  | Ekeli UK          | 800 GBP |

### <a name="time-entry"></a>Tidsoppføring

Tabellen nedenfor viser den resulterende transaksjonen på salgssiden som opprettes av PSA for et prosjekt på tre timer.


| Prosjekt   | Oppgave    | Rolle      | Antall | Enhet  | Enhetspris | Ufakturert salgsbeløp |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Prosjekt A | Utforming  | Utvikler | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Vanlige spørsmål om tidsenheter

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Konverterer PSA til andre enheter når det gjelder utgifter?
Nr. Enhetskonverteringen fungerer bare for tid. For utgifter, hvis systemet ikke finner en pris for kombinasjonen av utgiftskategori og enhet, settes prisen til 0,00 som standard.

### <a name="why-does-psa-convert-time-units"></a>Hvorfor konverterer PSA tidsenheter?
I noen land eller områder er det juridiske krav for at faktureringspriser skal angis i dager. Prisforhandling og rabattering i løpet av tilbudssyklusen utføres ved hjelp av dagsrater for hver fakturerbare rolle. Tidsplanestimat og tidsregistrering utføres i timer. PSA konverterer tidsenheter for å støtte denne forskjellen i tidsenheter.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Kan tidsenheter endres i prosjektestimater?
Nr. Tidsplanestimering er for øyeblikket begrenset til timer og kan ikke endres.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Kan enheter og enhetsgrupper redigeres, slettes og legges til?
Ja. Med unntak av **Tid**-enhetsgruppen og **Time**-enheten kan alle enheter slettes eller redigeres, og det kan legges til nye enheter. I PSA kan **Tid**-enhetsgruppen og **Time**-enheten ikke slettes. De kan imidlertid oppdateres med en oversatt tekst for **Navn**-feltet.
