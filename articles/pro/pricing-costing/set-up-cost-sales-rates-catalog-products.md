---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Dette emnet gir informasjon om hvordan du konfigurerer kostnads- og salgssatser for varer i en produktkatalog.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764569"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurere kostnads- og salgspriser for katalogprodukter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Definisjon av priser for produktkatalogelementer i Dynamics 365 Project Operations er det samme som i Dynamics 365 Sales.

I Project Operations kan ikke produkter beregnes eller brukes på prosjekter, så produktkatalogpriser behøver ikke angis i prosjektprislister for tilbud og kontrakter.

Bruk feltet **Produktpris** i et tilbud, en kontrakt eller en konto til å angi produktkatalogpriser. Ikke definer produktkatalogpriser i prosjektprislistene. Prosjektprislister er eksklusive for Project Operations. Appspesifikk forretningslogikk kopierer prislistene fra et tilbud til en kontrakt. Resultatet er en kontraktsspesifikk prosjektprisliste. Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor. Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter. Ettersom ingen kopiering er involvert, påvirkes ikke ytelsen til tilbudsprosessen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]