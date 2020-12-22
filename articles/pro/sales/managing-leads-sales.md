---
title: Behandle kundeemner – Lite
description: Denne emnet gir informasjon om behandling av prosjektbaserte kundeemner (Pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e789295d4b1f5a53fcf179a2998f60d35f48f99
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513801"
---
# <a name="manage-leads---lite"></a>Behandle kundeemner – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Prosjektrelaterte kundeemner kan administreres og kvalifiseres i Project Operations. Prosessen med behandling av kundeemner inkluderer opprettelse av arbeidsbaserte kundeemner og kvalifisering av disse kundeemnene. 

## <a name="list-of-project-sales-leads"></a>Liste over salgsmuligheter for prosjekt

I **Salg**-delen, i den venstre navigasjonsruten, åpner du listesiden **Kundeemner** for å vise en liste over alle kundeemneoppføringer i systemet. Kundeemnene i listen er arbeidsbaserte og andre typer kundeemner som kan opprettes hvis du også har Dynamics 365 Sales- eller Dynamics 365 Field Service-applikasjoner.

Du kan opprette en filtrert visning for å se bare kundeemner som er basert på prosjekter, ved å opprette et filter på **Type**-verdien. Du kan for eksempel velge å vise bare arbeidsbaserte kundeemner.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Opprette et nytt kundeemne for en prosjektbasert avtale

Når et prosjektbasert kundeemne er kvalifisert, opprettes det en salgsmulighet og en forretningsforbindelse. En prosjektbasert salgsmulighet er utgangspunktet for salgsoppfølgingsoppgaver i Salgsmulighet-fasen. Prosjektrelaterte salgsmuligheter har unike funksjoner som kreves for å selge prosjektarbeid. Disse funksjonene omfatter følgende:

- Faktureringsmetodene for tid og materiale og fast pris
- Prislister med flere gyldige datoer for personale, utgifter og materiell påløpt for prosjekter.

Hvis du vil opprette en salgsmulighet automatisk for et kvalifisert kundeemne, setter du **Type**-attributtet til **Arbeidsbasert** når du oppretter kundeemnet. Hvis du velger en annen type, vil ikke emnet opprette en prosjektbasert salgsmulighet når det er kvalifisert. Hvis den prosjektbaserte psalgsmuligheten ikke blir opprettet, vil ikke de prosjektspesifikke funksjonene være tilgjengelig i salgsprosessene nedstrøms.

Tabellen nedenfor inneholder viktig feltinformasjon for et kundeemne, og innvirkningene nedstrøms av disse feltene.

| **Felt** | **Plassering** | **Beskrivelse** | **Nedstrøms påvirkning** |
| --- | --- | --- | --- |
| Emne | Generelt, kategori | Dette tekstfeltet må inneholde en kort beskrivelse av avtalen. | Emne for kundeemnet blir som standard emnet for salgsmuligheten og navnet på tilbuds- og prosjektkontrakten. |
| Type | Generelt, kategori | Dette alternativsettfeltet inneholder følgende alternativer:</br>- Arbeidsbasert (bare tilgjengelig når Project Operations er installert)</br>- Varebasert (bare tilgjengelig når Project Operations og Sales er installert)</br>- Basert på service og vedlikehold (tilgjengelig når Field Service er installert) | Når verdien i dette feltet er satt til **Arbeidsbaset** for kundeemnet, er kundeemnet kvalifisert til å opprette en prosjektbasert salgsmulighet. En prosjektbasert salgsmulighet kreves for å aktivere alle prosjektspesifikke utvidelser og funksjonalitet i den salgsprosessen nedstrøms for denne avtalen. |
| Fornavn | Generelt, kategori | Fornavnet til emnets kontaktperson | Når kundeemnet er kvalifisert, opprettes det en forretningsforbindelse, kontaktperson og salgsmulighet. Fornavnet for kontaktpersonen er verdien som er angitt her. |
| Etternavn | Generelt, kategori | Etternavnet til emnets kontaktperson | Når kundeemnet er kvalifisert, opprettes det en forretningsforbindelse, kontaktperson og salgsmulighet. Etternavnet for kontaktpersonen er verdien som er angitt her. |
| Selskap | Generelt, kategori | Navnet på kundeemnets firma | Når kundeemnet er kvalifisert, opprettes det en forretningsforbindelse, kontaktperson og salgsmulighet. Navnet på forretningsforbindelsen som er opprettet, er verdien som er angitt her. |
| Valuta | Detaljer-fanen | Valuta for kundeemne | Når kundeemnet er kvalifisert, opprettes det en forretningsforbindelse, kontaktperson og salgsmulighet. Valutaen til forretningsforbindelsen som er opprettet, er verdien som er angitt her. |

## <a name="qualify-a-new-project-based-lead"></a>Kvalifisere et nytt prosjektbasert kundeemne

Kundeemner som har **Type**-verdien satt til **Arbeidsbasert**, kalles for prosjektbaserte kundeemner. Når et prosjektbasert kundeemne er kvalifisert, opprettes følgende:

- En forretningsforbindelse som bruker **Firma**-feltet fra emnet.
- En kontaktoppføring som er knyttet til forretningsforbindelsen basert på verdiene i feltene **Fornavn** og **Etternavn** for kundeemnet.
- En prosjektbasert salgsmulighet som har **Type**-feltet satt til **Arbeidsbasert**.

Hvis du vil ha mer detaljert informasjon om kvalifiserende kundeemner, kan du se [Kvalifisere eller konvertere kundeemner](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Forretningsprosessflyt for prosjekt baserte avtaler

Følgende forretningsprosessflyter støttes for prosjektbaserte avtaler i Project Operations:

- Forretningsprosessen for kundeemne til salgsmulighet
- Salgsprosess for salgsmulighet

Forretningsprosessen for kundeemne til salgsmulighet støtter følgende faser:

| Fasenavn | Tilordnet enhet | Funksjonalitet |
| --- | --- | --- |
| Kvalifiser | Emne | Kvalifiser kundeemnet for å opprette en forretningsforbindelse, kontakt og salgsmulighet. |
| Utarbeid | Salgsmulighet | Utvikle salgsmuligheten for å legge til mer informasjon om arbeidet som er involvert, viktige interessenter og konkurranse. |
| Foreslå | Salgsmulighet | Utvikle forslaget, og få godkjennelse fra det interne gjennomgangsteamet. |
| Lukk | Salgsmulighet | Vinn salgsmuligheten for å lukke avtalen. |
