---
title: Parametere for utgiftshåndtering
description: Følgende parametere styrer funksjonaliteten i utgiftshåndtering.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 454d3f6feb46b28762a6a1249df2336f1aa5e91a
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960394"
---
# <a name="expense-management-parameters"></a>Parametere for utgiftshåndtering


Parameterne styrer den generelle funksjonaliteten i utgiftshåndtering.

### <a name="general"></a>Generelt

| **Felt**                                                | **Beskrivelse**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standardsats for kjørelengde**                             | Angi refusjonssatsen for kjøreutgifter. Satsen multipliseres med kjørelengden som er angitt for utgiften, for å beregne beløpet som skal refunderes for reiseutgiften.                       |
|**Private utgifter betalt av**                             | Velg hvem som er ansvarlig for å betale eventuelle kredittkorttransaksjonsbeløp som er kategorisert som private.                                                                                                     |
|**Vis hele reiseregningen ved tilbakedrilling**               | Velg dette alternativet for å vise alle utgifter for en reiseregning når detaljene i det opprinnelige dokumentet vises for et bestemt bilag som ble generert da reiseregningen ble postert.              |
|**Forhåndsautorisasjon av reise er obligatorisk**                 | Velg dette alternativet hvis du vil kreve at en reiserekvisisjon skal sendes inn og godkjennes før en ansatt kan sende inn en reiseregning.                                                                    |
|**Tillat redigering av distribusjoner før postering**            | Velg om distribusjonene av en reiseregning kan redigeres før postering.                                                                                                                 |
|**Evaluer policyer for utgiftsbehandling**                     | Velg når utgifter skal evalueres for å avgjøre om en utgiftspolicy er brutt. Utgifter kan sjekkes for brudd når utgiftsoppføringen er registrert og lagret, eller når utgiften sendes til godkjenning. Policyreglene for kvitteringer som kreves, sjekkes når utgiftslinjen lagres.                   |
|**Tillat konserninterne utgiftslinjer**                         | Velg om det skal være tillatt å registrer utgifter for andre juridiske enheter i en reiseregning.                                                                                                          |
|**Tillat redigering av valutakursen for kredittkortutgifter** | Velg dette alternativet hvis du vil at brukeren skal kunne redigere valutakursen for importerte kredittkortutgifter.                                                                        |
|**Felt med flernivåhierarkier som skal vises**                  | Velg hvilke felt for godkjennere som skal vises når typen arbeidsflyttilordning for reiseregning er satt til å være hierarki, og når hierarkivalget er angitt for å bruke hierarkiet for godkjenning av utgifter i flere nivåer. Når godkjenningshierarkiet med flere nivåer brukes for en arbeidsflyt, vises de valgte feltene i reiseregningen og kan redigeres. |
|**Angi kredittkortnummer for ansatt (oppdateringen fra juli 2017)**     | Velg om et 15-tegns eller 16-tegns nummer kan registreres og lagres i feltet **Kort-ID** på **Kredittkort**-siden for en ansatt.                                                                          |

### <a name="financial"></a>Finansielle tjenester

| **Felt**                                                            | **Beskrivelse**     |
|----------------------------------------------------------------------|------------------------------------|
|**Daglig journalnavn for hovedbok**                                         | Velg navnet på hovedbokjournalen som godkjente reiseregninger posteres til.            |
|**Aktiver avgiftsfradrag fra utgifter**                                  | Velg dette alternativet for å aktivere avgiftsfradrag for berettigede utgifter. Dette alternativet kan ikke aktiveres hvis amerikanske regler for merverdiavgift og skatt er aktivert.      |
|**Bokfør kontantforskudd umiddelbart**                                     | Velg dette alternativet for å bokføre et godkjent kontantforskudd når prosessen for å betale og overføre er fullført. Hvis det ikke er merket av for dette alternativet, genererer prosessen Betal og overfør en upostert hovedbokjournal. |
|**Korriger regnskapsdato under bokføring**                             | Velg dette alternativet for å oppdatere regnskapsdatoen når utgifter bokføres, hvis gjeldende periode er på vent eller lukket. Regnskapsdatoen blir satt til neste åpne periode.   |
|**Tillat gruppering av transaksjoner basert på motkonto angitt i betalingsmetoden**      | Velg dette alternativet for å oppsummere utgiftstransaksjonene for en reiseregning basert på motkontoen som er angitt i betalingsmetoden for utgiftene.   
|**Avgifter inkludert**                                                   | Velg dette alternativet for å inkludere merverdiavgift i utgiftsbeløpet som standard.             |
|**Frigi heftelser ved lukking av reiserekvisisjoner**            | Velg dette alternativet for å frigi beheftede midler når en godkjent reiserekvisisjon blir avsluttet.                                                                                   |
|**Tillat sending av reiserekvisisjon ved budsjettoverskridelse for budsjettregister og prosjektbudsjett** | Velg dette alternativet hvis du vil at ansatte skal kunne sende reiserekvisisjoner til godkjenning, selv om de enten overskrider det tillatte budsjettet som er angitt i budsjettregisteret, eller det tillatte budsjettet for et prosjekt.            |
|**Tillat sending av reiseregning ved budsjettoverskridelse for budsjettregister og prosjektbudsjett**    | Velg dette alternativet hvis du vil at ansatte skal kunne sende reiseregninger til godkjenning, selv om de enten overskrider det tillatte budsjettet som er angitt i budsjettregisteret, eller det tillatte budsjettet for et prosjekt.                |
|**Tillat godkjenning av reiseregning ved budsjettoverskridelse bare for budsjettregister**                | Velg dette alternativet for å tillate at godkjennerne kan godkjenne reiseregninger som overskrider det tillatte budsjettet som er angitt i budsjettregisteret.                                                                       |

