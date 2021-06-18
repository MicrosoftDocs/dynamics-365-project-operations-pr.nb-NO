---
title: Opprette en mal for arbeidstimer
description: Dette emnet beskriver hvordan du oppretter en mal for arbeidstimer i Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997208"
---
# <a name="create-a-work-hours-template-project-service"></a>Opprette en mal for arbeidstimer (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Hvis du vil opprette og administrere et prosjekt, må du bruke en kalendermal på prosjektet. Kalendermalen definerer følgende prosjektattributter:

- Arbeidstid, inkludert start- og sluttidspunkt
- Arbeidsdager
- Kalenderunntak, for eksempel fridager

Kalendermalen som brukes på et prosjekt, er en kopi av kalendermalen som er definert i organisasjonens innstillinger.

> [!NOTE]
> Hvis du endrer kalendermalen, overføres ikke disse endringene til arbeidstiden for prosjektet. Hvis du vil endre arbeidstiden for prosjektet, må du bruke en ny mal.

Hvis du vil opprette en kalendermal for organisasjonen, er det to viktige krav:

- Definer ønsket arbeidstid for malen ved hjelp av en ny eller eksisterende ressurs som kan reserveres.
- Opprett en ny kalendermal, og knytt malen til ressursen som kan reserveres.

**Definer arbeidstimene for malen**

1. Gå til **Ressurser** \> **Ressurser**.
2. Opprett en ny ressurs som skal refereres til i kalendermalen, eller velg en eksisterende ressurs.
3. Velg kategorien **Arbeidstimer** for ressursen, og fullfør instruksjonene i [Angi arbeidstimer for en ressurs](/dynamics365/field-service/set-work-hours-resource.md) for å konfigurere kalenderreglene.

**Opprett en ny kalendermal**

1. Gå til **Innstillinger** \> **Kalendermal**.
2. Velg **Ny**, og skriv inn et navn, en beskrivelse og en malressurs.


> [!NOTE]
> Når det refereres til en ressurs i en kalendermal, knyttes en kopi av ressursens kalender til kalendermalen. Hvis arbeidstimene for den kopierte malen endres, overføres ikke disse endringene til kalendermalen.


### <a name="see-also"></a>Se også  
 [Definere ressurser](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
