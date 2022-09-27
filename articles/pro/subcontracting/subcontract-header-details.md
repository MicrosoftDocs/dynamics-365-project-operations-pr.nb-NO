---
title: Hodedetaljer for underkontrakter
description: Denne artikkelen forklarer funksjonaliteten i underkontrakthodet i Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 00b7c08235654d4bed0bcb4053d2044a3d092b54
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522573"
---
# <a name="header-details-for-subcontracts"></a>Hodedetaljer for underkontrakter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Denne artikkelen forklarer funksjonaliteten i underkontrakthodet i Dynamics 365 Project Operations.

Siden prosjektledere planlegger og kjører prosjekter, kan de bruke underleverandører og kjøpe produkter og tjenester fra leverandører. Når en prosjektleder må kjøpe produkter eller tjenester, kan vedkommende opprette en underkontrakt i Project Operations.

Fullfør fremgangsmåten nedenfor for å opprette en underkontrakt.

1. Velg **Underkontrakter** i navigasjonsruten, og velg **Ny** på siden **Underkontrakt**.
2. Angi den nødvendige informasjonen, og klikk deretter **Lagre**.

    Tabellen nedenfor inneholder informasjon om feltene på siden **Underkontrakthode**.

    | Felt | Beskrivelse |Funksjonsinnvirkning |
    |---|------|---| 
    | Navn | Navnet på underkontrakten. | I alle rullegardinlister for underkontrakt vises navnet på underkontrakten i den første kolonnen for å hjelpe deg med å identifisere underkontrakten. | 
    | Beskrivelse | En kort beskrivelse av tjenester og produkter som blir kjøpt på underkontrakten. | Ingen |
    | Forhandler | Navnet på firmaet som produktene og tjenester blir kjøpt fra. Denne kontooppføringen har relasjonstypen **Leverandør** eller **Forsyner**. | Basert på leverandøren som er valgt, angis det automatisk standardverdier for følgende felter:<br/> **• Valuta** </br> **• Prislister** </br> **• Betalingsbetingelser**</br> **• Betalingsadresse**</br> **• Fakturaadresse**</br> **• Fakturanavn** </br>**• Leverandørkontoansvarlig**|
    | Underkontraktdato | Datoen da underkontrakten ble opprettet. | Underkontraktsdatoen brukes til å velge riktig innkjøpsprisliste fra prislistene som er knyttet til den relaterte leverandøren eller fra prosjektparameterne. |
    | Statusårsak | Statusen for underkontrakten. | Statusen avgjør hvor underkontrakten er i forretningsprosessen, og om den kan redigeres. <br/>Verdier inkluderer:<br>• **Utkast**: Underkontrakten kan redigeres. Du kan bare redigere underkontrakter med statusen **Utkast**.<br/>• **Bekreftet**: Forhandlingen med leverandøren er fullført, og underkontrakten er godkjent for levering. <br/>• **Lukket**: Leveringen på underkontrakten er fullført.<br/>• **Annullert**: Underkontrakten ble annullert, og ingen levering er planlagt.  | 
    | Valuta | Valutaen som produkter og tjeneste kjøpes i. Standardverdien angis automatisk fra leverandørkontoen, men den kan endres. | Valutaen til underkontrakten brukes til å velge innkjøpsprisliste fra prislistene som er knyttet til den relaterte leverandøren eller fra prosjektparameterne. Prislister i en annen valuta kan ikke tilknyttes underkontrakten. Kostnadene for tid, utgifter og materiell som leverandørressursene leverer fra denne underkontrakten, registreres i denne valutaen på prosjektet. Når underkontraktsoppføringen er lagret, kan ikke valutaen for underkontrakten endres.|
    | Kontraktsenhet | Divisjonen i firmaet som inngår en innkjøpskontrakt eller en underkontrakt med leverandøren. | Ingen |
    | Betalingsbetingelser | Betalingsbetingelsene på leverandørfakturaer som er utstedt på denne underkontrakten. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Betalingsbetingelser fra underkontrakten kopieres til alle leverandørfakturaer som er relatert til denne underkontrakten. Betalingsbetingelser kan oppdateres hvis underkontrakten har statusen **Utkast**. | 
    | Betalingsadresse | Adressen til leverandøren som betalinger må sendes til. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Betalingsadressen fra underkontrakten kopieres som betalingsadressen til alle leverandørfakturaer som er opprettet for denne underkontrakten. Betalingsadressen kan oppdateres hvis underkontrakten har statusen **Utkast**.|
    | Fakturanavn | Navnet på personen eller divisjonen i leverandørens firma som skal sende fakturaen. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Verdien **Fakturanavn** fra underkontrakten kopieres til alle leverandørfakturaer som er relatert til denne underkontrakten. Dette feltet kan oppdateres hvis underkontrakten har statusen **Utkast**.|
    | Fakturaadresse | Adressen som brukes på fakturaer fra leverandøren. Standardverdien angis automatisk fra oppføring for leverandørkontoen. | Denne adressen er faktura fra-adressen på leverandørfakturaer som er opprettet for denne underkontrakten. |
    | Delsum | Hvis en underkontrakt ikke har noen linjer, angir du delsummen for ordren før avgifter. Hvis underkontrakten har linjer, er dette feltet skrivebeskyttet. Beløpet som vises, er delsumbeløpet fra alle linjene i underkontrakten. | Ingen |
    | Avgifter totalt | Hvis en underkontrakt ikke har noen linjer, angir avgifter totalt på denne underkontrakten. Hvis underkontrakten har linjer, er dette feltet skrivebeskyttet. Beløpet som vises, er summen av avgiftsbeløpet fra alle linjene i underkontrakten. | Ingen |
    | Totalbeløp | Dette beregnede feltet viser totalbeløpet for underkontraktlinjen etter at avgifter er inkludert. | Ingen |
    | Dato bekreftet | Datoen da underkontrakten ble bekreftet. | Ingen |
    | Forespurt av | Som standard er dette feltet satt til navnet på brukeren som oppretter underkontrakten. Den som opprettet underkontrakten, kan imidlertid endre verdien for å angi personen som vedkommende oppretter underkontrakten på vegne av. | Ingen |
    | Leverandørkontoansvarlig | Navnet på hovedkontakten for leverandørkontoen. Standardverdien angis automatisk fra oppføring for leverandørkontoen. Du kan velge en annen kontakt som leverandørkontoleder for underkontrakten. | Du kan konfigurere e-postvarsler for å varsle kontakten når det gjøres endringer i underkontrakten som et resultat av prisforhandlinger. |
