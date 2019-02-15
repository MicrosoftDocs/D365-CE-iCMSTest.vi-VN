---
title: Web API Functions and Actions Sample (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This group of samples demonstrates how to perform bound and unbound functions and actions, including custom actions, using the Dynamics 365 for Customer Engagement Web API. These are implemented using Client-side JavaScript and C#
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 953c3137-6171-4e6e-b249-6a96221c6e96
caps.latest.revision: 16
author: JimDaly
ms.author: jdaly
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 587f2bb091e25f4ab65c24cbe1dcc5856a32ce28
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386091"
---
# <a name="web-api-functions-and-actions-sample"></a><span data-ttu-id="ef8ae-104">Web API Functions and Actions Sample</span><span class="sxs-lookup"><span data-stu-id="ef8ae-104">Web API Functions and Actions Sample</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="ef8ae-105">This group of samples demonstrate how to perform bound and unbound functions and actions, including custom actions, using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-105">This group of samples demonstrate how to perform bound and unbound functions and actions, including custom actions, using the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps Web API.</span></span> <span data-ttu-id="ef8ae-106">This sample is implemented as a separate project for the following languages:</span><span class="sxs-lookup"><span data-stu-id="ef8ae-106">This sample is implemented as a separate project for the following languages:</span></span>  
  
- [<span data-ttu-id="ef8ae-107">Functions and Actions Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-107">Functions and Actions Sample (C#)</span></span>](web-api-functions-actions-sample-csharp.md)  
  
  <span data-ttu-id="ef8ae-108">This topic explains the structure and content of the sample at a higher, language-neutral level.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-108">This topic explains the structure and content of the sample at a higher, language-neutral level.</span></span> <span data-ttu-id="ef8ae-109">Review the linked sample topics above for language-specific implementation details about how to perform the operations described in this topic.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-109">Review the linked sample topics above for language-specific implementation details about how to perform the operations described in this topic.</span></span>  
  
<a name="bkmk_demonstrates"></a>  
 
## <a name="demonstrates"></a><span data-ttu-id="ef8ae-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="ef8ae-110">Demonstrates</span></span>  

 <span data-ttu-id="ef8ae-111">This sample is divided into the following principal sections, containing Web API functions and actions operations which are discussed in greater detail in the associated conceptual topics.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-111">This sample is divided into the following principal sections, containing Web API functions and actions operations which are discussed in greater detail in the associated conceptual topics.</span></span>  
  
|<span data-ttu-id="ef8ae-112">Topic section</span><span class="sxs-lookup"><span data-stu-id="ef8ae-112">Topic section</span></span>|<span data-ttu-id="ef8ae-113">Associated topic(s)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-113">Associated topic(s)</span></span>|  
|-------------------|---------------------------|  
|[<span data-ttu-id="ef8ae-114">Dữ liệu mẫu</span><span class="sxs-lookup"><span data-stu-id="ef8ae-114">Sample data</span></span>](#bkmk_sampleData)||  
|[<span data-ttu-id="ef8ae-115">Using unbound function with no parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-115">Using unbound function with no parameters</span></span>](#bkmk_unboundFunctionNoParams)|[<span data-ttu-id="ef8ae-116">Unbound functions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-116">Unbound functions</span></span>](use-web-api-functions.md#bkmk_unboundFunctions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" />|  
|[<span data-ttu-id="ef8ae-117">Using unbound function with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-117">Using unbound function with parameters</span></span>](#bkmk_unboundFunctionWithParams)|[<span data-ttu-id="ef8ae-118">Unbound functions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-118">Unbound functions</span></span>](use-web-api-functions.md#bkmk_unboundFunctions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.GetTimeZoneCodeByLocalizedName?text=GetTimeZoneCodeByLocalizedName Function" />|  
|[<span data-ttu-id="ef8ae-119">Using bound function with no parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-119">Using bound function with no parameters</span></span>](#bkmk_boundFunctionWithParams)|[<span data-ttu-id="ef8ae-120">Bound functions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-120">Bound functions</span></span>](use-web-api-functions.md#bkmk_boundFunctions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncident?text=CalculateTotalTimeIncident Function" />|  
|[<span data-ttu-id="ef8ae-121">Using unbound action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-121">Using unbound action with parameters</span></span>](#bkmk_unboundActionWithParams)|[<span data-ttu-id="ef8ae-122">Unbound actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-122">Unbound actions</span></span>](use-web-api-actions.md#bkmk_unboundActions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.WinOpportunity?text=WinOpportunity Action" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.opportunity?text=opportunity EntityType" />|  
|[<span data-ttu-id="ef8ae-123">Using bound action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-123">Using bound action with parameters</span></span>](#bkmk_boundActionWithParams)|[<span data-ttu-id="ef8ae-124">Bound actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-124">Bound actions</span></span>](use-web-api-actions.md#bkmk_boundActions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" /><br /><br /> <xref href="Microsoft.Dynamics.CRM.letter?text=letter EntityType" />|  
|[<span data-ttu-id="ef8ae-125">Using bound custom action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-125">Using bound custom action with parameters</span></span>](#bkmk_boundCustomActionWithParams)|[<span data-ttu-id="ef8ae-126">Use a custom action</span><span class="sxs-lookup"><span data-stu-id="ef8ae-126">Use a custom action</span></span>](use-web-api-actions.md#bkmk_customActions)<br /><br /> [<span data-ttu-id="ef8ae-127">Bound actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-127">Bound actions</span></span>](use-web-api-actions.md#bkmk_boundActions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />|  
|[<span data-ttu-id="ef8ae-128">Using unbound custom action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-128">Using unbound custom action with parameters</span></span>](#bkmk_unboundCustomActionWithParams)|[<span data-ttu-id="ef8ae-129">Use a custom action</span><span class="sxs-lookup"><span data-stu-id="ef8ae-129">Use a custom action</span></span>](use-web-api-actions.md#bkmk_customActions)<br /><br /> [<span data-ttu-id="ef8ae-130">Unbound actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-130">Unbound actions</span></span>](use-web-api-actions.md#bkmk_unboundActions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.account?text=account EntityType" />|  
|[<span data-ttu-id="ef8ae-131">Handling custom action exceptions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-131">Handling custom action exceptions</span></span>](#bkmk_boundCustomActionErrorHandling)|[<span data-ttu-id="ef8ae-132">Use a custom action</span><span class="sxs-lookup"><span data-stu-id="ef8ae-132">Use a custom action</span></span>](use-web-api-actions.md#bkmk_customActions)<br /><br /> [<span data-ttu-id="ef8ae-133">Unbound actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-133">Unbound actions</span></span>](use-web-api-actions.md#bkmk_unboundActions)<br /><br /> <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />|  
  
 <span data-ttu-id="ef8ae-134">The following sections contain a brief discussion of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations performed, along with the corresponding HTTP messages and associated console output.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-134">The following sections contain a brief discussion of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API operations performed, along with the corresponding HTTP messages and associated console output.</span></span>  
  
<a name="bkmk_sampleData"></a>
   
## <a name="sample-data"></a><span data-ttu-id="ef8ae-135">Dữ liệu mẫu</span><span class="sxs-lookup"><span data-stu-id="ef8ae-135">Sample data</span></span>  

 <span data-ttu-id="ef8ae-136">To ensure the operations in this sample work properly, we first create sample data on the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-136">To ensure the operations in this sample work properly, we first create sample data on the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] server.</span></span> <span data-ttu-id="ef8ae-137">These sample data will be deleted from the server unless the user chooses to not delete them.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-137">These sample data will be deleted from the server unless the user chooses to not delete them.</span></span> <span data-ttu-id="ef8ae-138">The data in this sample are created individually as follows.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-138">The data in this sample are created individually as follows.</span></span>  
  
-   <span data-ttu-id="ef8ae-139">Create an account (e.g.: `Fourth Coffee`) and associate it with an incident that has three 30 minute tasks (90 minutes total).</span><span class="sxs-lookup"><span data-stu-id="ef8ae-139">Create an account (e.g.: `Fourth Coffee`) and associate it with an incident that has three 30 minute tasks (90 minutes total).</span></span> <span data-ttu-id="ef8ae-140">After the tasks are created, they are then marked as completed.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-140">After the tasks are created, they are then marked as completed.</span></span> <span data-ttu-id="ef8ae-141">The operation will calculate the total time it took to complete these three tasks.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-141">The operation will calculate the total time it took to complete these three tasks.</span></span>  
  
    ```json  
    {  
      title: "Sample Case",  
      "customerid_account@odata.bind": accountUri,  
      Incident_Tasks: [  
       {  
        subject: "Task 1",  
        actualdurationminutes: 30  
       },  
       {  
        subject: "Task 2",  
        actualdurationminutes: 30  
       },  
       {  
        subject: "Task 3",  
        actualdurationminutes: 30  
       }  
      ]  
     };  
    ```  
  
-   <span data-ttu-id="ef8ae-142">Create an account and associate it with an opportunity.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-142">Create an account and associate it with an opportunity.</span></span> <span data-ttu-id="ef8ae-143">This opportunity will be mark as won in the sample operation.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-143">This opportunity will be mark as won in the sample operation.</span></span>  
  
    ```json  
    {  
     name: "Sample Account for WebAPIFunctionsAndActions sample",  
     opportunity_customer_accounts: [{  
      name: "Opportunity to win"  
     }]  
    };  
    ```  
  
-   <span data-ttu-id="ef8ae-144">Create a letter activity.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-144">Create a letter activity.</span></span> <span data-ttu-id="ef8ae-145">The letter will be added to the current user's queue in the sample operation.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-145">The letter will be added to the current user's queue in the sample operation.</span></span>  
  
    ```json  
    {  
      description: "Example letter"  
    }  
    ```  
  
-   <span data-ttu-id="ef8ae-146">Create a contact to use with a custom action `sample_AddNoteToContact` in the sample operation.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-146">Create a contact to use with a custom action `sample_AddNoteToContact` in the sample operation.</span></span>  
  
    ```json  
    {  
      firstname: "Jon",  
      lastname: "Fogg"  
    }  
    ```  
  
<a name="bkmk_sampleOperations"></a>
   
## <a name="sample-operations"></a><span data-ttu-id="ef8ae-147">Sample operations</span><span class="sxs-lookup"><span data-stu-id="ef8ae-147">Sample operations</span></span>  

 <span data-ttu-id="ef8ae-148">The sample operations in this topic are organized in the following ways.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-148">The sample operations in this topic are organized in the following ways.</span></span>  
  
-   <span data-ttu-id="ef8ae-149">Working with functions: These operations show bound and unbound functions that either accept parameters or not.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-149">Working with functions: These operations show bound and unbound functions that either accept parameters or not.</span></span>  
  
-   <span data-ttu-id="ef8ae-150">Working with actions: These operations show bound and unbound actions that either accept parameters or not.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-150">Working with actions: These operations show bound and unbound actions that either accept parameters or not.</span></span>  
  
-   <span data-ttu-id="ef8ae-151">Custom actions: These operations show bound and unbound actions and how to handle custom error exceptions.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-151">Custom actions: These operations show bound and unbound actions and how to handle custom error exceptions.</span></span>  
  
<a name="bkmk_workingWithFunctions"></a> 
  
## <a name="working-with-functions"></a><span data-ttu-id="ef8ae-152">Working with functions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-152">Working with functions</span></span>  

 <span data-ttu-id="ef8ae-153">[Functions](web-api-types-operations.md#bkmk_functions) are operations that do not have side effects.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-153">[Functions](web-api-types-operations.md#bkmk_functions) are operations that do not have side effects.</span></span> <span data-ttu-id="ef8ae-154">A function can be bound to an entity instance or an entity collection.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-154">A function can be bound to an entity instance or an entity collection.</span></span> <span data-ttu-id="ef8ae-155">Query functions are never bound.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-155">Query functions are never bound.</span></span> <span data-ttu-id="ef8ae-156">For more info, see [Use Web API functions](use-web-api-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ef8ae-156">For more info, see [Use Web API functions](use-web-api-functions.md).</span></span> <span data-ttu-id="ef8ae-157">This section shows samples of how bound and unbound functions are used and how parameters are passed in.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-157">This section shows samples of how bound and unbound functions are used and how parameters are passed in.</span></span>  
  
<a name="bkmk_unboundFunctionNoParams"></a>  
 
### <a name="using-unbound-function-with-no-parameters"></a><span data-ttu-id="ef8ae-158">Using unbound function with no parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-158">Using unbound function with no parameters</span></span> 
 
 <span data-ttu-id="ef8ae-159">Use an unbound function to retrieve the current user's full name by making use of the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-159">Use an unbound function to retrieve the current user's full name by making use of the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span></span> <span data-ttu-id="ef8ae-160">This operation demonstrates how to call an unbound function that does not accept parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-160">This operation demonstrates how to call an unbound function that does not accept parameters.</span></span> <span data-ttu-id="ef8ae-161">This operation returns the current user's full name.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-161">This operation returns the current user's full name.</span></span>  
  
 <span data-ttu-id="ef8ae-162">Getting the request and response for the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-162">Getting the request and response for the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span></span>  
  
 <span data-ttu-id="ef8ae-163">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-163">**Request**</span></span>  
  
```http  
GET http://[Organization URI]/api/data/v9.0/WhoAmI HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8   
```  
  
 <span data-ttu-id="ef8ae-164">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-164">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 273  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.WhoAmIResponse",  
   "BusinessUnitId":"0d6cc84a-d3f6-e511-80d0-00155da84802",  
   "UserId":"b08dc84a-d3f6-e511-80d0-00155da84802",  
   "OrganizationId":"0f47eae2-a906-4ae4-9215-f09875979f6a"  
}  
```  
  
<a name="bkmk_unboundFunctionWithParams"></a>
   
### <a name="using-unbound-function-with-parameters"></a><span data-ttu-id="ef8ae-165">Using unbound function with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-165">Using unbound function with parameters</span></span>  

 <span data-ttu-id="ef8ae-166">Use an unbound function to retrieve the time zone code.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-166">Use an unbound function to retrieve the time zone code.</span></span> <span data-ttu-id="ef8ae-167">This operation demonstrates how to call an unbound function that accept parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-167">This operation demonstrates how to call an unbound function that accept parameters.</span></span> <span data-ttu-id="ef8ae-168">This operation returns the current time zone code for the specified time zone.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-168">This operation returns the current time zone code for the specified time zone.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ef8ae-169">[Passing parameters to a function](use-web-api-functions.md#bkmk_passParametersToFunctions)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-169">[Passing parameters to a function](use-web-api-functions.md#bkmk_passParametersToFunctions)</span></span>  
  
 <span data-ttu-id="ef8ae-170">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-170">**Request**</span></span>  
  
```http  
GET http://[Organization URI]/api/data/v9.0/GetTimeZoneCodeByLocalizedName(LocalizedStandardName=@p1,LocaleId=@p2)?@p1='Pacific%20Standard%20Time'&@p2=1033 HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8 
```  
  
 <span data-ttu-id="ef8ae-171">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-171">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 154  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.GetTimeZoneCodeByLocalizedNameResponse",  
   "TimeZoneCode":4  
}  
```  
  
 <span data-ttu-id="ef8ae-172">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-172">**Console output**</span></span>  
  
```  
Unbound function: GetTimeZoneCodeByLocalizedName  
    Function returned time zone Pacific Standard Time, with code '4'.  
```  
  
<a name="bkmk_boundFunctionWithParams"></a>
   
### <a name="using-bound-function-with-no-parameters"></a><span data-ttu-id="ef8ae-173">Using bound function with no parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-173">Using bound function with no parameters</span></span>  

 <span data-ttu-id="ef8ae-174">Use a  bound function to retrieve the total time it took to complete all the tasks of an incident.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-174">Use a  bound function to retrieve the total time it took to complete all the tasks of an incident.</span></span> <span data-ttu-id="ef8ae-175">This operation demonstrates how to call a bound function that does not accept parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-175">This operation demonstrates how to call a bound function that does not accept parameters.</span></span> <span data-ttu-id="ef8ae-176">This operation returns the total minutes the incident took to close out all its tasks.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-176">This operation returns the total minutes the incident took to close out all its tasks.</span></span> <span data-ttu-id="ef8ae-177">This function also makes use of the incident data we created for this sample program.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-177">This function also makes use of the incident data we created for this sample program.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ef8ae-178">[Bound functions](use-web-api-functions.md#bkmk_boundFunctions)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-178">[Bound functions](use-web-api-functions.md#bkmk_boundFunctions)</span></span>  
  
 <span data-ttu-id="ef8ae-179">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-179">**Request**</span></span>  
  
```http  
GET http://[Organization URI]/api/data/v9.0/incidents(3d920da5-fb4a-e611-80d5-00155da84802)/Microsoft.Dynamics.CRM.CalculateTotalTimeIncident() HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
  
```  
  
 <span data-ttu-id="ef8ae-180">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-180">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 148  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse",  
   "TotalTime":90  
}  
```  
  
 <span data-ttu-id="ef8ae-181">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-181">**Console output**</span></span>  
  
```  
Bound function: CalculateTotalTimeIncident  
    Function returned 90 minutes - total duration of tasks associated with the incident.  
```  
  
<a name="bkmk_workingWithActions"></a> 
  
## <a name="working-with-actions"></a><span data-ttu-id="ef8ae-182">Working with actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-182">Working with actions</span></span>  

 <span data-ttu-id="ef8ae-183">[Actions](web-api-types-operations.md#bkmk_actions) are operations that allow side effects.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-183">[Actions](web-api-types-operations.md#bkmk_actions) are operations that allow side effects.</span></span> <span data-ttu-id="ef8ae-184">An action is either bound or unbound.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-184">An action is either bound or unbound.</span></span> <span data-ttu-id="ef8ae-185">For more info, see [Use Web API actions](use-web-api-actions.md).</span><span class="sxs-lookup"><span data-stu-id="ef8ae-185">For more info, see [Use Web API actions](use-web-api-actions.md).</span></span> <span data-ttu-id="ef8ae-186">This section shows samples of how bound and unbound actions are used and how parameters are passed in.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-186">This section shows samples of how bound and unbound actions are used and how parameters are passed in.</span></span> <span data-ttu-id="ef8ae-187">It also shows how custom actions are used and how to handle exceptions from these custom actions.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-187">It also shows how custom actions are used and how to handle exceptions from these custom actions.</span></span>  
  
<a name="bkmk_unboundActionWithParams"></a>
   
### <a name="using-unbound-action-with-parameters"></a><span data-ttu-id="ef8ae-188">Using unbound action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-188">Using unbound action with parameters</span></span> 
 
 <span data-ttu-id="ef8ae-189">Use an unbound action that takes a set of parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-189">Use an unbound action that takes a set of parameters.</span></span> <span data-ttu-id="ef8ae-190">This operation closes an opportunity and marks it as won by calling the <xref href="Microsoft.Dynamics.CRM.WinOpportunity?text=WinOpportunity Action" />.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-190">This operation closes an opportunity and marks it as won by calling the <xref href="Microsoft.Dynamics.CRM.WinOpportunity?text=WinOpportunity Action" />.</span></span> <span data-ttu-id="ef8ae-191">The <xref href="Microsoft.Dynamics.CRM.opportunity?text=opportunity EntityType" /> was created as sample data earlier in the program.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-191">The <xref href="Microsoft.Dynamics.CRM.opportunity?text=opportunity EntityType" /> was created as sample data earlier in the program.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ef8ae-192">[Unbound actions](use-web-api-actions.md#bkmk_unboundActions)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-192">[Unbound actions](use-web-api-actions.md#bkmk_unboundActions)</span></span>  
  
 <span data-ttu-id="ef8ae-193">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-193">**Request**</span></span>  
  
```http  
POST http://[Organization URI]/api/data/v9.0/WinOpportunity HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
  
{  
   "Status":3,  
   "OpportunityClose":{  
      "subject":"Won Opportunity",  
      "opportunityid@odata.bind":"http://[Organization URI]/api/data/v9.0/opportunities(47920da5-fb4a-e611-80d5-00155da84802)"  
   }  
}  
```  
  
 <span data-ttu-id="ef8ae-194">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-194">**Response**</span></span>  
  
```http  
HTTP/1.1 204 No Content  
OData-Version: 4.0   
```  
  
 <span data-ttu-id="ef8ae-195">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-195">**Console output**</span></span>  
  
```  
Unbound Action: WinOpportunity  
    Opportunity won.  
```  
  
<a name="bkmk_boundActionWithParams"></a>
   
### <a name="using-bound-action-with-parameters"></a><span data-ttu-id="ef8ae-196">Using bound action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-196">Using bound action with parameters</span></span>
  
 <span data-ttu-id="ef8ae-197">Use a bound action that takes parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-197">Use a bound action that takes parameters.</span></span> <span data-ttu-id="ef8ae-198">This operation adds a letter to the current user's queue.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-198">This operation adds a letter to the current user's queue.</span></span> <span data-ttu-id="ef8ae-199">To accomplish this, we use the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> and the <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" /> to get a reference to the current user's queue.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-199">To accomplish this, we use the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> and the <xref href="Microsoft.Dynamics.CRM.systemuser?text=systemuser EntityType" /> to get a reference to the current user's queue.</span></span>  <span data-ttu-id="ef8ae-200">We also need reference to the <xref href="Microsoft.Dynamics.CRM.letter?text=letter EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-200">We also need reference to the <xref href="Microsoft.Dynamics.CRM.letter?text=letter EntityType" />.</span></span> <span data-ttu-id="ef8ae-201">This letter was created as sample data earlier in the program.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-201">This letter was created as sample data earlier in the program.</span></span> <span data-ttu-id="ef8ae-202">Then the bound <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> is called to add the letter to the current user's queue.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-202">Then the bound <xref href="Microsoft.Dynamics.CRM.AddToQueue?text=AddToQueue Action" /> is called to add the letter to the current user's queue.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ef8ae-203">[Bound actions](use-web-api-actions.md#bkmk_boundActions)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-203">[Bound actions](use-web-api-actions.md#bkmk_boundActions)</span></span>  
  
 <span data-ttu-id="ef8ae-204">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-204">**Request**</span></span>  
  
```http  
POST http://[Organization URI]/api/data/v9.0/queues(1f7bcc50-d3f6-e511-80d0-00155da84802)/Microsoft.Dynamics.CRM.AddToQueue HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Content-Length: 110  
  
{  
   "Target":{  
      "activityid":"4c920da5-fb4a-e611-80d5-00155da84802",  
      "@odata.type":"Microsoft.Dynamics.CRM.letter"  
   }  
}  
```  
  
 <span data-ttu-id="ef8ae-205">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-205">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 170  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.AddToQueueResponse",  
   "QueueItemId":"67bdfabd-fc4a-e611-80d5-00155da84802"  
}  
```  
  
 <span data-ttu-id="ef8ae-206">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-206">**Console output**</span></span>  
  
```  
Bound Action: AddToQueue  
    QueueItemId returned from AddToQueue Action: 67bdfabd-fc4a-e611-80d5-00155da84802  
```  
  
<a name="bkmk_customActions"></a> 
  
## <a name="working-with-custom-actions"></a><span data-ttu-id="ef8ae-207">Working with custom actions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-207">Working with custom actions</span></span>  

 <span data-ttu-id="ef8ae-208">If you define custom actions for your solution, you can call them using the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-208">If you define custom actions for your solution, you can call them using the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] Web API.</span></span> <span data-ttu-id="ef8ae-209">Regardless of whether the operations included in your custom action have side effects, they can potentially modify data and therefore are considered actions rather than functions.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-209">Regardless of whether the operations included in your custom action have side effects, they can potentially modify data and therefore are considered actions rather than functions.</span></span> <span data-ttu-id="ef8ae-210">There is no way to create a custom function.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-210">There is no way to create a custom function.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ef8ae-211">[Use a custom action](use-web-api-actions.md#bkmk_customActions).</span><span class="sxs-lookup"><span data-stu-id="ef8ae-211">[Use a custom action](use-web-api-actions.md#bkmk_customActions).</span></span>  
  
 <span data-ttu-id="ef8ae-212">This sample comes with two custom actions.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-212">This sample comes with two custom actions.</span></span> <span data-ttu-id="ef8ae-213">They both require parameters but one is bound and the other is unbound.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-213">They both require parameters but one is bound and the other is unbound.</span></span>  
  
- <span data-ttu-id="ef8ae-214">`sample_AddNoteToContact`: A bound custom action that takes two parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-214">`sample_AddNoteToContact`: A bound custom action that takes two parameters.</span></span> <span data-ttu-id="ef8ae-215">One is a `NoteTitle` and the other is a `NoteText`.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-215">One is a `NoteTitle` and the other is a `NoteText`.</span></span> <span data-ttu-id="ef8ae-216">This custom action adds a note to a <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-216">This custom action adds a note to a <xref href="Microsoft.Dynamics.CRM.contact?text=contact EntityType" />.</span></span> <span data-ttu-id="ef8ae-217">Below is a screen shot of the **Information** page for this custom action.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-217">Below is a screen shot of the **Information** page for this custom action.</span></span>  
  
  <span data-ttu-id="ef8ae-218">![Custom Action - AddNoteToContact information](../media/custom-action-add-note-contact.PNG "Custom Action - AddNoteToContact information")</span><span class="sxs-lookup"><span data-stu-id="ef8ae-218">![Custom Action - AddNoteToContact information](../media/custom-action-add-note-contact.PNG "Custom Action - AddNoteToContact information")</span></span>  
  
- <span data-ttu-id="ef8ae-219">`sample_CreateCustomer`: An unbound custom action that require different parameters depending on what type of customer is being created.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-219">`sample_CreateCustomer`: An unbound custom action that require different parameters depending on what type of customer is being created.</span></span> <span data-ttu-id="ef8ae-220">For example, when the `AccountType` is "account" then it only requires `AccountName` parameter.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-220">For example, when the `AccountType` is "account" then it only requires `AccountName` parameter.</span></span> <span data-ttu-id="ef8ae-221">When the `AccountType` is "contact", a `ContactFirstName` and `ContactLastName` parameters are required.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-221">When the `AccountType` is "contact", a `ContactFirstName` and `ContactLastName` parameters are required.</span></span> <span data-ttu-id="ef8ae-222">Below is a screen shot of the **Information** page for this custom action.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-222">Below is a screen shot of the **Information** page for this custom action.</span></span>  
  
  <span data-ttu-id="ef8ae-223">![Custom Action - CreateCustomer information](../media/custom-action-create-customer.PNG "Custom Action - CreateCustomer information")</span><span class="sxs-lookup"><span data-stu-id="ef8ae-223">![Custom Action - CreateCustomer information](../media/custom-action-create-customer.PNG "Custom Action - CreateCustomer information")</span></span>  
  
<a name="bkmk_boundCustomActionWithParams"></a>
   
### <a name="using-bound-custom-action-with-parameters"></a><span data-ttu-id="ef8ae-224">Using bound custom action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-224">Using bound custom action with parameters</span></span> 
 
 <span data-ttu-id="ef8ae-225">This example calls the `sample_AddNoteToContact` custom action which is bound to the contact entity  with the required parameters.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-225">This example calls the `sample_AddNoteToContact` custom action which is bound to the contact entity  with the required parameters.</span></span> <span data-ttu-id="ef8ae-226">This custom action adds a note to an existing contact.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-226">This custom action adds a note to an existing contact.</span></span> <span data-ttu-id="ef8ae-227">This action returns an entity with an `annotationid` property.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-227">This action returns an entity with an `annotationid` property.</span></span> <span data-ttu-id="ef8ae-228">To show that the note was added, the `annotationid` is used to request information about the note.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-228">To show that the note was added, the `annotationid` is used to request information about the note.</span></span>  
  
 <span data-ttu-id="ef8ae-229">The request and response of the action.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-229">The request and response of the action.</span></span>  
  
 <span data-ttu-id="ef8ae-230">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-230">**Request**</span></span>  
  
```http  
POST http://[Organization URI]/api/data/v9.0/contacts(4d920da5-fb4a-e611-80d5-00155da84802)/Microsoft.Dynamics.CRM.sample_AddNoteToContact HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Content-Length: 80  
  
{  
   "NoteTitle":"The Title of the Note",  
   "NoteText":"The text content of the note."  
}  
```  
  
 <span data-ttu-id="ef8ae-231">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-231">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 149  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#annotations/$entity",  
   "annotationid":"ba146d0b-fd4a-e611-80d5-00155da84802"  
}  
```  
  
 <span data-ttu-id="ef8ae-232">The request and response of the annotation.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-232">The request and response of the annotation.</span></span>  
  
 <span data-ttu-id="ef8ae-233">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-233">**Request**</span></span>  
  
```http  
GET http://[Organization URI]/api/data/v9.0/annotations(ba146d0b-fd4a-e611-80d5-00155da84802)?$select=subject,notetext&$expand=objectid_contact($select=fullname) HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
  
```  
  
 <span data-ttu-id="ef8ae-234">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-234">**Response**</span></span>  
  
```http  
HTTP/1.1 200 OK  
OData-Version: 4.0  
Content-Length: 450  
  
{  
   "@odata.context":"http://[Organization URI]/api/data/v9.0/$metadata#annotations(subject,notetext,objectid_contact,objectid_contact(fullname))/$entity",  
   "@odata.etag":"W/\"622978\"",  
   "subject":"The Title of the Note",  
   "notetext":"The text content of the note.",  
   "annotationid":"ba146d0b-fd4a-e611-80d5-00155da84802",  
   "objectid_contact":{  
      "@odata.etag":"W/\"622968\"",  
      "fullname":"Jon Fogg",  
      "contactid":"4d920da5-fb4a-e611-80d5-00155da84802"  
   }  
}  
```  
  
 <span data-ttu-id="ef8ae-235">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-235">**Console output**</span></span>  
  
```http  
Custom action: sample_AddNoteToContact  
    A note with the title 'The Title of the Note' and the content 'The text content of the note.' was created and associated with the contact Jon Fogg.  
```  
  
<a name="bkmk_unboundCustomActionWithParams"></a> 
  
### <a name="using-unbound-custom-action-with-parameters"></a><span data-ttu-id="ef8ae-236">Using unbound custom action with parameters</span><span class="sxs-lookup"><span data-stu-id="ef8ae-236">Using unbound custom action with parameters</span></span>  

 <span data-ttu-id="ef8ae-237">This operation calls the `sample_CreateCustomer`  custom action to create an "account" customer.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-237">This operation calls the `sample_CreateCustomer`  custom action to create an "account" customer.</span></span> <span data-ttu-id="ef8ae-238">Required parameters  are passed in for a `CustomerType` of `account`.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-238">Required parameters  are passed in for a `CustomerType` of `account`.</span></span>  
  
 <span data-ttu-id="ef8ae-239">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-239">**Request**</span></span>  
  
```http  
POST http://[Organization URI]/api/data/v9.0/sample_CreateCustomer HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Content-Length: 103  
  
{  
   "CustomerType":"account",  
   "AccountName":"Account Customer Created in WebAPIFunctionsAndActions sample"  
}  
```  
  
 <span data-ttu-id="ef8ae-240">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-240">**Response**</span></span>  
  
```http  
HTTP/1.1 204 No Content  
OData-Version: 4.0  
  
```  
  
<a name="bkmk_boundCustomActionErrorHandling"></a> 
  
### <a name="handling-custom-action-exceptions"></a><span data-ttu-id="ef8ae-241">Handling custom action exceptions</span><span class="sxs-lookup"><span data-stu-id="ef8ae-241">Handling custom action exceptions</span></span>  

 <span data-ttu-id="ef8ae-242">This example shows that custom actions can return custom error messages.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-242">This example shows that custom actions can return custom error messages.</span></span> <span data-ttu-id="ef8ae-243">You handle custom exceptions the same way you handle standard exceptions.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-243">You handle custom exceptions the same way you handle standard exceptions.</span></span> <span data-ttu-id="ef8ae-244">To get the custom error message from the  `sample_CreateCustomer`  custom action , this example creates a "contact" customer.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-244">To get the custom error message from the  `sample_CreateCustomer`  custom action , this example creates a "contact" customer.</span></span> <span data-ttu-id="ef8ae-245">However, we intentionally pass in the wrong parameters for this `CustomerType` parameter.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-245">However, we intentionally pass in the wrong parameters for this `CustomerType` parameter.</span></span> <span data-ttu-id="ef8ae-246">This operation then catches the exception and displays the error message, then continues with the sample program.</span><span class="sxs-lookup"><span data-stu-id="ef8ae-246">This operation then catches the exception and displays the error message, then continues with the sample program.</span></span>  
  
 <span data-ttu-id="ef8ae-247">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-247">**Request**</span></span>  
  
```http  
POST http://[Organization URI]/api/data/v9.0/sample_CreateCustomer HTTP/1.1  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
Content-Type: application/json; charset=utf-8  
Content-Length: 103  
  
{  
   "CustomerType":"contact",  
   "AccountName":"Account Customer Created in WebAPIFunctionsAndActions sample"  
}  
```  
  
 <span data-ttu-id="ef8ae-248">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-248">**Response**</span></span>  
  
```http  
HTTP/1.1 500 Internal Server Error  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
Content-Length: 2760  
  
{  
   "error":{  
      "code":"",  
      "message":"ContactFirstName and ContactLastName are required when CustomerType is contact.",  
      "innererror":{  
         "message":"ContactFirstName and ContactLastName are required when CustomerType is contact.",  
         ...[truncated]  
      }  
   }  
}  
```  
  
 <span data-ttu-id="ef8ae-249">**Console output**</span><span class="sxs-lookup"><span data-stu-id="ef8ae-249">**Console output**</span></span>  
  
```  
Expected custom error: ContactFirstName and ContactLastName are required when CustomerType is contact.  
```  
  
### <a name="see-also"></a><span data-ttu-id="ef8ae-250">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ef8ae-250">See also</span></span>  

 <span data-ttu-id="ef8ae-251">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="ef8ae-251">[Use the Dynamics 365 for Customer Engagement Web API](../use-microsoft-dynamics-365-web-api.md) </span></span>  
 <span data-ttu-id="ef8ae-252">[Use Web API functions](use-web-api-functions.md) </span><span class="sxs-lookup"><span data-stu-id="ef8ae-252">[Use Web API functions](use-web-api-functions.md) </span></span>  
 <span data-ttu-id="ef8ae-253">[Use Web API actions](use-web-api-actions.md) </span><span class="sxs-lookup"><span data-stu-id="ef8ae-253">[Use Web API actions](use-web-api-actions.md) </span></span>  
 [<span data-ttu-id="ef8ae-254">Web API Functions and Actions Sample (C#)</span><span class="sxs-lookup"><span data-stu-id="ef8ae-254">Web API Functions and Actions Sample (C#)</span></span>](web-api-functions-actions-sample-csharp.md)   

