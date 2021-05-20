---
title: Integrering av prosjektfaktura
description: Dette emnet gir informasjon om integrasjon av dobbel skriving for Project Operations for kundefakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955803"
---
# <a name="project-invoice-integration"></a>Integrering av prosjektfaktura

Dette emnet gir informasjon om integrasjon av dobbel skriving for Project Operations for kundefakturering.

I Project Operations administrerer prosjektlederen prosjektfaktureringsrestansen og oppretter en proformafaktura for kunden i Microsoft Dataverse. Basert på denne proformafakturaen oppretter medarbeideren for utestående fordringer eller prosjektregnskapsføreren en kunderettet faktura. Integrering med dobbel skriving sikrer at proformafakturadetaljene synkroniseres med Finance and Operations-apper. Når den kunderettede fakturaen er postert, oppdaterer systemet de relevante faktiske prosjektdataene i Dataverse med regnskapsdetaljene. Grafikken nedenfor gir en konseptuell oversikt på høyt nivå over denne integreringen.

   ![Integrering av prosjektfaktura](./media/DW5Invoicing.png)

Når prosjektlederen har bekreftet proformafakturaen i Dataverse, synkroniseres informasjonen om proformafakturahodet til Finance and Operations-apper ved hjelp av tabelltilordningen for dobbel skriving, **Prosjektfakturaforslag V2 (fakturaer)**. Dette er en enveisintegrasjon fra Dataverse til Finance and Operations-apper. Oppretting eller sletting av prosjektfakturaforslag direkte i Finance and Operations-apper støttes ikke.

Fakturabekreftelse i Dataverse utløser også forretningslogikken for å opprette faktureringsrelaterte oppføringer i **Faktiske verdier**-enheten. Disse oppføringene synkroniseres til Finance and Operations-apper ved hjelp av tabelltilordningen for dobbeltskriving **Faktiske verdier for Project Operations-integrering (msdyn\_actuals).** Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md). 

Prosjektfakturaforslagslinjer opprettes av den periodiske prosessen **Importer skjemaoppsamling**. Denne prosessen er basert på detaljer om faktiske data for fakturert salg i tabellen **Oppsamling av faktiske verdier**. Hvis du vil ha mer informasjon, kan du se [Behandle prosjektfakturaforslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
