---
title: Behandle en proforma prosjektfaktura
description: Dette emnet inneholder informasjon om hvordan du arbeider med proforma prosjektfakturaer.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2146e62bddc4a6286fa303ff2cc2c5622ea3133c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866918"
---
# <a name="manage-a-proforma-project-invoice"></a>Behandle en proforma prosjektfaktura 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Proformafakturaer i Dynamics 365 Project Operations er bygget som en forlengelse til fakturaene i Dynamics 365 Sales. Det er imidlertid mange forskjeller i faktureringsprosessen mellom Salg og Project Operations når det gjelder fakturering. Det er for eksempel ikke mulig å opprette en ny faktura fra siden **Fakturaliste** i Project Operations, men det er mulig å gjøre dette i Salg. Disse forskjellene og utvidelsene er på plass for å støtte faktureringsprosesser for prosjekter som er forskjellige fra en vanlig faktura for en salgsordre.

> [!IMPORTANT]
> På grunn av forskjellene må du ikke bruke fakturaer i Salg og Project Operations om hverandre.

## <a name="invoice-header"></a>Fakturahode

Følgende informasjon er tilgjengelig for et proformatafakturahode i Project Operations.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Fakturanummer** | **Sammendrag**-fanen | ID-en som blir generert automatisk når en proformafaktura blir opprettet. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes som referanse for hver proformafaktura. |
| **Navn** | **Sammendrag**-fanen | Angi navnet på prosjektkontrakten som standard. Dette feltet kan redigeres av brukeren. | &nbsp;  |
| **Valuta** | **Sammendrag**-fanen | Angi valutaen på prosjektkontrakten som standard. Et skrivebeskyttet felt som er låst for redigering. |&nbsp; |
| **Prisliste** | **Sammendrag**-fanen | Angi prislisten på prosjektkontrakten som standard. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Salgsmulighet** | **Sammendrag**-fanen | Referansen til den koblede salgsmuligheten. Et skrivebeskyttet felt som er låst for redigering. | &nbsp;  |
| **Kontrakt** | **Sammendrag**-fanen | Referansen til den koblede prosjektkontrakten. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Kunde** | **Sammendrag**-fanen | Referansen til den koblede prosjektkontrakten. Et skrivebeskyttet felt som er låst for redigering. |&nbsp;  |
| **Beskrivelse** | **Sammendrag**-fanen | Tekstfeltet som beskriver fakturaen. Dette feltet kan redigeres av brukeren. | &nbsp; |
| **Faktura til** og relaterte felt | **Sammendrag-fane** | Standardverdiene angis fra projektkontraktkunden. Dette feltet kan redigeres av brukeren.  | &nbsp; |
| **Status** | **Sammendrag**-fanen | Angir følgende alternativer: **Aktiv**, **Lukket**, **Betalt** og **Kansellert**, og kan redigeres av brukeren. | Statusene for Project Operations inkluderer **Lukket** og **Annullert**. </br> Statusen settes til **Aktiv** når fakturaen opprettes. </br>Statusen skal bare settes til **Betalt** etter at fakturaen er bekreftet. |
| **Prosjektfakturastatus** | **Sammendrag**-fanen | Angir følgende alternativer: **Utkast**, **Til gjennomgang** og **Bekreftet**, og kan redigeres av brukeren. | I både **Utkast**- og **Til gjennomgang**-statusen kan du redigere fakturaen. Fakturaen kan ikke redigeres etter at den er bekreftet. |
| **Nettobeløp** | **Sammendrag**-fanen | Summen av beløpene på alle fakturalinjene etter forskudd og fradrag. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes til å beregne det endelige beløpet. |
| **Rabatt (%)** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi en rabattprosent. Dette feltet støttes ikke av Project Operations-funksjonalitet. | Dette er et ustøttet felt. |
| **Rabattbeløp** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi rabattbeløpet. Dette feltet støttes ikke av Project Operations-funksjonalitet. | Dette er et ustøttet felt. |
| **Beløp før frakt** | **Sammendrag-fane** | Det totale fakturabeløpet etter at rabatter er brukt. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes til å beregne det endelige beløpet. |
| **Fraktbeløp** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi fraktbeløp. Dette feltet støttes ikke av Project Operations-funksjonalitet. | Dette er et ustøttet felt. |
| **Avgifter totalt** | **Sammendrag**-fanen | Total avgift fra alle fakturalinjer på fakturaen. Et skrivebeskyttet felt som er låst for redigering. | Ingen. |
| **Totalbeløp** | **Sammendrag**-fanen | Summen av beløpet etter rabatter og avgifter. | Summen er beløpet kunden må betale. |
## <a name="project-based-invoice-lines"></a>Prosjektbaserte fakturalinjer

