---
title: Oversikt over prisdimensjoner
description: Dette emnet gir informasjon om prisdimensjonene i Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 4b3b71c0b64a24f6914c70c4383eee654e7d4947ececaf9b4e6394f45a081a4c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001983"
---
# <a name="pricing-dimensions-overview"></a>Oversikt over prisdimensjoner

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Dimensjonene som brukes i personalet til å definere priser og kostnader, kan deles inn i to kategorier:

- Personer
- Planlagt arbeid

På grunn av dette er to typer prisdimensjonsverdier tilgjengelige:

- **Alternativsett**: Dimensjoner som er faste opplistinger for et sett med verdier.
- **Enhetsbaserte verdier**: Dimensjoner som kan være et variert sett med verdier.

## <a name="pricing-dimensions"></a>Prisdimensjoner

Dynamics 365 Project Operations leveres med et standardsett med prisdimensjoner. Du kan vise disse prisdimensjonene ved å gå til **Project Operations** > **Parametere**. i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**. Når disse feltene er aktivert, kan du konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.

![Skjermbilde av Project Service-parametere med Gjelder salg uthevet.](media/PS-OOB-parameters.png)

Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner. Hvis du vil ha mer informasjon, kan du se følgende emner. 
  
  > [!NOTE]
  > Prosedyrene må fullføres i den rekkefølgen de vises.

1. [Opprette en løsning for egendefinerte prisdimensjoner](../sales/create-solution-custompd.md)
2. [Opprette egendefinerte felt og enheter](create-custom-fields-entities-pricing-dimensions.md)
3. [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter ](add-custom-fields-price-setup-transactional-entities.md)
4. [Konfigurere egendefinerte felt som prisdimensjoner ](set-up-custom-fields-pricing-dimensions.md)
5. [Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a>Prising av personaltid
Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen. Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.

Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt. Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner. 

Vurder om prisdimensjonen skal være en tabell eller et alternativsett. Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett. Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.

Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører. Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører. I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:

**Eksempel på kostnadssatser**

| Rolle        | Organisasjonsenhet    |Enhet      |Pris      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Utvikler   | Contoso – USA  |Time | 200|USD     |
| Utvikler   | Contoso India |Time|   112|USD     |


**Eksempel på kostnadssatser**

| Lønnssats     | Organisasjonsenhet    |Enhet      |Pris      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mitt firma_Band1 | Contoso – USA  |Time | 145|USD     |
| Mitt firma_Band2 | Contoso India |Time|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]