---
title: Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android
description: Dette emnet inneholder vanlige mønstre for bruk av utvidelser for å implementere egendefinerte felt.
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
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
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 5dae571fce746b49281587f5349774a7f2c4111b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271005"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="a1d34-103">Implementere egendefinerte felt for Microsoft Dynamics 365 Project Timesheet-mobilappen på iOS og Android</span><span class="sxs-lookup"><span data-stu-id="a1d34-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1d34-104">Dette emnet inneholder vanlige mønstre for bruk av utvidelser for å implementere egendefinerte felt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="a1d34-105">Følgende emner omhandles:</span><span class="sxs-lookup"><span data-stu-id="a1d34-105">The following topics are covered:</span></span>

- <span data-ttu-id="a1d34-106">De forskjellige datatypene som det egendefinerte feltrammeverket støtter</span><span class="sxs-lookup"><span data-stu-id="a1d34-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="a1d34-107">Slik viser du skrivebeskyttede eller redigerbare felt i timeregistreringsoppføringer og lagrer brukerangitte verdier tilbake til databasen</span><span class="sxs-lookup"><span data-stu-id="a1d34-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="a1d34-108">Slik viser du skrivebeskyttede felt i timeregistreringshodet</span><span class="sxs-lookup"><span data-stu-id="a1d34-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="a1d34-109">Slik integrerer du andre egendefinerte forretningslogikker for å angi standardverdier i felt og utføre ytterligere validering</span><span class="sxs-lookup"><span data-stu-id="a1d34-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="a1d34-110">Målgruppe</span><span class="sxs-lookup"><span data-stu-id="a1d34-110">Audience</span></span>

<span data-ttu-id="a1d34-111">Dette emnet er ment for utviklere som integrerer sine egendefinerte felt i Microsoft Dynamics 365 Project Timesheet-mobilappen som er tilgjengelig for Apple iOS og Google Android.</span><span class="sxs-lookup"><span data-stu-id="a1d34-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="a1d34-112">Det forutsettes er at lesere er kjent med funksjonene for X++-utvikling og funksjonene for prosjekttimeregistrering.</span><span class="sxs-lookup"><span data-stu-id="a1d34-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="a1d34-113">Datakontrakt – klassen TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="a1d34-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="a1d34-114">**TSTimesheetCustomField**-klassen er X++-datakontraktklassen som representerer informasjon om et egendefinert felt for timeregistreringsfunksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="a1d34-115">Det blir sendt lister over de egendefinerte feltobjektene både for TSTimesheetDetails-datakontrakten og TSTimesheetEntry-datakontrakten for å vise egendefinerte felt i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="a1d34-116">**TSTimesheetDetails** – Kontrakten for timeregistreringshodet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="a1d34-117">**TSTimesheetEntry** – Kontrakten for timeregistreringstransaksjonen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="a1d34-118">Grupper av disse objektene som har samme prosjektinformasjon og **timesheetLineRecId**-verdi, utgjør en linje.</span><span class="sxs-lookup"><span data-stu-id="a1d34-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="a1d34-119">fieldBaseType (typer)</span><span class="sxs-lookup"><span data-stu-id="a1d34-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="a1d34-120">Egenskapen **FieldBaseType** i **TsTimesheetCustom**-objektet bestemmer typen av feltet som vises i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="a1d34-121">Følgende **Typer**-verdier som støttes.</span><span class="sxs-lookup"><span data-stu-id="a1d34-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="a1d34-122">Typer-verdi</span><span class="sxs-lookup"><span data-stu-id="a1d34-122">Types value</span></span> | <span data-ttu-id="a1d34-123">Type</span><span class="sxs-lookup"><span data-stu-id="a1d34-123">Type</span></span>              | <span data-ttu-id="a1d34-124">Notater</span><span class="sxs-lookup"><span data-stu-id="a1d34-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="a1d34-125">0</span><span class="sxs-lookup"><span data-stu-id="a1d34-125">0</span></span>           | <span data-ttu-id="a1d34-126">Streng (og Enum)</span><span class="sxs-lookup"><span data-stu-id="a1d34-126">String (and Enum)</span></span> | <span data-ttu-id="a1d34-127">Feltet vises som et tekstfelt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="a1d34-128">1</span><span class="sxs-lookup"><span data-stu-id="a1d34-128">1</span></span>           | <span data-ttu-id="a1d34-129">Integer</span><span class="sxs-lookup"><span data-stu-id="a1d34-129">Integer</span></span>           | <span data-ttu-id="a1d34-130">Verdien vises som et tall uten desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="a1d34-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="a1d34-131">2</span><span class="sxs-lookup"><span data-stu-id="a1d34-131">2</span></span>           | <span data-ttu-id="a1d34-132">Reell</span><span class="sxs-lookup"><span data-stu-id="a1d34-132">Real</span></span>              | <span data-ttu-id="a1d34-133">Verdien vises som et tall med desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="a1d34-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="a1d34-134">Hvis du vil vise den reelle verdien som en valuta i appen, bruker du egenskapen **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="a1d34-135">Du kan bruke egenskapen **numberOfDecimals** til å angi antall desimalplasser som vises.</span><span class="sxs-lookup"><span data-stu-id="a1d34-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="a1d34-136">3</span><span class="sxs-lookup"><span data-stu-id="a1d34-136">3</span></span>           | <span data-ttu-id="a1d34-137">Date</span><span class="sxs-lookup"><span data-stu-id="a1d34-137">Date</span></span>              | <span data-ttu-id="a1d34-138">Datoformater bestemmes av innstillingene for brukerens **dato, klokkeslett og tallformat** som er angitt under **innstillingen for språk og land/område** i **Brukeralternativer**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="a1d34-139">4</span><span class="sxs-lookup"><span data-stu-id="a1d34-139">4</span></span>           | <span data-ttu-id="a1d34-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="a1d34-140">Boolean</span></span>           | |
| <span data-ttu-id="a1d34-141">15</span><span class="sxs-lookup"><span data-stu-id="a1d34-141">15</span></span>          | <span data-ttu-id="a1d34-142">GUID</span><span class="sxs-lookup"><span data-stu-id="a1d34-142">GUID</span></span>              | |
| <span data-ttu-id="a1d34-143">16</span><span class="sxs-lookup"><span data-stu-id="a1d34-143">16</span></span>          | <span data-ttu-id="a1d34-144">Int64</span><span class="sxs-lookup"><span data-stu-id="a1d34-144">Int64</span></span>             | |

