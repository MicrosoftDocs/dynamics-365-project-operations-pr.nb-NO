---
title: Mobilappen Project Timesheet
description: Dette emnet viser informasjon om Microsoft Dynamics 365 Project Timesheet-mobilappen. Med mobilappen Project Timesheet kan brukere sende og godkjenne timeregistreringer for prosjekter på den mobile enheten.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081793"
---
# <a name="project-timesheet-mobile-application"></a>Mobilappen Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

Med mobilappen Microsoft Dynamics 365 Project Timesheet kan brukere sende og godkjenne timeregistreringer for prosjekter på den mobile enheten (iPhone eller Android). Denne mobilappen viser timeregistreringsfunksjonen i prosjektstyrings- og regnskapsområdet i Dynamics 365 Finance, som forbedrer brukerproduktiviteten og -effektiviteten samt aktivering av driftstid og godkjenning av prosjekttimeregistreringer.

## <a name="download-and-install-the-mobile-app"></a>Laste ned og installere mobilappen

Last ned og Installer Microsoft Dynamics 365 Project Timesheet-mobilappen for Android eller iPhone fra mobilbutikken for enheten.

## <a name="enable-the-app"></a>Aktivere appen 

I Finance må Project Timesheet-mobilappen være aktivert. Hvis du vil aktivere funksjonaliteten, går du til **Parametere for prosjektstyring og regnskap \> Timeregistrering** og velger **Aktiver Microsoft Dynamics 365 Project Timesheet**-parameteren.

## <a name="sign-in-to-the-app"></a>Logge på appen

1.  Start appen på mobilenheten.

2.  Angi Finance-URL-en.

3.  Første gang du logger deg på, blir du bedt om å oppgi brukernavn og passord. Angi legitimasjonen din.

4.  Du blir logget på standardfirmaet ditt.

## <a name="submit-a-project-timesheet"></a>Sende inn en prosjekttimeregistrering

Du kan opprette og sende en prosjekttimeregistrering i appen. Du kan basere en ny timeregistrering på informasjon fra en tidligere timeregistrering, lagrede linjer eller prosjekttilordninger. Hvis du er angitt som representant, kan du også angi en timeregistrering for en annen arbeider. Hvis du vil opprette en timeregistrering som en representant, velger du **Meny**-knappen, og deretter velger du et ressursnavn.

Timeregistreringssiden vil opprette en ny timeregistrering for time registreringsperioden, basert på gjeldende dato. Arbeidsuken vises. Hvis timeregistreringsperioden dekker flere uker, kan du velge en annen arbeidsuke fra kategoriene for arbeidsuke.
Hvis det finnes en timeregistrering for gjeldende dato, vises den. Hvis du må opprette en ny timeregistrering i en annen timeregistreringsperiode, velger du **Meny**-knappen og velger deretter **Ny timeregistrering**.

Du kan skrive inn prosjektinformasjon ved å klikke handlingen **Legg til tid** eller handlingen **Kopier tid fra**. **Kopierings tid fra**-handlingen vil kopiere prosjektlinjeinformasjon, men ikke timene. Menyen **Kopier tid fra** inneholder følgende alternativer:

- **Kopier fra eksisterende timeregistrering** – Kopier timeregistreringslinjer fra en eksisterende timeregistrering.

- **Kopier fra favoritter** – Opprett nye timeregistreringslinjer ved hjelp av innstillingene for timeregistrering som du valgte som favoritter.

- **Kopier fra tilordning** – Opprett nye timeregistreringslinjer fra tilordnede prosjekter.

Prosjektinformasjonen som vises, er avhengig av mobilparameterne du definerte på siden **Parametere for prosjektstyring og regnskap**.

I feltet **Juridisk enhet** velger du den juridiske enheten du utførte prosjektarbeid for. Fletet **Juridisk enhet** er bare tilgjengelig hvis støtte for konsernintern timeregistrering er aktivert for den juridiske enheten.

Velg kunden som er knyttet til prosjektet for timeregistreringen. For den første versjonen på Android støttes ikke oppføring etter kunde, siden du må velge prosjektet først. Hvis du valgte prosjektet først, fylles **Kunde**-feltet ut automatisk.

I **Prosjekt**-feltet velger du prosjektet du angir tid for. **Kunde**-feltet fylles ut automatisk.

Kunde- og prosjektoppslag gjør det mulig å søke på tvers av både kunder og prosjekter.

Velg informasjon i feltene **Kategori**, **Aktivitet**, **Linjeegenskap**, **Mva-gruppe** og **Merverdiavgiftsgruppe for vare**. Disse feltene kan overstyres.

Feltet **Linjeegenskap** settes til en standardverdi basert på prosjektstyrings- og regnskapsparametere. Når parameterne for prosjekt/kategori og kategori/ressurs er aktivert, settes verdien for **Linjeegenskap** til standardverdien du har definert for denne valideringen. Når parameterne for prosjekt/kategori og kategori/ressurs ikke er aktivert, settes verdien for **Linjeegenskap** til standard i henhold til feltet **Aktiver standard linjeegenskap** på siden **Parametere for prosjektstyring og regnskap**. Verdien **Linjeegenskap** kan overstyres.

Velg en dag for å legge til en tid. Skriv inn antall timer du arbeidet hver dag.

Hvis du vil legge til kommentarer om timene du skriver inn, klikker du **Legg til kommentarer**, og deretter skriver du inn kommentarer for en intern målgruppe, kundemålgruppe eller begge.
Interne kommentarer kan vises av prosjektledere. Kundekommentarer inkluderes på fakturaer.

Hvis du vil lagre linjen som en favoritt, merker du av, og deretter klikker du **Lagre som favoritt**.

Støtte for finansdimensjon og vedlegg finnes ikke i mobilappen.

Fortsett med å legge til prosjektlinjer etter behov for å fullføre timeregistreringen.

Klikk **Send** for å sende timeregistreringen til godkjenningsarbeidsflyten.

## <a name="review-timesheets"></a>Gå gjennom timeregistreringer

En liste over timeregistreringene som må gjennomgås, er tilgjengelig på menyen. Dette alternativet er bare tilgjengelig hvis du er angitt som en arbeidsflytgodkjenner. Både overskrifts- og linjegodkjenning støttes. Godkjenning på linjenivå gir mulighet til å merke én eller flere linjer for godkjenning. Når du har gått gjennom timeregistreringsinformasjonen, klikker du **Godkjenn**, **Deleger** eller **Retur** for å fortsette arbeidsflyten.
