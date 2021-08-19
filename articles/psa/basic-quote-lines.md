---
title: Tilbud og tilbudslinjer
description: Dette emnet inneholder informasjon om tilbud og tilbudslinjer.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: c98708cf91f9c5d078f3a1d3d619c9ca93cffa3e6bbca34511947b602a1c678a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995458"
---
# <a name="quotes-and-quote-lines"></a>Tilbud og tilbudslinjer

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation finnes det to typer tilbud: prosjekttilbud og salgstilbud. De to typene er forskjellige på følgende måter:

- I et salgstilbud er det bare ett rutenett for linjeelementer. I etprosjekt tilbud finnes det to rutenett for linje elementer: et for prosjektlinjer og et for produktlinjer.
- Et salgstilbud støtter aktivering og revisjoner. Et prosjekttilbud støtter ikke disse prosessene.
- Du kan knytte flere ordrer til et salgstilbud. Du kan bare knytte én prosjektkontrakt til et prosjekttilbud.
- Du kan vinne et salgstilbud og holde den relaterte salgsmuligheten åpen. Når et prosjekttilbud er vunnet, blir den relaterte salgsmuligheten lukket.
- Et salgstilbud inkluderer ikke enkelte felt og konsepter som er inkludert i et prosjekttilbud som har felt. Feltene omfatter **Kontraktenhet**, **Forretningsforbindelsesansvarling** og **Navn på kontakt for fakturering**.  
- Salgstilbud og prosjekttilbud identifiseres også ved hjelp av et felt basert på et alternativsett med navnet **Type**. For et salgstilbud har dette feltet verdien **Varebasert**. For et prosjekttilbud har det verdien **Arbeidsbasert**.

Dette emnet fokuserer på detaljene i prosjekttilbud.

Et prosjekttilbud i PSA kan ha flere linjeelementer eller tilbudslinjer. Et prosjekttilbud har faktisk to rutenett for linjeelementer. Det ene rutenettet er for prosjektbaserte linjer som tillater detaljerte beregninger. Det andre rutenettet er for produktbaserte linjer som bruker en enkel enhetspris og den antallsbaserte metoden.

- **Prosjektbasert** – Beløpet (tilbudsverdien) bestemmes etter at du har beregnet hvor mye arbeid som kreves. Du kan beregne arbeid på et stort nivå, eller du kan beregne det direkte som linjedetaljer under hver tilbudslinje. Til slutt kan du beregne arbeid basert på beregning av faktiske data, ved å bruke et prosjekt og en prosjektplan. Prosjektbaserte tilbudslinjer finnes bare i prosjektrelaterte tilbud som opprettes ved hjelp av Project Service Automation. Denne typen tilbudslinje er en tilpasset form av tilbudslinjer utenfor produktkatalogen som er tilgjengelige i Microsoft Dynamics 365 Sales.
- **Produktbasert** – Beløpet (tilbudsverdien) fastsettes basert på antall enheter som selges, og produktets enhetssalgspris. Produktet på en produktbasert linje kan komme fra en produktkatalog i Salg, eller det kan være et produkt som du definerer. Denne typen tilbudslinje er også tilgjengelig for prosjektrelaterte tilbud som opprettes ved hjelp av PSA.

Beløpet i et tilbud er summen på tvers av de produktbaserte linjene og de prosjektbaserte linjene.

> [!NOTE]
> Tilbud og tilbudslinjer kreves ikke i PSA. Du kan starte prosjektprosessen med en prosjektkontrakt (solgt prosjekt). En salgsmulighet er imidlertid alltid nødvendig, uansett om du starter med et tilbud eller en prosjektkontrakt.

## <a name="project-based-quote-lines"></a>Prosjektbaserte tilbudslinjer

En prosjektbasert tilbudslinje i PSA har følgende faktureringsmetoder:

- Tid og materiale
- Fast pris

### <a name="time-and-material"></a>Tid og materiale

