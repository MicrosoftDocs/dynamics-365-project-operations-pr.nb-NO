---
title: Konfigurere prosjektkategorier
description: Denne emnet gir informasjon om konfigurering av prosjektkategorier.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131940"
---
# <a name="configure-project-categories"></a>Konfigurere prosjektkategorier

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Project Operations tilbyr kraftige funksjoner for kategorisering av omsetning og utgifter på prosjekter. Kategorier gir mulighet til å rapportere og analysere prosjekttransaksjoner, og å postere til hovedboken.

Følgende diagram illustrerer korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier. 

Transaksjonskategorier er den grunnleggende grupperingen av prosjekttransaksjoner. I denne grupperingen finnes det et sett med delte kategorier som kan deles på tvers av programmer og moduler. For å bli enda mer spesifikk er prosjektkategorier det mest detaljerte nivået av kategorier. Prosjektkategorier er spesifikke for juridisk enhet, modul og program.

![Korrelasjonen mellom transaksjonskategorier, delte kategorier og prosjektkategorier](media/project-categories.png)

## <a name="transaction-categories"></a>Transaksjonskategorier

Transaksjonskategorier representerer den grunnleggende grupperingen av prosjekttransaksjoner, og er ikke firma- eller transaksjonstypespesifikk. Ekeli bruker for eksempel kategoriene Design, Reise, Installasjon og Servicetransaksjon til å gruppere prosjekttransaksjoner.

Transaksjonskategorier defineres i Project Operations-modulen. 
1. Gå til **Innstillinger** \> **Transaksjonskategorier** for å åpne skjemaet. 
2. Opprett en ny transaksjonskategori enten ved å velge **Ny** eller ved å velge **Importer fra Excel**.

## <a name="shared-categories"></a>Delta kategorier

Dynamics 365 bruker delte kategorier til å kategorisere utgifter i forskjellige programmer, for eksempel Dynamics 365 Finance, Dynamics 365 Supply Chain og Dynamics 365 Project Operations. For hver transaksjonskategori som opprettes, oppretter Project Operations automatisk fire relaterte delte kategorier: timer, utgift, avgifter og vare. Du kan se gjennom og justere de delte kategoriene ved å gå til **Prosjektstyring og regnskap** \> **Oppsett** \> **Kategorier** \> **Delte kategorier**.

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