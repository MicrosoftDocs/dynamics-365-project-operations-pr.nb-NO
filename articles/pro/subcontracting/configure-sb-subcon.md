---
title: Konfigurere planleggingstavlen for å vise kontraktarbeidere og underkontraktkapasitet
description: Denne artikkelen beskriver hvordan du konfigurerer Planleggingstavle i Microsoft Dynamics 365 Project Operations til å vise ressurskapasitet for underkontrakt under bemanning av prosjektressurskrav.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262229"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurere planleggingstavlen for å vise kontraktarbeidere og underkontraktkapasitet 

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Planleggingstavlen i Microsoft Dynamics 365 Project Operations kan brukes til å søke etter ressurser på to måter:

- Generelt ressurssøk uten konteksten for et bestemt prosjektbasert ressurskrav.
- Kravspesifikt ressurssøk der prosjektkravet vil gi konteksten for ressursene som foreslås.

Hvis du vil varsle planleggingstavlen om ressurskapasitet og kontraktarbeidere for underkontrakt, må du gjøre oppdateringer i innstillingene for Planleggingstavlen. Disse oppdateringene inkluderer: 
- Oppdater innstillinger for planleggingstavle for generelt ressurssøk.
- Oppdater innstillinger for planleggingstavle for kravbasert ressurssøk.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Oppdatere innstillinger for planleggingstavle for generelt ressurssøk
### <a name="update-filters-for-general-resource-search"></a>Oppdatere filtre for generelt ressurssøk
Når du søker etter en ressurs, må de tilgjengelige filtrene på planleggingstavlen oppdateres, slik at du også kan søke etter eksterne ressurser ved å angi ett eller alle av følgende:
  - Arbeidertype, om ressursene som vises, skal være kontraktarbeidere eller ansatte.
  - Leverandørfirmaet som en ressurs bør tilhøre.
  - Ressurser som tilhører en bestemt underkontrakt eller underleverandørlinje.
    
### <a name="update-retrieve-resource-query"></a>Oppdatere spørringen Hent ressurser
Spørringen som brukes for søk, bør også oppdateres til å bruke disse ekstra filterattributtene. Bruk følgende trinn for å oppdatere konfigurasjon for planleggingstavle for generelt ressurssøk:  
1. Åpne **Innstillinger for planleggingstavle** for en bestemt planleggingstavle.
2. Åpne kategorien **Generelle innstillinger**, og rull til **Andre innstillinger**.
3. I listen over innstillinger i denne delen oppdaterer du **Filteroppsett** til **Standard filteroppsett for Project Operations Lite**.
4. Oppdater **Spørringen Hent ressurser** til **Standard spørring for henting av ressurser for Project Operations Lite**.

![Oppdatere innstillinger for planleggingstavle for generelt ressurssøk](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Oppdatere innstillinger for planleggingstavle for kravbasert ressurssøk
### <a name="update-filters-for-requirement-specific-resource-search"></a>Oppdatere filtre for kravspesifikt ressurssøk 
Når du søker etter en ressurs, må de tilgjengelige filtrene på planleggingstavlen oppdateres, slik at du også kan søke etter eksterne ressurser ved å angi ett eller alle av følgende:
 - Arbeidertype, om ressursene som vises, skal være kontraktarbeidere eller ansatte.
 - Leverandørfirmaet som en ressurs bør tilhøre.
 - Ressurser som tilhører en bestemt underkontrakt eller underleverandørlinje.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Oppdatere hent ressursspørring for kravspesifikt ressurssøk 
Spørringen som brukes for søk, bør også oppdateres til å bruke disse ekstra filterattributtene. Bruk følgende trinn for å oppdatere konfigurasjon for planleggingstavle for kravbasert ressurssøk:

1. Åpne **Innstillinger for planleggingstavle** for en bestemt planleggingstavle, og velg deretter **Åpne standardinnstillinger** for å åpne innstillingene for kravspesifikk søk.
2. Åpne kategorien **Generelle innstillinger**, og rull til **Andre innstillinger**.
3. I listen over innstillinger i denne delen oppdaterer du **Filteroppsett** til **Standard filteroppsett for Project Operations Lite**.
4. Oppdater **Spørringen Hent ressurser** til **Standard spørring for henting av ressurser for Project Operations Lite**.
5. Åpne kategorien **Planleggingstyper**, og gå til **Prosjekt**.
6. Under innstillingene for **Prosjekt** oppdaterer du **Spørringen Hent ressurser for planleggingsassistent** til **Standard spørring for henting av ressurser for Project Operations Lite** og oppdaterer **Spørringen Hent begrensninger for planleggingsassistent** til **Standard spørring for henting av begrensninger for Project Operations Lite**.

![Oppdatere innstillinger for planleggingstavle for kravbasert ressurssøk](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