Faktureringsmetoden for tid og materiale er basert på forbruk. Når du velger denne faktureringsmetoden, faktureres kunden etter hvert som kostnader påløper i prosjektet. Fakturaer opprettes etter en datobasert periodisk frekvens. I løpet av salgsprosessen gir tilbudsverdien for en tid-og-material-komponent bare et estimat av den endelige kostnaden til kunden. Leverandøren forplikter seg ikke til selv å fullføre prosjektet med nøyaktig den siterte verdien. Tid-og materiell-komponenter øker kundens risiko. Det kan hende at kundene vil forhandle på flere ikke-overskrid-klausuler for å redusere risikoen. PSA støtter ikke angivelse av ikke-overskrid-klausuler.

### <a name="fixed-price"></a>Fast pris

I faktureringsmetoden fast pris forplikter en leverandør seg til å levere prosjektet til en fast kostnad for kunden. Kunden faktureres for den angitte verdien på tilbudslinjen med fast pris, uansett hvilken kostnader som påløper for leverandøren for å levere denne tilbudslinjen. Tilbudslinjen med fast pris blir fakturert på én av følgende måter: 

- Som et totalbeløp i begynnelsen eller slutten av prosjektet, eller når en milepæl for et prosjekt er nådd. 
- Med en datobasert hyppighet med like andeler av den faste verdien på tilbudslinjen. Disse andelene kalles periodiske milepæler.
- I avdrag som har en pengeverdi som er justert etter fremdriften for arbeidet eller bestemte milepæler som er oppnådd i prosjektet. I dette tilfellet kan verdien for hvert avdrag være forskjellige, men de må alle summeres til den faste verdien på tilbudslinjen.

PSA støtter alle tre typer fakturaplaner for tilbudslinjer med fast pris.

## <a name="transaction-classification"></a>Transaksjonsklassifisering

Profesjonelle serviceorganisasjoner oppgir og fakturerer vanligvis kundene etter klassifisering av kostnader. I PSA representeres kostnadene av følgende transaksjonsklassifiseringer:

- **Tid** – denne klassifiseringen representerer kostnadene for arbeid eller personale i et prosjekt.
- **Utgift**: – denne klassifiseringen representerer alle andre typer utgifter i et prosjekt. Siden utgifter kan klassifiseres bredt, kan de fleste organisasjoner opprette underkategorier, for eksempel reise, leiebil, hotell eller kontorutstyr.
- **Avgift** – denne klassifiseringen representerer diverse kostnader, straffer og andre elementer som er belastet kunden. 
- **Skatt** – denne klassifiseringen representerer skattebeløp som brukere legger til mens de registrerer utgifter.
- **Materialetransaksjon** – denne klassifiseringen representerer faktiske verdier fra produktlinjer på en bekreftet prosjektfaktura.
- **Milepæl** – denne klassifiseringen brukes av faktureringslogikken for fast pris i PSA.

En eller flere av disse transaksjonsklassifiseringene kan tilknyttes hver tilbudslinje. Når et tilbud er vunnet, blir tilordningen mellom transaksjonsklassifiseringen og tilbudslinjen overført til kontraktlinjen.
 
> ![Skjermbilde av tilordning av transaksjonstyper til tilbuds- og kontraktlinjer.](media/basic-guide-5.png)
  
Et tilbud kan for eksempel inneholde følgende to tilbudslinjer: 
- Konsulentarbeid som bruker en faktureringsmetode for tid og materialer, der klassifiseringer av tid og gebyrtransaksjoner gjelder. Alle tids- og gebyrtransaksjoner for eksempelprosjektet for **Dynamics AX-implementering** faktureres for eksempel til kunden basert på tiden og materialene som brukes. 
- Relaterte reiseutgifter som bruker en faktureringsmetode for fast pris. Alle reiseutgifter for eksempelprosjektet **Dynamics AX-implementering** blir for eksempel fakturert med et fast beløp.

> [!NOTE]
> Kombinasjonen av prosjekt- og transaksjonsklassifiseringen for **Tid**, **Utgift** og **Avgift** som er tilknyttet en tilbudslinje eller kontraktlinje, må være unik. Hvis samme kombinasjon av prosjekt- og transaksjonsklasse er tilknyttet mer enn én kontraktlinje eller tilbudslinje, fungerer ikke PSA på riktig måte.

## <a name="billing-types"></a>Faktureringstyper

Feltet **Faktureringstype** definerer konseptet belastbarhet i PSA. Det er et alternativsett som har følgende mulige verdier:

