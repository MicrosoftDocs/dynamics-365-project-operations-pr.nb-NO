---
title: Behandle forslag om prosjektfaktura
description: Dette emnet inneholder detaljer om behandling av kunderettede fakturaer med Project Operations for ressurs- eller ikke-lagerbaserte scenarier.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4e663a9a0ca5b197e556d8c36233ab25affda876
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275865"
---
# <a name="manage-project-invoice-proposals"></a>Behandle forslag om prosjektfaktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Prosjektfakturaforslag kan behandles av faktureringsavdelingen når følgende to betingelser er oppfylt:

  - Prosjektlederen bekrefter proformafakturaen i Microsoft Dataverse.
  - Alle tidsbaserte og materielle ikke-fakturerte salgstransaksjoner som er inkludert i proformafakturaen, posteres ved hjelp av journalen for integrering av Dynamics 365 **Project Operations**.

Bruk fremgangsmåten nedenfor til å fullføre et prosjektfakturaforslag i Dynamics 365 Finance.

1. Se gjennom faktureringsinformasjon for etterregningstransaksjoner, og poster journalen for **integrering av Project Operations**.
2. Se gjennom faktureringsinformasjon for faktureringsmilepæler med fast pris.
3. Se gjennom og formatere prosjektfakturaforslag.
4. Postere og skrive ut prosjektfakturaer.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Behandle faktureringsinformasjon i journalen for integrering av Project Operations

Faktiske prosjekter som er opprettet i Dataverse, blir gjennomgått og lagt inn i Økonomi av prosjektregnskapsføreren. Hvis du vil ha mer informasjon om hvordan du arbeider med integreringsjournalen, kan du se [Integreringsjournal i Project Operations](../project-accounting/project-operations-integration-journal.md).

Faktiske kostnader og ufakturerte faktiske verdier for salg, legges til i integreringskladden som separate linjer:

  - Enhetskostnadsprisen og kostnadsbeløpet i den faktiske kostnaden fra transaksjonen for faktisk prosjektkostnad i Dataverse.
  - Enhetssalgspris og salgsbeløp i den ikke-fakturerte salgstransaksjonen er standard fra den ikke-fakturerte salgstransaksjonen i Dataverse for et faktisk prosjekt.

### <a name="billing-sales-tax"></a>Faktureringsavgift

Beregningen av salgsavgift for fakturering fastslås av kombinasjonen av feltene **Mva-gruppe for fakturering** og **Mva-gruppe for faktureringselement** på en ikke-fakturert salgsoppføring på journallinjen for **Project Operations-integrering**. Disse feltverdiene brukes som standard basert på innstillinger i kategorien **Økonomi** på siden **Parametere for prosjektstyring og regnskap**.

- **Metode for salgsavgiftsgruppe** bestemmer standardlogikken for faktureringsavgiftsgruppe:
  
  - **Prosjekt**: Vil alltid bruke gruppen for faktureringsavgift fra prosjektet som standard. Du kan se gjennom eller endre standardgruppen for merverdiavgift for fakturering for et prosjekt ved å velge **Vis standardregnskap** på siden **Alle prosjekter**.
  - **Prosjektkontrakt**: Vil alltid bruke gruppen for faktureringsavgift fra prosjektkontrakten som standard. Du kan se gjennom eller endre standardgruppen for merverdiavgift for en prosjektkontrakt ved å velge **Vis standardregnskap** på siden **Prosjektkontrakter**.
  - **Kunde**: Vil alltid bruke gruppen for faktureringsavgift fra kunden som standard.
  - **Søk**: Søker på tvers av alle enhetene ovenfor og velger den første tilgjengelige verdien. Søket starter med **Prosjekt**-enheten, deretter **Prosjektkontrakt**-enheten, og til slutt **Kunde**-enheten.

- **Metode for mva-gruppe for element** fastslår standardlogikken for mva-gruppe for faktureringselement:
  
  - For transaksjonstyper for tid, utgift og avgift vil gruppen for salgsavgift for faktureringselement alltid være standard fra enheten **Prosjektkategori**.
  - For materialtransaksjonstyper brukes standardverdiene for mva-gruppen for faktureringselement basert på innstillingen **Metode for mva-gruppe for element** i **Parametere for prosjektstyring og regnskap**. Varenummeret bruker som standard salgsavgiftsgruppen for elementet fra enheten **Utgitt produkt**. Kategorien bruker som standard salgsavgiftsgruppen for elementet fra enheten **Prosjektkategori**.

### <a name="financial-dimensions"></a>Finansdimensjoner

