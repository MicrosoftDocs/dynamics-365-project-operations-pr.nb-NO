---
title: Enheter og enhetsgrupper
description: Dette emnet gir informasjon om hvordan du oppretter enheter og enhetsgrupper i Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081743"
---
# <a name="units-and-unit-groups"></a>Enheter og enhetsgrupper

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Enhetene er antallet eller målene som du kan selge produktene eller tjenestene i. Hvis du for eksempel selger hageutstyr, kan du selge frø i pakker, bokser og paller. En enhetsgruppe er en samling av disse ulike enhetene.

Hvis du vil fullføre trinnene i dette emnet, må du sørge for at du er tilordnet rollen Systemadministrator- eller Sales Professional-leder eller tilsvarende tillatelser.

## <a name="create-a-unit-group"></a>Opprette en enhetsgruppe

1. Velg **Enheter** i områdekartet.
2. Velg **Ny** , og skriv inn enhetsnavnet i dialogboksen **Opprett enhetsgruppe**.
3. Skriv inn laveste felles målenheten som produktet skal selges i, i feltet **Primærenhet**. Du kan for eksempel skrive inn "stykk" eller "ounce".
4. Velg **OK**.

## <a name="add-units-to-a-unit-group"></a>Legge til enheter i en enhetsgruppe

1. Åpne en enhetsgruppe, og velg **Enheter** i kategorien **Relatert**. Du ser at primærenheten allerede er lagt til.
2. Velg **Legg til ny enhet**. På siden **Hurtigoppretting: Enhet** i **Navn** -feltet angir du navnet på enheten.
3. I **Antall** -feltet angir du antallet som enheten skal inneholde. Hvis en boks inneholder for eksempel 2 deler, ville du skrevet "2". 
4. I **Basisenhet** -feltet velger du en basisenhet for å fastsette den laveste målenheten for enheten. Du kan for eksempel velge "Stykk".
5. Velg **Lagre** :