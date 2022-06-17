---
title: Endringer av enhet, kontroll og brukergrensesnitt (Project Service Automation 3.x)
description: Denne artikkelen beskriver løsningsendringer for Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926880"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Endringer av enhet, kontroll og brukergrensesnitt (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Med utgivelsen av Microsoft Dynamics Project Service Automation (PSA) 3.x er det utført mange endringer i enhetene, kontrollene, visningene og brukergrensesnittet. I denne artikkelen finner du informasjon om disse viktige endringene.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Forholdet mellom overordnet-underordnet for enhetene salgsdokument, salgsdokumentlinje, salgsdokumentlinjedetalj
I versjoner av Dynamics 365 Project Service Automation (PSA) som er utgitt før versjon 3.0, ble noe av relasjonene mellom salgsdokumenter, salgsdokumentlinjer og salgsdokumentlinjedetaljer implementert ved hjelp av strengfelt som ville ha en streng representasjon av GUID for den relaterte enheten. Dette skyldes plattformbegrensninger som krevde betydelig egendefinert kode på server- og klientsidene av løsningen, slik at disse relasjonene fungerer på samme måte som vanlige Dynamics CRM-enhetsrelasjoner og får strengfelt til å fungere som oppslagsfelt.

PSA 3.0 er oppdatert til å dra nytte av de nye enhetsrelasjonene mellom salgsdokumenter og salgsdokumentlinjer.

Siden oppslags felt nå kan brukes til å angi referanser til enheter, er ikke lenger feltene som innehar strengverdien for GUID-en til den relaterte enheten i tidligere versjoner, lenger nødvendige, og de er derfor avskrevet. Den egendefinerte koden på klient- og serversiden som håndterer relasjoner som er definert av gamle strengfelt, er også avskrevet.

### <a name="entity-schema-changes"></a>Endringer i enhetsskjema
Følgende tabell viser de avskrevne strengfeltene ett etter ett og de nye oppslagsfeltene for enhetene. 

 Enhet |   Avskrevet felt (streng) | Nytt felt (oppslag)
--- | --- | ---
invoicedetail (fakturalinje) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (faktisk verdi) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (fakturaplan for prosjektkontraktlinje) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (milepæl for prosjektkontraktlinje) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (faktum) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (fakturalinjedetalj) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (journallinje) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (ressurskategori for prosjektkontraktlinje) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (detalj på prosjektkontraktlinje) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (transaksjonskategori for prosjektkontraktlinje) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (transaksjonsklassifisering for prosjektkontraktlinje) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (fakturaplan for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (ressurskategori for tilbudslinje) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (milepæl på tilbudslinje) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (tilbudslinjedetalj) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (transaksjonskategori for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (transaksjonsklassifisering for tilbudslinje) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (ordrelinje) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Avskrevne egendefinerte visninger og kontroller
Følgende egendefinerte visninger og kontroller, og de relaterte artefaktene, er avskrevet.

- Belastbarhets-visning.
- Egendefinerte rutenettkontroller for å vise tilbudslinjedetaljer på siden **Prosjektinformasjon** for tilbudslinjen.
- Egendefinerte rutenettkontroller for å vise prosjektkontraktsinjedetaljer på siden **Prosjektinformasjon** for salgsordrelinjen.

> [!NOTE]
> Hvis du vil ha en fullstendig liste over avskrevne ressurser, se [Avskrevne nettressurser i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Appmodul for enhetlig klientgrensesnitt
Ved innføringen av appmoduler for enhetlig klientgrensesnitt er PSA-områdekartoppføringenet fjernet fra systemet.  
Funksjonaliteten som er relatert til skjemabytting for salgsmulighet, tilbud, ordre og faktura, er avskrevet fordi den ikke lenger er nødvendig, fordi UCI-appmodulen bare inkluderer PSA-versjoner av skjemaene.  

Følgende nettressurser er avskrevet:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Hvis du vil ha en fullstendig liste over avskrevne ressurser, se [Avskrevne nettressurser i Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
