---
title: Kontantforskudd
description: Dette emnet inneholder informasjon om kontantforskudd.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6881fc8251a2d3c7d6af0016780a92358ce63397d09b9a0cde201126cd2912cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988528"
---
# <a name="cash-advance"></a>Kontantforskudd

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Et kontantforskudd gjør det mulig for ansatte å låne penger fra selskapet før de pådrar seg eventuelle utgifter. Når et forespurt kontantforskudd er godkjent og betalt, kan den ansatte bruke pengene til forretningsutgiftene de kan være i ferd med å pådra seg. 

## <a name="create-and-submit-a-cash-advance-request"></a>Opprette og sende inn en forespørsel om kontantforskudd
Gjør følgende for å opprette et nytt forskudd og sende en forespørsel om forskudd: 

1. Under **Mine utgifter** velger du **Kontantforskudd** > **Nytt**. 
2. På siden **Forespørsel om nytt kontantforskudd** angir du utgiftsformålet og velger plasseringen der utgiften skal påløpe.
3. Angi ønsket beløp og valuta, og velg deretter **Lagre**. 
4. Når du er klar til å sende inn forespørselen om kontantforskudd, går du til siden **Forespørsel om kontantforskudd** og velger **Arbeidsflyt** > **Send inn**.

## <a name="modify-a-cash-advance-request"></a>Endre en forespørsel om kontantforskudd

Du kan endre en forespørsel om kontantforskudd hvis den ikke er sendt til godkjenning.

1. Under **Mine utgifter: Kontantforskudd** finner og velger du kontantforskuddet du vil redigere.
2. Velg **Rediger**, og gjør de nødvendige endringene i forespørselen om kontantforskudd. 
3. Velg **Lagre og lukk**.


## <a name="view-cash-advance-requests"></a>Vise forespørsler om kontantforskudd
Du kan se gjennom listen over alle kontantforskuddene som er i utkast, sendt, i gjennomgang eller betalt, under **Mine utgifter: Kontantforskudd**. 

## <a name="approve-cash-advance-requests"></a>Godkjenne forespørsler om kontantforskudd

Ledere eller brukere som er konfigurert som godkjennere i arbeidsflyten, kan godkjenne kontantforskuddene som sendes til dem for gjennomgang. 

1. Hvis du vil godkjenne et kontantforskudd, går du til **Behandle kontantforskudd** og velger **Kontantforskudd for min gjennomgang**.
2. Velg kontantforskuddet du må gå gjennom, og velg **Godkjenn**.  

## <a name="pay-cash-advances"></a>Betale kontantforskudd 
Fremgangsmåten nedenfor fullføres vanligvis av en regnskapsfører eller en bruker med regnskapstillatelser.

1. Hvis du vil postere godkjente forskudd, velger du **Godkjente kontantforskudd**, og deretter velger du **Betal og Overfør**.  
2. Angi journaldetaljene for forskuddene, og velg deretter **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Sende inn en reiseregning mot et betalt forskudd 

Når du oppretter og sender en utgiftsrapport for kontantforskuddet du allerede har mottatt, justeres utgiftene automatisk mot det forskuddet. Hvis kontantforskuddet er større enn utgiftsbeløpet, må du returnere saldoen til firmaet ved hjelp av utgiftskategorien **Tilbakebetal kontanter**. Hvis kontantforskuddet som er betalt for selskapet, er mindre enn beløpet du utbetalte, må firmaet betale deg saldoen. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Velg kontantforskudd som gjelder for utgiftene dine
Før du sender en utgiftsrapport, kan du velge kontantforskuddet som er på linje med utgiftstransaksjonene i rapporten. Hvis du vil bruke denne funksjonaliteten, må følgende to funksjoner aktiveres fra arbeidsområdet for **Funksjonsbehandling**:

  - Nyskapte utgiftsrapporter
  - Mulighet til å tilordne kontantforskudd til utgiftslinjer
 
 Når disse funksjonene er aktivert:
 
  - Du kan legge til ett eller flere kontantforskudd for hver utgiftslinje.
  - Den tilgjengelige saldoen for et kontantforskudd vises i sanntid når en utgiftsrapport lagres. Dette gjør det mulig å behandle utgiftstransaksjoner og returnere kontanttransaksjonen samtidig.
  - Du kan velge flere kontantforskudd for én utgiftstransaksjon.
  - Avstemmingsdata for kontantforskudd er tilgjengelige ved hjelp av en spørring. 
 
Hvis du ikke bruker disse funksjonene, vil funksjonaliteten være den samme, og eksisterende kontantforskudd reduseres automatisk etter at en utgift er sendt.

### <a name="example"></a>Eksempel 
Du planlegger å reise fra Bergen til New York City på en konferanse. Du oppretter en forespørsel om kontantforskudd for 3000.00 USD basert på den beregnede kostnaden for konferansebilletten, flyreiser, overnatting, måltider og taxiutgifter. Du får ikke betalt med mindre din overordnede godkjenner denne forespørselen. Når din overordnede godkjenner, betales det forespurte kontantforskuddet som 10 000 kroner til bankkontoen din. Deretter deltar du på konferansen. Når du har fullført reisen, oppdager du at den totale utgiften bare ble 8000 kroner. Velg **Kontant** i feltet **Betalingsmåte**, og send inn utgifter for 2790.00 USD. Det sendte utgiftsbeløpet justeres automatisk mot forskuddet på 10 000 kroner som ble utlånt til deg. Nå er du skyldig 210.00 USD (3000.00 - 2790.00), som du kan returnere til selskapet ved hjelp av utgiftskategorien **Returner kontanter**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
