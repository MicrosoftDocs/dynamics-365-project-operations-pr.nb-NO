---
title: Nyheter eller endringer i Project Operations i oktober 2021 for lagerførte/produksjonsbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for lagerførte/produksjonsbaserte scenarioer fra oktober 2021.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029955"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Nyheter eller endringer i Project Operations i oktober 2021 for lagerførte/produksjonsbaserte scenarioer

_**Gjelder:** Project Operations for lagerførte/produksjonsbaserte scenarioer_

Denne artikkelen gjelder følgende komponenter og versjoner av Microsoft Dynamics 365 Project Operations:

- Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.22
 
## <a name="quality-updates"></a>Kvalitetsoppdateringer

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
|--------------|------------------|----------------|
| Prosjektstyring og regnskap | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Varer i arbeid (VIA) for prosjekt og påløpt omsetningsbeløp tilbakeføres ikke riktig når en konsernintern kundefaktura posteres. |
| Prosjektstyring og regnskap | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Funksjonaliteten **Forhindre prosjektlukking hvis det finnes åpne transaksjoner** fungerer ikke. |
| Prosjektstyring og regnskap | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | Faktureringsklassifiseringen i en fritekstfaktura fyller ikke ut dimensjoner automatisk fra prosjekter når denne funksjonaliteten er aktivert. |
| Prosjektstyring og regnskap | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | VIA og påløpt omsetningsbeløp tilbakeføres ikke riktig i ikke-konserninterne scenarioer når prosjektfakturaen posteres. |
| Prosjektstyring og regnskap | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Debet- og kreditverdier byttes når Microsoft Excel-tillegget brukes med prosjektutgiftsjournalen og feltet **Motkontotype** er satt til **Prosjekt**. |
| Prosjektstyring og regnskap | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Beløpet som posteres i prosjekttransaksjoner, overvurderes i en prosjektbestilling som inneholder lagerførte varer og har avgiftsbeløp som ikke er fradragsberettiget, når **UseTax** er merket. |
| Prosjektstyring og regnskap | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Systemet deler beløpet mellom resultatrapportene for prosjektet og VIA-rapportene for prosjektet. |
| Prosjektstyring og regnskap | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | Lagerbeholdningen er feil etter at et delvis returnert varebehov er justert. |
| Prosjektstyring og regnskap | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Ressursnavn dupliseres i Project Operations når de redigeres i Microsoft Project. |
| Prosjektstyring og regnskap | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Konserninterne utgiftsrapporter som har konserninterne kostnader i ventende leverandørfaktura for leverandør posteres først i posteringstypen **Prosjekt - VIA-kostnad**. De estimatrelaterte kostnadene blir imidlertid postert i posteringstypen **Prosjektkostnad** under behandling i stedet for den forventede posteringstypen **Konsernintern kostnad**. |
| Prosjektstyring og regnskap | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Tilbakeholdt leverandørbeløp gjør at prosjektutgiftstransaksjoner ikke vises. |
| Prosjektstyring og regnskap | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | Timeregistreringen må runde av transaksjonsbeløpet i transaksjonsvalutaen til angitt antall desimaler i alle regnskapsdistribusjoner og tildelingsoppføringer i økonomijournalen. |
| Prosjektstyring og regnskap | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Antall for prosjektvarebehov oppdateres automatisk når de planlagte ordrene autoriseres. |
| Prosjektstyring og regnskap | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Bilagsnummeret, transaksjonstypen leverandørsaldo og nummeret for forretningsforbindelse kan ikke tilbakeføres i forskuddsfakturaen for en bestilling. |
| Prosjektstyring og regnskap | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Den konserninterne leverandørfakturaen ødelegges når integrering av leverandørfaktura er aktivert. |
| Prosjektstyring og regnskap | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Når du oppretter en prosjektutgiftsjournal, vises kostnadsbeløpet i **Kredit**-feltet. |
| Prosjektstyring og regnskap | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Betalingsbetingelsene på prosjektfakturaer fungerer ikke som forventet. |
| Prosjektstyring og regnskap | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Timeregistreringsbilag kan brukes på nytt når nummerserien er konfigurert som sammenhengende. |
| Prosjektstyring og regnskap | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANKRIKE: Logikken i **Manuelt tilbakeholdelsesbeløp** samsvarer ikke med logikken i **Automatisk tilbakeholdelsesbeløp** i fakturaforslaget for prosjektkontrakt. |
| Prosjektstyring og regnskap | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Når det tilbakeholdte leverandørbeløpet frigis, får bilagsposteringen feil tilleggslinjer. |
| Prosjektstyring og regnskap | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Når **Fakturadato**-feltet på siden **Opprett fakturaforslag** endres, kan følgende feil oppstå: «Objektreferanse er ikke satt til en objektforekomst.» |
| Prosjektstyring og regnskap | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Det oppstår en feil når du prøver å godkjenne en timeregistrering fra arbeidsflyten **TSLine** og det finnes en timeregistreringspolicy for lørdag og søndag. |
| Prosjektstyring og regnskap | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Prosjektvaretypen for startsaldo utelates fra **Transaksjonssammendrag for fakturaforslag** når fakturatotalen beregnes for fakturaforslaget. |
| Prosjektstyring og regnskap | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Hvis forbrukskostnaden i en prosjektproduksjonsordre er 0 (null), oppstår følgende feil når du prøver å beregne: «Forsøkte å dele med null.» |
| Prosjektstyring og regnskap | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | Mobilappen Project-timeregistrering for Android slutter å svare. Problemet er knyttet til **TimeEntryDataManager ArgumentNullException**. |
| Prosjektstyring og regnskap | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Journalen for Project Operations-integrering mislykkes når du posterer den, fordi en konto mangler dimensjoner. Kontoen som mangler dimensjonene, er imidlertid ikke kontoen du posterer til. |
| Prosjektstyring og regnskap | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | **ToDate**-filteret i søk fjernes ikke når det fjernes fra dialogboksen **Velg** på siden **Poster kostnad**. |
| Prosjektstyring og regnskap | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Tilbakestill all distribusjon** mislykkes og viser en feil for timeregistreringene som er opprettet for et prosjekt av typen **Bare klokkeslett**. |
| Prosjektstyring og regnskap | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Prosjekt**-fanen kan ikke redigeres i en ventende leverandørfaktura når innkjøpskategorien er tilordnet til varen. |
| Prosjektstyring og regnskap | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigasjonsruten mangler hvis du ikke er logget på Project Operations Dataverse. |
| Prosjektstyring og regnskap | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Når det gjelder konserninterne prosjektjusteringstransaksjoner, er det problemer i målfirmaet. |
| Prosjektstyring og regnskap | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Igangsatt kost for et prosjekt beregner feil antall og kostpris hvis bestillingen ble behandlet av **Årsavslutning for bestilling** i Økonomimodul. |
| Prosjektstyring og regnskap | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Når en prosjektproduksjonsordre som har kvalitetsordrer, rapporteres som fullført, oppstår følgende feil: «Ingen virtuelle transaksjoner er merket med lagertransaksjon.» |
| Prosjektstyring og regnskap | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Når en prosjektrelatert leverandørfaktura posteres, vises følgende feil: «Opplistet tekst Prosjekt - kostnad - vare finnes ikke.» |
| Prosjektstyring og regnskap | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Indirekte kostnader fordobles når du avsetter omsetning manuelt. |
| Prosjektstyring og regnskap | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Avsett omsetning og VIA-postering produserer ikke transaksjoner. |
| Prosjektstyring og regnskap | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | Aktivering av ventende pris mislykkes for en vare med standardkostnad når det finnes en mottatt prosjektbestilling. |
| Prosjektstyring og regnskap | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | Verdien for tilbakeført VIA fra en fakturapostering er forskjellig fra den opprinnelige posterte VIA-verdien fra en tidsoppføring. |
| Prosjektstyring og regnskap | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Det er et posteringsproblem for prosjektfakturert omsetning i tilfeller med brukte honorarer der transaksjonene i bilag ikke er i balanse. |
| Prosjektstyring og regnskap | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Hvis du oppretter et estimat etter at et fakturaforslag er postert, blokkeres importen av korrigeringslinjer i Project Operations. |
| Prosjektstyring og regnskap | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Endring av en fullstendig fakturert milepæloppføring skal ikke være mulig. |
| Prosjektstyring og regnskap | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Når du bruker automatiske tillegg, kan du ikke postere den konserninterne kundefakturaen for en timeregistrering, og det vises en feilmelding. |
| Prosjektstyring og regnskap | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | Adressen i et underprosjekt blir ikke oppdatert riktig. |
| Prosjektstyring og regnskap | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Kostprisen i varebehov oppdateres med innkjøpsprisen for konsoliderte bestillinger. |
| Prosjektstyring og regnskap | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Den posterte kostnaden stemmer ikke etter at innkjøpsprisen er oppdatert og parameteren **Aktiver endringsadministrasjon** er aktivert. |
| Reise og utgift | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Du kan se alle brukerutgifter når du søker etter en kategori i mobilappen for utgifter. |
| Reise og utgift | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Det posteres feil beløp i leverandørtransaksjoner og salgsavgiftstransaksjoner fra en utgift som ble opprettet fra en kredittkorttransaksjon. |
| Reise og utgift | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Det vises en irrelevant advarsel når du oppdaterer utgiftsrapportsidene. |
| Reise og utgift | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Feil midlertidig godkjenner brukes når du sletter en midlertidig godkjenner og deretter sender inn på nytt via arbeidsflyt. |
| Reise og utgift | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Det oppstår en posteringsfeil som er knyttet til konfigurasjonen for reisegodtgjørelse. |
| Reise og utgift | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | Distribusjon oppdaterer ikke den juridiske enheten når en ikke-tilknyttet transaksjon legges til i utgiftsrapporten på nytt for en konsernintern utgift. |

### <a name="regulatory-updates"></a>Forskriftsmessige oppdateringer

Hvis du vil ha informasjon om forskriftsmessige oppdateringer for økonomi- og driftsapper, kan du se [Forskriftsmessige oppdateringer](/dynamics365/finance/localizations/regulatory-updates). Du kan også logge på Microsoft Dynamics Lifecycle Services (LCS) og bruke verktøyet Problemsøk til å vise de planlagte forskriftsmessige oppdateringene. Med Problemsøk kan du søke etter land eller område, funksjonstype og utgivelse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
