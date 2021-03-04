---
title: Konfigurere standardkostnader for arbeid og utgifter
description: Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081677"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Konfigurere standardkostnader for arbeid og utgifter

[!include [banner](../../includes/banner.md)]

Dette emnet forklarer hvordan du definerer standardkostnader for arbeid og utgifter for et prosjekt. Denne oppgaven bruker USSI-datasett.

1. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (time)**.
2. Velg **Ny**.
3. Angi en dato i feltet **Effektiv dato**.
4. Angi et tall i **Kostpris** -feltet. Du kan angi en standard kostpris for prosjektkategorien, eller du kan angi en kostpris basert på arbeidernummer, prosjektnummer, kategori, dato eller en hvilken som helst kombinasjon av disse. Kostprisen som brukes, er kostprisen på det høyeste detaljnivået.  
5. Velg **Lagre**.
6. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgspris (time)**.
7. Velg **Ny**.
8. Angi en dato i feltet **Effektiv dato**.
9. Velt et alternativ i feltet **Gyldig for**.
10. Angi et tall i **Priser** -feltet. Du kan angi en standard salgspris for timetransaksjoner eller for en prosjektkategori. Du kan også angi salgspriser etter arbeidernummer, prosjektnummer, kategori, transaksjonsdato eller en hvilken som helst kombinasjon av disse. Den faktiske salgsprisen, som brukes når en arbeider angir en transaksjon i timejournalen, er salgsprisen med høyest detaljnivå. Hvis det for eksempel er angitt både en generell salgspris og en arbeidsspesifikk salgspris, brukes den arbeidsspesifikke salgsprisen.  
11. Velg **Lagre**.
12. Lukk siden.
13. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Kostpris (utgift)**.
14. Velg **Ny**.
15. Angi en dato i feltet **Effektiv dato**.
16. Angi et tall i **Kostpris** -feltet. Flere felt kan fylles ut, men dette er minimum som kreves for å lagre oppføringen.  
17. Velg **Lagre**.
18. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Salgpris (utgift)**.
19. Velg **Ny**.
20. Angi en dato i feltet **Effektiv dato**.
21. Velt et alternativ i feltet **Gyldig for**.
22. Angi et tall i **Priser** -feltet. Den faktiske salgsprisen, som brukes når en arbeider angir transaksjoner i en utgiftsjournalen, er salgsprisen med høyest detaljnivå. Hvis det for eksempel er angitt både en generell og en arbeidsspesifikk salgspris, brukes den arbeidsspesifikke salgsprisen.  
23. Velg **Lagre**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]