---
title: Arbeide med personlige utgifter i en utgiftsrapport
description: Dette emnet inneholder informasjon om hvordan du arbeider med personlige utgifter som påløper for ansatte når de reiser i forretningsformål.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 5e1162133eec5a85675bf686855d420c50de0eaf045d81c4b417b6fe66ee19fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993163"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Arbeide med personlige utgifter i en utgiftsrapport

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

I løpet av forretningsreiser kan en ansatt kreve personlige utgifter for bedriftens kredittkort. Hvis en prosess ikke er definert for håndtering av personlige utgifter, kan godkjenningsprosessen for utgiftsrapport bli avbrutt når en ansatt sender sin spesifiserte utgiftsrapport.

Du kan bruke to metoder for å arbeide med personlige utgifter for en ansatt:

  - **Betalt av ansatt**: Organisasjonen betaler ikke personlige utgifter som vises på fakturaen for firmaets kredittkort. I stedet betaler den ansatte kredittkortleverandøren direkte for utgiftene. 
  - **Betalt av firma**: Organisasjonen betaler hele regningen for bedriftskredittkortet, og deretter belaster arbeiderens konto for de personlige utgiftene.

Du kan velge metoden organisasjonen bruker, på siden **Parametere for utgiftshåndtering**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert

Funksjonen **Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert**, gjelder bare utgiftsrapporter som er godkjent ved hjelp av en arbeidsflyt på linjenivå. Rapporter godkjennes ved å gå til **Behandle kostnadsrapporter** > **Kostnadsrapporter tilordnet til meg** > **Åpne utgiftsrapport**. 

Hvis du vil aktivere denne funksjonen, går du til **Arbeidsområder** > **Funksjonsbehandling**, velger **Aktiver funksjon for delt utgift når personlig beløpsfelt har verdi definert**, og deretter velger du **Aktiver nå**. 

Når funksjonen er aktivert, genererer utgiftslinjer som bruker denne funksjonaliteten, to linjer når rapporten sendes. To linjer genereres, slik at godkjenneren kan godkjenne hver linje separat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
