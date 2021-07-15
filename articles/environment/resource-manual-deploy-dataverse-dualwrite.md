---
title: Distribuer Project Operations Dataverse-appen manuelt med støtte for dobbel skriving
description: Dette emnet forklarer hvordan du distribuerer Project Operations Dataverse-appen manuelt slik at den støtter dobbel skriving.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274020"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Distribuer Project Operations Dataverse-appen manuelt med støtte for dobbel skriving

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Dette emnet forklarer hvordan du distribuerer Microsoft Dynamics 365 Project Operations i Microsoft Dataverse slik at den støtter dobbel skriving. Project Operations registrerer konfigurasjonen av miljøet og legger til ytterligere støtte for dobbel skriving hvis forutsetningene oppfylles.

Hvis du har fulgt instruksjonene i dette emnet under distribusjon gjennom Microsoft Dynamics Lifecycle Services (LCS), kan du hoppe over distribusjonen av Microsoft Power Platform-integreringen (tidligere kjent som Common Data Service-miljøet).

Prosessen med å distribuere Project Operations i Dataverse slik at den støtter dobbel skriving har fire hovedtrinn:

1. [Opprett et nytt miljø i Dataverse som støtter dobbel skriving](#create).
2. [Legg til forutsetninger til dobbel skriving i miljøet](#prerequisites).
3. [Legg til Project Operations Dataverse-appen](#dataverse).
4. [Koble til miljøene](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Opprett et nytt miljø i Dataverse som støtter dobbel skriving

Hvis du vil fullføre denne fremgangsmåten, må du logge på som administrator.

1. Åpne [Power Platform-administrasjonssenteret](https://admin.powerplatform.com), og logg på som administrator.
2. Opprett et nytt miljø og gi det navn.
3. Velg miljøtypen. Hvis du registrerte deg for prøveversjonstilbudet, velger du **Prøveversjon (abonnementsbasert)**.
4. Bekreft distribusjonsområdet.
5. Aktiver alternativet **Opprett en database for dette miljøet**. 
6. Bekreft språket, og bekreft deretter at valutaen samsvarer med valutaen for Finance and Operations-appene dine.
7. Aktiver alternativet **Dynamics 365-apper**, og bekreft at feltet **Automatisk distribusjon av disse appene** er satt til **Ingen**.
8. Legg til en sikkerhetsgruppe hvis det kreves en sikkerhetsgruppe.
9. Velg **Lagre** for å opprette miljøet.
10. Vent til distribusjonen er fullført og miljøet når tilstanden **Klar**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Legg til forutsetninger til dobbel skriving i miljøet

Støtte for dobbel skriving inkluderer flere felter som legges til viktige enheter, for eksempel **Firma**-enheten. Hvis du legger til støtte for dobbel skriving i et eksisterende miljø, må du kanskje oppdatere dataene for å aktivere støtten. Hvis du vil ha mer informasjon om hvordan du starter opp dataene, kan du se [Bootstrap-firmadata](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Hvis du vil ha mer informasjon om dobbel skriving, kan du se [Systemkrav for dobbel skriving](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Fullfør denne fremgangsmåten for å legge til forutsetningene for dobbel skriving i miljøet.

1. Åpne miljøet du nettopp opprettet, og gå deretter til **Ressurs** \> **Dynamics 365-apper**.
2. Velg **Løsning for dobbel skriving** i applisten, og installer den.
3. Vent til installasjonen er fullført. Velg deretter **Orkestreringsløsning for dobbel skriving** i applisten, og installer den.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Legg til Project Operations Dataverse-appen

Du kan bare fullføre denne fremgangsmåten hvis du har fullført de forrige fremgangsmåtene før du installerte Project Operations. Under installasjonen analyserer systemet miljøkonfigurasjonen og støtte for dobbel skriving hvis det er nødvendig.

1. Åpne miljøet du opprettet tidligere, og gå deretter til **Ressurs** \> **Dynamics 365-apper**.
2. Velg **Microsoft Dynamics 365 Project Operations** i applisten, og installer den.

## <a name="link-your-environments"></a><a name="link"></a>Koble til miljøene

Når Dataverse-miljøet er distribuert, kan du konfigurere koblingen i Finance and Operations-appene dine. Følg fremgangsmåten i [Bruk veiviseren for dobbel skriving til å koble miljøene](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).