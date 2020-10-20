---
title: Registrer deg for et forhåndsversjonsbonnement
description: Dette emnet gir informasjon om hvordan du abonnerer på og distribuerer Lite-distribusjon i Project Operations – avtale til proformafakturering.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948999"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Registrer deg for et forhåndsversjonsabonnement for Lite-distribusjon – avtale til proformafakturering

Dette eforklarer hvordan du abonnerer på tilbudet om forhåndsversjon for partnere og distribuerer Lite-distribusjon i Dynamics 365 Project Operations – avtale til proformafakturering.

> [!NOTE]
> Denne prosessen vil endres i kommende versjoner av Project Operations.

## <a name="prerequisites"></a>Forutsetninger

- Du vil motta en e-post som inviterer deg til å delta i forhåndsversjonen. Du kan be om en forhåndsversjon på [Project Operations-nettstsedet](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Brukeren som distribuerer forhåndsversjonen, må ha globale administratorrettigheter for Azure-leieren.
- Brukeren som distribuerer forhåndsversjonen, må ha et telefonnummer og et gyldig kredittkort. Under registreringen påløper ingen gebyrer for kortet i seks måneder. Etter seks måneder må du stoppe abonnementet. 
- Gå gjennom alle vilkår.

## <a name="subscribe"></a>Abonner

Når du mottar en [forespørsel om godkjenning av forhåndsversjon](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), får du to tilbud fra Microsoft via e-post. Med disse tilbudene kan du distribuere forhåndsversjonen av Project Operations:

- Forhåndsversjon av Dynamics 365 Customer Service – kode for éngangsbruk
- Dynamics 365 Project Operations – forhåndsversjon

### <a name="dynamics-365-customer-service-paid-offer"></a>Betalt tilbud på Dynamics 365 Customer Service

1. Ved hjelp av et InPrivate-eller inkognito nettleservindu kan du løse inn den første tilbudskoden for Dynamics 365 Customer Service. Hvis du vil registrere deg for Customer Service, trenger du følgende:

- Et telefonnummer
- Et kredittkort. Når du registrerer deg, påløper ingen gebyrer for kortet i seks måneder. Etter seks måneder må du stoppe abonnementet.
- Gå gjennom alle vilkår.

2. Oppgi kontaktinformasjonen din.

![Informasjon om kontakt](./media/1ContactInformation.png)

3. Oppgi de nye leierdetaljene.

![Opprett bruker-ID](./media/2CreateUserID.png)

4. Kontroller identiteten din, lagre den nye bruker-ID-en, og velg deretter **Konfigurer**.

![Lagre informasjon](./media/3SaveInfo.png)

5. Fullfør kredittkortregistreringen, og se gjennom alle betingelser. 

![Fullfør kredittkort](./media/4CompleteCreditCard.png)

![Kredittkortbetaling](./media/5CreditCardCheckout.png)

![Lagre ordre](./media/6SaveOrder.png)

![Kredittkortinformasjon](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Avbryt Dynamics 365 Customer Service Enterprise-tilbudet

Dynamics 365 Customer Service Enterprise-tilbudet er gratis i seks måneder. Tilbudet fornyes til full pris ved slutten av perioden på seks måneder. Hvis du vil annullere før fornyelsesdatoen, følger du instruksjonene nedenfor. 

> [!NOTE]
> Når du har fullført disse trinnene, vil du ikke lenger kunne bruke det offentlige forhåndsvisningsmiljøet i Project Operations.

1. Gå til [administrasjonsportalen](https://admin.microsoft.com/). Under **Fakturering** velger du **Dine produkter**.

![Administrasjonsportalen, siden Dine produkter](./media/8AdminPortal.png)

2. Velg **Dynamics 365 Customer Service Enterprise-tilbudet**.

![Stoppe abonnementet](./media/9CancelSubscription.png)

3. Velg **Innstillinger** > **Handlinger** > **Stopp abonnement**.
4. På skjemaet **Abonnementsavslutning** angir du informasjon i de obligatoriske feltene.
5. Velg **Avbryt** > **Abonnement.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations – forhåndsversjon

1. Løs inn det andre tilbudet, prøveversjonen av Dynamics 365 Project Operations, med URL-adressen fra e-postmeldingen.

![Løse inn tilbud 2](./media/10RedeemOffer2.png)

2. Kontroller at du er logget på som brukeren som tilhører den samme organisasjonen som abonnerte ved hjelp av den første tilbudskoden, og fortsett deretter med å løse inn tilbudet. 
3. Velg **Ja, Legg det til på kontoen min**.

![Legg til på konto](./media/11AddToAccount.png)

![Prøv nå-skjermen](./media/12TryNow.png)

![Ordredetaljer](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Tilordne lisenser

> [!IMPORTANT]
> Du må ha administrativ tilgang til organisasjonens Office 365-portal for å kunne utføre følgende trinn.

1. Gå til [administrasjonssenteret for Microsoft 365](https://portal.office.com/) for å tilordne lisensene til brukerne dine.

![Startsiden for administrasjonssenteret](./media/14AdminPortal.png)

2. På siden **Aktive brukere** velger du brukerne du vil tilordne en lisens til.

![Tilordne lisenser](./media/15AssignLicenses.png)

3. Kontroller at **Customer Service Enterprise**- og **Project Operations**-lisensen er valgt, og velg **Lagre endringer**.

## <a name="create-a-new-cds-environment"></a>Opprett et nytt CDS-miljø

Klargjør et nytt Project Operations CDS-distribusjonsmiljø ved å følge instruksjonene i emnet [CDS-distribusjonsmodell](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Installer en CDS-konfigurasjon og konfigurer demodata

Installer CDS-konfigurasjonen og konfigurer demodata ved å følge instruksjonene i emnet [Bruk demonstrasjonsoppsett og konfigurasjonsdata](lite-apply-demo-setup-config-data.md).
