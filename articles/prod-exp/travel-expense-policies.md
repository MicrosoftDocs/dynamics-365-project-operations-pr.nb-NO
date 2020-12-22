---
title: Konfigurere utgiftspolicyer
description: Du kan konfigurere utgiftspolicyene som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner i Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650106"
---
# <a name="set-up-expense-policies"></a>Konfigurere utgiftspolicyer

[!include [banner](../includes/banner.md)]

Du kan definere policyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.         
Ved å implementere utgiftspolicyer kan du administrere utgifter effektivt.         

Du kan for eksempel angi en policy for hotellutgifter i New York, som angir at reiseutgiften ikke kan overskrides USD 250 per natt.       
Hvis en arbeider sender en reiseregning eller en reiserekvisisjon der romprisen overskrider dette beløpet, vil systemet varsle        
arbeideren om at policybeløpet for utgiften er overskredet. Du kan konfigurere meldingen som arbeideren skal motta når du        
definener policyen.      
        
Du kan definere tre typer policyer:         
        
- Advarsel – Gjør det mulig for den ansatte å sende en reiseregningsrapport eller reiserekvisisjon, men utgiften blir merket for alle godkjennere og        
  for senere rapportering.        

- Feil – Krever at arbeideren reviderer utgiften for å overholde policyen før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.       
 
 - Begrunnelse – Krever at arbeideren eller en overordnet angir en begrunnelse for å overskride policybeløpet før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.        

## <a name="policy-tips"></a>Policytips
Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for håndtering av reiseregning og utlegg. 
* Policyer er datobaserte, og en policy trer ikke i kraft hvis den opprettes med en dato etter datoen da utgiften oppstod. Hvis du for eksempel oppretter en ny policy i dag for å håndheve en maksimal måltidsutgift på $50, sjekkes ikke eksisterende utgifter som er registrert i går, mot denne policyen.
* Når du oppretter en policy for en utgiftskategori som kan spesifiseres, vurderer du å legge til en betingelse for utgiftslinjetypen. Noen policyer, for eksempel krav om kvittering, vil kanskje ikke gi mening for spesifiserte linjer, og bør bare brukes på hodelinjen eller en linje uten varer. 
* Policyer for utgiftsadministrasjon evalueres mot kildeenheten som standard. For konserninterne scenarioer kan du angi at policyen skal evalueres mot målenheten (enhet som låner) i stedet. Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen for evaluering av reiseregninger mot juridisk låneenhet i arbeidsområdet **Funksjonsbehandling**.

## <a name="when-to-evaluate-policies"></a>Når policyer skal evalueres

I parametere for reiseregning og utlegg er det et alternativ for å evaluere policyer for reiseregning og utlegg når en linje lagres, eller når en reiseregning sendes. Hvis du velger å evaluere når en linje lagres, sørger dette for at brukere får tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig. Hvis ikke kan du utsette policyevalueringen og spare tid under innsending til arbeidsflyten hvis valideringen foregår på slutten.
