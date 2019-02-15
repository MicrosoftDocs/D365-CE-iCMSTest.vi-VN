---
title: Web API Query Data Sample (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This group of samples shows how to query data using the Web API. These are implemented using Client-side JavaScript and C#
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 9457ce4f-0ef6-4085-8346-fe3134ec7106
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 1e23df06067b940952a55718172cc28b9247ab0f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386546"
---
# <a name="web-api-query-data-sample"></a><span data-ttu-id="b6b90-104">Web API Query Data Sample</span><span class="sxs-lookup"><span data-stu-id="b6b90-104">Web API Query Data Sample</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b6b90-105">This group of  samples demonstrate how to query data using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span><span class="sxs-lookup"><span data-stu-id="b6b90-105">This group of  samples demonstrate how to query data using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span></span> <span data-ttu-id="b6b90-106">This sample is implemented as a separate project for the following languages:</span><span class="sxs-lookup"><span data-stu-id="b6b90-106">This sample is implemented as a separate project for the following languages:</span></span>

- [<span data-ttu-id="b6b90-107">Web API Query Data Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b6b90-107">Web API Query Data Sample (Client-side JavaScript)</span></span>](web-api-query-data-sample-client-side-javascript.md)

- [<span data-ttu-id="b6b90-108">Query Data Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="b6b90-108">Query Data Sample (C#)</span></span>](web-api-query-data-sample-csharp.md)

  <span data-ttu-id="b6b90-109">This topic describes a common set of operations implemented by each sample in this group.</span><span class="sxs-lookup"><span data-stu-id="b6b90-109">This topic describes a common set of operations implemented by each sample in this group.</span></span> <span data-ttu-id="b6b90-110">This topic describes the HTTP requests and responses and text output that each sample in this group will perform without the language specific details.</span><span class="sxs-lookup"><span data-stu-id="b6b90-110">This topic describes the HTTP requests and responses and text output that each sample in this group will perform without the language specific details.</span></span> <span data-ttu-id="b6b90-111">See the language specific descriptions and the individual samples for details about how this operations are performed.</span><span class="sxs-lookup"><span data-stu-id="b6b90-111">See the language specific descriptions and the individual samples for details about how this operations are performed.</span></span>

## <a name="demonstrates"></a><span data-ttu-id="b6b90-112">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="b6b90-112">Demonstrates</span></span>

 <span data-ttu-id="b6b90-113">This sample is divided into the following principal sections, containing Web API query data operations which are discussed in greater detail in the associated conceptual topics.</span><span class="sxs-lookup"><span data-stu-id="b6b90-113">This sample is divided into the following principal sections, containing Web API query data operations which are discussed in greater detail in the associated conceptual topics.</span></span>

|<span data-ttu-id="b6b90-114">Topic section</span><span class="sxs-lookup"><span data-stu-id="b6b90-114">Topic section</span></span>|<span data-ttu-id="b6b90-115">Associated topic(s)</span><span class="sxs-lookup"><span data-stu-id="b6b90-115">Associated topic(s)</span></span>|
|-------------------|---------------------------|
|[<span data-ttu-id="b6b90-116">Selecting specific properties</span><span class="sxs-lookup"><span data-stu-id="b6b90-116">Selecting specific properties</span></span>](#bkmk_selectproperties)|[<span data-ttu-id="b6b90-117">Retrieve specific properties</span><span class="sxs-lookup"><span data-stu-id="b6b90-117">Retrieve specific properties</span></span>](retrieve-entity-using-web-api.md#bkmk_requestProperties)<br /><br /> [<span data-ttu-id="b6b90-118">Include formatted values</span><span class="sxs-lookup"><span data-stu-id="b6b90-118">Include formatted values</span></span>](query-data-web-api.md#bkmk_includeFormattedValues)|
|[<span data-ttu-id="b6b90-119">Using query functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-119">Using query functions</span></span>](#bkmk_queryfunctions)|[<span data-ttu-id="b6b90-120">Filter results</span><span class="sxs-lookup"><span data-stu-id="b6b90-120">Filter results</span></span>](query-data-web-api.md#bkmk_filter)<br /><br /> [<span data-ttu-id="b6b90-121">Standard query functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-121">Standard query functions</span></span>](query-data-web-api.md#bkmk_buildInQueryFunctions)<br /><br /> [<span data-ttu-id="b6b90-122">Compose a query with functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-122">Compose a query with functions</span></span>](use-web-api-functions.md#bkmk_composeQueryWithFunctions)<br /><br /> <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex>|
|[<span data-ttu-id="b6b90-123">Using operators</span><span class="sxs-lookup"><span data-stu-id="b6b90-123">Using operators</span></span>](#bkmk_operators)|[<span data-ttu-id="b6b90-124">Standard filter operators</span><span class="sxs-lookup"><span data-stu-id="b6b90-124">Standard filter operators</span></span>](query-data-web-api.md#bkmk_buildInFilterOperators)|
|[<span data-ttu-id="b6b90-125">Setting precedence</span><span class="sxs-lookup"><span data-stu-id="b6b90-125">Setting precedence</span></span>](#bkmk_prededence)|[<span data-ttu-id="b6b90-126">Standard filter operators</span><span class="sxs-lookup"><span data-stu-id="b6b90-126">Standard filter operators</span></span>](query-data-web-api.md#bkmk_buildInFilterOperators)|
|[<span data-ttu-id="b6b90-127">Ordering results</span><span class="sxs-lookup"><span data-stu-id="b6b90-127">Ordering results</span></span>](#bkmk_orderresults)|[<span data-ttu-id="b6b90-128">Order results</span><span class="sxs-lookup"><span data-stu-id="b6b90-128">Order results</span></span>](query-data-web-api.md#bkmk_order)<br /><br /> [<span data-ttu-id="b6b90-129">Filter results</span><span class="sxs-lookup"><span data-stu-id="b6b90-129">Filter results</span></span>](query-data-web-api.md#bkmk_filter)|
|[<span data-ttu-id="b6b90-130">Parameter alias</span><span class="sxs-lookup"><span data-stu-id="b6b90-130">Parameter alias</span></span>](#bkmk_parameteralias)|[<span data-ttu-id="b6b90-131">Use parameter aliases with system query options</span><span class="sxs-lookup"><span data-stu-id="b6b90-131">Use parameter aliases with system query options</span></span>](query-data-web-api.md#bkmk_useParameterAliases)|
|[<span data-ttu-id="b6b90-132">Limit results</span><span class="sxs-lookup"><span data-stu-id="b6b90-132">Limit results</span></span>](#bkmk_limitresults)|[<span data-ttu-id="b6b90-133">Limit results</span><span class="sxs-lookup"><span data-stu-id="b6b90-133">Limit results</span></span>](query-data-web-api.md#bkmk_limitResults)<br /><br /> [<span data-ttu-id="b6b90-134">Limits on number of entities returned</span><span class="sxs-lookup"><span data-stu-id="b6b90-134">Limits on number of entities returned</span></span>](query-data-web-api.md#bkmk_limits)|
|[<span data-ttu-id="b6b90-135">Expanding results</span><span class="sxs-lookup"><span data-stu-id="b6b90-135">Expanding results</span></span>](#bkmk_expandresults)|[<span data-ttu-id="b6b90-136">Retrieve related entities by expanding navigation properties</span><span class="sxs-lookup"><span data-stu-id="b6b90-136">Retrieve related entities by expanding navigation properties</span></span>](query-data-web-api.md#bkmk_expandRelated)|
|[<span data-ttu-id="b6b90-137">FetchXML queries</span><span class="sxs-lookup"><span data-stu-id="b6b90-137">FetchXML queries</span></span>](#bkmk_fetchxml)|[<span data-ttu-id="b6b90-138">FetchXML schema</span><span class="sxs-lookup"><span data-stu-id="b6b90-138">FetchXML schema</span></span>](../org-service/fetchxml-schema.md)<br /><br /> [<span data-ttu-id="b6b90-139">Page large result sets with FetchXML</span><span class="sxs-lookup"><span data-stu-id="b6b90-139">Page large result sets with FetchXML</span></span>](../org-service/page-large-result-sets-with-fetchxml.md)<br /><br /> [<span data-ttu-id="b6b90-140">Use custom FetchXML</span><span class="sxs-lookup"><span data-stu-id="b6b90-140">Use custom FetchXML</span></span>](retrieve-and-execute-predefined-queries.md#bkmk_useFetchXML)|
|[<span data-ttu-id="b6b90-141">Predefined queries</span><span class="sxs-lookup"><span data-stu-id="b6b90-141">Predefined queries</span></span>](#bkmk_predefinedqueries)|[<span data-ttu-id="b6b90-142">Retrieve and execute predefined queries</span><span class="sxs-lookup"><span data-stu-id="b6b90-142">Retrieve and execute predefined queries</span></span>](retrieve-and-execute-predefined-queries.md)<br /><br /> <xref href="Microsoft.Dynamics.CRM.userquery?text=userquery EntityType" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.savedquery?text=savedquery EntityType" />|

 <span data-ttu-id="b6b90-143">The following sections contain a brief discussion of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations performed, along with the corresponding HTTP messages and associated console output.</span><span class="sxs-lookup"><span data-stu-id="b6b90-143">The following sections contain a brief discussion of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations performed, along with the corresponding HTTP messages and associated console output.</span></span>

<a name="bkmk_sampleData"></a>

## <a name="sample-data"></a><span data-ttu-id="b6b90-144">Dữ liệu mẫu</span><span class="sxs-lookup"><span data-stu-id="b6b90-144">Sample data</span></span>  
 <span data-ttu-id="b6b90-145">To ensure the queries in this sample work properly, a standard set of sample records is created by this sample.</span><span class="sxs-lookup"><span data-stu-id="b6b90-145">To ensure the queries in this sample work properly, a standard set of sample records is created by this sample.</span></span> <span data-ttu-id="b6b90-146">These sample records will be deleted unless the user chooses to not delete them.</span><span class="sxs-lookup"><span data-stu-id="b6b90-146">These sample records will be deleted unless the user chooses to not delete them.</span></span> <span data-ttu-id="b6b90-147">This is the data the sample will be querying.</span><span class="sxs-lookup"><span data-stu-id="b6b90-147">This is the data the sample will be querying.</span></span> <span data-ttu-id="b6b90-148">You may get different results depending on any existing data in your environment.</span><span class="sxs-lookup"><span data-stu-id="b6b90-148">You may get different results depending on any existing data in your environment.</span></span>  
  
 <span data-ttu-id="b6b90-149">The data is added using *deep insert* in a single `POST` request and matches the following structure:</span><span class="sxs-lookup"><span data-stu-id="b6b90-149">The data is added using *deep insert* in a single `POST` request and matches the following structure:</span></span>  
  
```json  
  
 {  
        "name": "Contoso, Ltd. (sample)",  
        "primarycontactid": {  
            "firstname": "Yvonne", "lastname": "McKay (sample)", "jobtitle": "Coffee Master",  
            "annualincome": 45000, "Contact_Tasks": [  
            { "subject": "Task 1", "description": "Task 1 description" },  
            { "subject": "Task 2", "description": "Task 2 description" },  
            { "subject": "Task 3", "description": "Task 3 description" }  
            ]  
        },   
                            "Account_Tasks": [  
        { "subject": "Task 1", "description": "Task 1 description" },  
        { "subject": "Task 2", "description": "Task 2 description" },  
        { "subject": "Task 3", "description": "Task 3 description" }  
        ],  
        "contact_customer_accounts": [  
            {  
                "firstname": "Susanna", "lastname": "Stubberod (sample)", "jobtitle": "Senior Purchaser",  
                "annualincome": 52000, "Contact_Tasks": [  
            { "subject": "Task 1", "description": "Task 1 description" },  
            { "subject": "Task 2", "description": "Task 2 description" },  
            { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Nancy", "lastname": "Anderson (sample)", "jobtitle": "Activities Manager",  
                "annualincome": 55500, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Maria", "lastname": "Cambell (sample)", "jobtitle": "Accounts Manager",  
                "annualincome": 31000, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Nancy", "lastname": "Anderson (sample)", "jobtitle": "Logistics Specialist",  
                "annualincome": 63500, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Scott", "lastname": "Konersmann (sample)", "jobtitle": "Accounts Manager",  
                "annualincome": 38000, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Robert", "lastname": "Lyon (sample)", "jobtitle": "Senior Technician",  
                "annualincome": 78000, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Paul", "lastname": "Cannon (sample)", "jobtitle": "Ski Instructor",  
                "annualincome": 68500, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Rene", "lastname": "Valdes (sample)", "jobtitle": "Data Analyst III",  
                "annualincome": 86000, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            },  
            {  
                "firstname": "Jim", "lastname": "Glynn (sample)", "jobtitle": "Senior International Sales Manager",  
                "annualincome": 81400, "Contact_Tasks": [  
                { "subject": "Task 1", "description": "Task 1 description" },  
                { "subject": "Task 2", "description": "Task 2 description" },  
                { "subject": "Task 3", "description": "Task 3 description" }  
                ]  
            }  
        ]  
    }  
```  
  
<a name="bkmk_selectproperties"></a>   
## <a name="selecting-specific-properties"></a><span data-ttu-id="b6b90-150">Selecting specific properties</span><span class="sxs-lookup"><span data-stu-id="b6b90-150">Selecting specific properties</span></span>  
 <span data-ttu-id="b6b90-151">Always construct  queries using the `$select` query option, otherwise the server will return all properties of each entity which reduces performance.</span><span class="sxs-lookup"><span data-stu-id="b6b90-151">Always construct  queries using the `$select` query option, otherwise the server will return all properties of each entity which reduces performance.</span></span> <span data-ttu-id="b6b90-152">This example demonstrates how to construct a basic query by selecting three properties of a <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="b6b90-152">This example demonstrates how to construct a basic query by selecting three properties of a <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span></span> <span data-ttu-id="b6b90-153">The properties are `fullname`, `jobtitle`, `annualincome`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-153">The properties are `fullname`, `jobtitle`, `annualincome`.</span></span> <span data-ttu-id="b6b90-154">The section also illustrates the differences between formatted and unformatted values as seen in the results of the contact's `annualincome` property.</span><span class="sxs-lookup"><span data-stu-id="b6b90-154">The section also illustrates the differences between formatted and unformatted values as seen in the results of the contact's `annualincome` property.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-155">[Request specific properties](query-data-web-api.md#bkmk_requestProperties), [Include formatted values](query-data-web-api.md#bkmk_includeFormattedValues).</span><span class="sxs-lookup"><span data-stu-id="b6b90-155">[Request specific properties](query-data-web-api.md#bkmk_requestProperties), [Include formatted values](query-data-web-api.md#bkmk_includeFormattedValues).</span></span>  
  
 <span data-ttu-id="b6b90-156">In this example, we are requesting for a specific contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-156">In this example, we are requesting for a specific contact.</span></span> <span data-ttu-id="b6b90-157">In this case, it's the primary contact of the account, `Yvonne McKay (sample)`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-157">In this case, it's the primary contact of the account, `Yvonne McKay (sample)`.</span></span>  
  
 <span data-ttu-id="b6b90-158">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-158">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts(b848fdee-c143-e611-80d5-00155da84802)?$select=fullname,jobtitle,annualincome HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-159">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-159">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 517  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)/$entity",  
   "@odata.etag":"W/\"619718\"",  
   "fullname":"Yvonne McKay (sample)",  
   "jobtitle":"Coffee Master",  
   "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
   "annualincome":45000.0000,  
   "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
   "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
   "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
}  
```  
  
 <span data-ttu-id="b6b90-160">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-160">**Console output**</span></span>  
  
```  
Contact basic info:  
    Fullname: 'Yvonne McKay (sample)'  
    Jobtitle: 'Coffee Master'  
    Annualincome: '45000' (unformatted)  
    Annualincome: $45,000.00 (formatted)  
  
```  
  
<a name="bkmk_queryfunctions"></a>   
## <a name="using-query-functions"></a><span data-ttu-id="b6b90-161">Using query functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-161">Using query functions</span></span>  
 <span data-ttu-id="b6b90-162">Use filter options to set criteria for the results you want.</span><span class="sxs-lookup"><span data-stu-id="b6b90-162">Use filter options to set criteria for the results you want.</span></span> <span data-ttu-id="b6b90-163">You can  build simple to complex filters using a combination of query functions, comparison operators, and logical operators.</span><span class="sxs-lookup"><span data-stu-id="b6b90-163">You can  build simple to complex filters using a combination of query functions, comparison operators, and logical operators.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-164">[Filter results](query-data-web-api.md#bkmk_filter).</span><span class="sxs-lookup"><span data-stu-id="b6b90-164">[Filter results](query-data-web-api.md#bkmk_filter).</span></span>  
  
 <span data-ttu-id="b6b90-165">Query functions are functions that can be used as a filter criteria in a query.</span><span class="sxs-lookup"><span data-stu-id="b6b90-165">Query functions are functions that can be used as a filter criteria in a query.</span></span> <span data-ttu-id="b6b90-166">There are standard query functions and [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] specific query functions.</span><span class="sxs-lookup"><span data-stu-id="b6b90-166">There are standard query functions and [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] specific query functions.</span></span> <span data-ttu-id="b6b90-167">These functions accept parameters and return a `Boolean` value.</span><span class="sxs-lookup"><span data-stu-id="b6b90-167">These functions accept parameters and return a `Boolean` value.</span></span> <span data-ttu-id="b6b90-168">This sample illustrates how to create a query for each type.</span><span class="sxs-lookup"><span data-stu-id="b6b90-168">This sample illustrates how to create a query for each type.</span></span>  
  
### <a name="standard-query-functions"></a><span data-ttu-id="b6b90-169">Standard query functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-169">Standard query functions</span></span>  
 [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] <span data-ttu-id="b6b90-170">supports a small subset of OData built-in query functions, specifically: `contains`, `endswith`, and `startswith`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-170">supports a small subset of OData built-in query functions, specifically: `contains`, `endswith`, and `startswith`.</span></span> <span data-ttu-id="b6b90-171">For example, the `contains` standard query function allows us to filter for properties matching a string.</span><span class="sxs-lookup"><span data-stu-id="b6b90-171">For example, the `contains` standard query function allows us to filter for properties matching a string.</span></span> <span data-ttu-id="b6b90-172">In this operation, we are querying for all contacts with `fullname` containing the string `(sample)`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-172">In this operation, we are querying for all contacts with `fullname` containing the string `(sample)`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-173">[Standard query functions](query-data-web-api.md#bkmk_buildInQueryFunctions).</span><span class="sxs-lookup"><span data-stu-id="b6b90-173">[Standard query functions](query-data-web-api.md#bkmk_buildInQueryFunctions).</span></span>  
  
 <span data-ttu-id="b6b90-174">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-174">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)') HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-175">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-175">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 4284  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619718\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619839\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"1cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619843\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"24c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619847\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"2cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619851\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"34c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619853\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"38c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-176">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-176">**Console output**</span></span>  
  
```  
Contacts filtered by fullname containing '(sample)':  
    1) Yvonne McKay (sample), Coffee Master, $45,000.00  
    2) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Maria Cambell (sample), Accounts Manager, $31,000.00  
    5) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    6) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    7) Robert Lyon (sample), Senior Technician, $78,000.00  
    8) Paul Cannon (sample), Ski Instructor, $68,500.00  
    9) Rene Valdes (sample), Data Analyst III, $86,000.00  
    10) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
  
```  
  
### <a name="includepndynamicscrmincludespn-dynamics-crmmd-query-functions"></a>[!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] <span data-ttu-id="b6b90-177">query functions</span><span class="sxs-lookup"><span data-stu-id="b6b90-177">query functions</span></span>  
 [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] <span data-ttu-id="b6b90-178">query functions provide a large number of options to build queries which are relevant for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="b6b90-178">query functions provide a large number of options to build queries which are relevant for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="b6b90-179">For a complete list of these functions, see <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex>.</span><span class="sxs-lookup"><span data-stu-id="b6b90-179">For a complete list of these functions, see <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex>.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-180">[Compose a query with functions](use-web-api-functions.md#bkmk_composeQueryWithFunctions)</span><span class="sxs-lookup"><span data-stu-id="b6b90-180">[Compose a query with functions](use-web-api-functions.md#bkmk_composeQueryWithFunctions)</span></span>  
  
 <span data-ttu-id="b6b90-181">You will use these query functions in a manner similar to the standard query functions.</span><span class="sxs-lookup"><span data-stu-id="b6b90-181">You will use these query functions in a manner similar to the standard query functions.</span></span> <span data-ttu-id="b6b90-182">The main difference is, when using [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] query functions, you must provide the full name of the function including the parameter name(s).</span><span class="sxs-lookup"><span data-stu-id="b6b90-182">The main difference is, when using [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] query functions, you must provide the full name of the function including the parameter name(s).</span></span> <span data-ttu-id="b6b90-183">For example, to get a list of contacts created in the last hour, you can construct a query using the <xref href="Microsoft.Dynamics.CRM.LastXHours?text=LastXHours Function" />.</span><span class="sxs-lookup"><span data-stu-id="b6b90-183">For example, to get a list of contacts created in the last hour, you can construct a query using the <xref href="Microsoft.Dynamics.CRM.LastXHours?text=LastXHours Function" />.</span></span>  
  
 <span data-ttu-id="b6b90-184">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-184">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=Microsoft.Dynamics.CRM.LastXHours(PropertyName='createdon',PropertyValue='1') HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-185">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-185">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 4284  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619718\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619839\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"1cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619843\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"24c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619847\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"2cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619851\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"34c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619853\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"38c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-186">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-186">**Console output**</span></span>  
  
```  
Contacts that were created within the last 1hr:  
    1) Yvonne McKay (sample), Coffee Master, $45,000.00  
    2) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Maria Cambell (sample), Accounts Manager, $31,000.00  
    5) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    6) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    7) Robert Lyon (sample), Senior Technician, $78,000.00  
    8) Paul Cannon (sample), Ski Instructor, $68,500.00  
    9) Rene Valdes (sample), Data Analyst III, $86,000.00  
    10) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
