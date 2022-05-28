---
title: Distribuere Project Operations – Lite
description: Dette emnet gir informasjon om hvordan du installerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580744"
---
# <a name="deploy-project-operations---lite"></a>Distribuere Project Operations – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_



Project Operations støtter flere distribusjonsmodeller. Hvis du vil finne den beste distribusjonsmodellen, kan du se [Distribusjonstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Denne distribusjonen, Lite-distribusjon – avtale til proformafakturering, fører til en **distribusjon av Project Operations bare med Dataverse**.

- [Installer Project Operations i et nytt Dataverse-miljø](#new)
- [Installer i et eksisterende Dataverse-miljø](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations i et nytt Dataverse-miljø

1. Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens oppretter du et nytt Dataverse-miljø i [PowerPlatform-administrasjonssenteret](https://admin.powerplatform.com). Kontroller at **Opprett en database for dette miljøet** og **Dynamics 365 Apps** er aktivert. Hvis du vil ha mer informasjon, kan du se [Opprette og administrere miljøer i Power Platform-administrasjonssenteret](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Velg **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations i et eksisterende Dataverse-miljø
1. Kontroller at miljøet ikke er konfigurert med [dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), siden installasjonen da vil installere [Project Operations-funksjoner for ressursbaserte/ikke-lagerbaserte scenarioer](project-operations-integrated-deployment-overview.md).
2. Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.
3. Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper. Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
