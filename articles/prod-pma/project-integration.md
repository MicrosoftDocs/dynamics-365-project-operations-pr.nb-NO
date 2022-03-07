---
title: Integrasjon med Microsoft Project Client
description: Det kan være komplisert å planlegge og vedlikeholde en prosjektplan, så prosjektledere trenger å bruke verktøy som hjelper dem med å administrere denne oppgaven. Integrasjon med Microsoft Project Client gir støtte for å åpne og administrere en arbeidsnedbrytningsstruktur for et prosjekt.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: b312ec5b1f4e6a98a2cbf1667b2f55b758b2d613
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269847"
---
# <a name="microsoft-project-client-integration"></a>Integrasjon med Microsoft Project Client

[!include [banner](../includes/banner.md)]

Det kan være komplisert å planlegge og vedlikeholde en prosjektplan, så prosjektledere trenger å bruke verktøy som hjelper dem med å administrere denne oppgaven. Integrasjon med Microsoft Project Client gir støtte for å åpne og administrere en arbeidsnedbrytningsstruktur for et prosjekt. Prosjektlederen kan publisere eventuelle endringer tilbake til arbeidsnedbrytningsstrukturen for Dynamics 365 Finance-prosjektet.

> [!NOTE]
> Hvis du bruker juli-oppdateringen (versjon 10.0.4), må du installere KB 4054797 og 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Konfigurere tilleggsprogrammet Microsoft Project Client
Hvis du vil aktivere integreringen med Microsoft Project Client, må et Microsoft Dynamics 365-tillegg installeres i brukerens klient for Microsoft Project-programmet. Dette gjøres ved å åpne **Arbeidsområdet for prosjektstyring**.

•   Klikk **Konfigurer prosjektklienttillegg** fra delen **Koblinger** > **Oppsett** i arbeidsområdet.

•   Klikk **Åpne**, og klikk deretter **Kjør** når du blir bedt om det.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Åpne og rediger et eksisterende utkast for en arbeidsnedbrytningsstruktur i Microsoft Project Client
Hvis et prosjekt i Dynamics 365 Finance allerede har opprettet en arbeidsnedbrytningsstruktur, kan arbeidsnedbrytningsstrukturen åpnes i Microsoft Project Client-programmet hvis arbeidsnedbrytningsstrukturen er i utkaststatus. Hvis du vil åpne fra **Prosjekt**-siden, klikker du **Åpne i Microsoft Project**-koblingen i kategorien **Plan**. Du kan også åpne denne siden i Microsoft Project Client-programmet ved å klikke **Åpne** i kategorien **Microsoft Dynamics 365**. Velg **Juridisk enhet** og **Prosjekt** fra listen.

> [!NOTE]
> Hvis du bruker Internet Explorer som webleser, må du klikke **Lagre** for å åpne manuelt fra plasseringen som filen er lastet ned til. Du kan også klikke **Lagre og åpne** for å åpne filen i Microsoft Project Client. Ikke gi nytt navn til filen når du lagrer.

Før du redigerer filen ved hjelp av Microsoft Project Client, må du sjekke den ut. Klikk **Sjekk ut** i kategorien **Microsoft Dynamics 365**. Dette hindrer at andre brukere kan redigere arbeidsnedbrytningsstrukturen fra Finance samtidig. Hvis du vil publisere arbeidsnedbrytningsstruktur etter at du har fullført eventuelle redigeringer, klikker du **Sjekk inn** i kategorien **Microsoft Dynamics 365**.

Hvis et prosjektteam allerede er lagt til i prosjektet i Finance, vil ressurslisten fylles ut med teammedlemmene. Hvis et prosjektteam ennå ikke er lagt til i prosjektet, kan du velge ressurser og bygge teamet i Microsoft Project Client ved å klikke **Ressurser**-knappen i kategorien **Microsoft Dynamics 365**. 

Følgende data blir synkronisert til Finance som en del av innsjekkingsprosessen:

•   Aktivitetsnavn

•   Startdato

•   Sluttdato

•   Foregående oppgaver

•   Ressursnavn

•   Fane

•   Ressurskategori

•   Arbeidstimer

•   Merknader

•   Prioritet

> [!NOTE]
> Hvis du legger til andre kolonner i Microsoft Project Client-filen, blir de ikke lagret i filen, og vises ikke når filen åpnes på nytt.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Opprette arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project Client
Slik oppretter du en ny arbeidsnedbrytningsstruktur ved hjelp av Microsoft Project Client:


1.  Åpne Microsoft Project Client.

2.  I kategorien **Microsoft Dynamics 365** klikker du **Åpne**.

3.  Velg **Juridisk enhet** for prosjektet.

4.  Velg **Prosjektet**.

5.  Klikk **Sjekk ut** i kategorien **Microsoft Dynamics 365**.

6.  Når du er klar til å publisere til Finance, klikker du **Sjekk inn** i kategorien **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Erstatte den eksisterende arbeidsnedbrytningsstrukturen for et eksisterende prosjekt ved hjelp av Microsoft Project Client
Følg denne fremgangsmåten for å opprette en ny arbeidsnedbrytningsstruktur med Microsoft Project Client og erstatte en eksisterende arbeidsnedbrytningsstruktur for et eksisterende prosjekt:

1.  Åpne Microsoft Project Client.

2.  Opprett tidsplanen i Microsoft Project Client.

3.  I kategorien **Microsoft Dynamics 365** klikker du **Lagre endringer** > **Erstatt eksisterende prosjekt**.

4.  Velg **Juridisk enhet** for prosjektet.

5.  Velg **Prosjektet**.

6.  Klikk **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Opprette et nytt prosjekt fra Microsoft Project Client


1.  Åpne Microsoft Project Client.

2.  Opprett tidsplanen i Microsoft Project Client.

3.  I kategorien **Microsoft Dynamics 365** klikker du **Lagre endringer** > **Lagre til nytt prosjekt**.

4.  Velg **Juridisk enhet** for prosjektet.

5.  Angi **Prosjekt-ID** om nødvendig.

6.  Angi **Produktnavn**.

7.  Velg **Prosjekttype**, **Prosjektgruppe** og **Prosjektkontrakt-ID**. Du kan også opprette en ny prosjektkontrakt ved å klikke **Ny**.

8.  Velg **Kalenderen** som skal brukes for ressurser.

11. Klikk **OK**.

> [!NOTE]
> Tillegget for prosjektklienten støtter ikke følgende tegn i prosjekt-ID-formatet:
> 
>   - Understrek
>   - Periode
>   - Mellomrom
>   - Skråstrek

[!INCLUDE[footer-include](../includes/footer-banner.md)]
