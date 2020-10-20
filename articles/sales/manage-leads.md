---
title: Behandle kundeemner
description: Denne emnet gir informasjon om behandling av prosjektbaserte kundeemner.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a10be42f4ae1ecc8ae5613ed8fdc669304e0ec72
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898633"
---
# <a name="manage-leads"></a>Behandle kundeemner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Prosjektrelaterte kundeemner kan administreres og kvalifiseres i Project Operations. Prosessen med behandling av kundeemner inkluderer opprettelse av arbeidsbaserte kundeemner og kvalifisering av disse kundeemnene. 

## <a name="project-sales-leads"></a>Kundeemner i prosjekt

I **Salg**-delen, i den venstre navigasjonsruten, åpner du listesiden **Kundeemner** for å vise en liste over alle kundeemneoppføringer i systemet. Listen over kundeemner som vises, er arbeidsbasert, og andre typer kundeemner kan opprettes hvis du også har Dynamics 365 Sales eller Dynamics 365 Field Service.

Du kan opprette en filtrert visning for å se bare kundeemner som er basert på prosjekter, ved å opprette et filter på **Type**-verdien. Du kan for eksempel velge å vise bare arbeidsbaserte kundeemner.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Opprett et nytt kundeemne for en prosjektbasert avtale

Når et prosjektbasert kundeemne er kvalifisert, opprettes det en salgsmulighet og en forretningsforbindelse. En prosjektbasert salgsmulighet er utgangspunktet for salgsoppfølgingsoppgaver i Salgsmulighet-fasen. Prosjektrelaterte salgsmuligheter har unike funksjoner som kreves for å selge prosjektarbeid. Disse funksjonene omfatter følgende:

- Faktureringsmetodene for tid og materiale og fast pris
- Prislister med flere gyldige datoer for personale, utgifter og materiell påløpt for prosjekter

Hvis du vil opprette en salgsmulighet automatisk for et kvalifisert kundeemne, setter du **Type**-attributtet til **Arbeidsbasert** når du oppretter kundeemnet. Hvis du velger en annen type, vil ikke emnet opprette en prosjektbasert salgsmulighet når det er kvalifisert. Hvis den prosjektbaserte psalgsmuligheten ikke blir opprettet, vil ikke de prosjektspesifikke funksjonene være tilgjengelig i salgsprosessene nedstrøms.

Tabellen nedenfor inneholder viktig feltinformasjon for et kundeemne, og innvirkningene nedstrøms av disse feltene.
 
| **Felt** | **Plassering** | **Relevans, formål og veiledning** | **Nedstrøms påvirkning** |
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
- En prosjektbasert salgsmulighet som har **Type**-feltet satt til &quot;**Arbeidsbasertert**.

Hvis du vil ha mer detaljert informasjon om kvalifisering av kundeemner, kan du se [Kvalifisere eller konvertere kundeemner](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Informasjon om emnekvalifisering og juridisk enhet 

Når du kjører Project Operations ved hjelp av distribusjonsmodusen Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, må hver kunde og salgsmulighet ha feltet **Eiende firma** angitt. Det eiende firmaet er en juridisk enhet i organisasjonen som eier levering av prosjektet. Hver kunde eller forretningsforbindelse relasjonstypen kunde må ha feltverdien **Eiende firma** angitt til den juridiske enheten som inngår kontrakter og forhandler med denne kunden. En kunde kan bare være i én juridisk enhet.

Når et emne kvalifiseres, vil kunde- og salgsmulighetsoppføringene som opprettes, ha **Eiende firma**-feltet angitt til firmaet til den gjeldende brukerens bestillbare ressursoppføring.

Hvis den gjeldende brukerens bestillbare ressursoppføring er tom, brukes verdien i feltet **Eiende firma** på brukeroppføringen som standard på kunde- og salgsmulighetsoppføringene.

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
