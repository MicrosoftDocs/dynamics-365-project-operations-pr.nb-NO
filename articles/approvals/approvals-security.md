---
title: Sikkerhet og godkjenninger
description: Denne artikkelen inneholder informasjon om sikkerhetsoppsettet for arbeid med godkjenninger i Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841936"
---
# <a name="security-and-approvals"></a>Sikkerhet og godkjenninger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Microsoft Dynamics 365 Project Operations bruker to sikkerhetsroller for å tillate godkjenning av tids-, utgifts- og materialeoppføringer:

- Prosjektgodkjenner
- Prosjektgodkjenneradministrator

## <a name="project-approver"></a>Prosjektgodkjenner

Du må ha sikkerhetsrollen **Prosjektgodkjenner** for å godkjenne tids-, utgifts- og materialeoppføringer i prosjektet. Du må også ha tilgang til de relevante relaterte enhetene, for eksempel **Prosjekt**. Denne tilgangen kan tilordnes av en person som har rollen **Prosjektleder**. I tillegg må du være teammedlem i prosjektet og merket som godkjenner.

For godkjenning av ikke-prosjektoppføringer må du være en overordnet for innsenderen.

## <a name="project-approver-admin"></a>Prosjektgodkjenneradministrator

> [!NOTE]
> Funksjonen [Godkjenningssett](approval-sets.md) må være aktivert før du kan bruke funksjonen Prosjektgodkjenneradministrator.

Med sikkerhetsrollen **Prosjektgodkjenneradministrator** kan brukere omgå policyer og tillate godkjenning av oppføringer på tvers av alle prosjekter. Tilordning av denne rollen vil omgå valideringslogikken som krever teammedlemskap og at brukeren er merket som godkjenner. Du må ha tilgang til de relevante relaterte tabellene, for eksempel **Prosjekt**, via sikkerhetsroller som er tilordnet til deg.

SYSTEM-brukerkonteksten omgår valideringer på samme måte som sikkerhetsrollen Prosjektgodkjenneradministrator.
