---
title: Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9094b6928c5c276a40166ef5d8cb0facb539685b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575822"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_



Dette emnet forklarer hvordan du abonnerer på prøveversjonstilbudet og distribuerer Project Operations-miljøet for ressursbaserte/ikke-lagerbaserte scenarioer.

## <a name="prerequisites"></a>Forutsetninger
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren. Du kan opprette en leier i løpet av den første innløsningen av tilbudet. 
- Distribusjon av et Finance-miljø krever et gyldig Azure-abonnement som blir fakturert per miljø. Du kan bruke organisasjonens eksisterende abonnement eller bruke en [Azure-prøveversjon](https://azure.microsoft.com/free/) for å komme i gang. CDS-miljøet tilbys gratis i en begrenset periode på 30 dager.

> [!IMPORTANT]
> Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven. Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.
> 
> Prøveversjoner er enkeltbruk i leieren. Du kan bare kjøre en prøveversjon én gang. Vi anbefaler at du oppretter en ny leier i forbindelse med prøveversjonen.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) – forhåndsversjonsprøveversjon 

Før du begynner, må du forsikre deg om at du er logget på en nettleser med brukerarbeidskontoen i leieren der du vil ha forhåndsversjonen av Project Operations.

1. Bruk koden for første tilbud, **Dynamics 365 Project Operations** [her: Project Operations-prøveversjon](https://aka.ms/try-po).
2. Bekreft ordren.

  Du ser en bekreftelse på at tilbudet ble løst inn.

### <a name="dynamics-365-finance-preview-trial"></a>Prøveversjon av Dynamics 365 Finance-forhåndsversjon

Gå til [Prøveversjon av Dynamics 365 for Finance-forhåndsversjon](https://aka.ms/trypoche), og gjenta trinnene fra forrige del med tilbudet, Registrer deg for det skybaserte miljøet.  

## <a name="assign-licenses"></a>Tilordne lisenser

> [!IMPORTANT]
> Du må ha administrativ tilgang til organisasjonens Microsoft 365-portal for å kunne utføre følgende trinn.

1. Gå til [Microsoft 365-administrasjonssenteret](https://portal.office.com/) for å tilordne lisensene til brukerne.

2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.

3. Kontroller at **Dynamics 365 Project Operations**-lisensen er valgt, og velg **Lagre endringer**.

> [!NOTE]
> Prøvetilbudet på Finance trenger ikke tilordnes til en bruker.

## <a name="start-a-new-project-in-lcs"></a>Start et nytt prosjekt i LCS

Opprett et nytt LCS-prosjekt slik det er beskrevet i emnet [Start et nytt prosjekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Legg til et Azure-abonnement i et LCS Project

For å fullføre denne oppgaven må du følge fremgangsmåten i emnet [Legg til et Azure-abonnement i et LCS-prosjekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuer Finance-demonstrasjonsmiljø med Project Operations for scenarioer for ressursbaserte/ikke-lagerførte scenarioer

Følg veiledningen i emnet [Klargjør et nytt miljø](resource-provision-new-environment.md) for å fullføre distribusjonen. Bruk distribusjonstypen [demonstrasjonsmiljø](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) for forhåndsversjonen. 

## <a name="install-cds-setup-and-configuration-data"></a>Installer CDS-oppsett og konfigurasjonsdata

Installer CDS-oppsett og konfigurasjonsdata slik det er beskrevet i emnet [Konfigurer og bruk konfigurasjonsdata i Common Data Service](resource-apply-pro-setup-config-data.md).
Fullfør dette trinnet først etter at Finance-demomiljøet er distribuert og demodata er klare.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
