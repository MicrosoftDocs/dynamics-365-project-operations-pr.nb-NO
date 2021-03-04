---
title: Definere prosjektressurser
description: Dette emnet gir informasjon om å sette opp eller be om prosjektressurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081792"
---
# <a name="set-up-project-resources"></a>Definere prosjektressurser

[!include [banner](../includes/banner.md)]

Du må sette opp en kalender og knytte den til en ansatt eller en arbeider. Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet. Under kalenderinstallasjonen kan prosjektledere utføre ressursutjevning som en del av ressursoptimaliseringen. Restriksjoner kan brukes på ressurser basert på kalendertidsplanen. Du kan sette opp en kalender på **Kalenderere** -siden.

Når du definerer en arbeider som en prosjektressurs, kan du velge blant arbeidere som arbeider i firmaet som du konfigurerer ressurser for. Du kan også velge arbeidere fra andre selskaper i organisasjonen. Disse arbeiderne kalles konserninterne ressurser.

Fremgangsmåten nedenfor forklarer hvordan du konfigurerer en arbeider som en prosjektressurs i firmaet, og hvordan du oppretter en konsernintern prosjektressurs.

## <a name="set-up-a-worker-as-a-project-resource"></a>Konfigurere en arbeider som en prosjektressurs

1. På siden **Arbeidere** i listen **Arbeidere** velger du arbeideren som du legger til som prosjektressurs, og åpner arbeideroppføringen.
2. I handlingsruten velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.
3. Velg en kalender, og lukk deretter siden.

Du kan også angi standardprosjekter for en ressurs som en type forhåndstilordning. Forhåndstildelinger kan brukes når ressurslederen eller prosjektlederen vet hvilke prosjekter ressursen skal jobbe med på forhånd. Forhåndstildelinger kan også være basert på forespørselen fra en prosjektsponsor eller kunde. Hvis du vil forhåndstilordne et prosjekt, velger du det gjeldende prosjektet på siden **Tilordne prosjekter** i kategorien **Prosjekter** på listen **Gjenværende prosjekter**.

## <a name="set-up-an-intercompany-resource"></a>Konfigurere en konsernintern ressurs

Når du definerer en arbeider som en konsernintern ressurs, må du fullføre oppsettet i både utlånsselskapet og lånefirmaet.

### <a name="in-the-lending-company"></a>I utlånsfirmaet

1. Kontroller at utlånsfirmaet er valgt i Finance, og fullfør deretter fremgangsmåten i forrige del, "Konfigurere en arbeider som en prosjektressurs".
2. På siden **Konserninternt regnskap** velger du **Ny**.
3. I feltet **ID for juridisk enhet** velger du utlånsselskapet. Fyll ut de gjenværende feltene etter behov, og velg **Lagre**.
4. På siden **Overføringspris** velger du **Ny**.
5. I feltet **Juridisk enhet som låner** velger du riktig selskap.
6. Hvis du vil låne låneselskapet bare ressursen du opprettet i begynnelsen av denne delen, velger du navnet på ressursen du opprettet, i **Ressurs** -feltet. Hvis du vil gjøre alle ressursene i utlånsfirmaet tilgjengelige for lånefirmaet, lar du **Ressurs** -feltet stå tomt.
7. På siden **Parametere for prosjektstyring og regnskap** , i kategorien **Konsernintern** , setter du **Aktiver konsernintern ressursplanlegging og timeregistreringer** til **Ja**.

### <a name="in-the-borrowing-company"></a>I lånefirmaet

- På siden **Ressursliste** , i søkefilteret, skriver du inn navnet på ressursen du opprettet for utlånsfirmaet, for å kontrollere at navnet er inkludert i ressurslisten for lånefirmaet.

## <a name="request-project-resources"></a>Be om prosjektressurser
Funksjonaliteten for planlegging av prosjektressurser gjør det bare for ressursledere å distribuere bemannede ressurser på engasjementer eller prosjekter. Hvis du vil aktivere denne funksjonaliteten, må du utføre følgende oppgaver eller kontrollere at de er fullført:

- Angi nummerserier.
- Konfigurere prosjektstyrings- og regnskapsflyter.
- Aktivere ressursforespørselsflyter.

Når de foregående oppgavene er fullført, kan du utføre følgende oppgaver slik du ønsker:

- Opprett en ressursforespørsel fra en uforpliktende bemannet ressurs.
- Overvåk ressursforespørsler.
- Oppfyll ressursforespørsler.
- Be om en bemannet ressurs fra en WBS.
- Reserver ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.


[!INCLUDE[footer-include](../includes/footer-banner.md)]