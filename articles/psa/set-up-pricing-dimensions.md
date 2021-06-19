---
title: Konfigurere egendefinerte felt som prisdimensjoner
description: Dette emnet gir informasjon om hvordan du konfigurerer egendefinerte prisdimensjoner.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: cce3a3fe6aef247380f6284f58d49337f969c38c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008323"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Konfigurere egendefinerte felt som prisdimensjoner 

[!include [banner](../includes/psa-now-project-operations.md)]

Før du begynner antar dette emnet at du har fullført prosedyrene i emnene [Opprette egendefinerte felt og enheter](create-custom-fields-entities.md) og [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md). Hvis du ikke har utført disse prosedyrene, kan du gå tilbake og fullføre dem og deretter gå tilbake til dette emnet. 

Dette emnet gir informasjon om hvordan du konfigurerer egendefinerte prisdimensjoner. I Project Service-webgrensesnittet, på siden **Parametere**, viser kategorien **Beløpsbaserte prisdimensjoner** oppføringene i prisingsdimensjonsenhetene. Som standard oppretter Project Service-installasjonen 2 rader i rutenettet i denne kategorien:

- **msdyn_resourcecategory** (rolle)
- **msdyn_OrganizationalUnit** (organisasjonsenhet)

> [!IMPORTANT]
> Ikke slett disse radene. Hvis du ikke trenger dem, kan du imidlertid gjøre dem tilgjengelige i en bestemt kontekst ved å angi **Gjelder kostnad**, **Gjelder salg** og **Gjelder kjøp** til **Nei**. Ved å sette disse attributtverdiene til **Nei**, har det samme effekt som å ikke ha feltet som prisdimensjon.

For at et felt skal bli en prismodell, må det være følgende:

- Opprettet som et felt i enhetene **Rollepris** og **Rolleprispåslag**. For mer informasjon om hvordan du gjør dette, se [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md).
- Opprettet som en rad i tabellen **Prisdimensjon**. Legg for eksempel til prisdimensjonsrader som vises i grafikken nedenfor. 

![Rader for beløpsbaserte prisdimensjoner](media/Amt-based-PD.png)

Merk at Arbeidstimer for ressurs (**msdyn_resourceworkhours**) er lagt til som en påslagsbasert dimensjon og er lagt til i rutenettet i kategorien **Påslagsbasert prisdimensjon**.

![Rader for påslagsbaserte prisdimensjon](media/Markup-based-PD.png)

> [!IMPORTANT]
> Alle endringer i prisdimensjonsdata i denne tabellen, eksisterende eller nye, overføres bare til Project Service-prisforretningslogikken når hurtigbufferen er oppdatert. Oppdateringstiden for bufferen kan ta opptil 10 minutter. Vent denne tiden for å se endringene i standardlogikken for priser som må resultere fra endringer i prisdimensjonsdata.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Attributter for prisdimensjonstabellen
Avsnittene nedenfor inneholder informasjon om de forskjellige attributtene i tabellen **Prisdimensjoner**.

### <a name="pricing-dimension-name"></a>Prisdimensjonsnavn
Denne verdien må være identisk med skjemanavnet til feltet som legges til i tabellen **Rollepris** for egendefinerte prisdimensjoner. Hvis du vil ha mer informasjon om hvordan du legger til felt i tabellen **Rollepris**, kan du se [Legge til egendefinerte felt i prisoppsett og transaksjonsenheter](field-references.md).

### <a name="type-of-dimension"></a>Dimensjonstype
Det finnes to typer prisdimensjoner:
  
  - **Beløpsbaserte dimensjoner**: Dimensjonsverdiene fra inndatakonteksten samsvares med dimensjonsverdiene på linjen **Rollepris**, og prisen/kostnaden settes som standard direkte fra tabellen **Rollepris**.
  - **Påslagsbaserte prisdimensjoner**: Dette er dimensjoner der Project Service bruker følgende 3-trinnsprosess til å hente pris/kostnad
 
    1. Project Service samsvarer med ikke-påslagsbaserte dimensjonsverdier fra inndatakonteksten til Rollepris-linjen for å hente basisprisen.
    2. Project Service samsvarer med alle dimensjonsverdier fra inndatakonteksten til **Rolleprispåslag**-linjen for å hente påslagsprosenten.
    3. Project Service bruker påslagsprosenten fra det andre trinnet i basisprisen som hentes fra **Rollepris**-tabellen i det første trinnet, for å komme til endelig pris/kostnad.
   
   Tabellen nedenfor illustrerer beregning av prispåslag.
  
| Rolle        | Organisasjonsenhet    |Arbeidssted      |Standardtittel      |Arbeidstid for ressurs      |  Påslag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|På stedet            |                    |Overtid                 |15     |
|             | Contoso India|Lokal             |                    |Overtid                 |10     |
|             | Contoso – USA   |Lokal             |                    |Overtid                 |20     |


Hvis en ressurs fra Contoso India som har en basispris på 100 USD, arbeider på stedet, og de registrerer 8 timer normal tid og 2 timer overtid i tidsoppføringen, vil Project Service-prismotoren bruke basisprisen på 100 for de 8 timene for å registrere 800 USD. For de 2 timene overtid brukes et påslag på 15 % på basisprisen på100 for å få en enhetspris på 115 USD, og det registreres en total kostnad på 230 USD.

### <a name="applicable-to-cost"></a>Gjelder kostnad 
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av kostnads- og påslagsrater.

### <a name="applicable-to-sales"></a>Gjelder salg
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av faktura- og påslagsrater.

### <a name="applicable-to-purchase"></a>Gjelder kjøp
Hvis det er satt til **Ja**, indikerer det at dimensjonsverdien fra inndatakonteksten skal brukes til å samsvare **Rollepris** og **Rolleprispåslag** ved henting av kjøpsprisen. For tiden støtter ikke Project Service underleveransescenarioer, så dette feltet brukes ikke. 

### <a name="priority"></a>Prioritet
Ved å angi dimensjonsprioriteten kan Project Service-prisingen produsere en pris selv når den ikke finner et nøyaktig samsvar mellom inndatadimensjonsverdiene og verdiene fra tabellene **Rollepris** eller **Rolleprispåslag**. I dette scenarioet bruker Project Service nullverdier for dimensjonsverdier som ikke samsvarer, ved å vekte dimensjonene i henhold til prioriteten.

- **Kostnadsprioritet**: Verdien for dimensjonens kostnadsprioritet angir vekten på denne dimensjonen når den samsvares med oppsettet for kostpriser. Verdien for **Kostnadsprioritet** må være unik på tvers av dimensjoner som **Gjelder kostnad**.
- **Salgsprioritet**: Verdien for dimensjonens salgsprioritet angir vekten på denne dimensjonen når den samsvares med oppsettet for salgspriser eller fakturasatser. Verdien for **Salgsprioritet** må være unik på tvers av dimensjoner som **Gjelder salg**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]