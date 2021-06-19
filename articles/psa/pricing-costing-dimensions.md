---
title: Hjemmeside for pris- og kostnadsdimensjoner
description: Dette emnet gir en oversikt over prisdimensjoner.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9a2e2f7ed394229bbc553af9e616a6f322857195
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009268"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Hjemmeside for pris- og kostnadsdimensjoner

[!include [banner](../includes/psa-now-project-operations.md)]

Dimensjonene som brukes til å angi pris og kostnad for arbeid i prosjektbaserte organisasjoner, er påvirket av følgende attributter:

- Personer som utfører arbeid som ligner på deres erfaring, rolle eller geografi
- Arbeid som skal utføres på samme måte som kompleksiteten eller tiden på dagen

Gitt den vanlige typen av disse attributtene for arbeidet og personene som kreves for å utføre arbeidet, er de to typer prisdimensjonsverdier tilgjengelige i Project Service Automation: 

- **Alternativsett** – attributter som er faste opplistinger for et sett med verdier.
- **Enhetsbaserte verdier** – attributter som kan ha et variert sett med verdier som er begrensede, men som kan endre seg over tid.

## <a name="pricing-dimensions"></a>Prisdimensjoner

PSA leveres med et standardsett med prisdimensjoner. Du kan vise disse ved å gå til **Project Service** > **Parametere**. i parameteroppføringen, i kategorien **Beløpsbaserte prisdimensjoner** kontrollerer du at rollen **msdyn_resourcecategory** og ressursorganisasjonsenheten **msdyn_organizationalunit** har feltene **Gjelder salg** og **Gjelder kostnad** satt til **Ja**. Dette gjør det mulig å konfigurere prisen og kostnaden for hver kombinasjon av rolle og organisasjonsenhet.

![Skjermbilde av Project Service-parametere med "Gjelder salg" uthevet](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Hvis du har brukt de medfølgende feltene for rolle og organisasjonsenhet som prisdimensjoner før versjon 3 av PSA, vil det ikke være noen observerbar endring. Du kan fortsette å bruke Project Service på vanlig måte. 

Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner. Hvis du vil ha mer informasjon, kan du se følgende emner, men vær oppmerksom på at du må fullføre prosedyrene i rekkefølgen angitt nedenfor:

- [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md)
- [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md)
- [Konfigurere egendefinerte felt som prisdimensjoner ](set-up-pricing-dimensions.md)
- [Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Prising av personaltid
Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen. Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.

Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt. Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner. 

Vurder om prisdimensjonen skal være en tabell eller et alternativsett. Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett. Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste bedriftsbrukere.

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