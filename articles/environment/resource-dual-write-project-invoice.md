---
title: Integrering av prosjektfaktura
description: Denne artikkelen inneholder informasjon om integrering av dobbel skriving i Project Operations for kundefakturering.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912114"
---
# <a name="project-invoice-integration"></a>Integrering av prosjektfaktura

Denne artikkelen inneholder informasjon om integrering av dobbel skriving i Project Operations for kundefakturering.

I Project Operations administrerer prosjektlederen prosjektfaktureringsrestansen og oppretter en proformafaktura for kunden i Microsoft Dataverse. Basert på denne proformafakturaen oppretter medarbeideren for utestående fordringer eller prosjektregnskapsføreren en kunderettet faktura. Integrering av to dobbel skriving sikrer at proformafakturadetaljene synkroniseres med økonomi- og driftsapper. Når den kunderettede fakturaen er postert, oppdaterer systemet de relevante faktiske prosjektdataene i Dataverse med regnskapsdetaljene. Grafikken nedenfor gir en konseptuell oversikt på høyt nivå over denne integreringen.

   ![Integrering av prosjektfaktura.](./media/DW5Invoicing.png)

Når prosjektlederen har kontrollert proformafakturaen i Dataverse, synkroniseres informasjonen i proformafakturahodet med økonomi- driftsapper ved hjelp av tabelltilordningen med dobbel skriving, **Prosjektfakturaforslag V2 (fakturaer)**. Dette er en enveisintegrering fra Dataverse til økonomi- og driftsapper. Oppretting eller sletting av prosjektfakturaforslag direkte i økonomi- og driftsapper støttes ikke.

Fakturabekreftelse i Dataverse utløser også forretningslogikken for å opprette faktureringsrelaterte oppføringer i **Faktiske verdier**-enheten. Disse oppføringer synkroniseres til Finance and Operations ved å bruke tabelltilordningen med dobbel skriving, **Faktiske verdier for Project Operations-integrering (msdyn\_actuals).** Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md). 

Prosjektfakturaforslagslinjer opprettes av den periodiske prosessen **Importer skjemaoppsamling**. Denne prosessen er basert på detaljer om faktiske data for fakturert salg i tabellen **Oppsamling av faktiske verdier**. Hvis du vil ha mer informasjon, kan du se [Behandle prosjektfakturaforslag](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
