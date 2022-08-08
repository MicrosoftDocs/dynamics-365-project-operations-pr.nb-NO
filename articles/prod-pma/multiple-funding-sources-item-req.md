---
title: Varekrav for prosjektkontrakter med flere finansieringskilder
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer og bruker varekrav med flere finansieringskilder.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028500"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Varekrav for prosjektkontrakter med flere finansieringskilder

_**Gjelder for:** Project Operations for lagerførte/produksjonsbaserte scenarioer_

Noen kontraktavtaler for prosjektbaserte leveringer kan kreve flere finansieringskilder. Denne artikkelen forklarer hvordan du velger og konfigurerer de ønskede finansieringskildene når flere kilder kreves for et prosjekt eller en prosjektkontrakt.

## <a name="terminology"></a>Terminologi

- **Finansieringskilde** – Enheten som finansierer prosjektkontraktens arbeid. Denne enheten kan være en intern organisasjon eller en ekstern fakturakonto (kunde eller tilskudd).
- **Prosjektkunde** – Enheten som prosjektarbeidet leveres til.
- **Fakturakonto** – Den eksterne enheten som betaler for prosjektarbeidet.

## <a name="example"></a>Eksempel

Contoso har vunnet en kontrakt for fornyelse av utstyr med to av sine kunder: Adatum US og Adatum Corporate. Kontrakten omfatter maskinvare- og installasjonstjenester som skal leveres til Adatum US (prosjektkunden). Maskinvaren skal finansieres av Adatum Corporate (fakturakonto 1), og installasjonsarbeidet skal finansieres av Adatum US (fakturakonto 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Konfigurer standardregler for fakturakontoer for varekrav

### <a name="prerequisites"></a>Forutsetning

- Microsoft Dynamics 365 Finance **versjon 10.0.27 eller senere** kreves for å bruke varekrav som har flere fakturakontoer.
- Systemadministratoren må aktivere funksjonen **Tillat varekrav med flere finansieringskilder for lagerførte/produksjonsbaserte scenarioer i Project Operations** i arbeidsområdet **Funksjonsbehandling**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Konfigurer standardregler for fakturakontoen

Følg denne fremgangsmåten for å konfigurere standardreglene for fakturakontoen.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Parametere for prosjektstyring og regnskap**.
1. På **Generelt**-fanen i delen **Salgsordrer og varekrav** setter du alternativet **Tillat prosjekter med flere finansieringskilder** til **Ja**.
1. I feltet **Standardkunde** angir du hvor kunden for prosjektlevering i varekravet kommer fra som standard:

    - **Fra finansieringskilde** – Standardkunden for prosjektlevering kommer fra finansieringskilden. Hvis flere finansieringskilder er knyttet til prosjektkontrakten, brukes den første finansieringskilden i listen.
    - **Fra prosjekt** – Standardkunden for prosjektlevering kommer fra kunden som er valgt i feltet **Konto for prosjektoppføring**.

1. Valgfritt: Angi eller endre standard fakturakonto i prosjektoppføringer:

    1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**, og åpne prosjektoppføringsdetaljene.
    2. På **Generelt**-fanen angir eller oppdaterer du feltet **Standard fakturakonto**. Kontoen du angir, blir brukt som standard fakturakonto for nye varekrav som opprettes for prosjektet. Hvis du lar feltet stå tomt, brukes fakturakontoen for den første finansieringskilden til prosjektkontrakten som standard. Brukere kan imidlertid endre kontoen når de lagrer oppføringen.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Velg fakturakontoen som skal brukes når du oppretter et varekrav

Følg trinnene nedenfor for å velge fakturakontoen som skal brukes når du oppretter et varekrav.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**, og velg prosjektoppføringen.
1. På **Plan**-fanen velger du **Varekrav**.
1. Opprett en ny varekravoppføring.

    - Som standard er **Fakturakonto**-feltet i oppføringen angitt til fakturakontoen som er angitt for prosjektet. Du kan endre verdien i **Fakturakonto**-feltet og deretter lagre oppføringen. Når oppføringen er lagret, kan du ikke lenger oppdatere **Fakturakonto**-verdien. Hvis du må oppdatere **Fakturakonto**-verdien for varekravet, sletter du det eksisterende varekravet, og deretter oppretter du et nytt som har den ønskede verdien.
    - Som standard angis **Kunde**-feltet for varekravet basert på verdien for **Standardkunde** som er angitt på siden **Parametere for prosjektstyring og regnskap**.

    Når varekravoppføringen lagres, knyttes den til hodeoppføringen **Salgsordre for varekrav**. Hvis ingen åpne salgsordrehoder har den valgte fakturakontoen, oppretter systemet en og knytter varekravlinjen til den.

> [!NOTE]
> Varekrav blir alltid fullstendig fakturert til fakturakontoen som er angitt i oppføringen. Systemet støtter for øyeblikket ikke regler for finansieringstildeling som har varekrav, og det deler ikke posteringene basert på oppsettet av regler for finansieringstildeling.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Opprett et varekrav fra en vareprognoseoppføring

Følg trinnene nedenfor for å opprett et varekrav fra en vareprognoseoppføring.

1. Gå til **Prosjektstyring og regnskap** \> **Prosjekter** \> **Alle prosjekter**, og velg prosjektoppføringen.
1. På **Plan**-fanen velger du **Vareprognoser**.
1. Opprett en ny vareprognoseoppføring.
1. Valgfritt: På **Prosjekt**-fanen, i **Finansieringskilde**-feltet, velger du den ønskede fakturakontoen.
1. Velg **Opprett varekrav**, og bekreft meldingen du mottar.

    > [!NOTE]
    > Systemet kopierer **Finansieringskilde**-verdien fra vareprognoseoppføringen til den nylig opprettede varekravoppføringen.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Standard fakturakonto når systemet automatisk oppretter et varekrav fra en bestillingslinje

Hvis alternativet **Opprett varekrav** er satt til **Ja** på siden **Parametere for prosjektstyring og regnskap**, oppretter systemet automatisk et varekrav når en ny prosjektbestillingslinje lagres. Som standard er feltene **Fakturakonto** og **Varekrav** angitt til verdien i feltet **Standard fakturakonto** i prosjektoppføringen. Systemet støtter for øyeblikket ikke oppdatering eller endring av fakturakontoen for oppføringer av denne typen.
