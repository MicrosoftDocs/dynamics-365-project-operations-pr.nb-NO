---
title: Utgifter til kostgodtgjørelse
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med utgifter til kostgodtgjørelse.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923200"
---
# <a name="per-diem-expenses"></a>Utgifter til kostgodtgjørelse

> [!IMPORTANT] 
> Funksjonaliteten som er beskrevet i denne artikkelen, er tilgjengelig for angitte brukere som en del av en forhåndsversjon.

Betaling av kostgodtgjørelse dag er en fast, forhåndsbestemt daglig sats som et selskap betaler til sine ansatte for innkvartering (hoteller), måltider og tilfeldige utgifter som de ansatte pådrar seg mens de er på jobbreise. Selskapet betaler denne godtgjørelsen til de ansatte i stedet for å betale de faktiske reiseutgiftene. De ansatte kan bruke kostgodtgjørelsessatsen under **Tilfeldige utgifter / Annet** til å dekke tips, romservice, klesvask eller stryking av klær for viktige forretningsmøter. Satsen for kostgodtgjørelse kan variere, avhengig av om arbeidsgiveren velger å refundere for den kombinerte kostnaden for innkvartering og måltider, eller bare for kostnader for måltider og tilfeldige utgifter.

Kostgodtgjørelsessatser kan baseres på tiden på året, reisestedet eller begge deler. Når du oppretter en kostgodtgjørelsesregel, kan du angi at en prosentandel av kostgodtgjørelsessatsen skal holdes tilbake hvis en ansatt mottar gratis måltider eller tjenester. Du kan også angi et minimum antall timer og et maksimalt antall timer som satsen for kostgodtgjørelse kan brukes på reisen til en ansatt.

Satsen for kostgodtgjørels beregnes som den totale kvoten som tilbys per dag, minus måltidsreduksjonen (kostnad for gratis tilbud) som gis til den ansatte.

## <a name="configure-per-diems"></a>Konfigurer kostgodtgjørelser

Følg denne fremgangsmåten for å konfigurere utgifter til kostgodtgjørelse.

1. Gå til **Utgiftshåndtering** \> **Oppsett** \> **Generelt** \> **Parametere for utgiftshåndtering**.
2. På fanen **Kostgodtgjørelse**, i feltet **Beregn måltidsreduksjon etter**, velger du hvordan kostgodtgjørelser skal beregnes:

    - **Type måltid per tur**– Beregn kostgodtgjørelsen på typen måltid som legges inn (frokost, lunsj eller middag), og på måltidsreduksjonen som angis for hver type måltid for kostgodtgjørelseskvoten for varigheten av reisen.
    - **Type måltid per dag**– Beregn kostgodtgjørelsen på typen måltid som legges inn, og på måltidsreduksjonen som angis for hver type måltid for kostgodtgjørelseskvoten per dag.
    - **Antall måltider per dag** – Beregn kostgodtgjørelsen basert på antall måltider som er angitt per dag, og på måltidsreduksjonen for antall måltider som er levert per dag.

3. Gå til **Utgiftshåndtering** \> **Oppsett** \> **Beregninger og koder** \> **Kostgodtgjørelsessteder**.
4. Legg til steder der kostgodtgjørelse kan brukes.
5. For hvert sted du legger til,velger du kostgodtgjørelsessatsen og valutaen som er gyldig mellom spesifikke startdatoer for innkvartering, måltider og andre utgifter, på fanen **Kostgodtgjørelser**. Hvis du vil konfigurere kostgodtgjørelsessatser og valutaer, går du til **Utgiftshåndtering** \> **Oppsett** \> **Beregninger og koder** \> **Kostgodtgjørelser**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Kostgodtgjørelser i det nyskapte utgiftsgrensesnittet

Funksjonen for kostgodtgjørelse støttes i det nyskapte **Utgiftshåndtering**-arbeidsområdet i Microsoft Dynamics 365 Finance versjon 10.0.25 og senere.

Følg fremgangsmåten nedenfor for å aktivere kostgodtgjørelser.

1. I arbeidsområdet **Funksjonsbehandling** finner du og velger funksjonen **Nyskapte utgiftsrapporter** og velger deretter **Aktiver nå**.
2. Finn og velg funksjonen **Kostgodtgjøreser for det nyskapte grensenittet for utgiftsrapporter** i listen, og velg deretter **Aktiver nå**.

## <a name="how-the-feature-works"></a>Hvordan funksjonen fungerer

Denne delen inneholder eksempler på tre konfigurasjonsscenarioer. Feltet **Beregn måltidsreduksjon etter** er for eksempel angitt til en annen verdi. For alle tre eksemplene er totalbeløpet som er belastbart, det samme frem til måltidsreduksjonen blir brukt. Etter dette er det totale belastbare beløpet forskjellig for hvert eksempel.

Følg denne fremgangsmåten for å opprette utgiften til kostgodtgjørelse som brukes i alle tre eksemplene.

