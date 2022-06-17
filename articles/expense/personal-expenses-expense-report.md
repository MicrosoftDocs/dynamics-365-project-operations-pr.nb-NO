---
title: Arbeide med personlige utgifter i en utgiftsrapport
description: Denne artikkelen inneholder informasjon om hvordan du arbeider med personlige utgifter påløpt av ansatte når de er på forretningsreiser.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 1cda5151a32482f92c69402bcc0056d7b6572db8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922280"
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
