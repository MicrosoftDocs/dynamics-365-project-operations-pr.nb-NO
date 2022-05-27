---
title: Utgiftsspesifisering
description: Dette emnet forklarer hvordan du spesifiserer utgifter ved hjelp av det nyskapte utgiftsarbeidsområdet.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574534"
---
# <a name="expense-itemization"></a>Utgiftsspesifisering

[!include [banner](../includes/banner.md)]

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Organisasjoner krever ofte at ansatte sørger for en detaljert oversikt over utgifter som påløper under reisen. Et hotell kan for eksempel inneholde flere spesifiserte linjer for rompris, avgifter, parkering og andre diverse utgifter som påløper hver dag i løpet av oppholdet. Eller en måltidsutgift kan kreve at du oppgir en mer nedbryting av frokost, lunsj eller middag. Uansett behov i organisasjonen kan hver utgiftskategori angis slik at den gjenspeiler underkategoriene eller linjeelementene som utgjør en utgift. Selv om spesifisering alltid har vært støttet i **Utgiftshåndtering**, gir arbeidsområdet for **Nyskapt utgift** mer effektiv spesifisering når funksjonen **Evne til å spesifisere regelmessige utgifter** er aktivert.  

## <a name="enable-quick-itemization"></a>Aktivere hurtigspesifisering 

Du kan bruke funksjonen **Evne til å spesifisere regelmessige utgifter** til raskt å spesifisere regelmessige utgifter samtidig som du unngår behovet for å oppgi dagsutgiftene hver gang for varigheten av oppholdet. Fullfør fremgangsmåten nedenfor for å aktivere hurtigspesifisering.

1. Gå til arbeidsområdet **Funksjonsbehandling**, og i listen over funksjoner finner og velger du **Nyskapte utgiftsrapporter**. 
2. Velg **Aktiver nå**. 
3. I funksjonslisten finner og velger du **Evne til å spesifisere regelmessige utgifter**.
4. Velg **Aktiver nå**. 

## <a name="itemization-grid"></a>Rutenett for spesifisering 

Hvis en utgiftskategori har underkategorier eller forskjellige komponenter som utgjør utgiftene, kan den spesifiseres. Hvis du vil angi en utgift, velger du utgiftslinjen i utgiftsrapporten og i ruten **Utgiftsdetaljer** velger du **Handlinger** > **Spesifiser**. Glidebryteren **Spesifisering** viser et rutenett med felt. Tabellen nedenfor viser et eksempel på hvert felt i rutenettet og hvordan feltet gjengis i utgiftsrapporten. 

|     Felt          |     Description                                                                                  |     Eksempel              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Underkategori    |     Listen over underkategorier konfigurert under utgiftskategoritypen **Hotell**.             |     Rompris daglig      |
|     Startdato     |     Datoen da utgiftselementet først ble pådratt.                                           |     13/09/2021           |
|     Dagspris     |     Beløpet som påløper for utgiftselementet.                                                    |     200                  |
|     Antall       |     Antall ganger utgiften gjentas i en sammenhengende periode.                       |     3                    |

![Spesifiser utgift.](media/Itemization%20screen%201.png)

Når du lagrer en spesifisering, vises en individuell spesifisert linje for antallet som er angitt i Spesifisering-rutenettet. Hver linje starter på datoen som er angitt i rutenettet.

![Spesifisert rapport.](media/Itemization%20screen%202.png)

