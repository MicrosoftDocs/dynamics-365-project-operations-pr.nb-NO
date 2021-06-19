---
title: Estimere salg og kostnader for prosjekter når en ressurs som kan reserveres fyller flere roller i et prosjekt
description: Dette emnet forklarer hvordan du bruker prisdimensjoner til å støtte pris- og kostnadsestimater for en ressurs som fyller flere roller i et prosjekt.
author: rumant
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7ef9765b7db1c6650fb0599bf5fb4b4b6304be69
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013678"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-on-a-project"></a>Estimere salg og kostnader for prosjekter når en ressurs som kan reserveres fyller flere roller i et prosjekt 

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering, og Project Operations for lagerførte/produksjonsbaserte scenarioer_ 

Prosjektbaserte selskaper har ofte behov for at én ressurs fyller flere roller i et prosjekt. Hver rolle kan være priset og kalkulert forskjellig. Dette betyr at den samme ressursens tid på et prosjekt kan få et annet økonomisk overslag, avhengig av faktura- og kostnadssatser for hver rolle. Du kan angi verdiene i teammedlemsoppføringen for den navngitte ressursen med forskjellige overstyringer for hver av oppgavene som teammedlemmet er tilordnet til.

Følgende eksempel veileder deg gjennom hvordan enkel overstyring av en verdi gjør det mulig for en ressurs å ha flere roller i et prosjekt med forskjellige kostnads-og fakturasatser.

## <a name="create-tasks"></a>Opprett oppgaver
Hvis du vil opprette oppgaver, må du legge til oppgaver i tillegg til hovedaktiviteter, deretter må du tilordne oppgaven før du legger til oppgavevarighet. 

### <a name="add-tasks-and-summary-tasks"></a>Legge til oppgaver og aktivitetssammendrag
Du legger til en oppgave ved å følge denne fremgangsmåten:

1. Gå til **Prosjekter**, og åpne prosjektet du vil legge til oppgaver i.
2. Velg **Legg til ny oppgave**. Gi oppgaven et navn, og trykk deretter **Enter**.
3. Angi et nytt oppgavenavn og trykk **Enter**. Gjenta dette til du har en fullstendig liste med oppgaver.
3. Hvis du vil rykke inn oppgaver under **Hoved**-aktiviteter, velger du de tre loddrette prikkene ved aktivitetsnavnet, og deretter velger du **Lag delaktivitet**. 

  > [!TIP]
  > Hvis du vil velge mer enn én oppgave, velger du en oppgave, trykk og hold nede **Ctrl**, og deretter velger du en annen oppgave.
  >
  > Du kan også velge **Fremme delaktivitet** for å flytte oppgaver ut fra **Hoved**-aktiviteter.

### <a name="assign-tasks"></a>Tilordne oppgaver

Du tilordner oppgaver ved å fullføre følgende trinn:

1. Velg personikonet i **Tilordnet til**-kolonnen for en oppgave.
2. Velg et teammedlem fra listen, eller skriv inn tekst for å søke etter et navn.

### <a name="add-task-duration-and-columns"></a>Legg til oppgavevarighet og kolonner

Det er ofte enklest å starte med å konstruere prosjektet med varighet. Du legger til en oppgavevarighet ved å fullføre følgende trinn.

1. I **Varighet**-kolonnen for en oppgave skriver du inn antallet dager du tror det vil ta for å fullføre oppgaven. Hvis du vil bruke en annen tidsenhet, angir du et tall pluss ordet **timer**, **uker** eller **måneder**.
2. Hvis du vil at oppgaven skal vises som en diamantformet milepæl i **Tidslinje**-visningen, skriver du inn **0 dager** i **Varighet**-kolonnen.
3. Trykk **Enter**  for å gå til neste oppgaves **Varighet**-felt og fortsett å angi varigheter.

  > [!NOTE]
  > Du kan ikke skrive inn en varighet for hovedaktiviteter.

Du kan legge til kolonner i prosjektet for å vise flere detaljer. Dette gjør du ved å velge **Legg til kolonne**. 

