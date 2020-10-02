---
title: Oversikt over prisdimensjoner
description: Dette emnet gir information om prisdimensjonene i Dynamics 365 Project Operations.
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898228"
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

Hvis du har behov for pris eller kostnad for ressursene ved hjelp av flere attributter, kan du opprette egendefinerte felt, enheter og dimensjoner.

## <a name="pricing-human-resource-time"></a>Prising av personaltid
Hvordan en organisasjon priser personaltid er ofte en viktig strategisk betraktning som direkte påvirker lønnsomheten i organisasjonen. Du kan arbeide med økonomiteamene og øve på når organisasjonen er klar til å identifisere hvordan de vil sette opp faktura- og kostnadssatser for personale.

Andre hensyn til prisingen inkluderer om felt eller enheter som ikke er prisdimensjoner, men gjelder som en prisdimensjon for organisasjonen, skal brukes på nytt. Felt som **Transaksjonskategori** (**msdyn_transactioncategory**) og **Bestillbar ressurs** (**bookableresource**) er eksempler på kandidatdimensjoner. 

Vurder om prisdimensjonen skal være en tabell eller et alternativsett. Hvis du forforutser endringer i verdiene til en dimensjon som vil overskride 10 eller 12, og du trenger flere attributter for disse verdiene, kan du opprette en enhet i stedet for et alternativsett. Vedlikehold av et alternativsett, for eksempel legge til eller fjerne verdier, krever en administrator eller utvikler, mens det å legge til nye rader i en tabell kan utføres av de fleste brukere.

Følgende eksempel viser kostnadssatser som er definert basert på rollen og organisasjonsenheten som ressursen tilhører. Kostnadssatser er vanligvis basert på lønnssatsen til den ansatte og organisasjonsenheten de tilhører. I dette eksemplet vil tabellene for faktura- og kostnadssats se slik ut:

**Eksempel på kostnadssatser**

| Rolle        | Organisasjonsenhet    |Enhet      |Pris      |Valuta  |
| ------------|-------------|----------|----------:|----------|
| Utvikler   | Contoso US  |Hour | 200|USD     |
| Utvikler   | Ekeli India |Hour|   112|USD     |


**Eksempel på kostnadssatser**

| Lønnssats     | Organisasjonsenhet    |Enhet      |Pris      |Valuta  |
| ----------------|-------------|----------|----------:|----------|
| Mitt firma_Band1 | Contoso US  |Hour | 145|USD     |
| Mitt firma_Band2 | Ekeli India |Hour|   67|USD     |
