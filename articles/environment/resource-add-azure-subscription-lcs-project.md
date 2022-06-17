---
title: Legg til et Azure-abonnement i et LCS Project
description: Denne artikkelen inneholder informasjon om hvordan du kobler Azure-abonnementet til et LCS-prosjekt.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912160"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Legg til et Azure-abonnement i et LCS Project

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Skydriftede miljøer må distribueres ved hjelp av et eksisterende Azure-abonnement. Denne artikkelen forklarer hvordan du kobler det eksisterende Azure-abonnementet til et LCS-prosjekt. 

## <a name="grant-admin-consent"></a>Gi admin-tillatelse

1. I LCS-prosjektet, i **Miljøer**-delen velger du **Microsoft Azure-innstillinger**.

![Innstillinger for Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. På siden **Prosjektinnstillinger** i kategorien **Azure-kontakter** velger du **Autoriser**. Dette gjør det mulig å distribuere miljøer til dette prosjektet.

![Azure-koblinger.](./media/2AzureConnectors.png)

3. Velg **Autoriser** på nytt for å gi administratorsamtykke.

![Gi admin-tillatelse.](./media/3GrantAdminConsent.png)

4. Godta tillatelsesforespørselen.

![Godta tillatelsesforespørsel.](./media/4AcceptPermissionRequest.png)

Autorisasjonen er nå fullført. 

![Autorisasjon vellykket.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Gi Dynamics Deployment Services tilgang til Azure-abonnementet

1. Gå til [Microsoft Azure-fakturering](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade), og velg abonnementet ditt. Dynamics Deployment Services må ha tilgang til dette abonnementet for å kunne distribuere miljøer.

![Azure-abonnementsdetaljer.](./media/6AzureSubscription.png)

2. Velg **Tilgangskontroll (IAM)** i navigasjonsruten, og velg deretter **Legg til rolletildeling**.
3. På glidebryteren til høyre velger du **Bidragsyterroller**, og finn og velg **Dynamics Deployment Services** i listen som vises. 
4. Velg **Lagre**.

![Abonnementstilgang.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Legg til en abonnementskontakt i et LCS Project

1. I LCS-prosjektet, på siden **Microsoft Azure-innstillinger**, velger du **Legg til** for å legge til en ny kontakt.
2. Skriv inn Azure abonnements-ID-en din. Du finner Azure-abonnements-ID-en i [Azure-portalen](https://ms.portal.azure.com/), under **Innstillinger** nederst til venstre på skjermen.
3. I feltet **Konfigurer for å bruke Azure Resource Manager** velger du **Ja**.
4. Kontroller at Azure-abonnementets AAD-leierdomene samsvarer med det domeneeiende Azure-abonnementet du bruker, og velg **Neste**.
5. På skjermen **Microsoft Azure-oppsett** velger du **Neste** for å bekrefte. Hvis du får en feil på denne skjermen, går du tilbake til delen [Gi Dynamics-distribusjonstjenester tilgang til Azure-abonnement](#provide) i denne artikkelen og kontrollerer at du har fullført alle trinnene.
6. Last ned Azure Management-sertifikatet til en lokal mappe på datamaskinen. Be administrator for Azure-abonnementet ditt om å laste opp sertifikatet til Azure Management-portalen ved å velge abonnementet og gå til **Innstillinger** > **Administrasjonssertifikater**. Dette sertifikatet gjør det mulig for LCS å kommunisere med Azure på dine vegne. Du kan hoppe over dette trinnet hvis brukeren har tilgang til abonnementet.
7. Velg **Neste**.
8. Velg Azure-området du skal distribuere i, og velg et datasenter som er nær stedet der du vil bruke dette systemet.
9.  Velg **Koble til**.

Du har koblet til Azure-abonnementet. Du kan nå distribuere skybaserte Dynamics 365 Finance-miljøer.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
