---
title: Konfigurer ikke lagerførte materialer og ventende leverandørfakturaer
description: Dette emnet forklarer hvordan du aktiverer ikkee lagerførte materialer og ventende leverandørfakturaer.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880671"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Konfigurer ikke lagerførte materialer og ventende leverandørfakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

## <a name="minimum-version-requirement"></a>Påkrevd minimumsversjon

Bruk av ikke lagerført materiell og ventende leverandørfakturaer for Dynamics 365 Project Operations ikke lagerførte/ressursbaserte scenarier krever følgende versjoner:

Dynamics 365 Dataverse-løsninger:

- Project Operations – 4.9.0.221 eller senere
- Ordningsløsning for dobbel skriving – 2.2.2.23 eller høyere

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) eller høyere. Sørg for at Økonomi-miljøet er oppdatert og at alle kvalitetsoppdateringer brukes for å oppfylle minimumskravene for versjon.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Kjøre tilordninger for dobbel skriving for ikke-lagerført materiell og integrering av leverandørfaktura

Denne delen inneholder informasjon om spesifikke tilordninger som kreves for ikke-lagerført materiell og leverandørfakturaer. Kontroller at de nødvendige tilordningene som er oppført i emnet [Klargjøre et nytt miljø](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps), kjører i miljøet.

1. Gå til Lifecycle Services (LCS), gå til LCS-prosjektet og gå til siden **Miljødetaljer**.
2. I delen **Common Data Service-miljøinformasjon** velger du **Koble til CDS for Apps**. Når du har valgt koblingen, blir du omdirigert til listen over enheter i tilordningene.
3. Kontroller at følgende tilordninger kjører. Hvis de ikke kjører, starter du dem og kontrollerer at de inneholder alle relaterte tabelltilordninger.

    - CDS ga ut distinkte produkter (produkter)
    - Leverandører v2 (msdyn_vendors)
    - Project Operations-tabell for materialestimater (msdyn_estimatelines)
    - Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn_projectvendorinvoices)
    - Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn_projectvendorinvoicelines)
    - Faktiske verdier for Project Operations-integrering (msdyn_actuals). Kontroller at du kjører kartversjon 1.0.0.14 eller høyere. Du kan se den aktive versjonen av tilordningen i **Versjon**-kolonnen på siden **Dobbel skriving**. Du kan aktivere en ny versjon av tilordningen ved å velge **Tabelltilordningsversjon**, og deretter lagre den valgte versjonen.

Hvis du bruker standard demonstrasjonsdata, kan det også hende du må stoppe og starte følgende enhetstilordninger på nytt med første synkronisering:
  - Betalingsdager CDS V2 (msdyn_paymentdays)
  - Betalingsplan (msdyn_paymentschedules)
  - Betalingsbetingelser (msdyn_paymentterms)
  - Leverandørgrupper (msdyn_vendorgroups)
  - Enheter (uom)

> [!NOTE]
> Den første synkroniseringen for leverandørgrupper og enheter kan mislykkes for noen få oppføringer i det eksisterende demonstrasjonsdatasettet. Du kan ignorere feilene fordi de ikke vil hindre deg i å bruke demonstrasjonsdata med Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Konfigurere krav i Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Aktiver arbeidsflyt for å opprette forretningsforbindelser basert på leverandørenhet

