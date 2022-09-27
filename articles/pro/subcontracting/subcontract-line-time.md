---
title: Underkontraktlinjer for tid
description: Denne artikkelen forklarer hvordan du registrerer underkontraktlinjer for tid og registrerer kjøp av tid fra leverandører.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522245"
---
# <a name="subcontract-lines-for-time"></a>Underkontraktlinjer for tid

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

En underkontrakt i Dynamics 365 Project Operations kan ha en underleverandørlinje for tid. Ved hjelp av underkontraktlinjer for tid kan en prosjektleder kjøpe leverandørressurstid for å bemanne prosjektoppgaver og ressurskrav.

Hvis du vil opprette en underkontraktlinje for tid i Project Operations, følger du fremgangsmåten nedenfor.

1. Velg **Underkontrakter** i navigasjonsruten, og åpne en underkontrakt.
2. Velg **Ny** i fanen **Underkontraktlinjer** for å opprette en ny underkontraktlinje.
3. Velg **Klokkeslett** i feltet **Transaksjonsklasse**-feltet på siden **Hurtigoppretting**.
4. Angi resten feltinformasjonen, og velg deretter **Lagre**.

  Tabellen nedenfor inneholder informasjon om feltene på siden **Underkontraktlinje** og **Hurtigoppretting**.

| **Felt** | **Beskrivelse** | **Funksjonsinnvirkning** |
| --- | --- | --- |
| Navn | Navn på underkontraktlinjen for å hjelpe med identifisering. | Dette vises som den første kolonnen i alle oppslag basert på underkontraktlinjer. |
| Beskrivelse | En kort beskrivelse av tjenester som blir kjøpt på underkontraktlinjen. |Ingen |
| Linjetype |   Dette feltet har en standardverdi på **antallsbasert**.| Ingen |
| Faktureringsmetode | Dette er en alternativsett som representerer de to hovedkontraktsmodellene som støttes av Project Operations: **Fast pris** og **Tid og materiell**. | Basert på faktureringsmetoden som er valgt, gjøres en milepælbasert fakturaplan tilgjengelig for underkontraktslinjer med faktureringsmetoden Fast pris. |
| Transaksjonsklasse | Standardverdien er **Tid**. | Dette angir at underkontraktlinjen brukes til å registrere et kjøp av underleverandørtid. |
| Rolle | Velg rollen til underkontraktsressursene som det blir kjøpt tid for. | Rollen som utføres av underkontraktsressursene, bestemmer innkjøpskostnaden. |
| Ønsket start | Angi datoen da underleverandørressursene kreves for å begynne å arbeide. | Denne brukes til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for rollen på underkontraktslinjen kommer fra den prislisten. |
| Ønsket slutt | Angi datoen da tilordningen av underleverandørressursen slutter. | Denne brukes til å vise advarsler når en prosjektleder trekker fra kapasiteten for ressurskrav som inntreffe etter denne datoen. |
| Antall bestilt | Angi antall timer for rollen som kjøpes fra leverandøren. | Denne brukes til å vise advarsler når en prosjektleder overtrekker fra kapasiteten for ressurskrav som inntreffe. |
| Enhetsgruppe | Standardverdien er **Tidsenhetsgruppe**, som ikke kan endres. | Ingen|
| Enhet | Standarden for dette feltet er basisenheten for timer fra **Tidsenhetsgruppe**. Du kan endre denne verdien for å kjøpe en hvilken som helst enhet i **tidsenhetsgruppen**, for eksempel dag eller uke. | Kombinasjonen av **Rolle** og **Enhet** brukes som standard eller beregnet for enhetsprisen for underkontraktslinjen. |
| Enhetspris | Standard enhetspris bruker kombinasjonen av **Rolle** og **Enhet** fra prosjektprislisten som gjelder for **ønsket startdato** for underkontraktslinjen. | Når den aktuelle prosjektprislisten har satt opp prisen i en annen enhet enn enheten på underkontraktlinjen, bruker systemet enhetskonverteringen til å beregne enhetsprisen. |
| Delsum |    Dette er et skrivebeskyttet felt som beregnes som Antall x Enhetspris hvis det angis både antall- og enhetsprisverdier. Hvis antall, enhetspris eller begge deler er tomme, kan du angi en verdi i feltet. | Ingen|
| Merverdiavgift |   Angi mva-beløpet. |Ingen |
| Totalbeløp | Totalbeløpet for underkontraktlinjen inkludert avgifter. Dette feltet beregnes som delsum + merverdiavgift.|Ingen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
