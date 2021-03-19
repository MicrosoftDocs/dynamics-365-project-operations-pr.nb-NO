---
title: Valuta
description: Dette emnet gir informasjon om hvordan du legger til og fjerner valutatyper i Project Operations.
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
ms.openlocfilehash: 7368dc5d4901e8083f15b0174b7cc58a6b6dbd91
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277485"
---
# <a name="currency"></a>Valuta

_**Gjelder for:** Project Operations for ressursbaserte/ikke-lagerbaserte scenarioer, Lite-distribusjon – avtale til proformafakturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Valutaer bestemmer prisen på produktene i produktkatalogen og kostnaden for transaksjoner, for eksempel salgsordrer. Hvis kundene dine er spredt over ulike områder, kan du legge til valutaene deres for å behandle transaksjonene. Legg til valutaene som er mest aktuelle for dine gjeldende og fremtidige forretningsbehov.  

> [!NOTE]
> Hvis miljøet er et Common Data Service-miljø, er du i Power Platform -administrasjonssenteret, og du velger siden **Valutaer** (**Miljøer** > [velg miljø] > **Innstillinger** > **Virksomhet** > **Valutaer**), vil siden være tom. Dette skyldes at angivelse av en valuta ikke støttes i Common Data Service-miljøer.

## <a name="add-a-currency"></a>Legge til en valuta  
Før du starter denne prosedyren, må du kontrollere at sikkerhetsrollen inneholder tillatelser for systemadministrator. 

1. Velg et miljø i administrasjonssenteret for Power Platform. 
2. Velg **Innstillinger** > **Forretning**.
3. Velg **Valutater**.  
4. Velg **Ny**.  
5. Fyll inn informasjonen etter behov.  


   |          Felt          |                                                                                                                                                                                                                                                                                                                                                                            Beskrivelse                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Valutatype**    | - **System** – Velg dette alternativet hvis du vil bruke valutaene som er tilgjengelige i modelldrevne apper i Dynamics 365. Velg **Oppslag** for å søke etter en valuta. Når du velger en valutakode, legges **valutanavnet** og **valutasymbolet** automatisk til for den valgte valutaen.<br />- **Egendefinert** – Velg dette alternativet hvis du vil legge til en valuta som ikke er tilgjengelig i modelldrevne apper i Dynamics 365. I dette tilfellet må du angi verdier manuelt for **Valutakode**, **Valutapresisjon**, **Valutanavn**, **Valutasymbol** og **Valutaomregning**. |
   |    **Valutakode**    |                                                                                                                                                                                                                                                                                                                                            Kortform for valutaen. Eksempel: **USD** for amerikanske dollar.                                                                                                                                                                                                                                                                                                                                            |
   | **Valutapresisjon**  |                                                                                                                                                                                  Skriv inn antall desimaler du vil bruke for valutaen.  Du kan legge til en verdi mellom 0 og 4. **Obs!**  Hvis du har angitt en presisjonsverdi i **Systeminnstillinger**-dialogboksen, vises denne verdien her.                                                                                                                                                                                  |
   |    **Valutanavn**    |                                                                                                                                                                                                                                         Hvis du valgte en valutakode fra listen over tilgjengelige valutaer i modelldrevne apper i Dynamics 365, vises valutanavnet for den valgte koden her. Hvis du valgte **Egendefinert** som valutatype, skriver du inn navnet på valutaen.                                                                                                                                                                                                                                          |
   |   **Valutasymbol**   |                                                                                                                                                                                                                                                                      Hvis du valgte en valutakode fra listen over tilgjengelige valutaer, vises symbolet for den valgte valutaen her. Hvis du valgte **Egendefinert** som valutatype, skriver du inn symbolet for den nye valutaen.                                                                                                                                                                                                                                                                       |
   | **Valutakonvertering** |                                                                                                                                                                                                                                     Skriv inn verdien for den valgte valutaen i henhold til én amerikansk dollar. Dette er beløpet som brukes ved konvertering av den valgte valutaen til standardvalutaen. **Viktig!**  Pass på at du oppdaterer denne verdien så ofte som nødvendig for å unngå eventuelle unøyaktige beregninger i transaksjonene.                                                                                                                                                                                                                                      |


6. Når du er ferdig, kan du velge **Lagre** eller **Lagre og Lukk** på kommandolinjen.  

   > [!TIP]
   >  Hvis du vil redigere en valuta, klikker du valutaen og angir eller velger deretter de nye verdiene.  

## <a name="delete-a-currency"></a>Slette en valuta  

1. Velg et miljø i administrasjonssenteret for Power Platform. 
2. Velg **Innstillinger** > **Forretning**.
3. Velg **Valutater**.  
4. Velg valutaen som skal slettes, fra listen over valutaer som vises.  
5. Velg **Slett**.  
6. Bekreft slettingen.  

> [!IMPORTANT]
>  Du kan ikke slette valutaer som brukes av andre oppføringer. Du kan bare deaktivere dem. Du fjerner ikke valutainformasjonen som er lagret i eksisterende oppføringer, for eksempel salgsmuligheter eller ordrer, ved å deaktivere valutaoppføringene. Du vil imidlertid ikke kunne velge den deaktiverte valutaen for nye transaksjoner.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]