I Project Operations er det alltid én fakturalinje for hver prosjektkontraktlinje. Fakturalinjen opprettes selv om det ikke finnes noen faktiske verdier. Følgende informasjon er tilgjengelig for en proformatafakturalinje.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| **Fakturanummer** | **Generelt**-kategorien | Referansen til faktura-IDen. Et skrivebeskyttet felt som er låst for redigering. | Du kan bruke fakturanummer-koblingen til å navigere tilbake til fakturahodet. |
| **Navn** | **Generelt**-kategorien | Navnet på fakturalinjen som er angitt som standard, fra kontraktlinjenavnet. Dette feltet kan redigeres av brukeren. | &nbsp; |
| **Project** | **Generelt**-kategorien | Prosjektet på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. | Prosjektkoblingen kan brukes til å navigere til prosjektet. |
| **Faktureringsmetode** | **Generelt**-kategorien | Faktureringsmetoden på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Kontraktlinjebeløp** | **Generelt**-kategorien | Kontraktbeløpet på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Fakturert hittil** | **Generelt**-kategorien | Summen av beløpene på alle fakturalinjedetaljene for denne fakturaen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Beløp** | **Generelt**-kategorien | Summen av beløpene på alle belastbare fakturalinjedetaljene for denne fakturaen. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes til å beregne det endelige beløpet på fakturahodet. |
| **Avgift** | **Generelt**-kategorien | Summen av mva-beløpene på alle fakturalinjedetaljene for denne fakturalinjen. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes til å beregne det endelige mva-beløpet på fakturahodet. |
| **Samlet beløp** | **Generelt**-kategorien | Summen av totalbeløpene (**avgift + beløp**) på alle belastbare fakturalinjedetaljer for denne fakturalinjen. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet brukes til å beregne det endelige beløpet på fakturahodet. |


## <a name="invoice-line-details"></a>Fakturalinjedetaljer

Hver fakturalinje i en prosjektfaktura inkluderer fakturalinjedetaljer. Disse linjedetaljene er relatert til de ufakturerte faktiske verdiene for salg og milepæler som er relatert til kontraktlinjen som fakturalinjen refererer til. Alle disse transaksjonene er merket **Klar for fakturering**.

For en linje på en **Tid og materiale-faktura** er fakturalinjedetaljene gruppert som **Belastbar**, **Ikke-belastbar** og **Gratis** på **Fakturalinje**-siden. **Belastbar fakturalinje**-detaljer legges til fakturalinjetotalen. **Gratis** og **Ikke-belastbare faktiske verdier** bidrar ikke til totalsummen på fakturalinjen.

For en linje på en **fastprisfaktura** opprettes fakturalinjedetaljene fra milepæler som er merket som **Klar for fakturering** på den relaterte kontraktlinjen. Når fakturalinjedetaljene er opprettet fra en milepæl, oppdateres faktureringsstatusen på milepælen til **Opprettet kundefaktura**.

### <a name="edit-invoice-line-details"></a>Redigere fakturalinjedetaljer

