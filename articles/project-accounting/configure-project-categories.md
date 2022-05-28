---
title: Konfigurere prosjektkategorier
description: Denne emnet gir informasjon om konfigurering av prosjektkategorier.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 94b66feef4164f3cd52d5fe917071647f731b047
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591554"
---
# <a name="configure-project-categories"></a>Konfigurere prosjektkategorier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations tilbyr kraftige funksjoner for kategorisering av omsetning og utgifter på prosjekter. Kategorier gir mulighet til å rapportere og analysere prosjekttransaksjoner, og å postere til hovedboken.

Følgende diagram illustrerer korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier. 

Transaksjonskategorier er den grunnleggende grupperingen av prosjekttransaksjoner. I denne grupperingen finnes det et sett med delte kategorier som kan deles på tvers av programmer og moduler. For å bli enda mer spesifikk er prosjektkategorier det mest detaljerte nivået av kategorier. Prosjektkategorier er spesifikke for juridisk enhet, modul og program.

![Korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier.](media/project-categories.png)

## <a name="transaction-categories"></a>Transaksjonskategorier

Transaksjonskategorier representerer den grunnleggende grupperingen av prosjekttransaksjoner, og er ikke firma- eller transaksjonstypespesifikk. Ekeli bruker for eksempel kategoriene Design, Reise, Installasjon og Servicetransaksjon til å gruppere prosjekttransaksjoner.

Transaksjonskategorier defineres i Project Operations-modulen. 
1. Gå til **Innstillinger** \> **Transaksjonskategorier** for å åpne skjemaet. 
2. Opprett en ny transaksjonskategori enten ved å velge **Ny** eller ved å velge **Importer fra Excel**.

## <a name="shared-categories"></a>Delta kategorier

Dynamics 365 bruker konseptet Delte kategorier til å kategorisere utgifter i forskjellige apper, for eksempel Dynamics 365 Finance, Dynamics 365 Supply Chain og Dynamics 365 Project Operations. For hver transaksjonskategori som opprettes, oppretter Project Operations automatisk fire relaterte delte kategorier: timer, utgift, avgifter og vare. Du kan se gjennom og justere de delte kategoriene ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Delte kategorier**.

## <a name="project-categories"></a>Prosjektkategorier

Prosjektkategorier representerer det mest detaljertenivået av kategorikonfigurasjon, og må konfigureres separat og for hvert selskap av en prosjektregnskapsfører.

1. Gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Prosjektkategorier**.
2. Velg **Ny**.
3. Velg **Kategori-ID** for den delte kategorien du opprettet i den forrige delen. Project Operations tillater bare bruk av de delte kategoriene som er tilknyttet transaksjonskategorier.
4. Velg en kategorigruppe.

## <a name="category-groups"></a>Kategorigrupper

Kategorigrupper brukes til å dele egenskaper, primært postering av profiler, mellom relaterte prosjektkategorier. Det må finnes minst én kategorigruppe for hver transaksjonstype, og hver prosjektkategori er tilordnet en gruppe.

Posteringsspesifikasjonene i Project Operations er definert av reglene for prosjektkostnader og omsetning, prosjektkategoriene og kategorigruppene. Du kan konfigurere kategorigrupper ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Kategorigrupper**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]