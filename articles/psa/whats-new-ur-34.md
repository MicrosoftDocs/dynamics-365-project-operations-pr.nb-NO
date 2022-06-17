---
title: Hva er nytt eller endret i Project Service Automation Update Release 34, V3
description: Denne artikkelen viser funksjoner og rettelser i Project Service Automation Update Release 34 V3.
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
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928674"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Hva er nytt eller endret i Project Service Automation Update Release 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å kunngjøre den nyeste oppdateringen for Microsoft Dynamics 365 Project Service Automation-appen. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Den er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, kan du gå til siden for administrasjonssenteret for Dynamics 365 Online-løsninger og installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation V3, Update Release 34. Denne versjonen har et build-nummer på V3.10.55.38 og er allment tilgjengelig via en egenoppdatering i juli 2021.

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
