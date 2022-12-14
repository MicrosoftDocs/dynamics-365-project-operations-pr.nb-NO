---
title: Distribuer Project Operations Lite
description: Denne artikkelen inneholder informasjon om hvordan du installerer Project Operations Lite-distribusjon – avtale til proformafakturering.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810991"
---
# <a name="deploy-project-operations-lite"></a>Distribuer Project Operations Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_



Project Operations støtter flere distribusjonsmodeller. Hvis du vil finne den beste distribusjonsmodellen, kan du se [Distribusjonstyper](determine-deployment-type.md).


> [!IMPORTANT]
> Denne distribusjonen, Lite-distribusjon – avtale til proformafakturering, fører til en **distribusjon av Project Operations bare med Dataverse**.

- [Installer Project Operations i et nytt Dataverse-miljø](#new)
- [Installer i et eksisterende Dataverse-miljø](#existing)
- [Installer i et eksisterende Dataverse-miljø som har komponenter for dobbel skriving](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>Installer Project Operations Lite i et nytt Dataverse-miljø

1. Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens oppretter du et nytt Dataverse-miljø i [PowerPlatform-administrasjonssenteret](https://admin.powerplatform.com). Kontroller at **Opprett en database for dette miljøet** og **Dynamics 365 Apps** er aktivert. Hvis du vil ha mer informasjon, kan du se [Opprette og administrere miljøer i Power Platform-administrasjonssenteret](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Velg **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>Installer Project Operations Lite i et eksisterende Dataverse-miljø 
1. Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.
1. Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper. Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a>Installer Project Operations Lite i et eksisterende Dataverse-miljø der løsninger for dobbel skriving allerede finnes

Hvis du vil fortsette å kjøre Project Operations i modusen Lite-distribusjon, bør du følge denne fremgangsmåten:

1. Som [global eller Power Platform-administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) med en Project Operations-lisens finner du miljøet i [administrasjonssenteret for Power Platform](https://admin.powerplatform.com) der du ønsker å installere Project Operations.
1. Installer **Microsoft Dynamics 365 Project Operations** fra distribusjonslisten over Dynamics 365-apper. Hvis du vil ha mer informasjon, kan du se [Administrere Dynamics 365-apper](/power-platform/admin/manage-apps).
1. Siden miljøet har installerte komponenter for dobbel skriving som bidrar til integrering med økonomi- og driftsapper, installerer en installasjon av Project Operations også funksjonene og utvidelsene som kreves for å integrere prosjektrelaterte data i økonomi- og driftsapper. Siden du ønsker å kjøre Project Operations i Lite-distribusjon, fjerner du disse integreringskomponentene fordi de fører til begrensninger og indirekte kostnader i scenarioer med Lite-distribusjon. Avinstaller løsningene **Dobbel skriving i Dynamics 365 Project Operations** og **Enhetstilordninger for dobbel skriving i Dynamics 365 Project Operations** for å fjerne disse komponentene.
1. Gå til **Project Operations -> Innstillinger -> Parametere**. Åpne detaljsiden **Prosjektparameter**, og sett feltet **Virkemåte for løsningsoppgradering** til **Bare Lite**. Dette sikrer at påfølgende oppgraderinger av Project Operations ikke bringer integreringskomponentene tilbake i Project Operations.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
