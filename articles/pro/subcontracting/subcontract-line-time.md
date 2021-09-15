---
title: Underkontraktlinjer for tid
description: Dette emnet forklarer hvordan du registrerer underkontraktlinjer for tid og registrerer kjøp av tid fra leverandører.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323878"
---
# <a name="subcontract-lines-for-time"></a>Underkontraktlinjer for tid

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En underkontrakt i Dynamics 365 Project Operations kan ha en underleverandørlinje for tid. Ved hjelp av underkontraktlinjer for tid kan en prosjektleder kjøpe leverandørressurstid for å bemanne prosjektoppgaver og ressurskrav.

Hvis du vil opprette en underkontraktlinje for tid i Project Operations, følger du fremgangsmåten nedenfor.

1. Velg **Underkontrakter** i navigasjonsruten, og åpne en underkontrakt.
2. Velg **Ny** i fanen **Underkontraktlinjer** for å opprette en ny underkontraktlinje.
3. Velg **Klokkeslett** i feltet **Transaksjonsklasse**-feltet på siden **Hurtigoppretting**.
4. Angi resten feltinformasjonen, og velg deretter **Lagre**.

  Tabellen nedenfor inneholder informasjon om feltene på siden **Underkontraktlinje** og **Hurtigoppretting**.

| **Felt** | **Beskrivelse** |
| --- | --- |
| Navn | Navnet på underkontraktlinjen. |
| Beskrivelse | En kort beskrivelse av tjenester som blir kjøpt på underkontraktlinjen. | 
| Linjetype | Dette feltet er en standardverdi.  |
| Faktureringsmetode | Velg faktureringsmetoden. Basert på faktureringsmetoden til den refererte underkontraktlinjen, gjøres en milepælbasert fakturaplan tilgjengelig for faktureringsmetoden med fast pris. |
| Transaksjonsklasse | Dette feltet er en standardverdi som angir om underkontraktlinjen brukes til å registrere et kjøp av underleverandørtid. |
| Rolle | Rollen til underkontraktressursene som det blir kjøpt tid av. Rollen som er tilordnet underkontraktressursene, bestemmer innkjøpskostnaden. |
| Ønsket start | Datoen når underleverandørressursene skal begynne å arbeide. Ønsket start brukes også til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for rollen på underkontraktlinjen brukes deretter som standard fra den prislisten. |
| Ønsket slutt | Datoen når oppgaven til underleverandøren slutter. Denne datoen brukes til å vise advarsler når en prosjektleder trekker fra denne kapasiteten for ressurskrav som inntreffe etter denne datoen. |
| Antall bestilt | Antall rolletimer som blir kjøpt fra leverandøren. Denne verdien brukes til å vise advarsler når en prosjektleder overtrekker fra denne kapasiteten for ressurskrav. |
| Enhetsgruppe | Denne feltverdien er standard for tidsenhetsgruppen og kan ikke endres.  |
| Enhet | Dette feltet brukes som standard basisenhet for timer fra tidsenhetsgruppen. Du kan endre denne verdien for å kjøpe en hvilken som helst enhet i tidsenhetsgruppen, for eksempel dag eller uke. Kombinasjonen av Rolle og Enhet brukes til å beregne enhetsprisen for underkontraktlinjen. |
| Enhetspris | Enhetsprisen er standard fra kombinasjonen av Rolle og Enhet fra prosjektprislisten som gjelder for ønsket startdato for underkontraktlinjen. Når den aktuelle prosjektprislisten har satt opp prisen i en annen enhet enn enheten på underkontraktlinjen, bruker systemet enhetskonverteringen til å beregne enhetsprisen. |
| Delsum | Dette er et skrivebeskyttet felt som automatisk beregnes som **Antall x Enhetspris** hvis både antalls- og enhetsprisverdiene angis. Hvis antall, enhetspris eller begge deler er tomme, kan du angi en verdi i feltet. |
| Merverdiavgift |  Angi mva-beløpet. |
| Totalbeløp | Totalbeløpet for underkontraktlinjen etter at avgifter er inkludert. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
