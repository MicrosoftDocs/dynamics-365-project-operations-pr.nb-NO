---
title: Konfigurer en honorarplan
description: Dette emnet gir informasjon om hvordan du konfigurerer en honorarplan i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596384"
---
# <a name="set-up-a-retainer-schedule"></a>Konfigurer en honorarplan

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Honorarplaner konfigureres på **Prosjektkontrakt**-siden i Dynamics 365 Project Operations.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]