Ordningsløsningen for dobbel skriving gir [hovedintegrering av leverandører](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Som en forutsetning for denne funksjonen må leverandørdata opprettes i **Forretningsforbindelser**-enheten. Aktiver en arbeidsflytprosess for maler for å opprette leverandører i tabellen **Forretningsforbindelser**, som beskrevet i [Veksle mellom leverandørutforminger](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Angi at produkter skal opprettes som aktive

Ikke-lagerført materiell må konfigureres som **Frigitte produkter** i Økonomi. Ordningsløsningen for dobbel skriving gir en standard [frigitt produktintegrering i Dataverse-produktkatalogen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Produkter fra Økonomi synkroniseres som standard til Dataverse i utkasttilstand. Hvis du vil synkronisere produktet til en aktiv tilstand, slik at det kan brukes direkte i materielle bruksdokumenter eller ventende leverandørfakturaer, går du til **System** > **Administrasjon** > **Systemadministrasjon** > **Systeminnstillinger**, og i **Salgs**-kategorien setter du deretter **Opprett produkter i aktiv tilstand** til **Ja**.

## <a name="configure-prerequisites-in-finance"></a>Konfigurere krav i Økonomi

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Aktivere funksjonsnøkkelen for ventende leverandørfakturaer

Fullfør fremgangsmåten nedenfor for å aktivere funksjonalitet for å legge til prosjektdetaljer på ventende fakturalinjer for leverandør.

1. Gå til arbeidsområdet **Funksjonsbehandling** i Økonomi.
2. Finn funksjonen for å **aktivere ventende leverandørfakturaer i Project Operations for ressursbaserte/ikke-lagerførte scenarioer**, og velg **Aktiver**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definere kategorigrupper og prosjektkategorier for elementer

Konfigurer minst én kategorigruppe for transaksjonstypen **Element**, og minst én prosjektkategori ved hjelp av denne gruppen. Hvis du vil ha mer informasjon, kan du se [Konfigurere prosjektkategorier](../project-accounting/configure-project-categories.md#category-groups).

Se gjennom prosjektkostnads- og omsetningsprofilene, og konfigurer oppsett for finanspostering for varetransaksjoner. Hvis du vil ha mer informasjon, kan du se [Konfigure regnskap for fakturerbare prosjekter](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Konfigurere et produkt ikke i produktkatalog

I Project Operations kan du registrere materialestimater og bruk for katalogprodukter som er konfigurert i den frigitte produktkatalogen og for produkter som ikke er i produktkatalogen. Bruk av produkter som ikke er i produktkatalogen, krever ett enkelt utgitt produkt som er konfigurert i Økonomi for dette formålet. Fullfør fremgangsmåten nedenfor for å konfigurere et produkt som ikke er i produktkatalogen. Gjenta disse trinnene i hver juridiske enhet som bruker Project Operations for scenarier for ressurser/ikke-lagerførte operasjoner.

1. I Økonomi går du til **Produktinformasjonsbehandling** > **Produkter** > **Frigitte produkter**, og velg **Ny**.
2. I **Produkttype**-feltet velger du **Vare** og deretter **Produkt** i feltet **Produktets undertype**.
3. Angi produktnummeret (WRITEIN) og produktnavnet (ikke i produktkatalogen).
4. Velg varemodellgruppen. Kontroller at varemodellgruppen du velger, har feltet **Lagerpolicy for lagerført produkt** satt til **Usann**.
5. Velg verdier i feltene **Varegruppe**, **Lagringsdimensjonsgruppe** og **Sporing av dimensjonsgruppe**. Bruk **lagringsdimensjonen** bare for **Sted**, og ikke angi sporingsdimensjoner.
6. Velg verdier i feltet **Lagerenhet**, **Innkjøpsenhet** og **Salgsenhet**, og lagre deretter endringene.
7. Angi standard ordeinnstillinger i kategorien **Plan**, og angi deretter standard sted og lager i kategorien **Lagerbeholdning**.
8. Gå til **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**, og åpne **Project Operations i Dynamics 365 Dataverse**. 
9. Velg produktet du opprettet, i **Materialer**-fanen i feltet **Ikke i produktkatalog**.
10. I områdekartet i Dataverse-miljøet velger du **Produkter**-enheten og finner produktoppføringen som ikke er i produktkatalogen. 
11. Åpne oppføringsdetaljene, og angi produktstatus til **Avviklet**. Denne produkttilstanden hindrer at noen ved et uhell kan bruke denne oppføringen direkte i materielle estimater og bruksdokumenter.

### <a name="set-up-a-procurement-integration-account"></a>Konfigurere en integrasjonskonto for innkjøp

Integrasjonskontoen for innkjøp brukes som en avregningskonto når du posterer en ventende leverandørfaktura med linjer tillagt et prosjekt.

Når systemet posterer en ventende leverandørfaktura, brukes denne kontoen for prosjektkostnadsbeløpet. Leverandørfakturadetaljene behandles i Dataverse, og det opprettes et tilsvarende faktisk prosjekt. Informasjonen fra det faktiske prosjektet legges til i journalen for integrering av Project Operations. Når du posterer integreringsjournalen, tømmes beløpet fra integrasjonskontoen for innkjøp og registreres til prosjektkostnaden.

1. For å konfigurere integrasjonskontoen for innkjøp gå til **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**, og åpne **Project Operations i Dynamics 365 Dataverse**. 
2. Velg kategorien **Materialer**, og velg verdien i feltet **Integrasjonskonto for innkjøp**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Konfigurere prosjektkategoristandarder for en vare

1. I Økonomi går du til **Prosjektstyring og regnskap** > **Oppsett** > **Parametere for prosjektstyring og regnskap**, og åpner **Project Operations i Dynamics 365 Dataverse**. 
2. Velg en verdi i kategorien **Prosjektkategoristandarder** i **Vare**-feltet. Denne prosjektkategorien brukes for materielle transaksjoner hvis prosjektkategorien ikke er angitt for oppføringen for faktiske prosjekter.
