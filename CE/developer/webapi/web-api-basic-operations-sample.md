---
title: Web API Basic Operations Sample (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This group of sample demonstrates how to perform CRUD (Create, Retrieve, Update and Delete) operations using the Web API. These are implemented using Client-side JavaScript and C#
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f006f88c-74cb-4fde-90e5-e1faf2051673
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1cb6be1e0c1a387df28b013e27314fa6e87b91fd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385914"
---
# <a name="web-api-basic-operations-sample"></a><span data-ttu-id="d9ebb-104">Web API Basic Operations Sample</span><span class="sxs-lookup"><span data-stu-id="d9ebb-104">Web API Basic Operations Sample</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="d9ebb-105">This group of samples demonstrate how to perform basic CRUD (Create, Retrieve, Update, and Delete) and associative operations using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-105">This group of samples demonstrate how to perform basic CRUD (Create, Retrieve, Update, and Delete) and associative operations using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span></span>  
  
-   [<span data-ttu-id="d9ebb-106">Web API Basic Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-106">Web API Basic Operations Sample (C#)</span></span>](web-api-basic-operations-sample-csharp.md)  
  
  
  
 <span data-ttu-id="d9ebb-107">This topic describes a common set of operations implemented by each sample in this group.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-107">This topic describes a common set of operations implemented by each sample in this group.</span></span> <span data-ttu-id="d9ebb-108">This topic describes the HTTP requests and responses and text output that each sample in this group will perform without the language specific details.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-108">This topic describes the HTTP requests and responses and text output that each sample in this group will perform without the language specific details.</span></span> <span data-ttu-id="d9ebb-109">See the language specific descriptions and the individual samples for details about how these operations are performed.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-109">See the language specific descriptions and the individual samples for details about how these operations are performed.</span></span>  
  
<a name="bkmk_demonstrates"></a>  
 
## <a name="demonstrates"></a><span data-ttu-id="d9ebb-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d9ebb-110">Demonstrates</span></span>  

 <span data-ttu-id="d9ebb-111">This sample is divided into the following sections, containing [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations which are discussed in greater detail in the specified associated conceptual topics.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-111">This sample is divided into the following sections, containing [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations which are discussed in greater detail in the specified associated conceptual topics.</span></span>  
  
|<span data-ttu-id="d9ebb-112">Code section</span><span class="sxs-lookup"><span data-stu-id="d9ebb-112">Code section</span></span>|<span data-ttu-id="d9ebb-113">Associated conceptual topics</span><span class="sxs-lookup"><span data-stu-id="d9ebb-113">Associated conceptual topics</span></span>|  
|------------------|----------------------------------|  
|[<span data-ttu-id="d9ebb-114">Section 1: Basic create and update operations</span><span class="sxs-lookup"><span data-stu-id="d9ebb-114">Section 1: Basic create and update operations</span></span>](#bkmk_section1)|[<span data-ttu-id="d9ebb-115">Basic create</span><span class="sxs-lookup"><span data-stu-id="d9ebb-115">Basic create</span></span>](create-entity-web-api.md#bkmk_basicCreate) <br /> [<span data-ttu-id="d9ebb-116">Create with data returned</span><span class="sxs-lookup"><span data-stu-id="d9ebb-116">Create with data returned</span></span>](create-entity-web-api.md#bkmk_createWithDataReturned) <br /> [<span data-ttu-id="d9ebb-117">Basic update</span><span class="sxs-lookup"><span data-stu-id="d9ebb-117">Basic update</span></span>](update-delete-entities-using-web-api.md#bkmk_update) <br /> [<span data-ttu-id="d9ebb-118">Update with data returned</span><span class="sxs-lookup"><span data-stu-id="d9ebb-118">Update with data returned</span></span>](update-delete-entities-using-web-api.md#bkmk_updateWithDataReturned)|  
|[<span data-ttu-id="d9ebb-119">Section 2: Create with association</span><span class="sxs-lookup"><span data-stu-id="d9ebb-119">Section 2: Create with association</span></span>](#bkmk_section2)|[<span data-ttu-id="d9ebb-120">Associate entities on create</span><span class="sxs-lookup"><span data-stu-id="d9ebb-120">Associate entities on create</span></span>](associate-disassociate-entities-using-web-api.md#bkmk_Associateentitiesoncreate)|  
|[<span data-ttu-id="d9ebb-121">Section 3: Create related entities (deep insert)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-121">Section 3: Create related entities (deep insert)</span></span>](#bkmk_section3)|[<span data-ttu-id="d9ebb-122">Create related entities in one operation</span><span class="sxs-lookup"><span data-stu-id="d9ebb-122">Create related entities in one operation</span></span>](create-entity-web-api.md#bkmk_CreateRelated)|  
|[<span data-ttu-id="d9ebb-123">Section 4: Associate and disassociate existing entities</span><span class="sxs-lookup"><span data-stu-id="d9ebb-123">Section 4: Associate and disassociate existing entities</span></span>](#bkmk_section4)|[<span data-ttu-id="d9ebb-124">Associate and disassociate entities using the Web API</span><span class="sxs-lookup"><span data-stu-id="d9ebb-124">Associate and disassociate entities using the Web API</span></span>](associate-disassociate-entities-using-web-api.md)|  
|[<span data-ttu-id="d9ebb-125">Section 5: Delete entities (sample cleanup)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-125">Section 5: Delete entities (sample cleanup)</span></span>](#bkmk_section5)|[<span data-ttu-id="d9ebb-126">Basic delete</span><span class="sxs-lookup"><span data-stu-id="d9ebb-126">Basic delete</span></span>](update-delete-entities-using-web-api.md#bkmk_delete)|  
  
> [!NOTE]
>  <span data-ttu-id="d9ebb-127">For brevity, less pertinent HTTP headers have been omitted.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-127">For brevity, less pertinent HTTP headers have been omitted.</span></span> <span data-ttu-id="d9ebb-128">The URLs of the records will vary with the base organization address and the ID of the record assigned by your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-128">The URLs of the records will vary with the base organization address and the ID of the record assigned by your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server.</span></span>  
  
<a name="bkmk_section1"></a>
   
## <a name="section-1-basic-create-and-update-operations"></a><span data-ttu-id="d9ebb-129">Section 1: Basic create and update operations</span><span class="sxs-lookup"><span data-stu-id="d9ebb-129">Section 1: Basic create and update operations</span></span> 
 
 <span data-ttu-id="d9ebb-130">This section creates a single contact then performs a series of updates upon that instance.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-130">This section creates a single contact then performs a series of updates upon that instance.</span></span> <span data-ttu-id="d9ebb-131">Note that the response header [OData-EntityId](http://docs.oasis-open.org/odata/odata/v4.0/os/part1-protocol/odata-v4.0-os-part1-protocol.html#_Toc372793637) contains the URL to this newly created record (entity instance), which parenthetically includes the unique ID for this record.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-131">Note that the response header [OData-EntityId](http://docs.oasis-open.org/odata/odata/v4.0/os/part1-protocol/odata-v4.0-os-part1-protocol.html#_Toc372793637) contains the URL to this newly created record (entity instance), which parenthetically includes the unique ID for this record.</span></span>  
  
1. <span data-ttu-id="d9ebb-132">Create a new contact, named  Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-132">Create a new contact, named  Peter Cambel.</span></span>  
  
   <span data-ttu-id="d9ebb-133">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-133">**Request**</span></span> 
  
   ```http
   POST http://[Organization URI]/api/data/v9.0/contacts HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "firstname": "Peter",  
     "lastname": "Cambel"  
   }  
   ```  
  
   <span data-ttu-id="d9ebb-134">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-134">**Response**</span></span>  
  
   ```http  
   HTTP/1.1 204 No Content  
   OData-Version: 4.0  
   OData-EntityId: http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)  
   ```  
  
   <span data-ttu-id="d9ebb-135">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-135">**Console output**</span></span>  
  
   ```  
   Contact 'Peter Cambel' created.  
   ```  
  
    <span data-ttu-id="d9ebb-136">The properties available for each type are defined within the metadata document and are also documented for each type in the <xref:Microsoft.Dynamics.CRM.EntityTypeIndex> section.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-136">The properties available for each type are defined within the metadata document and are also documented for each type in the <xref:Microsoft.Dynamics.CRM.EntityTypeIndex> section.</span></span> <span data-ttu-id="d9ebb-137">For more general information, see [Web API types and operations](web-api-types-operations.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-137">For more general information, see [Web API types and operations](web-api-types-operations.md).</span></span>  
  
2. <span data-ttu-id="d9ebb-138">Update the contact with values for annual income ($80,000)  and job title (Junior Developer).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-138">Update the contact with values for annual income ($80,000)  and job title (Junior Developer).</span></span>  
  
   <span data-ttu-id="d9ebb-139">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-139">**Request**</span></span> 
  
   ```http  
   PATCH http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "annualincome": 80000,  
     "jobtitle": "Junior Developer"  
   }  
   ```  
  
   <span data-ttu-id="d9ebb-140">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-140">**Response**</span></span>  
  
   ```http  
   HTTP/1.1 204 No Content  
   ```  
  
   <span data-ttu-id="d9ebb-141">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-141">**Console output**</span></span>  
  
   ```  
   Contact 'Peter Cambel' updated with job title and annual income.  
   ```  
  
3. <span data-ttu-id="d9ebb-142">Retrieve the contact with its set of explicitly initialized properties.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-142">Retrieve the contact with its set of explicitly initialized properties.</span></span>  <span data-ttu-id="d9ebb-143">The `fullname` is a read-only property that is calculated from the `firstname` and `lastname` properties, which were explicitly initialized when the instance was created.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-143">The `fullname` is a read-only property that is calculated from the `firstname` and `lastname` properties, which were explicitly initialized when the instance was created.</span></span> <span data-ttu-id="d9ebb-144">In contrast, the `description` property was not explicitly initialized, so it retains its default value, a `null` string.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-144">In contrast, the `description` property was not explicitly initialized, so it retains its default value, a `null` string.</span></span>  
  
    <span data-ttu-id="d9ebb-145">Note that the response, in addition to the requested values and typical headers, also automatically returns the following types of additional information:</span><span class="sxs-lookup"><span data-stu-id="d9ebb-145">Note that the response, in addition to the requested values and typical headers, also automatically returns the following types of additional information:</span></span>  
  
   -   <span data-ttu-id="d9ebb-146">The primary ID for the current entity type, here `contactid`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-146">The primary ID for the current entity type, here `contactid`.</span></span>  
  
   -   <span data-ttu-id="d9ebb-147">An *ETag* value, denoted by the `@odata.etag` key, which identifies the specific version of the resource requested.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-147">An *ETag* value, denoted by the `@odata.etag` key, which identifies the specific version of the resource requested.</span></span> <span data-ttu-id="d9ebb-148">For more information, see [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-148">For more information, see [Perform conditional operations using the Web API](perform-conditional-operations-using-web-api.md).</span></span>  
  
   -   <span data-ttu-id="d9ebb-149">The metadata context, denoted by the  `@odata.context` key, provides a way to compare query results to determine if they came from the same query.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-149">The metadata context, denoted by the  `@odata.context` key, provides a way to compare query results to determine if they came from the same query.</span></span>  
  
   -   <span data-ttu-id="d9ebb-150">A `_transactioncurrencyid_value` that indicates the local currency of the monetary  transaction.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-150">A `_transactioncurrencyid_value` that indicates the local currency of the monetary  transaction.</span></span>  
  
   <span data-ttu-id="d9ebb-151">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-151">**Request**</span></span> 
  
   ```http  
   GET http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)?$select=fullname,annualincome,jobtitle,description HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   ```  
  
   <span data-ttu-id="d9ebb-152">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-152">**Response**</span></span>  
  
   ```http
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,annualincome,jobtitle,description)/$entity",  
      "@odata.etag":"W/\"628883\"",  
      "fullname":"Peter Cambel",  
      "annualincome":80000.0000,  
      "jobtitle":"Junior Developer",  
      "description":null,  
      "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03",  
      "contactid":"60f77a42-5f0e-e611-80e0-00155da84c03"  
   }  
   ```  
  
   <span data-ttu-id="d9ebb-153">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-153">**Console output**</span></span>  
  
   ```http    
   Contact 'Peter Cambel' retrieved:  
           Income: 80000  
           Job title: Junior Developer  
           Description: .    
   ```  
  
   > [!IMPORTANT]
   >  <span data-ttu-id="d9ebb-154">You should always use selection and filtering in retrieval operations to optimize performance.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-154">You should always use selection and filtering in retrieval operations to optimize performance.</span></span> <span data-ttu-id="d9ebb-155">For more information, see [Query Data using the Web API](query-data-web-api.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-155">For more information, see [Query Data using the Web API](query-data-web-api.md).</span></span>  
  
4. <span data-ttu-id="d9ebb-156">Update the contact entity instance by supplying new values to these same properties.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-156">Update the contact entity instance by supplying new values to these same properties.</span></span>  
  
   <span data-ttu-id="d9ebb-157">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-157">**Request**</span></span> 
  
   ```http
   PATCH http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "jobtitle": "Senior Developer",  
     "annualincome": 95000,  
     "description": "Assignment to-be-determined"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-158">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-158">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
   <span data-ttu-id="d9ebb-159">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-159">**Console output**</span></span>  
  
   ```http    
   Contact 'Peter Cambel' updated:  
           Job title: Senior Developer  
           Annual income: 95000  
           Description: Assignment to-be-determined    
   ```  
  
   > [!IMPORTANT]
   >  <span data-ttu-id="d9ebb-160">Only send changed properties in update requests.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-160">Only send changed properties in update requests.</span></span> <span data-ttu-id="d9ebb-161">For more information, see [Basic update](update-delete-entities-using-web-api.md#bkmk_update).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-161">For more information, see [Basic update](update-delete-entities-using-web-api.md#bkmk_update).</span></span>  
  
5. <span data-ttu-id="d9ebb-162">Explicitly set a single property, the primary phone number.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-162">Explicitly set a single property, the primary phone number.</span></span> <span data-ttu-id="d9ebb-163">Note this is a `PUT` request and that the JSON key named `value` is used when performing operations on individual properties.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-163">Note this is a `PUT` request and that the JSON key named `value` is used when performing operations on individual properties.</span></span>  
  
   <span data-ttu-id="d9ebb-164">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-164">**Request**</span></span> 
  
   ```http  
   PUT http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)/telephone1 HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "value": "555-0105"  
   }  
   ```  
  
   <span data-ttu-id="d9ebb-165">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-165">**Response**</span></span>  
  
   ```http  
   HTTP/1.1 204 No Content  
   ```  
  
   <span data-ttu-id="d9ebb-166">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-166">**Console output**</span></span>  
  
   ```  
   Contact 'Peter Cambel' phone number updated.  
   ```  
  
6. <span data-ttu-id="d9ebb-167">Retrieve that same single property, the primary phone number.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-167">Retrieve that same single property, the primary phone number.</span></span> <span data-ttu-id="d9ebb-168">Again note the use of the key named `value`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-168">Again note the use of the key named `value`.</span></span>  
  
   <span data-ttu-id="d9ebb-169">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-169">**Request**</span></span> 
  
   ```http  
   GET http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)/telephone1 HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   ```  
  
   <span data-ttu-id="d9ebb-170">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-170">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(60f77a42-5f0e-e611-80e0-00155da84c03)/telephone1",  
      "value":"555-0105"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-171">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-171">**Console output**</span></span>  
  
   ```  
   Contact's telephone# is: 555-0105.  
   ```  
  
7. <span data-ttu-id="d9ebb-172">Create a similar contact but also return instance information in the same operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-172">Create a similar contact but also return instance information in the same operation.</span></span> <span data-ttu-id="d9ebb-173">This latter capability is enabled by the `Prefer: return=representation` header.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-173">This latter capability is enabled by the `Prefer: return=representation` header.</span></span> <span data-ttu-id="d9ebb-174">This capability was introduced with the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)] and requires version 8.2 or higher.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-174">This capability was introduced with the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)] and requires version 8.2 or higher.</span></span>  
  
   <span data-ttu-id="d9ebb-175">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-175">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,annualincome,jobtitle,contactid HTTP/1.1  
   OData-Version: 4.0  
   Content-Type: application/json; charset=utf-8  
   Prefer: return=representation  
   {  
     "firstname": "Peter_Alt",  
     "lastname": "Cambel",  
     "jobtitle": "Junior Developer",  
     "annualincome": 80000,  
     "telephone1": "555-0110"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-176">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-176">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 201 Created  
   Content-Type: application/json; odata.metadata=minimal  
   Preference-Applied: return=representation  
   OData-Version: 4.0  
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts/$entity","@odata.etag":"W/\"758870\"","_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03","annualincome":80000.0000,"contactid":"199250b7-6cbe-e611-80f7-00155da84c08","jobtitle":"Junior Developer","fullname":"Peter_Alt Cambel"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-177">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-177">**Console output**</span></span>  
  
   ```    
   Contact 'Peter_Alt Cambel' created:  
           Annual income: 80000  
           Job title: Junior Developer  
   Contact URI: http://[Organization URI]/api/data/v9.0/contacts(199250b7-6cbe-e611-80f7-00155da84c08)  
   ```  
  
8. <span data-ttu-id="d9ebb-178">Update this similar contact and also return instance information in the same operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-178">Update this similar contact and also return instance information in the same operation.</span></span> <span data-ttu-id="d9ebb-179">Again, this capability is enabled by the `Prefer: return=representation` header.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-179">Again, this capability is enabled by the `Prefer: return=representation` header.</span></span> <span data-ttu-id="d9ebb-180">This capability was introduced with the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)] and requires version 8.2 or higher.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-180">This capability was introduced with the [!INCLUDE[pn_crm_8_2_0_both](../../includes/pn-crm-8-2-0-both.md)] and requires version 8.2 or higher.</span></span>  
  
   <span data-ttu-id="d9ebb-181">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-181">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,annualincome,jobtitle,contactid HTTP/1.1  
   OData-Version: 4.0  
   Content-Type: application/json; charset=utf-8  
   Prefer: return=representation  
   {  
     "firstname": "Peter_Alt",  
     "lastname": "Cambel",  
     "jobtitle": "Junior Developer",  
     "annualincome": 80000,  
     "telephone1": "555-0110"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-182">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-182">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 201 Created  
   Content-Type: application/json; odata.metadata=minimal  
   Preference-Applied: return=representation  
   OData-Version: 4.0  
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts/$entity","@odata.etag":"W/\"758870\"","_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03","annualincome":80000.0000,"contactid":"199250b7-6cbe-e611-80f7-00155da84c08","jobtitle":"Junior Developer","fullname":"Peter_Alt Cambel"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-183">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-183">**Console output**</span></span>  
  
   ```    
   Contact 'Peter_Alt Cambel' updated:  
           Annual income: 95000  
           Job title: Senior Developer   
   ```  
  
<a name="bkmk_section2"></a>  
 
## <a name="section-2-create-with-association"></a><span data-ttu-id="d9ebb-184">Section 2: Create with association</span><span class="sxs-lookup"><span data-stu-id="d9ebb-184">Section 2: Create with association</span></span> 
 
 <span data-ttu-id="d9ebb-185">This section creates a new account instance named `Contoso, Ltd.` and associates it to an existing contact, `Peter Cambel`, which was created in [Section 1](#bkmk_section1).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-185">This section creates a new account instance named `Contoso, Ltd.` and associates it to an existing contact, `Peter Cambel`, which was created in [Section 1](#bkmk_section1).</span></span>  <span data-ttu-id="d9ebb-186">This creation and association is performed in a single POST operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-186">This creation and association is performed in a single POST operation.</span></span>  
  
1. <span data-ttu-id="d9ebb-187">Create the Contoso, Ltd. account and set its primary contact attribute to the existing contact Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-187">Create the Contoso, Ltd. account and set its primary contact attribute to the existing contact Peter Cambel.</span></span>  <span data-ttu-id="d9ebb-188">The `@odata.bind` annotation indicates that an association is being created, here binding the `primarycontactid` single-valued navigation property to an existing contact, Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-188">The `@odata.bind` annotation indicates that an association is being created, here binding the `primarycontactid` single-valued navigation property to an existing contact, Peter Cambel.</span></span>  
  
   <span data-ttu-id="d9ebb-189">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-189">**Request**</span></span> 
  
   ```http  
   POST http://[Organization URI]/api/data/v9.0/accounts HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "name": "Contoso Inc",  
     "telephone1": "555-5555",  
     "primarycontactid@odata.bind": "http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-190">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-190">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content  
   OData-Version: 4.0  
   OData-EntityId: http://[Organization URI]/api/data/v9.0/accounts(65f77a42-5f0e-e611-80e0-00155da84c03)    
   ```  
  
   <span data-ttu-id="d9ebb-191">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-191">**Console output**</span></span>  
  
   ```  
   Account 'Contoso Inc' created.  
   ```  
  
2. <span data-ttu-id="d9ebb-192">Retrieve the primary contact for the account Contoso, Ltd., again using `$expand`  with the  `primarycontactid` single-valued navigation property to access the associated <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> record.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-192">Retrieve the primary contact for the account Contoso, Ltd., again using `$expand`  with the  `primarycontactid` single-valued navigation property to access the associated <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" /> record.</span></span>  
  
   <span data-ttu-id="d9ebb-193">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-193">**Request**</span></span> 
  
   ```http    
   GET http://[Organization URI]/api/data/v9.0/accounts(65f77a42-5f0e-e611-80e0-00155da84c03)?$select=name,&$expand=primarycontactid($select=fullname,jobtitle,annualincome) HTTP/1.1  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0   
   ```  
  
   <span data-ttu-id="d9ebb-194">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-194">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0  
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,primarycontactid(fullname,jobtitle,annualincome))/$entity",  
      "@odata.etag":"W/\"628886\"",  
      "name":"Contoso Inc",  
      "accountid":"65f77a42-5f0e-e611-80e0-00155da84c03",  
      "primarycontactid":{   
         "@odata.etag":"W/\"628885\"",  
         "fullname":"Peter Cambel",  
         "jobtitle":"Senior Developer",  
         "annualincome":95000.0000,  
         "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03",  
         "contactid":"60f77a42-5f0e-e611-80e0-00155da84c03"  
      }  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-195">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-195">**Console output**</span></span>  
  
   ```    
   Account 'Contoso Inc' has primary contact 'Peter Cambel':  
        Job title: Senior Developer  
        Income: 95000    
   ```  
  
<a name="bkmk_section3"></a>  
 
## <a name="section-3-create-related-entities-deep-insert"></a><span data-ttu-id="d9ebb-196">Section 3: Create related entities (deep insert)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-196">Section 3: Create related entities (deep insert)</span></span>  

 <span data-ttu-id="d9ebb-197">This section demonstrates how to create an entity instance and related entity instances, in a single POST request.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-197">This section demonstrates how to create an entity instance and related entity instances, in a single POST request.</span></span> <span data-ttu-id="d9ebb-198">Using this method, all instances are newly created; there are no existing instances to associate with.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-198">Using this method, all instances are newly created; there are no existing instances to associate with.</span></span> <span data-ttu-id="d9ebb-199">This approach has two advantages.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-199">This approach has two advantages.</span></span> <span data-ttu-id="d9ebb-200">It is more efficient, replacing multiple simpler creation and association operations with one combined operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-200">It is more efficient, replacing multiple simpler creation and association operations with one combined operation.</span></span> <span data-ttu-id="d9ebb-201">Also, it is [atomic](https://msdn.microsoft.com/library/aa719484\(v=vs.71\).aspx), where either the entire operation succeeds and all the related objects are created, or the operation fails and none are created.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-201">Also, it is [atomic](https://msdn.microsoft.com/library/aa719484\(v=vs.71\).aspx), where either the entire operation succeeds and all the related objects are created, or the operation fails and none are created.</span></span>  
  
 <span data-ttu-id="d9ebb-202">This section creates an account, its primary contact, and a set of tasks for that contact in one request.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-202">This section creates an account, its primary contact, and a set of tasks for that contact in one request.</span></span>  
  
1. <span data-ttu-id="d9ebb-203">Create the account `Fourth Coffee` and its primary contact `Susie Curtis` and her three related tasks in one operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-203">Create the account `Fourth Coffee` and its primary contact `Susie Curtis` and her three related tasks in one operation.</span></span>  <span data-ttu-id="d9ebb-204">Note the use of the single-valued `primarycontactid` navigation property and the collection-valued navigation property `Contact_Tasks` to define these relationships, respectively.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-204">Note the use of the single-valued `primarycontactid` navigation property and the collection-valued navigation property `Contact_Tasks` to define these relationships, respectively.</span></span>  <span data-ttu-id="d9ebb-205">Single-valued navigational properties take an object value, whereas collection-valued navigation properties take an array value.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-205">Single-valued navigational properties take an object value, whereas collection-valued navigation properties take an array value.</span></span>  
  
   <span data-ttu-id="d9ebb-206">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-206">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/accounts HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "name": "Fourth Coffee",  
     "primarycontactid": {  
       "firstname": "Susie",  
       "lastname": "Curtis",  
       "jobtitle": "Coffee Master",  
       "annualincome": 48000,  
       "Contact_Tasks": [  
         {  
           "subject": "Sign invoice",  
           "description": "Invoice #12321",  
           "scheduledend": "2016-04-19T00:00:00-07:00"  
         },  
         {  
           "subject": "Setup new display",  
           "description": "Theme is - Spring is in the air",  
           "scheduledstart": "2016-04-20T00:00:00-07:00"  
         },  
         {  
           "subject": "Conduct training",  
           "description": "Train team on making our new blended coffee",  
           "scheduledstart": "2016-06-01T00:00:00-07:00"  
         }  
       ]  
     }  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-207">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-207">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content  
   OData-Version: 4.0  
   OData-EntityId: http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03)    
   ```  
  
   <span data-ttu-id="d9ebb-208">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-208">**Console output**</span></span>  
  
   ```  
   Account 'Fourth Coffee' created.  
   ```  
  
2. <span data-ttu-id="d9ebb-209">Selectively retrieve the newly created Fourth Coffee account and its primary contact.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-209">Selectively retrieve the newly created Fourth Coffee account and its primary contact.</span></span>  <span data-ttu-id="d9ebb-210">An expansion is performed on the single-valued navigation property `primarycontactid`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-210">An expansion is performed on the single-valued navigation property `primarycontactid`.</span></span>  
  
   <span data-ttu-id="d9ebb-211">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-211">**Request**</span></span> 
  
   ```http    
   GET http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03)?$select=name,&$expand=primarycontactid($select=fullname,jobtitle,annualincome) HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-212">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-212">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0   
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,primarycontactid(fullname,jobtitle,annualincome))/$entity",  
      "@odata.etag":"W/\"628902\"",  
      "name":"Fourth Coffee",  
      "accountid":"6af77a42-5f0e-e611-80e0-00155da84c03",  
      "primarycontactid":{   
         "@odata.etag":"W/\"628892\"",  
         "fullname":"Susie Curtis",  
         "jobtitle":"Coffee Master",  
         "annualincome":48000.0000,  
         "_transactioncurrencyid_value":"0d4ed62e-95f7-e511-80d1-00155da84c03",  
         "contactid":"6bf77a42-5f0e-e611-80e0-00155da84c03"  
      }  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-213">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-213">**Console output**</span></span>  
  
   ```    
   Account 'Fourth Coffee' has primary contact 'Susie Curtis':  
           Job title: Coffee Master  
           Income: 48000    
   ```  
  
3. <span data-ttu-id="d9ebb-214">Selectively retrieve the tasks associated with the primary contact retrieved in the previous operation.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-214">Selectively retrieve the tasks associated with the primary contact retrieved in the previous operation.</span></span>  <span data-ttu-id="d9ebb-215">An expansion is performed on the collection-valued navigation property `Contact_Tasks`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-215">An expansion is performed on the collection-valued navigation property `Contact_Tasks`.</span></span>  
  
   <span data-ttu-id="d9ebb-216">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-216">**Request**</span></span> 
  
   ```http    
   GET http://[Organization URI]/api/data/v9.0/contacts(6bf77a42-5f0e-e611-80e0-00155da84c03)?$select=fullname,&$expand=Contact_Tasks($select=subject,description,scheduledstart,scheduledend) HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-217">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-217">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0   
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,Contact_Tasks,Contact_Tasks(subject,description,scheduledstart,scheduledend))/$entity",  
      "@odata.etag":"W/\"628892\"",  
      "fullname":"Susie Curtis",  
      "contactid":"6bf77a42-5f0e-e611-80e0-00155da84c03",  
      "Contact_Tasks":[   
         {   
            "@odata.etag":"W/\"628903\"",  
            "subject":"Sign invoice",  
            "description":"Invoice #12321",  
            "scheduledstart":"2016-04-19T00:00:00Z",  
            "scheduledend":"2016-04-19T00:00:00Z",  
            "activityid":"6cf77a42-5f0e-e611-80e0-00155da84c03"  
         },  
         {   
            "@odata.etag":"W/\"628905\"",  
            "subject":"Setup new display",  
            "description":"Theme is - Spring is in the air",  
            "scheduledstart":"2016-04-20T00:00:00Z",  
            "scheduledend":"2016-04-20T00:00:00Z",  
            "activityid":"6df77a42-5f0e-e611-80e0-00155da84c03"  
         },  
         {   
            "@odata.etag":"W/\"628907\"",  
            "subject":"Conduct training",  
            "description":"Train team on making our new blended coffee",  
            "scheduledstart":"2016-06-01T00:00:00Z",  
            "scheduledend":"2016-06-01T00:00:00Z",  
            "activityid":"6ef77a42-5f0e-e611-80e0-00155da84c03"  
         }  
      ]  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-218">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-218">**Console output**</span></span>  
  
   ```    
   Contact 'Susie Curtis' has the following assigned tasks:  
   Subject: Sign invoice,  
           Description: Invoice #12321  
           Start: 4/19/2016  
           End: 4/19/2016  
  
   Subject: Setup new display,  
           Description: Theme is - Spring is in the air  
           Start: 4/20/2016  
           End: 4/20/2016  
  
   Subject: Conduct training  
           Description: Train team on making our new blended coffee,  
           Start: 6/1/2016  
           End: 6/1/2016    
   ```  
  
<a name="bkmk_section4"></a>
   
## <a name="section-4-associate-and-disassociate-existing-entities"></a><span data-ttu-id="d9ebb-219">Section 4: Associate and disassociate existing entities</span><span class="sxs-lookup"><span data-stu-id="d9ebb-219">Section 4: Associate and disassociate existing entities</span></span>  

 <span data-ttu-id="d9ebb-220">This section demonstrates how to associate and disassociate existing entity instances.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-220">This section demonstrates how to associate and disassociate existing entity instances.</span></span> <span data-ttu-id="d9ebb-221">Forming an association requires the use of a reference URI and relationship object, which are then sent in a POST request.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-221">Forming an association requires the use of a reference URI and relationship object, which are then sent in a POST request.</span></span> <span data-ttu-id="d9ebb-222">Disassociating requires sending a DELETE request to the reference URI for that association.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-222">Disassociating requires sending a DELETE request to the reference URI for that association.</span></span>  <span data-ttu-id="d9ebb-223">First a one-to-many association is formed between a contact and an account.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-223">First a one-to-many association is formed between a contact and an account.</span></span>  <span data-ttu-id="d9ebb-224">Then a many-to-many association is formed between a competitor and one or more opportunities.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-224">Then a many-to-many association is formed between a competitor and one or more opportunities.</span></span>  
  
1. <span data-ttu-id="d9ebb-225">Add Peter Cambel as a contact to the account Fourth Coffee using the `contact_customer_accounts` collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-225">Add Peter Cambel as a contact to the account Fourth Coffee using the `contact_customer_accounts` collection-valued navigation property.</span></span> <span data-ttu-id="d9ebb-226">Note the use of the special key `@odata.id` to specify the associated record.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-226">Note the use of the special key `@odata.id` to specify the associated record.</span></span>  
  
   <span data-ttu-id="d9ebb-227">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-227">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03)/contact_customer_accounts/$ref HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "@odata.id": "http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03)"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-228">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-228">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
   <span data-ttu-id="d9ebb-229">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-229">**Console output**</span></span>  
  
   ```  
   Contact 'Peter Cambel' associated to account 'Fourth Coffee'.  
   ```  
  
2. <span data-ttu-id="d9ebb-230">Confirm the previous operation by retrieving the collection of contacts for the account Fourth Coffee.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-230">Confirm the previous operation by retrieving the collection of contacts for the account Fourth Coffee.</span></span> <span data-ttu-id="d9ebb-231">The response contains the array with a single element, the recently assigned contact Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-231">The response contains the array with a single element, the recently assigned contact Peter Cambel.</span></span>  
  
   <span data-ttu-id="d9ebb-232">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-232">**Request**</span></span> 
  
   ```http    
   GET http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03)/contact_customer_accounts?$select=fullname,jobtitle HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-233">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-233">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   Content-Type: application/json; odata.metadata=minimal  
   OData-Version: 4.0   
   {  
     "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle)","value":[  
       {  
         "@odata.etag":"W/\"632481\"","fullname":"Peter Cambel","jobtitle":"Senior Developer","contactid":"00b6e0e2-b010-e611-80e1-00155da84c03"  
       }  
     ]  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-234">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-234">**Console output**</span></span>  
  
   ```    
   Contact list for account 'Fourth Coffee':  
           Name: Peter Cambel, Job title: Senior Developer    
   ```  
  
3. <span data-ttu-id="d9ebb-235">Remove the association that was just created between account Fourth Coffee and contact Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-235">Remove the association that was just created between account Fourth Coffee and contact Peter Cambel.</span></span>  
  
   <span data-ttu-id="d9ebb-236">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-236">**Request**</span></span> 
  
   ```http    
   DELETE http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03)/contact_customer_accounts/$ref?$id=http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-237">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-237">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
   <span data-ttu-id="d9ebb-238">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-238">**Console output**</span></span>  
  
   ```  
   Contact 'Peter Cambel' dissociated from account 'Fourth Coffee'.  
   ```  
  
4. <span data-ttu-id="d9ebb-239">Create a competitor named `Adventure Works`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-239">Create a competitor named `Adventure Works`.</span></span>  
  
   <span data-ttu-id="d9ebb-240">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-240">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/competitors HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "name": "Adventure Works",  
     "strengths": "Strong promoter of private tours for multi-day outdoor adventures"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-241">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-241">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content  
   OData-Version: 4.0  
   OData-EntityId: http://[Organization URI]/api/data/v9.0/accounts(77f77a42-5f0e-e611-80e0-00155da84c03)    
   ```  
  
   <span data-ttu-id="d9ebb-242">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-242">**Console output**</span></span>  
  
   ```  
   Competitor 'Adventure Works' created.  
   ```  
  
5. <span data-ttu-id="d9ebb-243">Create an opportunity named `River rafting adventure`.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-243">Create an opportunity named `River rafting adventure`.</span></span>  
  
   <span data-ttu-id="d9ebb-244">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-244">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/opportunities HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "name": "River rafting adventure",  
     "description": "Sales team on a river-rafting offsite and team building"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-245">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-245">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content  
   OData-Version: 4.0  
   OData-EntityId: http://[Organization URI]/api/data/v9.0/opportunities(7cf77a42-5f0e-e611-80e0-00155da84c03)    
   ```  
  
   <span data-ttu-id="d9ebb-246">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-246">**Console output**</span></span>  
  
   ```  
   Opportunity 'River rafting adventure' created.  
   ```  
  
6. <span data-ttu-id="d9ebb-247">Associate this new opportunity to this new competitor.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-247">Associate this new opportunity to this new competitor.</span></span> <span data-ttu-id="d9ebb-248">Note that the same general syntax is used in this many-to-many association as was used in the previous one-to-many association.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-248">Note that the same general syntax is used in this many-to-many association as was used in the previous one-to-many association.</span></span>  
  
   <span data-ttu-id="d9ebb-249">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-249">**Request**</span></span> 
  
   ```http    
   POST http://[Organization URI]/api/data/v9.0/opportunities(7cf77a42-5f0e-e611-80e0-00155da84c03)/opportunitycompetitors_association/$ref HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0  
   {  
     "@odata.id": "http://[Organization URI]/api/data/v9.0/competitors(77f77a42-5f0e-e611-80e0-00155da84c03)"  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-250">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-250">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
   <span data-ttu-id="d9ebb-251">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-251">**Console output**</span></span>  
  
   ```  
   Opportunity 'River rafting adventure' associated with competitor 'Adventure Works'.  
   ```  
  
7. <span data-ttu-id="d9ebb-252">Selectively retrieve all the opportunities associated with the competitor Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-252">Selectively retrieve all the opportunities associated with the competitor Adventure Works.</span></span>  <span data-ttu-id="d9ebb-253">An array is returned containing a single opportunity.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-253">An array is returned containing a single opportunity.</span></span>  
  
   <span data-ttu-id="d9ebb-254">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-254">**Request**</span></span> 
  
   ```http    
   GET http://[Organization URI]/api/data/v9.0/competitors(77f77a42-5f0e-e611-80e0-00155da84c03)?$select=name,&$expand=opportunitycompetitors_association($select=name,description) HTTP/1.1  
   Accept: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-255">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-255">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 200 OK  
   {   
      "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#competitors(name,opportunitycompetitors_association,opportunitycompetitors_association(name,description))/$entity",  
      "@odata.etag":"W/\"628913\"",  
      "name":"Adventure Works",  
      "competitorid":"77f77a42-5f0e-e611-80e0-00155da84c03",  
      "opportunitycompetitors_association":[   
         {   
            "@odata.etag":"W/\"628917\"",  
            "name":"River rafting adventure",  
            "description":"Sales team on a river-rafting offsite and team building",  
            "opportunityid":"7cf77a42-5f0e-e611-80e0-00155da84c03"  
         }  
      ]  
   }    
   ```  
  
   <span data-ttu-id="d9ebb-256">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-256">**Console output**</span></span>  
  
   ```    
   Competitor 'Adventure Works' has the following opportunities:  
           Name: River rafting adventure,  
           Description: Sales team on a river-rafting offsite and team building    
   ```  
  
8. <span data-ttu-id="d9ebb-257">Dissociate the opportunity from the competitor.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-257">Dissociate the opportunity from the competitor.</span></span>  <span data-ttu-id="d9ebb-258">Note again, that this has the same general syntax used to remove a one-to-many association.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-258">Note again, that this has the same general syntax used to remove a one-to-many association.</span></span>  
  
   <span data-ttu-id="d9ebb-259">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-259">**Request**</span></span> 
  
   ```http    
   DELETE http://[Organization URI]/api/data/v9.0/opportunities(7cf77a42-5f0e-e611-80e0-00155da84c03)/opportunitycompetitors_association/$ref?$id=http://[Token-CRM-Org-Name]/Contoso/api/data/v8.1/competitors(77f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-260">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-260">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
   <span data-ttu-id="d9ebb-261">**Console output**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-261">**Console output**</span></span>  
  
   ```  
   Opportunity 'River rafting adventure' disassociated from competitor 'Adventure Works'.  
   ```  
  
<a name="bkmk_section5"></a> 
  
## <a name="section-5-delete-entities-sample-cleanup"></a><span data-ttu-id="d9ebb-262">Section 5: Delete entities (sample cleanup)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-262">Section 5: Delete entities (sample cleanup)</span></span> 
 
 <span data-ttu-id="d9ebb-263">This section demonstrates how to delete entity instances.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-263">This section demonstrates how to delete entity instances.</span></span> <span data-ttu-id="d9ebb-264">The corresponding message is a straightforward DELETE request that uses the URI of the entity instance to be deleted.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-264">The corresponding message is a straightforward DELETE request that uses the URI of the entity instance to be deleted.</span></span>  <span data-ttu-id="d9ebb-265">If the target entity has a parent-child relationship with other entities, then deleting the parent will, by default, automatically cascade delete child instances.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-265">If the target entity has a parent-child relationship with other entities, then deleting the parent will, by default, automatically cascade delete child instances.</span></span> <span data-ttu-id="d9ebb-266">For example, in this sample, tasks have contact as their parent.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-266">For example, in this sample, tasks have contact as their parent.</span></span> <span data-ttu-id="d9ebb-267">For more information, see [Entity relationship behavior](../entity-relationship-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="d9ebb-267">For more information, see [Entity relationship behavior](../entity-relationship-behavior.md).</span></span>  
  
1. <span data-ttu-id="d9ebb-268">Each element of the collection of entity URLs is deleted.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-268">Each element of the collection of entity URLs is deleted.</span></span>  <span data-ttu-id="d9ebb-269">The first is a contact record for Peter Cambel.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-269">The first is a contact record for Peter Cambel.</span></span>  
  
   <span data-ttu-id="d9ebb-270">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-270">**Request**</span></span> 
  
   ```http
   DELETE http://[Organization URI]/api/data/v9.0/contacts(60f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   Content-Type: application/json  
   OData-MaxVersion: 4.0  
   OData-Version: 4.0    
   ```  
  
   <span data-ttu-id="d9ebb-271">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-271">**Response**</span></span>  
  
   ```http    
   HTTP/1.1 204 No Content    
   ```  
  
2. <span data-ttu-id="d9ebb-272">Subsequent iterations through the collection delete the remaining records.</span><span class="sxs-lookup"><span data-stu-id="d9ebb-272">Subsequent iterations through the collection delete the remaining records.</span></span>  
  
   <span data-ttu-id="d9ebb-273">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="d9ebb-273">**Request**</span></span> 
  
   ```http    
   DELETE http://[Organization URI]/api/data/v9.0/accounts(65f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   . . .  
  
   DELETE http://[Organization URI]/api/data/v9.0/accounts(6af77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   . . .  
  
   DELETE http://[Organization URI]/api/data/v9.0/contacts(6bf77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   . . .  
  
   DELETE http://[Organization URI]/api/data/v9.0/competitors(77f77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   . . .  
  
   DELETE http://[Organization URI]/api/data/v9.0/opportunities(7cf77a42-5f0e-e611-80e0-00155da84c03) HTTP/1.1  
   . . .    
   ```  
  
### <a name="see-also"></a><span data-ttu-id="d9ebb-274">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d9ebb-274">See also</span></span>  

 <span data-ttu-id="d9ebb-275">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d9ebb-275">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="d9ebb-276">[Create an entity using the Web API](create-entity-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d9ebb-276">[Create an entity using the Web API](create-entity-web-api.md) </span></span>  
 <span data-ttu-id="d9ebb-277">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d9ebb-277">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span></span>  
 <span data-ttu-id="d9ebb-278">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d9ebb-278">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="d9ebb-279">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="d9ebb-279">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span></span>  
 [<span data-ttu-id="d9ebb-280">Web API Basic Operations Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="d9ebb-280">Web API Basic Operations Sample (C#)</span></span>](web-api-basic-operations-sample-csharp.md)   

