---
title: Konfigurere parametere for utgiftshåndtering
description: Dette emnet beskriver parameterne som kontrollerer den generelle virkemåten i utgiftshåndtering.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8ecbd0abc16d0a29eea47d6bd1653a204a83de4c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897283"
---
# <a name="configure-expense-management-parameters"></a>Konfigurere parametere for utgiftshåndtering

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet beskriver parameterne som kontrollerer den generelle virkemåten i utgiftshåndtering.

## <a name="general"></a>Generelt

| Felt                                                    | Beskrivelse |
|----------------------------------------------------------|-------------|
| Standardsats for kjørelengde                                 | Angi refusjonssatsen for kjøreutgifter. Denne satsen multipliseres med kjørelengden som er angitt for utgiften, for å beregne beløpet som skal refunderes for reiseutgiften. |
| Valider utgiftsformål                                 | Aktiver dette alternativet for å begrense brukere til et eksisterende sett med verdier som er konfigurert i feltet **Formål for reiseregning**, når de oppretter reiseregninger. |
| Private utgifter betalt av                                | Velg hvem som er ansvarlig for å betale eventuelle kredittkorttransaksjonsbeløp som er kategorisert som private. |
| Vis hele reiseregningen ved tilbakedrilling               | Velg dette alternativet for å vise alle utgifter for en reiseregning når detaljene i det opprinnelige dokumentet vises for et bestemt bilag som ble generert da reiseregningen ble postert. |
| Forhåndsautorisasjon av reise er obligatorisk                 | Velg dette alternativet hvis du vil kreve at en reiserekvisisjon skal sendes inn og godkjennes før en ansatt kan sende inn en reiseregning. |
| Tillat redigering av distribusjoner før postering            | Velg om distribusjonene av en reiseregning kan redigeres før den posteres. |
| Evaluer policyer for utgiftsbehandling                     | Velg når utgifter skal evalueres for å avgjøre om en utgiftspolicy er brutt. Utgifter kan evalueres for brudd når utgiftsoppføringen er registrert og lagret, eller når utgiften sendes til godkjenning. Policyreglene for kvitteringer som kreves, evalueres når utgiftslinjen lagres. |
| Tillat konserninterne utgiftslinjer                         | Velg om utgifter for andre juridiske enheter kan registreres i en reiseregning. |
| Tillat redigering av valutakursen for kredittkortutgifter | Velg dette alternativet hvis du vil at brukeren skal kunne redigere valutakursen for importerte kredittkortutgifter. |
| Felt med flernivåhierarkier som skal vises                  | Velg hvilke felt for godkjennere som skal vises når typen arbeidsflyttilordning er satt til et hierarki, og når **Hierarki** er angitt for å bruke godkjenningshierarkiet, godkjenning av utgifter i flere nivåer. Når godkjenningshierarkiet med flere nivåer brukes for en arbeidsflyt, vises de valgte feltene i reiseregningen og kan redigeres. |
| Angi kredittkortnummer for ansatt                        | Velg om et 15-tegns eller 16-tegns nummer kan registreres og lagres i feltet **Kort-ID** på **Kredittkort**-siden for en ansatt. |
| Valider formål med reiserekvisisjon                      | Aktiver dette alternativet for å begrense brukere til et eksisterende sett med verdier som er konfigurert i feltet **Formål for reiseregning**, når de oppretter reiserekvisisjoner. |

## <a name="financial"></a>Finansielle tjenester

| Felt                                                                                    | Beskrivelse |
|------------------------------------------------------------------------------------------|-------------|
| Daglig journalnavn for hovedbok                                                                | Velg navnet på hovedbokjournalen som godkjente reiseregninger posteres til. |
| Aktiver avgiftsfradrag fra utgifter                                                        | Velg dette alternativet for å aktivere avgiftsfradrag for berettigede utgifter. Dette alternativet kan ikke velges hvis amerikanske regler for merverdiavgift og skatt er aktivert. |
| Bokfør kontantforskudd umiddelbart                                                           | Velg dette alternativet for å bokføre et godkjent kontantforskudd når prosessen Betal og overfør er fullført. Hvis det ikke er merket av for dette alternativet, genererer prosessen Betal og overfør en upostert hovedbokjournal. |
| Korriger regnskapsdato under bokføring                                                   | Velg dette alternativet for å oppdatere regnskapsdatoen når utgifter bokføres, hvis gjeldende periode er på vent eller lukket. Regnskapsdatoen blir satt til neste åpne periode. |
| Tillat gruppering av transaksjoner basert på motkonto angitt i betalingsmetoden       | Velg dette alternativet for å oppsummere utgiftstransaksjonene for en reiseregning basert på motkontoen som er angitt i betalingsmetoden for utgiftene. |
| Avgifter inkludert                                                                             | Velg dette alternativet for å inkludere merverdiavgift i utgiftsbeløpet som standard. |
| Frigi heftelser ved lukking av reiserekvisisjoner                                      | Velg dette alternativet for å frigi beheftede midler når en godkjent reiserekvisisjon blir avsluttet. |
| Tillat sending av reiserekvisisjon ved budsjettoverskridelse for budsjettregister og prosjektbudsjett | Velg dette alternativet hvis du vil at ansatte skal kunne sende reiserekvisisjoner til godkjenning, selv om de enten overskrider det tillatte budsjettet som er angitt i budsjettregisteret, eller det tillatte budsjettet for et prosjekt. |
| Tillat sending av reiseregning ved budsjettoverskridelse for budsjettregister og prosjektbudsjett     | Velg dette alternativet hvis du vil at ansatte skal kunne sende reiseregninger til godkjenning, selv om de enten overskrider det tillatte budsjettet som er angitt i budsjettregisteret, eller det tillatte budsjettet for et prosjekt. |
| Tillat godkjenning av reiseregning ved budsjettoverskridelse bare for budsjettregister                 | Velg dette alternativet for å tillate at godkjennerne kan godkjenne reiseregninger som overskrider det tillatte budsjettet som er angitt i budsjettregisteret. |