- <span data-ttu-id="a1d34-145">Hvis egenskapen **stringOptions** ikke er angitt på **TSTimesheetCustomField**-objektet, gis det et fritekstfelt til brukeren.</span><span class="sxs-lookup"><span data-stu-id="a1d34-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="a1d34-146">Egenskapen **stringLength** kan brukes til å angi maksimal strenglengde som brukere kan angi.</span><span class="sxs-lookup"><span data-stu-id="a1d34-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="a1d34-147">Hvis **stringOptions** er angitt på **TSTimesheetCustomField**-objektet, er disse listeelementene de eneste verdiene brukerne kan velge ved å bruke alternativknapper (alternativknapper).</span><span class="sxs-lookup"><span data-stu-id="a1d34-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="a1d34-148">I dette tilfellet kan strengfeltet fungere som en opplistingsverdi for formålet med brukeroppføringen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="a1d34-149">Hvis du vil lagre verdien i databasen som en opplisting, må du manuelt tilordne strengverdien tilbake til opplistingsverdien før du lagrer databasen ved hjelp av kommandokjede (se "Bruke kommandokjede i TSTimesheetEntryService-klassen for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).</span><span class="sxs-lookup"><span data-stu-id="a1d34-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="a1d34-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="a1d34-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="a1d34-151">Du kan bruke denne egenskapen til å formatere reelle verdier som valuta.</span><span class="sxs-lookup"><span data-stu-id="a1d34-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="a1d34-152">Denne metoden gjelder bare når **fieldBaseType**-verdien er **Reell**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="a1d34-153">**TSCustomFieldExtendedType:None** – Ingen formatering brukes.</span><span class="sxs-lookup"><span data-stu-id="a1d34-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="a1d34-154">**TSCustomFieldExtendedType::Currency** – Formaterer verdien som valuta.</span><span class="sxs-lookup"><span data-stu-id="a1d34-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="a1d34-155">Når valutaformatering er aktiv, kan **stringValue**-feltet brukes til å sende valutakoden som skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="a1d34-156">Verdien er en skrivebeskyttet verdi.</span><span class="sxs-lookup"><span data-stu-id="a1d34-156">The value is a read-only value.</span></span>

    <span data-ttu-id="a1d34-157">Feltet **realValue** inneholder pengebeløpet som skal lagres i databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="a1d34-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="a1d34-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="a1d34-159">Du kan bruke denne egenskapen til å angi hvor det egendefinerte feltet skal vises i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="a1d34-160">**TSCustomFieldSection::Header** – Feltet vises i delen **Vis flere detaljer** i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="a1d34-161">Disse feltene er alltid skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-161">These fields are always read-only.</span></span>
