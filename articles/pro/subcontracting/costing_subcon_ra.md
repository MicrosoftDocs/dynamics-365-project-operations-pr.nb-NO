---
title: Kostnadsberegning av tilordninger for underleveranseressurs
description: Dette emnet forklarer hvordan Microsoft Dynamics 365 Project Operations beregner kostnadsberegning av tilordninger for underleveranseressurs.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 5a94840a3735639532683153105fea85bea99c9d
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902905"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Kostnadsberegning av tilordninger for underleveranseressurs

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

Oppgavetilordninger for prosjektteammedlemmer for underkontrakt kalkuleres ved hjelp av prislisten **Kjøp** som er knyttet til underkontrakten for den relaterte teammedlemsoppføringen. Dette er forskjellig fra hvordan ressurstilordninger for ansatte kostnadsberegnes der oppgavetilordninger for ansattressurser er kostnadsberegnet ved hjelp av **Kostnad**-prislisten som er knyttet til kontraktsenheten for prosjektet. 

For generiske prosjektteammedlemmer på underkontrakt kalkuleres tilordningene ved hjelp av et rollebasert prisoppsett i innkjøpsprislisten som er knyttet til underkontrakten. Innkjøpspriser kan også angis spesifikt for hver ressurs. Disse ressursspesifikke prisene prioriteres når kostnadsoppgavetilordninger for navngitte prosjektteammedlemmer er kontraktarbeidere. 

Prioriteten ved å bruke rollespesifikk innkjøpspris kontra ressursspesifikk drives av konfigureringen av prissettingsdimensjonsprioriteten i **Parametere > Beløpsbaserte prisdimensjoner**.

Denne funksjonaliteten for dynamisk utledede priser basert på dimensjonsoppsett for innkjøpspriser for underleverandører er den samme som hvordan kostnader og fakturasatser utledes for heltidsansatte. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Opprette oppgavetilordninger for å få kostnadsestimater for underleverandørressurser

Oppgavetilordninger for underleverandører kan opprettes på to måter: 
- Bruke kategorien **Oppgaver**.
- Bruk kategorien **Team**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Opprette ressurstilordninger ved hjelp av kategorien Oppgaver
Ved hjelp av **Ressurser**-listen i kategorien **Oppgaver** for en bestemt oppgave kan du opprette en oppgavetilordning for en navngitt ressurs eller en generell ressurs. Hvis du velger en navngitt ressurs fra rullegardinlisten **Tilordnede ressurser** på oppgaven, og denne ressursen er en kontraktarbeider, tilordnes den navngitte ressursen til oppgaven, og en tilsvarende oppføring for prosjektteammedlem opprettes med arbeidstypen satt til **Kontraktarbeider** og **Gyldighet** satt til **Ugyldig**. Som et neste trinn må du åpne medlemsoppføringen for prosjektteamet og velge en underkontrakt og underkontraktlinje. Dette oppdaterer oppgavetilordningen slik at den har en referanse til underkontrakt og underkontraktlinjen, og status for teammedlemmet oppdateres også til **Gyldig**.

Hvis du velger å opprette et generisk teammedlem fra rullegardinlisten **Tilordnede ressurser** på oppgaven, tillater dialogboksen for **oppretting av generisk teammedlem** at du kan velge en underkontrakt og underkontraktlinje. Når den generelle ressursen er tilordnet til oppgaven, og den tilsvarende oppføringen for prosjektteammedlemmet opprettes, legger du merke til at oppføringen for prosjektteammedlem opprettes med arbeidstype satt til **Kontraktarbeider** og **Gyldighet** satt til **Gyldig**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Opprette prosjektteammedlemmer ved hjelp av kategorien Team
Ved hjelp av kategorien Team i prosjektet kan du opprette et generisk teammedlem eller et navngitt teammedlem. Når du oppretter teammedlemmet, kan du velge underkontrakten og underkontraktlinjen. Når teammedlemmet er opprettet, må du tilordne teammedlemmet til en oppgave ved å bruke rullegardinlisten **Tilordnede ressurser** på oppgaven. 

## <a name="updating-estimates"></a>Oppdatere estimater
Når du har tilordnet prosjektteammedlemmer til oppgaver, må du gå til kategorien **Estimater** i prosjektet og velge **Oppdater priser** for å sikre at kostnadssatsene for ressurstilordninger for underleverandør oppdateres basert på innkjøpsprislisten som er knyttet til underkontrakten. Merk at estimater ikke genereres for ikke-tilordnede oppgaver i Microsoft Dynamics 365 Project Operations. Dette fører til at du må opprette oppgavetilordninger til pris- og kostnadsvariable oppgaver på prosjektet. 

> [OBS!] Prosjektteammedlemmer som har **Arbeidertype** som **Kontraktarbeider**, men som ikke har en underkontraktsreferanse, blir flagget som **Ugyldig** i rutenettet for **Prosjektteammedlemmer**. Hvis det finnes prosjektteammedlemmer med denne statusen, åpner du oppføringen for prosjektteamet og oppdaterer feltene for underkontrakt og underkontraktlinje manuelt, slik at estimatet for økonomisk kostnad gjenspeiler underleverandørkostnaden nøyaktig i kategorien **Estimater**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
