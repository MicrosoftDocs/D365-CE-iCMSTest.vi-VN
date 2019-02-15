---
title: Create auto-number-attributes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs)
description: Learn about creating auto-number attribute in the same way you create a string attribute using the StringAttributeMetadata class except that you use the new AutoNumberFormat property. Use the AutoNumberFormat property to define a pattern that includes sequential numbers and random strings by composing placeholders, which indicates the length and type of values that are generated.
keywords: Auto-number attributes
ms.date: 06/13/2018
ms.service: crm-online
ms.topic: article
applies_to:
- CRM 2017
- Dynamics 365 for Customer Engagement
ms.assetid: e97477d2-5509-9f5e-76e0-e0039b2e72c8
author: kabala123
ms.author: kabala
manager: kudesia
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9101f02e1aa875af203c2c5212ca61361931f74d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388235"
---
# <a name="create-auto-number-attributes"></a><span data-ttu-id="5c4c9-105">Create auto-number attributes</span><span class="sxs-lookup"><span data-stu-id="5c4c9-105">Create auto-number attributes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="5c4c9-106">With the [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] release, you can add an auto-number attribute for any entity.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-106">With the [!INCLUDE [pn-crm-9-0-0-online](../includes/pn-crm-9-0-0-online.md)] release, you can add an auto-number attribute for any entity.</span></span> <span data-ttu-id="5c4c9-107">Currently, you can add the attribute programmatically.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-107">Currently, you can add the attribute programmatically.</span></span> <span data-ttu-id="5c4c9-108">There is no user interface to add this type of attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-108">There is no user interface to add this type of attribute.</span></span> <span data-ttu-id="5c4c9-109">The topic explains how you can programmatically create an auto-number attribute and set a seed value for sequential elements.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-109">The topic explains how you can programmatically create an auto-number attribute and set a seed value for sequential elements.</span></span> <span data-ttu-id="5c4c9-110">In addition, the topic shows how to set the sequence number for the next record if you need to reset the seed at any time later.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-110">In addition, the topic shows how to set the sequence number for the next record if you need to reset the seed at any time later.</span></span>
> [!NOTE]
><span data-ttu-id="5c4c9-111">The setting of the seed is optional.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-111">The setting of the seed is optional.</span></span> <span data-ttu-id="5c4c9-112">There is no need to call the seed if you don’t need to reseed.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-112">There is no need to call the seed if you don’t need to reseed.</span></span>


<span data-ttu-id="5c4c9-113">You can create an auto-number attribute in the same way you create a string attribute using the **StringAttributeMetadata** class except that you use the new **AutoNumberFormat** property.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-113">You can create an auto-number attribute in the same way you create a string attribute using the **StringAttributeMetadata** class except that you use the new **AutoNumberFormat** property.</span></span> <span data-ttu-id="5c4c9-114">Use the **AutoNumberFormat** property to define a pattern that includes sequential numbers and random strings by composing placeholders, which indicates the length and type of values that are generated.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-114">Use the **AutoNumberFormat** property to define a pattern that includes sequential numbers and random strings by composing placeholders, which indicates the length and type of values that are generated.</span></span> <span data-ttu-id="5c4c9-115">The random strings help you to avoid duplicates or collisions, especially when offline clients trying to create auto-numbers.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-115">The random strings help you to avoid duplicates or collisions, especially when offline clients trying to create auto-numbers.</span></span>

