---
title: Integrering av prosjektfaktura
description: Denne artikkelen inneholder informasjon om integrering av dobbel skriving i Project Operations for kundefakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029036"
---
# <a name="project-invoice-integration"></a>Integrering av prosjektfaktura

Denne artikkelen inneholder informasjon om integrering av dobbel skriving i Project Operations for kundefakturering.

I Project Operations administrerer prosjektlederen prosjektfaktureringsrestansen og oppretter en proformafaktura for kunden i Microsoft Dataverse. Basert på denne proformafakturaen oppretter medarbeideren for utestående fordringer eller prosjektregnskapsføreren en kunderettet faktura. Integrering av to dobbel skriving sikrer at proformafakturadetaljene synkroniseres med økonomi- og driftsapper. Når den kunderettede fakturaen er postert, oppdaterer systemet de relevante faktiske prosjektdataene i Dataverse med regnskapsdetaljene. Grafikken nedenfor gir en konseptuell oversikt på høyt nivå over denne integreringen.

   ![Integrering av prosjektfaktura.](./media/DW5Invoicing.png)

Når prosjektlederen har kontrollert proformafakturaen i Dataverse, synkroniseres informasjonen i proformafakturahodet med økonomi- driftsapper ved hjelp av tabelltilordningen med dobbel skriving, **Prosjektfakturaforslag V2 (fakturaer)**. Dette er en enveisintegrering fra Dataverse til økonomi- og driftsapper. Oppretting eller sletting av prosjektfakturaforslag direkte i økonomi- og driftsapper støttes ikke.

Fakturabekreftelse i Dataverse utløser også forretningslogikken for å opprette faktureringsrelaterte oppføringer i **Faktiske verdier**-enheten. Disse oppføringer synkroniseres til økonomi og drift ved å bruke tabelltilordningen med dobbel skriving, **Faktiske verdier for Project Operations-integrering (msdyn\_actuals).** Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md). 

Prosjektfakturaforslagslinjer opprettes av den periodiske prosessen **Importer skjemaoppsamling**. Denne prosessen er basert på detaljer om faktiske data for fakturert salg i tabellen **Oppsamling av faktiske verdier**. Hvis du vil ha mer informasjon, kan du se [Behandle prosjektfakturaforslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
