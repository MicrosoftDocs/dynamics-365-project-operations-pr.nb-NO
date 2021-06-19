---
title: Oppgraderingshensyn for arbeidsnedbrytningsstruktur
description: Dette emnet gir informasjon om oppgradering av arbeidsnedbrytningsstrukturen fra Project Service Automation 2.x til 3.x.
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 868b0daadaf6cf96ca7bf847914bca8014412f26
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005623"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a>Oppgraderingshensyn for arbeidsnedbrytningsstruktur

[!include [banner](../includes/psa-now-project-operations.md)]

Dette emnet gir informasjon om oppgradering av arbeidsnedbrytningsstrukturen fra Project Service Automation 2.x til 3.x. Dette emnet definerer om statusen for et prosjekt er ok i Project Service Automation (PSA), slik at en vellykket oppgradering kan utføres. Det finnes også informasjon om vanlige blokkeringstilstander som vil føre til at oppgraderingen mislykkes. Hvis du vil ha mer informasjon om hvordan du definerer prosjektpppgaver og deres funksjoner i en prosjekttidsplan, kan du se [Prosjektplaner](project-creating.md).

## <a name="key-entities"></a>Viktige enheter
For en presis arbeidsnedbrytningsstruktur som allerede er lastet inn med ressurser, kreves følgende enheter:

- [Prosjekt](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [Prosjektteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [Prosjektoppgave](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [Ressurstilordninger](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [Avhengighet for prosjektoppgaver](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [Ressurser som kan reserveres](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

For å definere en ressursbelastet arbeidsnedbrytingsstruktur må du utføre følgende trinn:

1. Opprett et nytt prosjekt. Hvis du vil ha mer informasjon om hvordan du oppretter et nytt prosjekt, se [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).
2. Opprett én eller flere oppgaver. Hvis du vil ha mer informasjon om hvordan du oppretter en oppgave, se [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).
3. Definer aktivitetsavhengighetene. Hvis du vil ha mer informasjon, se [Avhengighet for prosjektoppgaver](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).
4. Tilordne prosjektteammedlemmer til prosjektet. Hvis du vil ha mer informasjon, kan du se [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).
5. Tilordne prosjektteammedlemmer til oppgavene. Hvis du vil ha mer informasjon, kan du se [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).

## <a name="project-team-relationships"></a>Prosjektteamrelasjoner

For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:
- Alle prosjektteammedlemmer må tilknyttes en ressurs som kan reserveres.
- Alle prosjektteammedlemmer må tilknyttes samme prosjekt. 

## <a name="project-task-relationships"></a>Prosjektoppgaverelasjoner
For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:

- Alle relaterte oppgaver må tilknyttes samme prosjekt.
- Hver linjeoppgave må ha en overordnet oppgave.
- Hver oppgave må ha et overordnet prosjekt.

### <a name="valid-conditions"></a>Gyldige betingelser

- Alle oppgavevarigheter må være større enn eller lik (> =) én time og mindre enn 1 800 000 minutter (1 250 dager). *
- Alle oppgaver må ha en startdato som ikke er tidligere enn 2000/01/01.*
- Alle oppgaver må ha en startdato som ikke er senere enn 17 år fra den gjeldende dagen.*
- Alle oppgaver må ha en startdato som er tidligere enn eller lik sluttdatoen.
- Alle transaksjonstyper på klassifiseringer (utgift, material, avgift og tid) må ha verdier for **Standardenhet** og **Enhetsgruppe**.
- Datoformater med bokstaver bør unngås.

### <a name="potential-mitigation-steps"></a>Potensielle løsningstrinn
- Bruk Avansert søk til å identifisere prosjektoppgaver som ikke inneholder en prosjekt-ID.
- Bruk Avansert søk til å identifisere prosjektoppgaver der planlagt varighet er større enn > 1 800 000.
- Før du gjør endringer i dataene må du undersøke alle tilpassinger som er knyttet til enheten, og som kan ha fått dataene i en ugyldig tilstand. Disse tilpassingene bør adresseres før du fortsetter med datarelaterte oppdateringer.
- For de identifiserte oppgavene som har vært isolerte, bør du vurdere å slette disse oppgavene hvis de ikke er nødvendige, eller hvis de skal knyttes til det riktige overordnede prosjektet.
- For alle oppgaver der varigheten er større enn 1 250 dager, bør du vurdere å legge til flere oppgaver for å representere den totale varigheten hvis det er mulig.

> [!NOTE]
> Elementer som er angitt med en stjerne (\*), har grenser som skyldes at kunderelasjonsstyring (CRM) bare støtter 7 320 regelmessighetsutvidelser. Du må være under denne grensen.

## <a name="resource-assignment-relationships"></a>Ressurstilordningsrelasjoner
For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:

- Alle ressurstilordninger i en arbeidsnedbrytningsstruktur må være relatert til samme prosjekt.
- Alle ressurstilordninger i en arbeidsnedbrytningsstruktur må være tilknyttet prosjekteammedlemmene i samme prosjekt.

### <a name="potential-mitigation-steps"></a>Potensielle løsningstrinn
- Identifiser alle oppgaver som faller utenfor vilkårene som er beskrevet ovenfor.  
- Eventuelle ressurstilordninger som ikke er gyldige lenger, må slettes.

## <a name="project-task-dependency-relationships"></a>Relasjoner for prosjektoppgaveavhengighet
For å sikre en vellykket oppgradering må følgende relasjoner vedlikeholdes på riktig måte:

- Alle avhengigheter for prosjektoppgaver må være relatert til samme prosjekt.
- En oppgave kan ikke referere til samme avhengighet mer enn én gang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]