<a name="bkmk_operators"></a>   
## <a name="using-operators"></a><span data-ttu-id="b6b90-187">Using operators</span><span class="sxs-lookup"><span data-stu-id="b6b90-187">Using operators</span></span>  
 <span data-ttu-id="b6b90-188">Use the [Standard filter operators](query-data-web-api.md#bkmk_buildInFilterOperators) (`eq`,`ne`,`gt`,`ge`,`lt`,`le`,`and`,`or`,`not`)  to further refine our results.</span><span class="sxs-lookup"><span data-stu-id="b6b90-188">Use the [Standard filter operators](query-data-web-api.md#bkmk_buildInFilterOperators) (`eq`,`ne`,`gt`,`ge`,`lt`,`le`,`and`,`or`,`not`)  to further refine our results.</span></span> <span data-ttu-id="b6b90-189">In this example, we are requesting a list of all contacts with `fullname` containing `(sample)` and annual income greater than `55000`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-189">In this example, we are requesting a list of all contacts with `fullname` containing `(sample)` and annual income greater than `55000`.</span></span>  
  
 <span data-ttu-id="b6b90-190">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-190">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')%20and%20annualincome%20gt%2055000 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-191">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-191">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 2629  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619851\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"34c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619853\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"38c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-192">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-192">**Console output**</span></span>  
  
```  
Contacts filtered by fullname and annualincome (<$55,000):  
    1) Nancy Anderson (sample), Activities Manager, $55,500.00  
    2) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    3) Robert Lyon (sample), Senior Technician, $78,000.00  
    4) Paul Cannon (sample), Ski Instructor, $68,500.00  
    5) Rene Valdes (sample), Data Analyst III, $86,000.00  
    6) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
<a name="bkmk_prededence"></a>   
## <a name="setting-precedence"></a><span data-ttu-id="b6b90-193">Setting precedence</span><span class="sxs-lookup"><span data-stu-id="b6b90-193">Setting precedence</span></span>  
 <span data-ttu-id="b6b90-194">You will use parentheses to establish the order in which your conditions are evaluated.</span><span class="sxs-lookup"><span data-stu-id="b6b90-194">You will use parentheses to establish the order in which your conditions are evaluated.</span></span>  
  
 <span data-ttu-id="b6b90-195">In this example, we are requesting a list of all contacts with `fullname` containing `(sample)`, `jobtitle` containing either `senior` or `specialist`, and `annualincome` greater than `55000`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-195">In this example, we are requesting a list of all contacts with `fullname` containing `(sample)`, `jobtitle` containing either `senior` or `specialist`, and `annualincome` greater than `55000`.</span></span> <span data-ttu-id="b6b90-196">To get the results we want, parentheses are used to group the `jobtitle` filters together.</span><span class="sxs-lookup"><span data-stu-id="b6b90-196">To get the results we want, parentheses are used to group the `jobtitle` filters together.</span></span> <span data-ttu-id="b6b90-197">Since all operators have the same precedence, omitting the parentheses will give the `or` operator the same precedence as the `and` operators.</span><span class="sxs-lookup"><span data-stu-id="b6b90-197">Since all operators have the same precedence, omitting the parentheses will give the `or` operator the same precedence as the `and` operators.</span></span>  <span data-ttu-id="b6b90-198">Filters are applied from left to right.</span><span class="sxs-lookup"><span data-stu-id="b6b90-198">Filters are applied from left to right.</span></span> <span data-ttu-id="b6b90-199">The order in which these statements appear in the filter can affect the results.</span><span class="sxs-lookup"><span data-stu-id="b6b90-199">The order in which these statements appear in the filter can affect the results.</span></span> <span data-ttu-id="b6b90-200">This is what the query in this example looks like: `$filter=contains(fullname,'(sample)') and (contains(jobtitle,'senior') or contains(jobtitle,'specialist')) and annualincome gt 55000`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-200">This is what the query in this example looks like: `$filter=contains(fullname,'(sample)') and (contains(jobtitle,'senior') or contains(jobtitle,'specialist')) and annualincome gt 55000`.</span></span>  
  
 <span data-ttu-id="b6b90-201">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-201">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')%20and%20(contains(jobtitle,'senior')%20or%20contains(jobtitle,'specialist'))%20and%20annualincome%20gt%2055000 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-202">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-202">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 1393  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-203">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-203">**Console output**</span></span>  
  
```  
Contacts filtered by fullname, annualincome and jobtitle (Senior or Specialist):  
    1) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    2) Robert Lyon (sample), Senior Technician, $78,000.00  
    3) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
