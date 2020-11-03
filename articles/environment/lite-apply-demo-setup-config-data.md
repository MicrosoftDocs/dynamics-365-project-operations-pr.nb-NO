---
title: Bruk demonstrasjonsoppsett og konfigurasjonsdata
description: Dette emnet gir informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081485"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Bruk demonstrasjonsoppsett og konfigurasjonsdata for Lite-distribusjon i Project Operations – avtale til proformafakturering

_**Lite-distribusjon – avtale til proformafakturering_

1. Last ned [Master data-pakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Naviger til mappen *ProjOpsDemoDataSetupAndMaster - Integrert CMT* , og kjør den kjørbare filen *DataMigrationUtility*.
3. På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.

![Konfigurasjonsoverføring](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.
5. Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.
6. Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.

![Logg på konfigurasjon](./media/2ConfigurationSignin.png)

7. På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.
8. På side 4 velger du zip-filen *MasterAndSetupData* fra den utpakkede mappen, *ProjOpsDemoDataSetupAndMaster - Integrert CMT*.

![Zip-fil](./media/3ZipFile.png)

![Velg en fil](./media/4SelectAFile.png)

9. Når du har valgt zip-filen, velger du **Importer data**.

![Importer data](./media/5ImportData.png)

10. Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten. Når den er fullført, avslutter du CMT-veiviseren. 
11. Kontroller organisasjonen for data i følgende 20 enheter:

- Valuta
- Organisasjonsenhet
- Kontakt
- Avgiftsgruppe
- Kundegruppe
- Enhet
- Enhetsgruppe
- Prisliste
- Prisliste for prosjektparameter
- Fakturafrekvens
- Fakturafrekvensdetalj
- Kategori for ressurs som kan reserveres
- Transaksjonskategori
- Utgiftskategori
- Rollepris
- Pris for transaksjonskategorier
- Kjennetegn
- Ressurs som kan reserveres
- Kategoritilknytning for ressurs som kan reserveres
- Kjennetegn for ressurs som kan reserveres

![Fullført import](./media/6CompleteImport.png)
