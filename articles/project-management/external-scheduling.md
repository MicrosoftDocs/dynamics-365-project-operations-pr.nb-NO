---
title: Ekstern planlegging
description: Denne artikkelen inneholder informasjon om ekstern planlegging.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736969"
---
# <a name="external-scheduling"></a>Ekstern planlegging

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Med modusen for ekstern planlegging kan du opprette, oppdatere og slette enheter som er knyttet til arbeidsnedbrytningsstrukturer (WBS-er), men uten gjeldende grenser som håndheves av Microsoft Project for the Web. Den gir også begrenset validering. Denne modusen kan bare brukes av følgende kunder:

- Kunder som har verktøyene som kreves for å definere en WBS utenfor planleggingslogikken som leveres av Project Operations
- Kunder som må administrere tidsplanhierarki, avhengigheter eller oppgavevarighet

> [!IMPORTANT]
> Det kan hende at data som ikke er riktig angitt i de WBS-relaterte enhetene, ikke gjengis i rutenettet for ressursavstemming, rutenettet for estimater, rutenettet for sporing eller rutenettet for ressurstilordning.

## <a name="configuration"></a>Configuration

Denne funksjonen er aktivert som standard. På den bruksklare hovedsiden for prosjekter er imidlertid ikke det relaterte feltet synlig som standard. Hvis du vil aktivere feltet, åpner du hovedsiden for prosjektenheten i Maker-portalen, velger feltet **Planleggingsmotor** og endrer deretter feltet til **Synlig som standard**. Hvis du ikke bruker den bruksklare hovedsiden for prosjekt, redigerer du den eksisterende siden og legger til feltet **Planleggingsmotor** på den.

## <a name="settings"></a>Innstillinger

Hvis du vil bruke modusen for ekstern planlegging, må du først opprette et nytt prosjekt og velge planleggingsmotoren **Eksternt planlagt** i rullegardinlisten på hovedsiden for prosjekt. Etter at denne modusen er konfigurert for et prosjekt, kan den ikke endres.

## <a name="viewing-the-wbs"></a>Vis WBS-en

Hvis et prosjekt er eksternt planlagt, er tilgang til Project for the Web begrenset for dette prosjektet. Hvis du vil vise WBS-en, må du gå til rutenettet for sporing, der hele WBS-en vises.

## <a name="creating-and-editing-the-wbs"></a>Opprett og rediger WBS-en

Hvis ekstern planlegging er aktivert for et prosjekt, må du definere dataene for alle WBS-relaterte enheter, inkludert oppgaver, teammedlemmer, ressurstilordninger og avhengigheter.

Illustrasjonen nedenfor viser datamodellen for prosjektplanlegging.

![Datamodell for prosjektplanlegging.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Funksjonsbegrensninger

Følgende operasjoner er ikke tillatt i eksternt planlagte prosjekter.

### <a name="project-planning"></a>Prosjektplanlegging

- **Kopier prosjekt** – Denne operasjonen støttes ikke i eksternt planlagte prosjekter.
- **Flytt prosjekt** – Endring av startdatoen til et prosjekt, flytter ikke starten på oppgaver eller ressurstilordninger i WBS-en.
- **Oppdatering av prosjektbehandlingen** – Endringer i prosjektbehandlingen på hovedsiden for prosjekt oppretter ikke automatisk et nytt prosjektteammedlem før prosjektet er konvertert.
- **Oppdatering av prosjektets arbeidstidsmal** – Endringer i prosjektets arbeidstidsmal beregner ikke tidsplanen for prosjektet på nytt.
- **Ressurstilordningsomfang** – Oppretting av ressurstilordninger oppdaterer ikke **mdyn\_PlannedWork**-feltet automatisk. Dette feltet brukes til å lagre omfang for ressurstilordningsarbeid. Hvis du viser tidsfaset arbeid i rutenettet for ressurstilordning eller i rutenettet for ressursavstemming, må du definere gyldige omfang for ressurstilordning. Disse omfangene må formateres riktig, slik at de utløser beregning av både kostnadsomfang og salgsprisomfang. Vi anbefaler at du oppretter et testprosjekt som planlegges av Project for the Web og deretter ser gjennom de tilknyttede dataene for å bekrefte kravene og formateringen.

### <a name="resource-management"></a>Ressursstyring

- **Fullføring av generell ressurs** – Fullføring av generell ressurs støttes ikke for eksternt planlagte prosjekter. Forsøk på å oppfylle aktive åpne behov oppretter nye prosjektteammedlemmer, men det sletter ikke det generelle teammedlemmet eller erstatter det generelle teammedlemmet i eventuelt eksisterende ressurstilordninger.
- **Slett teammedlem** – Sletting av et teammedlem sletter ikke ressurstilordninger automatisk.

### <a name="quoting-and-contracting"></a>Tilbudsgiving og kontrahering

- **Import av detaljer for tilbudslinje og kontraktlinje** – Når detaljer for tilbuds- eller kontraktlinje importeres fra et prosjekt, støtter programmet maksimalt 500 oppgaver i WBA i henhold til tester, basert på en grense på 20 tilordninger per oppgave.

### <a name="actuals-and-invoicing"></a>Faktiske verdier og fakturering

- Selv om det ikke er noen endringer i eksisterende valideringer mellom WBS og økonomiske transaksjoner, er det viktig at du holder deg til den bruksklare datamodellen, for å sikre at alle nedstrøms transaksjoner kjører som forventet.