Hvis du vil ha mer informasjon, kan du se [Opprett et prosjekt](https://support.microsoft.com/en-us/office/create-a-project-a5b5e823-fb2e-45fd-be00-7d84422d9749).

## <a name="set-up-the-role-and-organization-unit-for-a-generic-project-team-member"></a>Konfigurere rollen og organisasjonsenheten for et generisk prosjektteammedlem
Du konfigurerer en rolle og organisasjonsenhet for et generelt teammedlem ved å følge denne fremgangsmåten.

1. På **Oppgaver**-siden velger du **Oppgave**-raden for **Oppgave A**. 
2. I **Tilordnet til** velger du **Legg til generell ressurs**. Dette åpner **Hurtigoppretting av teammedlem**-siden.
3. På siden **Hurtigoppretting av teammedlem** angir du attributtene for det generelle teammedlemmet som kan utføre denne oppgaven.
4. Velg riktig rolle og organisasjonsenhet, og velg deretter **Lagre og Lukk**. Et generelt teammedlem blir opprettet og tilordnet til denne oppgaven. 
5. Gjenta trinn 1–4 for **Oppgave B**. **Oppgave B** må imidlertid ha en annen rolle og organisasjonsenhet tilordnet det generelle teammedlemmet enn **Oppgave A**. 

## <a name="set-up-the-role-and-organization-unit-for-a-project-task"></a>Konfigurere rollen og organisasjonsenheten for en prosjektoppgave
Du konfigurerer en rolle og organisasjonsenhet for en oppgave ved å følge denne fremgangsmåten.

1. Når du har opprettet **Oppgave A**, velger du oppgaven, og deretter velger du **i**-ikonet for å åpne **Oppgavedetaljer**-ruten. 
2. I **Oppgavedetaljer**-ruten ruller du til bunnen og velger **Vis detaljer** for å åpne **Oppgavedetaljer**-siden.
3. På **Oppgavedetaljer**-siden i **Rolle** og **Organisasjonsenhet** legger du til verdiene som kreves for å utføre denne oppgaven for ressursen. 

  > [!NOTE]
  > Hvis du full fører dette scenariet ved hjelp av demonstrasjonsdata for Project Operations, velger du **Sjefskonsulent** for rollen, og **Fabrikam US** som organisasjonsenheten.

4. Velg **Oppgave B**, og velg deretter oppgaven.
5. Velg **i**-ikonet for å åpne **Oppgavedetaljer**-ruten. 
6. I **Oppgavedetaljer**-ruten ruller du til bunnen og velger **Vis detaljer** for å åpne **Oppgavedetaljer**-siden.
7. På **Oppgavedetaljer**-siden i **Rolle** og **Organisasjonsenhet** legger du til verdiene som kreves av en ressurs som ville utføre denne oppgaven. Verdiene i **Rolle** og **Organisasjonsenhet** for **Oppgave B** må være forskjellige fra de for **Oppgave A**. 

  > [!NOTE]
  > Hvis du fullfører dette scenariet ved hjelp av demonstrasjonsdata for Project Operations, velger du **Nettverkstekniker** for rollen, og **Fabrikam US** som organisasjonsenheten.

8. Lagre og lukk siden **Oppgavedetaljer**. 

## <a name="team-member-and-estimates-behavior"></a>Teammedlem og estimatfunksjon 
Fullfør fremgangsmåten nedenfor for å forstå funksjonen til **Teammedlem**-rutenettet og estimatene.

1. På **Teammedlem**-rutenettet velger du de to generelle teammedlemmene, og deretter velger du **Generer krav**. Dette genererer ressurskrav. 
2. Velg teammedlemsraden for **Sjefskonsulent**, og velg deretter **Bestill**. Planleggingstavlen åpnes med en liste over ressurser. Velg en ressurs, og velg deretter **Bestill** for å reservere ressursen til det kravet.
3. Velg teammedlemsraden for **Nettverkstekniker**, og velg deretter **Bestill**. Planleggingstavlen åpnes med en liste over ressurser. Velg samme ressurs som ovenfor, og velg deretter **Bestill** for å reservere ressursen til det kravet.

### <a name="team-member-grid"></a>Rutenettet Teammedlem 

På **Teammedlem**-rutenettet er de to generelle teammedlemsoppføringene slettet og erstattet med bare én ressurs. Det er et sett med verdier for denne ressursen, som er et standardsett med verdier for **Rolle** og **Organisasjonsenhet**.

Når du utvider raden for teammedlemsoppføringen, kan du se spesifikke tildelinger i teammedlemsoppføringen for begge oppgavene. Hver tildelingsrad har oppgavespesifikke verdier for **Rolle** og **Organisasjonsenhet**. 

### <a name="estimates-grid"></a>Rutenett for estimater 

På **Estimater**-rutenettet er begge tilordningene for den samme ressursen priset forskjellig. Tilordningen for ressursen i **Oppgave A** er priset ved hjelp av **Rolle**-attributtverdien for **Sjefskonsulent**. Tilordningen for den samme ressursen i **Oppgave B** er priset ved hjelp av **Rolle**-attributtverdien for **Nettverkstekniker**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]