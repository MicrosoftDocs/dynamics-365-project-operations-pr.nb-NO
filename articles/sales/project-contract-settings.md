---
title: Innstillinger for prosjektkontrakt
description: Dette emnet gir informasjon om feltene som påvirker kontraktlinjer, og informasjon om kontrakten som er oppsummert, på tvers av alle linjeelementene.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4c04ff004febf3a07b329bf375e38acb43d19887
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277620"
---
# <a name="project-contract-settings"></a>Innstillinger for prosjektkontrakt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet gir informasjon om felt som gjelder for hele prosjektkontrakten, inkludert innstillinger som påvirker alle kontraktlinjene. Informasjon om kontrakten som er oppsummert på tvers av alle linjeelementene for å drive KPI-er for prosjektkontrakten, er også inkludert.

Tabellen nedenfor viser feltene i en prosjektkontrakt som er unike for Dynamics 365 Project Operations, eller som har noen viktige endringer i virkemåten fra salgsordre i Dynamics 365 Sales.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Type | Kategorien **Sammendrag** (skjult) | Dette er et alternativsettfelt med følgende alternativer:</br>- **Arbeidsbasert** (bare tilgjengelig når Project Operations er installert)</br>- **- Varebasert** (bare tilgjengelig når Project Operations og Sales er installert)</br>- **Basert på service og vedlikehold** (tilgjengelig når Dynamics 365 Field Service er installert) | I Project Operations er verdien i dette feltet **Arbeidsbasert** som standard, og det klassifiserer kontrakten som en prosjektbasert kontrakt. En kontrakt må være prosjektbasert for å aktivere alle prosjektspesifikke utvidelser og funksjoner. |
| Eiende firma | **Sammendrag**-fanen | Den juridiske enheten som står for kostnadene og inntektene som påløper fra prosjektene som er tilknyttet denne prosjektkontrakten. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. | Det eiende firmaet tilsvarer konseptet juridisk enhet i modulen **Prosjektstyring og regnskap** i Project Operations. Alle kostnader og inntekter som påløper fra dette prosjektet, blir regnskapsført i hovedboken til det eiende firmaet. |
| Kunde | **Sammendrag**-fanen | En referanse til kundens firma- eller forretningsforbindelsesoppføring. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. | Valutaen i prosjektkontrakten blir som standard basert på valutaen til kunden. Valutaen kan endres før kontrakten lagres. |
| Kontoadministrator | **Sammendrag**-fanen | Navnet på kontoadministratoren for denne avtalen. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. | Kontoadministratoren er ansvarlig for å administrere relasjonen med kunden gjennom fullføringen av prosjektet. Basert på oppføringen av den bestillbare ressursen som er knyttet til kontoadministratoren, blir kontraktenheten som standard i prosjektkontrakten. |
| Kontraktsenhet | **Sammendrag**-fanen | Organisasjonsenheten som er ansvarlig for levering av prosjektene tilknyttet denne kontrakten. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. | Kontraktenheten er avdelingen i firmaet som skal kjøre prosjektene. Hver kontraktenhet har en valuta, og denne valutaen brukes til å rapportere beregnet og faktisk kostnad som påløpte under prosjektet. |
| Produktprisliste | **Sammendrag**-fanen | Denne prislisten brukes til standardpriser på de produktbaserte kontraktlinjene. Listen over rullegardinalternativer for dette feltet viser en liste over prislister der prislistevalutaen samsvarer med valutaen i kontrakten. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. I prosjektkontrakten hentes dette feltet som standard fra kontooppføringen, men kan endres. | Dette feltet har ingen relevans nedstrøms. |
| Valuta | **Sammendrag**-fanen | Valutaen som brukes til å rapportere verdien for denne avtalen, og valutaen som kunden blir fakturert i. Når en kontrakt er opprettet fra et tilbud, kopieres dette feltet fra det tilsvarende feltet for tilbudsoppføringen. I prosjektkontrakten hentes dette feltet som standard fra kontooppføringen, men kan endres. | Når en kontrakt er lagret, kan ikke dette feltet lenger redigeres. Dette feltet brukes til å standardisere produktet og prosjektprislistene i kontrakten. Valutaen i kontrakten brukes til å samsvare valutaen i prislisten. |
| Må ikke overskrides-grense | **Sammendrag**-fanen | Dette feltet angir det forhandlede taket for den endelige verdien som kunden har godtatt for denne avtalen. | Taket evalueres under kjøring og gjelder på tvers av alle linjeelementer og prosjekter som er tilknyttet denne avtalen. |
| Ønsket leveringsdato | **Sammendrag**-fanen | Når en kontrakt er opprettet fra et prosjekttilbud, kopieres dette feltet fra det tilsvarende feltet for prosjekttilbudet. | Denne datoen brukes som sluttdato for å generere fakturaplaner. |

