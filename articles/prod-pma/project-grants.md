---
title: Prosjektstøtte
description: Dette emnet forklarer hvordan du oppretter eller endrer et tilskudd.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081801"
---
# <a name="project-grants"></a>Prosjektstøtte

[!include [banner](../includes/banner.md)]

Et tilskudd er en pengegave for et bestemt formål eller prosjekt. Det finnes vanligvis begrensninger for hvordan et tilskudd kan brukes. I Prosjektstyring og regnskap kan du angi og spore tilskudd og definere relasjoner til prosjekter og prosjektkontrakter. Du kan for eksempel utføre følgende oppgaver:

- Du kan knytte tilskudd til prosjekter og finansieringskilder via koblinger til sidene **Prosjekt** og **Prosjektkontraktdetaljer**.
- Angi og spore endringer i et tilskudd når det går fra én status til en annen.
- Angi og spore kostnader, ønskede beløp og tildelte beløp.
- Opprett hovedtilskudd, og knytt undertilskudd til dem.

Du kan opprette et tilskudd ved å angi alle detaljene i en ny oppføring, eller du kan kopiere detaljene fra et eksisterende tilskudd og deretter oppdatere dem.

## <a name="create-a-new-grant"></a>Opprett et nytt tilskudd

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg **Nytt** \> **Tilskudd**.
3. På siden med tilskuddsdetaljer, på hurtigfanen **Generelt** , i feltet **Tilskudds-ID** , angir du en alfanumerisk identifikator for tilskuddet.
4. Skriv inn et navn på tilskuddet i feltet **Navn på tilskudd**.
5. I **Beskrivelse** -feltet legger du til detaljer om det nye tilskuddet.

    De fleste av de andre feltene på siden er valgfrie, og du kan angi så lite eller så mye informasjon som du ønsker.

    Følgende liste beskriver informasjonen som er angitt på hver hurtigfane på siden med tilskuddsdetaljer:

    - **Generelt** – Angi navnet på tilskuddet, status, beskrivelse, formål og beløp.
    - **Kontaktinformasjon** – Angi detaljer om ansatte, avdelingen som håndterer tilskuddet, og tilskuddskunden eller organisasjonskilden for tilskuddet. Du kan også angi om organisasjonen er et mellomledd som mottar tilskuddet og deretter sender det til en annen mottaker. Velg **Legg til** for å legge til kontaktinformasjon, for eksempel telefonnumre og e-postadresser, for organisasjonen som gir tilskuddet.
    - **Datoer og tidsfrister** – Angi datoer som er relatert til tilskuddet og tilskuddsprogrammet. Eksempler inkluderer søknadens forfallsdato, sendedatoen og datoen for når tilskuddet er godkjent eller avvist.
    - **Tilknyttede prosjekter og prosjektkontrakter** – Du kan angi informasjon på denne hurtigfanen bare hvis **Tilskuddsstatus** -feltet på hurtigfanen **Generelt** er angitt til **Aktiv** eller **Tildelt**. Velg blant følgende alternativer for å fullføre den relaterte oppgaven:

        - **Legg til finansieringskilde** – Legg til en ny finansieringskilde for tilskuddet. Du kan skrive inn alle detaljene nå, eller du kan bruke standardinformasjonen og deretter oppdatere den senere.
        - **Legg til prosjektkontrakt** – Legg til eller oppdater informasjon om prosjektkontrakten.
        - **Legg til prosjekt** – Legg til eller oppdater prosjektdetaljer.

    - **Oppsett** – Angi detaljer om matchende midler hvis denne informasjonen er nødvendig. Mange organisasjoner som tildeler tilskudd, krever at mottakerne bruker et bestemt beløp av sine egne penger eller ressurser, slik at de matcher beløpet som er tildelt tilskuddet. I feltet **Lokalt prosjekt eller sporings-ID** kan du angi en identifikator som er forskjellig fra prosjektidentifikatoren.

        > [!NOTE]
        > Hvis en del av tilskuddet skal tildeles en annen organisasjon, setter du alternativet **Underordnet tilskuddsgiver** til **Ja**. For tilskudd som tildeles i USA, kan du angi om et tilskudd skal tildeles under et delstatsmandat eller et føderalt mandat.

    - **Nedtegningsdetaljer** – Legg til eller oppdater informasjon om hvor ofte tilskuddsmidler kan trekkes tilbake, faktureres eller brukes.

## <a name="create-a-new-grant-from-a-copy"></a>Opprette et nytt tilskudd fra en kopi

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg **Ny** \> **Kopier fra tilskudd**.
3. Angi en alfanumerisk identifikator og et navn for det nye tilskuddet, og velg deretter **OK**.
4. Gå gjennom detaljene for det kopierte tilskuddet på siden med tilskuddsdetaljer, og gjør de nødvendige endringene. De fleste feltene på siden er valgfrie.

## <a name="view-or-modify-grant-details"></a>Vise eller endre tilskuddsdetaljer

1. Gå til **Prosjektstyring og regnskap** \> **Tilskudd** \> **Tilskudd**.
2. Velg tilskuddet du vil endre.
3. I handlingsruten i kategorien **Tilskudd** i gruppen **Vedlikehold** velger du **Rediger**.
4. Se gjennom tilskuddsdetaljene, og gjør de nødvendige endringene.