- **Belastbar** – kostnaden som er påløpt av denne rollen/kategorien, er en direkte kostnad som styrer prosjektutførelsen, og kunden vil betale for dette arbeidet. Betalingen kan administreres som en ordning med tid og materialer eller fast pris. Den ansatte som bruker denne tiden, vil imidlertid motta den tilsvarende kreditten for sin fakturerbare utnyttelse.
- **Ikke-belastbar** – kostnaden som er påløpt av denne rollen/kategorien, regnes som en direkte kostnad som styrer prosjektutførelsen, selv om kunden ikke anerkjenner dette faktumet og ikke vil betale for dette arbeidet. Den ansatte som bruker denne tiden, blir ikke kreditert med fakturerbar utnyttelse for den.
- **Gratis** – kostnaden som er påløpt av denne rollen/kategorien, regnes som en direkte kostnad som styrer prosjektutførelsen, og kunden anerkjenner dette faktumet. Den ansatte som bruker denne tiden, blir kreditert for fakturerbar utnyttelse for den. Denne kostnaden belastes imidlertid ikke kunden.
- **Ikke tilgjengelig** – kostnadene som påløper på interne prosjekter som ikke krever inntektssporing, spores ved hjelp av dette alternativet.

## <a name="invoice-schedule"></a>Fakturaplan

En fakturaplan er en serie datoer der fakturering for et prosjekt inntreffer. Du kan opprette en fakturaplan på en tilbudslinje i PSA hvis dette er aktuelt. Hver tilbudslinje kan ha sin egen fakturaplan. Hvis du vil opprette en fakturaplan, må du angi følgende attributtverdier:

- En startdato for fakturering 
- En leveringsdato som representerer sluttdatoen for fakturering i prosjektet
- En fakturafrekvens

PSA bruker disse tre attributtverdiene til å generere et foreløpig sett med datoer som fakturering skal inntreffe på.

## <a name="invoice-frequency"></a>Fakturafrekvens

Faktureringsfrekvens er en enhet som lagrer attributtverdier som bidrar til å uttrykke frekvensen av fakturaopprettelser. Følgende attributter uttrykker eller definerer faktureringsfreksensen:

- **Periode** – månedlig, annenhver uke og ukentlige perioder støttes. 
- **Kjøringer per periode** – for perioder ukentlig og annenhver uke kan du bare definere én kjøring per periode. For månedlige perioder kan du definere mellom én og fire kjøringer per periode. 
- **Dager for kjøring** – dagene når fakturering skal kjøres. Du kan konfigurere dette attributtet på to forskjellige måter:
  - **Ukedager** – du kan for eksempel angi at fakturering skal kjøres hver mandag eller annenhver mandag. Kunder som må angi at fakturering skal kjøre på en arbeidsdag, kan foretrekke denne typen konfigurasjon. 
  - **Kalenderdager** – du kan for eksempel angi at fakturering skal kjøres den sjuende og tjueførste dagen i hver måned. Enkelte organisasjoner kan foretrekke denne typen konfigurasjon, fordi den bidrar til å garantere at fakturering kjøres etter en fast tidsplan hver måned.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Fakturaplan for en tilbudslinje med fast pris

For en tilbudslinje med fast pris kan du bruke rutenettet **Fakturaplen** til å opprette faktureringsmilepæler som er lik verdien på tilbudslinjen.

- Hvis du vil opprette faktureringsmilepæler som er likt inndelt, velger du en fakturafrekvens, angir startdatoen for fakturering på tilbudslinjen og velger **Forespurt fullføringsdato** for tilbudet i **Sammendrag**-delen i tilbudshodet. . Deretter velger du **Generer periodiske milepæler** for å opprette likt delte milepæler basert på den valgte fakturafrekvensen. 
- Hvis du vil opprette en faktureringsmilepæl for et engangsbeløp, oppretter du en milepæl, og deretter angir du tilbudslinjeverdien som milepælbeløpet.
- Hvis du vil opprette faktureringsmilepæler som er basert på bestemte oppgaver i prosjektplanen, oppretter du en milepæl og tilordner den til prosjektets tidsplanelement i brukergrensesnittet for faktureringsmilepælen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]