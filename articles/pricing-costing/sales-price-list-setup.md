---
title: Sette opp salgsprisliste
description: Dette emnet gir information om salgsprislister for prosjektpriser.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896473"
---
# <a name="sales-price-list-setup"></a>Sette opp salgsprisliste

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

For prosjekttilbud og kontrakter har en prosjektprisliste et annet prisoverstyringsmønster enn en produktprisliste. På en produktkatalogbasert tilbudslinje kan du overstyre prisen for roller og kategorier direkte på tilbudslinjen, fordi hver tilbudslinje peker på nøyaktig ett katalogelement. På en prosjektbasert tilbudslinjen kan du imidlertid ikke overstyre prisen til roller og kategorier direkte på tilbudslinjen. Du kan bruke prosjektprislisten til å arbeide med de to spesifikke overstyringsmønstrene.

> [!NOTE]
> Vi anbefaler at du har en egen prisliste for prosjektressursene og katalogelementene på grunn av virkemåteforskjellene mellom de to når du overstyrer prisen.

Hver av de følgende enhetene kan ha én eller flere tilknyttede salgsprislister for prosjektprising:

- Kunde (forretningsforbindelse) 
- Salgsmulighet 
- Tilbud 
- Prosjektkontrakt

Tilknytningen til disse enhetene og en prisliste angis av prosjektprislistene. Du kan knytte én eller flere prislister til salgsenhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt.

Det registreres ikke automatisk en standard prosjektprisliste i en kundeoppføring. Du kan imidlertid legge ved en prosjektprisliste manuelt i kundeoppføringen. Likevel bør du likevel legge ved en prosjekt prisliste manuelt bare når du har en egen definert prisingsavtale med kunden. 

Når en prosjektprisliste er knyttet til en salgsenhet, valideres følgende informasjon:

- Prislisten som en kontekst for **Salg**. 
- Valutaen i prislisten samsvarer med kundevalutaen. 

I en prosjektkontrakt brukes følgende prioritetsrekkefølge til automatisk å angi relaterte prosjektprislister:

1. Tilbud
2. Salgsmulighet
3. Kunde 
4. Globale innstillinger 

Når en prosjektprisliste er angitt som standard, validerer systemet at valutaen samsvarer med kundens valuta, og at standardprislistene som er lagt inn, har en kontekst for **Salg**.

Du kan knytte flere prosjektprislister til enhetene Kunde, Salgsmulighet, Tilbud og Prosjektkontrakt. Denne funksjonen støtter datospesifikke standardpriser for en langvarig prosjektkontrakt, der du kan trenge mer enn én prisliste for å ta hensyn til prisoppdateringer som inntreffer på grunn av inflasjonen. Hvis prislistene som du knytter til enheten Kunde, Salgsmulighet, Tilbud eller Prosjektkontrakt, for eksempel har overlappende datogyldighet, kan standard prisene være feil. Derfor bør du sørge for at prosjektprislister som har overlappende datogyldighet, ikke er tilknyttet disse enhetene.