Finansdimensjonene for ufakturerte salgsoppføringer i journalen **Project Operations-integrering** hentes som standard fra **Prosjekt**-enheten. Finansdimensjoner kan ses gjennom og justeres ved å velge **Distribuer beløp**. Hvis du må endre finansdimensjonene for den ikke-fakturerte salgsoppføringen etter at integreringskladden er postert, men før proformafakturaen bekreftes, går du til **Alle prosjekter** > **Behandle** > **Publiserte transaksjoner**, velger transaksjonen, og velger deretter **Prosess** > **Justering av regnskap**.

### <a name="exchange-rates"></a>Valutakurser

Valuta for ufakturert transaksjon i Dataverse brukes som transaksjonsvaluta i Økonomi og konverteres til selskapets regnskapsvaluta ved hjelp av valutakurser som er definert i Økonomi.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Administrere finansattributter for faktureringsmilepæler 

Prosjektkontraktlinjer som bruker faktureringsmetoden med fast pris, faktureres via [Milepæler for fast pris](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Prosjektregnskapsføreren kan gå gjennom faktureringsmilepælene i Økonomi ved å gå til **Prosjektadministrasjon og regnskap** > **Alle prosjekter** > **Behandle** > **A-kontotransaksjoner**.

### <a name="billing-sales-tax"></a>Faktureringsavgift

Verdiene for **Mva-gruppe** og **Mva-gruppe for element** hentes som standard fra innstillingene når en ny faktureringsmilepæl opprettes i Dataverse. Systemet standardiserer verdiene til disse feltente basert på innstillinger i kategorien **Økonomi** på siden **Parametere for prosjektstyring og regnskap**.

- **Metode for mva-gruppe** fastslår standardiseringslogikken for **Mva-gruppe for fakturering**:

    - **Prosjekt** vil alltid bruke gruppen for faktureringsavgift fra prosjektet som standard. Du kan se gjennom eller endre standardgruppen for merverdiavgift for et prosjekt ved å velge **Vis standardregnskap** på siden **Alle prosjekter**.
    - **Prosjektkontrakt** vil alltid bruke gruppen for faktureringsavgift fra prosjektkontrakten som standard. Du kan se gjennom eller endre standardgruppen for merverdiavgift for en prosjektkontrakt ved å velge **Vis standardregnskap** på siden **Prosjektkontrakter**.
    - **Kunde** vil alltid bruke gruppen for faktureringsavgift fra kunden som standard.
    - **Søk** vil søke på tvers av alle enhetene i denne listen og velge den første tilgjengelige verdien. Søket starter med **Prosjekt**-enheten, deretter **Prosjektkontrakt**-enheten, og deretter **Kunde**-enheten.

- **Mva-gruppe for fast pris for milepælelement** brukes til å standardisere verdien i feltet **Mva-gruppe for element**.

### <a name="financial-dimensions"></a>Finansdimensjoner

Standard finansdimensjoner for faktureringsmilepælen med fast pris er angitt på prosjektkontraktlinjer. Gå til **Prosjektkontrakter** > **Vis standardregnskap**, og i kategorien **Kontraktlinjer** velger du **Priskontraktlinje**. Deretter angir du finansdimensjonsverdiene du vil bruke som standard.

Prosjektregnskapsføreren kan redigere informasjonen om salgsavgift og finansdimensjoner for fakturamilepæler til prosjektfakturaforslaget er opprettet.


## <a name="create-project-invoice-proposals"></a>Opprette forslag om prosjektfaktura

Prosjektfakturaforslag kan ses gjennom i modulen **Prosjektstyring og regnskap** ved å gå til **Prosjektfakturaer** > **Prosjektfakturaforslag**.

Toppteksten for prosjektfakturaforslag opprettes i Økonomi når proformafakturaen bekreftes i Dataverse. For enklere avstemming setter systemet nummeret på prosjektfakturaforslaget i Økonomi til samme nummer som proformafakturaens ID i Dataverse. Ettersom proformafakturaer ikke nødvendigvis bekreftes i samme rekkefølge som de er opprettet, må nummersekvensen for prosjektfakturaforslag i Økonomi tillate endringer til lavere og høyere tall. Konfigurer tallsekvenser ved å gjøre følgende:

1. Gå til **Administrasjon av organisasjon** > **Nummersekvenser** > **Nummersekvenser** i Økonomi.
2. I filteret **Område** velger du **Prosjekter**.
3. I filteret **Referanse** velgler du **Fakturaforslag**.
4. Bruk feltet **Firma** til å filtrere hver juridiske enhet med integrering av Project Operations Dataverse aktivert.
5. Åpne **Detaljer om nummersekvens**, og velg følgende i kategorien **Generelt**:

    - **Tillat brukerendringer: Til et lavere tall** = **Ja**
    - **Tillat brukerendringer: Til et høyere tall** = **Ja**

Linjer i prosjektfakturaforslag legges til av systemet ved hjelp av den periodiske prosessen **Import fra oppsamlingstabell** (**Prosjektstyring og regnskap** > **Periodisk** > **Project Operations-integrering** > **Import fra oppsamlingstabell**). Denne prosessen kan kjøres manuelt eller ved hjelp av en periodisk plan. Systemet legger ikke til linjer i fakturaforslagsdokumentet før alle linjene er klare til å bli fakturert. Tids- og materialtransaksjoner er klar til å faktureres bare når de posteres ved hjelp av journalen for **Project Operations-integrering**.

## <a name="format-and-print-invoice-proposals"></a>Formatere og skrive ut fakturaforslag

Prosjektregnskapsføreren kan tilpasse en prosjektfakturautskrift ved å bruke siden **Formater fakturaforslag** og skrive ut administrasjonsfunksjoner.

### <a name="format-invoice-proposals"></a>Formatere fakturaforslag

På siden **Formater fakturaforslag** kan egendefinerte grupperingstransaksjoner vises i kundeprosjektfakturaen.

1. På siden **Prosjektfakturaforslag** velger du **Skriv ut** > **Formater fakturaforslag**.
2. Velg **Ny** for å opprette en ny gruppering for prosjektfakturautskriften.
3. Velg alternativer for denne grupperingen i feltet **Detalj/Sammendrag**:

    - Velg **Detalj** for å skrive ut transaksjonsdetaljene for kundefakturaen.
    - Velg **Sammendrag** for å skrive ut transaksjonssammendraget for kundefakturaen.

> [!NOTE]
> Valget i feltet **Detalj/Sammendrag** på siden **Formater fakturaforslag** overstyrer alternativet som er valgt i feltet **Faktureringsformat** på siden **Fakturaforslag** for å skrive ut en detaljert faktura eller en sammendragsfaktura.

- Velg transaksjonslinjene som skal inkluderes i denne delen i kategorien **Available transactions**, og velg **Inkluder transaksjoner** for å flytte dem til kategorien **Valgra transaksjoner**.
- Velg **Flytt opp** og **Flytt ned** for å endre rekkefølgend på delene.
- Velg **Forhåndsvisning** for å forhåndsvise formatert faktura.

### <a name="print-management"></a>Utskriftsbehandling

Utskriftsbehandling bruker forskjellige rapportfiler til å skrive ut, angi mål og tilpasse bunntekst for fakturaen. Utskriftsbehandling kan konfigureres på modulnivå, men disse innstillingene kan overstyres for et bestemt kunde-, kontrakt- eller fakturaforslag. Hvis du vil ha tilgang til denne funksjonen på siden **Prosjektfakturaforslag**, velger du **Utskrift** > **Utskriftsbehandling**.

Oppsettet for utskriftsbehandling vises som en trevisning, der hvert nodenivå viser de tilgjengelige dokumentene som skal justeres. Du kan tilordne egendefinerte utskrifter på dokumentnivået modul, kunde, kontrakt eller fakturaforslag. Hvis du vil endre utskriften av det opprinnelige dokumentet, utvider du den ønskede noden og velger **Opprinnelig element**. I feltet **Rapportformat** velger du rapportformatet som skal brukes til å skrive ut. Du kan bruke egendefinerte rapportformater ved hjelp av [rammeverket for forretningsdokumentbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Publisere fakturaforslag

Når fakturaen er gjennomgått og redigert, og fakturaforslagslinjene er tilfredes, kontrollerer du totalbeløpet for fakturaen og merverdiavgift. Velg gruppen **Detaljer**, velg **Totalt**, og velg deretter **Publiser** for å publisere fakturaen.

Hvis du vil vise fakturaen før du publiserer, fjerner du merket for **Publisering**. **Proforma** blir trykt på fakturaen for å betegne at det er en eksempelfaktura. Merk av for **Skriv ut faktura** for å skrive ut fakturaen.

I tillegg til siden **Fakturaforslag** kan fakturaforslag også publiseres ved å kjøre den periodiske jobben, **Publisere fakturaforslag**. Du finner denne jobben ved å gå til **Prosjektbehandling og regnskap** > **Periodisk** > **Prosjektfakturaer** > **Publiser fakturaforslag**.

Denne siden viser alle fakturaforslagene som er klare til publisering. Du kan planlegge publisering av fakturaforslag ved å velge **Batch**. Sett **Parameter for satsvis behandling** til **Ja**, og angi regelmessigheten for satsvis behandling ved å velge **Regelmessighet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]