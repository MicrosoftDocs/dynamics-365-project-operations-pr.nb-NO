---
title: Legge til obligatoriske egendefinerte felt i prisoppsett og transaksjonsenheter
description: Denne artikkelen inneholder informasjon om hvordan du legger til obligatoriske egendefinerte feltreferanser i enheter og skjemaer og visninger.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a984dc9e04857e101fa012734fd822440899aced
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926052"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Legge til obligatoriske egendefinerte felt i prisoppsett og transaksjonsenheter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen forutsetter at du har fullført fremgangsmåtene i artikkelen [Opprette egendefinerte felter og enheter som skal brukes som prisdimensjoner](create-custom-fields-entities-pricing-dimensions.md). Hvis du ikke har fullført disse fremgangsmåtene, kan du gå tilbake og fullføre dem og deretter gå tilbake til denne artikkelen. 

I denne artikkelen viser fremgangsmåtene hvordan du legger til de obligatoriske egendefinerte feltreferansene i enheter og i brukergrensesnittelementene, for eksempel skjemaer og visninger.

## <a name="add-custom-pricing-dimension-fields"></a>Legg til egendefinerte felt for prisdimensjon 
Når egendefinerte felt og enheter er opprettet, er det neste trinnet å gjøre prisoppsett og transaksjonsenheter klar over egendefinerte enheter eller alternativsett, ved å opprette referansefelt. Avhengig av om prisdimensjonslisten inneholder alternativsettdimensjoner eller enhetsdimensjoner eller begge deler, følger du bare trinnene i **Egendefinerte prisdimensjoner basert på alternativsett** eller **Egendefinerte prisdimensjoner basert på enheter**, eller begge deler.

### <a name="option-set-based-custom-pricing-dimensions"></a>Egendefinerte prisdimensjoner basert på alternativsett
Når en egendefinert prisdimensjon er basert på alternativsett, legger du den til som et felt i viktige enheter. I fremgangsmåten nedenfor brukes **Arbeidssted for ressurs** og **Arbeidstimer for ressurs** som prisdimensjoner basert på alternativsett. Disse må først legges til som felt i prisenhetene **Rollepris** og **Rolleprispåslag**.

1. I Project Operations velger du **Innstillinger** > **Løsninger** og dobbeltklikker **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Rollepris**.
3. Vis **Rollepris**-enheten, og velg **Felt**.
4. Velg **Ny** for å opprette et nytt felt kalt **Arbeidssted for ressurs**, og velg **Alternativsett** som felttype. 
5. Velg **Bruk et eksisterende alternativsett**, velg alternativsettet **Arbeidssted for ressurs**, og klikk deretter **Lagre**.
6. Gjenta trinn 1-5 for å legge dette til feltet i enheten **Rolleprispåslag**. 
7. Gjenta trinn 1-5 for alternativsettet **Arbeidstimer for ressurs**.

> [!IMPORTANT]
> Når du legger til et felt i mer enn én enhet, bruker du det samme feltnavnet på tvers av alle enhetene. 

> ![Legge til arbeidssted for ressurs i rollepris.](media/RWL-Field.png)

I salgs- og estimeringsfasene for et prosjekt brukes en beregning av arbeidsinnsatsen som kreves for å utføre **lokalt** arbeid og **arbeid på stedet**, i **vanlige timer** og **overtidstimer** til å beregne verdien for tilbudet/prosjektet. Feltene **Arbeidssted for ressurs** og **Arbeidstimer for ressurs** legges til i estimatenhetene **Tilbudslinjedetalj**, **kontraktlinjedetalj**, **Prosjektteammedlem** og **Estimatlinje**.

1. I Project Operations velger du **Innstillinger** > **Løsninger** og dobbeltklikker **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Tilbudslinjedetalj**.
3. Utvid enheten **Tilbudslinjedetalj**, og velg **Felt**.
4. Velg **Ny** for å opprette et nytt felt kalt **Arbeidssted for ressurs**, og velg **Alternativsett** som felttype. 
5. Velg **Bruk et eksisterende alternativsett** og **Arbeidssted for ressurs**, og klikk deretter **Lagre**.
6. Gjenta trinn 1-5 for å legge til dette feltet i enhetene **Detalj for prosjektkontraktlinjer**, **Prosjektteammedlem** og **Estimatlinje**.
7. Gjenta trinn 1-6 for alternativsettet **Arbeidstimer for ressurs**. 

> ![Legge til arbeidssted for ressurs i estimatlinje.](media/RWL-Default-Value.png)

