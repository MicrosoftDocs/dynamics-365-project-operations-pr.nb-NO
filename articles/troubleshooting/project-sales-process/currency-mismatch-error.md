---
title: Valutakonfliktfeil
description: Dette emnet gir feilsøkingsinformasjon om en valutakonfliktfeil som oppstår når du lagrer bestemte oppføringstyper.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903492"
---
# <a name="currency-mismatch-error"></a>Valutakonfliktfeil 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Når du lagrer et prosjekt, en kontrakt, et tilbud eller bestillbare ressurser, kan det hende du mottar en feil, **Det eiende firmaet for prosjektkontrakt samsvarer ikke med valutaen for kontraktsenheten. Velg et annet eiende firma eller kontraktsenhet slik at prosjektkontrakten kan fortsette**. Dette skyldes at det ikke er samsvar i valutaen for kontraktørenheten for oppføringen og den eksisterende firmavalutaen.


## <a name="resolution"></a>Avslutning

Du løser dette ved å gjøre følgende:
- Kontroller valutaen for kontraktsenheten for denne oppføringen. Du kan se valutaen ved å åpne oppføringen for organisasjonsenheten og kontrollere verdien i kategorien **Generelt** i **Valuta**-feltet.
- Kontroller valutaen til det eiende firmaet. Du kan se valutaen ved å gå til **Relaterte** > **Finanskontoer** i firmaoppføringen. Dobbeltklikk finansoppføringen som er knyttet til firmaet, og kontroller verdien i kategorien **Generelt** i feltet **Regnskapsvaluta**.

Hvis valutaen som er angitt i kontraktsenheten og finansoppføringen ikke samsvarer, justerer du konfigurasjonen eller velger andre verdier når du lagrer oppføringen. Systemet krever at disse oppføringene samsvarer for å sikre riktige firmafakturaflyter. Hvis du vil ha mer informasjon om selskapets konfigurasjoner, kan du se [Opprette konserninterne transaksjoner](../../project-accounting/create-intercompany-transactions.md).

Hvis firmaoppføringen ikke har en tilknyttet finansoppføring, angir dette at det mangler konfigurasjon under oppsett av miljøet. Konfigurasjonen må rettes av administrator. Systemadministratoren må gå til **Konfigurasjoner med dobbeltskriving** og stoppe og starte **Tilordningsversjoner av dobbel skrivin** på nytt med den første synkroniseringen av denne tilordningen og tilhørende forhåndskrav. Hvis du vil ha mer informasjon, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../../environment/resource-dual-write-maps.md).
