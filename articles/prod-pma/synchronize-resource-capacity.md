---
title: Synkronisere ressurskapasitet
description: Dette emnet gir informasjon om hvordan du synkroniserer kapasiteten til en ressurs på tvers av kalendere og prosjekter.
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
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288579"
---
# <a name="synchronize-resource-capacity"></a>Synkronisere ressurskapasitet

[!include [banner](../includes/banner.md)]

Prosessene for hjelp for ressurssynkronisering garanterer at informasjon for kalenderen og basiskalenderen når frem til planleggingen av prosjektressurser. Hvis kalenderen endres, gjør prosessene de nødvendige oppdateringene for planleggingen av prosjektressurser. Prosessene bidrar også til å forbedre ytelsen fordi kalenderens ressursinformasjon er synkronisert på forhånd. Derfor skjer oppdatering av ressursplanleggingsinformasjonen raskere. Vi anbefaler at du planlegger prosessene som en bunke i stedet for én om gangen. Ellers er det en risiko for at noen vil glemme inklusivdatoene da informasjonen sist ble synkronisert. Hvis du ikke bruker noen datoer, kan det oppstå mellomrom under synkronisering av dato.

![Kalendersynkronisering](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synkroniser opprullering av ressurskapasitet

Synkroniseringsprosessen er utformet for å synkronisere all ressurskalenderinformasjon. Denne informasjonen inkluderer informasjon om basiskalenderen for eventuelle endringer i prosjektets tabellkapasitet for ressurskalender. Hvis det legges til nye ressurser i prosjektet, bidrar synkroniseringen til å garantere at den oppdaterte kalenderinformasjonen er tilgjengelig. Denne synkroniseringen kan gjøres når som helst.

Vi anbefaler at du bruker en bunke. Alternativene er tilgjengelige under synkronisering av kapasitetsreservasjoner.

1. Velg **Prosjektstyring og regnskap** &gt; **Periodisk** &gt; **Kapasitetssynkronisering** &gt; **Synkroniser opprullering av ressurskapasitet**.
2. Angi alternativene i tabellen nedenfor.

    | Alternativ      | Beskrivelse |
    |-------------|-------------|
    | Periodekode | Du kan også velge datointervallkoden for økonomimodulen for å angi start- og sluttdatoene for synkroniseringsprosessen for opprullering av ressurskapasitet. |
    | Startdato  | Angi startdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet. |
    | Sluttdato    | Angi sluttdatoen for synkroniseringsprosessen for opprullering av ressurskapasitet. |

[![Synkroniseringsfremdrift](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]