---
title: Konfigurere egendefinerte felt som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du konfigurerer prisdimensjoner ved hjelp av egendefinerte felt.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3a2a3b48df02853e519a45dc1d37052c8ba2529d
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896608"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Konfigurere egendefinerte felt som prisdimensjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Før du begynner antar dette emnet at du har fullført prosedyrene i emnene [Opprette egendefinerte felt og enheter](create-custom-fields-entities-pricing-dimensions.md) og [Legge til obligatoriske egendefinerte felt i prisoppsett og transaksjonsenheter](add-custom-fields-price-setup-transactional-entities.md). Hvis du ikke har utført disse prosedyrene, kan du gå tilbake og fullføre dem og deretter gå tilbake til dette emnet. 

Dette emnet gir informasjon om hvordan du konfigurerer egendefinerte prisdimensjoner. På **Parametere**-siden viser kategorien **Beløpsbaserte prisdimensjoner** oppføringene i Prisdimensjoner-enhetene. Som standard er det to rader i rutenettet i denne kategorien:

- **msdyn_resourcecategory** (rolle)
- **msdyn_OrganizationalUnit** (organisasjonsenhet)

> [!IMPORTANT]
> Ikke slett disse radene. Hvis du ikke trenger dem, kan du imidlertid gjøre dem tilgjengelige i en bestemt kontekst ved å angi **Gjelder kostnad**, **Gjelder salg** og **Gjelder kjøp** til **Nei**. Ved å sette disse attributtverdiene til **Nei**, har det samme effekt som å ikke ha feltet som prisdimensjon.

For at et felt skal bli en prismodell, må det være følgende:

- Opprettet som et felt i enhetene **Rollepris** og **Rolleprispåslag**. For mer informasjon om hvordan du gjør dette, se [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](add-custom-fields-price-setup-transactional-entities.md).
- Opprettet som en rad i tabellen **Prisdimensjon**. Legg for eksempel til prisdimensjonsrader som vises i grafikken nedenfor. 

Arbeidstimer for ressurs (**msdyn_resourceworkhours**) er lagt til som en påslagsbasert dimensjon og er lagt til i rutenettet i kategorien **Påslagsbasert prisdimensjon**.

> [!IMPORTANT]
> Alle endringer i prisdimensjonsdata i denne tabellen, eksisterende eller nye, overføres bare til prisforretningslogikken når hurtigbufferen er oppdatert. Oppdateringstiden for bufferen kan ta opptil 10 minutter. Vent denne tiden for å se endringene i standardlogikken for priser som må resultere fra endringer i prisdimensjonsdata.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributter for prisdimensjonstabellen
Avsnittene nedenfor inneholder informasjon om de forskjellige attributtene i tabellen **Prisdimensjoner**.

### <a name="pricing-dimension-name"></a>Prisdimensjonsnavn
Denne verdien må være identisk med skjemanavnet til feltet som legges til i tabellen **Rollepris** for egendefinerte prisdimensjoner. Hvis du vil ha mer informasjon om hvordan du legger til felt i tabellen **Rollepris**, kan du se [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimensjonstype
Det finnes to typer prisdimensjoner:
  
  - **Beløpsbaserte dimensjoner**: Dimensjonsverdiene fra inndatakonteksten samsvares med dimensjonsverdiene på linjen **Rollepris**, og prisen/kostnaden settes som standard direkte fra tabellen **Rollepris**.
  - **Påslagsbaserte prisdimensjoner**: Dette er dimensjoner der følgende tre-trinnsprosess brukes til å hente pris/kostnad:
 
    1. De ikke-påslagsbaserte dimensjonsverdiene fra inndatakonteksten samsvares med Rollepris-linjen for å hente basisprisen.
    2. Dimensjonsverdiene fra inndatakonteksten samsvares med **Rolleprispåslag**-linjen for å hente påslagsprosenten.
    3. Påslagsprosenten fra det andre trinnet brukes på basisprisen som hentes fra **Rollepris**-tabellen i det første trinnet, for å komme til endelig pris/kostnad.
   
   Tabellen nedenfor illustrerer beregning av prispåslag.
  
| Rolle        | Organisasjonsenhet    |Arbeidssted      |Standardtittel      |Arbeidstid for ressurs      |  Påslag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Ekeli India|På stedet            |                    |Overtid                 |15     |
|             | Ekeli India|Lokal             |                    |Overtid                 |10     |
|             | Contoso US   |Lokal             |                    |Overtid                 |20     |


Hvis en ressurs fra Ekeli India som har en basispris på 100 USD, arbeider på stedet, og de registrerer 8 timer normal tid og 2 timer overtid i tidsoppføringen, vil prismotoren bruke basisprisen på 100 for de 8 timene for å registrere 800 USD. For de 2 timene overtid brukes et påslag på 15 % på basisprisen på100 for å få en enhetspris på 115 USD, og det registreres en total kostnad på 230 USD.

### <a name="applicable-to-cost"></a>Gjelder kostnad 
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av kostnads- og påslagsrater.

### <a name="applicable-to-sales"></a>Gjelder salg
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av faktura- og påslagsrater.

### <a name="applicable-to-purchase"></a>Gjelder kjøp
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av kjøpsprisen. Det er ikke støtte for underleveransescenarioer, så dette feltet brukes ikke. 

### <a name="priority"></a>Prioritet
Ved å angi dimensjonsprioriteten kan prisingen produsere en pris selv når den ikke finner et nøyaktig samsvar mellom inndatadimensjonsverdiene og verdiene fra tabellene **Rollepris** eller **Rolleprispåslag**. I dette scenarioet brukes nullverdier for dimensjonsverdier som ikke samsvarer, ved å vekte dimensjonene i henhold til prioriteten.

- **Kostnadsprioritet**: Verdien for dimensjonens kostnadsprioritet angir vekten på denne dimensjonen når den samsvares med oppsettet for kostpriser. Verdien for **Kostnadsprioritet** må være unik på tvers av dimensjoner som **Gjelder kostnad**.
- **Salgsprioritet**: Verdien for dimensjonens salgsprioritet angir vekten på denne dimensjonen når den samsvares med oppsettet for salgspriser eller fakturasatser. Verdien for **Salgsprioritet** må være unik på tvers av dimensjoner som **Gjelder salg**.
