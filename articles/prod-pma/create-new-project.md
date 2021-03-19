---
title: Opprett et nytt prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter et nytt prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270735"
---
# <a name="create-a-new-project"></a>Opprett et nytt prosjekt

[!include [banner](../includes/banner.md)]

Fullfør fremgangsmåten nedenfor for å opprette et nytt prosjekt.

1. På siden **Prosjektledelse** velger du **Nytt prosjekt**, og angi følgende verdier:

    - **Prosjekttype:** Tid og materiale
    - **Prosjektnavn:** XYZ-oppgraderingsfase 2
    - **Prosjektgruppe:** TM\_VIA
    - **Prosjektkontrakt-ID:** 00000002

2. Velg **Opprett prosjekt**.

## <a name="assign-a-resource-to-a-project"></a>Tilordne en ressurs til et prosjekt

1. På siden **Arbeidere** i listen **Arbeidere** velger du oppføringen for arbeideren som du tidligere konfigurerte kompentanser for, åpne arbeideroppføringen.
2. I handlingsruten i kategorien **Prosjekt** i gruppen **Oppsett** velger du **Tilordne prosjekter**.
3. På siden **Prosjekttilordninger for ressursvalidering** i kategorien **Prosjekt** i feltet **Legg til prosjekt i valgte prosjekter** filtrerer du på prosjektet **XYZ-oppgraderingsfase 2**.
4. I ruten **Gjenstående prosjekter** velger du et prosjekt, og deretter velger du pilknappen for å legge den til i ruten **Valgte prosjekter**.

Du kan også tilordne kategorier for en ressurs slik du ønsker. Kategoritypen er enten **Kostnad** eller **Omsetning**. Kategoritypen bestemmes av organisasjonen. Hvis ingen kategorier er tilordnet en ressurs, slår Finance opp standardkategorien på timepriser for kostnad og omsetning.

## <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurere egenskaper for prosjektressurs og rolle

En prosjektleder kan bruke prosjektbemanningsfunksjonaliteten til å opprette rollene som kreves for prosjektet. Roller kan brukes hvis bekreftede ressurser fremdeles er ukjente når ressurser blir reservert. Roller kan være midlertidig reservert som planlagte ressurser, slik at du kan fortsette planleggingen av prosjektplanlegging.

[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso ble engasjert for å fullføre et Tid og materiale-prosjekt som har et godkjent prosjektcharter. Juniorprosjektlederen holder fremdeles på med å ferdigstille prosjektomfanget. Ressurslederen identifiserer for øyeblikket bestemte ressurser som blir reservert for å arbeide med det nye prosjektet. På grunn av den kritiske prosjekttypen ba prosjektsponsoren om at den overordnede prosjektlederen kunne ha én av rollene. Ressurslederen må skaffe den nye ressursen og definere rollen i systemet i tilfelle juniorprosjektlederen krever ressursinformasjon under planleggingen av prosjektet.

Fremgangsmåten nedenfor viser hvordan ressurslederen kan konfigurere rollen som overordnet prosjektleder og knytte ressursegenskaper til den. Senere kan rollen brukes til å søke etter tilgjengelige ressurser som samsvarer med de nødvendige ressurskompetansene.

1. På siden **Konfigurer roller** velger du **Ny**, og angi følgende verdier:

    - **Rolle-ID:** Overordnet prosjektleder
    - **Beskrivelse:** Overordnet prosjektleder

2. Velg **Opprett**.
3. Velg rollen **Overordnet prosjektleder**, og velg deretter **Konfigurer egenskaper**.
4. I feltet for **Type kjennetegn** velger du **Ferdighet**.
5. I feltet **Tilgjengelige kjennetegn** angir du ferdigheten du vil søke etter.
6. I feltet for **Type kjennetegn** velger du **Sertifikat**.
7. I feltet **Tilgjengelige kjennetegn** angir du sertifikattypen du vil søke etter.

## <a name="assign-a-project-resource-to-a-project"></a>Tilordne en prosjektressurs til et prosjekt

1. På siden **Alle prosjekter** velger du **XYZ-oppgraderingsfase 2**-prosjektet.
2. I kategorien **Prosjektteam og planlegging** velger du **Legg til**.
3. I feltet **Rolle** velger du **Teammedlem**.
4. Velg **Bestill fra kalender**.
5. På siden **Ressurstilgjengelighet** velger du **Visningsinnstillinger**.
6. Angi følgende verdier på siden **Juster visningsinnstillinger**:

    - **Format for visning av datoområde:** Dag
    - **Vis tilgjengelighetsbeskrivelser:** Ja
    - **Vis gjenstående kapasitet:** Ja

7. Velg en ressurs fra listen over ressurser.
8. Velg **Forpliktende bestilling** og **Full kapasitet**.

## <a name="assign-a-resource-to-a-default-role"></a>Tilordne en ressurs til en standardrolle

For å hjelpe kan prosjekt- og ressursledere drille ned ytterligere på ressursene som kan reserveres for et prosjekt. Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig innhentet ressurs. Når Daniel for eksempel ble leid inn, hadde han erfaringen og ferdighetene til å fylle rollen som forretningsanalytiker. Ressursbehandleren tilordnet denne rollen som Daniels standardrolle. Derfor har ressurslederen lagt til Daniel i en pulje av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.

Under ressursreservasjon kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter. De kan bruke denne informasjonen som ett vilkår når de utfører beslutningsanalyse med flere vilkår under ressursfullføring. De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har spesifikke ferdigheter, utdanning og erfaring for et gitt prosjekt.

**Scenario:** Et godkjent prosjekt har startet, og rollen overordnet prosjektleder er reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen. Ressursbehandleren har nå hentet en ressurs for å fullføre rollen overordnet prosjektleder.

1. På siden **Ressursliste** velger du **Daniel Goldschmidt**.
2. På siden **Ressursrolle** velger du **Ny**, og angi følgende verdier:

    - **Gyldig:** ngi gjeldende dato.
    - **Utløp:** Angi **Aldri**.
    - **Rolle-ID**: Angi **Overordnet prosjektleder**.

3. Velg **Lagre**, og lukk deretter siden.
4. I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og sertifikatet **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]