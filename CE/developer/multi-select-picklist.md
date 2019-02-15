---
title: Multi-Select Picklist attributes (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about multi-select picklist attributes that allow storing multiple option choices in a single attribute.
ms.custom: ''
ms.date: 09/05/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 2a71402b-dbd1-449c-b43b-d9531c858a18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 332f8516fc00a7f945600dfe418453d25881cc03
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388098"
---
# <a name="multi-select-picklist-attributes"></a><span data-ttu-id="875ef-103">Multi-Select Picklist attributes</span><span class="sxs-lookup"><span data-stu-id="875ef-103">Multi-Select Picklist attributes</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

> [!NOTE]
> <span data-ttu-id="875ef-104">Multi-select picklist attributes were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span><span class="sxs-lookup"><span data-stu-id="875ef-104">Multi-select picklist attributes were added with the [!INCLUDE[../includes/pn-crm-9-0-0-online.md](../includes/pn-crm-9-0-0-online.md)].</span></span>
>
> <span data-ttu-id="875ef-105">Clients that do not use the current .NET assemblies need to include <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion> with a value of `9.0.0.0` or higher in order to work with <xref:Microsoft.Xrm.Sdk.Metadata.MultiSelectPicklistAttributeMetadata> attributes.</span><span class="sxs-lookup"><span data-stu-id="875ef-105">Clients that do not use the current .NET assemblies need to include <xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion> with a value of `9.0.0.0` or higher in order to work with <xref:Microsoft.Xrm.Sdk.Metadata.MultiSelectPicklistAttributeMetadata> attributes.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="875ef-106"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion>.</span><span class="sxs-lookup"><span data-stu-id="875ef-106"><xref:Microsoft.Xrm.Sdk.Client.OrganizationServiceProxy.SdkClientVersion>.</span></span>

<span data-ttu-id="875ef-107">Customizers can define an attribute that allows selection of multiple options.</span><span class="sxs-lookup"><span data-stu-id="875ef-107">Customizers can define an attribute that allows selection of multiple options.</span></span> <span data-ttu-id="875ef-108">The <xref:Microsoft.Xrm.Sdk.Metadata.MultiSelectPicklistAttributeMetadata> class defines an attribute type that inherits from the <xref:Microsoft.Xrm.Sdk.Metadata.EnumAttributeMetadata> class.</span><span class="sxs-lookup"><span data-stu-id="875ef-108">The <xref:Microsoft.Xrm.Sdk.Metadata.MultiSelectPicklistAttributeMetadata> class defines an attribute type that inherits from the <xref:Microsoft.Xrm.Sdk.Metadata.EnumAttributeMetadata> class.</span></span> <span data-ttu-id="875ef-109">Just like the <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> class, this attribute includes an <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadata> <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadata.Options> property that contains the valid options for the attribute.</span><span class="sxs-lookup"><span data-stu-id="875ef-109">Just like the <xref:Microsoft.Xrm.Sdk.Metadata.PicklistAttributeMetadata> class, this attribute includes an <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadata> <xref:Microsoft.Xrm.Sdk.Metadata.OptionSetMetadata.Options> property that contains the valid options for the attribute.</span></span> <span data-ttu-id="875ef-110">The difference is that the values you get or set are an <xref:Microsoft.Xrm.Sdk.OptionSetValueCollection> type that contains an array of integers representing the selected options.</span><span class="sxs-lookup"><span data-stu-id="875ef-110">The difference is that the values you get or set are an <xref:Microsoft.Xrm.Sdk.OptionSetValueCollection> type that contains an array of integers representing the selected options.</span></span> <span data-ttu-id="875ef-111">Formatted values for this attribute are a semi-colon separated string containing the labels of the selected options.</span><span class="sxs-lookup"><span data-stu-id="875ef-111">Formatted values for this attribute are a semi-colon separated string containing the labels of the selected options.</span></span>

<span data-ttu-id="875ef-112">With the Web API, this attribute is defined using the <xref href="Microsoft.Dynamics.CRM.MultiSelectPicklistAttributeMetadata?text=MultiSelectPicklistAttributeMetadata EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="875ef-112">With the Web API, this attribute is defined using the <xref href="Microsoft.Dynamics.CRM.MultiSelectPicklistAttributeMetadata?text=MultiSelectPicklistAttributeMetadata EntityType" />.</span></span>

<span data-ttu-id="875ef-113">Just like picklist attributes, there is technically no upper limit on the number of options that can be defined.</span><span class="sxs-lookup"><span data-stu-id="875ef-113">Just like picklist attributes, there is technically no upper limit on the number of options that can be defined.</span></span> <span data-ttu-id="875ef-114">Usability considerations should be applied as the limiting factor.</span><span class="sxs-lookup"><span data-stu-id="875ef-114">Usability considerations should be applied as the limiting factor.</span></span> <span data-ttu-id="875ef-115">However only 150 options can be selected for a single attribute.</span><span class="sxs-lookup"><span data-stu-id="875ef-115">However only 150 options can be selected for a single attribute.</span></span> <span data-ttu-id="875ef-116">Also, a default value cannot be set.</span><span class="sxs-lookup"><span data-stu-id="875ef-116">Also, a default value cannot be set.</span></span>

## <a name="setting-multi-select-picklist-values"></a><span data-ttu-id="875ef-117">Setting multi-select picklist values</span><span class="sxs-lookup"><span data-stu-id="875ef-117">Setting multi-select picklist values</span></span>

<span data-ttu-id="875ef-118">With the Web API, you set the values by passing a string containing comma separated number values as shown in the following example:</span><span class="sxs-lookup"><span data-stu-id="875ef-118">With the Web API, you set the values by passing a string containing comma separated number values as shown in the following example:</span></span>
### <a name="request"></a><span data-ttu-id="875ef-119">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="875ef-119">Request</span></span>
```http
POST [organization uri]/api/data/v9.0/contacts HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0

{
    "@odata.type": "Microsoft.Dynamics.CRM.contact",
    "firstname": "Wayne",
    "lastname": "Yarborough",
    "sample_outdooractivities": "1, 9"
}
```
### <a name="response"></a><span data-ttu-id="875ef-120">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="875ef-120">Response</span></span>
```http
HTTP/1.1 204 No Content
OData-Version: 4.0
OData-EntityId: [organization uri]/api/data/v9.0/contacts(0c67748a-b78d-e711-811c-000d3a75bdf1)
```

<span data-ttu-id="875ef-121">With the Organization service using the assemblies, use the <xref:Microsoft.Xrm.Sdk.OptionSetValueCollection> to set values for this attribute as shown in the following C# example:</span><span class="sxs-lookup"><span data-stu-id="875ef-121">With the Organization service using the assemblies, use the <xref:Microsoft.Xrm.Sdk.OptionSetValueCollection> to set values for this attribute as shown in the following C# example:</span></span>
```csharp
OptionSetValueCollection activities = new OptionSetValueCollection();
activities.Add(new OptionSetValue(1)); //Swimming
activities.Add(new OptionSetValue(9)); //Camping

Contact contact = new Contact();
contact["firstname"] = "Wayne";
contact["lastname"] = "Yarborough";
contact["sample_outdooractivities"] = activities;

_serviceProxy.Create(contact);
```

## <a name="query-data-from-multi-select-picklists"></a><span data-ttu-id="875ef-122">Query data from multi-select picklists</span><span class="sxs-lookup"><span data-stu-id="875ef-122">Query data from multi-select picklists</span></span>

<span data-ttu-id="875ef-123">Two new condition operators have been added to support querying values in multi-select option sets: `ContainValues` and `DoesNotContainValues` or the FetchXml `contain-values` and `not-contain-values` operators.</span><span class="sxs-lookup"><span data-stu-id="875ef-123">Two new condition operators have been added to support querying values in multi-select option sets: `ContainValues` and `DoesNotContainValues` or the FetchXml `contain-values` and `not-contain-values` operators.</span></span> <span data-ttu-id="875ef-124">With the Web API there are the equivilent `ContainValues` and `DoesNotContainValues` query functions.</span><span class="sxs-lookup"><span data-stu-id="875ef-124">With the Web API there are the equivilent `ContainValues` and `DoesNotContainValues` query functions.</span></span>

<span data-ttu-id="875ef-125">Other existing condition operators that can be used with this type of attribute include: `Equal`, `NotEqual`, `NotNull`, `Null`, `In` and `NotIn`.</span><span class="sxs-lookup"><span data-stu-id="875ef-125">Other existing condition operators that can be used with this type of attribute include: `Equal`, `NotEqual`, `NotNull`, `Null`, `In` and `NotIn`.</span></span> 

> [!NOTE]
> <span data-ttu-id="875ef-126">The `ContainValues` and `DoesNotContainValues` operators depend on full-text indexing to be applied on the database tables that store the multiple values.</span><span class="sxs-lookup"><span data-stu-id="875ef-126">The `ContainValues` and `DoesNotContainValues` operators depend on full-text indexing to be applied on the database tables that store the multiple values.</span></span> <span data-ttu-id="875ef-127">There is some latentcy after new records are created and the full-text index takes effect.</span><span class="sxs-lookup"><span data-stu-id="875ef-127">There is some latentcy after new records are created and the full-text index takes effect.</span></span> <span data-ttu-id="875ef-128">You may need to wait several seconds after new records are created before filters using these operators can evaluate the values.</span><span class="sxs-lookup"><span data-stu-id="875ef-128">You may need to wait several seconds after new records are created before filters using these operators can evaluate the values.</span></span>

<span data-ttu-id="875ef-129">The following examples shows the use of `ContainValues` and `not-contain-values` using `FetchXML` against the following data set on a multi-select picklist attribute named `sample_outdooractivities` on the `contact` entity.</span><span class="sxs-lookup"><span data-stu-id="875ef-129">The following examples shows the use of `ContainValues` and `not-contain-values` using `FetchXML` against the following data set on a multi-select picklist attribute named `sample_outdooractivities` on the `contact` entity.</span></span>

### <a name="multi-select-picklist-sampleoutdooractivities-options"></a><span data-ttu-id="875ef-130">Multi-select picklist `sample_outdooractivities` options:</span><span class="sxs-lookup"><span data-stu-id="875ef-130">Multi-select picklist `sample_outdooractivities` options:</span></span>

|<span data-ttu-id="875ef-131">Value</span><span class="sxs-lookup"><span data-stu-id="875ef-131">Value</span></span>|<span data-ttu-id="875ef-132">Nhãn</span><span class="sxs-lookup"><span data-stu-id="875ef-132">Label</span></span>|
|-----|-----|
|<span data-ttu-id="875ef-133">1</span><span class="sxs-lookup"><span data-stu-id="875ef-133">1</span></span>|<span data-ttu-id="875ef-134">Swimming</span><span class="sxs-lookup"><span data-stu-id="875ef-134">Swimming</span></span>|
|<span data-ttu-id="875ef-135">2</span><span class="sxs-lookup"><span data-stu-id="875ef-135">2</span></span>|<span data-ttu-id="875ef-136">Hiking</span><span class="sxs-lookup"><span data-stu-id="875ef-136">Hiking</span></span>|
|<span data-ttu-id="875ef-137">3</span><span class="sxs-lookup"><span data-stu-id="875ef-137">3</span></span>|<span data-ttu-id="875ef-138">Mountain Climbing</span><span class="sxs-lookup"><span data-stu-id="875ef-138">Mountain Climbing</span></span>|
|<span data-ttu-id="875ef-139">4</span><span class="sxs-lookup"><span data-stu-id="875ef-139">4</span></span>|<span data-ttu-id="875ef-140">Fishing</span><span class="sxs-lookup"><span data-stu-id="875ef-140">Fishing</span></span>|
|<span data-ttu-id="875ef-141">5</span><span class="sxs-lookup"><span data-stu-id="875ef-141">5</span></span>|<span data-ttu-id="875ef-142">Hunting</span><span class="sxs-lookup"><span data-stu-id="875ef-142">Hunting</span></span>|
|<span data-ttu-id="875ef-143">6</span><span class="sxs-lookup"><span data-stu-id="875ef-143">6</span></span>|<span data-ttu-id="875ef-144">Đang chạy</span><span class="sxs-lookup"><span data-stu-id="875ef-144">Running</span></span>|
|<span data-ttu-id="875ef-145">7</span><span class="sxs-lookup"><span data-stu-id="875ef-145">7</span></span>|<span data-ttu-id="875ef-146">Boating</span><span class="sxs-lookup"><span data-stu-id="875ef-146">Boating</span></span>|
|<span data-ttu-id="875ef-147">8</span><span class="sxs-lookup"><span data-stu-id="875ef-147">8</span></span>|<span data-ttu-id="875ef-148">Skiing</span><span class="sxs-lookup"><span data-stu-id="875ef-148">Skiing</span></span>|
|<span data-ttu-id="875ef-149">9</span><span class="sxs-lookup"><span data-stu-id="875ef-149">9</span></span>|<span data-ttu-id="875ef-150">Camping</span><span class="sxs-lookup"><span data-stu-id="875ef-150">Camping</span></span>|

### <a name="contact-entity-values"></a><span data-ttu-id="875ef-151">Contact entity values</span><span class="sxs-lookup"><span data-stu-id="875ef-151">Contact entity values</span></span>

|`fullname`| `sample_outdooractivities` |
|--------|-------------------|
|<span data-ttu-id="875ef-152">Wayne Yarborough</span><span class="sxs-lookup"><span data-stu-id="875ef-152">Wayne Yarborough</span></span>|<span data-ttu-id="875ef-153">1,9</span><span class="sxs-lookup"><span data-stu-id="875ef-153">1,9</span></span>|
|<span data-ttu-id="875ef-154">Monte Orton</span><span class="sxs-lookup"><span data-stu-id="875ef-154">Monte Orton</span></span>|<span data-ttu-id="875ef-155">2</span><span class="sxs-lookup"><span data-stu-id="875ef-155">2</span></span>|
|<span data-ttu-id="875ef-156">Randal Maple</span><span class="sxs-lookup"><span data-stu-id="875ef-156">Randal Maple</span></span>|<span data-ttu-id="875ef-157">4</span><span class="sxs-lookup"><span data-stu-id="875ef-157">4</span></span>|
|<span data-ttu-id="875ef-158">Hiram Mundy</span><span class="sxs-lookup"><span data-stu-id="875ef-158">Hiram Mundy</span></span>|<span data-ttu-id="875ef-159">2,3,8,9</span><span class="sxs-lookup"><span data-stu-id="875ef-159">2,3,8,9</span></span>|
|<span data-ttu-id="875ef-160">Barbara Weber</span><span class="sxs-lookup"><span data-stu-id="875ef-160">Barbara Weber</span></span>|<span data-ttu-id="875ef-161">1,4,7</span><span class="sxs-lookup"><span data-stu-id="875ef-161">1,4,7</span></span>|
|<span data-ttu-id="875ef-162">Georgette Sullivan</span><span class="sxs-lookup"><span data-stu-id="875ef-162">Georgette Sullivan</span></span>|<span data-ttu-id="875ef-163">4,5,9</span><span class="sxs-lookup"><span data-stu-id="875ef-163">4,5,9</span></span>|
|<span data-ttu-id="875ef-164">Verna Kennedy</span><span class="sxs-lookup"><span data-stu-id="875ef-164">Verna Kennedy</span></span>|<span data-ttu-id="875ef-165">2,4,9</span><span class="sxs-lookup"><span data-stu-id="875ef-165">2,4,9</span></span>|
|<span data-ttu-id="875ef-166">Marvin Bracken</span><span class="sxs-lookup"><span data-stu-id="875ef-166">Marvin Bracken</span></span>|<span data-ttu-id="875ef-167">1,2,8,9</span><span class="sxs-lookup"><span data-stu-id="875ef-167">1,2,8,9</span></span>|

### <a name="example-code-using-web-api"></a><span data-ttu-id="875ef-168">Example code using Web API</span><span class="sxs-lookup"><span data-stu-id="875ef-168">Example code using Web API</span></span>
<span data-ttu-id="875ef-169">The following example shows the use of the `ContainsValues` query function to return all the contacts who like hiking.</span><span class="sxs-lookup"><span data-stu-id="875ef-169">The following example shows the use of the `ContainsValues` query function to return all the contacts who like hiking.</span></span> <span data-ttu-id="875ef-170">Notice how the text of the options is returned as annotations due to the `odata.include-annotations="OData.Community.Display.V1.FormattedValue"` preference applied.</span><span class="sxs-lookup"><span data-stu-id="875ef-170">Notice how the text of the options is returned as annotations due to the `odata.include-annotations="OData.Community.Display.V1.FormattedValue"` preference applied.</span></span>

#### <a name="request"></a><span data-ttu-id="875ef-171">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="875ef-171">Request</span></span>
```http
GET [organization uri]/api/data/v9.0/contacts?$select=fullname,sample_outdooractivities&$filter=Microsoft.Dynamics.CRM.ContainValues(PropertyName='sample_outdooractivities',PropertyValues=%5B'2'%5D) HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Prefer: odata.include-annotations="OData.Community.Display.V1.FormattedValue"
```
#### <a name="response"></a><span data-ttu-id="875ef-172">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="875ef-172">Response</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"
Content-Length: 1092

{
    "@odata.context": "[organization uri]/api/data/v9.0/$metadata#contacts(fullname,sample_outdooractivities)",
    "value": [{
        "@odata.etag": "W/\"529811\"",
        "fullname": "Monte Orton",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Hiking",
        "sample_outdooractivities": "2",
        "contactid": "cdbcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529823\"",
        "fullname": "Hiram Mundy",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Hiking; Mountain Climbing; Skiing; Camping",
        "sample_outdooractivities": "2,3,8,9",
        "contactid": "d7bcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529838\"",
        "fullname": "Verna Kennedy",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Hiking; Fishing; Camping",
        "sample_outdooractivities": "2,4,9",
        "contactid": "e6bcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529843\"",
        "fullname": "Marvin Bracken",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Swimming; Hiking; Skiing; Camping",
        "sample_outdooractivities": "1,2,8,9",
        "contactid": "ebbcc48e-0b8d-e711-811c-000d3a75bdf1"
    }]
}
```
<span data-ttu-id="875ef-173">The following example shows the use of the `not-contain-values` operator in the following `FetchXml` query using the Web API.</span><span class="sxs-lookup"><span data-stu-id="875ef-173">The following example shows the use of the `not-contain-values` operator in the following `FetchXml` query using the Web API.</span></span>

```xml
<fetch distinct='false' no-lock='false' mapping='logical'>
    <entity name='contact'>
        <attribute name='fullname' />
        <attribute name='sample_outdooractivities' />
            <filter type='and'>
                <condition attribute='sample_outdooractivities' operator='not-contain-values'>
                    <value>2</value>
                </condition>
            </filter>
    </entity>
</fetch>
```

#### <a name="request"></a><span data-ttu-id="875ef-174">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="875ef-174">Request</span></span>
```http
GET [organization uri]/api/data/v9.0/contacts?fetchXml=%253Cfetch%2520distinct%253D'false'%2520no-lock%253D'false'%2520mapping%253D'logical'%253E%253Centity%2520name%253D'contact'%253E%253Cattribute%2520name%253D'fullname'%2520%252F%253E%253Cattribute%2520name%253D'sample_outdooractivities'%2520%252F%253E%253Cfilter%2520type%253D'and'%253E%253Ccondition%2520attribute%253D'sample_outdooractivities'%2520operator%253D'not-contain-values'%253E%253Cvalue%253E2%253C%252Fvalue%253E%253C%252Fcondition%253E%253C%252Ffilter%253E%253C%252Fentity%253E%253C%252Ffetch%253E HTTP/1.1
Accept: application/json
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Prefer: odata.include-annotations="OData.Community.Display.V1.FormattedValue"
```
#### <a name="response"></a><span data-ttu-id="875ef-175">Phản hồi</span><span class="sxs-lookup"><span data-stu-id="875ef-175">Response</span></span>
```http
HTTP/1.1 200 OK
Content-Type: application/json; odata.metadata=minimal
OData-Version: 4.0
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"

{
    "@odata.context": "[organization uri]/api/data/v9.0/$metadata#contacts(fullname,sample_outdooractivities,contactid)",
    "value": [{
        "@odata.etag": "W/\"529806\"",
        "fullname": "Wayne Yarborough",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Swimming; Camping",
        "sample_outdooractivities": "1,9",
        "contactid": "c8bcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529816\"",
        "fullname": "Randal Maple",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Fishing",
        "sample_outdooractivities": "4",
        "contactid": "d2bcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529828\"",
        "fullname": "Barbara Weber",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Swimming; Fishing; Boating",
        "sample_outdooractivities": "1,4,7",
        "contactid": "dcbcc48e-0b8d-e711-811c-000d3a75bdf1"
    }, {
        "@odata.etag": "W/\"529833\"",
        "fullname": "Georgette Sullivan",
        "sample_outdooractivities@OData.Community.Display.V1.FormattedValue": "Fishing; Hunting; Camping",
        "sample_outdooractivities": "4,5,9",
        "contactid": "e1bcc48e-0b8d-e711-811c-000d3a75bdf1"
    }]
}
```

### <a name="example-code-using-queryexpression-and-fetchexpression"></a><span data-ttu-id="875ef-176">Example code using QueryExpression and FetchExpression</span><span class="sxs-lookup"><span data-stu-id="875ef-176">Example code using QueryExpression and FetchExpression</span></span>

<span data-ttu-id="875ef-177">The following C# sample shows the use of the `ContainsValues` operator with `QueryExpression` and the `not-contain-values` using `FetchExpression` using `RetrieveMultiple` and the Organization service.</span><span class="sxs-lookup"><span data-stu-id="875ef-177">The following C# sample shows the use of the `ContainsValues` operator with `QueryExpression` and the `not-contain-values` using `FetchExpression` using `RetrieveMultiple` and the Organization service.</span></span>

```csharp
//Retrieve contacts who like hiking
//Using Query Expression
int[] hikingValue = new int[] { 2 };
ConditionExpression condition = new ConditionExpression("sample_outdooractivities", ConditionOperator.ContainValues, hikingValue);

FilterExpression filter = new FilterExpression();
filter.AddCondition(condition);

QueryExpression likesHikingQuery = new QueryExpression(Contact.EntityLogicalName);
likesHikingQuery.ColumnSet.AddColumns("fullname", "sample_outdooractivities");
likesHikingQuery.Criteria.AddFilter(filter);

EntityCollection hikers = _serviceProxy.RetrieveMultiple(likesHikingQuery);

Console.WriteLine("\nContacts who like Hiking");
Console.WriteLine("=========================");
foreach (Contact contact in hikers.Entities)
{
    string values = (contact["sample_outdooractivities"] == null) ? "null" : contact.FormattedValues["sample_outdooractivities"];
    Console.WriteLine("{0} {1}", contact.FullName, values);
}

    /*OUTPUT:
    Contacts who like Hiking
    =========================
    Monte Orton Hiking
    Hiram Mundy Hiking; Mountain Climbing; Skiing; Camping
    Verna Kennedy Hiking; Fishing; Camping
    Marvin Bracken Swimming; Hiking; Skiing; Camping
    */

//Retrieving contacts who do not like hiking:
//Using Fetch Expression
string fetchXml = @"<fetch distinct='false' no-lock='false' mapping='logical'>
                     <entity name='contact'>
                      <attribute name='fullname' />
                      <attribute name='sample_outdooractivities' />
                       <filter type='and'>
                        <condition attribute='sample_outdooractivities' operator='not-contain-values'>
                         <value>2</value>
                        </condition>
                       </filter>
                      </entity>
                     </fetch>";
FetchExpression doesNotLikeHiking = new FetchExpression(fetchXml);

EntityCollection nonHikers = _serviceProxy.RetrieveMultiple(doesNotLikeHiking);

Console.WriteLine("\nContacts who do not like Hiking");
Console.WriteLine("===============================");
foreach (Contact contact in nonHikers.Entities)
{
    string values = (contact["sample_outdooractivities"] == null) ? "null" : contact.FormattedValues["sample_outdooractivities"];
    Console.WriteLine("{0} {1}", contact.FullName, values);
}

    /* OUTPUT
    Contacts who do not like Hiking
    ===============================
    Wayne Yarborough Swimming; Camping
    Randal Maple Fishing
    Barbara Weber Swimming; Fishing; Boating
    Georgette Sullivan Fishing; Hunting; Camping 
    */
```


## <a name="create-a-multi-select-picklist-with-code"></a><span data-ttu-id="875ef-178">Create a multi-select picklist with code</span><span class="sxs-lookup"><span data-stu-id="875ef-178">Create a multi-select picklist with code</span></span>

<span data-ttu-id="875ef-179">The easiest way to create a multi-select picklist is to use the attribute editor in the customization tools.</span><span class="sxs-lookup"><span data-stu-id="875ef-179">The easiest way to create a multi-select picklist is to use the attribute editor in the customization tools.</span></span> <span data-ttu-id="875ef-180">More information [Create and edit fields](../customize/create-edit-fields.md)</span><span class="sxs-lookup"><span data-stu-id="875ef-180">More information [Create and edit fields](../customize/create-edit-fields.md)</span></span>

<span data-ttu-id="875ef-181">But if you need to automate creation of this kind of attribute you can use C# code like the following with the organization service which creates a multi-select picklist to allow choices of outdoor activities to the `contact` entity.</span><span class="sxs-lookup"><span data-stu-id="875ef-181">But if you need to automate creation of this kind of attribute you can use C# code like the following with the organization service which creates a multi-select picklist to allow choices of outdoor activities to the `contact` entity.</span></span> <span data-ttu-id="875ef-182">More information [Create attributes](org-service/work-attribute-metadata.md#create-attributes)</span><span class="sxs-lookup"><span data-stu-id="875ef-182">More information [Create attributes](org-service/work-attribute-metadata.md#create-attributes)</span></span>

```csharp
    private const int _languageCode = 1033; //English

    MultiSelectPicklistAttributeMetadata outDoorActivitiesAttribute = new MultiSelectPicklistAttributeMetadata()
    {
    SchemaName = "sample_OutdoorActivities",
    LogicalName = "sample_outdooractivities",
    DisplayName = new Label("Outdoor activities", _languageCode),
    RequiredLevel = new AttributeRequiredLevelManagedProperty(AttributeRequiredLevel.None),
    Description = new Label("Outdoor activities that the contact likes.", _languageCode),
    OptionSet = new OptionSetMetadata()
        {
            IsGlobal = false,
            OptionSetType = OptionSetType.Picklist,
            Options = {
                new OptionMetadata(new Label("Swimming",_languageCode),1),
                new OptionMetadata(new Label("Hiking",_languageCode),2),
                new OptionMetadata(new Label("Mountain Climbing",_languageCode),3),
                new OptionMetadata(new Label("Fishing",_languageCode),4),
                new OptionMetadata(new Label("Hunting",_languageCode),5),
                new OptionMetadata(new Label("Running",_languageCode),6),
                new OptionMetadata(new Label("Boating",_languageCode),7),
                new OptionMetadata(new Label("Skiing",_languageCode),8),
                new OptionMetadata(new Label("Camping",_languageCode),9)}
        }
    };

    CreateAttributeRequest createAttributeRequest = new CreateAttributeRequest
    {
        EntityName = Contact.EntityLogicalName,
        Attribute = outDoorActivitiesAttribute
    };
```

### <a name="see-also"></a><span data-ttu-id="875ef-183">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="875ef-183">See also</span></span>
[<span data-ttu-id="875ef-184">Introduction to entity attributes</span><span class="sxs-lookup"><span data-stu-id="875ef-184">Introduction to entity attributes</span></span>](introduction-entity-attributes.md)<br />
[<span data-ttu-id="875ef-185">Create an entity using the Web API</span><span class="sxs-lookup"><span data-stu-id="875ef-185">Create an entity using the Web API</span></span>](webapi/create-entity-web-api.md)<br />
[<span data-ttu-id="875ef-186">Query Data using the Web API</span><span class="sxs-lookup"><span data-stu-id="875ef-186">Query Data using the Web API</span></span>](webapi/query-data-web-api.md)<br />
[<span data-ttu-id="875ef-187">Work with attribute metadata</span><span class="sxs-lookup"><span data-stu-id="875ef-187">Work with attribute metadata</span></span>](org-service/work-attribute-metadata.md)<br />
[<span data-ttu-id="875ef-188">Sample: Work with attribute metadata</span><span class="sxs-lookup"><span data-stu-id="875ef-188">Sample: Work with attribute metadata</span></span>](org-service/sample-work-attribute-metadata.md)<br />
[<span data-ttu-id="875ef-189">Use the early-bound entity classes for create, update, and delete</span><span class="sxs-lookup"><span data-stu-id="875ef-189">Use the early-bound entity classes for create, update, and delete</span></span>](org-service/use-early-bound-entity-classes-create-update-delete.md)
