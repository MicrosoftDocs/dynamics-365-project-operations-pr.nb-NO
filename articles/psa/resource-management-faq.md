---
title: Vanlige spørsmål om ressursbehandling
description: Dette emnet inneholder svar på vanlige spørsmål om ressursbehandling.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d335a12a9b478bff63b6c93809c89dac9718a4be
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144380"
---
# <a name="resource-management-faq"></a>Vanlige spørsmål om ressursbehandling

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Hva er forskjellen mellom et teammedlem og et ressurskrav?

Et prosjektteammedlem kan tildeles oppgaver, bestilte eller overbestilte, og angis som en godkjenner. Et ressurskrav kan eksistere uten et prosjektteammedlem, som et utkast til behov. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Hva er forskjellen mellom foreslåtte og ikke-forpliktende timer?

Foreslåtte timer og ikke-forpliktende timer er forskjellige i synligheten. Foreslåtte timer vises bare for ressursledere og prosjektlederen som igangsatte behovet ved å bruke en ressursforespørsel. Ikke-forpliktende timer er synlige for alle som har tilgang til planleggingstavlen.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Hvordan kan jeg vise ikke-forpliktende timer for ressurser i et team?

Ikke-forpliktende bestillinger kan utføres når du bestiller et ressurskrav. Ressurser som er ikke-forpliktende bestilt i et prosjektteam, vises som teammedlemmer som har ikke-forpliktende timer. De vises også på planleggingstavlen.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Hvordan endrer jeg de nødvendige timene, og start- og sluttdatoene for en ressurs (genereøt eller navngitt) som jeg har bestilt?

Når ressursene er bestilt, velger du **Vedlikehold bestillinger** for å gjøre eventuelle endringer som kreves.

## <a name="what-resources-types-does-project-service-automation-support"></a>Hvilke ressurstyper støtter Project Service Automation?

**Bruker** og **Kontakt** er de eneste ressurstypene som støttes i Dynamics 365 Project Service Automation. Selv om du kan opprette andreressurs typer (for eksempel **Utstyr** og **Gruppe**), er det ingen ende-til-ende-brukstilfelle som støttes for dem.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Hva er forskjellen mellom en tilordning og en bestilling?

Tildelinger er tilordningen av ressurser til prosjektoppgaver i prosjektplanen. Ressursene kan være enten reelle ressurser eller generelle ressurser. Bestillinger er forpliktende eller ikke-forpliktende tildeling av ressurser i et prosjekt. Forpliktende bestillinger bruker kapasiteten til en ressurs. Ideelt sett bør bestillinger og tildelinger for reelle ressurser være de samme, fordi de ikke er forskjellige. PSA håndhever imidlertid ikke denne avtalen. Avstemming-visningen viser en prosjektleder steder der bestillingene og tildelingene til en ressurs ikke er de samme.
