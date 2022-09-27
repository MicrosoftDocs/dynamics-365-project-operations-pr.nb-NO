---
title: Underkontraktalternativer for prosjektteammedlemmer
description: Denne artikkelen forklarer underkontraktalternativene for prosjektteammedlemmer i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 046b5d38ef7e433d02e3eac2e858a3333e941c45
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522291"
---
# <a name="subcontracting-options-for-project-team-members"></a>Underkontraktalternativer for prosjektteammedlemmer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I Microsoft Dynamics 365 Project Operations kan du evaluere underkontraktsalternativene som er tilgjengelige for ett eller flere prosjektteammedlemmer. Med de tilgjengelige underkontraktalternativene kan du gjøre følgende:

- Opprett en ny underkontrakt og/eller opprett nye linjer på en eksisterende underkontrakt for de valgte prosjektgruppemedlemmene. 
- Reserver mot en eksisterende underkontrakt og underkontraktlinje. 

Du kan velge blant de tilgjengelige underkontraktsalternativene for generelle prosjektteammedlemmer, eller velge blant prosjektteammedlemmer som er bemannet med en navngitt ressurs som er en kontraktarbeider. 

Det finnes ingen tilgjengelige underkontraktalternativer for følgende:

- Prosjektteammedlemmer som har vært bemannet med en ansatt. 
- Prosjektteammedlemmer som allerede er tilknyttet en underkontrakt og en underkontraktlinje. 

## <a name="subcontracting-an-unstaffed-project-team-member"></a>Underkontrakt for et ubemannet prosjektteammedlem

Følg denne fremgangsmåten for å se gjennom og velge blant de tilgjengelige underkontraktsalternativene for et generisk eller ubemannet prosjektteammedlem:

1. Velg én eller flere oppføringer for prosjektteam der ressursen er en generell ressurs.
2. Kontroller at ingen av de valgte medlemsoppføringene for prosjektteamet allerede er underkontrakt. 
3. Velg **Underkontraktalternativer** på delrutenettet for prosjektteammedlemmer. Dialogboksen **Underkontraktalternativer** åpnes. 
4. Hvis du bare valgte én oppføring for prosjektteam i trinn 1, vil følgende alternativer være tilgjengelige:
    - Opprett nye underkontraktlinjer. 
    - Reserver mot en eksisterende underkontrakt hvis du valgte flere prosjektteammedlemsoppføringer i trinn 1, er det eneste tilgjengelige alternativet å opprette en ny underkontraktlinje.
5. Alternativet for reservering mot en eksisterende underkontraktslinje gjør det mulig å velge en underkontrakt og underkontraktslinje som du vil reservere mot. Når du velger en underkontraktlinje for å reservere kapasitet, må du sørge for at den valgte underkontraktlinjen er et tidsskjema, og at rollen som kreves for prosjektteammedlemmet, samsvarer med rollen som ble kjøpt på underkontraktlinjen.
6. Når du velger å opprette nye underkontraktlinjer for prosjektteammedlemmene, tillater systemet at du velger underkontrakten du ønsker for å opprette disse linjene. Underkontrakten du velger å opprette nye linjer i, må ha statusen **Utkast**. Med dette alternativet for å opprette nye underkontraktslinjer for de valgte prosjektgruppemedlemmene, oppretter systemet én underkontraktslinje for tid for hvert prosjektteammedlem. Rollen, tiden og datoene kopieres fra prosjektteammedlemmet til hver underkontraktslinje som opprettes. 
7. Når et generisk teammedlem er knyttet til en underkontrakt og underkontraktslinje, oppdateres feltet **Arbeidertype** for det generiske teammedlemet til **Kontraktarbeider**, og verdien for **Gyldighet for underkontrakt** settes til **Gyldig**.

## <a name="subcontracting-a-staffed-project-team-member"></a>Underkontrakt for et bemannet prosjektteammedlem

På samme måte som generiske eller ubemannede teammedlemmer kan du også vise underkontraktsalternativer for et bemannet prosjektgruppemedlem så lenge den bemannede teammedlemmen er kontraktarbeider. Følg denne fremgangsmåten for å se gjennom og velge blant de tilgjengelige underkontraktsalternativene for et bemannet eller navngitt prosjektteammedlem:

1. Velg én eller flere prosjektteamoppføringer der ressursen er en navngitt kontraktarbeider.
2. Kontroller at ingen av de valgte medlemsoppføringene for prosjektteamet allerede er underkontrakt. 
3. Velg **Underkontraktalternativer** på delrutenettet for prosjektteammedlemmer. Dialogboksen **Underkontraktalternativer** åpnes. 
4. Hvis du bare valgte én oppføring for prosjektteam i trinn 1, vil følgende alternativer være tilgjengelige:
      - Opprett nye underkontraktlinjer.
      - Reserver mot en eksisterende underkontrakt.
  Hvis du valgte flere prosjektteammedlemsoppføringer i trinn 1, er det eneste tilgjengelige alternativet å opprette en ny underkontraktlinje.
5. Alternativet for reservering mot en eksisterende underkontraktslinje gjør det mulig å velge en underkontrakt og underkontraktslinje som du vil reservere mot. Når du velger en underkontraktlinje for å reservere kapasitet, må du sørge for følgende:
      - Den valgte underkontraktlinjen gjelder for tid. 
      - Rollen som kreves for prosjektteammedlemmet, samsvarer med rollen som ble kjøpt på underkontraktslinjen. 
      - Leverandøren som kontraktarbeideren er tilknyttet, er den samme som leverandøren på underkontrakten.
6. Når du velger å opprette nye underkontraktlinjer for prosjektteammedlemmene, tillater systemet at du velger underkontrakten du ønsker for å opprette disse linjene. Med dette alternativet kan du sikre at leverandøren som kontraktarbeideren tilhører, er den samme som leverandøren på underkontrakten. 
7. Underkontrakten du velger å opprette nye linjer i, må ha statusen **Utkast**. Med dette alternativet for å opprette nye underkontraktslinjer for de valgte prosjektgruppemedlemmene, oppretter systemet én underkontraktslinje for tid for hvert prosjektteammedlem. Rollen, tiden og datoene kopieres fra prosjektteammedlemmet til hver underkontraktslinje som opprettes.  
8. Når et navgitt teammedlem er knyttet til en underkontrakt og underkontraktslinje, oppdateres feltet **Arbeidertype** for det navngitte teammedlemet til **Kontraktarbeider**, og verdien for **Gyldighet for underkontrakt** settes til **Gyldig**.

## <a name="re-costing-subcontractor-assignments"></a>Ny kalkulering av underleverandørtilordninger

Når et prosjektteammedlem (generisk eller navngitt) er koblet til underkontraktlinjer ved hjelp av dialogboksen **Underkontraktsalternativer**, vil eventuelle tilordninger til oppgaver som teammedlemmet har, bli kalkulert på nytt basert på innkjøpsprislisten som er knyttet til underkontrakten. I kategorien **Estimater** på **Prosjektdetaljer**-siden velger du **Oppdater priser**-knappen for å vise oppdaterte priser og/eller kostnader som følger av beslutningen om underkontrakt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