<span data-ttu-id="5c4c9-116">When creating an auto-number attribute, the **StringAttributeMetadata.FormatName** property or the **StringAttributeMetadata.Format** property values must be Text.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-116">When creating an auto-number attribute, the **StringAttributeMetadata.FormatName** property or the **StringAttributeMetadata.Format** property values must be Text.</span></span> <span data-ttu-id="5c4c9-117">Since these are the default values you will typically not set this property.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-117">Since these are the default values you will typically not set this property.</span></span> <span data-ttu-id="5c4c9-118">You cannot create an auto-number attribute that uses any other special kind of format such as Email, Phone, TextArea, Url or any other [existing formats](https://msdn.microsoft.com/en-us/library/microsoft.xrm.sdk.metadata.stringformatname.aspx).</span><span class="sxs-lookup"><span data-stu-id="5c4c9-118">You cannot create an auto-number attribute that uses any other special kind of format such as Email, Phone, TextArea, Url or any other [existing formats](https://msdn.microsoft.com/en-us/library/microsoft.xrm.sdk.metadata.stringformatname.aspx).</span></span>

<span data-ttu-id="5c4c9-119">The sequential segment is generated by SQL and hence uniqueness is guaranteed by SQL.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-119">The sequential segment is generated by SQL and hence uniqueness is guaranteed by SQL.</span></span>

> [!NOTE]
><span data-ttu-id="5c4c9-120">You can modify an existing format text attribute to be an auto-number format.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-120">You can modify an existing format text attribute to be an auto-number format.</span></span>

<span data-ttu-id="5c4c9-121">When you add the auto-number attribute as a field to a form, the auto-number attribute field behaves as read-only in the form, and end-users cannot edit the field.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-121">When you add the auto-number attribute as a field to a form, the auto-number attribute field behaves as read-only in the form, and end-users cannot edit the field.</span></span> <span data-ttu-id="5c4c9-122">The value is set only after you save the entity.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-122">The value is set only after you save the entity.</span></span> <span data-ttu-id="5c4c9-123">You can see auto-number attribute as any other field value in views, grids and so on.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-123">You can see auto-number attribute as any other field value in views, grids and so on.</span></span>

### <a name="examples"></a><span data-ttu-id="5c4c9-124">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5c4c9-124">Examples</span></span>
<span data-ttu-id="5c4c9-125">The following examples show how to create a new auto-number attribute named **new\_SerialNumber** for a custom entity named **new\_Widget** which will have a value that looks like this: **WID-00001-AB7LSFG-20170913070240**.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-125">The following examples show how to create a new auto-number attribute named **new\_SerialNumber** for a custom entity named **new\_Widget** which will have a value that looks like this: **WID-00001-AB7LSFG-20170913070240**.</span></span>
<span data-ttu-id="5c4c9-126">Using the Organization service with SDK assemblies **CreateAttributeRequest** and **StringAttributeMetadata** classes:</span><span class="sxs-lookup"><span data-stu-id="5c4c9-126">Using the Organization service with SDK assemblies **CreateAttributeRequest** and **StringAttributeMetadata** classes:</span></span>

```csharp
CreateAttributeRequest widgetSerialNumberAttributeRequest = new CreateAttributeRequest
            {
                EntityName = "newWidget",
                Attribute = new StringAttributeMetadata
                {
                    //Define the format of the attribute
                    AutoNumberFormat = "WID-{SEQNUM:5}-{RANDSTRING:6}-{DATETIMEUTC:yyyyMMddhhmmss}",
                    LogicalName = "new_serialnumber",
                    SchemaName = "new_SerialNumber",
                    RequiredLevel = new AttributeRequiredLevelManagedProperty(AttributeRequiredLevel.None),
                    MaxLength = 100, // The MaxLength defined for the string attribute must be greater than the length of the AutoNumberFormat value, that is, it should be able to fit in the generated value.
                    DisplayName = new Label("Serial Number", 1033),
                    Description = new Label("Serial Number of the widget.", 1033)
                }
            };
            _serviceProxy.Execute(widgetSerialNumberAttributeRequest);
```

## <a name="use-web-api"></a><span data-ttu-id="5c4c9-127">Use Web API</span><span class="sxs-lookup"><span data-stu-id="5c4c9-127">Use Web API</span></span>

<span data-ttu-id="5c4c9-128">You can create and update entity definitions using the Web API.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-128">You can create and update entity definitions using the Web API.</span></span>

<span data-ttu-id="5c4c9-129">More information: [Create and update entity definitions using the Web API > Create attributes](https://msdn.microsoft.com/en-us/library/mt593078.aspx#Anchor_3).</span><span class="sxs-lookup"><span data-stu-id="5c4c9-129">More information: [Create and update entity definitions using the Web API > Create attributes](https://msdn.microsoft.com/en-us/library/mt593078.aspx#Anchor_3).</span></span>

#### <a name="request"></a><span data-ttu-id="5c4c9-130">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5c4c9-130">Request</span></span>
```http
POST [Organization URI]/api/data/v9.0/EntityDefinitions(LogicalName='new_widget')/Attributes HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
 "AttributeType": "String",
 "AttributeTypeName": {
  "Value": "StringType"
 },
 "Description": {
  "@odata.type": "Microsoft.Dynamics.CRM.Label",
  "LocalizedLabels": [
   {
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",
    "Label": "Serial Number of the widget.",
    "LanguageCode": 1033
   }
  ]
 },
 "DisplayName": {
  "@odata.type": "Microsoft.Dynamics.CRM.Label",
  "LocalizedLabels": [
   {
    "@odata.type": "Microsoft.Dynamics.CRM.LocalizedLabel",
    "Label": "Serial Number",
    "LanguageCode": 1033
   }
  ]
 },
 "RequiredLevel": {
  "Value": "None",
  "CanBeChanged": true,
  "ManagedPropertyLogicalName": "canmodifyrequirementlevelsettings"
 },
 "SchemaName": "new_SerialNumber",
 "AutoNumberFormat": "WID-{SEQNUM:5}-{RANDSTRING:6}-{DATETIMEUTC:yyyyMMddhhmmss}",
 "@odata.type": "Microsoft.Dynamics.CRM.StringAttributeMetadata",
 "FormatName": {
  "Value": "Text"
 },
 "MaxLength": 100
}
```

#### <a name="response"></a><span data-ttu-id="5c4c9-131">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="5c4c9-131">Response</span></span>

```http
HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.0/EntityDefinitions(402fa40f-287c-e511-80d2-00155d2a68d2)/Attributes(f01bef16-287c-e511-80d2-00155d2a68d2)
```

## <a name="autonumberformat-options"></a><span data-ttu-id="5c4c9-132">AutoNumberFormat options</span><span class="sxs-lookup"><span data-stu-id="5c4c9-132">AutoNumberFormat options</span></span>

<span data-ttu-id="5c4c9-133">These examples show how you can configure the **AutoNumberFormat** property to get different results:</span><span class="sxs-lookup"><span data-stu-id="5c4c9-133">These examples show how you can configure the **AutoNumberFormat** property to get different results:</span></span>

|<span data-ttu-id="5c4c9-134">**AutoNumberFormat value**</span><span class="sxs-lookup"><span data-stu-id="5c4c9-134">**AutoNumberFormat value**</span></span>|<span data-ttu-id="5c4c9-135">**Example value**</span><span class="sxs-lookup"><span data-stu-id="5c4c9-135">**Example value**</span></span>|
|:----------|:----------|
|`CAR-{SEQNUM:3}-{RANDSTRING:6}`|`CAR-123-AB7LSF`|
|`CNR-{RANDSTRING:4}-{SEQNUM:4}`|`CNR-WXYZ-1000`|
|`{SEQNUM:6}-#-{RANDSTRING:3}`  |`123456-#-R3V`|
|`KA-{SEQNUM:4}`                |`KA-0001`|
|`{SEQNUM:10}`                  |`1234567890`|
|`QUO-{SEQNUM:3}#{RANDSTRING:3}#{RANDSTRING:5}`|      `QUO-123#ABC#PQ2ST`|
|`QUO-{SEQNUM:7}{RANDSTRING:5}` |`QUO-0001000P9G3R`|
|`CAS-{SEQNUM:6}-{RANDSTRING:6}-{DATETIMEUTC:yyyyMMddhhmmss}`|`CAS-002000-S1P0H0-20170913091544`|
|`CAS-{SEQNUM:6}-{DATETIMEUTC:yyyyMMddhh}-{RANDSTRING:6}`|`CAS-002002-2017091309-HTZOUR`|
|`CAS-{SEQNUM:6}-{DATETIMEUTC:yyyyMM}-{RANDSTRING:6}-{DATETIMEUTC:hhmmss}`|`CAS-002000-201709-Z8M2Z6-110901`|

<span data-ttu-id="5c4c9-136">The random string placeholders are optional.You can include more than one random string placeholder.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-136">The random string placeholders are optional.You can include more than one random string placeholder.</span></span> <span data-ttu-id="5c4c9-137">Use any of the format value for datetime placeholders from [Standard Date and Time Format Strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="5c4c9-137">Use any of the format value for datetime placeholders from [Standard Date and Time Format Strings](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-date-and-time-format-strings).</span></span>

### <a name="string-length"></a><span data-ttu-id="5c4c9-138">String length</span><span class="sxs-lookup"><span data-stu-id="5c4c9-138">String length</span></span>

<span data-ttu-id="5c4c9-139">The table shows the string length value for the random and sequential placeholders.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-139">The table shows the string length value for the random and sequential placeholders.</span></span>

<table>
  <tr>
    <th><span data-ttu-id="5c4c9-140">Placeholder</span><span class="sxs-lookup"><span data-stu-id="5c4c9-140">Placeholder</span></span></th>
    <th><span data-ttu-id="5c4c9-141">String Length</span><span class="sxs-lookup"><span data-stu-id="5c4c9-141">String Length</span></span></th>
    <th><span data-ttu-id="5c4c9-142">Output Scenario</span><span class="sxs-lookup"><span data-stu-id="5c4c9-142">Output Scenario</span></span></th>
  </tr>
  <tr>
    <td><code>{RANDSTRING:MIN_LENGTH}</code></td>
    <td><span data-ttu-id="5c4c9-143">The value of <b>MIN_LENGTH</b> is between 1 and 6.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-143">The value of <b>MIN_LENGTH</b> is between 1 and 6.</span></span></td>
     <td><span data-ttu-id="5c4c9-144">When you save the entity, the auto-number attribute generates the random string with the defined length if the value is between 1 and 6.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-144">When you save the entity, the auto-number attribute generates the random string with the defined length if the value is between 1 and 6.</span></span> <span data-ttu-id="5c4c9-145">If you use the <b>MIN_LENGTH</b> value as 7 or beyond 7, you get to see an Invalid Argument error.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-145">If you use the <b>MIN_LENGTH</b> value as 7 or beyond 7, you get to see an Invalid Argument error.</span></span></td>
  </tr>
  <tr>
    <td><code>{SEQNUM:MIN_LENGTH}</code></td>
    <td><span data-ttu-id="5c4c9-146">The minimum value of the <b>MIN_LENGTH</b> is 1.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-146">The minimum value of the <b>MIN_LENGTH</b> is 1.</span></span> <span data-ttu-id="5c4c9-147">The number continues to increment beyond the minimum length.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-147">The number continues to increment beyond the minimum length.</span></span></td>
    <td><span data-ttu-id="5c4c9-148">When you save the entity, the auto-number attribute works fine and continue to work fine for larger values of <b>MIN_LENGTH</b>.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-148">When you save the entity, the auto-number attribute works fine and continue to work fine for larger values of <b>MIN_LENGTH</b>.</span></span></td></table>

<span data-ttu-id="5c4c9-149">For sequential value placeholders, the **MIN_LENGTH** is a minimum length.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-149">For sequential value placeholders, the **MIN_LENGTH** is a minimum length.</span></span> <span data-ttu-id="5c4c9-150">If you set the value to be 2, the initial value will be 01, and the 100th entity value will be 100.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-150">If you set the value to be 2, the initial value will be 01, and the 100th entity value will be 100.</span></span> <span data-ttu-id="5c4c9-151">The number will continue to increment beyond the minimum length.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-151">The number will continue to increment beyond the minimum length.</span></span> <span data-ttu-id="5c4c9-152">The value in setting the length for sequential values is to establish a consistent length for the auto-generated value by adding additional 0s to the initial value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-152">The value in setting the length for sequential values is to establish a consistent length for the auto-generated value by adding additional 0s to the initial value.</span></span> <span data-ttu-id="5c4c9-153">It will not limit the absolute value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-153">It will not limit the absolute value.</span></span> <span data-ttu-id="5c4c9-154">Random value placeholders will always be the same length.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-154">Random value placeholders will always be the same length.</span></span>

<span data-ttu-id="5c4c9-155">Because the sequential values can get larger than the minimum length allotted for them, you should not adjust the **StringAttributeMetadata.MaxLength** property to match the length of your formatted value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-155">Because the sequential values can get larger than the minimum length allotted for them, you should not adjust the **StringAttributeMetadata.MaxLength** property to match the length of your formatted value.</span></span> <span data-ttu-id="5c4c9-156">There is little value in doing this and it could cause an error in the future if the value exceeds the **MaxLength** value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-156">There is little value in doing this and it could cause an error in the future if the value exceeds the **MaxLength** value.</span></span> <span data-ttu-id="5c4c9-157">Make sure you leave enough room for a realistic range of sequential values.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-157">Make sure you leave enough room for a realistic range of sequential values.</span></span>

> [!NOTE]
> <span data-ttu-id="5c4c9-158">There is no validation of the placeholder values when you create the attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-158">There is no validation of the placeholder values when you create the attribute.</span></span> <span data-ttu-id="5c4c9-159">The error appears only when you try to save an entity instance that uses an incorrectly configured **AutoNumberFormat** value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-159">The error appears only when you try to save an entity instance that uses an incorrectly configured **AutoNumberFormat** value.</span></span>
> <span data-ttu-id="5c4c9-160">For example, if you specify the length of the random string more than 6, the first person creating a new entity instance gets an **Invalid Argument** error when they first try to save the entity containing the new auto-number attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-160">For example, if you specify the length of the random string more than 6, the first person creating a new entity instance gets an **Invalid Argument** error when they first try to save the entity containing the new auto-number attribute.</span></span>

## <a name="update-auto-number-attributes"></a><span data-ttu-id="5c4c9-161">Update auto-number attributes</span><span class="sxs-lookup"><span data-stu-id="5c4c9-161">Update auto-number attributes</span></span>

<span data-ttu-id="5c4c9-162">If you create an auto-number attribute with an incorrect configuration or you want to modify an existing auto-number attribute, you can update the attribute the **AutoNumberFormat** value.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-162">If you create an auto-number attribute with an incorrect configuration or you want to modify an existing auto-number attribute, you can update the attribute the **AutoNumberFormat** value.</span></span>

<span data-ttu-id="5c4c9-163">The following code snippet explains you to retrieve, modify, and update the auto-number attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-163">The following code snippet explains you to retrieve, modify, and update the auto-number attribute.</span></span>

<span data-ttu-id="5c4c9-164">To modify an existing auto-number attribute, you must retrieve the attribute using the **RetrieveAttributeRequest** class.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-164">To modify an existing auto-number attribute, you must retrieve the attribute using the **RetrieveAttributeRequest** class.</span></span>

```csharp
// Create the retrieve request
RetrieveAttributeRequest attributeRequest = new RetrieveAttributeRequest
            {
                EntityLogicalName = entityName.ToLower(),
                LogicalName = "new_serialnumber",
                RetrieveAsIfPublished = true
            };
// Retrieve attribute response
RetrieveAttributeResponse attributeResponse = (RetrieveAttributeResponse)_serviceProxy.Execute(attributeRequest);
```

<span data-ttu-id="5c4c9-165">After retrieving the auto-number attribute, you need to modify and update the attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-165">After retrieving the auto-number attribute, you need to modify and update the attribute.</span></span>

```csharp            
//Modify the retrieved auto-number attribute
AttributeMetadata retrievedAttributeMetadata = attributeResponse.AttributeMetadata;
retrievedAttributeMetadata.AutoNumberFormat = "CAR-{RANDSTRING:5}{SEQNUM:6}"; //Modify the existing attribute by writing the format as per your requirement 

// Update the auto-number attribute            
UpdateAttributeRequest updateRequest = new UpdateAttributeRequest
                        {
                            Attribute = retrievedAttributeMetadata,
                            EntityName = "newWidget",
                        };
// Execute the request
_serviceProxy.Execute(updateRequest);
```

## <a name="set-a-seed-value"></a><span data-ttu-id="5c4c9-166">Set a seed value</span><span class="sxs-lookup"><span data-stu-id="5c4c9-166">Set a seed value</span></span>

<span data-ttu-id="5c4c9-167">By default, all auto-number sequential values start with 1000 and use 0 as the prefix depending on the length.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-167">By default, all auto-number sequential values start with 1000 and use 0 as the prefix depending on the length.</span></span> <span data-ttu-id="5c4c9-168">In this way, the length of the value is always same.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-168">In this way, the length of the value is always same.</span></span> <span data-ttu-id="5c4c9-169">If you want to change the initial value, you need to change the initial seed value using the API below to set the next number that are used for the sequential segment.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-169">If you want to change the initial value, you need to change the initial seed value using the API below to set the next number that are used for the sequential segment.</span></span>

<span data-ttu-id="5c4c9-170">For example, when the length of the sequential number is 5, you may want to start with an initial value of 10000 instead of the default value of 00001.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-170">For example, when the length of the sequential number is 5, you may want to start with an initial value of 10000 instead of the default value of 00001.</span></span> <span data-ttu-id="5c4c9-171">If you want to choose a different starting value after creating the auto-numbering attribute, use the **SetAutoNumberSeed** message.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-171">If you want to choose a different starting value after creating the auto-numbering attribute, use the **SetAutoNumberSeed** message.</span></span> <span data-ttu-id="5c4c9-172">Use the **SetAutoNumberSeedRequest** class when using the SDK assemblies and **SetAutoNumberSeed** action when using the Web API.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-172">Use the **SetAutoNumberSeedRequest** class when using the SDK assemblies and **SetAutoNumberSeed** action when using the Web API.</span></span>

<span data-ttu-id="5c4c9-173">The **AutoNumberSeed** message has the following parameters:</span><span class="sxs-lookup"><span data-stu-id="5c4c9-173">The **AutoNumberSeed** message has the following parameters:</span></span>


|<span data-ttu-id="5c4c9-174">**Tên**</span><span class="sxs-lookup"><span data-stu-id="5c4c9-174">**Name**</span></span>|<span data-ttu-id="5c4c9-175">**Loại**</span><span class="sxs-lookup"><span data-stu-id="5c4c9-175">**Type**</span></span>|<span data-ttu-id="5c4c9-176">**Mô tả**</span><span class="sxs-lookup"><span data-stu-id="5c4c9-176">**Description**</span></span>|
|:----------|:----------|:----------|
|<span data-ttu-id="5c4c9-177">EntityName</span><span class="sxs-lookup"><span data-stu-id="5c4c9-177">EntityName</span></span>|<span data-ttu-id="5c4c9-178">chuỗi</span><span class="sxs-lookup"><span data-stu-id="5c4c9-178">string</span></span>|<span data-ttu-id="5c4c9-179">The logical name of the entity that contains the attribute you want to set the seed on.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-179">The logical name of the entity that contains the attribute you want to set the seed on.</span></span>|
|<span data-ttu-id="5c4c9-180">AttributeName</span><span class="sxs-lookup"><span data-stu-id="5c4c9-180">AttributeName</span></span>|<span data-ttu-id="5c4c9-181">chuỗi</span><span class="sxs-lookup"><span data-stu-id="5c4c9-181">string</span></span>|<span data-ttu-id="5c4c9-182">The logical name of the attribute you want to set the seed on.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-182">The logical name of the attribute you want to set the seed on.</span></span>|
|<span data-ttu-id="5c4c9-183">Value</span><span class="sxs-lookup"><span data-stu-id="5c4c9-183">Value</span></span>|<span data-ttu-id="5c4c9-184">int</span><span class="sxs-lookup"><span data-stu-id="5c4c9-184">int</span></span>|<span data-ttu-id="5c4c9-185">Next auto-number value for the attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-185">Next auto-number value for the attribute.</span></span>|

> [!NOTE]
> <span data-ttu-id="5c4c9-186">Setting the seed only changes the **current number value** for the specified attribute in the current environment.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-186">Setting the seed only changes the **current number value** for the specified attribute in the current environment.</span></span> <span data-ttu-id="5c4c9-187">It does not imply a common **start value** for the attribute.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-187">It does not imply a common **start value** for the attribute.</span></span> <span data-ttu-id="5c4c9-188">The seed value is not included in a solution when installed in a different environments.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-188">The seed value is not included in a solution when installed in a different environments.</span></span> <span data-ttu-id="5c4c9-189">To set the starting number after a solution import, use **SetAutoNumberSeed** message in the target environment.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-189">To set the starting number after a solution import, use **SetAutoNumberSeed** message in the target environment.</span></span>

### <a name="examples"></a><span data-ttu-id="5c4c9-190">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="5c4c9-190">Examples</span></span>
<span data-ttu-id="5c4c9-191">The following samples set the seed to 10000 for an auto-number attribute named **new\_SerialNumber** for a custom entity named **new\_Widget**.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-191">The following samples set the seed to 10000 for an auto-number attribute named **new\_SerialNumber** for a custom entity named **new\_Widget**.</span></span>

<span data-ttu-id="5c4c9-192">Using the Organization service with SDK assemblies **SetAutoNumberSeedRequest** class:</span><span class="sxs-lookup"><span data-stu-id="5c4c9-192">Using the Organization service with SDK assemblies **SetAutoNumberSeedRequest** class:</span></span>
```csharp
//Define the seed 
SetAutoNumberSeedRequest req = new SetAutoNumberSeedRequest();
req.EntityName = "newWidget";
req.AttributeName = "newSerialnumber";
req.Value = 10000;
_serviceProxy.Execute(req);
```
<span data-ttu-id="5c4c9-193">Using the Web API **SetAutoNumberSeed** Action.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-193">Using the Web API **SetAutoNumberSeed** Action.</span></span>

<span data-ttu-id="5c4c9-194">More information: [Use Web API actions > Unbound actions](https://msdn.microsoft.com/en-us/library/mt607600.aspx#bkmk_unboundActions)</span><span class="sxs-lookup"><span data-stu-id="5c4c9-194">More information: [Use Web API actions > Unbound actions](https://msdn.microsoft.com/en-us/library/mt607600.aspx#bkmk_unboundActions)</span></span>

#### <a name="request"></a><span data-ttu-id="5c4c9-195">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="5c4c9-195">Request</span></span>

```http
POST [Organization URI]/api/data/v9.0/SetAutoNumberSeed HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
 "EntityName": "new_Widget",
 "AttributeName": "new_Serialnumber",
 "Value": 10000
} 
```

#### <a name="response"></a><span data-ttu-id="5c4c9-196">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="5c4c9-196">Response</span></span>

```json
HTTP/1.1 204 No Content
OData-Version: 4.0
```
## <a name="community-tools"></a><span data-ttu-id="5c4c9-197">Các công cụ dành cho cộng đồng</span><span class="sxs-lookup"><span data-stu-id="5c4c9-197">Community tools</span></span>

### <a name="auto-number-manager"></a><span data-ttu-id="5c4c9-198">Auto Number Manager</span><span class="sxs-lookup"><span data-stu-id="5c4c9-198">Auto Number Manager</span></span>

<span data-ttu-id="5c4c9-199">**[Auto Number Manager](https://www.xrmtoolbox.com/plugins/Rappen.XrmToolBox.AutoNumManager/)** for XrmToolBox is a community driven tool for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps that provides a UI to set, update and remove auto number format on new or existing attributes.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-199">**[Auto Number Manager](https://www.xrmtoolbox.com/plugins/Rappen.XrmToolBox.AutoNumManager/)** for XrmToolBox is a community driven tool for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps that provides a UI to set, update and remove auto number format on new or existing attributes.</span></span>
<span data-ttu-id="5c4c9-200">Please see the [Developer tools](developer-tools.md) topic for community developed tools and [anm.xrmtoolbox.com](http://anm.xrmtoolbox.com) for more information about Auto Number Manager.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-200">Please see the [Developer tools](developer-tools.md) topic for community developed tools and [anm.xrmtoolbox.com](http://anm.xrmtoolbox.com) for more information about Auto Number Manager.</span></span>

> [!NOTE]
> <span data-ttu-id="5c4c9-201">The community tools are not a product of [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] apps and does not extend support to the community tools.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-201">The community tools are not a product of [!include[pn_microsoft_dynamics](../includes/pn-microsoft-dynamics.md)] apps and does not extend support to the community tools.</span></span> <span data-ttu-id="5c4c9-202">If you have questions pertaining to the tool, please contact the publisher.</span><span class="sxs-lookup"><span data-stu-id="5c4c9-202">If you have questions pertaining to the tool, please contact the publisher.</span></span> <span data-ttu-id="5c4c9-203">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span><span class="sxs-lookup"><span data-stu-id="5c4c9-203">More Information: [XrmToolBox](https://www.xrmtoolbox.com).</span></span> 


### <a name="see-also"></a><span data-ttu-id="5c4c9-204">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5c4c9-204">See Also</span></span>
[<span data-ttu-id="5c4c9-205">Metadata and data models</span><span class="sxs-lookup"><span data-stu-id="5c4c9-205">Metadata and data models</span></span>](metadata-data-models.md)  
[<span data-ttu-id="5c4c9-206">Customize entity attribute metadata</span><span class="sxs-lookup"><span data-stu-id="5c4c9-206">Customize entity attribute metadata</span></span>](customize-entity-attribute-metadata.md) 
