---
title: Konfigurere fakturasatser for arbeid
description: Denne artikkelen inneholder informasjon om hvordan du konfigurerer faktureringssatser for arbeid i Project Operations.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0ad83e899030be480baed95597e1ccfc0e560e24
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924350"
---
# <a name="set-up-labor-bill-rates"></a>Konfigurere fakturasatser for arbeid

_ **Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

Hver prisliste har et sett med rollepriser, eller arbeidssatser, som gjelder for konteksten og datogyldigheten som er inkludert i prislistehodet. Fakturasatser for tidspunkt i Dynamics 365 Project Operations kan bare angis i én valuta, som er valutaen i Prisliste-hodet.

1. Hvis du vil konfigurere fakturasatser for arbeid for en salgsprisliste, går du til **Salg** > **Kunder** > **Prislister** og velger **Ny** for å opprette en ny prisliste. 
2. I delrutenettet i kategorien **Rollepriser** velger du **Ny rollepris**. 
3. I **hurtigopprettingsruten** angir du hvilken kombinasjon av rolle og organisasjonsenhet du må definere fakturasatsen for.

   Tabellen nedenfor inkluderer feltene i kategorien **Generelt** og **Hurtigopprett**-ruten for en rolleprislinje som du må huske på når du oppretter rollepriser i en salgs- eller kostprisliste.

    | Felt | Sted | Beskrivelse | Nedstrøms påvirkning |
    | --- | --- | --- | --- |
    | Rolle | Kategorien **Generelt** og **hurtigopprettingsruten** | Velg rollen du angir fakturasatsen for. | Rollen på det innkommende estimatet eller den faktiske verdien samsvares mot denne linjen for å standardisere fakturasatsen for rollen. |
    | Ressursstyringsfirma | Kategorien **Generelt** og **hurtigopprettingsruten** | Velg firmaet eller den juridiske enheten som rollen er fra. For eksempel en utvikler fra Fabrikam India eller en utvikler fra Fabrikam USA. | Resursfirmaet på det innkommende estimatet eller den faktiske verdien samsvares mot denne linjen for å standardisere fakturasatsen for rollen. |
    | Ressursenhet | Kategorien **Generelt** og **hurtigopprettingsruten** | Velg organisasjonsenheten eller divisjonen av firmaet som rollen er fra. For eksempel en utvikler fra robotavdelingen hos Fabrikam India eller en utvikler fra programvareavdelingen hos Fabrikam USA. | Resursenheten på det innkommende estimatet eller den faktiske verdien samsvares mot denne linjen for å standardisere fakturasatsen for rollen. |
    | Pris | Kategorien **Generelt** og **hurtigopprettingsruten** | Angi fakturasatsen for kombinasjonen av ressursfirma og ressursenhet for rollen. En utvikler fra Fabrikam India har for eksempel en fakturasats på 100 USD, mens en utvikler fra Fabrikam USA har en fakturasats på 150 USD. | Denne prisen er standard fakturasats på prisen per enhet på det innkommende estimatet eller den faktiske linjen i tidstransaksjonsklassen. |
    | Valuta | Kategorien **Generelt** og **hurtigopprettingsruten**| Som standard kommer valutaverdien fra valutaen i hodet i salgsprislistehodet. I en salgsprisliste kan ikke valutaen overstyres. | Denne valutaen er standardvalutaen for prisen per enhet på den innkommende faktiske salgslinjen i tidstransaksjonsklassen. |
    | Tidsplan for enhet | Kategorien **Generelt** og **hurtigopprettingsruten** | Denne enhetsplanen bruker tid som standard og kan ikke endres i rolleprisenheten fordi den brukes til å uttrykke priser etter tidsenheter. | Dette feltet har ingen nedstrøms påvirkning. |
    | Enhet | Kategorien **Generelt** og **hurtigopprettingsruten** | Enhetsverdien kommer fra **Tidsenhet**-feltet i salgsprislistehodet. Men verdien kan imidlertid overstyres. En utvikler fra Fabrikam India har for eksempel en fakturasats på 1000 USD per **dag i India**. En utvikler fra Fabrikam USA har en fakturasats på 1500 USD per **dag i USA**. | Når prisen per enhet som standard brukes på et innkommende estimat eller en faktisk linje, bruker systemet enheter og konvertering i basisenheter for å beregne en pris per enhet. Estimatet er for eksempel 10 **dager i India** med arbeid for en utvikler fra India, og enhet dag i India defineres som 10 timer. Når denne estimatlinjen skal prises, beregner programmet enhetsprisen på estimatet som 1000 USD/10 timer = 100 USD per time. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Overføring av priser eller oppsett av fakturasatser fra andreorganisasjons enheter eller divisjoner 

Prosjektbaserte selskaper bruker ofte ansatte fra ulike juridiske enheter og ulike divisjoner innenfor den juridiske enheten til å arbeide med prosjekter. Prosjekter kan utføres fra en bestemt juridisk enhet og divisjon, mens de ansatte eller konsulenter som arbeider med prosjektene, kan komme fra samme juridiske enhet og divisjon eller fra en annen. Prosjektet kan også bestå av en kombinasjon av personer fra forskjellige juridiske enheter og divisjoner. I Project Operations kalles den juridiske enheten som eier leveringen av prosjektet, for det **eiende selskapet**, og divisjonen som eier leveringen, kalles for en **kontraktenheten**. Alle de andre juridiske enhetene som leverer ressurser, kalles for **ressursselskaper**, og divisjonene som leverer ressurser, kalles for **ressursenheter**. På grunn av forskjellen i arbeidskostnadene på tvers av forskjellige geografier og arbeidsmarkeder over hele verden er det også satt opp kostnadssatser for arbeidskraft på forskjellige måter for forskjellige geografier.

En utvikler fra robotavdelingen hos Fabrikam India som arbeider med et prosjekt i USA, blir for eksempel fakturert med en sats på 100 USD per time. En utvikler fra robotavdelingen hos Fabrikam US som arbeider med et prosjekt i USA, blir fakturert på 150 USD per time. 

### <a name="example-set-up-a-bill-rate"></a>Eksempel: Definere en fakturasats 

1. Opprett en salgsprisliste kalt for *Fakturasatser for Fabrikam USA*, og angi datogyldigheten.
2. Angi følgende satsinformasjon i salgsprislisten:

    | Rolle | Ressursstyringsfirma | Ressursenhet | Fakturasats |
    | --- | --- | --- | --- |
    | Developer | Fabrikam India | Fabrikam India - robot | $ 100 |
    | Developer | Fabrikam Filippinene | Fabrikam Filippinene -robot | $90 |
    | Developer | Fabrikam USA | Fabrikam USA - robot | $150 |

3. Legg ved salgsprislisten, **Fakturasatser for Fabrikam USA** i prosjektprislisten for prosjektkontrakten eller en bestemt forretningsforbindelse.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
