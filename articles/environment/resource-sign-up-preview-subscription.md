---
title: Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Project Operations for ressursbaserte/ikke-lagerførte scenarioer.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949002"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrer deg for forhåndsversjonsabonnementer på Project Operations for ressursbaserte/ikke-lagerførte scenarioer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet forklarer hvordan du abonnerer på tilbudet om forhåndsversjon/partner og distribuerer Project Operations-miljøer for ressursbaserte/ikke-lagerførte scenarioer.

## <a name="prerequisites"></a>Forutsetninger

- Du vil motta en e-post som inviterer deg til å delta i forhåndsversjonen. Du kan be om en forhåndsversjon på [Project Operations-nettstsedet](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.
- Distribusjon av et Finance-miljø krever et gyldig Azure-abonnement som blir fakturert per miljø. Du kan bruke organisasjonens eksisterende abonnement eller bruke en [Azure-prøveversjon](https://azure.microsoft.com/en-us/free/) for å komme i gang. CDS-miljøet tilbys gratis i en begrenset periode på 30 dager.

## <a name="subscribe"></a>Abonner

Når [forespørselen din om forhåndsversjon](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) er godkjent, får du to tilbud fra Microsoft via e-post. Med disse tilbudene kan du distribuere forhåndsversjonen av Project Operations:

- Dynamics 365 Project Operations – forhåndsversjon
- Dynamics 365 for Finance and Operations – forhåndsversjon.

> [!IMPORTANT]
> Bare én person, leieradministratoren, i en organisasjon trenger å utføre denne oppgaven. Hvis det ikke er du som er abonnent for denne versjonen, må du vente til organisasjonen har registrert seg og du har mottatt brukerlegitimasjonen.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – forhåndsversjon

1. Løs inn det første tilbudet, **prøveversjonen av Dynamics 365 Project Operations**, med URL-adressen fra e-postmeldingen.

![Første tilbud](./media/1FirstOffer.png)

2. Kontroller at du er logget på som brukeren som tilhører organisasjonen, og som skal abonnere på tjenesten.
3. Fortsett med å løse inn tilbudet. 
4. Velg **Ja, Legg det til på kontoen min**.

![Løs inn tilbud](./media/2RedeemFirstOffer.png)

![Bekreft tilbud](./media/3ConfirmFirstOffer.png)

![Tilbud løst inn](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance – forhåndsversjon

Gjenta de samme trinnene med det andre tilbudet fra e-postmeldingen.

## <a name="assign-licenses"></a>Tilordne lisenser

> [!IMPORTANT]
> Du må ha administrativ tilgang til organisasjonens Office 365-portal for å kunne utføre følgende trinn.

1. Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisenser til brukerne dine.

![Administrasjonsportal for Office](./media/5OfficeAdminPortal.png)

2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.

![Tilordne lisenser](./media/6AssignLicenses.png)

3. Kontroller at Project Operations-lisensen er valgt, og velg **Lagre endringer**. 

> [!NOTE]
> Prøvetilbudet på Finance trenger ikke tilordnes til en bruker.

## <a name="start-a-new-project-in-lcs"></a>Start et nytt prosjekt i LCS

Opprett et nytt LCS-prosjekt slik det er beskrevet i emnet [Start et nytt prosjekt i LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Legg til et Azure-abonnement i et LCS Project

For å fullføre denne oppgaven må du følge fremgangsmåten i emnet [Legg til et Azure-abonnement i et LCS-prosjekt](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Distribuer Finance-demonstrasjonsmiljø med Project Operations for scenarioer for ressursbaserte/ikke-lagerførte scenarioer

Følg veiledningen i emnet [Klargjør et nytt miljø](resource-provision-new-environment.md) for å fullføre distribusjonen. Bruk distribusjonstypen [demonstrasjonsmiljø](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) for forhåndsversjonen.

## <a name="install-cds-setup-and-configuration-data"></a>Installer CDS-oppsett og konfigurasjonsdata

Installer CDS-oppsett og konfigurasjonsdata slik det er beskrevet i emnet [Konfigurer og bruk konfigurasjonsdata i Common Data Service](resource-apply-pro-setup-config-data.md).

