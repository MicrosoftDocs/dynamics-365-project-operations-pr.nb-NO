---
title: Konsernintern fakturering
description: Denne artikkelen inneholder informasjon og eksempler på konsernintern fakturering for prosjekter.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1debf8f67b7dbe7752075c6f8e5f2cdd37a3ae
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002788"
---
# <a name="intercompany-invoicing"></a>Konsernintern fakturering

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon og eksempler på konsernintern fakturering for prosjekter.

Det kan hende at organisasjonen har flere divisjoner, datterselskaper og andre juridiske enheter som overfører produkter og servicer til hverandre for prosjekter. Den juridiske enheten som leverer tjenesten eller produktet, kalles den *juridiske utlånsenheten*, og den juridiske enheten som mottar tjenesten eller produktet, kalles den *juridiske låneenheten*. 

Illustrasjonen nedenfor viser et typisk scenario der to juridiske enheter, SI FR (den juridiske låneenheten), og SI USA (den juridiske utlånsenheten) deler ressurser for å levere et prosjekt til kunde A. I dette scenarioet skal SI FR brukes til å levere arbeidet til kunde A. 

[![Eksempel på konsernintern fakturering](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Målet er å gjøre kostnadskontroll, inntektsføring, avgifter og overføringspris for konserninterne prosjekttransaksjoner mer fleksible og effektive. I tillegg leveres følgende funksjoner:

-   Opprett kundefakturaer mot et prosjekt i en juridisk låneenhet, ved å bruke konserninterne timeregistreringer, utgifter og leverandørfakturaer i en juridisk utlånsenhet.
-   Støtter avgiftsberegninger og indirekte kostnader.
-   Utsett inntektsføring i en juridisk utlånsenhet og når en juridisk låneenhet skal gjenkjenne kostnaden.
-   Akkumuler VIA-inntekter i juridisk utlånsenhet.
-   Angi overføringspriser som kan være basert på forskjellige prismodeller. Her er noen eksempler:
    -   **Antall** – Beløpet du angir i feltet **Priser**, er faktisk kostnad per antall eller enhet.
    -   **Gebyrbeløp** – Prisen/kostnaden per transaksjon pluss gebyrbeløpet du skriver inn i **Pris**-feltet.
    -   **Gebyrprosent** – Overføringsprisen er prisen/kostnaden per transaksjon multiplisert med gebyrprosenten du har angitt i **Pris**-feltet.
    -   **Prosent av salgspris** – Prosentandelen av salgsprisen som er overført til den juridiske utlånsenheten.
    -   **Beløp under salgspris** – Beløpet som den juridiske låneenheten holder tilbake fra salgsprisene før overføringen til den juridiske utlånsenheten.
    -   **Dekningsgrad** – Antallet du skriver inn i **Pris**-feltet, er dekningsgraden, som uttrykkes som en prosentandel av salgsprisen.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Eksempel 1: Konfigurere parametere for konsernintern fakturering
I dette eksemplet er USSI en juridisk utlånsenhet, og ressursene rapporterer tid mot den juridiske låneenheten, FRSI, som eier kontrakten med sluttkunden. Timer og utgifter som USSI-ansatte rapporterer om, kan inkluderes i prosjektfakturaen som FRSI genererer. I tillegg finnes det en tredje kilde over transaksjoner som kan være hentet fra den juridiske utlånsenheten (USSI i dette eksemplet) når den leverer delte leverandørtjenester til datterselskaper (for eksempel FRSI), og deretter sender disse kostnadene til prosjekter innenfor disse datterselskapene. Alle samsvarende fakturadokumenter og avgiftsberegninger fullføres i Finance. 

I dette eksemplet må FRSI være en kunde i den juridiske enheten USSI, og USSI må være en leverandør i den juridiske enheten FRSI. Deretter kan du konfigurere en konsernintern relasjon mellom de to juridiske enhetene. Fremgangsmåten nedenfor viser hvordan du konfigurerer parameterne slik at begge juridiske enheter kan delta i konsernintern fakturering.

1. Konfigurer FRSI som en kunde i den juridiske enheten USSI, og sett opp USSI som en leverandør i den juridiske enheten FRSI. Det finnes tre startpunkter for trinnene som kreves for denne oppgaven.

   | Trinn |                                                       Startpunkt                                                        |                                                                                                                                                                                               Beskrivelse                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | I USSI klikker du <strong>Utestående fordringer</strong> &gt; <strong>Kunder</strong> &gt; <strong>Alle kunder</strong>. |                                                                                                                                                                  Opprett en ny kundeoppføring for FRSI, og velg deretter kundegruppen.                                                                                                                                                                  |
   |  F   |    I FRSI klikker du <strong>Leverandørgjeld</strong> &gt; <strong>Leverandører</strong> &gt; <strong>Alle leverandører</strong>.     |                                                                                                                                                                    Opprett en ny leverandøroppføring for USSI, og velg deretter leverandørgruppen.                                                                                                                                                                    |
   |  C   |                                  Åpne leverandøroppføringen du nettopp opprettet, i FRSI.                                  | I handlingsruten i kategorien <strong>Generelt</strong> i gruppen <strong>Oppsett</strong> velger du <strong>Konsernintern</strong>. På siden <strong>Konsernintern</strong> i kategorien <strong>Handelsforbindelse</strong> setter du glidebryteren <strong>Aktiv</strong> til <strong>Ja</strong>. I feltet <strong>Kundefirma</strong> velger du kundeoppføringen du opprettet i trinn A. |


2. Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Parametere for prosjektstyring og regnskap**, og klikk deretter kategorien **Konsernintern**. Måten du angir parametere på, avhenger av om du er den juridiske låneenheten eller den juridiske utlånsenheten.
   -   Hvis du er en juridisk låneenhet, velger du innkjøpskategorien som skal brukes til å samsvare med leverandørfakturaer, som genereres automatisk.
   -   Hvis du er juridisk utlånsenhet, velger du en standard prosjektkategori for hver av transaksjonstypene for hver utlånsenhet. Prosjektkategorier brukes for avgiftskonfigurasjon når den fakturerte kategorien i konserninterne transaksjoner bare eksisterer i den juridiske låneenheten. Du kan velge å avsette omsetning for konserninterne transaksjoner. Denne avsetningen utføres når transaksjonene blir postert, og da tilbakeføres den når den konserninterne fakturaen bokføres.

3. Klikk **Prosjektstyring og regnskap** &gt; **Oppsett** &gt; **Priser** &gt; **Overføringspris**.
4. Velg en valuta, transaksjonstype og modell for overføringspris. Valutaen som brukes på fakturaen, er valutaen som konfigureres i kundeoppføringen for den juridiske låneenheten i den juridiske utlånsenheten. Valutaen brukes til å samsvare oppføringer i tabellen overføringspris.
5. Klikk **Økonomimodul** &gt; **Bokføringsoppsett** &gt; **Konserninternt regnskap**, og angi en relasjon for USSI og FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Eksempel 2: Opprette og postere konserninterne timeregistreringer
USSI, den juridiske utlånsenheten, må opprette og postere timeregistreringen for et prosjekt fra FRSI, som er den juridiske låneenheten. Det finnes to startpunkter for trinnene som kreves for denne oppgaven.

| Trinn | Startpunkt                                                                       | Beskrivelse                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Prosjektstyring og regnskap** &gt; **Timeregistreringer** &gt; **Alle timeregistreringer** | Opprett en ny timeregistrering. Velg **FRSI** på timeregistreringslinjen i feltet **Juridisk enhet**. Velg prosjektet i FRSI i feltet **Prosjekt-ID**. Angi timene for hver ukedag. |
| F    | Siden **Timeregistrering**                                                                | Når arbeidsflyten kjører, posterer du timeregistreringen og noterer bilagsnummeret.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Eksempel 3: Opprette og postere konsernintern leverandørfaktura
USSI, den juridiske utlånsenheten, må opprette og postere den konserninterne leverandørfakturaen for et prosjekt fra FRSI, som er den juridiske låneenheten. Denne leverandørfakturaen representerer arbeidet og utgiften som er satt ut, som ble utført av leverandører som er betalt av USSI. Det finnes to startpunkter for trinnene som kreves for denne oppgaven.

| Trinn | Startpunkt                                                                                      | Beskrivelse                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverandør** &gt; **Fakturaer** &gt; **Åpne leverandørfakturaer** &gt; **Ny leverandørfaktura** | Opprett en ny leverandørfaktura, og angi tjenestene som ble skaffet på vegne av FRSIens prosjekt.                                                                                                                                                                                  |
| F    | Siden **Leverandørfaktura**                                                                      | Angi linjer som representerer de utsatte tjenestene på vegne av FRSI. På hurtigfanen **Linjedetaljer** i kategorien **Prosjekt** for fakturalinjen, i feltet **Prosjektselskap**, angir du **FRSI**. Angi prosjektet og tilhørende informasjon. Deretter bokfører du leverandørfakturaen. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Eksempel 4: Opprette og postere den konserninterne fakturaen
USSI, den juridiske utlånsenheten, må opprette og postere den konserninterne fakturaen. Det finnes to startpunkter for trinnene som kreves for denne oppgaven.

| Trinn | Startpunkt                                                                                             | Beskrivelse                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konsernintern kundefaktura**  | Klikk **Ny** for å åpne siden **Opprett konsernintern faktura**.                                                                                  |
| F    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konsernintern kundefakturaer** | På siden **Opprett konsernintern faktura** angir du den juridiske enheten, angi hvilken transaksjon som skal tas med, og klikk deretter **Søk**. |
| C    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Konsernintern kundefakturaer** | Velg transaksjonene som skal faktureres, eller klikk **Velg alle** for å fakturere alle transaksjonene i listen, og klikk deretter **OK**.                  |
| D    | Siden **Konsernintern faktura**                                                                       | Det konserninterne kundefakturaforslaget vises.                                                                                             |
| E    | Siden **Konsernintern faktura**                                                                       | Klikk **Publiser**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Eksempel 5: Postere leverandørfakturaen og fakturere kunden
Når den juridiske utlånsenheten, USSI, legger inn den konserninterne kundefakturaen, opprettes det en samsvarende ventende leverandørfaktura i den juridiske låneenheten, FRSI. Når denne leverandørfakturaen er postert, fakturerer også FRSI prosjektkunden for timene som USSI angav. Det finnes tre startpunkter for trinnene som kreves for denne oppgaven.

| Trinn | Startpunkt                                                                                        | Beskrivelse                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Leverandørgjeld** &gt; **Fakturaer** &gt; **Ventende leverandørfakturaer**                            | Se gjennom fakturaen for å kontrollere at timeregistreringsverdiene er inkludert, og bokfør deretter leverandørfakturaen.                  |
| F    | **Prosjektstyring og regnskap** &gt; **Prosjektfakturaer** &gt; **Fakturaforslag for prosjekt** | Opprett en ny prosjektfaktura for prosjektet, og kontroller at timetransaksjonene som ble postert, vises.            |
| C    | Siden **Prosjektfaktura**                                                                       | Velg prosjektfakturaen, og klikk deretter **Vis detaljer** for å se gjennom kostnads- og salgsbeløpet. Deretter bokfører du fakturaen. |


Hvis du vil ha mer informasjon, kan du se [Konfigurere konsernintern prosjektfakturering](tasks/configure-intercompany-project-invoicing.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]