- <span data-ttu-id="a1d34-162">**TSCustomFieldSection::Line** – Feltet vises etter alle standardlinjefelt i timeregistreringsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a1d34-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="a1d34-163">Disse feltene kan enten være redigerbare eller skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="a1d34-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="a1d34-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="a1d34-165">Denne egenskapen identifiserer feltet når verdier som appen gir, lagres tilbake til databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="a1d34-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="a1d34-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="a1d34-167">Denne egenskapen identifiserer feltet når verdier som appen gir, lagres tilbake til databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="a1d34-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a1d34-168">isEditable (NoYes)</span></span>

<span data-ttu-id="a1d34-169">Sett denne egenskapen til **Ja** for å angi at feltet i delen for timeregistreringoppføring bør redigeres av brukere.</span><span class="sxs-lookup"><span data-stu-id="a1d34-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="a1d34-170">Sett egenskapen til **Nei** for å gjøre feltet skrivebeskyttet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="a1d34-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="a1d34-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="a1d34-172">Sett denne egenskapen til **Ja** for å angi at feltet i delen for timeregistreringoppføring bør være obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="a1d34-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="a1d34-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="a1d34-173">label (str)</span></span>

<span data-ttu-id="a1d34-174">Denne egenskapen angir etiketten som vises ved siden av feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="a1d34-175">stringOptions (liste over strenger)</span><span class="sxs-lookup"><span data-stu-id="a1d34-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="a1d34-176">Denne egenskapen gjelder bare når **fieldBaseType** er satt til **String**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="a1d34-177">Hvis **stringOptions** er angitt, angis strengverdiene som er tilgjengelige for valget via alternativknapper (alternativknapper), av strengene i listen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="a1d34-178">Hvis det ikke er angitt noen strenger, tillates fritekstregistrering i strengfeltet (se "Bruke kommandokjede i TSTimesheetEntryService-klassen for å lagre en timeregistreringsoppføring fra appen tilbake til databasen" senere i dette emnet for å se et eksempel).</span><span class="sxs-lookup"><span data-stu-id="a1d34-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="a1d34-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="a1d34-179">stringLength (int)</span></span>

<span data-ttu-id="a1d34-180">Denne egenskapen angir maksimumslengden for et strengfelt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="a1d34-181">Den gjelder bare når **fieldBaseType** er satt til **Streng**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="a1d34-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="a1d34-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="a1d34-183">Denne egenskapen angir antallet desimaler som vises for et reelt felt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="a1d34-184">Den gjelder bare når **fieldBaseType** er satt til **Reell**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="a1d34-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="a1d34-185">orderSequence (int)</span></span>

<span data-ttu-id="a1d34-186">Denne egenskapen kontrollerer i hvilken rekkefølge de egendefinerte feltene vises i appen når mer enn ett egendefinert felt er angitt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="a1d34-187">Felt som har lavere tall, vises først.</span><span class="sxs-lookup"><span data-stu-id="a1d34-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="a1d34-188">booleanValue (boolsk)</span><span class="sxs-lookup"><span data-stu-id="a1d34-188">booleanValue (boolean)</span></span>