## <a name="per-diem"></a>Kostgodtgjørelse

| Felt                                 | Beskrivelse |
|---------------------------------------|-------------|
| Minimum timer for kostgodtgjørelse            | Angi standard minimumsantall timer som en ansatt må jobbe i løpet av en dag, for å få rett til å motta kostgodtgjørelse for reiserelaterte utgifter. Denne verdien brukes som standardverdi bare for feltet **Minimum timer** for satsnivåer for kostgodtgjørelse. |
| Måltidsprosent                          | Angi standard prosentandel av kostgodtgjørelse for måltider som brukes på første og siste dag i den reiserelaterte utgiften, når feltet **Beregn måltidsfradrag etter** er satt til **Måltidstype per dag** eller **Antall måltider per dag**. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til **0** (null), blir fradraget for første og siste dag 0,00. |
| Hotellprosent                         | Angi standard prosentandel for kostgodtgjørelsen for hoteller som brukes på den første og siste dagen, i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til **0** (null), blir fradraget for første og siste dag 0,00. |
| Annet prosent                         | Angi standard prosentandel for kostgodtgjørelsen for diverse utgifter som brukes på den første og siste dagen, i den reiserelaterte utgiften. Arbeidsdagen på første og siste dag kan være kortere enn en standard arbeidsdag. Derfor kan beløpet for kostgodtgjørelsen på disse dagene være forskjellig fra standardbeløpet. Hvis prosentandelen er satt til **0** (null), blir fradraget for første og siste dag 0,00. |
| Reduksjon i prosent for frokost | Angi beløpet som kostgodtgjørelsen skal reduseres med for frokost. Hvis for eksempel en ansatt får gratis frokost, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 10 prosent. |
| Reduksjon i prosent for lunsj     | Angi beløpet som kostgodtgjørelsen skal reduseres med for lunsj. Hvis for eksempel en ansatt får gratis lunsj, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 15 prosent. |
| Reduksjon i prosent for middag    | Angi beløpet som kostgodtgjørelsen skal reduseres med for middag. Hvis for eksempel en ansatt får gratis middag, kan det hende du vil redusere beløpet for kostgodtgjørelsen med 25 prosent. |
| Beregn måltidsreduksjon med           | Angi hvordan systemet skal beregne reduksjonen i kostgodtgjørelsen for måltidet, ved å velge om reduksjonen er basert på måltidstypen per reise eller per dag, eller om den er basert på antall måltider per dag. |
| Avrunding for kostgodtgjørelse                     | Velg avrundingstypen som brukes for kostgodtgjørelsesutgifter. Hvis du velger normal avrunding, blir alle kostgodtgjørelsesutgifter som har et beløp på 0,50, rundet opp til 1,00, og alle kostgodtgjørelsesutgifter som har et beløp som er mindre enn 0,50, rundes ned til 0,00. |
| Basisberegning for kostgodtgjørelse på          | Velg om et kostgodtgjørelsesbeløp er basert på en kalenderdag eller en 24-timers periode. |

## <a name="fax-cover-pages"></a>Faksforsider

| Felt                          | Beskrivelse |
|--------------------------------|-------------|
| Instruksjoner                   | Angi instruksjonene som ansatte må følge når de oppretter en forside for en telefaks som brukes til å sende kvitteringer som er relatert til en reiseregning. Hvis du vil angi språkspesifikk tekst som skal vises, basert på brukerspråket, velger du **Oversettelser**. |
| Bruker-ID (strekkodeinformasjon) | Velg dette alternativet for å lagre en ansatts unike identifikator i strekkoden som brukes på forsiden av telefaksen. |
| Strekkode                       | Velg strekkoden som brukes på forsiden av telefaksen. Strekkodene 39 og 128 støttes i utgiftshåndtering. |

## <a name="anti-corruption"></a>Anti-korrupsjon

| Felt                                 | Beskrivelse |
|---------------------------------------|-------------|
| Vis anti-korrupsjonsattest   | Velg dette alternativet for å vise anti-korrupsjonsteksten når det opprettes en reiseregning. Bestemte utgiftskategorier kan aktiveres som krever at anti-korrupsjonsattestering velges i reiseregningen. En gavekategori som er relatert til en utgift for en offisiell myndighetsperson, kan for eksempel kreve at den ansatte må bekrefte at utgiften overholder i firmaets retningslinjer som er relatert til offisielle myndighetspersoner. |
| Anti-korrupsjonsmelding for innsender | Skriv inn teksten som skal vises for en ansatt som oppretter en reiseregning. Hvis du vil angi språkspesifikk tekst som skal vises, basert på brukerspråket, velger du **Oversettelser**. |
| Anti-korrupsjonsmelding for godkjenner  | Skriv inn teksten som skal vises til godkjenneren når en reiseregning opprettes. Hvis du vil angi språkspesifikk tekst som skal vises, basert på brukerspråket, velger du **Oversettelser**. |
