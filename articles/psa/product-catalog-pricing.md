---
title: Prising i produktkatalog
description: Dette emnet inneholder informasjon om hvordan prising i produktkatalogen fungerer i Dynamics 365 Project Service Automation (PSA).
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 59e05a55d41573b96785a2f41a7d5d822f6b515fb55edddea5ef1862b7694a1b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000183"
---
# <a name="product-catalog-pricing"></a>Prising i produktkatalog 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Prislister og prislisteelementer støtter produktkatalogprising. Denne funksjonaliteten brukes for det meste av katalogbaserte linjer i prosjekttilbud og prosjektkontrakter.

For prosjektbaserte linjer representerer en kontrakt avtalen etter at den ble vunnet. Fordi forhandlingen vanligvis kommer før kontrakten er vunnet, kopieres prisene som er knyttet til tilbudet, alltid til en ny prisliste og knyttes til kontrakten. Den nye prislisten kan ikke endres utenfor kontraktsområdet. Denne begrensningen bidrar til å beskytte rangeringskortet som ble forhandlet ut fra alle prisendringer som forekommer i hovedprislisten.

Produkter bør settes opp slik at de har standard kostnads- og prislister i produkt katalogen. Du må bruke listeprisen, standardkostnaden og gjeldende kostnad for å konfigurere standard kostnader og listepriser. Standard listeprisene brukes på en tilbudslinje eller en prosjektkontraktlinje når systemet ikke finner en prislistelinje for produktet i produktprislisten for tilbudet eller prosjektkontrakten.

Kostprisen for produktkataloglinjer kan endres mellom tilbud. Denne funksjonen er viktig fordi hvis du ikke kan spore kostnader nøyaktig, kan du ikke fastsette driftsfortjeneste på prosjektforhandlinger. Som standard er standardkostnaden for produktet brukt som kostprisen. Standard kostpris kan imidlertid oppdateres i tilbudslinjen hvis det er en annen kostnadspris for det aktuelle tilbudet.

## <a name="price-list-items"></a>Prislisteelementer

Du kan legge til produkter fra en produktkatalog i forskjellige prislister. Prislistelinjer for produkter refererer alltid til en bestemt enhet. Priser for et produkt i prislisteelementer kan konfigureres som et valutabeløp. De kan også konfigureres som en funksjon av listepris, løpende kostnad eller standardkostnad.

PSA støtter ulike avrundingsalternativer når priser konfigureres som en funksjon av listepris, standardkostnad eller løpende kostnad. I tillegg til å dra nytte av flere prisingsmetoder og avrundingsalternativer kan du knytte rabattlister til prislisteelementer. 

> ![Legge til produkter fra en katalog i forskjellige prislister.](media/basic-guide-16.png)

Når du oppretter en ny egen definert prisliste for et tilbud ved **Opprett egendefinert prising** på siden **Prosjekttilbud**, lager PSA en kopi av prislisten, og **Enhet**-feltet i overskriften i den nye prislisten settes til **Salgsenhet**. Navnet på den nye prislisten føyes til med navnet på tilbudet og et tidsstempel. Du kan også bruke navnet på den nye prislisten og navnet på tilbudet i egendefinerte arbeidsflyter for å utløse ytterligere gjennomsyn og godkjenninger for tilbud som bruker et egendefinert pris.

 
## <a name="default-product-price-list"></a>Standard produktprisliste
Hver kundeoppføring har et **Standard prisliste**-felt der du kan angi en prisliste som samsvarer med kundens valuta. I PSA blir det ikke automatisk lagt inn en standardverdi i dette feltet. Når en egendefinert prisavtale med en bestemt kunde finnes, kan du bruke dette feltet til å knytte en prisliste til den aktuelle kunden.

Enhetene Salgsmulighet, Tilbud og Prosjektkontrakt bruker følgende rekkefølge til å angi standard prislister for produkter. Den samme rekkefølgen brukes for prosjektprislister.

1.  Tilbud
2.  Salgsmulighet
3.  Kunde
4.  Globale innstillinger for PSA

**Produkt**-feltet på tilbudslinjen viser som standard alle de aktive produktene i produktprislisten for tilbudet. Hvis et produkt er deaktivert, eller det er et utkastprodukt, vises det ikke, selv om det er i prislisten. 

Produktkataloglinjer legges til som fakturalinjer på den første fakturaen som opprettes for en prosjektkontrakt. Disse fakturalinjene kan slettes på et fakturautkast. I slike tilfeller vil linjene vises på en etterfølgende faktura til de faktureres eller til fakturaen sendes til kunden. I PSA kan du ikke fakturere et delvist antall av en produktfakturalinje. Når produktlinjene fra prosjektkontrakten faktureres, opprettes faktiske verdier. De faktiske verdiene blir imidlertid ikke koblet til den relaterte prosjektenheten. Med andre ord er produktbaserte prosjektkontraktlinjer uavhengige av prosjektbasert forbruk. PSA sporer ikke materialforbruk på prosjekter.


[!INCLUDE[footer-include](../includes/footer-banner.md)]