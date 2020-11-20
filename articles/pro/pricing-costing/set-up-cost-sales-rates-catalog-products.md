---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176713"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurere kostnads- og salgspriser for katalogprodukter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Konfigurering av priser for produktkatalogvarer i Dynamics 365 Project Operations er likt som i Dynamics 365 Sales.

Siden produkter ikke kan estimeres eller brukes i prosjekter i Project Operations, er det ikke nødvendig å angi produktkatalogpriser i prosjektprislister for tilbud og kontrakter.

Produktkatalogpriser bør konfigureres i **Produktpris**-feltet for et tilbud, en kontrakt eller en forretningsforbindelse. Ikke konfigurer produktkatalogpriser i prosjektprislistene for disse enhetene. Prosjektprislister er eksklusive for Project Operations. Det finnes programspesifikk forretningslogikk som kopierer prislistene fra et tilbud til en kontrakt. Resultatet er en kontraktsspesifikk prosjektprisliste. Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor. Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter. Dette betyr at produktprislister ikke påvirker ytelsen til prosessen ved å vinne tilbudet.
