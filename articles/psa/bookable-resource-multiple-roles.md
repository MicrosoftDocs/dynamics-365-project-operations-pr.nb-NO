---
title: Beregne salg og kostnader for prosjekter når en ressurs som kan reserveres, fyller flere roller i et prosjekt
description: Dette emnet gir informasjon om hvordan prisdimensjoner kan brukes til å støtte prissetting og kostberegning for en ressurs som fyller flere roller i et prosjekt.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081672"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a>Beregne salg og kostnader for prosjekter når en ressurs som kan reserveres, fyller flere roller i et prosjekt 

Prosjektrelaterte selskaper har ofte behov for at én ressurs utfører flere roller i et prosjekt. Hver av disse rollene kan være priset og kalkulert på forskjellige måter, noe som betyr at den samme ressursens tid på prosjektet kan få et annet økonomisk estimat, avhengig av fakturerings- og kostnadssatser for hver av rollene. Med Project Service Automation kan du konfigurere verdiene i teammedlemsoppføringen for den navngitte ressursen og tillate forskjellige overstyringer for hver av oppgavene som teammedlemmet er tilordnet til.

Eksemplet nedenfor forklarer hvordan den enkle overstyringen av denne verdien tillater at en ressurs har flere roller i et prosjekt med forskjellige kostnads- og faktureringssatser.

## <a name="create-tasks"></a>Opprett oppgaver
Opprett to prosjektoppgaver på 40 timer hver, oppgave A og oppgave B. Velg oppgave A som forgjenger for oppgave B.

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurere rolle og organisasjonsenhet for et generelt prosjektteammedlem

1. På siden **Planlegg** velger du **Oppgave** -raden for oppgave A. 
2. I **Ressurser** -feltet velger du **Opprett** i rullegardinlisten.
3. På siden **Hurtigoppretting av teammedlem** angir du attributtene for det generelle teammedlemmet som kan utføre denne oppgaven.
4. Velg riktig rolle og organisasjonsenhet, og velg deretter **Lagre og Lukk**. Et generelt teammedlem blir opprettet og tilordnet til denne oppgaven. 

Gjenta disse trinnene for oppgave B, og kontroller at rollen og organisasjonsenheten for det generelle teammedlemmet som er opprettet for oppgave B, er forskjellig fra oppgave A. 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a>Konfigurere rolle og organisasjonsenhet for en prosjektoppgave

1. Når du har opprettet oppgave A, velger du oppgaven, og deretter velger du **Rediger oppgave**.
2. På siden **Oppgavedetaljer** finnre du feltene **Rolle** og **Organisasjonsenhet** , der du må legge til verdiene som kreves for en ressurs som skal utføre denne oppgaven. 

  > [!NOTE]
  > Hvis du utfører disse scenarioene ved hjelp av demonstrasjonsdata for Project Service Automation, velger du **Sjefskonsulent** for rollen og **Fabrikam US** som organisasjonsenhet.

3. Velg oppgave B, og velg deretter **Rediger oppgave**.
4. På siden **Oppgavedetaljer** finnre du feltene **Rolle** og **Organisasjonsenhet** , der du må legge til verdiene som kreves for en ressurs som skal utføre denne oppgaven. Kontroller at verdiene i feltene **Rolle** og **Organisasjonsenhet** er forskjellige mellom oppgave B og oppgave A. 

  > [!NOTE]
  > Hvis du utfører disse scenarioene ved hjelp av demonstrasjonsdata for Project Service Automation, velger du **Nettverkstekniker** for rollen og **Fabrikam US** som organisasjonsenhet.

5. Lagre og lukk siden **Oppgavedetaljer**. 

## <a name="team-member-and-estimates-behaviour"></a>Virkemåte for teammedlemmer og estimater 

1. På siden **Oppgavedetaljer** , under **Teammedlem** , velger du de to generelle teammedlemmene, og deretter velger du **Generer krav**. Dette genererer ressurskrav. 
2. Velg gruppemedlemsraden for **Sjefskonsulent** , og velg deretter **Bestill**. Planleggingstavlen åpnes og bestiller en ressurs til dette kravet.
3. Velg gruppemedlemsraden for **Nettverkstekniker** , og velg deretter **Bestill**. Planleggingstavlen åpnes og bestiller den samme ressursen til dette kravet.

### <a name="team-member-grid"></a>Rutenettet Teammedlem 
På rutenettet **Teammedlem** kan du legge merke til at oppføringene til de to generelle teammedlemmene er slettet, og at de har erstattet én ressurs. Det finnes ett sett med verdier for denne ressusen som viser et standardsett med verdier for **Rolle** og **Organisasjonsenhet**.
Når du utvider raden for denne teammedlemsoppføringen, kan du se forskjellige tildelinger i teammedlemsoppføringen for begge disse oppgavene. Hver tildelingsrad har oppgavespesifikke verdier for **Rolle** og **Organisasjonsenhet**. 

### <a name="estimates-grid"></a>Rutenett for estimater 
Når du navigerer til rutenettet **Estimater** , vil du legge merke til at begge tilordningene for den samme ressursen har forskjellig pris.
Tilordningen for ressursen i oppgave A er priset ved hjelp av **Rolle** -attributtverdien for **Sjefskonsulent**. Tilordningen for den samme ressursen i oppgave B er priset ved hjelp av **Rolle** -attributtverdien for **Nettverkstekniker**.




