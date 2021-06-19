---
title: Prosjektinnsatssporing
description: Dette emnet gir informasjon om hvordan du sporer prosjektinnsats og arbeidsfremdrift.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3fdf7787f0144dace84852a0442406085bdc1639
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010888"
---
# <a name="project-effort-tracking"></a>Prosjektinnsatssporing

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Behovet for å spore fremdriften mot en tidsplan varierer etter bransje. Noen bransjer sporer på et detaljert nivå, mens andre bransjer sporer på et høyere nivå. Dette emnet viser hvordan du planlegger for å oppfylle organisasjonens krav.

## <a name="effort-tracking-view"></a>Visning av innsatssporing

Visningen **Innsatssporing** sporer fremdriften for oppgaver i tidsplanen ved å sammenligne de faktiske innsatstimene som er brukt på en oppgave, med oppgavens planlagte innsatstimer. Dynamics 365 Project Operations bruker følgende formler til å beregne sporingsmåledata:

- **Fremdriftsprosent**: Faktisk innsats brukt til dags dato ÷ sluttestimat (EAC) 
- **Resterende innsats**: Estimert innsats ved fullføring – faktisk innsats brukt til dags dato 
- **EAC**: Resterende innsats + faktisk innsats brukt til dags dato 
- **Forventet innsatsavvik**: Planlagt innsats – EAC

Project Operations viser en projeksjon av innsatsvariasjonen for oppgaven. Hvis EAC er større enn den planlagte innsatsen, blir oppgaven beregnet til å ta mer tid enn det som opprinnelig ble planlagt, og er etter tidsplanen. Hvis EAC er mindre enn den planlagte innsatsen, blir oppgaven beregnet til å ta mindre tid enn det som opprinnelig ble planlagt, og er foran tidsplanen.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Projisere innsats på nytt for bladnodeoppgaver

Prosjektleder reviderer ofte de opprinnelige beregningene på en aktivitet. Reprojisering av prosjekter er en prosjektleders oppfatning av estimater, gitt gjeldende status for et prosjekt. Vi anbefaler imidlertid ikke at prosjektledere endrer tallene for planlagt innsats. Dette skyldes at prosjektplanleggingen representerer den etablerte sannhetskilden til prosjektplanen og kostnadsestimatet, og alle prosjektinteressentene har godtatt den.

En prosjektleder kan projisere innsats på oppgaver på nytt ved å oppdatere standardverdien for **Resterende innsats** med et nytt overslag for aktiviteten. Denne oppdateringen fører til en omberegning av oppgavens estimat ved fullføring, fremdriftsprosenten og det beregnede innsatsavviket for en oppgave. EAC, ETC- og fremdriftsprosenten på aktivitetssammendragene beregnes også på nytt, og det lages en ny projisering av innsatsavvik.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Reprojisering av innsats i aktivitetssammendrag

Innsats i aktivitetssammendrag eller beholderaktivitet kan projiseres på nytt. Prosjektledere kan oppdatere gjenværende innsats i sammendragsoppgavene. Oppdatering av gjenværende innsats utløser følgende sett med beregninger i programmet:

- EAC og fremdriftsprosent for aktiviteten beregnes.
- Den nye EAC fordeles i de underordnede aktivitetene i samme proporsjon som den opprinnelige EAC var på aktiviteten.
- Den nye EAC for hver av de individuelle aktivitetene ned til bladnodeoppgavene blir beregnet. 
- De berørte underordnede oppgavene til bladnodene får gjenstående innsats og fremdriftsprosenten beregnet på nytt basert på EAC-verdien. Dette fører til en ny projeksjon for innsatsavviket i aktiviteten. 
- EAC-er for aktivitetssammendragene helt til rotnoden beregnes på nytt.


## <a name="project-status-summary"></a>Oppsummering av prosjektstatus

Sporingsdata i visningene **Innsatssporing** og **Kostnadssporing** viser fremdrift og kostnadsforbruk på oppgavenivåene prosjektrotnode, aktivitetssammendrags og bladnode. **Status**-delen på siden **Prosjektenhet** viser et sammendrag av status på prosjektnivå.

## <a name="status-summary-fields"></a>Statussammendragsfelt

Feltet **Generell prosjektstatus** er et redigerbart felt som viser den generelle statusen til prosjektet. Det bruker fargekoding, for eksempel grønn, gul og rød, for å vise økende risikoer. Med **Kommentarer**-feltet kan prosjektlederen angi spesifikke kommentarer om statusen. Feltet **Status oppdatert** er ikke redigerbart, og verdien er et tidsstempel som angir når statusen sist ble oppdatert.

Feltene **Tidsplanytelse** og **Kostnadsytelse** angis fra sporingsdatoen. Når tidsplan- og kostnadsavviket for rotnoden i visningen **Innsatssporing** er positive, kan du angi disse feltene til **Foran**. Når tidsplan- og kostnadsavviket for rotnoden er negativ, kan du angi dem til **Bak**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
