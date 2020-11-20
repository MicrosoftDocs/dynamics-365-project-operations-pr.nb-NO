---
title: Konfigurere en tidsplan for honorarer – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer en honorarplan i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181284"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Konfigurere en tidsplan for honorarer – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En honorarplan konfigureres på siden **Prosjektkontrakt** i Dynamics 365 Project Operations.

1. På siden **Prosjektkontrakt**, i kategorien **Forskudd og honorarer**, velger du **Konfigurere en tidsplan for honorarer**.
2. På dialogsiden som åpnes, vises feltene i følgende tabellen. Tabellen gir deg en idé om hvordan de angitte verdiene påvirker eller har innvirkning på honorartidsplanen som blir opprettet.

| Felt | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- |
| Prosjektkontraktkunde | Kunden på kontrakten som skal faktureres for dette honoraret eller forskuddet. | Hvis du har flere kunder i kontrakten og må fakturere hver av dem for et bestemt honorar eller forskudd, oppretter du én faktura for hver kunde manuelt. |
| Starten på honorarplan | Angi startdatoen for honorarplanen. | Denne datoen kan ikke være datoen da det første honoraret eller forskuddet ble opprettet. Datoen da det første honoraret eller forskuddet ble opprettet, påvirkes også av fakturafrekvensen. |
| Slutten av honorarplan | Angi sluttdatoen for honorarplanen. | Denne datoen kan ikke være datoen da det siste honoraret eller forskuddet ble opprettet. Datoen da det siste honoraret eller forskuddet ble opprettet, påvirkes også av fakturafrekvensen. |
| Antall honorarer som skal opprettes | Når du angir antall honorarer som skal opprettes, bruker systemet startdatoen og hyppigheten til å opprette nummeret i dette feltet. | Når dette feltet oppdateres manuelt, ignorerer systemet verdien i feltet **Slutten av honorarplan**, og i stedet opprettes det spesifikke antallet honorarer eller forskudd. |
| Fakturafrekvens | Hvor ofte programmet vil opprette honorarer og forskudd. | Denne verdien har direkte innvirkning på antall honorarer og forskudd og de opprettede datoene. |
| Totalbeløp | Totalbeløpet er beløpet som er delt inn i de individuelle honorar- og forskuddsbetalingene som blir opprettet. | Dette feltet har ingen nedstrøms påvirkning. |