<a name="bkmk_orderresults"></a>   
## <a name="ordering-results"></a><span data-ttu-id="b6b90-204">Ordering results</span><span class="sxs-lookup"><span data-stu-id="b6b90-204">Ordering results</span></span>  
 <span data-ttu-id="b6b90-205">You can specify either an ascending or descending order on the results by using the `$orderby` filter option .</span><span class="sxs-lookup"><span data-stu-id="b6b90-205">You can specify either an ascending or descending order on the results by using the `$orderby` filter option .</span></span> <span data-ttu-id="b6b90-206">In this example, we will query for all contacts with `fullname` containing `(sample)` and request the data in ascending order based on the `jobtitle` property value and then in  descending based on the `annualincome` property value using this syntax: `$orderby=jobtitle asc, annualincome desc`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-206">In this example, we will query for all contacts with `fullname` containing `(sample)` and request the data in ascending order based on the `jobtitle` property value and then in  descending based on the `annualincome` property value using this syntax: `$orderby=jobtitle asc, annualincome desc`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-207">[Order results](query-data-web-api.md#bkmk_order).</span><span class="sxs-lookup"><span data-stu-id="b6b90-207">[Order results](query-data-web-api.md#bkmk_order).</span></span>  
  
 <span data-ttu-id="b6b90-208">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-208">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')%20&$orderby=jobtitle%20asc,%20annualincome%20desc HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-209">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-209">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 4284  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619847\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"2cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619843\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"24c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619718\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619853\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"38c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619839\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"1cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619851\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"34c364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-210">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-210">**Console output**</span></span>  
  
```  
Contacts ordered by jobtitle (ascending) and annualincome (descending):  
    1) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    2) Maria Cambell (sample), Accounts Manager, $31,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Yvonne McKay (sample), Coffee Master, $45,000.00  
    5) Rene Valdes (sample), Data Analyst III, $86,000.00  
    6) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    7) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
    8) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    9) Robert Lyon (sample), Senior Technician, $78,000.00  
    10) Paul Cannon (sample), Ski Instructor, $68,500.00  
```  
  
<a name="bkmk_parameteralias"></a>   
## <a name="parameter-alias"></a><span data-ttu-id="b6b90-211">Parameter alias</span><span class="sxs-lookup"><span data-stu-id="b6b90-211">Parameter alias</span></span>  
 <span data-ttu-id="b6b90-212">Use parameter aliases to more easily reuse  parameters in your filters.</span><span class="sxs-lookup"><span data-stu-id="b6b90-212">Use parameter aliases to more easily reuse  parameters in your filters.</span></span> <span data-ttu-id="b6b90-213">Parameterized aliases can be used in `$filter` and `$orderby` options.</span><span class="sxs-lookup"><span data-stu-id="b6b90-213">Parameterized aliases can be used in `$filter` and `$orderby` options.</span></span> <span data-ttu-id="b6b90-214">If the alias isn’t assigned a value it is assumed to be null.</span><span class="sxs-lookup"><span data-stu-id="b6b90-214">If the alias isn’t assigned a value it is assumed to be null.</span></span> <span data-ttu-id="b6b90-215">You can also use parameter aliases when calling functions.</span><span class="sxs-lookup"><span data-stu-id="b6b90-215">You can also use parameter aliases when calling functions.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-216">[Use Web API functions](use-web-api-functions.md), [Use parameter aliases with system query options](query-data-web-api.md#bkmk_useParameterAliases).</span><span class="sxs-lookup"><span data-stu-id="b6b90-216">[Use Web API functions](use-web-api-functions.md), [Use parameter aliases with system query options](query-data-web-api.md#bkmk_useParameterAliases).</span></span> <span data-ttu-id="b6b90-217">Taking the order results operation for example, we can write that query again using parameters and we would get the same output results.</span><span class="sxs-lookup"><span data-stu-id="b6b90-217">Taking the order results operation for example, we can write that query again using parameters and we would get the same output results.</span></span>  
  
 <span data-ttu-id="b6b90-218">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-218">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(@p1,'(sample)')%20&$orderby=@p2%20asc,%20@p3%20desc&@p1=fullname&@p2=jobtitle&@p3=annualincome HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-219">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-219">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 4284  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619847\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"2cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619843\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"24c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619718\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619853\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"38c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619855\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"3cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619839\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"1cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619849\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"30c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619851\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"34c364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-220">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-220">**Console output**</span></span>  
  
```  
Contacts list using parameterized aliases:  
    1) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    2) Maria Cambell (sample), Accounts Manager, $31,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Yvonne McKay (sample), Coffee Master, $45,000.00  
    5) Rene Valdes (sample), Data Analyst III, $86,000.00  
    6) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    7) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
    8) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    9) Robert Lyon (sample), Senior Technician, $78,000.00  
    10) Paul Cannon (sample), Ski Instructor, $68,500.00  
```  
  
<a name="bkmk_limitresults"></a>   
## <a name="limit-results"></a><span data-ttu-id="b6b90-221">Limit results</span><span class="sxs-lookup"><span data-stu-id="b6b90-221">Limit results</span></span>  
 <span data-ttu-id="b6b90-222">Returning more data than you need is bad for performance.</span><span class="sxs-lookup"><span data-stu-id="b6b90-222">Returning more data than you need is bad for performance.</span></span> <span data-ttu-id="b6b90-223">The server will return a maximum of 5000 entities per request.</span><span class="sxs-lookup"><span data-stu-id="b6b90-223">The server will return a maximum of 5000 entities per request.</span></span> <span data-ttu-id="b6b90-224">You can limit the number of results returned using the `$top` query option or by adding `odata.maxpagesize` in the request header.</span><span class="sxs-lookup"><span data-stu-id="b6b90-224">You can limit the number of results returned using the `$top` query option or by adding `odata.maxpagesize` in the request header.</span></span> <span data-ttu-id="b6b90-225">The `$top` query option only returns the top number of entities from the result set and ignores the rest.</span><span class="sxs-lookup"><span data-stu-id="b6b90-225">The `$top` query option only returns the top number of entities from the result set and ignores the rest.</span></span> <span data-ttu-id="b6b90-226">The `odata.maxpagesize` request header specifies the number of entities return per page with an `@odata.nextLink` property to get results of the next page.</span><span class="sxs-lookup"><span data-stu-id="b6b90-226">The `odata.maxpagesize` request header specifies the number of entities return per page with an `@odata.nextLink` property to get results of the next page.</span></span> <span data-ttu-id="b6b90-227">For more information about `odata.maxpagesize`, see the section on [Pagination](#bkmk_filterPagination) and see also [Limits on number of entities returned](query-data-web-api.md#bkmk_limits).</span><span class="sxs-lookup"><span data-stu-id="b6b90-227">For more information about `odata.maxpagesize`, see the section on [Pagination](#bkmk_filterPagination) and see also [Limits on number of entities returned](query-data-web-api.md#bkmk_limits).</span></span>  
  
<a name="bkmk_topResults"></a>   
### <a name="top-results"></a><span data-ttu-id="b6b90-228">Top results</span><span class="sxs-lookup"><span data-stu-id="b6b90-228">Top results</span></span>  
 <span data-ttu-id="b6b90-229">We can apply the `$top` query option to limit the basic query operation to the first five contacts with `fullname` containing `(sample)`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-229">We can apply the `$top` query option to limit the basic query operation to the first five contacts with `fullname` containing `(sample)`.</span></span> <span data-ttu-id="b6b90-230">In this case, the request actually produces at least 10 results, but only the first 5 entries are returned in the response.</span><span class="sxs-lookup"><span data-stu-id="b6b90-230">In this case, the request actually produces at least 10 results, but only the first 5 entries are returned in the response.</span></span>  
  
 <span data-ttu-id="b6b90-231">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-231">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')&$top=5 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-232">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-232">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Content-Length: 2209  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "value":[  
      {  
         "@odata.etag":"W/\"619718\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"15c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619839\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"1cc364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619841\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"20c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619843\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"24c364b2-bf43-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"619845\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"28c364b2-bf43-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-233">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-233">**Console output**</span></span>  
  
```  
Contacts top 5 results:  
    1) Yvonne McKay (sample), Coffee Master, $45,000.00  
    2) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Maria Cambell (sample), Accounts Manager, $31,000.00  
    5) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
  
```  
  
<a name="bkmk_resultCount"></a>   
### <a name="result-count"></a><span data-ttu-id="b6b90-234">Result count</span><span class="sxs-lookup"><span data-stu-id="b6b90-234">Result count</span></span>  
 <span data-ttu-id="b6b90-235">You can get just the count of records from a collection-valued property or a count of matched entities in a filter.</span><span class="sxs-lookup"><span data-stu-id="b6b90-235">You can get just the count of records from a collection-valued property or a count of matched entities in a filter.</span></span> <span data-ttu-id="b6b90-236">Getting a count tells us the number of possible entities in our result.</span><span class="sxs-lookup"><span data-stu-id="b6b90-236">Getting a count tells us the number of possible entities in our result.</span></span> <span data-ttu-id="b6b90-237">However, the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server will return 5000 as the maximum count even if the result may have more.</span><span class="sxs-lookup"><span data-stu-id="b6b90-237">However, the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server will return 5000 as the maximum count even if the result may have more.</span></span> <span data-ttu-id="b6b90-238">In this example, we constructed a filter with `jobtitle` containing either `Senior` or `Manager` and we also requested a `$count` of the result.</span><span class="sxs-lookup"><span data-stu-id="b6b90-238">In this example, we constructed a filter with `jobtitle` containing either `Senior` or `Manager` and we also requested a `$count` of the result.</span></span> <span data-ttu-id="b6b90-239">The response contains the count in the `@odata.count` property as well as the results of the query.</span><span class="sxs-lookup"><span data-stu-id="b6b90-239">The response contains the count in the `@odata.count` property as well as the results of the query.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-240">[Retrieve a count of entities](query-data-web-api.md#bkmk_retrieveCount).</span><span class="sxs-lookup"><span data-stu-id="b6b90-240">[Retrieve a count of entities](query-data-web-api.md#bkmk_retrieveCount).</span></span>  
  
 <span data-ttu-id="b6b90-241">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-241">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(jobtitle,'senior')%20or%20contains(jobtitle,%20'manager')&$count=true HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-242">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-242">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 2654  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "@odata.count":6,  
   "value":[  
      {  
         "@odata.etag":"W/\"620258\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"bf48fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620260\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"c348fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620262\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"c748fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620266\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"cf48fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620268\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"d348fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620274\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"df48fdee-c143-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-243">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-243">**Console output**</span></span>  
  
```  
6 contacts have either 'Manager' or 'Senior' designation in their jobtitle.  
Manager or Senior:  
    1) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    2) Nancy Anderson (sample), Activities Manager, $55,500.00  
    3) Maria Cambell (sample), Accounts Manager, $31,000.00  
    4) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    5) Robert Lyon (sample), Senior Technician, $78,000.00  
    6) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
  
```  
  
<a name="bkmk_filterPagination"></a>   
### <a name="pagination"></a><span data-ttu-id="b6b90-244">Dàn trang</span><span class="sxs-lookup"><span data-stu-id="b6b90-244">Pagination</span></span>  
 <span data-ttu-id="b6b90-245">To retrieve a sequential subset of results for a query that returns a large number of entities, use the `odata.maxpagesize` instead of `$top`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-245">To retrieve a sequential subset of results for a query that returns a large number of entities, use the `odata.maxpagesize` instead of `$top`.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-246">[Specify the number of entities to return in a page](query-data-web-api.md#bkmk_specifyNumber).</span><span class="sxs-lookup"><span data-stu-id="b6b90-246">[Specify the number of entities to return in a page](query-data-web-api.md#bkmk_specifyNumber).</span></span>  
  
 <span data-ttu-id="b6b90-247">In this example, we ask for a `$count` and we set the `odata.maxpagesize` to `4`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-247">In this example, we ask for a `$count` and we set the `odata.maxpagesize` to `4`.</span></span> <span data-ttu-id="b6b90-248">This filter matches 10 contacts, but we are only retrieving 4 at a time.</span><span class="sxs-lookup"><span data-stu-id="b6b90-248">This filter matches 10 contacts, but we are only retrieving 4 at a time.</span></span> <span data-ttu-id="b6b90-249">We also use the count and the max page size to figured out how many total pages there are.</span><span class="sxs-lookup"><span data-stu-id="b6b90-249">We also use the count and the max page size to figured out how many total pages there are.</span></span> <span data-ttu-id="b6b90-250">The result of the first page is returned in this request.</span><span class="sxs-lookup"><span data-stu-id="b6b90-250">The result of the first page is returned in this request.</span></span>  
  
 <span data-ttu-id="b6b90-251">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-251">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')&$count=true HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=4, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-252">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-252">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=4  
Content-Length: 2294  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "@odata.count":10,  
   "value":[  
      {  
         "@odata.etag":"W/\"620138\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"b848fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620258\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"bf48fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620260\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"c348fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620262\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"c748fdee-c143-e611-80d5-00155da84802"  
      }  
   ],  
   "@odata.nextLink":"http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')&$count=true&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253ccontactid%2520last%253d%2522%257bC748FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520first%253d%2522%257bB848FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E"  
}  
```  
  
 <span data-ttu-id="b6b90-253">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-253">**Console output**</span></span>  
  
```  
Contacts total: 10  Contacts per page: 4.  
Page 1 of 3:  
    1) Yvonne McKay (sample), Coffee Master, $45,000.00  
    2) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    3) Nancy Anderson (sample), Activities Manager, $55,500.00  
    4) Maria Cambell (sample), Accounts Manager, $31,000.00  
  
```  
  
 <span data-ttu-id="b6b90-254">To retrieve page 2, use a `GET` request with the value of the  `@odata.nextLink` property.</span><span class="sxs-lookup"><span data-stu-id="b6b90-254">To retrieve page 2, use a `GET` request with the value of the  `@odata.nextLink` property.</span></span>  
  
 <span data-ttu-id="b6b90-255">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-255">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')&$count=true&$skiptoken=%3Ccookie%20pagenumber=%222%22%20pagingcookie=%22%253ccookie%2520page%253d%25221%2522%253e%253ccontactid%2520last%253d%2522%257bC748FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520first%253d%2522%257bB848FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=4, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-256">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-256">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=4  
Content-Length: 2294  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome)",  
   "@odata.count":10,  
   "value":[  
      {  
         "@odata.etag":"W/\"620264\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"cb48fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620266\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"cf48fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620268\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"d348fdee-c143-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620270\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"d748fdee-c143-e611-80d5-00155da84802"  
      }  
   ],  
   "@odata.nextLink":"http://[Organization URI]/api/data/v9.0/contacts?$select=fullname,jobtitle,annualincome&$filter=contains(fullname,'(sample)')&$count=true&$skiptoken=%3Ccookie%20pagenumber=%223%22%20pagingcookie=%22%253ccookie%2520page%253d%25222%2522%253e%253ccontactid%2520last%253d%2522%257bD748FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520first%253d%2522%257bCB48FDEE-C143-E611-80D5-00155DA84802%257d%2522%2520%252f%253e%253c%252fcookie%253e%22%20istracking=%22False%22%20/%3E"  
}  
```  
  
 <span data-ttu-id="b6b90-257">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-257">**Console output**</span></span>  
  
```  
Page 2 of 3:  
    1) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    2) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    3) Robert Lyon (sample), Senior Technician, $78,000.00  
    4) Paul Cannon (sample), Ski Instructor, $68,500.00  
```  
  
<a name="bkmk_expandresults"></a>   
## <a name="expanding-results"></a><span data-ttu-id="b6b90-258">Expanding results</span><span class="sxs-lookup"><span data-stu-id="b6b90-258">Expanding results</span></span>  
 <span data-ttu-id="b6b90-259">To retrieve information on associated entities, use the `$expand` query option on navigation properties.</span><span class="sxs-lookup"><span data-stu-id="b6b90-259">To retrieve information on associated entities, use the `$expand` query option on navigation properties.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-260">[Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated).</span><span class="sxs-lookup"><span data-stu-id="b6b90-260">[Retrieve related entities by expanding navigation properties](query-data-web-api.md#bkmk_expandRelated).</span></span>  
  
### <a name="expand-on-single-valued-navigation-property"></a><span data-ttu-id="b6b90-261">Expand on single-valued navigation property</span><span class="sxs-lookup"><span data-stu-id="b6b90-261">Expand on single-valued navigation property</span></span>  
 <span data-ttu-id="b6b90-262">A Single-valued navigation property represents a many-to-one relationships.</span><span class="sxs-lookup"><span data-stu-id="b6b90-262">A Single-valued navigation property represents a many-to-one relationships.</span></span> <span data-ttu-id="b6b90-263">In our sample data, the account has a relationship with a contact via the `primarycontactid` attribute.</span><span class="sxs-lookup"><span data-stu-id="b6b90-263">In our sample data, the account has a relationship with a contact via the `primarycontactid` attribute.</span></span> <span data-ttu-id="b6b90-264">In this relationship, the account can only have one primary contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-264">In this relationship, the account can only have one primary contact.</span></span>  <span data-ttu-id="b6b90-265">Using the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, we can create a query to get information about the account and expanded information about its primary contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-265">Using the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, we can create a query to get information about the account and expanded information about its primary contact.</span></span>  
  
 <span data-ttu-id="b6b90-266">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-266">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/accounts(b2546951-c543-e611-80d5-00155da84802)?$select=name&$expand=primarycontactid($select=fullname,jobtitle,annualincome) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-267">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-267">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 700  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,primarycontactid(fullname,jobtitle,annualincome))/$entity",  
   "@odata.etag":"W/\"620641\"",  
   "name":"Contoso, Ltd. (sample)",  
   "accountid":"b2546951-c543-e611-80d5-00155da84802",  
   "primarycontactid":{  
      "@odata.etag":"W/\"620534\"",  
      "fullname":"Yvonne McKay (sample)",  
      "jobtitle":"Coffee Master",  
      "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
      "annualincome":45000.0000,  
      "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
      "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
      "contactid":"b3546951-c543-e611-80d5-00155da84802"  
   }  
}  
```  
  
 <span data-ttu-id="b6b90-268">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-268">**Console output**</span></span>  
  
```  
Account 'Contoso, Ltd. (sample)' has the following primary contact person:  
    Fullname: 'Yvonne McKay (sample)'   
    Jobtitle: 'Coffee Master'   
    Annualincome: '45000'  
