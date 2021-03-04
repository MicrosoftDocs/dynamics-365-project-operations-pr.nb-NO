---
title: Organisasjonsenheter
description: Dette emnet inneholder informasjon om organisasjonsenheter i Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c1c86ce98213fba54fd2b477d4df6f8dc5409d55
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145641"
---
# <a name="organizational-units"></a>Organisasjonsenheter 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

I Dynamics 365 Project Service Automation er en organisasjonsenhet en distinkt gruppe eller divisjon i et profesjonelt tjenestefirma som bruker fakturerbare ressurser som har kostnadssatser.

For profesjonelle tjenesteselskaper som bruker tekniske ressurser i forskjellige øvelsesområder eller forretningslinjer, kan det være at kostnaden ved å fylle en rolle i et øvelsesområde eller en forretningslinje er forskjellig fra kostnaden ved å fylle en rolle i et annet øvelsesområde eller en forretningslinje. Konseptet med organisasjonsenheter bidrar til dette scenariet ved å muliggjøre gruppering av et sett med fakturerbare roller i en divisjon av et selskap som har en atskilt kostnadsstruktur for disse rollene.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Viktige attributter og tilknytninger av organisasjonsenheter

I PSA har en organisasjons enhet en bestemt valuta og bestemte kostprislister.

Valutaen til en organisasjonsenhet er den primære valutaen som brukes til å spore kostnader.

Én eller flere kostprislister kan knyttes til hver organisasjonsenhet. PSA har følgende begrensninger for prislistene som kan knyttes til en organisasjonsenhet:

- Prislister må være i valutaen for organisasjonsenheten
- Prislister må være kostprislister

I tillegg finnes det et attributt for organisasjonsenheten i ressursenheten. Hver ressurs kan tilordnes til én organisasjonsenhet.

## <a name="roles-of-organizational-units"></a>Roller til organisasjonsenheter

Organisasjonsenheten spiller to roller i PSA:

- **Kontraktsenhet** – organisasjonsenheten som representerer firmagruppen eller divisjonen som er primært ansvarlig for å vinne salget og administrere levering av arbeid og tjenester til kunden. Kontraktsenheten identifiseres av feltet **Kontraktsenhet** i overskriftsdelen på sidene **Salgsmulighet**, **Tilbud**, **Prosjektkontrakt** og **Prosjekt**.
- **Ressursenhet** – organisasjonsenheten som en ressurs tilhører eller er tilordnet til. Denne organisasjonsenheten kan levere ressursene for enkelte roller for arbeidsoppgaver (SOWs) og prosjekter som eies av kontraktsenheten.