For levering og fakturering må fullført arbeid være nøyaktig priset for å kunne velge om det ble utført **lokalt** eller **på stedet**, og om det ble fullført i **normal tid** eller **overtid** for faktiske verdier for prosjektet. Feltene **Arbeidssted for ressurs** og **Arbeidstimer for ressurs** må legges til i enhetene **Tidsoppføring**, **Faktisk verdi**, **Fakturalinjedetalj** og **Journallinje**.

1. Velg **Innstillinger** > **Løsninger**, og dobbeltklikk deretter **\<your organization name>-prisdimensjoner**.
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Tidsoppføring**.
3. Utvid enheten **Tilbudslinjedetalj**, og velg deretter **Felt**.
4. Velg **Ny** for å opprette et nytt felt kalt **Arbeidssted for ressurs**, og velg **Alternativsett** som felttype. 
5. Velg **Bruk et eksisterende alternativsett**, velg alternativsettet **Arbeidssted for ressurs**, og klikk deretter **Lagre**.
6. Gjenta trinn 1-5 for å legge til dette feltet i enhetene **Faktiske verdier**, **Fakturalinjedetalj** og **Journallinje**.
7. Gjenta trinn 1-6 for alternativsettet **Arbeidstimer for ressurs**. 

> ![Legge til arbeidssted for ressurs i tidsoppføring.](media/RWL-time-entry.png)

Dette fullfører skjemaendringene som kreves for egendefinerte dimensjoner basert på alternativsett.

## <a name="entity-based-custom-pricing-dimensions"></a>Egendefinerte prisdimensjoner basert på enheter

Når den egendefinerte prisdimensjonen er en enhet, legger du til 1:N-relasjoner mellom enhetene for dimensjonsenheten og de viktige enhetene. Når du bruker eksemplet med standardtittel ovenfor, er det rimelig å forvente at hver ansatt blir tilordnet en standardtittel. Derfor trenger du en 1:N-relasjon fra standardtittel til bestillbar ressurs, eller en N:1-relasjon hvis den ble opprettet fra bestillbar ressurs til standardtittel.

1. I Project Operations velger du **Innstillinger** > **Løsninger** og dobbeltklikker **\<your organization name>-prisdimensjoner**. 
2. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Standardtittel**.
3. Utvid enheten **Standardtittel**, og velg **1:N-relasjoner**.
4. Klikk **Ny** for å opprette en ny 1:N-relasjon kalt for **Standardtittel til bestillbar ressurs**. Angi den nødvendige informasjonen, og klikk deretter **Lagre**.

> ![Legge til standardtittel som et referansefelt for bestillbar ressurs.](media/ST-BR.png)

Standardtittelen må også legges til i prisenhetene **Rollepris** og **Rolleprispåslåg**. Dette utføres også med 1:N-relasjoner mellom enhetene **Standardtittel** og **Rollepris** og enhetene **Standardtittel** og **Rolleprispåslag**.

1. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Standardtittel**.
2. Utvid enheten **Standardtittel**, og velg **1:N-relasjoner**.
3. Klikk **Ny** for å opprette en ny 1:N-relasjon kalt for **Standardtittel til rollepris**. Angi den nødvendige informasjonen, og klikk deretter **Lagre**.
4. Gjenta trinn 1-4 for å opprette 1:N-relasjoner mellom enhetene **Standardtittel** og **Rolleprispåslag**.

I salgs- og estimeringsfasene for prosjektet, for å prise tilbudet/prosjektet, kreves det en estimater av arbeidsinnsatsen for hver standardtittel. Dette betyr at 1:N-relasjoner fra Standardtittel for hver av disse estimeringsenhetene er nødvendig: 

- **Tilbudslinjedetalj**
- **Detalj for prosjektkontraktlinjer**
- **Prosjektteammedlem**
- **Estimatlinje**

5. Gjenta trinn 1-5 for å opprette 1:N-rlasjoner fra **Standardtittel** til **Tilbudslinjedetalj**, **Detalj for prosjektkontraktlinjer**, **Prosjektteammedlem** og **Estimatlinje**.

> ![Legge til standardtittel som et referansefelt for estimatlinje.](media/ST-Estimate-Line.png)

  I leverings- og faktureringsfasene må arbeidet som er fullført i hver standardtittel, være nøyaktig priset i de faktiske verdiene for prosjektet. Dette betyr at det må være 1:N-relasjoner fra enhetene **Standardtittel** til **Tidsoppføring**, **Faktisk verdi**, **Fakturalinjedetalj** og **Journallinje**.

6. Gjenta trinn 1-6 for å opprette 1:N-relasjoner fra enhetene **Standardtittel** til **Tidsoppføring**, **Faktisk verdi**, **Fakturalinjedetalj** og **Journallinje**.

