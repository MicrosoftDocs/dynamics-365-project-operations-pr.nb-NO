---
title: Planleggingsytelse for prosjektressurs
description: Dette emnet gir informasjon om hvordan du forbedrer ytelsen til ressursplanlegging for et stort antall prosjekter.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007293"
---
# <a name="project-resource-scheduling-performance"></a>Planleggingsytelse for prosjektressurs

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Det kan oppstå ytelsesproblemer knyttet til ressursplanlegging når antallet prosjekter er flere tusener. En funksjon som brukes til å forbedre ressursplanleggingsytelsen, er tilgjengelig, og den gjør det mulig for brukere å redusere tiden det tar å starte ressurstilgjengelighetsskjemaet. Dette fjerner spesielt synkroniseringsprosessen for ressurskapasitet, og bruker **ResProjectResource**-tabellen til å øke hastigheten på ressursoppslagene. Vær oppmerksom på at **ResRollup**-tabellen ikke lenger skal brukes.

> [!IMPORTANT]
> Hvis det er en avhengighet av synkroniseringsprosessen for akkumulert ressurskapasitet eller **ResProjectResource**-tabellen, må du ikke bruke denne funksjonen.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktivere ytelsesforbedring for ressursplanlegging
Følg fremgangsmåten nedenfor for å aktivere ytelsesforbedring for ressursplanlegging.

1. Gå til **Funksjonsbehandling** > **Alle**, og finn **Aktiver funksjonen for ytelsesforbedring for ressursplanlegging** i funksjonslisten .
2. Velg **Aktiver nå**.

> [!NOTE]
> Hvis du ikke finner funksjonen i listen, velger du **Se etter oppdateringer** for å oppdatere listen.

3. Oppdater nettleseren, og gå deretter til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Synkroniser ressurskalenderkapasitet på tvers av alle firmaer**.
4. Sett **Fjern eksisterende kapasitetsoppføringer** til **Ja** for å fjerne tidligere data. Hvis du vil generere trinnvise data, setter du det til **Nei**.
5. I **Periodekode**-feltet velger du perioden som data skal genereres i. Hvis du velger en periodekode, trenger du ikke definere en start- og sluttdato.
6. Hvis du lar **Periodekode**-feltet være tomt, velger du bestemte start- og sluttdatoer for å generere data.
7. Velg **OK**.

 > [!NOTE]
 > Dette distribuerer generelle data til **ResCalendarCapacity**-tabellen i alle selskaper i miljøet, slik at den satsvise jobben bare må kjøres i én juridisk enhet. Dataene i denne satsvise jobben er nødvendige for å beregne ressurskapasitet gjennom den tilknyttede kalenderen.

8. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Prosjektressurser** > **Fyll ut prosjektressurser på tvers av alle firmaer**, og velg deretter **OK**. Dette er dataoppgraderingsskriptet for generelle data i tabellene **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**. Verdier for feltet **PSAPRojSchedRole.RootActivity** oppdateres også. Hvis dette ikke kjøres, får du en advarsel når du prøver å kjøre ressursplanleggingsoperasjoner.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Deaktivere ytelsesforbedring for ressursplanlegging

1. Gå til **Funksjonsbehandling** > **Alle**, og søk etter **Aktiver funksjonen for ytelsesforbedring for ressursplanlegging**.
2. Velg funksjonen, og klikk deretter **Deaktiver**-knappen.
3. Oppdater nettleseren din.
4. Gå til **Prosjektstyring og regnskap** > **Periodisk** > **Kapasitetssynkronisering** > **Synkronisering opprulling av ressurskapasitet**.
5. På siden **Synkronisering opprulling av kapasitet** setter du **Fjern eksisterende kapasitetsoppføringer** til **Ja** for å fjerne tidligere data. Hvis du vil generere trinnvise data, setter du det til **Nei**.
6. I **Periodekode**-feltet velger du perioden som data skal genereres i. Hvis du velger en periodekode, trenger du ikke definere en start- og sluttdato.
7. Hvis du lar **Periodekode**-feltet være tomt, velger du bestemte start- og sluttdatoer for å generere data.
8. Velg **OK**.

> [!NOTE]
> Dette distribuerer generelle data til **ResRollup**-tabellen i alle selskaper i miljøet, slik at den satsvise jobben bare må kjøres i én juridisk enhet. Denne satsvise jobben er nødvendig for alle **Ressurstilgjengelighet**-visninger. Hvis denne satsvise jobben ikke kjøres, genereres **ResRollup**-dataene direkte, noe som kan ta tid.


[!INCLUDE[footer-include](../includes/footer-banner.md)]