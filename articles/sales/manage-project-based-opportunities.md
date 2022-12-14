---
title: Administrer salgsmuligheter for prosjekt
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med salgsmuligheter som er knyttet til prosjekter.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 56eba38476dd5b49f0043eee5d411d51f9bf56b8
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825344"
---
# <a name="manage-project-opportunities"></a>Administrer salgsmuligheter for prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Prosjektrelaterte selskaper har vanligvis sine operasjoner for levering spredt på tvers av flere land og i flere geografier. Kostnaden av prosjektutførelsen og -leveringen kan variere avhengig av hvilken geografi eller divisjon som administrerer leveringen. Dette kan i sin tur påvirke marginene i avtalen. Levering av prosjektrelaterte tjenester involverer vanligvis store mengder menneskelig ressurstid, betydelige utgifter til reise, materialkostnader og andre utgifter.

Prosjektbaserte salgsmuligheter i Dynamics 365 Project Operations er utformet med utvidelser for Dynamics 365 Sales. Artikkelen inneholder detaljer om de forskjellige feltene og forretningslogikken som er inkludert i tilleggsfunksjonaliteten som kreves av prosjektbaserte firmaer for å administrere prosjektbaserte salgsmuligheter.

## <a name="view-all-project-based-opportunities"></a>Vise alle prosjektbaserte salgsmuligheter

Du kan se en liste over alle de prosjektrelaterte salgsmulighetene fra listesiden **Salgsmulighet**. 

1. Gå til **Salg** > **Salgsmuligheter**.
2. Bruk **Vis bryter** til å velge andre filtrerte visninger av salgsmulighetene. Du kan opprette dine egne visninger med egendefinerte filtervilkår for å konfigurere disse visningene og navigasjonsalternativene.

Du kan opprette eller slette prosjektsalgsmuligheter fra listesiden eller detaljsiden.

## <a name="business-process-flow-for-project-based-deals"></a>Forretningsprosessflyt for prosjekt baserte avtaler

Følgende forretningsprosessflyter støttes for prosjektbaserte avtaler i Project Operations:

- Forretningsprosessen for kundeemne til salgsmulighet
- Salgsprosess for salgsmulighet

### <a name="lead-to-opportunity-business-process"></a>Forretningsprosessen for kundeemne til salgsmulighet 
Forretningsprosessen for kundeemne til salgsmulighet støtter følgende faser:

| Etappe | Tilordnet enhet | Funksjonalitet |
| --- | --- | --- |
| Kvalifiser | Emne | Kvalifiser kundeemnet for å opprette en forretningsforbindelse, kontakt og salgsmulighet. |
| Utarbeid | Salgsmulighet | Utvikle salgsmuligheten for å legge til mer informasjon om arbeidet som er involvert, viktige interessenter og konkurranse. |
| Foreslå | Salgsmulighet | Utvikle forslaget, og få godkjennelse fra det interne gjennomgangsteamet. |
| Lukk | Salgsmulighet | Vinn salgsmuligheten for å lukke avtalen. |

### <a name="opportunity-sales-process"></a>Salgsprosess for salgsmulighet
Salgsprosessen for salgsmulighet i Project Operations er en utvidelse av forretningsflyten for salgsprosess for salgsmulighet i Sales-programmet. Denne forretningsprosessen er opprinnelig utformet for å støtte følgende faser for en prosjektbasert salgsmulighet.

| Etappe | Tilordnet enhet | Funksjonalitet |
| --- | --- | --- |
| Kvalifiser | Salgsmulighet | Kvalifiser kundeemnet for å opprette en forretningsforbindelse, kontakt og salgsmulighet. |
| Foreslå | Tilbud | Utvikle forslaget, bruke prosjekttilbud og få godkjennelse fra det interne gjennomgangsteamet. |
| Kontrakt | Prosjektkontrakt | Vinn tilbudet for å opprette kontrakten, og begynn kjøring og levering av prosjektet. |
| Lukk | Prosjektkontrakt | Fullfør arbeidet og lukk prosjektkontrakten. |

> [!NOTE]
> Hvis den prosjektbaserte avtalen startet med et kundeemne, tar forretningsprosessen for kundeemnet til salgsmulighet forrang.
>
> Hvis den prosjektbaserte avtalen startet med en salgsmulighet, tar forretningsprosessen for salgsmulighet forrang.

Du kan redigere forretningsprosessflyten for produktet eller opprette dine egne forretningsprosessflyter for å spore salgsprosessen etter behov. Hvis du vil ha mer informasjon om forretningsprosessflyten, kan du se [Oversikt over forretningsprosessflyter](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