> ![Kontraktsenheter og ressursenheter](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>Vanlige spørsmål om organisasjonsenheter

Her er noen av de vanligste spørsmålene om organisasjonsenheter:

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Hvordan er organisasjonsenheten i PSA relatert til organisasjonsenheten som allerede finnes i Dynamics 365?

Organisasjonsenheten i Microsoft Dynamics 365 representerer navnet på en global Dynamics 365-forekomst. Dette navnet er vanligvis navnet på den globale virksomheten.

Organisasjonsenheten representerer en gruppe eller divisjon i den globale virksomheten. Denne gruppen eller divisjonen har et sett med roller og en kostprisliste for disse rollene, og disse rollene og prislisten skiller seg fra rollene og prislisten for andre grupper eller divisjoner i virksomheten.

Når PSA er installert, opprettes det en standard organisasjonsenhet basert på organisasjonen. Alle eksisterende ressurser er tilordnet standard organisasjonsenheten. Hvis nye Active Directory-brukere eller -ressurser blir importert til Dynamics 365, tilordner brukerimporten dem til standard organisasjonsenheten i PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Hvordan skiller organisasjonsenheten seg fra forretningsenheten?

I Dynamics 365 er forretningsenheten en sikkerhetskonstruksjon. Tilknytningen til en bruker med en forretningsenhet bestemmer enhetene og enhetsoppføringene som brukeren har tilgang til. Den angir også tillatelsene (opprette, lese, skrive, slette, tilføye, tilføye til, tilordne eller dele) som brukeren har for disse enhetsoppføringene.

Organisasjonsenheten representerer en firmagruppe eller -divisjon som har egne kostnadsrater for ansatte som er tilordnet den. Tilknytningen mellom en ressurs og en organisasjonsenhet bestemmer ressursens kostnad til et prosjektengasjement.

Når du implementerer Dynamics 365, optimaliserer du sikkerhetsgodkjenningen for hierarkiet av forretningsenheter og tilordningen av brukere til forretningsenheter. Tilordne alle brukere som vanligvis må ha tilgang til samme oppføringssett, til samme forretningsenhet. Organisasjonsenheten har ingen innvirkning på sikkerhetsgodkjenning eller -tilgang.

#### <a name="example-of-organizational-units-and-business-units"></a>Eksempel på organisasjonsenheter og forretningsenheter

Ekeli, Ltd. har en fremgangsrik Microsoft-teknologipraksis. Noah og Jenny er begge C\#-utviklere, men Jenny er i USA, mens Noah er i India. De fleste prosjektforhandlinger krever ressurser fra Ekeli India og Ekeli US, og Noah og Jenny trenger samme nivå av sikkerhetstilgang til prosjekter i dette øvelsesområdet. Kostnadene til utviklere fra Ekeli India er imidlertid svært forskjellig fra kostnadene til utviklere fra Ekeli USA.

Her er en optimal måte å utforme for dette scenarioet på ved hjelp av Dynamics 365 og PSA.

1. Opprett Microsoft-teknologipraksisen som en forretningsenhet, og Knytt Noah og Jenny til den. På denne måten bidrar du til å garantere at begge ansatte har samme sikkerhetstilgangsnivå til prosjekter i øvelsesområdet. Begge kan kontrollere fremdrift og rapportere tid, utgifter og aktivitetsoppdateringer. 
2. Opprett to organisasjonsenheter for å garantere for at kostnaden til prosjektet gjenspeiles på riktig måte. 
3. Knytt Jenny til Ekeli US og Noah til Ekeli India.
4. Tilordne aktuelle kostprislister til begge organisasjonsenhetene. På denne måten bidrar du til å sikre at kostnadene som er registrert i prosjektet for Noah og Jenny, nøyaktig gjenspeiler forskjellen i kostnader mellom Ekeli US og Ekeli India.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Er organisasjonsenheter relatert til salgsdistrikter i Dynamics 365?

Det er ingen tilknytning eller relasjon mellom salgsdistrikter og organisasjonsenheter. Et salgsdistrikt er vanligvis et geografisk område der salget skjer. En salgsprisliste kan knyttes til hvert salgsdistrikt.

En organisasjonsenhet er en intern gruppe eller divisjon i firmaet som sporer kostnader for et sett med roller som det selger til andre divisjoner eller for eksterne kunder.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Eksempel på organisasjonsenheter og salgsdistrikter

Ekeli, Ltd. har to utviklingssentre: Ekeli US og Ekeli India. Ressurskostnader er svært forskjellige fra disse to utviklingssentrene.

Ekeli selger sine IT-tjenester i mange internasjonale markeder, for eksempel Latin-Amerika, Nord-Amerika, Asia, Vest-Europa og Midtøsten. Kostnadssatser for de samme prosjektrollene kan variere mye på tvers av disse markedene.

Ekeli US og Ekeli India bør settes opp som organisasjonsenheter, og hver organisasjonsenhet må ha sin egen kostprisliste. Asia – Stillehavs kysten, Latin-Amerika, Nord-Amerika, Vest-Europa og Midtøsten må være definert som salgsdistrikter, og hvert salgsdistrikt bør ha sin egen salgsprisliste.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Hvorfor er det begrensninger på tilknytningen mellom prislister og organisasjonsenheter? 

Salgsprising er vanligvis unikt for geografiske områder eller markeder der tjenester selges. Interne divisjoner av et selskap har vanligvis ikke sine egne salgspriser for samme tjenestetype. Interne divisjoner har imidlertid ulike kostnader for solgte varer (vareforbruk), avhengig av ferdighetene til personene de bruker, og arbeidsbetingelsene i området der de opererer. Fordi organisasjonsenheter er modellert som interne divisjoner av et selskap, kan de bare ha kostprislister.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Hvorfor kan vi ikke knytte salgsprislister til organisasjonsenheter?

I PSA kan salgsprislister knyttes til kunder og salgsdistrikter. Transaksjonsenheter, for eksempel salgsmulighet, tilbud, prosjektkontrakt og prosjekt, bruker salgsprislister som er knyttet til kundekontoen eller salgsdistriktet, for å bestemme betalingssatser og potensiell omsetning i prosjektengasjementet.

Kostprislister knyttes til organisasjonsenheter. Transaksjonsenheter, for eksempel salgsmulighet, tilbud, prosjektkontrakt og prosjekt, bruker kostprislister som er knyttet til kontraktsenheten, til å fastsette kostnader for et prosjektengasjement.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Er organisasjonsenheter hierarkiske i PSA?

Nr. I den nåværende versjonen av PSA er ikke organisasjonsenheter hierarkiske. Dette betyr at du ikke kan gjøre følgende:

- Konfigurere et mønster for standard kostpriser som beveger seg oppover i et hierarki. 
- Rapportere omsetning eller kostnader fremhevet på ulike nivåer i organisasjonsenhetshierarkiet.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Vi er et stort, flernasjonal firma med et komplekst, flernivåhierarki av kostsentre, divisjoner og faktureringskontorer. Hvordan kan vi gjøre best bruk av organisasjonsenhetskonseptet i denne versjonen av Project service-appen?

Når du har et komplekst hierarki av kostsentre, divisjoner, fakturakontorer og så videre, konfigurerer du bladnoder i dette hierarkiet som distinkte organisasjonsenheter.
Følgende eksempel viser et typisk hierarki:

**Ekeli India**

  - SAP-praksis 

    - Tekniske konsulenter 
    - Funksjonelle konsulenter 
    
  - Microsoft-teknologiøvelse 

    - Tekniske konsulenter
    - Funksjonelle konsulenter 
    
**Contoso US**

 - SAP-praksis 

    - Tekniske konsulenter 
    - Funksjonelle konsulenter 
    
 - Microsoft-teknologiøvelse 

    - Tekniske konsulenter 
    - Funksjonelle konsulenter 
 
Hvis hierarkiet er likt, må du konfigurere det som en flat liste, som vist her:
- Ekeli India – SAP-øvelse – tekniske konsulenter 
- Ekeli India – SAP-øvelse – funksjonelle konsulenter       
- Ekeli India – Microsoft-teknologiøvelse – funksjonelle konsulenter 
- Ekeli India – Microsoft-teknologiøvelse – funksjonelle konsulenter 
- Ekeli US – SAP-øvelse – tekniske konsulenter  
- Ekeli US – SAP-øvelse – funksjonelle konsulenter  
- Ekeli US – Microsoft-teknologiøvelse – tekniske konsulenter 
- Ekeli US – Microsoft-teknologiøvelse – funksjonelle konsulenter

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Vi er et lite profesjonelt tjenestefirma som fungerer som bare én divisjon. Hvordan kan vi best bruke organisasjonsenhetskonseptet i den gjeldende versjonen av PSA?

Hvis firmaet fungerer som én enhet som har én kostprisliste, trenger du ikke å konfigurere noen organisasjonsenheter. Under PSA-installasjonen oppretter Dynamics 365 én standard organisasjonsenhet som har samme navn som organisasjonen. Som standard tilordnes alle brukere til denne organisasjonsenheten. Når systemet krever at en organisasjonsenhet velges, velges denne organisasjonsenheten som standard.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Når et prosjekt opprettes fra et tilbud eller en prosjektkontraktslinje, kommer standard kontraktsenhet fra tilbudet eller prosjektkontrakten. Hva er standard kontraktsenheter hvis et prosjekt opprettes før salgsenheter, for eksempel et tilbud eller en prosjektkontrakt?

Når et prosjekt opprettes alene, er standard kontraktsenheten for prosjektet basert på brukeren som oppretter det. Denne brukeren er også standard prosjektleder. Hvis prosjektet er tilordnet en salgsenhet, for eksempel et tilbud eller en prosjektkontrakt, er kontraktsenheten i prosjektet basert på salgsenheten i stedet. I dette tilfellet kan det hende at prosjektestimater beregnes på nytt, fordi kostprislisten brukes til å beregne kostestimatendringer hvis kontraktsenheten endres. Salgsprislisten brukes til å beregne salgsestimatene som vil bli endret, slik at de er synkronisert med prosjektprislisten i tilbudet.

Feltene **Kontraktsenhet** og **Valuta** i prosjektet er låst for redigering fordi de må være synkronisert med verdiene i salgsenheten (tilbud eller prosjektkontrakt) som prosjektet er tilordnet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]