---
title: Bruke demonstrasjonsoppsett og konfigurasjonsdata – Lite
description: Dette emnet gir informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ecb5da3bccf35f8ed7e2246f68dd4da2b145c6be
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587000"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Bruke demonstrasjonsoppsett og konfigurasjonsdata for Project Operations – Lite 

_**Lite-distribusjon – avtale til proformafakturering_



## <a name="prerequisites"></a>Forutsetninger

Før du begynner å konfigurere, må du ha et Common Data Service (CDS)-miljø klargjort for Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruksjoner

1. Last ned [Master data-pakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Naviger til mappen *ProjOpsSampleSetupData - CE only CMT*, og kjør den kjørbare filen *DataMigrationUtility*.
3. På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.

    ![Konfigurasjonsoverføring.](./media/1ConfigurationMigration.png)

4. På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.
5. Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.
6. Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.

   ![Logg på konfigurasjon.](./media/2ConfigurationSignin.png)

7. På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.
8. På side 4 velger du ZIP-filen, *SampleSetupAndConfigData* fra mappen som er pakket ut, *ProjOpsSampleSetupData – CE only CMT*.

   ![Zip-fil.](./media/3ZipFile.png)

   ![Velg en fil.](./media/4SelectAFile.png)

9. Når du har valgt zip-filen, velger du **Importer data**.

   ![Importer data.](./media/5ImportData.png)

10. Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten. Når den er fullført, avslutter du CMT-veiviseren. 
11. Kontroller organisasjonen for data i følgende 18 enheter:

    -   Valuta
    -   Konto
    -   Organisasjonsenhet
    -   Kontakt
    -   Enhet
    -   Enhetsgruppe
    -   Prisliste
    -   Prisliste for prosjektparameter 
    -   Fakturafrekvens
    -   Kategori for ressurs som kan reserveres
    -   Transaksjonskategori
    -   Utgiftskategori
    -   Rollepris
    -   Pris for transaksjonskategorier
    -   Kjennetegn
    -   Ressurs som kan reserveres
    -   Kategoritilknytning for ressurs som kan reserveres
    -   Kjennetegn for ressurs som kan reserveres

    ![Fullført import.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
