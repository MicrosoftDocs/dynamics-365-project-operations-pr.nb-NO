---
title: Hvordan tilpasser jeg forretningsprosessflyten for prosjektfaser?
description: En oversikt over hvordan du tilpasser forretningsprosessflyten for prosjektfaser.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 2e6c60fe67aea908013077bde40c2faeabc2f39e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993158"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="5845a-103">Hvordan tilpasser jeg forretningsprosessflyten for prosjektfaser?</span><span class="sxs-lookup"><span data-stu-id="5845a-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="5845a-104">Det er en kjent begrensning i tidligere versjoner av programmet Project Service at navnene på fasene i forretningsprosessflyten for prosjektfaser må samsvare nøyaktig med de forventede engelske navnene (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="5845a-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="5845a-105">Ellers vil ikke forretningslogikken som er avhengig av de engelske fasenavnene, fungere som forventet.</span><span class="sxs-lookup"><span data-stu-id="5845a-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="5845a-106">Det er derfor du ikke ser kjente handlinger som for eksempel **Bytt prosess** eller **Rediger prosess** tilgjengelig på prosjektskjemaet, og det oppfordres ikke til tilpassing av forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="5845a-107">Denne begrensningen er håndtert i versjon 2.4.5.48 og senere.</span><span class="sxs-lookup"><span data-stu-id="5845a-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="5845a-108">Denne artikkelen inneholder foreslåtte løsninger hvis du ønsker å tilpasse standard forretningsprosessflyt for tidligere versjoner.</span><span class="sxs-lookup"><span data-stu-id="5845a-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="5845a-109">Forretningslogikk krever nøyaktig samsvar med engelske fasenavn</span><span class="sxs-lookup"><span data-stu-id="5845a-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="5845a-110">Forretningsprosessflyten for prosjektfaser inneholder forretningslogikk som bidrar til følgende virkemåter i appen:</span><span class="sxs-lookup"><span data-stu-id="5845a-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="5845a-111">Når prosjektet er knyttet til et tilbud, setter koden forretningsprosessflyten til **Quote**-fasen.</span><span class="sxs-lookup"><span data-stu-id="5845a-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="5845a-112">Når prosjektet er knyttet til en kontrakt, setter koden forretningsprosessflyten til **Plan**-fasen.</span><span class="sxs-lookup"><span data-stu-id="5845a-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="5845a-113">Når forretningsprosessflyten er gått videre til **Close**-fasen, deaktiveres prosjektoppføringen.</span><span class="sxs-lookup"><span data-stu-id="5845a-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="5845a-114">Når prosjektet er deaktivert, settes prosjektskjemaet og arbeidsnedbrytningsstrukturen (WBS) til skrivebeskyttet, de navngitte ressursbestillingene lanseres, og eventuelle tilknyttede prislister deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="5845a-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="5845a-115">Denne forretningslogikken er avhengig av de engelske navnene på prosjektfasene.</span><span class="sxs-lookup"><span data-stu-id="5845a-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="5845a-116">Denne avhengigheten av de engelske fasenavnene er hovedårsaken til at det ikke oppfordres til å tilpasse forretningsprosessflyten for prosjektfaser, og hvorfor du ikke ser vanlige forretningsprosessflythandlinger som **Bytt prosess** eller **Rediger prosess** i prosjektenheten.</span><span class="sxs-lookup"><span data-stu-id="5845a-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="5845a-117">Hva skjer hvis fasenavnene ikke samsvarer med de engelske navnene?</span><span class="sxs-lookup"><span data-stu-id="5845a-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="5845a-118">Når fasenavnene i forretningsprosessflyten ikke samsvarer nøyaktig med de engelske fasenavnene, i Project Service-appen versjon 1.x på 8.2-plattformen, blir forretningslogikken som angir riktig fase for tilbud eller kontrakter eller som lukker prosjektet, hoppet over.</span><span class="sxs-lookup"><span data-stu-id="5845a-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="5845a-119">Ingen feilmelding vises.</span><span class="sxs-lookup"><span data-stu-id="5845a-119">No error messages are displayed.</span></span> <span data-ttu-id="5845a-120">Det virker derfor som at du kan tilpasse forretningsprosessflyten for prosjektfaser.</span><span class="sxs-lookup"><span data-stu-id="5845a-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="5845a-121">Du kan imidlertid ikke se noen av de automatiske prosessene som jobber for tilbud, kontrakter, og prosjektlukking.</span><span class="sxs-lookup"><span data-stu-id="5845a-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="5845a-122">I Project Service-appen versjon 2.4.4.30 eller tidligere på 9.0-plattformen var det en betydelig arkitektonisk endring i forretningsprosessflyter som krevde en omskriving av forretningslogikken til forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="5845a-123">Hvis prosessfasenavnene ikke samsvarer med de forventede engelske navnene, får du derfor en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="5845a-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="5845a-124">Hvis du vil tilpasse forretningsprosessflyten for prosjektfaser for prosjektenheten, kan du altså bare legge til helt nye faser i standard forretningsprosessflyt for prosjektenheten mens du beholder fasene **Quote**, **Plan** og **Close** som de er.</span><span class="sxs-lookup"><span data-stu-id="5845a-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="5845a-125">Denne begrensningen sikrer at du ikke får feil fra forretningslogikken som forventer engelske fasenavn i forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="5845a-126">I versjon 2.4.5.48 eller nyere er forretningslogikken som er beskrevet i denne artikkelen, fjernet fra standard forretningsprosessflyt for prosjektenheten.</span><span class="sxs-lookup"><span data-stu-id="5845a-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="5845a-127">Hvis du oppgraderer til denne versjonen eller senere, kan du tilpasse eller erstatte standard forretningsprosessflyt med din egen.</span><span class="sxs-lookup"><span data-stu-id="5845a-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="5845a-128">Løsninger for tidligere versjoner</span><span class="sxs-lookup"><span data-stu-id="5845a-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="5845a-129">Hvis oppgradering ikke er noe alternativ, kan du tilpasse forretningsprosessflyten for prosjektfaser for prosjektenheten på en av disse to måtene:</span><span class="sxs-lookup"><span data-stu-id="5845a-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="5845a-130">Legg til flere faser i standardkonfigurasjonen samtidig som du beholder de engelske fasenavnene for **Quote**, **Plan** og **Close**.</span><span class="sxs-lookup"><span data-stu-id="5845a-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Skjermbilde av å legge til faser i standardkonfigurasjon](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="5845a-132">Opprett din egen forretningsprosessflyt og gjør den til den primære forretningsprosessflyten for prosjektenheten, som lar deg ha de fasenavnene du ønsker.</span><span class="sxs-lookup"><span data-stu-id="5845a-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="5845a-133">Hvis du imidlertid vil bruke de samme standardprosjektfasene **Quote**, **Plan** og **Close**, må du utføre noen tilpassinger som er basert på de egendefinert fasenavnene.</span><span class="sxs-lookup"><span data-stu-id="5845a-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="5845a-134">Den mer komplekse logikken er i lukkingen av prosjektet, som du fremdeles kan utløse ved å bare deaktivere prosjektoppføringen.</span><span class="sxs-lookup"><span data-stu-id="5845a-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF-tilpassing](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="5845a-136">Andre hensyn for Project Service-appen versjon 2.4.4.30 eller tidligere på plattform 9.0</span><span class="sxs-lookup"><span data-stu-id="5845a-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="5845a-137">I Project Service 2.4.4.30 eller tidligere på plattform 9.0 med en egendefinert forretningsprosessflyt brukes **Fasenavn**-feltet på prosjektenheten i **Prosjekt etter fase**-diagrammet, og prosjektlistevisninger oppdateres ikke fordi det er koblet til standard forretningsprosessflyten for prosjektfaser.</span><span class="sxs-lookup"><span data-stu-id="5845a-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="5845a-138">Du kan løse dette problemet med følgende trinn:</span><span class="sxs-lookup"><span data-stu-id="5845a-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="5845a-139">Legg til et egendefinert felt for å fange opp gjeldende forretningsprosessflyttrinn som oppdateres når brukeren går gjennom den egendefinerte forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="5845a-140">Endre **Prosjekt etter fase**-diagrammet slik at det fungerer med det egendefinerte feltet i stedet for standardkonfigurasjonen.</span><span class="sxs-lookup"><span data-stu-id="5845a-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="5845a-141">Trinn for å opprette din egen forretningsprosessflyt for prosjektenheten</span><span class="sxs-lookup"><span data-stu-id="5845a-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="5845a-142">Slik oppretter du din egen forretningsprosessflyt for prosjektenheten:</span><span class="sxs-lookup"><span data-stu-id="5845a-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="5845a-143">Gå til **Innstillinger** > **Prosessenter**.</span><span class="sxs-lookup"><span data-stu-id="5845a-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="5845a-144">Ikke kopier forretningsprosessflyten for prosjektfaser fordi dette kopierer også forretningslogikken for Project Service.</span><span class="sxs-lookup"><span data-stu-id="5845a-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Opprett prosess](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="5845a-146">Bruk prosessdesigneren til å opprette de fasenavnene du vil ha.</span><span class="sxs-lookup"><span data-stu-id="5845a-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="5845a-147">Hvis du vil ha samme funksjonalitet som standardfasene for **Tilbud**, **Planlegg** og **Lukk**, må du opprette dette basert på fasenavnene i den egendefinerte forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Skjermbilde av prosessdesigner som brukes til å tilpasse BPF](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="5845a-149">I prosessdesigneren klikker du på **Ordreprosessflyt** for å gjøre den egendefinerte forretningsprosessflyten til den primære forretningsprosessflyten for prosjektenheten, ved å flytte den over forretningsprosessflyten for prosjektfaser til øverst i listen.</span><span class="sxs-lookup"><span data-stu-id="5845a-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="5845a-150">Skjermbilde av bruk av ordreprosessflyt</span><span class="sxs-lookup"><span data-stu-id="5845a-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="5845a-151">Fremgangsmåten nedenfor bruker Project Service-appen 2.4.4.30 eller tidligere på 9.0-plattform</span><span class="sxs-lookup"><span data-stu-id="5845a-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="5845a-152">Legg til et nytt egendefinert felt i prosjektenheten for å registrere de egendefinerte fasene i den egendefinerte forretningsprosessflyten.</span><span class="sxs-lookup"><span data-stu-id="5845a-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="5845a-153">Du må legge til forretningslogikk (plugin/arbeidsflyt) for å oppdatere dette feltet når fasen i den egendefinerte forretningsprosessflyten oppdateres.</span><span class="sxs-lookup"><span data-stu-id="5845a-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Skjermbilde av tilpassing av prosjektenhet](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="5845a-155">Endre **Prosjekt etter fase**-diagrammet slik at det bruker det nye egendefinerte feltet for faser.</span><span class="sxs-lookup"><span data-stu-id="5845a-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Skjermbilde av bruk av diagrammet Prosjekt etter fase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="5845a-157">Endre eventuelle visninger for prosjektenheten for å ta med det nye egendefinerte feltet for faser.</span><span class="sxs-lookup"><span data-stu-id="5845a-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Skjermbilde av endring av visninger i prosjektenheten](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]