<span data-ttu-id="a1d34-189">For felt av typen **Boolsk** sender denne egenskapen den boolske verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="a1d34-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="a1d34-190">guidValue (guid)</span></span>

<span data-ttu-id="a1d34-191">For felt av typen **GUID** sender denne egenskapen verdien for den globalt unike identifikatoren (GUID) for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="a1d34-192">int64Value (Int64)</span><span class="sxs-lookup"><span data-stu-id="a1d34-192">int64Value (int64)</span></span>

<span data-ttu-id="a1d34-193">For felt av typen **Int64** sender denne egenskapen int64-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="a1d34-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="a1d34-194">intValue (int)</span></span>

<span data-ttu-id="a1d34-195">For felt av typen **Int** sender denne egenskapen int-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="a1d34-196">realValue (reell)</span><span class="sxs-lookup"><span data-stu-id="a1d34-196">realValue (real)</span></span>

<span data-ttu-id="a1d34-197">For felt av typen **Reell** sender denne egenskapen reell-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="a1d34-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="a1d34-198">stringValue (str)</span></span>

<span data-ttu-id="a1d34-199">For felt av typen **Streng** sender denne egenskapen streng-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="a1d34-200">Det brukes også for felt av typen **Reell** som er formatert som valuta.</span><span class="sxs-lookup"><span data-stu-id="a1d34-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="a1d34-201">For disse feltene brukes egenskapen til å sende valutakoden til appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="a1d34-202">dateValue (dato)</span><span class="sxs-lookup"><span data-stu-id="a1d34-202">dateValue (date)</span></span>

<span data-ttu-id="a1d34-203">For felt av typen **Dato** sender denne egenskapen dato-verdien for feltet mellom serveren og appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a1d34-204">Vise og lagre et egendefinert felt i delen for timeregistreringsoppføring</span><span class="sxs-lookup"><span data-stu-id="a1d34-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="a1d34-205">Nedenfor vises et skjermbilde fra mobilappen av oppretting av en timeregistreringsoppføring.</span><span class="sxs-lookup"><span data-stu-id="a1d34-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="a1d34-206">Den viser felt med flere bokser og et egendefinert felt i delen "Tidsregistrering" som kalles "Test streng" der opplistingsverdien "Andre alternativ" allerede er angitt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Egendefinerte felt for teststreng i appen](media/timesheet-entry.jpg)



<span data-ttu-id="a1d34-208">Nedenfor finner du et skjermbilde fra mobilappen av brukeren som velger et av opplistingsalternativene som er tilgjengelige for det egendefinerte feltet "Teststreng".</span><span class="sxs-lookup"><span data-stu-id="a1d34-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="a1d34-209">De to alternativene er "Første alternativ" og "Andre alternativ" som vises som alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="a1d34-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="a1d34-210">Det andre alternativet er allerede valgt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-210">The second option is currently selected.</span></span>

