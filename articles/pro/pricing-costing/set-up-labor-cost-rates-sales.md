---
title: Konfigurere kostnadssatser for arbeid – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnadssatser for arbeid i Project Operations.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c7b00d018f20dd79d5a6f8444a25ed4768cc6b220023fd08967eb917e2f4f2b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006123"
---
# <a name="set-up-labor-cost-rates---lite"></a>Konfigurere kostnadssatser for arbeid – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Hver prisliste har et sett med arbeidssatser (rollepriser), som er rettet inn etter innholdet og datogyldigheten for prislisten.

1. Opprett en prisliste, og velg **Ny rolle** i delrutenettet i kategorien **Rollepris**.
2. Velg rollen og organisasjonsenheten på **hurtigopprettingssiden**.
3. Angi annen obligatorisk informasjon i feltene.

Tabellen nedenfor inneholder noen av feltene som er viktige når du oppretter arbeidssatser i en kostprisliste.

| Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
| --- | --- | --- | --- |
| Rolle | Sidene **Generelt** og **Hurtigoppretting** | Velg rollen som kostnadssatsen gjelder for. | Rollen på det innkommende estimatet eller den faktiske verdien samsvares mot denne linjen for å standardisere kostnaden for rollen. |
| Ressursenhet | Sidene **Generelt** og **Hurtigoppretting** | Velg organisasjonsenheten eller divisjonen av firmaet som denne rollen skal brukes fra. For eksempel en utvikler fra robotavdelingen hos Fabrikam India eller en utvikler fra programvareavdelingen hos Fabrikam USA. | Resursenheten på det innkommende estimatet eller den faktiske verdien samsvares mot denne linjen for å standardisere kostnaden for rollen. |
| Pris | Sidene **Generelt** og **Hurtigoppretting** | Angi kostnadssatsen for kombinasjonen av ressursfirma og ressursenhet for rollen. For eksempel en utvikler fra Fabrikam India koster 1000 INR, eller en utvikler fra Fabrikam USA koster 150 USD. | Prisen er kostnadssatsen som brukes som standard på kostnaden per enhet på det innkommende estimatet eller den faktiske linjen i **Tid**-transaksjonsklassen. |
| Valuta | Sidene **Generelt** og **Hurtigoppretting** | Som standard kommer valutaverdien fra valutaen i hodet i kostprislsiten, men dette kan overstyres. En utvikler fra Fabrikam India koster for eksempel 1000 INR. En utvikler fra Fabrikam USA koster 150 USD. | Denne valutaen er standardvalutaen for kostnaden per enhet på den innkommende faktiske kostnadslinjen for **Tid**-transaksjonsklassen. I et prosjektestimat konverteres valutaverdien til prosjektvalutaen, og den vises i den tidsinndelte visningen av estimatet. |
| Tidsplan for enhet | Sidene **Generelt** og **Hurtigoppretting** | Enhetsplanen bruker tid som standard og kan ikke endres i rolleprisenheten fordi den brukes til å uttrykke priser etter tidsenheter. | Dette har ingen innvirkning nedstrøms. |
| Enhet | Sidene **Generelt** og **Hurtigoppretting** | som standard kommer verdien fra **Tidsenhet**-feltet i hodet i kostprislisten. Verdien kan overstyres. En utvikler fra Fabrikam India koster for eksempel 1000 INR per **dag i India**. En utvikler fra Fabrikam USA koster 150 USD **per dag i USA**. | Systemet bruker enhetssystemet og konverteringen i basisenheter til å beregne en kostnad per enhet, for å beregne standardprisen per enhet på et innkommende estimat eller en faktisk linje. Et estimat er for eksempel 10 **dager i India** med arbeid for en utvikler fra India, og enheten **dag i India** defineres som 10 timer. Ved kostnadsberegnings av denne estimatlinjen beregner programmet enhetskosten på estimatet som: 1000 INR / 10 timer = 100 INR per time, som konverteres til USD og vises som enhetskostnad på **Prosjektestimater**-siden. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Overføre prising og kostnader for ressurser utenfor divisjonen eller den juridiske enheten