> ![Legge til standardtittel som et referansefelt for tidsoppføring.](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Konfigurere standard dimensjonsverdi ved hjelp av tilordningsfunksjonene på plattformen
For tidsoppføringer kan det være nyttig å få systemet til å standardisere standardtittelen på tidsoppføringen fra den bestillbare ressursen som registrerer tidsoppføringen. Bruk fremgangsmåten nedenfor for å legge til felttilordninger i 1:N-relasjonen fra **Bestillbar ressurs** til **Tidsoppføring**.

1. I Løsningsutforsker, i den venstre navigasjonsruten, velger du **Enheter > Standardtittel**.
2. Utvid enheten **Standardtittel**, og velg **1:N-relasjoner**.
3. Dobbeltklikk **Bestillbar ressurs til tidsoppføring**. På **Relasjon**-siden klikker du **Bruk felttilordninger**. 
4. Klikk **Ny** for å opprette en ny felttilordning mellom feltet **Standardtittel** i enheten **Bestillbar ressurs** til referansefeltet **Standardtittel** i **Tidsoppføring**-enheten. 

> ![Definer felttilordninger for å tillate standardisering av standardtittel fra bestillbar ressurser til tidsoppføring.](media/ST-Mapping2.png)

Dette fullfører skjemaendringene som kreves for egendefinerte dimensjoner basert på enheter.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Legge til egendefinerte felt i skjemaer, visninger og forretningsregler

Når du har utført alle de nødvendige skjemaendringene, er det neste trinnet å gjøre feltene synlige i brukergrensesnittet ved å legge til feltene i skjemaene og visningene.

1. Åpne skjemaet eller visningen. I den høyre navigasjonsruten velger du feltet og drar det til skjemalerretet. 
2. Hvis du redigerer en visning, bruker du den høyre navigasjonsruten til å klikke **Legg til felt**, og i dialogboksen **Feltoppføring** velger du feltene du vil ha, og deretter klikker du **OK**.

Tabellen nedenfor er en omfattende liste over de medfølgende skjemaene og visningene som er oppført etter entitet, som må oppdateres med de nye feltene. Hvis du har andre visninger eller skjemaer i tilpassingen på disse enhetene, legger du til de nye feltene også.

| Entity        | Skjemaer som trenger det nye feltet   |Visninger som trenger det nye feltet      |
| ------------------------------|---------------------------------|----------------------------------|
|  Rollepris|• Informasjon |• Aktive ressurskategoripriser<br> • Tilknyttet visning for ressurskategoripriser|
|  Rolleprispåslag|• Informasjon|• Aktive rolleprispåslag<br>• Tilknyttet visning for rolleprispåslag|
|  Tilbudslinjedetalj|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Aktiv tilbudslinjedetalj<br>• Kombinerte tilbudslinjedetaljer<br>• Tilknyttet visning for tilbudslinjedetaljer|
|  Detalj for prosjektkontraktlinjer|• Prosjektinformasjon<br>• Hurtigoppretting av prosjekter|• Kombinerte kontraktlinjedetaljer<br>• Aktive kontraktlinjedetaljer<br>• Tilknyttet visning for kontraktlinjedetaljer|
|  Prosjektteammedlem|• Informasjon<br>• Nytt skjema|• Aktive prosjektteammedlemmer<br>• Prosjektteammedlemmer<br>• Tilknyttet visning for prosjektteammedlemmer|
|  Tidsoppføring|• Informasjon<br>• Opprett tidsoppføring|• Mine tidsoppføringer etter dato<br>• Mine tidsoppføringer for denne uken<br>• Tidsoppføringer for godkjenning|
|  Journallinje|• Informasjon<br>• Hurtigoppretting|• Aktive journallinjer<br>• Tilknyttet visning for journallinjer|
|  Fakturalinjedetalj|• Informasjon<br>• Hurtigoppretting|• Aktive fakturalinjedetaljer<br>• Belastbare fakturatransaksjoner<br>• Gratis fakturatransaksjoner<br>• Tilknyttet visning for fakturalinjedetaljer<br>• Ikke-belastbare fakturatransaksjoner|
|  Faktisk|• Informasjon<br>• Aktive faktiske data|• Tilknyttet visning for faktiske data|

Egendefinerte felt må også legges til i forretningsregler, avhengig av hva du har definert. Et typisk eksempel er for forretningsregelen **Redigerbarhet for tidsoppføring basert på status**. Denne regelen definerer hvilke felt som må låses når tidsoppføringen er i en status som ikke kan redigeres, for eksempel **Godkjent**. Legg til felt i denne forretningsregelen, slik at feltene låses for redigering når tidsoppføringen er i en annen status enn **Utkast** eller **Returnert**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]