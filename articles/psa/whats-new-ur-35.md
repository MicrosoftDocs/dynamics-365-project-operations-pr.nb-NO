---
title: Hva er nytt eller endret i Project Service Automation Update Release 35, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelige i Microsoft Dynamics 365 Project Service Automation-oppdateringsutgivelsen 35, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 09/03/2021
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
ms.reviewer: johnmichalak
ms.openlocfilehash: e210777f1e4d149b700721ac7fb9bd129b1166fe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574040"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-35-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 35, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 35, V3. Denne versjonen har et build-nummer på V3.10.56.110 og er tilgjengelig via en egenoppdatering i september 2021.

## <a name="update-release-35"></a>Update Release 35

### <a name="bug-fixes"></a>Feilrettinger

Følgende problemer har blitt løst.

**Tid og utgift**

- Prosjektgodkjenneren mottar en leserettighetsfeil når vedkommende godkjenner utgiftsoppføringer med en **prosjektgodkjennerrolle**.
- Prosjektgodkjenneren mottar en skriverettighetsfeil på **msdyn_projectapproval** når vedkommende annullerer en godkjent tidsoppføring med en **prosjektgodkjennerrolle**.
- Når du velger **Kopier uke** i en tidsoppføring i Dynamics 365 for telefon – Prosjektressurshub-appmodulen, oppstår følgende feil: ...\OfficeProductivity_RibbonRules.js.map: HTTP error: status code 404, net::ERR_HTTP_RESPONSE_CODE_FAILURE.
- Policyen for **nytt forsøk** godkjenner automatisk oppføringer som tidligere ble avvist.
- Delskjemaet **Godkjenningssett** viser båndhandlinger som ikke gjelder.
- Det mangler ikoner for **Prosjektoppgave** og **Ressursrolle** i enheten **Tidsoppføring**.
- Når du importerer ressurstilordninger, har ikke de importerte tidsoppføringene riktig varighet for tildelinger som er opprettet ved hjelp av oppgaver i manuell modus.
- **Slett** mangler på oppføringssiden **Avansert søk etter tidsoppføringer**.
- **Lagre** mangler på siden **Informasjon om tidsoppføring**. Dette problemet hindrer at endringer lagres når siden lukkes.

**Prosjektplanlegging**

- Rutenettene **Ressurstilordning** og **Ressursavstemming** sorterer ikke grupperte attributter alfabetisk.
- Oppgaver kan ikke opprettes hvis datofunksjonaliteten er tilpasset til **Bare dato**.

**Ressursstyring**

- Hvis både Dynamics 365 Field Service og Project Service Automation er installert, oppstår overlappingsproblemer når **tilknyttet visning for ressurskrav** er knyttet til en hovedside.
- Hvis du dobbeltklikker på **Lagre** i dialogboksen **Hurtigoppretting av teammedlem**, forhindres ressurskravet fra å bli opprettet.

**Salg**

- Det opprettes et unntak hvis du sletter en oppgave som er knyttet til et tilbud som har statusen **Vunnet**.
