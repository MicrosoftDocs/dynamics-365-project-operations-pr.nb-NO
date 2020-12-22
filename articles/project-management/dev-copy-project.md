---
title: Utvikle prosjektmaler med Kopier prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter prosjektmaler ved hjelp av den egendefinerte handlingen Kopier prosjekt.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642420"
---
# <a name="develop-project-templates-with-copy-project"></a>Utvikle prosjektmaler med Kopier prosjekt

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations støtter muligheten til å kopiere et prosjekt og gjenopprette eventuelle tildelinger til de generelle ressursene som representerer rollen. Kunder kan bruke denne funksjonaliteten til å bygge grunnleggende prosjektmaler.

Når du velger **Kopier prosjekt**, oppdateres statusen for målprosjektet. Bruk **Statusårsak** til å avgjøre når kopieringshandlingen er fullført. Ved å velge **Kopier prosjekt** oppdateres også startdatoen for prosjektet til nåværende startdato hvis det ikke registreres noen måldato i målprosjektenheten.

## <a name="copy-project-custom-action"></a>Egendefinert handling Kopier prosjekt 

### <a name="name"></a>Navn 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Inndataparametere
Det finnes tre inndataparametere:

| Parameter          | Type   | Verdier                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** eller **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Enhetsreferanse | Kildeprosjekt |
| Mål             | Enhetsreferanse | Målprosjekt |


- **{"clearTeamsAndAssignments":true}**: Standard virkemåte for prosjektet på nettet, og vil fjerne alle tilordninger og teammedlemmer.
- **{"removeNamedResources":true}** Standard virkemåte for Project Operations, og vil tilbakestille tilordninger til generelle ressurser.

For mer informasjon om handlinger, se [Bruke web-API-handlinger](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Angi felt som skal kopieres 
Når handlingen kalles, ser **Kopier prosjekt** på prosjektvisningen **Kopier prosjektkolonner** for å finne ut hvilke felter som skal kopieres når prosjektet kopieres.