Følgende felt er tilgjengelige i en fakturalinjedetalj som er støttet av et ikke-fakturert faktisk salg:

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| **Fakturalinje** | En referansen til **Fakturalinje-ID**. Skrivebeskyttet felt, låst for redigering. | Denne koblingen kan brukes til å navigere tilbake til fakturahodet. |
| **Beskrivelse** | En beskrivelse av fakturalinjedetaljen. Angis som standard fra feltet **Interne kommentarer** på **Tidsoppføring**, og fra **Beskrivelse**-feltet på **Utgiftsoppføring**. Feltet kan redigeres av brukeren.| &nbsp; |
| **Ekstern beskrivelse** | En beskrivelse av fakturalinjedetaljen. Angis som standard fra feltet **Eksterne kommentarer** på **Tidsoppføring**, og fra feltet **Beskrivelse** på **Utgiftsoppføring**. Feltet kan redigeres av brukeren. | Denne beskrivelsen kan brukes til å bestemme hva som skal være på den utskrevne fakturaen som sendes til kunden. I Project Operations har ikke en proformafaktura all den nødvendige funksjonaliteten til å konfigurere utskriftsinnstillinger for en faktura. |
| **Startdato** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Dette feltet kan redigeres i en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. |
| **Project** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Angi som standard til prosjektet på den relaterte kontraktlinjen. |
| **Oppgave** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres i en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. En rullegardin liste viser alle oppgavene som er knyttet til den relaterte prosjektkontraktlinjen.  |
| **Transaksjonskategori** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk kilde. |
| **Rolle** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. |
| **Ressurs som kan reserveres** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk kilde. |
| **Ressursenhet** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. |
| **Antall** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. |
| **Tidsplan for enhet** | For fakturalinjedetalj for tid er dette alltid satt til klokkeslett og kan ikke redigeres. For utgifter blir dette angitt som standard fra kilden til de faktiske utgiftene. Et skrivebeskyttet felt som er låst for redigering. | Settes som standard til **Tid** på en ny fakturalinjedetalj som ikke er støttet av en faktisk verdi. |
| **Enhet** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke er støttet av en faktisk verdikilde |
| **Pris** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Feltet kan redigeres på en ny fakturalinjedetalj som ikke blir støttet av en faktisk verdikilde. Hvis det ikke er angitt noen verdi, blir den som standard angitt etter **Lagre**. |
| **Valuta** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Angis som standard fra fakturahodet når du oppretter en ny fakturadetalj som ikke er støttet av en faktisk verdi.  Et skrivebeskyttet felt som er låst for redigering. |
| **Beløp** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Beregnet som **Antall \* Pris** når du oppretter en ny fakturadetalj som ikke er støttet av en faktisk verdi. Det beregnes etter at du velger **Lagre**. Et skrivebeskyttet felt som er låst for redigering. |
| **Avgift** | Angi som standard fra de faktiske verdikildene. Feltet kan redigeres av brukeren | Feltet kan redigeres av brukeren når du oppretter en ny fakturalinjedetalj som ikke er støttet av en faktisk verdi. |
| **Samlet beløp** | Et beregnet felt, beregnet som **Beløp + avgift**. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Faktureringstype** | Angi som standard fra de faktiske verdikildene. Feltet kan redigeres av brukeren. | Hvis du velger **Belastbar** legges linjen til fakturalinjetotalen. **Gratis** og **Ikke-belastbar** vil utelate den fra fakturalinjesummen. |
| **Velg produkt** | Dette feltet er skrivebeskyttet som standard fra den faktiske kilden. | Når du oppretter en ny fakturalinjedetalj uten en understøttende faktisk verdi, kan dette feltet redigeres. |
| **Produkt** | Dette feltet er skrivebeskyttet som standard fra den faktiske kilden. | Når du oppretter en ny fakturalinjedetalj uten en understøttende faktisk verdi, kan dette feltet redigeres hvis **Velg produkt**-feltet er satt til **Eksisterende produkt**. |
| **Produktnavn** | Dette feltet er skrivebeskyttet som standard fra den faktiske kilden. | I en ny fakturalinjedetalj der produkt-ID-en velges fra katalogen, settes dette feltet til produktnavnet. For et produkt som ikke er i produktkatalogen, settes feltet til navnet på produktet som ikke er i produktkatalogen. |
| **Beskrivelse av produkt ikke i produktkatalog** | Dette feltet er skrivebeskyttet som standard fra den faktiske kilden. | Når du oppretter en ny fakturalinjedetalj uten en understøttende faktisk verdi, kan du legge til en skrivebeskrivelse for produktet som ikke er i produktkatalogen. |
| **Transaksjonstype** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Settes som standard til **Fakturert salg** og låses når du oppretter en ny **Fakturalinjedetalj** som ikke er støttet av en faktisk verdi.  |
| **Transaksjonsklasse** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | Angi som standard basert på om brukeren velger å opprette en fakturalinjedetalj av typen **Tid**, **Utgift**, **Materiale** eller **Gebyr**, samtidig som det også opprettes en ny **fakturalinjedetalj** uten en understøttende faktisk verdi. Låst fra redigering. |

