---
title: Behandle en proforma prosjektbasert faktura
description: Dette emnet inneholder informasjon om hvordan du behandler og arbeider med proforma prosjektbaserte fakturaer.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593762"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Behandle en proforma prosjektbasert faktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Proformafakturaer i Dynamics 365 Project Operations er bygget som en forlengelse til fakturaene i Dynamics 365 Sales. Det er imidlertid mange forskjeller i faktureringsprosessen mellom Salg og Project Operations når det gjelder fakturering. Det er for eksempel ikke mulig å opprette en ny faktura fra siden **Fakturaliste** i Project Operations, men det er mulig å gjøre dette i Salg. Disse forskjellene og utvidelsene er på plass for å støtte faktureringsprosesser for prosjekter som er forskjellige fra en vanlig faktura for en salgsordre.

> [!IMPORTANT]
> På grunn av forskjellene må du ikke bruke fakturaer i Salg og Project Operations om hverandre.

## <a name="invoice-header"></a>Fakturahode

Følgende informasjon er tilgjengelig for et proformatafakturahode i Project Operations.

| Felt | Sted | Beskrivelse |
| --- | --- | --- | 
| **Fakturanummer** | **Sammendrag**-fanen | ID-en som blir generert automatisk når en proformafaktura blir opprettet. Et skrivebeskyttet felt som er låst for redigering. Dette feltet brukes som referanse for hver proformafaktura. |
| **Navn** | **Sammendrag**-fanen | Angi navnet på prosjektkontrakten som standard. Dette feltet kan redigeres. | 
| **Valuta** | **Sammendrag**-fanen | Angi valutaen på prosjektkontrakten som standard. Et skrivebeskyttet felt som er låst for redigering. |
| **Prisliste** | **Sammendrag**-fanen | Angi prislisten på prosjektkontrakten som standard. Et skrivebeskyttet felt som er låst for redigering. | 
| **Salgsmulighet** | **Sammendrag**-fanen | Referansen til den koblede salgsmuligheten. Et skrivebeskyttet felt som er låst for redigering. | 
| **Kontrakt** | **Sammendrag**-fanen | Referansen til den koblede prosjektkontrakten. Et skrivebeskyttet felt som er låst for redigering. | 
| **Kunde** | **Sammendrag**-fanen | Referansen til den koblede prosjektkontrakten. Et skrivebeskyttet felt som er låst for redigering. |
| **Beskrivelse** | **Sammendrag**-fanen | Tekstfeltet som beskriver fakturaen. Dette feltet kan redigeres. | 
| **Faktura til** og relaterte felt | **Sammendrag-fane** | Standardverdiene angis fra projektkontraktkunden. Dette feltet kan redigeres.  | 
| **Status** | **Sammendrag**-fanen | Angir følgende alternativer: **Aktiv**, **Lukket**, **Betalt** og **Annullert**, og kan redigeres. Statusene for Project Operations inkluderer **Lukket** og **Annullert**. </br> Statusen settes til **Aktiv** når fakturaen opprettes. </br>Statusen skal bare settes til **Betalt** etter at fakturaen er bekreftet.  | 
| **Prosjektfakturastatus** | **Sammendrag**-fanen | Angir følgende alternativer: **Utkast**, **Til gjennomgang** og **Bekreftet**, og kan redigeres. I både **Utkast**- og **Til gjennomgang**-statusen kan du redigere fakturaen. Fakturaen kan ikke redigeres etter at den er bekreftet. | 
| **Nettobeløp** | **Sammendrag**-fanen | Summen av beløpene på alle fakturalinjene etter forskudd og fradrag. Et skrivebeskyttet felt som er låst for redigering.  Dette feltet brukes til å beregne det endelige beløpet. | 
| **Rabatt (%)** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi en rabattprosent. Dette feltet støttes ikke av Project Operations-funksjonalitet. Dette er et ustøttet felt.|  
| **Rabattbeløp** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi rabattbeløpet. Dette feltet støttes ikke av Project Operations-funksjonalitet. Dette er et ustøttet felt. |  
| **Beløp før frakt** | **Sammendrag-fane** | Det totale fakturabeløpet etter at rabatter er brukt. Et skrivebeskyttet felt som er låst for redigering. Dette feltet brukes til å beregne det endelige beløpet.  | 
| **Fraktbeløp** | **Sammendrag**-fanen | Du kan redigere dette feltet for å angi fraktbeløp. Dette feltet støttes ikke av Project Operations-funksjonalitet. Dette er et ustøttet felt. |
| **Avgifter totalt** | **Sammendrag**-fanen | Total avgift fra alle fakturalinjer på fakturaen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Totalbeløp** | **Sammendrag**-fanen | Summen av beløpet etter rabatter og avgifter. Summen er beløpet kunden må betale. | 

