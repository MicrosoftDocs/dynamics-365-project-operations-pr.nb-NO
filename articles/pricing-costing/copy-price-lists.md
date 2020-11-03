---
title: Kopiere prislister
description: Dette emnet gir information om hvordan du kopierer prislister i Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081659"
---
# <a name="copy-price-lists"></a>Kopiere prislister

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan opprette kopier av prislister i Dynamics 365 Project Operations. Du kan for eksempel opprette prislister for forestående år ved hjelp av en prisliste fra inneværende år.  Du kan også kopiere en prisliste for fakturasatser og salgs priser fra prislistene for kostnad. 

Fullfør fremgangsmåten nedenfor for å lage en kopi av en prisliste.

1. Åpne prislisten du vil lage en kopi av, og velg **Kopier**.
2. Angi eventuell informasjon som er nødvendig for å kopiere prislisten. Tabellen nedenfor viser hensyn du må huske på når du skriver inn informasjon.

| Felt | Relevans, formål og veiledning | Nedstrøms påvirkning |
| --- | --- | --- |
| Navn | Navnet på kildeprislisten med **-kopi** tilføyd. | Prislisten inneholder denne verdien for alle listesider og alternativer i rullegardinlister. |
| Kontekst | Angi konteksten du vil ha for målprislisten. | En prisliste som har konteksten angitt til **Kostnad** , brukes til å slå opp prisen på kostnadsestimater og faktiske kostnader. En prisliste som har konteksten angitt til **Salg** , brukes til å slå opp prisen på salgsestimater og faktiske salgsverdier. Bare prislister som har konteksten angitt til **Salg** , kan knyttes til en prosjektprisliste for en kunde, et tilbud eller en kontrakt. |
| Startdato | Startdatoen i perioden som prislisten er gyldig i. | Sammen med **Sluttdato** brukes dette feltet til å finne ut hvilken prisliste som gjelder for et bestemt estimat eller en faktisk linje. |
| Sluttdato | Sluttdatoen i perioden som prislisten er gyldig i. | Sammen med **Startdato** brukes dette feltet til å finne ut hvilken prisliste som gjelder for et bestemt estimat eller en faktisk linje. |
| Valuta | Valutaen for kildeprislisten. Dette kan endres. | Når dette endres, konverteres alle resulterende prislinjer for arbeid, utgifter og produktkatalogvarer til valutaen for målprislisten under kopieringen. |
| Tidsenhet | Valutaen for kildeprislisten. Dette kan endres. | Når dette endres, konverteres alle resulterende prislinjer for arbeidselementer til enheten i målprislisten under kopieringen. Konverteringen fra enhetsoppsettet for tidsenheten for kildeprisliste og målprisliste brukes. |
| Beskrivelse | En beskrivelse av kildeprislisten med **-kopi** tilføyd. Dette er et tekstfelt som gjør det mulig å ha en flerlinjet beskrivelse av prislisten. | Dette feltet vises i de **tilknyttede** visningene i prislisten i ulike enheter som har relaterte prislister. |

3. Lagre prislisten. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Oppdatere en prisliste ved å bruke en merking på alle prisene

1. På fanene **Rolle** , **Kategori** og **Prislisteelement** i en prisliste kan du velge **Oppdater priser** for å bruke et påslag for alle prisene i delrutenettet. 
2. Angi et påslag på dialogsiden som åpnes. Du kan også angi en negativ påslagsprosent for å redusere prisen etter en bestemt prosentsats. 
3. Velg **OK** på dialogsiden, og kontroller deretter at prisene i delrutenettet gjenspeiler endringene du har gjort.