![Alternativknapper (radioknapper) for det egendefinerte feltet Teststreng](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a1d34-212">Utvid TSTimesheetLine-tabellen slik at den inneholder et egendefinert felt</span><span class="sxs-lookup"><span data-stu-id="a1d34-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="a1d34-213">I typiske scenarier er det sannsynlig at dataene for et egendefinert felt i delen for timeregistreringsoppføring blir lagret i TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="a1d34-214">Andre tabeller kan imidlertid brukes hvis dataene kan hentes basert på en TSTimesheetTrans-oppføring som er levert, eller hvis den ikke har en bestemt oppføringskontekst (for eksempel hvis feltet er angitt som skrivebeskyttet i prosjektparameterne).</span><span class="sxs-lookup"><span data-stu-id="a1d34-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a1d34-215">Vær oppmerksom på at egendefinerte felt ikke trenger å ha noen sikkerhetskopi av databaseoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a1d34-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a1d34-216">De kan genereres dynamisk basert på X++-logikk.</span><span class="sxs-lookup"><span data-stu-id="a1d34-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a1d34-217">Denne metoden kan være nyttig i skrivebeskyttede scenarier (se delen "Bruke kommandokjede i TSTimesheetDetails-klassen buildCustomFieldListForHeader-metoden for å fylle ut timeregistreringsdetaljer" for å se et eksempel på dynamisk genererte egendefinerte feltverdier.)</span><span class="sxs-lookup"><span data-stu-id="a1d34-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="a1d34-218">Nedenfor vises et skjermbilde fra Visual Studio av programobjekttreet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="a1d34-219">Den viser en utvidelse av tabellen TSTimesheetLine med TestLineString-feltet lagt til som et egendefinert felt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Linjestreng](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="a1d34-221">Bruke kommandokjede på buildCustomFieldList-metoden i TSTimesheetSettings-klassen for å vise et felt i delen for timeregistreringsoppføring</span><span class="sxs-lookup"><span data-stu-id="a1d34-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="a1d34-222">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a1d34-223">Feltet angir for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken del feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="a1d34-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a1d34-224">Følgende eksempel viser et strengefelt for tidsoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a1d34-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="a1d34-225">Dette feltet har to alternativer, **Første alternativ** og **Andre alternativ**, som er tilgjengelige via alternativknapper.</span><span class="sxs-lookup"><span data-stu-id="a1d34-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="a1d34-226">Feltet i appen er knyttet til **TestLineString**-feltet som legges til i TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="a1d34-227">Legg merke til bruken av metoden **TSTimesheetCustomField::newFromMetatdata()** for å forenkle initialiseringen av egenskapene for det egendefinerte feltet: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** og **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="a1d34-228">Du kan også angi disse parameterne manuelt, i henhold til hva du foretrekker.</span><span class="sxs-lookup"><span data-stu-id="a1d34-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="a1d34-229">Bruke kommandokjede på buildCustomFieldListForEntry-metoden i TSTimesheetEntry-klassen for å angi verdier i en timeregistreringsoppføring</span><span class="sxs-lookup"><span data-stu-id="a1d34-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="a1d34-230">Metoden **buildCustomFieldListForEntry** brukes til å angi verdier for de lagrede timeregistreringslinjene i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="a1d34-231">Det kreves en TSTimesheetTrans-oppføring som parameter.</span><span class="sxs-lookup"><span data-stu-id="a1d34-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="a1d34-232">Felt fra denne oppføringen kan brukes til å fylle ut verdien for det egendefinerte feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="a1d34-233">Bruke kommandokjede i TSTimesheetEntryService-klassen til å lagre en timeregistreringsoppføring fra appen tilbake til databasen</span><span class="sxs-lookup"><span data-stu-id="a1d34-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="a1d34-234">Hvis du vil lagre et egendefinert felt tilbake til databasen i vanlig bruk, må du utvide flere metoder:</span><span class="sxs-lookup"><span data-stu-id="a1d34-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="a1d34-235">Metoden **timesheetLineNeedsUpdating** brukes til å finne ut om linjeoppføringen har blitt endret av brukeren i appen og må lagres i databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="a1d34-236">Hvis ytelse ikke er problematisk, kan denne metoden forenkles, slik at den alltid returnerer **sann**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="a1d34-237">Metodene **PopulateTimesheetLineFromEntryDuringCreate** og **populateTimesheetLineFromEntryDuringUpdate** kan utvides slik at de registrerer verdier i TSTimesheetLine-databaseoppføringen fra TSTimesheetEntry-datakontraktoppføringen som tilbys.</span><span class="sxs-lookup"><span data-stu-id="a1d34-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="a1d34-238">I eksemplet nedenfor ser du hvordan tilordningen mellom databasefeltet og oppføringsfeltet utføres manuelt via X++-kode.</span><span class="sxs-lookup"><span data-stu-id="a1d34-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="a1d34-239">Metoden **PopulateTimesheetWeekFromEntry** kan også utvides hvis det egendefinerte feltet som er tilordnet til **TSTimesheetEntry**-objektet, må skrive tilbake til TSTimesheetLineweek-databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="a1d34-240">Følgende eksempel lagrer **firstOption**- eller **secondOption**-verdien som brukeren velger for databasen som en rå strengverdi.</span><span class="sxs-lookup"><span data-stu-id="a1d34-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="a1d34-241">Hvis databasefeltet er et felt av typen **Enum**, kan disse verdiene tilordnes manuelt til en opplistingsverdi og deretter lagres i et opplistingsfelt i databasetabellen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="a1d34-242">Vise et egendefinert felt i delen for timeregistreringshode</span><span class="sxs-lookup"><span data-stu-id="a1d34-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="a1d34-243">Nedenfor vises et skjermbilde fra mobilappen av en bruker som viser en timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="a1d34-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="a1d34-244">Knappen "Mer informasjon" er valgt i det øvre høyre hjørnet for å vise alternativet "Vis flere detaljer".</span><span class="sxs-lookup"><span data-stu-id="a1d34-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Kommandoen Vis flere detaljer](media/show-more.png)

