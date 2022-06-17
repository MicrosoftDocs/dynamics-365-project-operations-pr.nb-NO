---
title: Annuller godkjenningen av tidligere godkjente oppføringer
description: Denne artikkelen forklarer hvordan en prosjektleder kan annullere godkjenningen av tidligere godkjente tids-, utgifts- eller materialbruksoppføringer.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930468"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Annuller godkjenningen av tidligere godkjente oppføringer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

En prosjektleder eller godkjenner som tidligere har godtkjent tids-, utgifts- eller materialbruksoppføringer, kan annullere godkjenningen av disse oppføringene. 

Følg disse trinnene for å annullere godkjenningen av en tidligere godkjent tids-, eller utgifts- eller materialbruksoppføring.

1. Gå til **Prosjekter** \> **Mitt arbeid** \> **Godkjenninger**.
2. Listesiden **Godkjenninger** viser alle tidsoppføringer som venter på godkjenning. Endre visningen til **Mine tidligere godkjenninger**.
3. Velg tids-, utgifts- eller materialgodkjenningene du vil annullere. Velg deretter **Annuller godkjenning** i handlingsruten.
4. Velg **OK** i bekreftelsesmeldingsboksen som vises, for å bekrefte operasjonen.

> [!IMPORTANT]
> Du kan ikke annullere godkjenningen av tidligere godkjente tids-, utgifts- og materialbruksoppføringer som allerede er fakturert til kunden. Hvis du prøver, får du en melding som sier at godkjenningen ikke kan kanselleres fordi den allerede er fakturert. I dette tilfellet kan du bare annullere godkjenningen hvis en korrigeringsfaktura brukes til å gi kunden full kreditt eller refundering på den opprinnelige fakturaen.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Virkningen av å annullere godkjenningen av en tidligere godkjent oppføring

Når en godkjenning annulleres, får dette både driftsinnvirkning og finansiell innvirkning.

### <a name="operational-impact"></a>Driftsinnvirkning

Hvis godkjenningen av en oppføring blir annullert, merkes godkjenningsoppføringen som **Sendt inn**. Statusen for oppføringen endres til **Sendt inn**. I denne fasen kan et prosjektteammedlem tilbakekalle oppføringen uten å sende inn en tilbakekallingsforespørsel.

Godkjenneren kan endre verdiene for **Fakturerbart antall** og **Faktureringstype** og deretter godkjenne oppføringen én gang til.

### <a name="financial-impact"></a>Økonomisk innvirkning

Hvis godkjenningen av en oppføring annulleres, oppdateres de tilsvarende faktiske verdiene for kost og salg på følgende måte:

- Feltet **Justeringsstatus** oppdateres til **Justert**.
- Feltet **Faktureringsstatus** oppdateres til **Kansellert**.

Deretter opprettes tilbakeføringsoppføringer i tabellen over faktiske verdier. For å opprette tilbakeføringsoppføringer kopierer systemet over feltverdiene fra de opprinnelige faktiske verdiene. De eneste verdiene som ikke kopieres over, er antallsverdiene. Disse verdiene reverseres i stedet. Reverserte faktiske verdier opprettes både for de faktiske verdiene **Kostnad** og **Ufakturert salg**. Feltet **Justeringsstatus** for de tilbakeførte faktiske verdiene settes til **Kan ikke justeres**, og feltet **Faktureringsstatus** settes til **Annullert**. På grunn av disse endringene vil det registrerte forbruket og restinntekten for prosjektet ikke lengre regnes med for beløpene som disse faktiske verdiene representerer.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
