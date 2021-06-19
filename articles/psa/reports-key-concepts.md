---
title: Nøkkelkonsepter
description: Dette emnet gir informasjon om nøkkelkonseptene for ressursbehandling i Project Service Automation.
author: ruhercul
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
ms.openlocfilehash: 5f314e3a6cc70748628145f693fb81b598e568dc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008863"
---
# <a name="key-concepts"></a>Nøkkelkonsepter

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Følgende tabell definerer nøkkelkonseptene som brukes i Dynamics 365 Project Service Automation-appen.

| Konsept                    | Definisjon |
|----------------------------|------------|
| Prosjektteammedlem        | Som en del av prosjektteamet kan et prosjektteammedlem være en navngitt ressurs som har bestillinger, en navngitt ressurs som ikke har bestillinger, eller en generell ressurs. Generelle ressurser har ikke bestillinger, er lokale for prosjektet og har ikke kapasitetsbegrensninger på tvers av prosjekter. |
| Generell prosjektressurs   | En ressursplassholder som gjør det mulig for deg å danne et team og bemanne en prosjektplan uten å måtte vite den navngitte ressursen. Prosjektkalenderen brukes som kalenderen til den generelle ressursen. Du kan legge til generelle ressurser i et prosjektteam og tildele aktiviteter til dem. |
| Bestilte timer               | Ressurs timer er forpliktende mot et prosjekt for å sikre at prosjektarbeidet fullføres. Bestilte timer forbrukes fra ressursens totale kapasitet. Bestillinger er bare mot navngitte ressurser, ikke mot generelle ressurser. |
| Tilordnede timer             | Ressurstimer tildeles aktiviteter i prosjektplanen. Tilordningene kan være enten med navngitte ressurser eller generelle ressurser. Tilordninger kan være uavhengige av bestillinger. |
| Nødvendige timer             | Kapasiteten som er nødvendig, men som ennå ikke er fullført med en navngitt ressurs. Nødvendige timer er bare relevante for generelle teammedlemmer som har generert ressurskrav. |
| Behov                     | Gjeldende og innkommende arbeidsmengde. I Project Service Automation vises behovet som ressurskrav eller ressursforespørsler. |
| Ressurskrav       | En enhet som brukes til å registrere nødvendige timer, start- og sluttdatoer, ferdigheter, geografi og andre prisdimensjoner for de nødvendige ressursene. Ressurskrav er enten generert fra prosjektteammedlemmer eller enkeltvis opprettet. |
| Ressursforespørsel           | En enhetn som brukes som en "konvolutt" for å utføre behovet (ressurskravet) som må oppfylles av en ressursleder. |
| Standard ressursrolle:      | Rollen som en ressurs er gruppert under for utnyttelsesberegning. Ressursen antas å ha nødvendig kompetanse for rollen og oppfyller målutnyttelsen for den rollen. |
| Organisasjonsenhet for ressurs | Organisasjonsenheten som en ressurs er tilordnet til. |
| Profil                    | Oppgave, krav eller tilordningstimer, brutt ned til daglig fordeling. En 5-dagers oppgave på 40 timer kan for eksempel profileres til åtte timer per dag over fem dager. |
| Avstemmingsvisning        | En visning som viser bestillinger og tilordninger for hvert prosjektgruppemedlem. I denne visningen kan prosjektlederen se etter eventuelle manglende samsvar mellom bestillinger og tildelinger, og utføre korrigerende handlinger hvis det oppstår uoverensstemmelser. |
| Arbeidstider                 | En enhet som brukes til å identifisere ressurskapasitet og arbeidstid og ikke-arbeidstid. Denne enheten kalles også ressurskalenderen. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]