1. Gå til **Arbeidsområder** \> **Utgiftshåndtering**.
2. Velg **Ny utgiftsrapport**, eller velg en eksisterende rapport.
3. Legg til en ny utgift. I **Kategori**-feltet velger du **Kostgodtgjørelse**. Velg stedet og start- og sluttdatoene for reisen. Kostgodtgjørelsen for innkvartering, måltider og tilfeldige beløp (andre utgifter) beregnes basert på dagsgodtgjørelsen som er angitt for det valgte stedet.

    Du velger for eksempel **Redmond (USA)** som sted. Den daglige satsen for dette stedet er USD 150 for innkvartering, USD 75 for måltider og USD 5 for tilfeldige utgifter. Startdatoen er 10. januar og sluttdatoen er 14. januar. Derfor er den valgte varigheten fem dager når den valgte konfigurasjonen er kalenderdager med klokkeslett, og det valgte klokkeslettet begynner og slutter kl. 12:00 på start- og sluttdatoene. Her er beregningene:

    - Totalt belastbart beløp = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Andel for måltid og tilfeldige utgifter av totalbeløpet = 5 × (75 + 5) = USD 400

Hvis det ble servert lunsj, lunsj og lunsj under reisen, må disse måltidene tas med som måltidsreduksjon.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Eksempel 1: Kostgodtgjørelse der måltidsreduksjoner er basert på typen måltid per tur

I dette eksemplet er måltidsreduksjonen 30 prosent for frokost, 30 prosent for lunsj og 40 prosent for middag. På siden **Parametere for utgiftshåndtering** er feltet **Beregn måltidsreduksjon etter** angitt til **Type måltid per tur**. Her er beregningene hvis tre frokoster, to lunsjer og ingen middager ble levert til den ansatte:

- Måltidsreduksjon = (3 × \[75 × 30 %\]) + (2 × \[75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Måltider og tilfeldige utgifter = 400 – 112,50 = USD 287,50
- Totalt belastbart beløp = Total kvote – Måltidsreduksjon = 1150 – 112,50 = USD 1037,50

![Utgift til kostgodtgjørelse der måltidsreduksjonen er basert på typen måltid per tur.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Eksempel 2: Kostgodtgjørelse der måltidsreduksjoner er basert på typen måltid per dag

I dette eksemplet er måltidsreduksjonen 30 prosent for frokost, 30 prosent for lunsj og 40 prosent for middag. På siden **Parametere for utgiftshåndtering** er feltet **Beregn måltidsreduksjon etter** angitt til **Type måltid per dag**. I dette tilfellet fjerner du avmerkingen i **Måltider**-rutenettet i dialogboksen **Rediger utgift** for å indikere hvilke måltider du fikk levert under turen.

Her er for eksempel beregningene hvis frokost var inkludert de tre første dagene av reisen:

- Daglig måltidsreduksjon for hver av de tre første dagene = 75 × 30 % = USD 22,50
- Total måltidsreduksjon = 3 × 22,50 = USD 67,50
- Måltider og tilfeldige utgifter for dag 1 til og med 3 = 75 – 22,50 = USD 57,50
- Måltider og tilfeldige utgifter totalt = Summen av måltider og tilfeldige utgifter over fem dager = 400 – 67,50 = USD 332,50
- Totalt belastbart beløp = Totalbeløp – Måltidsreduksjon = 1150 – 67,50 = USD 1082,50

![Utgift til kostgodtgjørelse der måltidsreduksjonen er basert på typen måltid per dag.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Eksempel 3: Kostgodtgjørelse der måltidsreduksjoner er basert på antall måltider per dag

I dette eksemplet beregnes måltidsreduksjonen basert på antall måltider som ble levert per dag (det vil si at feltet **Beregn måltidsreduksjon etter** på siden **Parametere for utgiftshåndtering** er angitt til **Antall måltider per dag**). I **Måltider**-rutenettet i dialogboksen **Rediger utgift** fjerner du merker for å indikere hvilke måltider du fikk levert.
I dette tilfellet er måltidsreduksjonen bare basert på antall måltider du har fått dekket, og ikke av typen måltid (frokost/lunsj/middag) som ble dekket.

Her er beregningene for kostgodtgjørelse når den daglige godtgjørelsen er USD 150 for innkvartering, USD 75 for måltider og USD 5 for tilfeldige utgifter:

- **Totalt belastbart beløp** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Ett måltid:** Måltidsreduksjon = 20 % = USD 15
- **To måltider:** Måltidsreduksjon = 50 % = USD 37,50
- **Tre måltider:** Måltidsreduksjon = 100 % = USD 75

Her er beregningene for **kvoten for måltider og tilfeldige utgifter**, som inkluderer USD 5 for tilfeldige utgifter:

- Dag 1 – To måltider dekket = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 2 – To måltider dekket = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Dag 3 – Ett måltid dekket = (75 – 15) + 5 = 60 + 5 = USD 65
- Dag 4 – Null måltider dekket = (75 – 0) + 5 = 75 + 5 = USD 80
- Dag 5 – Tre måltider dekket = (75 – 75) + 5 = 0 + 5 = USD 5

- Måltider og tilfeldige utgifter totalt = Måltider og tilfeldige utgifter for dag 1 + dag 2 + dag 3 + dag 4 + dag 5 = USD 235
- Måltidsreduksjon totalt = Måltidsreduksjon for dag 1 + dag 2 + dag 3 + dag 4 + dag 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Totalt belastbart beløp = Total kvote – Måltidsreduksjon totalt = USD 1150 – USD 165 = USD 985

![Utgift til kostgodtgjørelse der måltidsreduksjonen er basert på antall måltider per dag.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Per Finance-versjon 10.0.23, hvis du bruker det nyskapte utgiftsgrensesnittet, kan du ikke opprette utgifter til kostgodtgjørelse som har overlappende datoer. Hvis du prøver, får du en feilmelding.
