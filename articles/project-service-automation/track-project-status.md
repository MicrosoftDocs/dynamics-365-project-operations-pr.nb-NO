---
title: Spore status for et prosjekt
description: Slik sporer du status for et prosjekt i Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7610aecb-318c-422b-b626-9106b0736b5f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: e4d53b6235c3b941bce525dca09ee3d647c3d242
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/24/2020
ms.locfileid: "3754187"
---
# <a name="track-a-projects-status-project-service"></a>Spore status for et prosjekt (Project Service)

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
 [Prosjektlederhåndbok](../project-service/project-manager-guide.md)