```  
  
### <a name="expand-on-partner-property"></a><span data-ttu-id="b6b90-269">Expand on partner property</span><span class="sxs-lookup"><span data-stu-id="b6b90-269">Expand on partner property</span></span>  
 <span data-ttu-id="b6b90-270">Each navigation property has a corresponding “partner” property.</span><span class="sxs-lookup"><span data-stu-id="b6b90-270">Each navigation property has a corresponding “partner” property.</span></span> <span data-ttu-id="b6b90-271">Once an association is made, we can retrieve information through this association.</span><span class="sxs-lookup"><span data-stu-id="b6b90-271">Once an association is made, we can retrieve information through this association.</span></span> <span data-ttu-id="b6b90-272">Which attribute we use depends on the base entity that the query is against.</span><span class="sxs-lookup"><span data-stu-id="b6b90-272">Which attribute we use depends on the base entity that the query is against.</span></span> <span data-ttu-id="b6b90-273">For example, in the previous operation, we created a query against the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" /> and we wanted to get additional information about its primary contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-273">For example, in the previous operation, we created a query against the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" /> and we wanted to get additional information about its primary contact.</span></span> <span data-ttu-id="b6b90-274">We did that via the `primarycontactid` attribute.</span><span class="sxs-lookup"><span data-stu-id="b6b90-274">We did that via the `primarycontactid` attribute.</span></span> <span data-ttu-id="b6b90-275">If we look up the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, under the [Single-valued navigation properties](/dynamics365/customer-engagement/web-api/account?view=dynamics-ce-odata-9#Single-valued_navigation_properties) section, we can see that the partner property that corresponds to `primarycontactid` is  `account_primary_contact` collection-valued navigation property found on the <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="b6b90-275">If we look up the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, under the [Single-valued navigation properties](/dynamics365/customer-engagement/web-api/account?view=dynamics-ce-odata-9#Single-valued_navigation_properties) section, we can see that the partner property that corresponds to `primarycontactid` is  `account_primary_contact` collection-valued navigation property found on the <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span></span>  
  
 <span data-ttu-id="b6b90-276">Writing a query against a contact, you can expand on the `account_primary_contact` attribute to get information about accounts where this contact is the primary contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-276">Writing a query against a contact, you can expand on the `account_primary_contact` attribute to get information about accounts where this contact is the primary contact.</span></span> <span data-ttu-id="b6b90-277">In the sample data, `Yvonne McKay (sample)` is the primary contact person for only one account.</span><span class="sxs-lookup"><span data-stu-id="b6b90-277">In the sample data, `Yvonne McKay (sample)` is the primary contact person for only one account.</span></span> <span data-ttu-id="b6b90-278">However, she can potentially be assigned to other accounts as primary contact.</span><span class="sxs-lookup"><span data-stu-id="b6b90-278">However, she can potentially be assigned to other accounts as primary contact.</span></span> <span data-ttu-id="b6b90-279">Because the `account_primary_contact` property has a many-to-one relationship the result is returned as an array of account entities.</span><span class="sxs-lookup"><span data-stu-id="b6b90-279">Because the `account_primary_contact` property has a many-to-one relationship the result is returned as an array of account entities.</span></span>  
  
 <span data-ttu-id="b6b90-280">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-280">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts(b3546951-c543-e611-80d5-00155da84802)?$select=fullname,jobtitle,annualincome&$expand=account_primary_contact($select=name) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-281">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-281">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 737  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome,account_primary_contact,account_primary_contact(name))/$entity",  
   "@odata.etag":"W/\"620534\"",  
   "fullname":"Yvonne McKay (sample)",  
   "jobtitle":"Coffee Master",  
   "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
   "annualincome":45000.0000,  
   "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
   "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
   "contactid":"b3546951-c543-e611-80d5-00155da84802",  
   "account_primary_contact":[  
      {  
         "@odata.etag":"W/\"620919\"",  
         "name":"Contoso, Ltd. (sample)",  
         "accountid":"b2546951-c543-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-282">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-282">**Console output**</span></span>  
  
```  
Contact 'Yvonne McKay (sample)' is the primary contact for the following accounts:  
    1) Contoso, Ltd. (sample)  
