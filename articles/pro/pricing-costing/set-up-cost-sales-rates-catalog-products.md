---
title: Konfigurere kostnads- og salgspriser for katalogprodukter – Lite
description: Denne artikkelen inneholder informasjon om hvordan du definerer kostnads- og salgspriser for varer i en produktkatalog.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4689d6929e24ebaa992232f809a7ec60908ee517
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917404"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Konfigurere kostnads- og salgspriser for katalogprodukter – Lite

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_


Definisjon av priser for produktkatalogelementer i Dynamics 365 Project Operations er det samme som i Dynamics 365 Sales.

I Project Operations kan ikke produkter beregnes eller brukes på prosjekter, så produktkatalogpriser behøver ikke angis i prosjektprislister for tilbud og kontrakter.

Bruk feltet **Produktpris** i et tilbud, en kontrakt eller en konto til å angi produktkatalogpriser. Ikke definer produktkatalogpriser i prosjektprislistene. Prosjektprislister er eksklusive for Project Operations. Appspesifikk forretningslogikk kopierer prislistene fra et tilbud til en kontrakt. Resultatet er en kontraktsspesifikk prosjektprisliste. Kopieringsoperasjonen kan forsinke prosessen med å vinne tilbudet hvis prosjektprislisten i tilbudet blir for stor. Produktprislister kopieres ikke for å opprette egendefinerte prislister i kontrakter. Ettersom ingen kopiering er involvert, påvirkes ikke ytelsen til tilbudsprosessen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]