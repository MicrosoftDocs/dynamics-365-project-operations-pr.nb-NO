---
title: Spore status for et prosjekt
description: Slik sporer du status for et prosjekt i Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149600"
---
# <a name="track-a-projects-status-project-service"></a>Spore status for et prosjekt (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Bruk [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] til å spore fremdriften for prosjektet til en klient.  

Senere i engasjementet oppdateres prosjektfasene for å gjenspeile fasen i engasjementet:  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Ny**    | Når du oppretter et prosjekt, er fasen satt til **Ny**. Hvis du opprettet prosjektet fra en mal, kan prosjektet i denne fasen ha en tidsplan, estimater og teamdata. Ellers vil det være disposisjonen for prosjektet, og du må manuelt angi resten av prosjektkomponentene. |
|  **Tilbud**   |      Når du knytter et prosjekt til et tilbud eller oppretter det fra et tilbud, er prosjektfasen satt til **Tilbud**, og de estimerte start- og sluttdatoene oppdateres også. Når prosjektet er i tilbudsfasen, vises detaljene for tilbudet i kategorien **Salg** på **Prosjekt**-siden.      |
|   **Plan**   |                                     Når du har vunnet et tilbud som er tilknyttet et prosjekt, og når dette engasjementet går videre til kontraktfasen, oppdateres prosjektfasen til **Plan**. Kontraktdetaljene vises i kategorien **Salg** på **Prosjekt**-siden.                                      |
| **Fullfør** |                    Når prosjektarbeidet er fullført, kan du bytte fase til **Fullført**. Når prosjektfasen er satt til Fullført, er det forstått at arbeidet er 100 % fullført, men prosjektet holdes åpent for alle ventende tids- eller utgiftsposter som skal registreres.                     |
|  **Lukk**   |           Når alle transaksjoner er registrert i prosjektet og du ikke forventer at flere skal loggføres, kan du manuelt sette fasen til **Lukk**. Når prosjektet er satt til **Lukk**, kan du ikke loggføre flere transaksjoner i prosjektet, og prosjektet vil være skrivebeskyttet.           |

## <a name="to-track-a-projects-status"></a>Slik sporer du status for et prosjekt  

1.  Gå til **Project Service > Prosjekter**.  

2.  Klikk prosjektet du vil arbeide på.  

3.  Velg pil ned ved siden av prosjektnavnet i feltet øverst på skjermen, og klikk deretter **Prosjektsporing**.  

4.  Velg **Innsatssporing** eller **Kostnadssporing** i rullegardinlisten over oppgavelisten.  

5.  Dobbeltklikk en hvilken som helst oppgave for å redigere den. Du kan også flytte eller endre størrelse på stolpene i Gantt-diagrammet for å endre klokkeslett og fremdriften for en oppgave.  

### <a name="see-also"></a>Se også  
 [Prosjektlederhåndbok](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]