```  
  
### <a name="expand-on-collection-valued-navigation-property"></a><span data-ttu-id="b6b90-283">Expand on collection-valued navigation property</span><span class="sxs-lookup"><span data-stu-id="b6b90-283">Expand on collection-valued navigation property</span></span>  
 <span data-ttu-id="b6b90-284">Collection-valued navigation properties support one-to-many or many-to-many relationships.</span><span class="sxs-lookup"><span data-stu-id="b6b90-284">Collection-valued navigation properties support one-to-many or many-to-many relationships.</span></span> <span data-ttu-id="b6b90-285">For example, in our sample data, the account has a relationship with many contacts via the `contact_customer_accounts` attribute.</span><span class="sxs-lookup"><span data-stu-id="b6b90-285">For example, in our sample data, the account has a relationship with many contacts via the `contact_customer_accounts` attribute.</span></span>  
  
 <span data-ttu-id="b6b90-286">Using the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, we can create a query to get information about the account and expand information about its contacts.</span><span class="sxs-lookup"><span data-stu-id="b6b90-286">Using the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />, we can create a query to get information about the account and expand information about its contacts.</span></span> <span data-ttu-id="b6b90-287">In this case, the `Contoso, Ltd. (sample)` is associated to nine other contacts via the `contact_customer_accounts` collection-valued navigation property.</span><span class="sxs-lookup"><span data-stu-id="b6b90-287">In this case, the `Contoso, Ltd. (sample)` is associated to nine other contacts via the `contact_customer_accounts` collection-valued navigation property.</span></span>  
  
 <span data-ttu-id="b6b90-288">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-288">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/accounts(86546951-c543-e611-80d5-00155da84802)?$select=name&$expand=contact_customer_accounts($select=fullname,jobtitle,annualincome) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-289">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-289">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 4073  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,contact_customer_accounts,contact_customer_accounts(fullname,jobtitle,annualincome))/$entity",  
   "@odata.etag":"W/\"620921\"",  
   "name":"Contoso, Ltd. (sample)",  
   "accountid":"86546951-c543-e611-80d5-00155da84802",  
   "contact_customer_accounts":[  
      {  
         "@odata.etag":"W/\"620847\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"8e546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620849\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"92546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620851\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"96546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620853\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9a546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620855\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9e546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620857\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a2546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620859\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a6546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620861\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"aa546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620863\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"ae546951-c543-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-290">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-290">**Console output**</span></span>  
  
```  
Account 'Contoso, Ltd. (sample)' has the following contact customers:  
    1) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    2) Nancy Anderson (sample), Activities Manager, $55,500.00  
    3) Maria Cambell (sample), Accounts Manager, $31,000.00  
    4) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    5) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    6) Robert Lyon (sample), Senior Technician, $78,000.00  
    7) Paul Cannon (sample), Ski Instructor, $68,500.00  
    8) Rene Valdes (sample), Data Analyst III, $86,000.00  
    9) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
