---
title: Bemanning av et prosjekt med kontraktarbeidere og underkontraktkapasitet
description: Denne artikkelen forklarer hvordan prosjektkrav kan bemannes ved hjelp av kontraktsarbeidere eller underordnet kapasitet i Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 173e1c20d2d046ee2120ec178e51d4868b70847d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922096"
---
# <a name="staffing-a-project-with-contract-workers-and-subcontracted-capacity"></a>Bemanning av et prosjekt med kontraktarbeidere og underkontraktkapasitet

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Generiske prosjektteammedlemmer kan bemannes med ansatte eller kontraktarbeidere. Når du bemanner et prosjekt med kontraktsarbeidere, kan du begrense bemanningsalternativene til bestemte kontraktarbeidere som er tilordnet en underleverandørlinje. 

## <a name="search-for-staff-resource-requirements-with-contract-workers-that-belong-to-a-specific-subcontract-line"></a>Søke etter ressurskrav for ansatte med kontraktarbeidere som tilhører en bestemt underkontraktlinje

Følg disse trinnene for å søke etter og bemanne ressurskrav for ansatte med kontraktarbeidere som tilhører en bestemt underkontraktlinje:

1. Opprett et generisk prosjektteammedlem som refererer til en underkontrakt og en underkontraktlinje.
2. Generer et ressurskrav for dette generiske prosjektteammedlemmet ved å bruke knappen **Generer krav**-knappen på delrutenettet for prosjektteammedlemmer.
3. Velg raden for teammedlem, og velg deretter **Bestill**-knappen i delrutenettet. 
4. Dermed åpnes planleggingstavlen med kravkonteksten. Sammen med andre attributter, for eksempel felt for datoer, rolle og organisasjonsfelt, fylles filtrene for planleggingstavlen automatisk ut med feltene for leverandør, underkontrakt og underkontraktlinje fra ressurskravet.
5. Systemet søker etter ressurser som oppfyller filtervilkårene, og viser dem. 
6. Velg en av de filtrerte ressursene, og reserver ressursen for kravet. 
7. Et prosjektteammedlem opprettes og oppdateres med referanser til underkontrakt og underkontraktlinje. Gå til **Prosjektestimater**, og velg **Oppdater priser** for å vise de oppdaterte kostnadene for ressurstilordningen. 

> [!NOTE]
> Det kan hende at det ikke alltid er mulig å oppdatere prosjektteammedlemmet med en underkontrakt- og underkontraktlinjereferanse i bestillingen hvis ressursen er tilordnet flere underkontraktlinjer. Hvis systemet ikke kan oppdatere prosjektteammedlemmet med en underkontrakt og en underkontraktlinjre, åpner du oppføringen for prosjektteamet og oppdaterer disse feltene manuelt, slik at estimatet for økonomisk kostnad gjenspeiler underleverandørkostnaden nøyaktig.

## <a name="search-for-and-staff-resource-requirements-with-any-contract-worker"></a>Søke etter og bemanne ressurskrav med hvilken som helst kontraktarbeider

Slik søker du etter og bemanner ressurskrav med hvilken som helst kontraktarbeider:

1. Opprett et generisk prosjektteammedlem.
2. Generer et ressurskrav for dette generiske prosjektteammedlemmet ved å bruke knappen **Generer krav**-knappen på delrutenettet for prosjektteammedlemmer.
3. Velg raden for teammedlem, og velg deretter **Bestill**-knappen i delrutenettet. 
4. Dermed åpnes planleggingstavlen med kravkonteksten. Sammen med andre attributter, for eksempel felt for datoer, rolle og organisasjonsfelt, fylles filtrene for planleggingstavlen automatisk ut med feltene for leverandør, underkontrakt og underkontraktlinje fra ressurskravet. Fordi det ikke ble fylt ut noen underkontrakt- eller underkontraktslinjeverdier for kravet, blir disse attributtene tomme i filterruten.
5. Systemet søker etter ressurser som oppfyller filtervilkårene, og viser dem.
6. Oppdater **Arbeidertype**-feltet i filterruten til **Kontraktarbeider** for å begrense søket til kontraktarbeidere. Oppdater **Leverandør** i filterruten til å velge en leverandør for å begrense søket til bare å vise kontraktarbeidere som tilhører et bestemt leverandørfirma.
7. Velg en kontraktarbeider fra listen, og reserver ressursen for kravet.
8. Et prosjektteammedlem opprettes. Prosjektteammedlemmet oppdateres imidlertid ikke med noen underkontrakt eller underkontraktlinje, og ressurstilordningen vil derfor ikke bli kostnadsbelagt med underkontraktsprisingene. Oppdater prosjektteammedlemmet manuelt med en underleverandørlinje, og gå til **Prosjektestimater**, og velg **Oppdater priser** for å vise de oppdaterte kostnadene for ressurstilordningen.

> [!NOTE]
> Prosjektteammedlemmer som har **Arbeidertype** som **Kontraktarbeider**, men som ikke har en underkontraktsreferanse, blir flagget som **Ugyldig** i rutenettet for **Prosjektteammedlemmer**. Hvis det finnes prosjektteammedlemmer med denne statusen, åpner du oppføringen for prosjektteamet og oppdaterer feltene for underkontrakt og underkontraktlinje manuelt, slik at estimatet for økonomisk kostnad gjenspeiler underleverandørkostnaden nøyaktig i kategorien **Estimater**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
