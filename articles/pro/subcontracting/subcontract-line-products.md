---
title: Underkontraktlinjer for produkter
description: Denne artikkelen forklarer hvordan du registrerer underkontraktlinjer for produkter og bruker de ulike feltene til å registrere produktkjøp fra leverandører.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff9636f86102fa671a443d7646614070b3e2ee79
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934378"
---
# <a name="subcontract-lines-for-products"></a>Underkontraktlinjer for produkter

[!include [banner](../../includes/dataverse-preview.md)]

_**Gjelder:** Lite-distribusjon – avtale til proformafakturering_

En underkontrakt i Dynamics 365 Project Operations kan ha en underleverandørlinje for produkter. Disse linjene gjør det mulig for en prosjektleder å kjøpe produkter fra leverandører som de deretter kan bruke på prosjektoppgaver.

Fullfør fremgangsmåten nedenfor for å opprette en underkontraktlinje for produkter i Project Operations.

1. Velg **Underkontrakter** på navigasjonssiden, og åpne underkontrakten du vil arbeide med. 
2. Velg **+ Ny** i fanen **Underkontraktlinjer** for å opprette en ny underkontraktlinje.
3. Velg **Materiale** i **Transaksjonsklasse**-feltet på **Hurtigoppretting**-siden, og angi eller velg den nødvendige feltinformasjonen. 
4. Velg **Lagre**.

Tabellen nedenfor inneholder informasjon om feltene på siden **Detaljer for underkontraktlinje** og **Hurtigoppretting** siden de er relevante for kjøp av produkter.

| Felt | Beskrivelse | Funksjonsinnvirkning|
| ----- | ----------- | ----------- |
| Navn | Navn på underkontraktlinjen for å hjelpe med identifisering. |Dette vises som den første kolonnen i alle oppslag basert på underkontraktlinjer.
| Beskrivelse | En kort beskrivelse av produkter som blir bestilt på underkontraktlinjen. | Ingen |
| Linjetype | Dette feltet har en standardverdi på **antallsbasert**. |Ingen |
| Faktureringsmetode | Dette er en alternativsett som representerer de to hovedkontraktsmodellene som støttes av Project Operations: **Fast pris** og **Tid og materiell**. | Basert på faktureringsmetoden som er valgt, gjøres en milepælbasert fakturaplan tilgjengelig for underkontraktslinjer med faktureringsmetoden Fast pris. |
| Transaksjonsklasse |Dette feltet har en standardverdi på **tid**. Hvis du vil opprette underkontraktlinjer for innkjøp av produkter, angir du **Material** i **Transaksjonsklasse**-feltet.  | Dette angir at underkontraktlinjen brukes til å registrere kjøp av produkter som skal brukes på prosjekter. |
| Velg produkt | Velg om produktet som kjøpes, vedlikeholdes i produktkatalogen eller er et produkt som ikke er i produktkatalogen. |Ingen |
| Produkt | Velg et aktivt produkt fra katalogen. Dette feltet er bare tilgjengelig når **Velg produkt** er satt til **Eksisterende**. |Kombinasjonen av **Produkt** og **Enhet** brukes som standard eller beregnet for enhetsprisen for underkontraktslinjen.
| Ikke i produktkatalog | Angi navnet på produktet ikke i produktkatalogen. Dette feltet er bare tilgjengelig når **Velg produkt** er satt til **Ikke i produktkatalog**.  |Innkjøpspris fylles ikke automatisk ut for produkter i produktkatalogen.|
| Ønsket leveringsdato | Angi ønsket leveringsdato for produktene.| Denne datoen brukes også til å velge en prosjektprisliste fra prosjektprislistene som er vedlagt underkontrakten. Kostnaden for produktet på underkontraktlinjen brukes deretter som standard fra den prislisten. |
| Avtalt leveringsdato | Angi datoen da produktene blir kontraktsmessig godtatt om å bli levert.  |Ingen|
| Antall bestilt | Angi antall produkter som kjøpes fra leverandøren.| Denne brukes til å vise advarsler når en prosjektleder overtrekker fra dette antallet.|
| Enhetsgruppe | Denne verdien brukes bare for katalogprodukter. |Når både **Produkt** og **Ønsket leveringsdato** er valgt, velger systemet den aktuelle prislisten basert på leveringsdatoen. De relaterte prislisteelementene spørres om det samsvarende produktet. Verdiene for enhet og enhetsgruppe er standardverdier fra oppsettet i prislisteelementoppføringen. |
| Enhet | Denne verdien settes som standard til enheten som er angitt i prislisteelementoppføringen. Du kan endre dette til en annen enhet etter behov.| Kombinasjonen av produkt og enhet brukes som standardverdi for enhetsprisen på underkontraktlinjen for eksisterende katalogprodukter. |
| Enhetspris | Enhetsprisen er standard ved å bruke kombinasjonen av produkt og enhet fra prislisteelementene knyttet til prosjektprislisten som gjelder for ønsket leveringsdato for underkontraktlinjen.  |Ingen |
| Delsum | Dette skrivebeskyttede feltet beregnes som Antall x Enhetspris hvis begge feltene har angitt verdier. Hvis feltet **Antall**, **Enhetspris** eller begge er tomme, kan du angi en verdi manuelt.  |Ingen |
| Merverdiavgift | Angi mva-verdien. |Ingen |
| Totalbeløp | Dette beregnede feltet viser totalbeløpet for underkontraktlinjen etter inkluderte avgifter. Verdien i dette feltet beregnes som delsum + avgift. |Ingen |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
