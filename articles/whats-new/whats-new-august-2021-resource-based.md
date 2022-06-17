---
title: Nyheter august 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer
description: Denne artikkelen inneholder informasjon om kvalitetsoppdateringene som er tilgjengelige i utgivelsen av Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer fra august 2021.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912298"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nyheter august 2021 – Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer

*Gjelder: Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer*

Denne artikkelen gjelder følgende komponenter og versjoner av Dynamics 365 Project Operations:

   - Project Operations i Microsoft Dataverse-miljø, versjon 4.13.0.152.
   - Prosjektledelse og regnskap i et Dynamics 365 Finance-miljø versjon 10.0.20.

## <a name="features-included-in-this-release"></a>Funksjoner som er inkludert i denne versjonen

Følgende funksjoner er inkludert i denne versjonen:

- **Godkjenningssett**: Godkjenningssett grupperer godkjenningsforespørsler for tid, utgifter eller materialbruk sammen til mindre delsett av operasjoner. Denne grupperingen tillater at godkjenninger kan behandles i en bestemt rekkefølge etter prosjekt, og gjør det mulig å prøve på nytt og å sekvensere. Gruppering av forespørslene forbedrer påliteligheten og sporbarheten ved godkjenningsbehandling for store godkjenningsvolumer. Hvis du vil ha mer informasjon, kan du se [Godkjenningssett](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Oppdateringer av tilordninger for dobbel skriving for Project Operations

Det finnes ingen oppdateringer for tilordninger av dobbel skriving i Project Operations i denne versjonen.

Hvis du vil ha en gjeldende liste og versjoner av tilordninger for dobbel skriving i Project Operations, kan du se [Tilordningsversjoner av dobbel skriving for Project Operations](../environment/resource-dual-write-maps.md).

Kjør alltid den nyeste versjonen av kartet i miljøet, og aktiver alle relaterte tabellkart når du oppdaterer Project Operations Dataverse-løsningen og Finance-løsningsversjonen. Enkelte funksjoner fungerer kanskje ikke på riktig måte hvis den nyeste versjonen av tilordningen ikke er aktivert. Du kan se den aktive versjonen av tilordningen på siden **Dobbel skriving** i kolonnen **Versjon**. Aktiver en ny versjon av tilordningen ved å velge **Versjoner av tabelltilordningen**, velge den nyeste versjonen og deretter lagre den valgte versjonen. Hvis du har tilpasset en medfølgende tabelltilordning, må du bruke endringene på nytt. Hvis du vil ha mer informasjon, se [Administrasjon av programlivssyklus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Hvis det oppstår et problem med å starte kartet, følger du instruksjonene i delen [Problem med manglende tabellkolonner på kart](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) i feilsøkingsveiledningen for dobbel skriving.

## <a name="quality-updates"></a>Kvalitetsoppdateringer

### <a name="project-operations-on-dataverse"></a>Project Operations på Dataverse

| **Funksjonsområdet** | **Referansenummer** | **Kvalitetsoppdatering** |
| --- | --- | --- |
| Fakturering og prising | 2295625 | Milepælnavnet må kopieres fra fakturaplanen til fakturalinjedetaljene. |
| Fakturering og prising | 2316323 | Rabatten bør ikke kunne redigeres på en proformafaktura i Project Operations for ressursbaserte scenarioer. |
|   Administrasjon av salgsmuligheter | 2338619 | Forretningsregler for **salgsmuligheter** og **tilbud** må bare startes på sider. |
| Ressursstyring | 2316523 | Hvis du bruker **Send forespørsel** fra et ressurskrav som har en vedlagt rolle, vises det ikke en feil. |
| Ressursstyring | 2326885 | Det skal ikke vises en feil når du oppretter et ressurskrav via et prosjekt. |
| Tid og utgifter | 2335584 | Avskrevne oppgaveflyter i tidsoppføringen. |
| Tid og utgifter | 2336884 | Tidsregistreringsknappen **Kopier uke** må fungere for mer enn bare gjeldende bruker. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Prosjektstyring og regnskap i Dynamics 365 Finance

| Funksjonsområdet | Referansenummer | Kvalitetsoppdatering |
| --- | --- | --- |
| Reise og utgift | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Feil beløp for leverandørtransaksjon og salgsavgiftstransaksjon posteres når en utgift opprettes fra en kredittkorttransaksjon. |
| Reise og utgift | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Feil avregning er linjer som opprettes når betalingskladden genereres. |
| Reise og utgift | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Feil beløp for salgsavgiftstransaksjon posteres når en utgift opprettes fra en kredittkorttransaksjon. |
| Reise og utgift | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Det kan ta lang tid å slette en utgiftslinje. |
| Prosjektregnskap | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Systemet støtter ikke konfigurasjon av fortløpende nummersekvensering når du legger inn et estimat etter bruk av KB 4619395. |
| Prosjektregnskap | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Det kan hende at publisering av leverandørfaktura mislykkes med feilmeldingen «Transaksjonene på bilaget balanseres ikke i henhold til 17.05.2021. (regnskapsvaluta: 0,00 – rapporteringsvaluta: 0,01)» |
