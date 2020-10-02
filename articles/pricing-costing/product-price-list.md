---
title: Produktprislister
description: Dette emnet gir informasjon om prislistene i katalogprising som brukes for prosjekttilbud og kontrakter.
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
ms.openlocfilehash: 3570aeb78804e9b267caa55a27e02d6c8df9a5c6
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898183"
---
# <a name="product-price-lists"></a>Produktprislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prislister og prislisteelementer støtter produktkatalogprising. Denne funksjonaliteten brukes for det meste av katalogbaserte linjer i prosjekttilbud og prosjektkontrakter.

For prosjektbaserte linjer representerer en kontrakt avtalen etter at den ble vunnet. Fordi forhandlingen vanligvis kommer før kontrakten er vunnet, kopieres prisene som er knyttet til tilbudet, alltid til en ny prisliste og knyttes til kontrakten. Den nye prislisten kan ikke endres utenfor kontraktsområdet. Denne begrensningen bidrar til å beskytte rangeringskortet som ble forhandlet ut fra alle prisendringer som forekommer i hovedprislisten.

Produkter bør settes opp slik at de har standard kostnads- og prislister i produkt katalogen. Bruk listeprisen, standardkostnaden og gjeldende kostnad for å konfigurere standard kostnader og listepriser. Standard listeprisene brukes på en tilbudslinje eller en prosjektkontraktlinje når systemet ikke finner en prislistelinje for produktet i produktprislisten for tilbudet eller prosjektkontrakten.

Kostprisen for produktkataloglinjer kan endres mellom tilbud. Denne funksjonen er viktig fordi hvis du ikke kan spore kostnader nøyaktig, kan du ikke fastsette driftsfortjeneste på prosjektforhandlinger. Som standard er standardkostnaden for produktet brukt som kostprisen. Standard kostpris kan imidlertid oppdateres i tilbudslinjen hvis det er en annen kostnadspris for det aktuelle tilbudet.

## <a name="price-list-items"></a>Prislisteelementer

Du kan legge til produkter fra en produktkatalog i forskjellige prislister. Prislistelinjer for produkter refererer alltid til en bestemt enhet. Priser for et produkt i prislisteelementer kan konfigureres som et valutabeløp. De kan også konfigureres som en funksjon av listepris, løpende kostnad eller standardkostnad.

PSA støtter ulike avrundingsalternativer når priser konfigureres som en funksjon av listepris, standardkostnad eller løpende kostnad. I tillegg til å dra nytte av flere prisingsmetoder og avrundingsalternativer kan du knytte rabattlister til prislisteelementer. 

Når du oppretter en ny egen definert prisliste for et tilbud ved **Opprett egendefinert prising** på siden **Prosjekttilbud**, lages det en kopi av prislisten, og **Enhet**-feltet i overskriften i den nye prislisten settes til **Salgsenhet**. Navnet på den nye prislisten føyes til med navnet på tilbudet og et tidsstempel. Du kan også bruke navnet på den nye prislisten og navnet på tilbudet i egendefinerte arbeidsflyter for å utløse ytterligere gjennomsyn og godkjenninger for tilbud som bruker et egendefinert pris.

 
## <a name="default-product-price-list"></a>Standard produktprisliste
Hver kundeoppføring har et **Standard prisliste**-felt der du kan angi en prisliste som samsvarer med kundens valuta. Det blir ikke automatisk lagt inn en standardverdi i dette feltet. Når en egendefinert prisavtale med en bestemt kunde finnes, kan du bruke dette feltet til å knytte en prisliste til den aktuelle kunden.

Enhetene Salgsmulighet, Tilbud og Prosjektkontrakt bruker følgende rekkefølge til å angi standard prislister for produkter. Den samme rekkefølgen brukes for prosjektprislister.

1.  Tilbud
2.  Salgsmulighet
3.  Kunde
4.  Globale innstillinger 

**Produkt**-feltet på tilbudslinjen viser som standard alle de aktive produktene i produktprislisten for tilbudet. Hvis et produkt er deaktivert, eller det er et utkastprodukt, vises det ikke, selv om det er i prislisten. 

Produktkataloglinjer legges til som fakturalinjer på den første fakturaen som opprettes for en prosjektkontrakt. Disse fakturalinjene kan slettes på et fakturautkast. I slike tilfeller vil linjene vises på en etterfølgende faktura til de faktureres eller til fakturaen sendes til kunden. Du kan ikke fakturere et delvist antall av en produktfakturalinje. Når produktlinjene fra prosjektkontrakten faktureres, opprettes faktiske verdier. De faktiske verdiene blir imidlertid ikke koblet til den relaterte prosjektenheten. Med andre ord er produktbaserte prosjektkontraktlinjer uavhengige av prosjektbasert forbruk. Materialforbruk spores ikke på prosjekter.
