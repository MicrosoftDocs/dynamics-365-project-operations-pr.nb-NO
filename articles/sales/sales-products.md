---
title: Produkter
description: Dette emnet gir informasjon om produktkatalogen som du kan bruke til å gi informasjon til kunder om produktene og prisen organisasjonen din tilbyr.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121275"
---
# <a name="products"></a>Produkter

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

Produktene er ryggraden i bedriften din. Produktkatalogen i Dynamics 365 Sales Professional er en samling av produkter og prisinformasjonen deres. Gjør det enklere for selgerne å øke salget ved å opprette en produktkatalog raskt.

## <a name="add-a-product"></a>Legge til et produkt

1.  Kontroller at du har en rolle som salgsleder eller systemansvarlig, slik at du kan legge til produkter i Dynamics 365 Sales Professional.
2.  I områdekartet under **Oppsett** velger du **Produkter**.
3.  Velg **Legg til produkt**, og fyll ut følgende informasjon:

    -  **Navn**
    -  **Produkt-ID**
    -  **Overordnet**: Velg en overordnet produktfamilie for produktet. Hvis du oppretter et underordnet produkt i en produktfamilie, fylles navnet på overordnet produktfamilie ut her. Dette kan ikke endres etter at oppføringen er lagret.
    -  **Gyldig fra**/**Gyldig til**: Definer perioden produktet er gyldig, ved å velge en **Gyldig fra**- og **Gyldig til**-dato.
    -  **Enhetsgruppe**: Velg en enhetsgruppe. En enhetsgruppe er en samling av ulike enheter som et produkt selges i, og definerer hvordan enkeltelementer grupperes i større mengder. Hvis du for eksempel legger til frø som et produkt, har du kanskje opprettet en enhetsgruppe kalt "Frø" og definert primærenheten som "pakke".
    -  **Standardenhet**: Velg den vanligste enheten som produktet skal selges i. Enhetene er antall eller mål som du selger produktene dine i. Hvis du legger til frø som et produkt, kan du for eksempel selge dem i pakker, esker eller paller. Hver av disse blir en produktenhet. Hvis frø for det meste selges i pakker, velger du dette som enheten.
    -  **Standard prisliste**: Hvis dette er et nytt produkt, er dette feltet skrivebeskyttet. Hvis du vil velge en standard prisliste, må du først fylle ut alle obligatoriske felt og deretter lagre oppføringen. Selv om det ikke er obligatorisk, bør du angi en standard prisliste for hvert produkt når du har lagret produktoppføringen. Da kan standard prisliste brukes i Sales for å generere tilbud, ordrer og fakturaer for kundeoppføringer som ikke inneholder en prisliste.
    -  **Støttede desimaler**: Angi et helt tall mellom 0 og 5. Hvis produktet ikke kan deles inn i delverdier, skriver du 0. Presisjonen for **Antall**-feltet i tilbuds-, ordre- eller fakturaproduktoppføringen, valideres mot verdien i dette feltet hvis det ikke er knyttet en prisliste til produktet.
    -  **Emne**: Knytt dette produktet til et emne. Du kan bruke emner til å kategorisere produkter og filtrere rapporter.

4.  Velg **Lagre**.
5.  Gå til kategorien **Flere detaljer**. I delen **Prislisteelementer** velger du **Flere kommandoer**, og deretter velger du **Legg til nytt prislisteelement**.
7.  Gå til kategorien **Flere detaljer**. I delen **Produktrelasjon** velger du **Flere kommandoer**-ikonet, og deretter velger du **Legg til ny produktrelasjon.**
8.  I **Ny produktrelasjon**-skjemaet angir du følgende informasjon, og på kommandolinjen velger du **Lagre og lukk**:

    -   **Relatert produkt**: Velg et produkt du vil legge til som et produkt som er relatert til den eksisterende produktoppføringen du arbeider på.
    -   **Salgsrelasjonstype**: Velg om du vil legge til produktet som et oppsalg, kryssalg, tilbehør eller erstatningsprodukt.
    -   **Retning**: Velg om relasjonen mellom produktene skal være enveis eller toveis. Når du velger enveis, vises produktet du velger i **Relatert produkt**, som en anbefaling for det eksisterende produktet, men ikke omvendt.

9.  Velg **Lagre** i produktskjemaet.

## <a name="import-products"></a>Importere produkter

Du kan bruke importmaler til å hente inn data om mange produkter i Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revidere et produkt

Hold produktbeholdningen oppdatert ved raskt å revidere egenskapene for produktene etter behov og publisere informasjonen på nytt, slik at selgerne kan se de siste endringene i beholdningen.

1.  Sørg for at du er tilordnet en av følgende sikkerhetsroller eller har tilsvarende tillatelser: systemadministrator, systemtilpasser, salgsleder, viseadministrerende direktør for salg, viseadministrerende direktør for markedsføring eller administrerende direktør.
2.  Velg **Produkter** i områdekartet.
3.  Åpne aktive produkter du vil endre, og velg **Revider** på kommandolinjen.
4.  I dialogboksen **Bekreft revidering** velger du **Bekreft**. Dermed endres produktstatusen til **Under revisjon**.
5.  Når du er ferdig med å gjøre endringer, velger du **Publiser** på kommandolinjen.

    > [!TIP]
    > Hvis du vil tilbakestille endringene og fortsette med den siste aktive versjonen av produktet, velger du **Gjenopprett**. Dermed endres statusen for produktet tilbake til **Aktiv**.

## <a name="clone-a-product"></a>Klone et produkt 

Når du oppretter nye produkter, kan du spare tid ved å klone en eksisterende forekomst. Da opprettes en kopi av den opprinnelige oppføringen med alle detaljene unntatt navn og ID.

1.  Sørg for at du er tilordnet en av følgende sikkerhetsroller eller har tilsvarende tillatelser: systemadministrator, systemtilpasser, salgsleder, viseadministrerende direktør for salg, viseadministrerende direktør for markedsføring eller administrerende direktør.
2.  Velg **Produkter** i områdekartet.
3.  Velg en produktoppføring som du vil klone, og velg **Klon** på kommandolinjen. En bekreftelsesdialogboks vises.
4.  Velg **Bekreft**.

En ny produktoppføring åpnes med samme informasjon som den opprinnelige bortsett fra navn og ID.

## <a name="retire-a-product"></a>Trekke tilbake et produkt 

Hvis organisasjonen ikke lenger selger et produkt, må du fjerne det slik at produktet er ikke lenger tilgjengelig for selgerne.

1.  Sørg for at du har en rolle som systemansvarlig eller Sales Professional-leder eller tilsvarende tillatelser.
2.  Velg **Produkter** i områdekartet.
3.  Åpne aktive produkter du vil trekke tilbake, og velg **Trekk tilbake** på kommandolinjen.
4.  I dialogboksen **Bekreft tilbaketrekking** velger du **Bekreft**.


## <a name="delete-a-product"></a>Slette et produkt

Hvis du vil slutte å selge et produkt, sletter du det.

> [!IMPORTANT]
> Du kan ikke gjenopprette en slettet oppføring.

1.  Sørg for at du har en rolle som systemansvarlig eller Sales Professional-leder eller tilsvarende tillatelser.
2.  Velg **Produkter** i områdekartet.
3.  Velg en produktoppføring som du vil slette, og velg **Slett** på kommandolinjen.
4.  Velg **Fortsett** i dialogboksen **Bekreft sletting**.
 
 ## <a name="quantity-factors-for-products"></a>Antallsfaktorer for produkter

Antallsfaktorer støtter salg av abonnementsbaserte produkter. Når det gjelder abonnementsbaserte produkter, uttrykkes antallet på tilbuds- eller prosjektkontraktlinjen som antall brukermåneder.

Vanligvis lagres prisen på abonnementsprogramvaren i katalogen som prisen per bruker per måned. Du kan imidlertid bruke andre tidsbeskrivelser i stedet. I løpet av salgsprosessen er prisen på tilbudslinjen vanligvis prisen per bruker per måned som ble forhandlet og diskontert av IT-salgsrepresentanten. Hver avtale har et forskjellig antall brukere og et forskjellig antall abonnementsmåneder. Antallet som brukes til å beregne beløpet for tilbudslinjen, er et produkt av antall brukere og antall abonnementsmåneder.

Antallsfaktorer er avhengig av produktattributter. Når du konfigurerer bestemte egenskaper for et produkt, kan du flagge et delsett av disse egenskapene, eller alle egenskapene, som antall faktorer.

Systemet validerer at bare numeriske egenskaper eller produktegenskaper som har numeriske datatyper, blir flagget som antallsfaktorer. Når et produkt som antallsfaktorer er konfigurert for, blir lagt til på en tilbudslinje, blir **Antall**-feltet på tilbuds linjen et skrivebeskyttet felt. Etter at du har angitt verdier for produktegenskaper som er antallsfaktorer, beregnes antallet på tilbudslinjen.

Hvis det for eksempel finnes følgende egenskaper: 

- **Antall brukere**: Antall brukere 
- **Antall måneder**: Antall abonnementsmåneder
- **Produkt-SKU** 

Egenskapene **Antall brukere** og **Antall måneder** kan flagges som antallsfaktorer ved å redigere egenskapene for produktlinjen. 
