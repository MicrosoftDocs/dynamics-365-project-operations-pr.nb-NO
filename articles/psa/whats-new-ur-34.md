---
title: Hva er nytt eller endret i Project Service Automation Update Release 34, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588702"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 34. Denne versjonen har et build-nummer på V3.10.55.38 og er allment tilgjengelig via en egenoppdatering i juli 2021.

## <a name="update-release-34"></a>Update Release 34

### <a name="bug-fixes"></a>Feilrettinger
Følgende problemer har blitt løst.

**Generelt**

- Utgiverdrevne oppdateringer aktiverer ikke den nye arbeidsflyten for moderne godkjenning.
- Attributtene **Målstatus** og **Handlingstype** mangler på hovedsiden for **godkjenningssettet**.

**Tid og utgift**

- Kan ikke godkjenne en forespørsel om tilbakekalling ved hjelp av den moderne godkjenningsflyten.
- Kopiering av en uke med tidsoppføringer fungerer ikke når du kopierer oppføringer som ikke er relatert til den innloggede brukeren.

**Prosjektplanlegging**

- Ressurstilordningskonturer er skadet under import fra tilleggsprogrammet for Microsoft Microsoft Project-skrivebordet.

**Ressursstyring**

- Når du publiserer et prosjekt fra klienttillegget for Microsoft Project-skrivebordet, endres sluttdatoen for eksisterende krav.
- Desimalpresisjon overskrider to desimalplasser i bekreftelsesdialogboksen for utvidelse av bestillinger.

**Salg**

- Når du legger til en produktbasert linje med et eksisterende produkt i en prosjektkontrakt, vises **en nøkkel som ikke finnes i ordlisteunntaket**.
- Kundeemner kan ikke kvalifiseres når en ordretype tilordnes fra et kundeemne til en salgsmulighet.