Følgende felter er tilgjengelige på en fakturalinjedetalj som er støttet av en milepæl:

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| **Fakturalinje** | Referanse til **Fakturalinje-ID**. Et skrivebeskyttet felt som er låst for redigering. | Koblingen kan brukes til å navigere tilbake til fakturahodet. |
| **Beskrivelse** | Beskrivelse av fakturalinjedetaljen. Angis som standard fra beskrivelsen av kildemilepælen. | &nbsp; |
|**Ekstern beskrivelse** | Beskrivelse av fakturalinjedetaljene som er angitt som standard fra beskrivelsen av kildemilepælen. | Dette feltet kan brukes til å bestemme hva som skal være på den utskrevne fakturaen som sendes til kunden. En proformafaktura i Project Operations har ikke all nødvendig funksjonalitet til å konfigurere utskriftsinnstillinger for en faktura. |
| **Startdato** | Angis som standard fra **Milepæl**-datoen i kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Project** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Oppgave** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Transaksjonskategori** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Rolle** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Ressurs som kan reserveres** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Ressursenhet** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Tidsplan for enhet** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Enhet** | Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Pris** | Angis som standard fra beløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Valuta** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. |&nbsp; |
| **Beløp** | Angis som standard fra beløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Avgift** | Angis som standard fra avgiftsbeløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Samlet beløp** | Angis som standard fra det utvidede beløpet på kildemilepælen. Feltet kan redigeres av brukeren | &nbsp; |
| **Faktureringstype** | Alltid angitt som standard til **Belastbar**. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Transaksjonstype** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |
| **Transaksjonsklasse** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | &nbsp; |

### <a name="create-new-invoice-line-details"></a>Opprette nye fakturalinjedetaljer

Du kan opprette nye fakturalinjedetaljer på tid og material-fakturalinjer. Disse fakturalinjedetaljene blir ikke støttet av en faktisk verdi. På fakturalinjen for en tid og material-fakturalinje kan du velge **Ny** for å opprette en ny fakturalinjedetalj for transaksjonsklassene som er inkludert på kontraktlinjen.

## <a name="refresh-invoice-transactions"></a>Oppdater fakturatransaksjoner

Hvis du har faktiske verdier som kom inn etter at du har opprettet fakturaen, kan du inkludere disse faktiske verdiene på fakturaen.

1. I **visning for faktureringsresistanse** merker du data som **Klar for fakturering**.   
2. Åpne kladdeproformafakturaen og, på båndet **Handlinger** klikker du **Oppdater fakturalinjetransaksjoner**.

  Dette oppretter fakturalinjedetaljer for faktiske verdier som er datert tidligere og merket som **Klar til fakturering**, men er ikke inkludert i fakturaen.

## <a name="product-based-invoice-lines"></a>Produktbaserte fakturalinjer

I Project Operations kan du opprette fakturalinjer for produkter som ikke gjelder for noe prosjekt eller for alle prosjekter sammen med prosjektbaserte fakturalinjer. Disse fakturalinjene opprettes som produktbaserte kontraktlinjer, og etter at de er merket som klare til fakturering, blir de lagt til som produktbaserte fakturalinjer.

Når du har lagt til produktbasert fakturalinjer, kan de ikke endres. De kan imidlertid slettes fra kladdeproformafakturaen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
