---
title: Tilbud - Nøkkelkonsepter
description: Dette emnet gir informasjon om prosjekttilbud og salgstilbud som er tilgjengelige i Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8a1b5152b76cbcdfb5160a0af78eceec2c42b9a13dfc76701b6ad935318c7ba8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997888"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konsepter som er unike for prosjektbaserte tilbud

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Dynamics 365 Project Operations finnes det to typer tilbud, prosjekttilbud og salgstilbud. De to typene tilbud er forskjellige på følgende måter:

- **Rutenett for linjeelementer**: I et salgstilbud er det bare ett rutenett for linjeelementer. Prosjekttilbud har to rutenett for linjeelementer. Ett rutenett er for prosjektlinjer, og det andre er for produktlinjer.
- **Aktivering og revisjoner**: Salgstilbud støtter aktivering og revisjoner. Disse prosessene støttes ikke i et prosjekttilbud.
- **Tilknyttede ordrer**: Du kan knytte flere ordrer til et salgstilbud. Du kan bare knytte én prosjektkontrakt til et prosjekttilbud.
- **Vinne et tilbud**: Når du vinner et tilbud, kan den relaterte salgsmuligheten forbli åpen. Når et prosjekttilbud er vunnet, blir den relaterte salgsmuligheten lukket.
- **Felt og konsepter**: Et salgstilbud inkluderer ikke enkelte felt og konsepter som er inkludert i et prosjekttilbud. Feltene omfatter **Kontraktenhet**, **Forretningsforbindelsesansvarling** og **Navn på kontakt for fakturering**.  
- **Type**: Salgstilbud og prosjekttilbud identifiseres også ved hjelp av feltet basert på et alternativsett med navnet **Type**. For et salgstilbud har dette feltet verdien **Varebasert**. For et prosjekttilbud har det verdien **Arbeidsbasert**.

Dette emnet fokuserer på detaljene i prosjekttilbud.

Et prosjekttilbud i Project Operations kan ha flere linjeelementer eller tilbudslinjer. Et prosjekttilbud har faktisk to rutenett for linjeelementer. Det ene rutenettet er for prosjektbaserte linjer som tillater detaljerte beregninger. Det andre rutenettet er for produktbaserte linjer som bruker en enkel enhetspris og den antallsbaserte metoden.

- **Prosjektbasert**: Tilbudsverdien bestemmes etter at du har beregnet hvor mye arbeid som kreves. Du kan beregne arbeid på et høyt nivå, direkte som linjedetaljer under hver tilbudslinje, eller basert på beregning av faktiske data, ved hjelp av et prosjekt og en prosjektplan. Prosjektbaserte tilbudslinjer finnes bare i prosjektrelaterte tilbud som opprettes ved hjelp av Project Operations. Denne typen tilbudslinje er en tilpasset form av tilbudslinjer utenfor produktkatalogen som er tilgjengelige i Microsoft Dynamics 365 Sales.

- **Produktbasert**: Tilbudsverdien fastsettes basert på antall enheter som selges, og produktets enhetssalgspris. Produktet på en produktbasert linje kan komme fra en produktkatalog i Salg, eller det kan være et produkt som du definerer. Denne typen tilbudslinje er også tilgjengelig for prosjektrelaterte tilbud som opprettes ved hjelp av Project Operations.

Beløpet i et tilbud er summen på tvers av de produktbaserte linjene og de prosjektbaserte linjene.

> [!NOTE]
> Tilbud og tilbudslinjer kreves ikke i Project Operations. Du kan starte prosjektprosessen med en prosjektkontrakt (solgt prosjekt). En salgsmulighet er imidlertid alltid nødvendig, uansett om du starter med et tilbud eller en prosjektkontrakt.

## <a name="project-based-quote-lines"></a>Prosjektbaserte tilbudslinjer

En prosjektbasert tilbudslinje i Project Operations har følgende faktureringsmetoder:

- Tid og materiale
- Fast pris

### <a name="time-and-material"></a>Tid og materiale

