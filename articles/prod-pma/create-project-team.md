---
title: Opprette et prosjektteam
description: Dette emnet gir informasjon om hvordan du oppretter og administrerer prosjektteam.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f134d7566954e640eea8ff8af98e184273ad570c
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683044"
---
# <a name="create-a-project-team"></a>Opprette et prosjektteam

[!include [banner](../includes/banner.md)]

Hvis du vil bruke rollene som ble opprettet tidligere i et prosjekt, må en prosjektleder knytte rollene til prosjektet. Det kan tilordnes flere roller for et prosjekt. Disse rollene blir automatisk merket under reservering for å unngå forvirring. Hvis prosjektlederen for eksempel krever tre ingeniører, genereres det automatisk tre programvareingeniørroller som har **programvareingeniør 1**, **programvareingeniør 2** og **programvareingeniør 3** som etikett. Hvis rolleegenskaper er angitt tidligere for rollen, brukes de som et filter under søk etter en ressurs. Du kan legge til flere karakteristikker som kreves for å presisere søket ytterligere.

Visningsinnstillinger kan også tilpasses for å gi en bedre visning av ressurstilgjengelighet. Det finnes alternativer for å vise tilgjengelighet for time, dag, uke, måned, kvartal og år. Det finnes også et alternativ for å vise tilgjengelig og gjenstående kapasitet på ressurser. Dette alternativet er nyttig for tidsstyring når du beregner tilgjengelig tid for aktiviteter eller ressurstilgjengelighet.

Prosjektlederen kan velge en rolle på siden og deretter velge å reservere en ressurs som fyller rollen, hvis det er en tilgjengelig ressurs som passer til kravet. Vær oppmerksom på at ressursene ikke må reserveres på dette tidspunktet i planleggingsfasen. Når du oppretter en WBS, kan du erstatte roller med bemannede ressurser for prosjektet. Hvis roller erstattes med bemannede ressurser i WBS, oppdaterer ressursoppsettet automatisk prosjektgruppens liste og planlegging.

[![Prosjektteamoppføring som inkluderer både roller og faktiske ressurser.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Prosjektlederen har forskjellige alternativer for bestilling av en ressurs for et prosjekt, for eksempel **Gjenstående kapasitet**, **Full kapasitet**, **Kapasitet i prosent** og **Angi timer**. Disse bestillingsalternativene kan kanselleres når som helst hvis ressurstilordningene endres. To typer bestillinger støttes:

- **Forpliktende bestilling** – Ressursreservasjonen ble godkjent og bekreftet til å fungere på avtalene for den angitte varigheten.
- **Ikke-forpliktende bestilling** – Ressursreservasjonene ble foreløpig angitt til å fungere på avtalene for den angitte varigheten.

Fremgangsmåten nedenfor forklarer hvordan du oppretter et prosjektteam.

## <a name="create-a-project-team"></a>Opprette et prosjektteam

1. På listesiden **Alle prosjekter** velger du et prosjekt, og deretter velger du **Rediger**.
2. I kategorien **Prosjektteam og planlegging** i feltet **Planlegg sluttdato** angir du startdato pluss én måned. Hvis for eksempel startdatoen for tidsplanen er 24. juni 2017 (24/06/2017), angir du **24/07/2017**.
3. Velg **Legg til**.
4. I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Overordnet prosjektleder**.
5. Velg **Nødvendige kompetanser**.
6. På siden **Velg egenskaper** velges egenskapene som du tidligere har angitt for rollen overordnet prosjektleder, som standard. Velg **OK**.
7. På siden **Legg til roller i prosjektet**, i feltet **Antall ressurser**, angir du **1**.
8. I **Ressurs**-feltet viser oppslaget alle ressurser som har de nødvendige kompetansene. Velg **Daniel Goldschmid**, og velg deretter **Opprett**.
9. Velg **Legg til** på siden **Prosjekt**.
10. I ruten **Legg til roller i prosjektet** i feltet **Rolle** velger du **Teammedlem**. I feltet **Antall ressurser** angir du **5**.
11. Velg **Opprett**.
12. På siden **Prosjekter** velger du **Fullfør ressurs**.

## <a name="monitor-project-teams"></a>Overvåke prosjektteam
1. På siden **Alle prosjekter** velger du koblingen **Prosjekt-ID** for prosjektet **XYZ-oppgraderingsfase 2**.
2. På hurtigfanen **Prosjektteam og planlegging** kontrollerer du at prosjektressursene som vises, er riktige.


[!INCLUDE[footer-include](../includes/footer-banner.md)]