---
title: Bestill ikke-lagerføre materialer for et prosjekt ved hjelp av prosjektbestillinger
description: Dette emnet forklarer hvordan du kan bestille ikke-lagerføre materialer for et prosjekt ved hjelp av prosjektbestillinger.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2aa8fb94e2f9cbf91182f3f169339284d3eb9f44
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612715"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Bestill innkjøpskategorier eller ikke-lagerføre materialer for et prosjekt ved hjelp av prosjektbestillinger

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

Innkjøpsavdelingen i organisasjonen kan bruke [bestillinger](/dynamics365/supply-chain/procurement/purchase-order-overview) til å spore varer og serviceordrer. Bestillinger for innkjøpskategorier ikke-lagerføre materialer kan skrives til et prosjekter. Fakturering av disse bestillingene registrerer kostnadene mot prosjektet.

## <a name="prerequisites"></a>Forutsetninger
Fullfør fremgangsmåten nedenfor for å aktivere funksjonaliteten for bestillinger.

1. I Dynamics 365 Finance går du til arbeidsområdet **Funksjonsbehandling**.
2. Finn og velg funksjonen i funksjonslisten, **Aktiver prosjektbestillinger på Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer**.
3. Velg **Aktiver**.
4. Konfigurere ikke-lagerført materiell og ventende leverandørfakturaer slik det er beskrevet i [Konfigurer ikke-lagerført materiell og ventende leverandørfakturaer](configure-materials-nonstocked.md).
5. Konfigurer innkjøpskategorier som beskrevet i [Bruk innkjøpskategorier med prosjektbestillinger og ventende leverandørfakturaer](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Opprett en prosjektbestilling fra prosjektbestillingslisten

1. I Finance går du til **Prosjektstyring og regnskap** > **Prosjekter** > **Alle prosjekter** og velger et prosjekt.
2. På handlingsruten på fanen **Administrer** i **Ny**-gruppen velger du **Vareoppgave** > **Bestilling**.
3. På siden **Opprett bestilling** velger du leverandøren du vil legge inn bestillingen hos, angir annen informasjon etter behov, og deretter velger du **OK**.
4. På siden **Bestilling** i **Bestillingslinjer**-rutenettet velger du **Legg til linje**.
5. Angi et varenummer eller en innkjøpskategori, antall, enhet, enhetspris og annen informasjon etter behov.

    > [!NOTE]
    > Bare innkjøpskategorier, ikke-lagerførte varer og tjenester kan brukes med prosjektbestilllinger. Lagerførte varer støttes ikke.

6. Fortsett for å legge til varer eller innkjøpskategorier etter behov, og bekreft bestillingen.

    Vare- og tjenestekvitteringer kan registreres ved å opprette og bokføre en produktkvittering.

    > [!NOTE]
    > Produktkvitteringer registreres ikke for de faktiske prosjektene i Microsoft Dataverse, og har ikke innvirkning på underfinansen for prosjektet.

    Når en leverandør har sendt fakturaen for varer og tjenester i bestillingen, kan innkjøpsavdelingen generere en faktura for bestillingen ved å gå til **Faktura** > **Generer** > **Faktura** i handlingsruten. Hvis du vil ha mer informasjon om ventende leverandørfakturaer, kan du se [Kjøp ikke-lagerført materiell ved hjelp av en ventende leverandørfaktura](pending-vendor-invoices.md).