### <a name="per-diem"></a>Kostgodtgjørelse

| **Felt**                             | **Beskrivelse**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimum timer for kostgodtgjørelse**           | Angi standard minimumsantall timer som en ansatt må jobbe i løpet av en dag, for å få rett til å motta kostgodtgjørelse for reiserelaterte utgifter.  Denne verdien brukes som standardverdi bare for feltet Minimum timer for satsnivåer for kostgodtgjørelse.                                                                                      |
|**Måltidsprosent**                          | Angi standard prosentandel av kostgodtgjørelse for måltider som brukes på første og siste dag i den reiserelaterte utgiften, når feltet **Beregn måltidsfradrag etter** er satt til **Måltidstype per dag** eller **Antall måltider per dag**. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til 0 (null), blir fradraget for første og siste dag 0,00. |
|**Hotellprosent**                        | Angi standard prosentandel for kostgodtgjørelsen for hoteller som brukes på den første og siste dagen, i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til 0 (null), blir fradraget for første og siste dag 0,00.                                              |
|**Annet prosent**                        | Angi standard prosentandel for kostgodtgjørelsen for diverse utgifter som brukes på den første og siste dagen, i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til 0 (null), blir fradraget for første og siste dag 0,00.                                                                                                     |
|**Reduksjon i prosent for frokost** | Angi beløpet som kostgodtgjørelsen skal reduseres med for frokost. Hvis for eksempel en ansatt får gratis frokost, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 10 prosent.                               |
|**Reduksjon i prosent for lunsj**    | Angi beløpet som kostgodtgjørelsen skal reduseres med for lunsj. Hvis for eksempel en ansatt får gratis lunsj, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 15 prosent.                                       |
|**Reduksjon i prosent for middag**   | Angi beløpet som kostgodtgjørelsen skal reduseres med for middag. Hvis for eksempel en ansatt får gratis middag, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 25 prosent.                                     |
|**Beregn måltidsreduksjon med**         | Velg hvordan systemet skal beregne reduksjonen i kostgodtgjørelsen for måltidet, ved å velge om reduksjonen er basert på måltidstypen per reise eller per dag, eller om den er basert på antall måltider per dag.|
|**Avrunding for kostgodtgjørelse**                  | Velg avrundingstypen som brukes for kostgodtgjørelsesutgifter. Hvis du velger normal avrunding, blir alle kostgodtgjørelsesutgifter som har et beløp på 0,50, rundet opp til 1,00, og alle kostgodtgjørelsesutgifter som har et beløp som er mindre enn 0,50, rundes ned til 0,00.                                                                                              |
|**Basisberegning for kostgodtgjørelse på**         | Velg om et kostgodtgjørelsesbeløp er basert på en kalenderdag eller en 24-timers periode.       |

### <a name="fax-cover-pages"></a>Faksforsider

| **Felt**                      | **Beskrivelse**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruksjoner**                   | Angi instruksjonene som ansatte må følge når de oppretter en forside for en telefaks som brukes til å sende kvitteringer som er relatert til en reiseregning. Klikk på **Oversettelser**-knappen for å angi språkspesifikk tekst som skal vises, basert på brukerspråket. |
|**Bruker-ID (strekkodeinformasjon)** | Velg dette alternativet for å lagre en ansatts unike identifikator i strekkoden som brukes på forsiden av telefaksen.                 |
|**Strekkode**                      | Velg strekkoden som brukes på forsiden av telefaksen. Strekkodene 39 og 128 støttes i utgiftshåndtering.               |

### <a name="anti-corruption"></a>Anti-korrupsjon

|                 <strong>Felt</strong>                 |                                                                                                                                                                                            <strong>Beskrivelse</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Vis anti-korrupsjonsattest</strong>  | Velg dette alternativet for å vise anti-korrupsjonsteksten når du oppretter en ny reiseregning. Bestemte utgiftskategorier kan aktiveres som krever at anti-korrupsjonsattestering velges i reiseregningen. En gavekategori som er relatert til en utgift for en offisiell myndighetsperson, kan for eksempel kreve at den ansatte må bekrefte at utgiften overholder i firmaets retningslinjer som er relatert til offisielle myndighetspersoner. |
| <strong>Anti-korrupsjonsmelding for innsender</strong> |                                                                                             Skriv inn teksten som skal vises for den ansatte, når det opprettes en ny reiseregning. Klikk på <strong>Oversettelser</strong>-knappen for å angi språkspesifikk tekst som skal vises, basert på brukerspråket.                                                                                             |
| <strong>Anti-korrupsjonsmelding for godkjenner</strong>  |                                                                                             Skriv inn teksten som skal vises for godkjenneren, når det opprettes en ny reiseregning. Klikk på <strong>Oversettelser</strong>-knappen for å angi språkspesifikk tekst som skal vises, basert på brukerspråket.                                                                                             |