I prosjektbaserte selskaper er det vanlig å bruke ansatte fra ulike juridiske enheter eller divisjoner på prosjekter. Et prosjekt kan utføres av én juridisk enhet, men de ansatte eller konsulenter som arbeider med prosjekt, kan komme fra samme juridiske enhet eller fra en annen, eller en kombinasjon av begge deler. I Dynamics 365 Project Operations er den juridiske enheten som eier leveringen av prosjektet, **Eierfirmaet**, og divisjonen som eier leveringen, er **Kontraktsenhet**. Andre juridiske enheter som leverer ressurser, kalles for **ressursselskaper**, og divisjonene som leverer ressurser, kalles for **ressursenheter**. I de fleste land kreves det at selskaper må forsikre seg om at den juridiske ressursenheten eller divisjonen, belaster det eiende firmaet og kontraktenheten for bruk av ressurser.

Fabrikam Corporation må for eksempel sikre at Fabrikam India - robot har et forhandlet et kostnadssatskort med Fabrikam USA - robot eller Fabrikam UK - robot

En utvikler fra Fabrikam India – robot koster $100 ved utlån til Fabrikam US - robot og $150 ved utlån til Fabrikam UK - robot

### <a name="set-up-costs-for-outside-resources"></a>Konfigurere kostnader for eksterne ressurser

1. Opprett en kostprisliste kalt *Kostnadssatser for Fabrikam US - robot*, og angi et gyldig datointervall.
2. Angi kostprislisten angir du satser ved å bruke informasjon fra tabellen nedenfor. 

| Rolle | Ressursstyringsfirma | Ressursenhet | Kostnadssats |
| --- | --- | --- | --- |
| Developer | Fabrikam India | Fabrikam India - robot | $ 100 |
| Developer | Fabrikam Filippinene | Fabrikam Filippinene -robot | $90 |
| Developer | Fabrikam USA | Fabrikam USA - robot | $150 |

3. Legg ved denne kostprislisten i organisasjonsenheten Fabrikam US - robot

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Konfigurere overføringspriser for en ressurs i riktig valuta 

I Project Operations kan du angi ressurspriser i hvilken som helst valuta. Valutaen settes som standard til den som er i prislistehodet, men dette kan endres.

Ved å bruke eksemplet på oppsett av overføringspris må informasjonen endres til:

Fabrikam Corporation må sikre at Fabrikam India - robot har et forhandlet en kostnadssats med Fabrikam USA - robot eller Fabrikam UK - robot

En utvikler fra Fabrikam India – robot koster 5000 INR ved utlån til Fabrikam US - robot og 5500 IRN ved utlån til Fabrikam UK - robot

I kostprislisten for Fabrikam US - robot kan kostnadssatser uttrykkes som følgende:

| Rolle | Ressursstyringsfirma | Kostnad |
| --- | --- | --- |
| Developer | Fabrikam India | 5000 INR |
| Developer | Fabrikam USA | 115 USD |

I kostprislisten for Fabrikam UK - robot kan kostnadssatser uttrykkes som følgende:

| Rolle | Ressursstyringsfirma | Kostnad |
| --- | --- | --- |
| Developer | Fabrikam India | 5500 INR |
| Developer | Fabrikam UK | 115 GBP |

Kostprislisten kan levere arbeidssatser i flere valutaer. Ved generering av et kostnadsestimat på prosjektet, konverterer Project Operations disse kostnadskostnadene til prosjektvalutaen, og den vises for brukeren. Når en tidsoppføring godkjennes og det blir opprettet en faktisk kostnad, er den faktiske kostnaden priset i valutaen for den tilsvarende rolleprislinjen i kostprislisten. Faktiske kostnader for tid i ett enkelt prosjekt kan registreres i flere valutaer. Ved beregning eller oppsummering av faktiske arbeidskostnader på prosjektnivå vil imidlertid Project Operations konvertere alle kostnadsbeløp for arbeid til prosjektvalutaen, som brukeren kan vise.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]