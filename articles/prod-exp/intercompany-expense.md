---
title: Konserninterne utgifter
description: Denne artikkelen inneholder informasjon om hvordan du bruker konserninterne utgifter til å tilordne en arbeiders utgifter til den juridiske enheten som arbeidet ble utført for.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932400"
---
# <a name="intercompany-expenses"></a>Konserninterne utgifter

En arbeider som er ansatt av én juridisk enhet i en organisasjon, kan utføre arbeid for en annen juridisk enhet i den samme organisasjonen. Du kan bruke konserninterne utgifter til å tilordne arbeiderens utgifter til den juridiske enheten som arbeidet ble utført for. Den juridiske enheten som bruker arbeideren, kalles den utlånende juridiske enheten. Den juridiske enheten som arbeideren påløper kostnader for, kalles den lånende juridiske enheten. 

Før en arbeider kan opprette og sende inn selskapets utgifter, må du aktivere linjer for selskapets utgifter. I den juridiske enheten for utlån på siden **Parametere for utgiftshåndtering** velger du **Tillat linjer for konsernintern utgift**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Avgiftspostering for konserninterne utgifter

[!include [banner](../includes/banner.md)]

Før du kan bruke avgiftsgrupper som er knyttet til den juridiske enheten for utlån (kilde) i stedet for den juridiske enheten (målet) i reiseregningen, må du aktivere funksjonaliteten i oppsettet av salgsavgift i økonomimodulen. Når parameteren **Juridisk enhet for konsernintern avgiftsbokføring** er satt til **Kilde** og **Bruk avgiftsregler for mva** er satt til **Nei**, brukes avgiftskombinasjonen for den juridisk enheten for utlån. Når den samme parameteren er satt til **Mål**, brukes avgiftskombinasjonen for den lånende juridiske enheten. Når det gjelder juridiske enheter i USA, når parameteren er angitt til **Kilde**, må feltet **Mva-fordringer** også konfigureres på den nye siden **Bokføringsgrupper i hovedbok**. Regnskapsmotoren bruker informasjonen fra dette feltet for avgiftsrelatert regnskapsregistrering.   
Funksjonaliteten er konsekvent for utgiftslinjer som er bokført med eller uten et prosjekt.  

## <a name="new-expense-expression-builder"></a>Nytt utgiftsuttrykksverktøy

Den nye utgiftsuttrykksverktøyet løser problemer med scenarioer for selskapets utgifter som bruker prosjekter. Denne funksjonen sikrer at utgiftsregelen valideres riktig mot prosjektet som er valgt på utgiftslinjen, når du oppretter en selskapsutgift, og at utgiftsrapporten kan sendes riktig.

For at utgiftsuttrykksverktøyet skal fungere må den være aktivert. I tillegg bør utgiftspolicyen som har en prosjekt-ID, angis.

Hvis du allerede har konfigurert policyer som validerer prosjekt-ID-en på utgiftslinjen, må disse policyene avvikles. Deretter kan du aktivere funksjonen og konfigurere policyene på nytt.

Følg fremgangsmåten nedenfor for å aktivere denne funksjonen.

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I listen velger du **Nytt utgiftsuttrykksverktøy for å løse problemer med konserninterne utgiftsscenarioer som bruker prosjekter**. Velg deretter **Aktiver nå**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