### <a name="expand-on-multiple-navigation-properties"></a><span data-ttu-id="b6b90-291">Expand on multiple navigation properties</span><span class="sxs-lookup"><span data-stu-id="b6b90-291">Expand on multiple navigation properties</span></span>  
 <span data-ttu-id="b6b90-292">You can expand on as many navigation properties as the query requires.</span><span class="sxs-lookup"><span data-stu-id="b6b90-292">You can expand on as many navigation properties as the query requires.</span></span> <span data-ttu-id="b6b90-293">However, the `$expand` option can only go one level deep.</span><span class="sxs-lookup"><span data-stu-id="b6b90-293">However, the `$expand` option can only go one level deep.</span></span>  
  
 <span data-ttu-id="b6b90-294">This example expands the `primarycontactid`, `contact_customer_accounts`, and `Account_Tasks` navigation properties of the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="b6b90-294">This example expands the `primarycontactid`, `contact_customer_accounts`, and `Account_Tasks` navigation properties of the <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />.</span></span>  <span data-ttu-id="b6b90-295">This query returns a response containing information about the account and two collections: a contacts collection and  a tasks collection.</span><span class="sxs-lookup"><span data-stu-id="b6b90-295">This query returns a response containing information about the account and two collections: a contacts collection and  a tasks collection.</span></span> <span data-ttu-id="b6b90-296">The sample code will process these collections separately.</span><span class="sxs-lookup"><span data-stu-id="b6b90-296">The sample code will process these collections separately.</span></span>  
  
 <span data-ttu-id="b6b90-297">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-297">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/accounts(86546951-c543-e611-80d5-00155da84802)?$select=name&$expand=primarycontactid($select=fullname,jobtitle,annualincome),contact_customer_accounts($select=fullname,jobtitle,annualincome),Account_Tasks($select=subject,description) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-298">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-298">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Preference-Applied: odata.maxpagesize=10  
