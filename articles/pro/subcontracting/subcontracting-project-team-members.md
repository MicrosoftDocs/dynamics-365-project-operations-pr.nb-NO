---
title: Prosjektteammedlemmer for underkontrakter
description: Denne artikkelen forklarer hvordan prosjektteammedlemmer legges til i underkontrakter i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 9/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a2f17d6f270029e3a517e99c7bb518cdb19b8d23
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522808"
---
# <a name="subcontracting-project-team-members"></a>Prosjektteammedlemmer for underkontrakter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Microsoft Dynamics 365 Project Operations kan du velge å legge til ubemannede og bemannede prosjektteammedlemmer i underkontrakter.

- Ubemannede prosjektteammedlemmer har en tilordnet generell ressurs.
- Bemannede teammedlemmer har en navngitt ressurs tilordnet.

Når du kobler et prosjektteammedlem til en underkontraktlinje, vil eventuelle tilordninger til oppgaver som teammedlemmet har, rekalkuleres basert på innkjøpsprislisten som er vedlagt underkontrakten.  I kategorien **Estimater** på **Prosjektdetaljer**-siden velger du **Oppdater priser**-knappen for å vise oppdaterte priser og/eller kostnader som følger av beslutningen om underkontrakt. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Underkontrakt for et ubemannet prosjektteammedlem
Siden **Teammedlemsdetaljer** har felt for underkontrakt og underkontraktlinje som gjør det mulig for en prosjektleder å uttrykke hvordan de ønsker å hente kapasiteten som kreves fra en underleverandør. Følg denne fremgangsmåten for å hente et prosjektteammedlem som en generell ressurs til underkontrakt:

1.  Velg en underkontrakt på siden for **detalj for teammedlem**.

2.  Du kan bare velge underkontrakter med status **Utkast** eller **Bekreftet**. Underkontrakter som er **Lukket** eller **Kansellert**, kan ikke velges. 

3.  Feltet for **Underkontraktlinje** blir synlig etter at du har valgt en underkontrakt.

4.  I feltet **Underkontraktlinje** kan du bare velge underkontraktlinjer som er for tid. Du kan ikke velge underkontraktlinjer for utgifter eller materiell.

5.  Rollen for prosjektteammedlemoppføringen må samsvare med rollen på underkontraktslinjen. Dette sikrer at tiden for rollen som blir beregnet for prosjektet, er den samme rollen som kjøpes på underkontraktslinjen. 

Når et generisk teammedlem er knyttet til en underkontrakt og underkontraktslinje, oppdateres feltet **Arbeidertype** for det generiske teammedlemet til **Kontraktarbeider**, og **Gyldighet for underkontrakt** settes til **Gyldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Underkontrakt for et bemannet prosjektteammedlem
På samme måte som generiske eller ubemannede teammedlemmer kan bemannet gruppemedlemskapasitet som kreves for et prosjekt, også kobles til en underkontrakt. Følg denne fremgangsmåten for å hente et navngitt prosjektteammedlem til en underkontrakt:

1.  Kontroller at den navngitte ressursen er konfigurert som en kontraktarbeidertype for ressurs som kan reserveres. Kontroller også at **Leverandør**-feltet for ressursen som kan reserveres, samsvarer med leverandøren på underkontrakten du velger. 

2.  Du kan bare velge underkontrakter med status **Utkast** eller **Bekreftet**. Underkontrakter som er **Lukket** eller **Kansellert**, kan ikke velges. 

3.  Feltet for **Underkontraktlinje** blir synlig etter at du har valgt en underkontrakt.

4.  I feltet **Underkontraktlinje** kan du bare velge underkontraktlinjer som er for tid. Du kan ikke velge underkontraktlinjer for utgifter eller materiell.

5.  Rollen for prosjektteammedlemoppføringen må samsvare med rollen på underkontraktslinjen. Dette sikrer at tiden for rollen som blir beregnet for prosjektet, er den samme rollen som kjøpes på underkontraktslinjen. 

Navngitte prosjektteammedlemmer som er konfigurert som en kontraktarbeidertype av typen **Bestillbar ressurs** vises med statusen **Ikke gyldig** hvis de ikke er koblet til en underkontrakt. Når et navngitt prosjektteammedlem er knyttet til en underkontrakt og underkontraktslinje, oppdateres feltet **Arbeidertype** i teammedlemraden til **Kontraktarbeider**, og **Gyldighet for underkontrakt** settes til **Gyldig**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
