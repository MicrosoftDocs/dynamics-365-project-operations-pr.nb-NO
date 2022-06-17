---
title: Oppdater programtilleggsattributter slik at de inkluderer nye prisdimensjoner
description: Denne artikkelen inneholder informasjon om hvordan du oppdaterer programtilleggsattributter for prisdimensjoner.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 459aefb510cc9a9ec55a86ca7e362db98ccabb70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913218"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Oppdater programtilleggsattributter slik at de inkluderer nye prisdimensjoner

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Hvis du ikke bruker tilbuds- og kontraktfunksjonene i Project Service Automation, kan du hoppe over denne artikkelen.

Denne artikkelen forutsetter at du har fullført prosedyrene i artiklene [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md), [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md) og [Konfigurere egendefinerte felt som prisdimensjoner](set-up-pricing-dimensions.md). Hvis du ikke har fullført disse fremgangsmåtene, kan du gå tilbake og fullføre dem og deretter gå tilbake til denne artikkelen.

Når det blir opprettet en tilbudslinjedetalj på siden **Tilbudslinje** for en prosjekttilbudslinje, oppretter systemet to estimatlinjer i bakgrunnen – én linje for kostnadssiden for estimatet og én for salgsiden. Dette er det samme for prosjektkontraktlinjer.

Når du gjør en endring i antallet eller et felt på kostnadssiden, overføres endringen til salgsiden. Dette kan skyldes at følgende programtillegg må registreres på nytt etter at du har endret prisdimensjoner.

- PreOperationContractLineDetailUpdate – oppdaterer **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate – oppdaterer **msdyn_quotelinetransaction**.

Fremgangsmåten nedenfor forklarer hvordan du registrerer programtilleggene.

1. Åpne **PluginRegistrationTool**, koble til forekomsten på nettet.
2. Klikk **Søk**, og søk etter programtillegget som du vil oppdatere.

 ![Skjermbilde av søketreet.](media/PRT-1.png)

3. Når programtillegget er funnet, velger du det, og deretter klikker du **Velg i hovedskjema**.

4. Velg trinnet i programtillegget som skal oppdateres, høyreklikk, og velg deretter **Oppdater**.

 ![Skjermbilde av programtillegget som skal oppdateres.](media/PRT-2.png)
 
5. I oppdateringsvinduet klikker du på ellipsen (**...**) i filtreringsegenskapene.

 ![Skjermbilde av konfigurasjonsinformasjon for oppdatering av eksisterende trinn.](media/PRT-3.png)
 
6. Velg avmerkingsboksen for prisattributt.

 ![Skjermbilde med avmerkingsboks for prissettingattributter.](media/PRT-4.png)

7. Klikk **OK** for å lukke siden, og velg deretter **Oppdater trinn**.

 ![Skjermbilde som viser Oppdater trinn-knappen.](media/PRT-5.png)
 
8. Gjenta denne prosessen for det andre programtillegget, **PreOperationQuoteLineDetail – oppdaterer msdyn_quotelinetransaction**.

9. Lukk registreringsverktøyet for programtillegg.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