Content-Length: 5093  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,primarycontactid,contact_customer_accounts,Account_Tasks,primarycontactid(fullname,jobtitle,annualincome),contact_customer_accounts(fullname,jobtitle,annualincome),Account_Tasks(subject,description))/$entity",  
   "@odata.etag":"W/\"620921\"",  
   "name":"Contoso, Ltd. (sample)",  
   "accountid":"86546951-c543-e611-80d5-00155da84802",  
   "primarycontactid":{  
      "@odata.etag":"W/\"620726\"",  
      "fullname":"Yvonne McKay (sample)",  
      "jobtitle":"Coffee Master",  
      "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
      "annualincome":45000.0000,  
      "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
      "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
      "contactid":"87546951-c543-e611-80d5-00155da84802"  
   },  
   "contact_customer_accounts":[  
      {  
         "@odata.etag":"W/\"620847\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"8e546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620849\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"92546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620851\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"96546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620853\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9a546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620855\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9e546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620857\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a2546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620859\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a6546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620861\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"aa546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620863\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"ae546951-c543-e611-80d5-00155da84802"  
      }  
   ],  
   "Account_Tasks":[  
      {  
         "@odata.etag":"W/\"620840\"",  
         "subject":"Task 1",  
         "description":"Task 1 description",  
         "activityid":"8b546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620842\"",  
         "subject":"Task 2",  
         "description":"Task 2 description",  
         "activityid":"8c546951-c543-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"620844\"",  
         "subject":"Task 3",  
         "description":"Task 3 description",  
         "activityid":"8d546951-c543-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-299">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-299">**Console output**</span></span>  
  
```  
-- Expanding multiple property types in one request --   
Account 'Contoso, Ltd. (sample)' has the following primary contact person:  
    Fullname: 'Yvonne McKay (sample)'   
    Jobtitle: 'Coffee Master'   
    Annualincome: '45000'  
Account 'Contoso, Ltd. (sample)' has the following related contacts:  
    1) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    2) Nancy Anderson (sample), Activities Manager, $55,500.00  
    3) Maria Cambell (sample), Accounts Manager, $31,000.00  
    4) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    5) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    6) Robert Lyon (sample), Senior Technician, $78,000.00  
    7) Paul Cannon (sample), Ski Instructor, $68,500.00  
    8) Rene Valdes (sample), Data Analyst III, $86,000.00  
    9) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
Account 'Contoso, Ltd. (sample)' has the following tasks:  
    1) Task 1, Task 1 description  
    2) Task 2, Task 2 description  
    3) Task 3, Task 3 description  
```  
  
<a name="bkmk_fetchxml"></a>   
## <a name="fetchxml-queries"></a><span data-ttu-id="b6b90-300">FetchXML queries</span><span class="sxs-lookup"><span data-stu-id="b6b90-300">FetchXML queries</span></span>  
 <span data-ttu-id="b6b90-301">Besides query filter operations, the Web API also supports FetchXML queries.</span><span class="sxs-lookup"><span data-stu-id="b6b90-301">Besides query filter operations, the Web API also supports FetchXML queries.</span></span> <span data-ttu-id="b6b90-302">FetchXml provides an alternative way to define queries and additional options to perform aggregations.</span><span class="sxs-lookup"><span data-stu-id="b6b90-302">FetchXml provides an alternative way to define queries and additional options to perform aggregations.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-303">[Build queries with FetchXML](../org-service/build-queries-fetchxml.md)</span><span class="sxs-lookup"><span data-stu-id="b6b90-303">[Build queries with FetchXML](../org-service/build-queries-fetchxml.md)</span></span>  
  
 <span data-ttu-id="b6b90-304">To use fetch xml you must compose a string representing the query.</span><span class="sxs-lookup"><span data-stu-id="b6b90-304">To use fetch xml you must compose a string representing the query.</span></span> <span data-ttu-id="b6b90-305">Make sure the query string conforms to the [FetchXML schema](../org-service/fetchxml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b6b90-305">Make sure the query string conforms to the [FetchXML schema](../org-service/fetchxml-schema.md).</span></span> <span data-ttu-id="b6b90-306">Before you include the string in the URL you must URL encode the string.</span><span class="sxs-lookup"><span data-stu-id="b6b90-306">Before you include the string in the URL you must URL encode the string.</span></span>  
  
 <span data-ttu-id="b6b90-307">All the query options we would normally define such as `$select`, `$filter`, and `$orderby` are now defined in the XML.</span><span class="sxs-lookup"><span data-stu-id="b6b90-307">All the query options we would normally define such as `$select`, `$filter`, and `$orderby` are now defined in the XML.</span></span> <span data-ttu-id="b6b90-308">In this operation, we query for all contacts whose `fullname` matches `(sample)`, and order the results descending by `fullname`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-308">In this operation, we query for all contacts whose `fullname` matches `(sample)`, and order the results descending by `fullname`.</span></span> <span data-ttu-id="b6b90-309">This is the XML for this query.</span><span class="sxs-lookup"><span data-stu-id="b6b90-309">This is the XML for this query.</span></span>  
  
```xml  
<fetch mapping="logical" output-format="xml-platform" version="1.0" distinct="false">  
  <entity name="contact">  
    <attribute name="fullname" />  
    <attribute name="jobtitle" />  
    <attribute name="annualincome" />  
    <order descending="true"  
           attribute="fullname" />  
    <filter type="and">  
      <condition value="%(sample)%"  
                 attribute="fullname"  
                 operator="like" />  
    </filter>  
  </entity>  
</fetch>  
```  
  
 <span data-ttu-id="b6b90-310">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-310">**HTTP Request**</span></span>  
  
 <span data-ttu-id="b6b90-311">The request query string is sent to the server in encoded form.</span><span class="sxs-lookup"><span data-stu-id="b6b90-311">The request query string is sent to the server in encoded form.</span></span> <span data-ttu-id="b6b90-312">The encoded header looks like this.</span><span class="sxs-lookup"><span data-stu-id="b6b90-312">The encoded header looks like this.</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?fetchXml=%253Cfetch%2520mapping%253D%2522logical%2522%2520output-format%253D%2522xml-platform%2522%2520version%253D%25221.0%2522%2520distinct%253D%2522false%2522%253E%2520%2520%2520%253Centity%2520name%253D%2522contact%2522%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522fullname%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522jobtitle%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522annualincome%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Corder%2520descending%253D%2522true%2522%2520attribute%253D%2522fullname%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cfilter%2520type%253D%2522and%2522%253E%2520%2520%2520%2520%2520%2520%2520%253Ccondition%2520value%253D%2522%2525(sample)%2525%2522%2520attribute%253D%2522fullname%2522%2520operator%253D%2522like%2522%2520%252F%253E%2520%2520%2520%2520%2520%253C%252Ffilter%253E%2520%2520%2520%253C%252Fentity%253E%2520%253C%252Ffetch%253E%2520 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-313">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-313">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Content-Length: 4345  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome,_transactioncurrencyid_value,transactioncurrencyid,contactid)",  
   "value":[  
      {  
         "@odata.etag":"W/\"621502\"",  
         "fullname":"Yvonne McKay (sample)",  
         "jobtitle":"Coffee Master",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$45,000.00",  
         "annualincome":45000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9255b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621627\"",  
         "fullname":"Susanna Stubberod (sample)",  
         "jobtitle":"Senior Purchaser",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$52,000.00",  
         "annualincome":52000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9955b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621635\"",  
         "fullname":"Scott Konersmann (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$38,000.00",  
         "annualincome":38000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a955b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621637\"",  
         "fullname":"Robert Lyon (sample)",  
         "jobtitle":"Senior Technician",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$78,000.00",  
         "annualincome":78000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"ad55b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621641\"",  
         "fullname":"Rene Valdes (sample)",  
         "jobtitle":"Data Analyst III",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$86,000.00",  
         "annualincome":86000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"b555b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621639\"",  
         "fullname":"Paul Cannon (sample)",  
         "jobtitle":"Ski Instructor",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$68,500.00",  
         "annualincome":68500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"b155b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621629\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"9d55b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621633\"",  
         "fullname":"Nancy Anderson (sample)",  
         "jobtitle":"Logistics Specialist",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$63,500.00",  
         "annualincome":63500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a555b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621631\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a155b257-c843-e611-80d5-00155da84802"  
      },  
      {  
         "@odata.etag":"W/\"621643\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"b955b257-c843-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-314">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-314">**Console output**</span></span>  
  
```  
Contacts Fetched by fullname containing '(sample)':  
    1) Yvonne McKay (sample), Coffee Master, $45,000.00  
    2) Susanna Stubberod (sample), Senior Purchaser, $52,000.00  
    3) Scott Konersmann (sample), Accounts Manager, $38,000.00  
    4) Robert Lyon (sample), Senior Technician, $78,000.00  
    5) Rene Valdes (sample), Data Analyst III, $86,000.00  
    6) Paul Cannon (sample), Ski Instructor, $68,500.00  
    7) Nancy Anderson (sample), Activities Manager, $55,500.00  
    8) Nancy Anderson (sample), Logistics Specialist, $63,500.00  
    9) Maria Cambell (sample), Accounts Manager, $31,000.00  
    10) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
### <a name="fetchxml-pagination"></a><span data-ttu-id="b6b90-315">FetchXML pagination</span><span class="sxs-lookup"><span data-stu-id="b6b90-315">FetchXML pagination</span></span>  
 <span data-ttu-id="b6b90-316">The way FetchXML handles paging is different than how query filter handles it.</span><span class="sxs-lookup"><span data-stu-id="b6b90-316">The way FetchXML handles paging is different than how query filter handles it.</span></span> <span data-ttu-id="b6b90-317">In FetchXML, you can specify a `count` attribute that will indicate how many results to return per page.</span><span class="sxs-lookup"><span data-stu-id="b6b90-317">In FetchXML, you can specify a `count` attribute that will indicate how many results to return per page.</span></span> <span data-ttu-id="b6b90-318">In the same request, you use the `page` attribute to specify the page number you want.</span><span class="sxs-lookup"><span data-stu-id="b6b90-318">In the same request, you use the `page` attribute to specify the page number you want.</span></span> <span data-ttu-id="b6b90-319">This operation will make a request for page 3 from the previous FetchXML sample.</span><span class="sxs-lookup"><span data-stu-id="b6b90-319">This operation will make a request for page 3 from the previous FetchXML sample.</span></span> <span data-ttu-id="b6b90-320">Based on our sample data, we should have ten contacts in our result.</span><span class="sxs-lookup"><span data-stu-id="b6b90-320">Based on our sample data, we should have ten contacts in our result.</span></span> <span data-ttu-id="b6b90-321">Breaking each page down to only four entities per page, we should have three pages.</span><span class="sxs-lookup"><span data-stu-id="b6b90-321">Breaking each page down to only four entities per page, we should have three pages.</span></span> <span data-ttu-id="b6b90-322">Page 3 should contain only two entities.</span><span class="sxs-lookup"><span data-stu-id="b6b90-322">Page 3 should contain only two entities.</span></span> <span data-ttu-id="b6b90-323">If we then ask for page 4, the system will return zero results.</span><span class="sxs-lookup"><span data-stu-id="b6b90-323">If we then ask for page 4, the system will return zero results.</span></span>  
  
```xml  
<fetch mapping="logical"  
       output-format="xml-platform"  
       version="1.0"  
       distinct="false"  
       page="3"  
       count="4">  
  <entity name="contact">  
    <attribute name="fullname" />  
    <attribute name="jobtitle" />  
    <attribute name="annualincome" />  
    <order descending="true"  
           attribute="fullname" />  
    <filter type="and">  
      <condition value="%(sample)%"  
                 attribute="fullname"  
                 operator="like" />  
    </filter>  
  </entity>  
</fetch>  
```  
  
 <span data-ttu-id="b6b90-324">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-324">**HTTP Request**</span></span>  
  
 <span data-ttu-id="b6b90-325">The request query string is sent to the server in encoded form.</span><span class="sxs-lookup"><span data-stu-id="b6b90-325">The request query string is sent to the server in encoded form.</span></span> <span data-ttu-id="b6b90-326">The encoded header looks like this.</span><span class="sxs-lookup"><span data-stu-id="b6b90-326">The encoded header looks like this.</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?fetchXml=%253Cfetch%2520mapping%253D%2522logical%2522%2520output-format%253D%2522xml-platform%2522%2520version%253D%25221.0%2522%2520distinct%253D%2522false%2522%2520page%253D%25223%2522%2520count%253D%25224%2522%253E%2520%2520%2520%253Centity%2520name%253D%2522contact%2522%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522fullname%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522jobtitle%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cattribute%2520name%253D%2522annualincome%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Corder%2520descending%253D%2522true%2522%2520attribute%253D%2522fullname%2522%2520%252F%253E%2520%2520%2520%2520%2520%253Cfilter%2520type%253D%2522and%2522%253E%2520%2520%2520%2520%2520%2520%2520%253Ccondition%2520value%253D%2522%2525(sample)%2525%2522%2520attribute%253D%2522fullname%2522%2520operator%253D%2522like%2522%2520%252F%253E%2520%2520%2520%2520%2520%253C%252Ffilter%253E%2520%2520%2520%253C%252Fentity%253E%2520%253C%252Ffetch%253E%2520 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
  
```  
  
 <span data-ttu-id="b6b90-327">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-327">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Content-Length: 1037  
  
{   
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,jobtitle,annualincome,_transactioncurrencyid_value,transactioncurrencyid,contactid)",  
   "value":[   
      {   
         "@odata.etag":"W/\"621631\"",  
         "fullname":"Maria Cambell (sample)",  
         "jobtitle":"Accounts Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$31,000.00",  
         "annualincome":31000.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"a155b257-c843-e611-80d5-00155da84802"  
      },  
      {   
         "@odata.etag":"W/\"621643\"",  
         "fullname":"Jim Glynn (sample)",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802",  
         "contactid":"b955b257-c843-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-328">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-328">**Console output**</span></span>  
  
```  
Contacts Fetched by fullname containing '(sample)' - Page 3:  
    1) Maria Cambell (sample), Accounts Manager, $31,000.00  
    2) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
```  
  
<a name="bkmk_predefinedqueries"></a>   
## <a name="predefined-queries"></a><span data-ttu-id="b6b90-329">Predefined queries</span><span class="sxs-lookup"><span data-stu-id="b6b90-329">Predefined queries</span></span>  
 <span data-ttu-id="b6b90-330">You can use the Web API to execute predefined queries.</span><span class="sxs-lookup"><span data-stu-id="b6b90-330">You can use the Web API to execute predefined queries.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="b6b90-331">[Retrieve and execute predefined queries](retrieve-and-execute-predefined-queries.md).</span><span class="sxs-lookup"><span data-stu-id="b6b90-331">[Retrieve and execute predefined queries](retrieve-and-execute-predefined-queries.md).</span></span>  
  
### <a name="saved-query"></a><span data-ttu-id="b6b90-332">Saved query</span><span class="sxs-lookup"><span data-stu-id="b6b90-332">Saved query</span></span>  
 <span data-ttu-id="b6b90-333">In this operation, we will make a request for the `savedqueryid` GUID of the saved query named **Active Accounts**.</span><span class="sxs-lookup"><span data-stu-id="b6b90-333">In this operation, we will make a request for the `savedqueryid` GUID of the saved query named **Active Accounts**.</span></span> <span data-ttu-id="b6b90-334">Then using the GUID and the `savedQuery` parameter, we will query for a list of active accounts.</span><span class="sxs-lookup"><span data-stu-id="b6b90-334">Then using the GUID and the `savedQuery` parameter, we will query for a list of active accounts.</span></span>  
  
 <span data-ttu-id="b6b90-335">Getting the saved query's GUID.</span><span class="sxs-lookup"><span data-stu-id="b6b90-335">Getting the saved query's GUID.</span></span>  
  
 <span data-ttu-id="b6b90-336">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-336">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/savedqueries?$select=name,savedqueryid&$filter=name%20eq%20'Active%20Accounts' HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
Referer: http://localhost:1469/WebAPIQuery.html  
```  
  
 <span data-ttu-id="b6b90-337">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-337">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 251  
  
{   
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#savedqueries(name,savedqueryid)",  
   "value":[   
      {   
         "@odata.etag":"W/\"443067\"",  
         "name":"Active Accounts",  
         "savedqueryid":"00000000-0000-0000-00aa-000010001002"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-338">Getting the saved query's content using the `savedQuery` parameter</span><span class="sxs-lookup"><span data-stu-id="b6b90-338">Getting the saved query's content using the `savedQuery` parameter</span></span>  
  
 <span data-ttu-id="b6b90-339">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-339">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/accounts?savedQuery=00000000-0000-0000-00aa-000010001002 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
```  
  
 <span data-ttu-id="b6b90-340">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-340">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
REQ_ID: 2bc532c4-d445-44cd-adae-1909a616d6bc  
OData-Version: 4.0  
Preference-Applied: odata.include-annotations="OData.Community.Display.V1.FormattedValue"  
Content-Length: 446  
  
{   
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#accounts(name,_primarycontactid_value,primarycontactid,accountid)",  
   "value":[   
      {   
         "@odata.etag":"W/\"621613\"",  
         "name":"Contoso, Ltd. (sample)",  
         "_primarycontactid_value@OData.Community.Display.V1.FormattedValue":"Yvonne McKay (sample)",  
         "_primarycontactid_value":"9255b257-c843-e611-80d5-00155da84802",  
         "accountid":"9155b257-c843-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-341">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-341">**Console output**</span></span>  
  
```  
-- Saved Query --   
Saved Query (Active Accounts):  
    1) Contoso, Ltd. (sample)  
```  
  
### <a name="user-query"></a><span data-ttu-id="b6b90-342">User query</span><span class="sxs-lookup"><span data-stu-id="b6b90-342">User query</span></span>  
 <span data-ttu-id="b6b90-343">This sample creates a user query, executes it, then deletes it from the system.</span><span class="sxs-lookup"><span data-stu-id="b6b90-343">This sample creates a user query, executes it, then deletes it from the system.</span></span> <span data-ttu-id="b6b90-344">This user query is asking for any contacts whose `fullname` contains `(sample)`, `jobtitle` contains `manager`, and `annualincome` greater than `55000`.</span><span class="sxs-lookup"><span data-stu-id="b6b90-344">This user query is asking for any contacts whose `fullname` contains `(sample)`, `jobtitle` contains `manager`, and `annualincome` greater than `55000`.</span></span> <span data-ttu-id="b6b90-345">Our sample data has two contacts matching this query.</span><span class="sxs-lookup"><span data-stu-id="b6b90-345">Our sample data has two contacts matching this query.</span></span>  
  
 <span data-ttu-id="b6b90-346">Getting the user query's GUID.</span><span class="sxs-lookup"><span data-stu-id="b6b90-346">Getting the user query's GUID.</span></span>  
  
 <span data-ttu-id="b6b90-347">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-347">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/userqueries?$select=name,userqueryid,&$filter=name%20eq%20'My%20User%20Query' HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Referer: http://localhost:1469/WebAPIQuery.html  
  
```  
  
 <span data-ttu-id="b6b90-348">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-348">**HTTP Response**</span></span>  
  
```  
Pragma: no-cache  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 246  
  
{   
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#userqueries(name,userqueryid)",  
   "value":[   
      {   
         "@odata.etag":"W/\"621698\"",  
         "name":"My User Query",  
         "userqueryid":"7ec390ab-c943-e611-80d5-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-349">Getting the user query's content passing the GUID value with the `userQuery` parameter.</span><span class="sxs-lookup"><span data-stu-id="b6b90-349">Getting the user query's content passing the GUID value with the `userQuery` parameter.</span></span>  
  
 <span data-ttu-id="b6b90-350">**HTTP Request**</span><span class="sxs-lookup"><span data-stu-id="b6b90-350">**HTTP Request**</span></span>  
  
```  
GET http://[Organization URI]/api/data/v9.0/contacts?userQuery=7ec390ab-c943-e611-80d5-00155da84802 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Prefer: odata.maxpagesize=10, odata.include-annotations=OData.Community.Display.V1.FormattedValue  
  
```  
  
 <span data-ttu-id="b6b90-351">**HTTP Response**</span><span class="sxs-lookup"><span data-stu-id="b6b90-351">**HTTP Response**</span></span>  
  
```  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 1040  
  
{   
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#contacts(fullname,contactid,jobtitle,annualincome,_transactioncurrencyid_value,transactioncurrencyid)",  
   "value":[   
      {   
         "@odata.etag":"W/\"621643\"",  
         "fullname":"Jim Glynn (sample)",  
         "contactid":"b955b257-c843-e611-80d5-00155da84802",  
         "jobtitle":"Senior International Sales Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$81,400.00",  
         "annualincome":81400.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802"  
      },  
      {   
         "@odata.etag":"W/\"621629\"",  
         "fullname":"Nancy Anderson (sample)",  
         "contactid":"9d55b257-c843-e611-80d5-00155da84802",  
         "jobtitle":"Activities Manager",  
         "annualincome@OData.Community.Display.V1.FormattedValue":"$55,500.00",  
         "annualincome":55500.0000,  
         "_transactioncurrencyid_value@OData.Community.Display.V1.FormattedValue":"US Dollar",  
         "_transactioncurrencyid_value":"518c78c9-d3f6-e511-80d0-00155da84802"  
      }  
   ]  
}  
```  
  
 <span data-ttu-id="b6b90-352">**Console output**</span><span class="sxs-lookup"><span data-stu-id="b6b90-352">**Console output**</span></span>  
  
```  
-- User Query --   
Saved User Query:  
    1) Jim Glynn (sample), Senior International Sales Manager, $81,400.00  
    2) Nancy Anderson (sample), Activities Manager, $55,500.00  
```  
  
### <a name="see-also"></a><span data-ttu-id="b6b90-353">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b6b90-353">See also</span></span>  
 <span data-ttu-id="b6b90-354">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="b6b90-354">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="b6b90-355">[Query Data using the Web API](query-data-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="b6b90-355">[Query Data using the Web API](query-data-web-api.md) </span></span>  
 <span data-ttu-id="b6b90-356">[Retrieve and execute predefined queries](retrieve-and-execute-predefined-queries.md) </span><span class="sxs-lookup"><span data-stu-id="b6b90-356">[Retrieve and execute predefined queries](retrieve-and-execute-predefined-queries.md) </span></span>  
 <span data-ttu-id="b6b90-357">[Web API Query Data Sample (C#)](web-api-query-data-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="b6b90-357">[Web API Query Data Sample (C#)](web-api-query-data-sample-csharp.md) </span></span>  
 [<span data-ttu-id="b6b90-358">Web API Query Data Sample (Client-side JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b6b90-358">Web API Query Data Sample (Client-side JavaScript)</span></span>](web-api-query-data-sample-client-side-javascript.md)
