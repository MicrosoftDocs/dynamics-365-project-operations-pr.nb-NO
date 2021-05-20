---
title: Integrering av leverandørfaktura
description: Dette emnet inneholder informasjon om integrering av leverandørfaktura i Project Operations.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07839436c3777b0554e0721d250bff643e38c088
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955806"
---
# <a name="vendor-invoice-integration"></a>Integrering av leverandørfaktura

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Prosjektrelaterte innkjøp i Dynamics 365 Project Operations kan registreres ved å gå til **Leverandørgjeld** > **Fakturaer** > **Ventende leverandørfakturaer** og bruke et ventende leverandørfakturadokument. Hvis du vil ha mer informasjon, kan du se [Kjøpe ikke-lagerførte materialer ved hjelp av en ventende leverandørfaktura](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Før du bruker funksjonaliteten som er beskrevet i dette emnet, må du se gjennom og bruke de nødvendige konfigurasjonene. Hvis du vil ha mer informasjon, kan du se [Aktivere ikke-lagerførte materialer og ventende leverandørfakturaer](../procurement/configure-materials-nonstocked.md).

I Project Operations posteres prosjektrelaterte leverandørfakturaer ved hjelp av spesielle posteringsregler:

- Prosjektrelaterte kostnader (inkludert ikke-reserverbar avgift) posteres ikke umiddelbart til prosjektkostnadskontoen i økonomimodulen. I stedet posteres kostnaden til **integrasjonskontoen for innkjøp**. Denne kontoen konfigureres i **Prosjektstyring og regnskap** > **Oppsett** > **Prosjektstyring og regnskapsparametere** i kategorien **Project Operations i Dynamics 365 Customer Engagement**.
- Dobbel skriving synkroniserer leverandørfakturadetaljer til Microsoft Dataverse ved hjelp av følgende tabelltilordninger:

     - **Project Operations-integrering, prosjektleverandør fakturaeksportenhet (msdyn_projectvendorinvoices)**: Denne tabelltilordningen synkroniserer informasjon om leverandørfakturahode. Bare leverandørfakturaer med minst én linje som inneholder en prosjekt-ID, synkroniseres til Dataverse.
     - **Project Operations-integrering, prosjektleverandør fakturalinjeeksportenhet (msdyn_projectvendorinvoicelines)**: Denne tabelltilordningen synkroniserer informasjon om leverandørfakturalinje. Bare linjer som inneholder en prosjekt-ID, synkroniseres med Dataverse.

     > [!NOTE]
     > Leverandørfakturadetaljer i Dataverse kan ikke redigeres.

Underordnede avgifter, underleverandører og andre finansielle innlegg registreres etter behov i Dynamics 365 Finance når leverandørfakturaen posteres.

![Integrering av leverandørfaktura](media/DW7VendorInvoice.png)

Når oppføringer skrives til en **leverandørfaktura**-enhet i Dataverse, starter en automatisert godkjenningsprosess for oppføringene. Hvis det er nødvendig, kan den automatiserte godkjenningsprosessstatusen gjennomgås i Dataverse ved å gå til **Avanserte innstillinger** > **System** > **Systemjobber**. Når godkjenningen er fullført, opprettes oppføringer for materialtransaksjonsklasse i **Faktiske verdier**-enheten.

Materialrelaterte faktiske verdier behandles deretter ved hjelp av tabelltilordningen med dobbeltskriving, **Faktiske verdier for Project Operations-integrering (msdyn_actuals)**. Hvis du vil ha mer informasjon, se [Prosjektestimater og faktiske verdier](resource-dual-write-estimates-actuals.md).

Den periodiske prosessen **Importer fra oppsamlingstabell** oppretter leverandørfakturarelaterte journallinjer for integrering av Project Operations. Forskyvningskontoen er som standard innkjøpskontoen for integrering. Når integreringskladden posteres, fjernes kontosaldoen for leverandørfakturatransaksjonen, og linjebeløpet flyttes til prosjektkostnadskontoen. Systemet oppretter også transaksjoner for underordnet prosjekt for nedstrømsfaking og inntektsføring.
