---
title: Definere utgiftspolicyer
description: Du kan definere utgiftspolicyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128430"
---
# <a name="define-expense-policies"></a>Definere utgiftspolicyer

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Du kan definere policyer som dine arbeidere må følge når de angir og sender ut reiseregningsrapporter og reiserekvisisjoner.         
Ved å implementere utgiftspolicyer kan du administrere utgifter effektivt.         

Du kan for eksempel angi en policy for hotellutgifter i New York, som angir at reiseutgiften ikke kan overskrides USD 250 per natt.       
Hvis en arbeider sender en reiseregning eller en reiserekvisisjon der romprisen overskrider dette beløpet, vil systemet varsle         
arbeideren om at policybeløpet for utgiften er overskredet. Du kan konfigurere meldingen som arbeideren skal motta når du        
definener policyen.      
        
Du kan definere tre typer policyer:         
        
- **Advarsel**: Gjør det mulig for den ansatte å sende en reiseregningsrapport eller reiserekvisisjon, men utgiften blir merket for alle godkjennere og         
  for senere rapportering.        

- **Feil**: Krever at arbeideren reviderer utgiften for å overholde policyen før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.        
 
 - **Begrunnelse**: Krever at arbeideren eller en overordnet angir en begrunnelse for å overskride policybeløpet før han/hun sender reiseregningsrapporten eller reiserekvisisjonen.        

## <a name="policy-tips"></a>Policytips
Her er noen forslag som kan hjelpe deg når du oppretter nye policyer for håndtering av reiseregning og utlegg: 

- Policyer er datobaserte, noe som betyr at en policy ikke trer i kraft hvis den opprettes med en dato etter datoen da utgiften oppstod. Du oppretter for eksempel en ny policy i dag for å angi en maksimal utgift for måltider på USD 50. Alle eksisterende utgifter som er angitt fra og med i går, blir ikke kontrollert mot denne policyen.
- Når du oppretter en policy for en utgiftskategori som kan spesifiseres, vurderer du å legge til en betingelse for utgiftslinjetypen. Noen policyer, for eksempel å kreve en kvittering, gir kanskje ikke mening for spesifiserte linjer. I denne situasjonen brukes policyen bare på hodelinjen eller en ikke-spesifisert linje. 
- Policyer for utgiftsadministrasjon evalueres mot kildeenheten som standard. For konserninterne scenarioer kan du angi at policyen skal evalueres mot målenheten (enhet som låner) i stedet. Hvis du vil kjøre policyene mot målenheten, kan du aktivere funksjonen for **evaluering av reiseregninger mot juridisk låneenhet** i arbeidsområdet for **funksjonsbehandling**.

## <a name="when-to-evaluate-policies"></a>Når policyer skal evalueres

I parametere for reiseregning og utlegg kan du velge å evaluere policyer for reiseregning og utlegg når en linje lagres, eller når en reiseregning sendes. Hvis du velger å evaluere når en linje lagres, vil brukere ha tidligere innsyn i hva de må gjøre for å fullføre reiseregningen samtidig. Hvis ikke kan du utsette policyevalueringen og spare tid ved å validere på slutten, under innsending til arbeidsflyten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]