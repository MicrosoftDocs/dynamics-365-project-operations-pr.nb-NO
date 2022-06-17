---
title: Produktprislister
description: Denne artikkelen inneholder informasjon om prislistene i katalogprising som brukes for prosjekttilbud og kontrakter.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917634"
---
# <a name="product-price-lists"></a>Produktprislister

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

 I Project Operations støtter **Produktprislister** og relaterte prislisteelementenheter funksjonalitet for prising av produkter på produktbaserte tilbuds- og kontraktlinjer. For produkter som brukes i prosjekter, brukes prislisteelementoppføringene for prosjektprislister. 

Produkter bør settes opp slik at de har standard kostnads- og prislister i produkt katalogen. Bruk listeprisen, standardkostnaden og gjeldende kostnad for å konfigurere standard kostnader og listepriser. Standard listeprisene brukes på en tilbudslinje eller en prosjektkontraktlinje når systemet ikke finner en prislistelinje for produktet i produktprislisten for tilbudet eller prosjektkontrakten.

Kostprisen for produktkataloglinjer kan endres mellom tilbud. Denne funksjonen er viktig fordi hvis du ikke kan spore kostnader nøyaktig, kan du ikke fastsette driftsfortjeneste på prosjektforhandlinger. Som standard er standardkostnaden for produktet brukt som kostprisen. Standard kostpris kan imidlertid oppdateres i tilbudslinjen hvis det er en annen kostnadspris for det aktuelle tilbudet.

## <a name="price-list-items"></a>Prislisteelementer

Du kan legge til produkter fra en produktkatalog i forskjellige prislister. Prislistelinjer for produkter refererer alltid til en bestemt enhet. Priser for et produkt i prislisteelementer kan konfigureres som et valutabeløp. De kan også konfigureres som en funksjon av listepris, løpende kostnad eller standardkostnad.

Prisingsfunksjonalitet støtter ulike avrundingsalternativer når produktpriser konfigureres som en funksjon av listepris, standardkostnad eller løpende kostnad. I tillegg til å dra nytte av flere prisingsmetoder og avrundingsalternativer kan du knytte rabattlister til prislisteelementer. 

 
## <a name="default-product-price-list"></a>Standard produktprisliste
Hver kundeoppføring har et **Standard prisliste**-felt der du kan angi en prisliste som samsvarer med kundens valuta. Det blir ikke automatisk lagt inn en standardverdi i dette feltet. Når en egendefinert prisavtale med en bestemt kunde finnes, kan du bruke dette feltet til å knytte en prisliste til den aktuelle kunden.

Enhetene Salgsmulighet, Tilbud og Prosjektkontrakt bruker følgende rekkefølge til å angi standard prislister for produkter. Den samme rekkefølgen brukes for prosjektprislister.

1.  Tilbud
2.  Salgsmulighet
3.  Kunde
4.  Globale innstillinger 

**Produkt**-feltet på tilbudslinjen viser som standard alle de aktive produktene i produktprislisten for tilbudet. Hvis et produkt er deaktivert, eller det er et utkastprodukt, vises det ikke, selv om det er i prislisten. 

Produktkataloglinjer legges til som fakturalinjer på den første fakturaen som opprettes for en prosjektkontrakt. Disse fakturalinjene kan slettes på et fakturautkast. I slike tilfeller vil linjene vises på en etterfølgende faktura til de faktureres eller til fakturaen sendes til kunden. Du kan ikke fakturere et delvist antall av en produktfakturalinje. Når produktlinjene fra prosjektkontrakten faktureres, opprettes faktiske verdier. De faktiske verdiene blir imidlertid ikke koblet til den relaterte prosjektenheten. Med andre ord er produktbaserte prosjektkontraktlinjer uavhengige av prosjektbasert forbruk. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
