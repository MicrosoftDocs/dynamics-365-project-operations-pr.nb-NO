---
title: Registrer deg for et forhåndsversjonsbonnement – Lite
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334794"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registrer deg for et forhåndsversjonsbonnement – Lite 

Dette emnet forklarer hvordan du abonnerer på prøveversjonstilbudet og distribuerer Dynamics 365 Project Operations Lite distribusjon – avtale til proformafakturering.

> [!NOTE]
> Denne prosessen vil endres i kommende versjoner av Project Operations.

## <a name="prerequisites"></a>Forutsetninger
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren. Du kan opprette en leier i løpet av den første innløsningen av tilbudet.

> [!IMPORTANT]
> Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven. Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.
> 
> Prøveversjoner er enkeltbruk i leieren. Du kan bare kjøre en prøveversjon én gang. Vi anbefaler at du oppretter en ny leier i forbindelse med prøveversjonen.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations-prøveversjon 

Før du begynner, må du forsikre deg om at du er logget på en nettleser med brukerarbeidskontoen i leieren der du vil ha forhåndsversjonen av Project Operations.

1. Gå til [Project Operations-prøveversjon](https://aka.ms/try-po) for å løse inn den første tilbudskoden, **Dynamics 365 Project Operations**.
2. Bekreft ordren.

  Du ser bekreftelsen på at tilbudet er innløst.

## <a name="assign-licenses"></a>Tilordne lisenser

> [!IMPORTANT]
> Du må ha administrativ tilgang til organisasjonens Microsoft 365-portal for å kunne utføre følgende trinn.


1. Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisensene til brukerne dine.
2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.
3. Kontroller at **Dynamics 365 Project Operations**-lisensen er valgt. 
4. Velg **Lagre endringer**.

## <a name="create-a-new-dataverse-environment"></a>Opprett et nytt Dataverse-miljø

1. Klargjør et nytt Project Operations Dataverse-distribusjonsmiljø ved å følge instruksjonene i emnet [Dataverse-distribusjonsmodell](lite-deployment.md). Når du velger miljøtypen, må du passe på å bruke **Prøveversjon (abonnementsbasert)**.

  ![Nytt miljø](./media/19CreateEnvironment.png)

2. Velg innstillingen **Enable Dynamics 365-apper**, og la **Distribuer disse appene automatisk** stå tomt.  
3. Velg **Lagre** for å opprette miljøet.

  ![Legg til database](./media/20CreateEnvironment1.png)

4. Når miljøet er opprettet, installerer du **Microsoft Dynamics 365 Project Operations**-løsningen. 

![Installere løsning](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfigurasjon og konfigurer demodata

Installer CDS-konfigurasjonen og konfigurer demodata ved å følge instruksjonene i emnet [Bruk demonstrasjonsoppsett og konfigurasjonsdata](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
