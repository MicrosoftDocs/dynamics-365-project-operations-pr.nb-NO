---
title: Hva er nytt eller endret i Project Service Automation Update Release 26, V3
description: Dette emnet viser funksjonene og reparasjonene som er tilgjengelig i Project Service Automation Update Release 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143570"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, Update Release 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Vi er glad for å annonsere den nyeste oppdateringen for Project Service Automation-programmet for Dynamics 365. Denne versjonen inkluderer viktige forbedringer av kvalitet, ytelse og anvendelighet. Denne versjonen er kompatibel med Dynamics 365 9.x. Hvis du vil oppdatere til denne versjonen, går du til administrasjonssenteret for Dynamics 365 online, og deretter går du til løsningssiden for å installere oppdateringen. For mer informasjon, se [Installere, oppdatere eller fjerne en foretrukket løsning](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Dette emnet viser funksjonene og rettinger som er nye eller endrede for Project Service Automation Update Release 26, V3. Denne versjonen har et build-nummer for V 3.10.44.59, og er generelt tilgjengelig via en egen oppdatering i desember 2020.

## <a name="update-release-26"></a>Update Release 26

### <a name="bug-fixes"></a>Feilrettinger

**Tid og utgift**

Følgende problemer har blitt løst:

- Brukere kan endre oppgaven i en tidsoppføring som er godkjent/sendt.
- «Objektreferanse er ikke angitt»-feilmelding under lagring av tidsoppføring.
- Tidsoppføringimport fra ressurstildelinger oppretter tidsoppføringer med feil dato/klokkeslett-verdier.
- Når både Project Service Automation- og Field Service-appen er installert, vises **Ny**-knappen to ganger på kommandolinjen for tidsoppføringer i Field Service-appen.
- **Tillat enhet** og **Enhetsgruppe**-celleoppdateringer fungerer nå på **Utgiftsestimat**-rutenettet.
- **Oppdater redigering for tidsoppføring**-skjema inkluderer **Tidslinje**.
- Tidsgodkjenning for tidsoppføringer som ikke er prosjekt, blokkerer systemet ved søk etter en prosjektgodkjennerrolle.

**Ressursbehandling**

Følgende problemer har blitt løst:

- Ekstra validering i **PostProjectCreate**-programtillegget for å se etter et primært krav før du oppretter et.
- **Prosjektteammedlem**-hurtigopprettingsskjema genererer et nullreferanseunntak hvis felt fjernes fra skjemaet.
- Generering av krav for 12 timer over 1 år vil mislykkes.
- Forbedret feilmelding om nullreferanseunntak under oppretting av ressurskrav.

**Prosjektledelse**

Følgende problemer har blitt løst:

- Forbedret validering for å løse nullreferanseunntak generert i **PreProjectUpdate**-programtillegget.
- Prosjekter som publiseres av Microsoft Project-tilleggsprogrammet, sletter oppgaver som ikke er tilordnet.
- Ekstra ny validering når en prosjektreferanse for en oppgave er ugyldig på grunn av nullreferanseunntak i **PreValidateProjectTaskUpdate**-programtillegget.
- Teammedlem-rutenettet viser ikke forskjellige tildelinger på teammedlemsoppføringen.
- Ekstra ny validering og feilmeldinger som skyldes nullreferanseunntak i **PreProjectTaskDelete**-programtillegget.

**Sales**

Følgende problemer har blitt løst:

- Når du velger en prosjektbasert linje i tilbud eller kontrakt, skal **Forslag**-knappen kun være synlig når du velger en produktbasert linje som er tilknyttet et eksisterende produkt.
- Dele **Create_Product**-rettighet fra **Create_ProjectContracts**-rettighet.
- Sletting av en fakturalinje forårsaker nullreferansefeil på **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.