<span data-ttu-id="a1d34-246">Nedenfor vises et skjermbilde fra mobilappen som viser delen "Mer" av en timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="a1d34-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="a1d34-247">Et egendefinert felt kalt "Utnyttelsesgrad for denne timeregistreringen (beregnet egendefinert felt)" er lagt til i delen for timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="a1d34-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="a1d34-248">En skrivebeskyttet verdi på "0,667" er angitt i det egendefinerte feltet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Delen Mer](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="a1d34-250">Utvid TSTimesheetTable-tabellen slik at den inneholder et egendefinert felt</span><span class="sxs-lookup"><span data-stu-id="a1d34-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="a1d34-251">I typiske scenarier er det sannsynlig at dataene for et egendefinert felt i hodedelen blir hentet fra TSTimesheetLine-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="a1d34-252">Andre tabeller kan imidlertid brukes hvis dataene kan hentes basert på en TSTimesheetTable-oppføring som er levert, eller hvis den ikke har en bestemt oppføringskontekst (for eksempel hvis feltet er angitt som skrivebeskyttet i prosjektparameterne).</span><span class="sxs-lookup"><span data-stu-id="a1d34-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="a1d34-253">Vær oppmerksom på at egendefinerte felt ikke trenger å ha noen sikkerhetskopi av databaseoppføringer.</span><span class="sxs-lookup"><span data-stu-id="a1d34-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="a1d34-254">De kan genereres dynamisk basert på X++-logikk.</span><span class="sxs-lookup"><span data-stu-id="a1d34-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="a1d34-255">Eksemplet nedenfor viser denne metoden.</span><span class="sxs-lookup"><span data-stu-id="a1d34-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="a1d34-256">Felt i hodedelen er alltid skrivebeskyttet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="a1d34-257">Bruke kommandokjede på buildCustomFieldList-metoden i TSTimesheetSettings-klassen for å vise et felt i hodedelen</span><span class="sxs-lookup"><span data-stu-id="a1d34-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="a1d34-258">Denne koden kontrollerer visningsinnstillingene for feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="a1d34-259">Feltet angir for eksempel felttypen, etiketten, om feltet er obligatorisk, og hvilken del feltet vises i.</span><span class="sxs-lookup"><span data-stu-id="a1d34-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="a1d34-260">Følgende eksempel viser en beregnet verdi i hodedelen i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="a1d34-261">Bruke kommandokjede på buildCustomFieldListForHeader-metoden i TSTimesheetDetails-klassen for å fylle ut timeregistreringsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a1d34-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="a1d34-262">Metoden **buildCustomFieldListForHeader** brukes til å fylle ut timeregistreringshodedetaljer i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="a1d34-263">Det kreves en TSTimesheetTable-oppføring som parameter.</span><span class="sxs-lookup"><span data-stu-id="a1d34-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="a1d34-264">Felt fra denne oppføringen kan brukes til å fylle ut verdien for det egendefinerte feltet i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="a1d34-265">Eksemplet nedenfor leser ingen verdier fra databasen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="a1d34-266">I stedet brukes X++-logikk til å generere en beregnet verdi som vises i appen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="a1d34-267">Andre muligheter for konfigurerbarhet/utvidelse</span><span class="sxs-lookup"><span data-stu-id="a1d34-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="a1d34-268">Legge til ytterligere validering for appen</span><span class="sxs-lookup"><span data-stu-id="a1d34-268">Adding additional validation for the app</span></span>

<span data-ttu-id="a1d34-269">Eksisterende logikk for timeregistreringsfunksjonalitet på databasenivået vil fremdeles fungere som forventet.</span><span class="sxs-lookup"><span data-stu-id="a1d34-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="a1d34-270">Hvis du vil avbryte fullføringen av lagre- eller sendoperasjoner og vise en bestemt feilmelding, kan du legge til en **vis feil ("melding til bruker")** i koden via en kommandokjedeutvidelse.</span><span class="sxs-lookup"><span data-stu-id="a1d34-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="a1d34-271">Her er tre eksempler på nyttige utvidbare metoder:</span><span class="sxs-lookup"><span data-stu-id="a1d34-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="a1d34-272">Hvis **validateWrite** i TSTimesheetLine-tabellen returnerer **usann** under en lagringsoperasjon for en timeregistreringslinje, vises det en feilmelding i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="a1d34-273">Hvis **validateSubmit** i TSTimesheetTable-tabellen returnerer **usann** under en sending av timeregistrering i appen, vises det en feilmelding for brukeren.</span><span class="sxs-lookup"><span data-stu-id="a1d34-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="a1d34-274">Logikk som fyller ut feltene (for eksempel **Linjeegenskap**) under **innsetting**-metoden i TSTimesheetLine-tabellen, kjører fremdeles.</span><span class="sxs-lookup"><span data-stu-id="a1d34-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="a1d34-275">Skjule og merke standardfelt som skrivebeskyttet via konfigurasjon</span><span class="sxs-lookup"><span data-stu-id="a1d34-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="a1d34-276">Du kan bruke prosjektparameterne til å skrivebeskytte eller skjule standardfelt i mobilappen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="a1d34-277">Angi alternativene i delen **Mobile timeregistreringer** i kategorien **Timeregistrering** på siden **Parametere for prosjektstyring og regnskap**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Prosjektparametere](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="a1d34-279">Endre aktivitetene som er tilgjengelige for valg via utvidelser</span><span class="sxs-lookup"><span data-stu-id="a1d34-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="a1d34-280">Aktivitetene som er tilgjengelige for valg for et prosjekt, fylles ut via metodene **getActivitiesForProject()** og **getActivityQuery()** i klassen **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="a1d34-281">Du kan bruke kommandokjeden til å endre denne virkemåten, slik at den samsvarer med forretningsscenarioet for aktivitetene som er tilgjengelige for valg for et bestemt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="a1d34-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="a1d34-282">Angi en standard prosjektkategori på timeregistreringsoppføringer</span><span class="sxs-lookup"><span data-stu-id="a1d34-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="a1d34-283">Angivelse av en standard prosjektkategori på timeregistreringsoppføringer på tre nivåer.</span><span class="sxs-lookup"><span data-stu-id="a1d34-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="a1d34-284">Du kan bruke kommandokjeden til å utvide virkemåten på noen av eller alle disse nivåene for å oppnå den ønskede virkemåten.</span><span class="sxs-lookup"><span data-stu-id="a1d34-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="a1d34-285">Følgende hierarki brukes:</span><span class="sxs-lookup"><span data-stu-id="a1d34-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="a1d34-286">Appen prøver å angi standardkategorien fra prosjektressursen.</span><span class="sxs-lookup"><span data-stu-id="a1d34-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="a1d34-287">Denne standardkategorien angis i metodene **getCurrentUserResource** og **getDelegatedResourcesForCurrentUser** i klassen **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="a1d34-288">Hvis standardkategorien ikke er angitt på ressursnivået for prosjektet, prøver appen å hente den fra prosjektaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="a1d34-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="a1d34-289">Denne standardkategorien angis i metoden **getActivitiesForProject** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="a1d34-290">Hvis standardkategorien ikke er angitt på aktivitetsnivået for prosjektet, hentes standardkategorien fra prosjektparameterne.</span><span class="sxs-lookup"><span data-stu-id="a1d34-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="a1d34-291">Denne standardkategorien angis i metoden **getProjectDetailsbyRule** i klassen **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="a1d34-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]