---
title: Hva er nytt i Project Service Automation Update Release 13, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754115"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, Update Release 13
Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og reparasjonene som er nye eller endrede for Project Service Automation V3, Update Release 13. Denne versjonen har buildnummer V3.10.3.18 og er tilgjengelig i henhold til følgende tidsplan:

- **Generell tilgjengelighet (egen oppdatering):** november 2019
- **Automatisk oppdatering:** desember 2019


## <a name="update-release-13"></a>Update Release 13 

### <a name="bug-fixes"></a>Feilrettinger

- Tid og utgift

     - Fikset: Søkefunksjonaliteten på siden **Utgiftsgodkjenning** fungerer ikke når det søkes etter utgiftsformål.

- Ressursbehandling

     - Fikset: Tallene i avstemmingen er oppdatert til å være høyrejustert.
     - Fikset: Navngitte ressurser kan ikke tilordnes oppgaver via kategorien **Tidsplan**.

- Prosjektledelse

     - Fikset: Nullreferanseunntak ved tilordning av teammedlemmer når **TransactionType** mangler oppsettinformasjon for **Enhet** og **DefaultGroup**.

- Sales

     - Fikset: Duplikate transaksjonstypeoppføringer returnerer en feil når rolleprisoppføringer opprettes.
     - Fikset: Ekstraknapper for **Ny salgsmulighet** **Tilbud**, **Ordrelinje** og **Legg til produkt** er synlige i kommandoer for salgsmuligheter, tilbud, ordreprodukter og i delrutenettet for de prosjektbaserte linjene.


