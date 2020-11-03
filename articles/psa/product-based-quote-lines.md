---
title: Produktbaserte tilbudslinjer
description: Dette emnet inneholder informasjon om produktbasere tilbudslinjer.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081800"
---
# <a name="product-based-quote-lines"></a>Produktbaserte tilbudslinjer

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Du kan opprette produktbaserte tilbudslinjer i Dynamics 365 Project Service Automation. Produktbaserte tilbudslinjer kan være "innskrevne" linjer, eller de kan være elementer fra produktkatalogen.

## <a name="product-catalog"></a>Produktkatalog

Produktene i en Dynamics 365-produktkatalog har en standardenhet og enhetsgruppe. Hvis flere produkter deler samme attributtsett, kan du opprette en produktserie som også har disse attributtene. Alle produktene i en produktserie arver samme attributtsett.

Et selskap selger for eksempel abonnementslisenser for en rekke typer programvare. All abonnementsprogramvare har følgende to attributter:

- Antall brukere 
- Abonnementsvarighet (i måneder)

En god måte å opprettholde denne typen katalog på, er å opprette en produktserie kalt **Abonnementsprogramvare** , og som har **Antall brukere** og **Abonnementsvarighet** som attributter. Du kan deretter legge til enkeltprodukter, for eksempel **Dynamics 365 Sales** eller **Dynamics 365 Field Service** i produktserien **Abonnementsprogramvare**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Legge til produktkatalogvarer i et prosjekttilbud

Sider med prosjekttilbud og prosjektkontrakter har deler for to linjetyper: prosjektbaserte linjer og produktbaserte linjer. For produktbaserte linjer brukes Dynamics 365 til å legge til varer fra en produktkatalog i et tilbud. Rullegardinlisten på tilbudslinjen eller prosjektkontraktlinjen inkluderer alle produkter og enheter i produktprislisten som er knyttet til tilbudet eller prosjektkontrakten. Du kan også legge til produkter som ikke er del av tilbudets produktprisliste.

Du kan også velge produkter fra andre prislister, eller du kan velge produkter direkte fra produktkatalogen. Når du velger produkter direkte fra en produktkatalog, brukes standardprislisten for dette produktet til å hente produktets salgspris. Hvis det ikke er angitt en standardprisliste, settes prisen til 0 (null).

Hvis en tilbudslinje er basert på en produktkatalog, kan du overstyre salgsprisen direkte i tilbudslinjen. Vær oppmerksom på at en tilbudslinje i Dynamics 365 har et **Prising** -felt. To verdier er tilgjengelige:

- Overstyr pris  
- Bruk standard

Hvis du angir dette feltet til **Overstyr pris** , angir ikke Dynamics 365 en standardpris. Du må angi en pris for produktet på tilbudslinjen. Hvis du angir dette feltet til **Bruk standard** , bruker Dynamics 365 standard salgspris og låser feltet for å forhindre redigering.

Når du har installert PSA, angis det standard salgspriser på de produktbasert linjene i et tilbud. **Pris** -feltet angis deretter til **Overstyr pris** , slik at du kan redigere standardprisen på tilbudslinjene.

> ![Angi Overstyr pris](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Antallsfaktorer for produkter

PSA bruker antallsfaktorer til å støtte salg av abonnementsbasert produkter. Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på tilbuds- eller prosjektkontraktlinjen som antall brukermåneder.

Vanligvis lagres prisen på abonnementsprogramvaren i katalogen som prisen per bruker per måned. Du kan imidlertid bruke andre tidsbeskrivelser i stedet. I løpet av salgsprosessen er prisen på tilbudslinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av IT-salgsrepresentanten. Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder. Antallet som brukes til å beregne beløpet for tilbudslinjen, er et produkt av antall brukere og antall abonnementsmåneder.

PSA har innført konseptet antallsfaktorer for å støtte denne typen salg. Antallsfaktorer er avhengig av produktattributter i Dynamics 365. Når du konfigurerer bestemte egenskaper for et produkt, kan du bruke PSA til å flagge et delsett av disse egenskapene, eller alle egenskapene, som antall faktorer.

PSA validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer. Når et produkt som antallsfaktorer er konfigurert for, blir lagt til på en tilbudslinje, blir **Antall** -feltet på tilbuds linjen et skrivebeskyttet felt. Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregner PSA antallet på tilbudslinjen.

Dynamics 365 kan for eksempel ha følgende egenskaper: 

- **Antall brukere** – antall brukere 
- **Antall måneder** – antall abonnementsmåneder
- **Produkt-SKU** 

Egenskapene **Antall brukere** og **Antall måneder** kan flagges som antallsfaktorer ved å redigere egenskapene for produktlinjen. 

> ![Flagge Antall brukere og Antall måneder som kvalitetsfaktorer](media/basic-guide-11.png)
 
