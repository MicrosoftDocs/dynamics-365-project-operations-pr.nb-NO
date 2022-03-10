---
title: Oppdatere programtilleggattributter med nye prisdimensjoner
description: Dette emnet gir informasjon om hvordan du oppdaterer programtilleggattributter for prisdimensjoner.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988348"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Oppdatere programtilleggattributter med nye prisdimensjoner

Dette emnet gir informasjon om hvordan du oppdaterer programtilleggattributter for prisdimensjoner.

> [!NOTE]
> Dette emnet gjelder bare for tilbuds- og kontraktfunksjonene i Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Forutsetninger
Før du fullfører trinnene i dette emnet, må du fullføre prosedyrene i følgende emner:

  - [Opprette egendefinerte felt og enheter](create-custom-fields-entities-pricing-dimensions.md) 
  - [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter ](add-custom-fields-price-setup-transactional-entities.md)
  - [Konfigurere egendefinerte felt som prisdimensjoner](set-up-custom-fields-pricing-dimensions.md). 
  
Hvis du ikke har fullført disse prosedyrene, kan du fullføre dem og deretter gå tilbake til dette emnet.

## <a name="register-a-plug-in"></a>Registrer et programtillegg
Når det blir opprettet en tilbudslinjedetalj på **Tilbudslinje**-siden for en tilbudslinje for prosjektet, oppretter systemet to estimatlinjer. Én linje gjelder for kostnadssiden for estimatet, og den andre linjen er for salgssiden. Dette er det samme for prosjektkontraktlinjer.

Når du gjør en endring i antallet eller et felt på kostnadssiden, overføres endringen også til salgssiden. Dette er mulig fordi PreOperation-programtilleggene på Quotelinedetail og kontraktlinjedetalj-enheter kobler bestemte attributter på kostnadssiden til salgssiden av transaksjonen. Hvis du trenger at endringer som er gjort på prisdimensjonsverdiene på salgssiden også blir gjort på kostnadssiden, må du også registrere følgende tilleggsprogrammer på nytt etter at du har gjort endringer i en prisdimensjon.

Dette er tilleggsprogrammene som skal oppdateres og registreres på nytt:

- PreOperationContractLineDetailUpdate – **Oppdater msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate – **Oppdaterer msdyn_quotelinetransaction**

Fullfør fremgangsmåten nedenfor for å oppdatere og registrere programtilleggene på nytt.

1. Åpne **PluginRegistrationTool** og koble til Project Operations Dataverse-miljøet.
2. Velg **Søk**, og skriv inn de første bokstavene i programtillegget som skal oppdateres.
3. Når programtillegget er funnet, velger du den, og deretter velger du **Velg på hovedskjema**.
4. Velg **Update msdyn_orderlinetransaction**-trinnet, høyreklikk og velg deretter **Oppdater**.
5. I **Oppdatering**-dialogbokssiden velger du ellipsen (**...**) i filtreringsattributtene.
6. Vinduet for filtreringsattributter åpnes og gir en liste over alle attributtene i enheten og prisdimensjonene. Velg avmerkingsboksene for prisdimensjonsattributtene.
7. Velg **OK** for å lukke siden, og velg deretter **Oppdater trinn**.
8. Gjenta trinn 2 til 7 for det andre programtillegget, **PreOperationQuoteLineDetail**. For dette programtillegget må du oppdatere, **Oppdatering av msdyn_quotelinetransaction**-trinnet.
9. Lukk **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]