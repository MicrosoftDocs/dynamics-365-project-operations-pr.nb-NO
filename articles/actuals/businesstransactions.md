---
title: Forretningstransaksjoner i Project Operations
description: Dette emnet gir en oversikt over konseptet med forretningstransaksjoner i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: 0c6fe583af0dcaa62204b35c1093746b13b6e00e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8582216"
---
# <a name="business-transactions-in-project-operations"></a>Forretningstransaksjoner i Project Operations

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Microsoft Dynamics 365 Project Operations er *forretningstransaksjon* et abstrakt konsept som ikke representeres av en enhet. Noen felles felt og prosesser på enheter er imidlertid utformet for å bruke konseptet forretnings transaksjoner. Følgende enheter bruker denne abstraksjonen:

- Tilbudslinjedetaljer
- Kontraktlinjedetaljer
- Estimatlinjer
- Journallinjer
- Faktisk

Av disse entitetene tilordnes tilbudslinjedetaljer, kontraktlinjedetaljer og estimatlinjer til *beregningsfasen* i prosjektets livssyklus. Enhetene Journallinjer og Faktiske enheter tilordnes til *utførelsesfasen* i prosjektets livssyklus.

Project Operations behandler oppføringer i alle disse fem enhetene som forretningstransaksjoner. Den eneste forskjellen er at oppføringer i enhetene som er tilordnet til beregningsfasen (tilbudslinjedetaljer, kontraktlinjedetaljer og estimatlinjer), betraktes som *finansielle prognoser*, mens oppføringer i enhetene som er tilordnet til utførelsesfasen (journallinjer og faktiske verdier), betraktes som *økonomiske fakta* som allerede har inntruffet.

Hvis du vil ha mer informasjon, se [Estimater](../project-management/estimating-projects-overview.md) og [Faktiske verdier](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Konsepter som er unike for forretningstransaksjoner

Følgende konsepter er unike for forretningstransaksjoner:

- Transaksjonstype
- Transaksjonsklasse
- Transaksjonsopprinnelse
- Transaksjonstilkobling

### <a name="transaction-type"></a>Transaksjonstype

Transaksjonstype representerer tidsberegningen og konteksten for den finansielle innvirkningen på et prosjekt. Den defineres av et alternativsett som har følgende støttede verdier i Project Operations:

- Kostnad
- Prosjektkontrakt
- Ufakturert salg
- Fakturert salg
- Salg mellom organisasjoner
- Kostnad for ressursenhet

### <a name="transaction-class"></a>Transaksjonsklasse

Transaksjonsklasse representerer de forskjellige kostnadstypene som er påløpt for prosjekter. Den defineres av et alternativsett som har følgende støttede verdier i Project Operations:

- Tid
- Utgift
- Materiale
- Gebyr
- Milepæl
- Avgift

> [!NOTE]
> **Milepæl**-verdien brukes vanligvis av forretningslogikken for fakturering med fast pris i Project Operations.

### <a name="transaction-origin"></a>Transaksjonsopprinnelse

Transaksjonsopprinnelse er en enhet som lagrer opprinnelsen for hver forretningstransaksjon for å bidra til rapportering og sporbarhet. Etter hvert som prosjektkjøringen begynner, oppretter hver forretningstransaksjon en annen forretningstransaksjon som i sin tur vil opprette en ny forretningstransaksjon og så videre.

### <a name="transaction-connection"></a>Transaksjonstilkobling

Transaksjonstilkobling er en enhet som lagrer relasjonen mellom to lignende forretningstransaksjoner, for eksempel kostnader og relaterte faktiske verdier for salg, eller transaksjonsannulleringer som utløses av faktureringsaktiviteter, for eksempel fakturabekreftelse eller fakturakorreksjoner.

Sammen hjelper transaksjonsopprinnelsen og transaksjonstilkoblingen deg med å spore relasjoner mellom forretningstransaksjoner og handlinger som gjorde det mulig å opprette en bestemt forretningstransaksjon.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
