---
title: Hva er nytt eller endret i Project Service Automation Update Release 13, V3
description: Dette emnet inneholder informasjon om hva som er nytt i Project Service Automation Update Release 13, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081580"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, Update Release 13, V3
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
     - Fikset: Ekstraknapper for **Ny salgsmulighet** **Tilbud** , **Ordrelinje** og **Legg til produkt** er synlige i kommandoer for salgsmuligheter, tilbud, ordreprodukter og i delrutenettet for de prosjektbaserte linjene.


