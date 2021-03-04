---
title: Motta varer på bestilling fra varebehov
description: Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081787"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Motta varer på bestilling fra varebehov

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du mottar varer på en bestilling fra et varebehov.

Ved å bruke et varebehov i stedet for en varetransaksjon kan du planlegge levering rett før varen faktisk brukes, opprette en bestilling, inkludere varen i handelsavtalestrukturen og inkludere varebehovet i produksjonsplanlegging. 

Denne oppgaven bruker USSI-datasett.

1. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter**.
2. I listen velger du koblingen i den ønskede raden.
3. Velg **Plan** i handlingsruten.
4. Velg **Elementkrav**.
5. Velg **Ny**.
6. Skriv inn eller velg en verdi i feltet **Varenummer**.
7. Angi et tall i **Antall** -feltet.
8. Velg **Lagre**.
9. Velg **Behandle** i handlingsruten.
10. Velg **Funksjoner**.
11. Velg **Opprett bestilling**.
12. Merk av for **Inkluder alle**.
13. Skriv inn eller velg en verdi i **Leverandørkonto** -feltet.
14. Velg **OK**.
15. I navigasjonsruten går du til **Moduler > Leverandørgjeld > Bestillinger > Alle bestillinger**.
16. I listen velger du koblingen i den ønskede raden.
17. Velg **Kjøp** i handlingsruten.
18. Velg **Bekreft**.
19. Velg **Motta** i handlingsruten.
20. Velg **Produktkvittering**.
21. Skriv inn en verdi i feltet **Produktkvittering**.
22. Velg **OK**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]