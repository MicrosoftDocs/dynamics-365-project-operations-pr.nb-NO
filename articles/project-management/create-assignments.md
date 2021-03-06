---
title: Opprett ressurstilordninger
description: Dette emnet gir informasjon om oppretting av generelle og navngitte ressurstilordninger.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906269"
---
# <a name="create-resource-assignments"></a>Opprett ressurstilordninger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_


En ressurstilordning er den direkte tilknytningen av et prosjektteammedlem til en bladnodeoppgave. Dette emnet gir informasjon om de forskjellige måtene å tilordne ressurse på.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Opprette et generelt teammedlem gjennom oppgavetilordning


Når du oppretter et generelt teammedlem via oppgavetilordning, oppretter du en plassholder eller generell ressurs. Denne generelle ressursen beskriver egenskapene til den navngitte ressursen som du vil skal arbeide med oppgavene. Deretter genererer du et krav, eller sender en forespørsel ved hjelp av kravet, som brukes til å søke etter og reservere den navngitte ressursen.

1. I rutenettet Planlegg for en oppgave velger du ressursikonet i **Ressurs**-cellen.
2. Skriv inn et navn som fungerer som plassholder for ressursens navn. For eksempel "Programleder".
3. Velg **Opprett**, og angi rollen for den generelle ressursen i feltet for **hurtigoppretting av prosjektteammedlem**.
4. Tilordne oppgaver etter behov til denne plassholderessursen ved å velge ressursen i **ressursvelgeren** for oppgaven. Ressursene er oppført under **Teammedlemmer**.
5. Når du er ferdig med å tilordne den generelle ressursen, velger du den generelle ressursen i kategorien **Team** og velger deretter **Generer krav** for å opprette et ressurskrav for den generelle ressursen.
6. Velg **Bestill** for den generelle ressursen, og bruk deretter planleggingstavlen for å finne og bestille en virkelige ressurs. Du kan også sende kravet for fullføring av en ressursleder.
7. Når den generelle ressursen er fullstendig oppfylt (delvis oppfyllelse av ressurskrav vil ikke resultere i en ressurstilordning) med en navngitt ressurs, fjernes den generelle ressursen fra teamet. Oppgavetilordningene for den generelle ressursen tilordnes den navngitte ressursen som oppfylte ressurskravet for den generelle ressursen.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Tilordne en navngitt ressurs fra listen over alle ressurser som kan reserveres

Du kan bruke søkeboksen i **ressursvelgeren** for å søke i alle aktive ressurser som kan reserveres, og tilordne dem til enhver bladnodeoppgave. Ressurser som er tilordnet på denne måten, blir lagt til i teamet uten bestillinger. Dette ligner på å legge til et teammedlem og velge **Ingen** som tildelingsmetode. Ressursen vises i kategoriene **Team**, **Ressurstilordning** og **Avstemming** som ressurser med bare tilordninger og et bestillingsunderskudd. Reserver dem hvis du vil bruke tilgjengeligheten deres.

1. Naviger til cellen **Tilordnet til** fra oppgaverutenettet, tavlen eller tidslinjen.
2. Begynn å skrive inn et navn i søkeboksen. Søkeresultater for navnet vises i **ressursvelgeren** under **Andre ressurser**.
3. Velg ressursen du vil tilordne til oppgaven, eller velg navnet på ressursen under **Andre teamressurser**.
