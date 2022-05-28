---
title: Vise belastbar utnyttelse for ressurser
description: Dette emnet gir informasjon om ressursutnyttelsesvisningen.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 0f6240a3337eb78496570ddfabc85d431e61d640
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595648"
---
# <a name="view-chargeable-utilization-for-resources"></a>Vise belastbar utnyttelse for ressurser

[!include [banner](../includes/psa-now-project-operations.md)]
 
I **Utnyttelse-visningen** på siden **Ressursutnyttelse i Project Service** vises den belastbare utnyttelsen for hver bestillbare ressurs. Siden visningen er basert på planleggingstavlen, finner du mange av de samme funksjonene.

> ![Skjermbilde av visningen Utnyttelse.](media/FAQ-utilization-1.png)
 

Beregningen av belastbar utnyttelse fungerer som følger:

   Belastbar utnyttelse = (belastbare faktiske timer) / (ressurskapasitet).

Cellene representerer beregnet belastbar utnyttelse for den valgte perioden (dager uker eller måneder).

Fargene i hver celle viser belastbar utnyttelse for en ressurs sammenlignet med belastbar målutnyttelse. 

Du kan angi målutnyttelse på ressursens standardrolle eller på den individuelle ressursen selv. Beregningen ser på den individuelle for målet først, og deretter på ressursens standardrolle.

## <a name="set-target-on-a-resource"></a>Angi mål for en ressurs

1. Gå til **Ressurser** \> **Ressurser**. 
2. Velg en ressurs for å åpne oppføringen. 
3. I kategorien **Project Service** kan du angi ressursens målutnyttelse.

> ![Skjermbilde av fanen Project Service for å angi målutnyttelse.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Angi målutnyttelse for en rolle

1. Gå til **Ressurser** \> **Ressursroller**. 
2. Velg en rolle, og åpne oppføringen. 
3. Angi målutnyttelsen for rollen.

> ![Skjermbilde av bruk av ressursroller for å angi målutnyttelse.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Beregne belastbar utnyttelse for en ressurs

Du må oppfylle noen forhåmndskrav for å beregne belastbar utnyttelse for en ressurs. 

### <a name="set-default-role-for-individual-resource"></a>Angi standardrolle for individuell ressurs

Du må angi målutnyttelse først på enten den individuelle ressursen eller på ressursroller. Hvis du bruker ressursroller for mål, må hver enkelt ressurs ha en standardrolle. 

1. Du angir dette ved å gå til **Ressurser** \> **Ressurser**. 
2. Velg en ressurs, åpne oppføringen, og velg deretter kategorien **Project Service**. 
3. I rutenettet **Ressursrolle** kontrollerer du at det finnes én rolle for ressursen, og at **Er standard** er satt til **Ja**.
 
### <a name="change-billing-type-for-resource-role"></a>Endre faktureringstype for ressursrolle

Ressursrollene må angis slik at de har faktureringstypen **Belastbar**. 

1. Gå til **Ressurser** \> **Ressursroller**. 
2. Åpne oppføringen du vil oppdatere, og angi deretter faktureringstypen standard til **Belastbar**.

### <a name="set-working-hours-for-resource-role"></a>Angi arbeidstimer for ressursrolle
 
Ressursen må ha arbeidstimer for beregning av kapasitet. 

1. Gå til **Ressurser** \> **Ressurser**. 
2. Velg en ressurs for å åpne oppføringen, og velg deretter **Vis arbeidstimer**. 
3. Du kan masseoppdatere listen over ressurser ved å bruke en **mal for arbeidstimer** i **ressurslistevisningen**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Feilsøke belastbare faktiske timer

De belastbare faktiske timene hentes fra enheten **Faktiske verdier**. Faktiske verdier med faktureringstypen **Belastbar** er med i beregningen, og derfor må du ha prosjekter der de faktiske verdiene er belastbare.

Hvis du ikke ser belastbar utnyttelse, er det noen ting du kan kontrollere:

- Ressursen har arbeidstimer definert for kapasitet.
- Ressursen har enten et individuelt definert utnyttelsesmål, eller har en standardrolle tilordnet til den. Rollen har et utnyttelsesmål definert for den.
- Faktiske verdier har faktureringstypen **Belastbar** for perioden du forventer en utnyttelsesberegning for. Sjekk følgende hvis du ser faktiske verdier med andre faktureringstyper enn belastbar:

  - Rollen som brukes på de faktiske verdiene, har en annen standard faktureringstype enn belastbar.
  - Rollen på prosjektkontraktlinjen som støtter prosjektet, er satt til ikke-belastbar.
  - Prosjektet har ingen tilknyttet kontraktlinje.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
