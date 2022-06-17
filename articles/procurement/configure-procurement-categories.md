---
title: Bruk innkjøpskategorier med prosjektbestillinger og ventende leverandørfakturaer
description: Denne artikkelen beskriver hvordan du konfigurerer innkjøpskategorier som kan brukes med prosjektbestillinger og ventende leverandørfakturaer.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927432"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Bruk innkjøpskategorier med prosjektbestillinger og ventende leverandørfakturaer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Innkjøpsansvarlige kan opprette og vedlikeholde kataloger for varene og tjenestene som kan brukes i prosjektbestillinger og ventende leverandørfakturaer. Med [innkjøpskataloger](/dynamics365/supply-chain/procurement/procurement-catalogs) kan du på en enkel måte kategorisere kjøp uten å måtte konfigurere og bruke en produktkatalog som er gitt ut. Hver innkjøpskategori kan tilordnes til en prosjektkategori for tids-, utgifts- eller varetransaksjoner. Når en ventende leverandørfaktura som bruker en innkjøpskategori, posteres, oppretter systemet faktiske tids-, utgifts- eller materialprosjektoppføringer, prosjekttransaksjoner og underfinansoppføringer.

## <a name="minimum-version-requirements"></a>Minimum versjonskrav

Følgende versjoner kreves for å bruke innkjøpskategorier med prosjektbestillinger for ikke-lagerførte/ressursbaserte scenarioer i Microsoft Dynamics 365 Project Operations:

- Project Operations Dataverse-løsningen, versjon 4.41.0.45 eller senere
- Versjon 10.0.26 eller senere av Finance and Operations-miljøet

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Kjør tilordninger med dobbel skriving for støtte for innkjøpskategorien

Kontroller at tilordningen for **Project Operations-eksportenheten msdyn\_projectvendorinvoicelines for leverandørfakturalinjen i integrasjonsprosjektet** bruker versjon 1.0.0.4 eller senere.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Aktiver funksjonsnøkkelen for innkjøpskategorier

Følg denne fremgangsmåten for å aktivere funksjonaliteten for bruk av innkjøpskategorier med prosjektbestillinger.

1. I Dynamics 365 Finance åpner du arbeidsområdet **Funksjonsbehandling**.
1. Finn funksjonen **Bruk innkjøpskategorier i Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer** i funksjonslisten, og velg deretter **Aktiver**.

> [!IMPORTANT]
> Som en forutsetning må du også aktivere funksjonen **Aktiver ventende leverandørfakturaer i Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Tilordne prosjektkategorier i Innkjøpskategorihierarki

Følg denne fremgangsmåten for å tilordne prosjektkategorier til innkjøpskategorier i **Innkjøpskategorihierarki**:

1. Gå til **Innkjøp og leverandører \> Innkjøpskategorier**.
1. Velg **Rediger kategorihierarki**.
1. Velg den ønskede kategorihierarkinoden, og gå deretter til fanen **Tilordne prosjektkategorier**, tilknytt noden med prosjektkategorien fra kategorien **Tid**, **Utgift** eller **Vareprosjekt** (det vil si kategorien **Standardtid** eller **Standardutgift**).
1. Velg **Lagre**.
1. Lukk siden.

> [!NOTE]
> Det er valgfritt å tilordne en innkjøpskategori til en prosjektkategori. Hvis en innkjøpskategori ikke er tilordnet, bruker systemet verdien som er angitt i **Vare**-feltet i delen **Standarder for prosjektkategori** på fanen **Project Operations på Dynamics 365 Customer Engagement** på siden **Parametere for prosjektstyring og regnskap**.
