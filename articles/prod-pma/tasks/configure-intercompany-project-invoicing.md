---
title: Konfigurere intern prosjektfakturering
description: Denne artikkelen viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 74548a4c30ceb6826e5280948f6829e567bc02e0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916622"
---
# <a name="configure-intercompany-project-invoicing"></a>Konfigurere intern prosjektfakturering

[!include [banner](../../includes/banner.md)]

Denne artikkelen viser hvordan du konfigurerer prosjektfakturering mellom to firmaer i organisasjonen. Denne oppgaven bruker USSI-datasett.

1. I navigasjonsruten går du til **Moduler > Leverandørgjelde > Leverandører > Alle leverandører**.
2. I listen **Alle leverandører** finner og velger du ønsket oppføring.
3. Velg **Generelt** i handlingsruten.
4. Velg **Konsernintern**.
5. Sett **Aktiv** til **Ja** for å aktivere konserninternt salg.
6. Skriv inn eller velg en verdi i **Kundefirma**-feltet.
7. Skriv inn eller velg en verdi i **Min konto**-feltet.
8. Velg **Lagre**.
9. Lukk sidene for å gå tilbake til startsiden.
10. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Parametere for prosjektstyring og regnskap**.
11. Velg kategorien **Konsernintern**.
12. Flytt glidebryteren til **Ja** for å aktivere planlegging og timelister for konsernintern ressurs.
13. Merk den valgte raden i listen.
14. Velg **Ny**.
15. Skriv inn eller velg en verdi i **Juridisk enhet som låner**-feltet.
16. Merk av for **Avsett inntekt**.
17. Skriv inn eller velg en verdi i **Standard timeregistreringskategori**-feltet.
18. Skriv inn eller velg en verdi i **Standard utgiftskategori**-feltet.
19. Velg **Lagre**.
20. Lukk siden.
21. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Bokføring > Finansposteringsoppsett**.
22. I feltet **Finanskontotyper** velger du et alternativ.
23. Velg **Ny**.
24. I feltet **Hovedkonto** i den nye raden angir du ønskede verdier.
25. Velg **Lagre**.
26. Lukk siden.
27. I navigasjonsruten går du til **Moduler > Prosjektstyring og regnskap > Oppsett > Priser > Overføringspris**.
28. Velg **Ny**.
29. Angi en dato i feltet **Effektiv dato**.
30. Skriv inn eller velg en verdi i **Juridisk enhet som låner**-feltet.
31. Velg et alternativ i feltet **Overføringsprismodell**.
32. Angi et tall i **Priser**-feltet.
33. Velg **Lagre**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]