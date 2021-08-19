---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bfb28e710c7b6da17d94679a72659f81df7a58e376e4bad94b58c36de781b197
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996043"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurere kostnads- og salgspriser for katalogprodukter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Definisjon av priser for produktkatalogelementer i Dynamics 365 Project Operations er det samme som i Dynamics 365 Sales.

I Project Operations kan ikke produkter beregnes eller brukes på prosjekter, så produktkatalogpriser behøver ikke angis i prosjektprislister for tilbud og kontrakter.

Bruk feltet **Produktpris** i et tilbud, en kontrakt eller en konto til å angi produktkatalogpriser. Ikke definer produktkatalogpriser i prosjektprislistene. Prosjektprislister er eksklusive for Project Operations. Appspesifikk forretningslogikk kopierer prislistene fra et tilbud til en kontrakt. Resultatet er en kontraktsspesifikk prosjektprisliste. Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor. Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter. Ettersom ingen kopiering er involvert, påvirkes ikke ytelsen til tilbudsprosessen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]