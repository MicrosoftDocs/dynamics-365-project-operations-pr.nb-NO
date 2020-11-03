---
title: Konfigurere kostnads- og salgspriser for katalogprodukter
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081687"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Konfigurere kostnads- og salgspriser for katalogprodukter

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Konfigurering av priser for produktkatalogvarer i Dynamics 365 Project Operations er likt som i Dynamics 365 Sales.

Siden produkter ikke kan estimeres eller brukes i prosjekter i Project Operations, er det ikke nødvendig å angi produktkatalogpriser i prosjektprislister for tilbud og kontrakter.

Produktkatalogpriser bør konfigureres i **Produktpris** -feltet for et tilbud, en kontrakt eller en forretningsforbindelse. Ikke konfigurer produktkatalogpriser i prosjektprislistene for disse enhetene. Prosjektprislister er eksklusive for Project Operations. Det finnes programspesifikk forretningslogikk som kopierer prislistene fra et tilbud til en kontrakt. Resultatet er en kontraktsspesifikk prosjektprisliste. Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor. Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter. Dette betyr at produktprislister ikke påvirker ytelsen til prosessen ved å vinne tilbudet.