## <a name="project-based-invoice-lines"></a>Prosjektbaserte fakturalinjer

I Project Operations er det alltid én fakturalinje for hver prosjektkontraktlinje. Fakturalinjen opprettes selv om det ikke finnes noen faktiske verdier. Følgende informasjon er tilgjengelig for en proformatafakturalinje.

| Felt | Sted | Beskrivelse | 
| --- | --- | --- |
| **Fakturanummer** | **Generelt**-kategorien | Referansen til faktura-IDen. Et skrivebeskyttet felt som er låst for redigering. Du kan bruke fakturanummer-koblingen til å navigere tilbake til fakturahodet. | 
| **Navn** | **Generelt**-kategorien | Navnet på fakturalinjen som er angitt som standard, fra kontraktlinjenavnet. Dette feltet kan redigeres. |
| **Project** | **Generelt**-kategorien | Prosjektet på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. Prosjektkoblingen kan brukes til å navigere til prosjektet. | 
| **Faktureringsmetode** | **Generelt**-kategorien | Faktureringsmetoden på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. |
| **Kontraktlinjebeløp** | **Generelt**-kategorien | Kontraktbeløpet på den relaterte prosjektkontraktlinjen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Fakturert hittil** | **Generelt**-kategorien | Summen av beløpene på alle fakturalinjedetaljene for denne fakturaen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Beløp** | **Generelt**-kategorien | Summen av beløpene på alle belastbare fakturalinjedetaljene for denne fakturaen. Et skrivebeskyttet felt som er låst for redigering. Dette feltet brukes til å beregne det endelige beløpet på fakturahodet. | 
| **Avgift** | **Generelt**-kategorien | Summen av mva-beløpene på alle fakturalinjedetaljene for denne fakturalinjen. Et skrivebeskyttet felt som er låst for redigering. Dette feltet brukes til å beregne det endelige mva-beløpet på fakturahodet. | 
| **Samlet beløp** | **Generelt**-kategorien | Summen av totalbeløpene (**avgift + beløp**) på alle belastbare fakturalinjedetaljer for denne fakturalinjen. Et skrivebeskyttet felt som er låst for redigering. Dette feltet brukes til å beregne det endelige beløpet på fakturahodet. |

## <a name="invoice-line-details"></a>Fakturalinjedetaljer

Hver fakturalinje i en prosjektfaktura inkluderer fakturalinjedetaljer. Disse linjedetaljene er relatert til de ufakturerte faktiske verdiene for salg og milepæler som er relatert til kontraktlinjen som fakturalinjen refererer til. Alle disse transaksjonene er merket **Klar for fakturering**.

For en linje på en **Tid og materiale-faktura** er fakturalinjedetaljene gruppert som **Belastbar**, **Ikke-belastbar** og **Gratis** på **Fakturalinje**-siden. **Belastbar fakturalinje**-detaljer legges til fakturalinjetotalen. **Gratis** og **Ikke-belastbare faktiske verdier** legges ikke til fakturalinjesummen.

For en linje på en **fastprisfaktura** opprettes fakturalinjedetaljene fra milepæler som er merket som **Klar for fakturering** på den relaterte kontraktlinjen. Når fakturalinjedetaljene er opprettet fra en milepæl, oppdateres faktureringsstatusen på milepælen til **Opprettet kundefaktura**.

### <a name="edit-invoice-line-details"></a>Redigere fakturalinjedetaljer

Følgende felt er tilgjengelige i fakturalinjedetaljene som er støttet av et ikke-fakturert faktisk salg.