Faktureringsmetoden for tid og materiale er basert på forbruk. Når du velger denne faktureringsmetoden, faktureres kunden etter hvert som kostnader påløper i prosjektet. Fakturaer opprettes etter en datobasert periodisk frekvens. I løpet av salgsprosessen gir tilbudsverdien for en tid-og-material-komponent bare et estimat av den endelige kostnaden til kunden. Leverandøren forplikter seg ikke til selv å fullføre prosjektet med nøyaktig den siterte verdien. Tid-og materiell-komponenter øker kundens risiko. Det kan hende at kundene vil forhandle på flere ikke-overskrid-klausuler for å redusere risikoen. Project Operations støtter ikke angivelse av ikke-overskrid-klausuler.

### <a name="fixed-price"></a>Fast pris

I faktureringsmetoden fast pris forplikter en leverandør seg til å levere prosjektet til en fast kostnad for kunden. Kunden faktureres for den angitte verdien på tilbudslinjen med fast pris, uansett hvilken kostnader som påløper for leverandøren for å levere denne tilbudslinjen. Tilbudslinjen med fast pris blir fakturert på én av følgende måter: 

- Som et totalbeløp i begynnelsen eller slutten av prosjektet, eller når en milepæl for et prosjekt er nådd. 
- Med en datobasert hyppighet med like andeler av den faste verdien på tilbudslinjen. Disse andelene kalles periodiske milepæler.
- I avdrag som har en pengeverdi som er justert etter fremdriften for arbeidet eller bestemte milepæler som er oppnådd i prosjektet. I dette tilfellet kan verdien for hvert avdrag være forskjellige, men de må alle summeres til den faste verdien på tilbudslinjen.

Project Operations støtter alle tre typer fakturaplaner for tilbudslinjer med fast pris.

## <a name="transaction-classification"></a>Transaksjonsklassifisering

Profesjonelle serviceorganisasjoner oppgir og fakturerer vanligvis kundene etter klassifisering av kostnader. Kostnadene representeres av følgende transaksjonsklassifiseringer:

- **Tid**: Denne klassifiseringen representerer kostnadene for arbeid eller personale i et prosjekt.
- **Utgift**: Denne klassifiseringen representerer alle andre typer utgifter i et prosjekt. Siden utgifter kan klassifiseres bredt, kan de fleste organisasjoner opprette underkategorier, for eksempel reise, leiebil, hotell eller kontorutstyr.
- **Avgift**: Denne klassifiseringen representerer diverse kostnader, straffer og andre elementer som er belastet kunden. 
- **Skatt**: Denne klassifiseringen representerer skattebeløp som brukere legger til mens de registrerer utgifter.
- **Materialetransaksjon**: Denne klassifiseringen representerer faktiske verdier fra produktlinjer på en bekreftet prosjektfaktura.
- **Milepæl**: Denne klassifiseringen brukes av faktureringslogikken for fast pris.

En eller flere av disse transaksjonsklassifiseringene kan tilknyttes hver tilbudslinje. Når et tilbud er vunnet, blir tilordningen mellom transaksjonsklassifiseringen og tilbudslinjen overført til kontraktlinjen.
  
Et tilbud kan for eksempel inneholde følgende to tilbudslinjer: 

- Konsulentarbeid som bruker en faktureringsmetode for tid og materialer, der klassifiseringer av tid og gebyrtransaksjoner gjelder. Alle tids- og gebyrtransaksjoner for eksempelprosjektet for **Dynamics AX-implementering** faktureres for eksempel til kunden basert på tiden og materialene som brukes. 
- Relaterte reiseutgifter som bruker en faktureringsmetode for fast pris. Alle reiseutgifter for eksempelprosjektet **Dynamics AX-implementering** blir for eksempel fakturert med et fast beløp.

> [!NOTE]
> Kombinasjonen av prosjekt- og transaksjonsklassifiseringen for **Tid**, **Utgift** og **Avgift** som er tilknyttet en tilbudslinje eller kontraktlinje, må være unik. Hvis samme kombinasjon av prosjekt- og transaksjonsklasse er tilknyttet mer enn én kontraktlinje eller tilbudslinje, fungerer ikke Project Operations på riktig måte.

## <a name="billing-types"></a>Faktureringstyper

Feltet **Faktureringstype** definerer konseptet belastbarhet. Det er et alternativsett som har følgende mulige verdier:

