---
title: Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner
description: Dette emnet inneholder informasjon om hvordan du oppdaterer plugin-attributter for prisdimensjoner.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988798"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Oppdater plugin-attributter slik at de inkluderer nye prisdimensjoner

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Hvis du ikke bruker tilbuds- og kontraktfunksjonene i Project Service Automation, kan du hoppe over dette emnet.

Dette emnet forutsetter at du har fullført prosedyrene i emnene [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md), [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md) og [Konfigurere egendefinerte felt som prisdimensjoner](set-up-pricing-dimensions.md). Hvis du ikke har utført disse prosedyrene, kan du gå tilbake og fullføre dem og deretter gå tilbake til dette emnet.

Når det blir opprettet en tilbudslinjedetalj på siden **Tilbudslinje** for en prosjekttilbudslinje, oppretter systemet to estimatlinjer i bakgrunnen – én linje for kostnadssiden for estimatet og én for salgsiden. Dette er det samme for prosjektkontraktlinjer.

Når du gjør en endring i antallet eller et felt på kostnadssiden, overføres endringen til salgsiden. Dette kan skyldes at følgende plugin-moduler må registreres på nytt etter at du har endret prisdimensjoner.

- PreOperationContractLineDetailUpdate – oppdaterer **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – oppdaterer **msdyn_quotelinetransaction**.

Fremgangsmåten nedenfor forklarer hvordan du registrerer plugin-modulene.

1. Åpne **PluginRegistrationTool**, koble til forekomsten på nettet.
2. Klikk **Søk**, og søk etter plugin-modulen som du vil oppdatere.

 ![Skjermbilde av søketreet.](media/PRT-1.png)

3. Når plugin-modulen er funnet, velger du den, og deretter klikker du **Velg i hovedskjema**.

4. Velg trinnet i plugin-modulen som skal oppdateres, høyreklikk, og velg deretter **Oppdater**.

 ![Skjermbilde av plugin-modulen som skal oppdateres.](media/PRT-2.png)
 
5. I oppdateringsvinduet klikker du på ellipsen (**...**) i filtreringsegenskapene.

 ![Skjermbilde av konfigurasjonsinformasjon for oppdatering av eksisterende trinn.](media/PRT-3.png)
 
6. Velg avmerkingsboksen for prisattributt.

 ![Skjermbilde med avmerkingsboks for prissettingattributter.](media/PRT-4.png)

7. Klikk **OK** for å lukke siden, og velg deretter **Oppdater trinn**.

 ![Skjermbilde som viser Oppdater trinn-knappen.](media/PRT-5.png)
 
8. Gjenta denne prosessen for den andre plugin-modulen, **PreOperationQuoteLineDetail – oppdaterer msdyn_quotelinetransaction**.

9. Lukk registreringsverktøyet for plugin-modul.



[!INCLUDE[footer-include](../includes/footer-banner.md)]