| Felt | Beskrivelse |
| --- | --- | 
| **Fakturalinje** | En referansen til **Fakturalinje-ID**. Dette feltet er skrivebeskyttet og låst for redigering. Denne koblingen kan brukes til å navigere tilbake til fakturahodet. | 
| **Beskrivelse** | En beskrivelse av fakturalinjedetaljen. Angis som standard fra feltet **Interne kommentarer** på **Tidsoppføring**, og fra **Beskrivelse**-feltet på **Utgiftsoppføring**. Feltet kan redigeres.| 
| **Ekstern beskrivelse** | En beskrivelse av fakturalinjedetaljen. Angis som standard fra feltet **Eksterne kommentarer** på **Tidsoppføring**, og fra feltet **Beskrivelse** på **Utgiftsoppføring**. Feltet kan redigeres. Denne beskrivelsen kan brukes til å bestemme hva som skal være på den utskrevne fakturaen som sendes til kunden. I Project Operations har ikke en proformafaktura all den nødvendige funksjonaliteten til å konfigurere utskriftsinnstillinger for en faktura. | 
| **Startdato** | Dette er et skrivebeskyttet felt som angis som standard fra den faktiske kilden. |
| **Project** | Dette er et skrivebeskyttet felt som angis som standard fra den faktiske kilden til prosjektet på den relaterte kontraktlinjen. |  
| **Oppgave** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |
| **Transaksjonskategori** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Rolle** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |  
| **Ressurs som kan reserveres** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Ressursstyringsfirma** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Ressursenhet** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Antall** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |  
| **Tidsplan for enhet** | For fakturalinjedetalj for tid er dette alltid satt til klokkeslett og kan ikke redigeres. For utgifter blir dette angitt som standard fra kilden til de faktiske utgiftene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Enhet** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |  
| **Pris** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |
| **Valuta** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Mengde** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Avgift** | Angi som standard fra de faktiske verdikildene. Feltet kan redigeres.| 
| **Samlet beløp** | Et beregnet felt, beregnet som **Beløp + avgift**. Et skrivebeskyttet felt som er låst for redigering. | 
| **Faktureringstype** | Angi som standard fra de faktiske verdikildene. Feltet kan redigeres. Hvis du velger **Belastbar** legges linjen til fakturalinjetotalen. **Gratis** og **Ikke-belastbar** vil utelate den fra fakturalinjesummen.| 
| **Velg produkt** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |
| **Produkt** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 
| **Produktnavn** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |  
| **Beskrivelse av produkt ikke i produktkatalog** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. |
| **Transaksjonstype** | Dette er et skrivebeskyttet felt som angis som standard fra den faktiske kilden til **Fakturert salg**. |  
| **Transaksjonsklasse** | Angi som standard fra de faktiske verdikildene. Et skrivebeskyttet felt som er låst for redigering. | 

Følgende felter er tilgjengelige på en fakturalinjedetalj som er støttet av en milepæl.

| Felt | Beskrivelse |
| --- | --- | 
| **Fakturalinje** | Referanse til **Fakturalinje-ID**. Et skrivebeskyttet felt som er låst for redigering. Koblingen kan brukes til å navigere tilbake til fakturahodet.  | 
| **Beskrivelse** | Beskrivelse av fakturalinjedetaljen. Angis som standard fra beskrivelsen av kildemilepælen. | 
|**Ekstern beskrivelse** | Beskrivelse av fakturalinjedetaljene som er angitt som standard fra beskrivelsen av kildemilepælen. Dette feltet kan brukes til å bestemme hva som skal være på den utskrevne fakturaen som sendes til kunden. En proformafaktura i Project Operations har ikke all nødvendig funksjonalitet til å konfigurere utskriftsinnstillinger for en faktura. | 
| **Startdato** | Angis som standard fra **Milepæl**-datoen i kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Project** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. |
| **Oppgave** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Transaksjonskategori** | Et skrivebeskyttet felt som er låst for redigering. |
| **Rolle** | Et skrivebeskyttet felt som er låst for redigering. | 
| **Ressurs som kan reserveres** | Et skrivebeskyttet felt som er låst for redigering. | 
| **Ressursenhet** | Et skrivebeskyttet felt som er låst for redigering. | 
| **Tidsplan for enhet** | Et skrivebeskyttet felt som er låst for redigering. | 
| **Enhet** | Et skrivebeskyttet felt som er låst for redigering. | 
| **Pris** | Angis som standard fra beløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. |
| **Valuta** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. |
| **Beløp** | Angis som standard fra beløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Avgift** | Angis som standard fra avgiftsbeløpet på kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. |
| **Samlet beløp** | Angis som standard fra det utvidede beløpet på kildemilepælen. Feltet kan redigeres. | 
| **Faktureringstype** | Alltid angitt som standard til **Belastbar**. Et skrivebeskyttet felt som er låst for redigering. |
| **Transaksjonstype** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | 
| **Transaksjonsklasse** | Angi som standard fra kildemilepælen. Et skrivebeskyttet felt som er låst for redigering. | 

## <a name="refresh-invoice-transactions"></a>Oppdater fakturatransaksjoner

Hvis du har faktiske verdier som kom inn etter at du har opprettet fakturaen, kan du inkludere disse faktiske verdiene på fakturaen.

1. I **visning for faktureringsresistanse** merker du data som **Klar for fakturering**.   
2. Åpne proformafakturautkastet, gå til **Handlinger**-båndet og velg **Oppdater fakturalinjetransaksjoner**.

  Fakturalinjedetaljer opprettes for eventuelle faktiske verdier som er datert tidligere og merket som **Klar for fakturering**, men som ikke er inkludert på fakturaen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
