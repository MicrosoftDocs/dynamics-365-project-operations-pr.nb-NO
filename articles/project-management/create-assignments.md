---
title: Opprett ressurstilordninger
description: Denne artikkelen inneholder informasjon om hvordan du oppretter generiske og navngitte ressurstilordninger.
author: ruhercul
ms.date: 11/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 42dd2906ce8db8844bf4dea232f24aca58a5d951
ms.sourcegitcommit: 9b1136d95f19cc039d675a4a1b0962ca3ec61646
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812006"
---
# <a name="create-resource-assignments"></a>Opprett ressurstilordninger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


En ressurstilordning er den direkte tilknytningen av et prosjektteammedlem til en bladnodeoppgave. Denne artikkelen inneholder informasjon om de forskjellige måtene du kan tilordne ressurser på.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Opprette et generelt teammedlem gjennom oppgavetilordning


Når du oppretter et generelt teammedlem via oppgavetilordning, oppretter du en plassholder eller generell ressurs. Denne generelle ressursen beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene. Deretter genererer du et krav eller sender inn en forespørsel ved hjelp av kravet, som brukes til å søke etter og reservere den navngitte ressursen.

1. I rutenettet Planlegg for en oppgave velger du ressursikonet i **Ressurs**-cellen.
2. Skriv inn et navn som fungerer som plassholder for ressursens navn. For eksempel "Programleder".
3. Velg **Opprett**, og angi rollen for den generelle ressursen i feltet for **hurtigoppretting av prosjektteammedlem**.
4. Tilordne oppgaver etter behov til denne plassholderessursen ved å velge ressursen i **ressursvelgeren** for oppgaven. Ressursene er oppført under **Teammedlemmer**.
5. Når du er ferdig å tilordne den generelle ressursen, velger du den generelle ressursen i kategorien **Team** og velger deretter **Generer krav** for å opprette et ressurskrav for den generelle ressursen.
6. Velg **Bestill** for den generelle ressursen, og bruk deretter planleggingstavlen for å finne og bestille en virkelige ressurs. Du kan også sende kravet for fullføring av en ressursleder.
7. Når den generelle ressursen er fullstendig oppfylt med en navngitt ressurs, fjernes den generelle ressursen fra teamet. (Delvis oppfyllelse av ressurskrav fører ikke til en ressurstilordning.) Oppgavetilordningene for den generelle ressursen tilordnes til den navngitte ressursen som oppfylte ressurskravet for den generelle ressursen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilordne en navngitt ressurs fra listen over alle ressurser som kan reserveres

Du kan bruke søkeboksen i **ressursvelgeren** for å søke i alle aktive ressurser som kan reserveres, og tilordne dem til enhver bladnodeoppgave. Ressurser som er tilordnet på denne måten, blir lagt til i teamet uten bestillinger. Dette ligner på å legge til et teammedlem og velge **Ingen** som tildelingsmetode. Ressursen vises i kategoriene **Team**, **Ressurstilordning** og **Avstemming** som ressurser med bare tilordninger og et bestillingsunderskudd. Reserver dem hvis du vil bruke tilgjengeligheten deres.

1. Naviger til cellen **Tilordnet til** fra oppgaverutenettet, tavlen eller tidslinjen.
2. Begynn å skrive inn et navn i søkeboksen. Søkeresultater for navnet vises i **ressursvelgeren** under **Andre ressurser**.
3. Velg ressursen du vil tilordne til oppgaven, eller velg navnet på ressursen under **Andre teamressurser**.

## <a name="editing-resource-assignment-contours"></a>Redigering av ressurstilordningsomfang

Når ressurser tilordnes til en oppgave i tidsplanen, fordeles arbeidet deres lineært til hver ressurs, basert på ressursens arbeidstid og prosjektets planleggingsmodus. En prosjektleder kan bruke rutenettet for ressurstilordning til å finjustere arbeidsestimatene for hver ressurs som er tilordnet til én eller mange oppgaver på tvers av de ulike tidsskalaene. Denne funksjonen hjelper prosjektledere å oppnå mer nøyaktige kostnads- og salgsestimater, som styres av ressurstilordningsomfangene som genereres når en ressurs tilordnes til en oppgave. Prosjektledere kan i tillegg lettere gjenspeile ressursbehovet som kreves for å bygge behovet i et ressurskrav.

### <a name="navigation"></a>Navigering

For å få tilgang til rutenettet for omfangsredigering velger prosjektlederen først **Oppgaver**-fanen på hovedsiden for prosjektet og deretter **Tilordninger**-fanen.

![Tilordninger-fanen i Oppgaver-fanen på hovedsiden for prosjektet.](media/AssignmentGrid.png)

Rutenettet støtter to metoder for gruppering: **grupper etter ressurs** og **grupper etter oppgave**. I motsetning til i rutenettvisningen kan ikke kolonner konfigureres. De eneste kolonnene som vises, er **Tilordnet til**, **Oppgavenavn**, **Tilordningsstart**, **Tilordningsslutt** og **Tilordningsarbeid**.

Når rutenettet først gjengis, begynner det ved det tidligste tilordningsomfanget. Hvis tidsplanen ikke inneholder noen tilordninger som har arbeid, blir rutenettet tomt og gjengir ingenting.

![Tomt tilordningsrutenett.](media/emptyassignmentgrid.png)

Hvis du vil vise omfangene og ulike tidsskalaer, er det skrivebeskyttede rutenettet for ressurstilordning og rutenettet for ressursavstemming også tilgjengelig.

### <a name="resource-calendars"></a>Ressurskalendere

Funksjonen for å redigere et omfang for en bestemt dag styres av ressursens arbeidsdager, som gjenspeiles i kalenderen. Hvis en celle er deaktivert for en gitt ressurs, har ikke denne ressursen arbeidsdager i denne perioden.

Omfangene til en ressurs kan strekke seg utover gjeldende start- og sluttdatoer for den tilordnede oppgaven. Hvis et omfang oppdateres slik at det kommer etter den siste sluttdatoen for en oppgave eller den tidligste startdatoen for en oppgave, endres sluttdatoen eller startdatoen for oppgaven etter behov. Hvis et omfang imidlertid oppdateres slik at det kommer tidligere enn startdatoen for en oppgave som er koblet til en foregående, mislykkes oppdateringen fordi tilordningen utløser oppgaven slik at den starter før den foregående er fullført, og denne virkemåten støttes ikke for øyeblikket.

### <a name="co-authoring"></a>Samtidig redigering

Endringer i rutenettet for ressurstilordning gjenspeiles automatisk i tilknyttede visninger, inkludert diagram-, tidslinje-, tavle- og rutenettvisninger. Hvis flere brukere går gjennom prosjektet samtidig, gjenspeiles eventuelle endringer som én bruker gjør, i rutenettet. Eventuelle endringer som gjøres i rutenettet for ressurstilordning, vises til alle andre brukere som viser prosjektet i samme økt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
