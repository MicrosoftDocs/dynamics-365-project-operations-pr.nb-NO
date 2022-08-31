---
title: Synkronisere prosjektstatus for å hindre oppføring mot lukkede prosjekter
description: Denne artikkelen forklarer hvordan du synkroniserer Prosjektstatus for å hindre oppføring mot inaktive eller lukkede prosjekter.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348041"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synkronisere prosjektstatus for å hindre oppføring mot lukkede prosjekter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer_

## <a name="scenario"></a>Scenario

Contoso trer i kraft med Microsoft Dynamics 365 Project Operations for ressursbaserte/ikke-lagerførte scenarioer. Som en del av normale forretningsaktiviteter kan prosjekter fullføres eller settes på vent. Du kan deaktivere prosjektet for å sikre at det ikke genereres utgifter eller fakturaer.

## <a name="solution"></a>Løsning

### <a name="prerequisites"></a>Forutsetning

-   Microsoft Dynamics 365 Finance 10.0.29 eller senere må være installert.
-   To skrivekart 1.0.0.3 for Prosjekter V2 (msdyn\_prosjekter) må installeres eller konfigureres manuelt, som beskrevet nedenfor.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Opprette en oppdatert versjon av Project Operations-integrasjon dobbel skriving for Prosjekter V2

Slik oppdaterer du dobbel skriving for Project Operations Prosjekter V2:

1. Gå til arbeidsområdet **Databehandling** og velg **Dobbel skriving**.
2. Velg **Dobbeltskriving**-flisen.
3. Fra **Tabelltilordning**-kolonnen, finner og velger du **Prosjekter V2 (msdyn\_prosjekter)**, og deretter velger du Stopp.
4. Velg tilordningsnavnet for å åpne tilordningen, og velg deretter **[Ingen]**.
5. Velg **statecode \[Project Status\]** i dialogboksen Velg kolonne, og velg deretter OK. Du kan skrive **tilstand** i filterverdien for å begrense listen.
6.  Velg **Legg til eller rediger transformasjon** i **karttype**-kolonnen for å redigere transformasjonen.
7.  Fra **Transformeringstype** velger du **ValueMap**.
8.  Velg **Legg til verditilordning**, og legg deretter til følgende **Nøkler** og **Verdier**:

   Key       | Verdi 
   ----------|-------
   InProcess | 0     
   fullført | 1     

![Skjermbilde som viser dobbeltskriving](media/projectstage-dw-mapping.png)

9. Velg **Lagre**.
10. Fra toppen av siden **Dobbeltskriving > Prosjekter V2 (msdyn_projects)** velger du **Lagre som**.
11. Fra **Legg til tabell**, i **Utgiver**-feltet, velger du **Standardutgiver for CDS**.
12. Sett **Versjon**-feltet til 1.0.0.3.
13. Skriv inn en **Beskrivelse**, og velg **Lagre**.
14. Fra siden **Dobbeltskriving > Prosjekter V2 (msdyn_projects)** velger du **Kjør** for å starte tilordningen, og deretter velger du **Ja** hvis du blir bedt om å bekrefte før kjøring. 

### <a name="close-a-newly-completed-project"></a>Lukke et nylig fullført prosjekt

Dynamics 365 Finance bruker **prosjektfase**-feltet til å skille mellom prosjekter som er **i arbeid** eller **fullført**. **Fullførte** prosjekter kan ikke pådra seg utgifter eller faktureres til kunder.

1. Åpne et prosjekt som skal deaktiveres.
2. Fra båndet velger du **Deaktiver**.

> [!NOTE]
> Du kan enten deaktivere eller lukke et prosjekt fordi begge vil fungere på samme måte i Finance.

3. Åpne listesiden **Alle prosjekter** i Finance.
4. Bekreft at det deaktiverte prosjektet ikke vises i listen.
5. Endre verdien fra **Aktiv** til **Alle** i filteret **vis prosjekter** over listen.
6. Du ser nå det deaktiverte prosjektet.

Hvis du prøver å logge tid eller utgifter mot dette prosjektet i Finance, skal du ikke se prosjektet for valg. Hvis du angir prosjektnummeret manuelt for en utgift, vises en melding som "Prosjektfase fullført tillater ikke innspilling i prosjektet". Fakturering og andre faktureringsfunksjoner bør deaktiveres fordi de er i konteksten for et lukket prosjekt.

