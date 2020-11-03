---
title: Registrer deg for et forhåndsversjonsbonnement
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5342466f308ab62a9f73a85fbd838d7c33bb1f47
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081483"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Registrer deg for et forhåndsversjonsabonnement for Lite-distribusjon – avtale til proformafakturering

Dette eforklarer hvordan du abonnerer på tilbudet om forhåndsversjon for partnere og distribuerer Lite-distribusjon i Dynamics 365 Project Operations – avtale til proformafakturering.

> [!NOTE]
> Denne prosessen vil endres i kommende versjoner av Project Operations.

## <a name="prerequisites"></a>Forutsetninger

- Du vil motta en e-post som inviterer deg til å delta i forhåndsversjonen. Du kan be om en forhåndsversjon på [Project Operations-nettstsedet](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.
- Gå gjennom alle vilkår.

## <a name="subscribe"></a>Abonner

Når du mottar en [forespørsel om godkjenning av forhåndsversjon](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), får du to tilbud fra Microsoft via e-post. Med disse tilbudene kan du distribuere forhåndsversjonen av Project Operations:

- Dynamics 365 Project Operations (CRM) – forhåndsversjon
- Office 365 Project Operations – forhåndsversjon

> [!IMPORTANT]
> Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven. Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) – forhåndsversjon 

Før du begynner, må du forsikre deg om at du er logget på en nettleser med brukerarbeidskontoen i leieren der du vil ha forhåndsversjonen av Project Operations.

1. Løs inn den første tilbudskoden, **Dynamics 365 Project Operations (CRM) – forhåndsversjon** ved å lime den inn i URL-adressen i nettleseren.

![Løs inn tilbud](./media/16RedeemFirstOfferNew.png)

2. Bekreft ordren.
![Bekreft ordren](./media/17ConfirmOrderNew.png)

Du ser en bekreftelse på at tilbudet ble løst inn.

![Bekreftelse](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations – forhåndsversjon

Gjenta de samme trinnene som med den første tilbudskoden. Pass på at du legger til den andre tilbudskoden ved hjelp av den samme brukerkontoen som ble brukt med første tilbudskode.

## <a name="assign-licenses"></a>Tilordne lisenser

> [!IMPORTANT]
> Du må ha administrativ tilgang til organisasjonens Microsoft 365-portal for å kunne utføre følgende trinn.


1. Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisensene til brukerne dine.

![Startsiden for administrasjonssenteret](./media/14AdminPortal.png)

2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.

![Tilordne lisenser](./media/15AssignLicenses.png)

3. Kontroller at lisensene **Dynamics 365 Project Operations (CRM) – forhåndsversjon** og **Office 365 Project Operations – forhåndsversjon** er valgt. 
4. Velg **Lagre endringer**.

## <a name="create-a-new-cds-environment"></a>Opprett et nytt CDS-miljø

1. Klargjør et nytt Project Operations CDS-distribusjonsmiljø ved å følge instruksjonene i emnet [CDS-distribusjonsmodell](lite-deployment.md). Når du velger miljøtypen, må du passe på å bruke **Prøveversjon (abonnementsbasert)**.
![Nytt miljø](./media/19CreateEnvironment.png)

2. Velg innstillingen **Enable Dynamics 365-apper** , og la **Distribuer disse appene automatisk** stå tomt.  
3. Velg **Lagre** for å opprette miljøet.

![Legg til database](./media/20CreateEnvironment1.png)

4. Når du har opprettet miljøet, installerer du **Microsoft Dynamics 365 Project Operations** -løsningen. 

![Installere løsning](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfigurasjon og konfigurer demodata

Installer CDS-konfigurasjonen og konfigurer demodata ved å følge instruksjonene i emnet [Bruk demonstrasjonsoppsett og konfigurasjonsdata](lite-apply-demo-setup-config-data.md).
