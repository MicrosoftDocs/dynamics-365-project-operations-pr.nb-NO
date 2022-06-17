---
title: Hva er nytt eller endret i Project Service Automation Update Release 13, V3
description: Denne artikkelen inneholder informasjon om hva som er nytt i Project Service Automation Update Release 13 V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930698"
---
# <a name="project-service-automation-update-release-13-v3"></a>Project Service Automation, Update Release 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glade for å annonsere den nyeste oppdateringen av Dynamics 365 Project Service Automation (PSA)-programmet. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](/power-platform/admin/install-remove-preferred-solution).

Denne artikkelen viser funksjoner og rettelser som er nye eller endret i Project Service Automation V3, Update Release 13. Denne versjonen har buildnummer V3.10.3.18 og er tilgjengelig i henhold til følgende tidsplan:

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
     - Fikset: Ekstra knapper for **Ny salgsmulighet**, **Tilbud**, **Ordrelinjer** og **Legg til produkt** vises i kommandoer for salgsmuligheter, tilbud, ordreprodukter og prosjektbaserte linjedelrutenettet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