- **Belastbar**: Kkategoriostnaden som er påløpt av denne rollen/kategorien, er en direkte kostnad som styrer prosjektutførelsen, og kunden vil betale for dette arbeidet. Betalingen kan administreres som en ordning med tid og materialer eller fast pris. Den ansatte som bruker denne tiden, vil imidlertid motta den tilsvarende kreditten for sin fakturerbare utnyttelse.
- **Ikke-belastbar**: Kostnaden som er påløpt av denne rollen/kategorien, regnes som en direkte kostnad som styrer prosjektutførelsen, selv om kunden ikke anerkjenner dette faktumet og ikke vil betale for dette arbeidet. Den ansatte som bruker denne tiden, blir ikke kreditert med fakturerbar utnyttelse for den.
- **Gratis** : Kostnaden som er påløpt av denne rollen/kategorien, regnes som en direkte kostnad som styrer prosjektutførelsen, og kunden anerkjenner dette faktumet. Den ansatte som bruker denne tiden, blir kreditert for fakturerbar utnyttelse for den. Denne kostnaden belastes imidlertid ikke kunden.
- **Ikke tilgjengelig**: Kostnadene som påløper på interne prosjekter som ikke krever inntektssporing, spores ved hjelp av dette alternativet.

## <a name="invoice-schedule"></a>Fakturaplan

En fakturaplan er en serie datoer der fakturering for et prosjekt inntreffer. Du kan opprette en fakturaplan på en tilbudslinje hvis dette er aktuelt. Hver tilbudslinje kan ha sin egen fakturaplan. Hvis du vil opprette en fakturaplan, må du angi følgende attributtverdier:

- En startdato for fakturering 
- En leveringsdato som representerer sluttdatoen for fakturering i prosjektet
- En fakturafrekvens

Disse tre attributtverdiene brukes til å generere et foreløpig sett med datoer som fakturering skal inntreffe på.

## <a name="invoice-frequency"></a>Fakturafrekvens

Faktureringsfrekvens er en enhet som lagrer attributtverdier som bidrar til å uttrykke frekvensen av fakturaopprettelser. Følgende attributter uttrykker eller definerer faktureringsfreksensen:

- **Periode**: Månedlig, annenhver uke og ukentlige perioder støttes. 
- **Kjøringer per periode**: For perioder ukentlig og annenhver uke kan du bare definere én kjøring per periode. For månedlige perioder kan du definere mellom én og fire kjøringer per periode. 
- **Dager for kjøring**: Dagene når fakturering skal kjøres. Du kan konfigurere dette attributtet på to forskjellige måter:
  - **Ukedager**: Du kan for eksempel angi at fakturering skal kjøres hver mandag eller annenhver mandag. Kunder som må angi at fakturering skal kjøre på en arbeidsdag, kan foretrekke denne typen konfigurasjon. 
  - **Kalenderdager**: Du kan for eksempel angi at fakturering skal kjøres den sjuende og tjueførste dagen i hver måned. Enkelte organisasjoner kan foretrekke denne typen konfigurasjon, fordi den bidrar til å garantere at fakturering kjøres etter en fast tidsplan hver måned.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fakturaplan for en tilbudslinje med fast pris

For en tilbudslinje med fast pris kan du bruke rutenettet **Fakturaplen** til å opprette faktureringsmilepæler som er lik verdien på tilbudslinjen.

- Hvis du vil opprette faktureringsmilepæler som er likt inndelt, velger du en fakturafrekvens, angir startdatoen for fakturering på tilbudslinjen og velger **Forespurt fullføringsdato** for tilbudet i **Sammendrag**-delen i tilbudshodet. . Deretter velger du **Generer periodiske milepæler** for å opprette likt delte milepæler basert på den valgte fakturafrekvensen. 
- Hvis du vil opprette en faktureringsmilepæl for et engangsbeløp, oppretter du en milepæl, og deretter angir du tilbudslinjeverdien som milepælbeløpet.
- Hvis du vil opprette faktureringsmilepæler som er basert på bestemte oppgaver i prosjektplanen, oppretter du en milepæl og tilordner den til prosjektets tidsplanelement i brukergrensesnittet for faktureringsmilepælen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
