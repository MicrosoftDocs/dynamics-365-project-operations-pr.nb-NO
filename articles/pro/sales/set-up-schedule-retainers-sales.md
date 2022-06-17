---
title: Konfigurer en honorarplan
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer en honorarplan i Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 077961d2f649754149315438252970609c246555
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927754"
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