---
title: Bruke demonstrasjonsoppsett og konfigurasjonsdata – Lite
description: Denne artikkelen inneholder informasjon om hvordan du bruker demonstrasjonsoppsett og konfigurasjonsdata for Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811038"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Bruke demonstrasjonsoppsett og konfigurasjonsdata for Project Operations – Lite 

_**Lite-distribusjon – avtale til proformafakturering_



## <a name="prerequisites"></a>Forutsetning

Før du begynner å konfigurere, må du ha et Dataverse-miljø klargjort for Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruksjoner

1. Last ned [konfigurasjonsdatapakken](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Naviger til mappen *ProjOpsSampleSetupData - CE only CMT*, og kjør den kjørbare filen *DataMigrationUtility*.
1. På side 1 i Common Data Service-veiviseren for konfigurasjonsoverføring (CMT) velger du **Importer data** og deretter **Fortsett**.

    ![Konfigurasjonsoverføring.](./media/1ConfigurationMigration.png)

1. På side 2 i CMT-veiviseren velger du **Microsoft 365** som **Distribusjonstype**.
1. Merk av for **Vis en liste over tilgjengelige organisasjoner** og **Vis avansert**.
1. Velg området for leieren din, skriv inn legitimasjonen din, og velg deretter **Logg på**.

   ![Logg på konfigurasjon.](./media/2ConfigurationSignin.png)

1. På side 3, fra listen over organisasjoner i leieren, velger du organisasjonen du vil importere demonstrasjonsdata til, og deretter velger du **Logg på**.
1. På side 4 velger du ZIP-filen, *SampleSetupAndConfigData* fra mappen som er pakket ut, *ProjOpsSampleSetupData – CE only CMT*.

   ![Zip-fil.](./media/3ZipFile.png)

   ![Velg en fil.](./media/4SelectAFile.png)

1. Når du har valgt zip-filen, velger du **Importer data**.

   ![Importer data.](./media/5ImportData.png)

1. Importen kjører i omtrent 2 til 10 minutter, avhengig av nettverkshastigheten. Når den er fullført, avslutter du CMT-veiviseren. 
1. Kontroller organisasjonen for data i følgende 18 enheter:

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
