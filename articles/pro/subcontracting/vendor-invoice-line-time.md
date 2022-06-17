---
title: Leverandørfakturalinjer for tid
description: Denne artikkelen forklarer hvordan du registrerer leverandørfakturalinjer for tidskostnader som underleverandører har lagt inn.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0b81d2884580e9054457906627c1f9101f435524
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927559"
---
# <a name="vendor-invoice-lines-for-time"></a>Leverandørfakturalinjer for tid

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En leverandørfaktura i Microsoft Dynamics 365 Project Operations kan ha leverandørfakturalinjer for tid. Prosjektledere kan bruke leverandørfakturalinjer til å registrere kostnadene for underleverandørtid på prosjekter.

Det kan hende at leverandørfakturalinjer for klokkeslett refererer til en underleverandørlinje for tid. Hvis en leverandørfakturalinje for tid refererer til en underleverandør, kan prosjektledere samsvare og kontrollere klokkeslettet som faktureres av leverandørfakturalinjen, i forhold til tidspunkt som er registrert av underleverandører og godkjent av prosjektledere på prosjektet.

Tabellen nedenfor inneholder informasjon om feltene på leverandørfakturalinjer for tid.

| Felt | Bekrivelse | Funksjonsinnvirkning |
| --- | --- | --- |
| Name | Navnet på leverandørfakturalinjen, for å hjelpe med identifisering. | Dette navnet vises som den første kolonnen i alle oppslag som er basert på leverandørfakturalinjer. |
| Bekrivelse | En kort beskrivelse av servicene som faktureres av leverandøren på leverandørfakturalinjen. | None |
| Underkontrakt | Underkontrakten som tjenestene opprinnelig ble bestilt på. | Når en underkontrakt er valgt for leverandørfakturaen, arver alle linjene på leverandørfakturaen dette valget. En leverandørfaktura kan ikke ha leverandørfakturalinjer som refererer til ulike underkontrakter. |
| Underkontraktlinje | Underkontraktlinjen som tjenestene ble bestilt på. Listen over underkontraktslinjer som kan velges, er begrenset til linjene på den valgte underkontrakten. | Når en underkontraktlinje er valgt på en leverandørfakturalinje for tid, angis standardverdier for feltene **Prosjekt**, **Rolle** og **Ressurs som kan reserveres**, fra de tilsvarende feltene på underkontraktlinjen. Hvis den valgte underkontraktlinjen har verdier i feltene **Prosjekt**, **Rolle** og **Kan reserveres**, kan ikke verdiene i de tilsvarende feltene på leverandørfakturalinjen avvike fra disse verdiene. |
| Transaksjonsdato | Datoen da faktiske kostnader for leverandørfakturalinjen registreres på prosjektet. | None |
| Transaksjonsklasse | Standardverdien er **Tid**. | Verdien **Tid** angir at leverandørfakturalinjen brukes til å registrere fakturabeløpet for underleverandørtiden. |
| Project | Navnet på prosjektet som tjenestene som blir fakturert, ble brukt på. | Dette feltet er obligatorisk og kan ikke være tomt. |
| Oppgave | Navnet på prosjektoppgaven som tjenestene som blir fakturert, ble brukt på. Dette feltet er bare tilgjengelig hvis et prosjekt er valgt. Valg av en prosjektoppgave er valgfritt. | Hvis dette feltet er tomt, kan prosjektlederen samsvare med leverandørfakturalinjen til en tid som registreres av underleverandørressurser for en hvilken som helst oppgave i prosjektet. Hvis fakturalinjen for leverandørfaktura ikke refererer til en underordnet linje, og dette feltet står tomt, blir ikke den faktiske kostnaden som opprettes av leverandørfakturalinjen, koblet til noen faktiske verdier for ikke-fakturert salg. Hvis oppgavebasert fakturering er konfigurert i dette tilfellet, kan det hende at kostnadene ikke kan faktureres til sluttkunden. |
| Rolle | Rollen til underkontraktsressursene som tiden blir fakturert for. | Dette feltet angir rollen som utføres av underkontraktsressursene, som har en fakturert tid på leverandørfakturaen. |
| Ressurs som kan reserveres | Navnet til underleverandøren som tiden blir fakturert for. Valg av en ressurs som kan reserveres, er valgfritt. | Hvis dette feltet er tomt, kan prosjektlederen samsvare med leverandørfakturalinjen til en tid som registreres av enhver ressurs som tilhører leverandøren på leverandørfakturalinjen. |
| Antall | Angi antallet timer som leverandøren faktureres for, på fakturalinjen. |None |
| Enhetsgruppe | Standardverdien er **Tidsenhetsgruppe**, og den kan ikke endres. | None |
| Enhet | Standardverdien er basisenheten for timer fra tidsenhetsgruppen. Du kan endre denne verdien for å kjøpe en hvilken som helst enhet i tidsenhetsgruppen, for eksempel dag eller uke. | Kombinasjonen av verdiene for **Rolle** og **Enhet** brukes som standard eller beregnet verdi for **Enhetspris**-feltet på leverandørfakturalinjen. |
| Enhetspris | Standard enhetspris bruker kombinasjonen av verdiene for **Rolle** og **Enhet** fra prosjektprislisten som gjelder for transaksjonsdatoen på leverandørfakturalinjen. | Hvis prisen for den aktuelle prosjektprislisten er angitt i en enhet som er forskjellig fra enheten på leverandørfakturalinjen, bruker systemet enhetskonverteringen til å beregne enhetsprisen. |
| Delsum | Dette skrivebeskyttede feltet beregnes som *Antall* &times; *Enhetspris* hvis verdier er angitt både i **Antall**-feltet og **Enhetspris**-feltet. Hvis ett av eller begge disse feltene er tomme, kan du angi en verdi i dette feltet. | None |
| Salgsavgift | Angi mva-beløpet. | None |
| Totalbeløp | Det totale beløpet for leverandørfakturalinjen, inkludert avgifter. Dette feltet beregnes som *Delsum* + *Merverdiavgift*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
