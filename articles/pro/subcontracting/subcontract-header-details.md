---
title: Overskriftsdetaljer for underkontrakter
description: Dettet emne forklarer funksjonaliteten i underkontrakthodet i Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323653"
---
# <a name="header-details-for-subcontracts"></a>Overskriftsdetaljer for underkontrakter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Dettet emne forklarer funksjonaliteten i underkontrakthodet i Dynamics 365 Project Operations.

Siden prosjektledere planlegger og kjører prosjekter, kan de bruke underleverandører og kjøpe produkter og tjenester fra leverandører. Når en prosjektleder må kjøpe produkter eller tjenester, kan vedkommende opprette en underkontrakt i Project Operations.

Fullfør fremgangsmåten nedenfor for å opprette en underkontrakt.

1. Velg **Underkontrakter** i navigasjonsruten, og velg **Ny** på siden **Underkontrakt**.
2. Angi den nødvendige informasjonen, og klikk deretter **Lagre**.

    Tabellen nedenfor inneholder informasjon om feltene på siden Underkontraktoverskrift.

    | **Felt** | **Beskrivelse** |
    | --- | --- | 
    | Navn | Navnet på underkontrakten. |
    | Beskrivelse | En kort beskrivelse av tjenester og produkter som blir kjøpt på underkontrakten. |
    | Forhandler | Navnet på firmaet som produktene og tjenester blir kjøpt fra. Denne kontooppføringen har relasjonstypen **Leverandør** eller **Forsyner**. |
    | Underkontraktdato | Datoen da underkontrakten ble opprettet. |
    | Statusårsak | Statusen for underkontrakten. |
    | Valuta | Valutaen som produkter og tjenester kjøpes i. Verdien i dette feltet kommer som standard fra leverandørkontoen, men kan endres. Prosjektprislister som brukes til å prise produkter og tjenester på underkontrakten, må være i denne valutaen. Prislister i andre valutaer kan ikke tilknyttes underkontrakten. Kostnaden for produkter og tjenester som påløper for denne underkontrakten, registreres på prosjektet i denne valutaen. |
    | Kontraktsenhet | Divisjonen i firmaet som inngår en innkjøpskontrakt eller en underkontrakt med leverandøren. |
    | Betalingsbetingelser | Betalingsbetingelsene for leverandørfakturaene som er utstedt på denne underkontrakten. Verdien i dette feltet kommer som standard fra leverandørkontooppføringen. |
    | Betalingsadresse | Adressen der betaling på leverandørfakturaer sendes. Verdien i dette feltet kommer som standard fra leverandørkontooppføringen. |
    | Fakturanavn | Navnet på personen eller divisjonen i leverandørens firma som skal sende fakturaen. Verdien i dette feltet kommer som standard fra oppføringen for leverandørkontoen, og blir brukt som navnet på hovedkontakten på leverandørfakturaer som er opprettet for denne underkontrakten. |
    | Fakturaadresse | Adressen som brukes på fakturaer fra denne leverandøren. Verdien i dette feltet kommer som standard fra leverandørkontooppføringen. Denne adressen brukes også som faktura fra adresse på leverandørfakturaer som er opprettet for denne underkontrakten. |
    | Delsum | Hvis en underkontrakt ikke har noen linjer, angir du en verdi i dette feltet som angir delsummen for ordren før avgifter. Hvis underkontrakten har linjer, er dette feltet skrivebeskyttet. Beløpet som vises, er delsumbeløpet fra alle linjene i underkontrakten. |
    | Avgifter totalt | Hvis en underkontrakt ikke har noen linjer, angir du en verdi i dette feltet som angir avgiftene på denne underkontrakten. Hvis underkontrakten har linjer, er dette feltet skrivebeskyttet. Beløpet som vises, er summen av avgiftsbeløpet fra alle linjene i underkontrakten. |
    | Totalbeløp |  Dette beregnede feltet viser totalbeløpet for underkontraktlinjen etter at avgifter er inkludert.  |
    | Dato bekreftet | Datoen da underkontrakten ble bekreftet.  |
    | Forespurt av | Verdien i dette feltet bruker som standard navnet på brukeren som oppretter underkontrakten. Denne verdien kan endres av den som opprettet underkontrakten, for å angi denne personen på vegne av hvem vedkommende de oppretter underkontrakten for.  |
    | Leverandørkontoansvarlig | Navnet på hovedkontakten for leverandørkontoen. Verdien i dette feltet kommer som standard fra leverandørkontooppføringen. Denne feltverdien kan endres av brukeren for å velge en annen kontakt som leverandørkontoleder for underkontrakten. E-postvarsler og prisforhandlinger kan konfigureres og sendes av denne kontakten. |