Følgende KPI-er er tilgjengelige i kategorien **Kontraktytelse** for en prosjektkontrakt.

| Felt | Sted | Beskrivelse |
| --- | --- | --- |
| Kontraktverdi | Samlet kontrakt | Totalverdien for prosjektkontrakten. |
| Fakturert beløp | Samlet kontrakt | Summen av beløpene på alle fakturaer mot denne kontrakten. |
| Påløpt kostnad | Samlet kontrakt | Summen av alle faktiske kostnader som er logget på alle prosjekter som er tilordnet kontrakten. |
| Bruttofortjeneste | Samlet kontrakt | Fakturert beløp – kostnad påløpt til dato / fakturert beløp |
| Forventet margin | Samlet kontrakt | (Kontraktverdi – estimerte kostnader) / kontraktverdi – estimerte kostnader = summen av alle estimerte kostnader for alle prosjekter som er tilordnet kontrakten.|
| Kontraktverdi | Prosjektbaserte linjer | Verdien på kontraktlinjen. |
| Fakturert beløp | Prosjektbaserte linjer | For kontraktlinje med fast pris: summen av beløpene for alle fakturerte faktiske verdier for salgsmilepæler mot denne kontraktlinjen på diverse fakturaer som er opprettet for denne kontrakten. For kontraktlinje med tid og materiale: summen av beløpene for alle belastbare fakturerte faktiske salgsverdier mot denne kontraktlinjen på diverse fakturaer som er opprettet for denne kontrakten. |
| Påløpt kostnad | Prosjektbaserte linjer | Summen av alle faktiske kostnader som er logget på alle prosjekter som er tilordnet kontraktlinjen. |
| Bruttofortjeneste | Prosjektbaserte linjer | (Fakturert beløp – kostnad påløpt til dato) / fakturert beløp |
| Forventet margin | Prosjektbaserte linjer | (Kontraktlinje beløp i standardvaluta – estimerte kostnader for kontraktlinjen i standardvaluta) / kontraktlinjebeløp i standardvaluta |
| Påløpt kostnad | Detaljer for en prosjektbasert linje | Tid: summen av beløpet for faktiske tidskostnader logget for denne rollen i prosjektet som er tilordnet til kontraktlinjen. Utgifter: summen av beløpet for alle faktiske utgiftskostnader logget for denne kategorien i prosjektet som er tilordnet til kontraktlinjen. |
| Logget antall | Detaljer for en prosjektbasert linje | Tid: all tid for faktiske tidskostnader for en rolle i prosjektet som er tilordnet til denne kontraktlinjen. Utgifter: alle utgifter for denne utgiftskategorien for de faktiske utguftskostnadene i prosjektet, er tilordnet til denne kontraktlinjen. |
| Fakturert beløp | Detaljer for en prosjektbasert linje | For en kontraktlinje med fast pris blir dette feltet stående tomt på detaljnivået, og det vises bare på kontraktlinjenivået. For en kontraktlinje for tid og materiale utføres beregninger på detaljnivå. Detaljene viser summen av beløpet på alle fakturerte inntektslinjer mot denne kontraktlinjen som er belastbar. |
| Fakturert antall | Detaljer for en prosjektbasert linje | For en kontraktlinje med fast pris blir dette feltet stående tomt på detaljnivået, og det vises bare på kontraktlinjenivået. For en kontraktlinje for tid og materiale utføres beregninger på detaljnivå for tid og utgifter. Tid: summen av timene på alle fakturerte inntektslinjer for denne rollen mot denne kontraktlinjen som er belastbar. Utgifter: alle utgifter for denne utgiftskategorien for de faktiske utguftskostnadene i prosjektet, er tilordnet til denne kontraktlinjen. |
| Kontraktverdi | Produktbaserte linjer | Kontraktlinjeverdien for denne produktbaserte kontraktlinjen. |
| Fakturert beløp | Produktbaserte linjer | Summen av beløpene på alle fakturalinjer mot denne produktbaserte kontraktlinjen på diverse fakturaer som opprettes for denne kontrakten. |
| Påløpt kostnad | Produktbaserte linjer | Summen av alle faktiske kostnader som er logget for den produktbaserte kontraktlinjen. |
| Bruttofortjeneste | Prosjektbaserte linjer | Fakturert beløp – kostnad påløpt til dato / fakturert beløp |
| Forventet margin | Produktbaserte linjer | (Kontraktlinjeverdi – estimerte kostnader for kontraktlinjen) / kontraktlinjeverdi |


[!INCLUDE[footer-include](../includes/footer-banner.md)]