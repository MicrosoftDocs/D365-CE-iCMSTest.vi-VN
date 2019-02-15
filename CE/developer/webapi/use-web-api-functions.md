---
title: Use Web API functions (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Functions are reusable operations that are used with a GET request to retrieve data from Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c6de9c12-e8e3-4ed5-a6ed-18ade572065f
caps.latest.revision: 45
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: dd678b1b20c57b464b1a47c8ec0d16060a824283
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385728"
---
# <a name="use-web-api-functions"></a><span data-ttu-id="76b9c-103">Use Web API functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-103">Use Web API functions</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="76b9c-104">Functions and actions represent re-usable operations you can perform using the Web API.</span><span class="sxs-lookup"><span data-stu-id="76b9c-104">Functions and actions represent re-usable operations you can perform using the Web API.</span></span> <span data-ttu-id="76b9c-105">There are two types of functions in the Web API:</span><span class="sxs-lookup"><span data-stu-id="76b9c-105">There are two types of functions in the Web API:</span></span>  
  
 <span data-ttu-id="76b9c-106">**Functions**</span><span class="sxs-lookup"><span data-stu-id="76b9c-106">**Functions**</span></span>  
 <span data-ttu-id="76b9c-107">Use a `GET` request with functions listed in <xref:Microsoft.Dynamics.CRM.FunctionIndex> to perform operations that have no side-effects.</span><span class="sxs-lookup"><span data-stu-id="76b9c-107">Use a `GET` request with functions listed in <xref:Microsoft.Dynamics.CRM.FunctionIndex> to perform operations that have no side-effects.</span></span> <span data-ttu-id="76b9c-108">These functions generally retrieve data.</span><span class="sxs-lookup"><span data-stu-id="76b9c-108">These functions generally retrieve data.</span></span> <span data-ttu-id="76b9c-109">They return either a collection or a complex type.</span><span class="sxs-lookup"><span data-stu-id="76b9c-109">They return either a collection or a complex type.</span></span> <span data-ttu-id="76b9c-110">Each of these functions has a corresponding message in the organization service.</span><span class="sxs-lookup"><span data-stu-id="76b9c-110">Each of these functions has a corresponding message in the organization service.</span></span>  
  
 <span data-ttu-id="76b9c-111">**Query Functions**</span><span class="sxs-lookup"><span data-stu-id="76b9c-111">**Query Functions**</span></span>  
 <span data-ttu-id="76b9c-112">Use the functions listed in <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex> to evaluate properties and values in the composition of a query.</span><span class="sxs-lookup"><span data-stu-id="76b9c-112">Use the functions listed in <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex> to evaluate properties and values in the composition of a query.</span></span> <span data-ttu-id="76b9c-113">Each of these functions has a corresponding <xref:Microsoft.Xrm.Sdk.Query.ConditionOperator> value.</span><span class="sxs-lookup"><span data-stu-id="76b9c-113">Each of these functions has a corresponding <xref:Microsoft.Xrm.Sdk.Query.ConditionOperator> value.</span></span>  
  
<a name="bkmk_passParametersToFunctions"></a>   
## <a name="passing-parameters-to-a-function"></a><span data-ttu-id="76b9c-114">Passing parameters to a function</span><span class="sxs-lookup"><span data-stu-id="76b9c-114">Passing parameters to a function</span></span>  
 <span data-ttu-id="76b9c-115">For those functions that require parameters, the best practice is to pass the values using parameters.</span><span class="sxs-lookup"><span data-stu-id="76b9c-115">For those functions that require parameters, the best practice is to pass the values using parameters.</span></span> <span data-ttu-id="76b9c-116">For example, when you use the <xref href="Microsoft.Dynamics.CRM.GetTimeZoneCodeByLocalizedName?text=GetTimeZoneCodeByLocalizedName Function" />, you must include the `LocalizedStandardName` and `LocaleId` parameter values.</span><span class="sxs-lookup"><span data-stu-id="76b9c-116">For example, when you use the <xref href="Microsoft.Dynamics.CRM.GetTimeZoneCodeByLocalizedName?text=GetTimeZoneCodeByLocalizedName Function" />, you must include the `LocalizedStandardName` and `LocaleId` parameter values.</span></span> <span data-ttu-id="76b9c-117">So, you could use the following inline syntax as shown here.</span><span class="sxs-lookup"><span data-stu-id="76b9c-117">So, you could use the following inline syntax as shown here.</span></span>  
  
```http
GET [Organization URI]/api/data/v9.0/GetTimeZoneCodeByLocalizedName(LocalizedStandardName='Pacific Standard Time',LocaleId=1033)  
```  
  
 <span data-ttu-id="76b9c-118">However, there’s an open issue using DateTimeOffset values with the inline syntax, as explained in the following article: [DateTimeOffset as query parameter #204](https://github.com/OData/WebApi/issues/204).</span><span class="sxs-lookup"><span data-stu-id="76b9c-118">However, there’s an open issue using DateTimeOffset values with the inline syntax, as explained in the following article: [DateTimeOffset as query parameter #204](https://github.com/OData/WebApi/issues/204).</span></span>  
  
 <span data-ttu-id="76b9c-119">Therefore, the best practice is to pass the values in as parameters as shown in the following code sample.</span><span class="sxs-lookup"><span data-stu-id="76b9c-119">Therefore, the best practice is to pass the values in as parameters as shown in the following code sample.</span></span> <span data-ttu-id="76b9c-120">If you use this best practice, you can avoid the open issue that applies to `DateTimeOffset`.</span><span class="sxs-lookup"><span data-stu-id="76b9c-120">If you use this best practice, you can avoid the open issue that applies to `DateTimeOffset`.</span></span>  
  
```http
GET [Organization URI]/api/data/v9.0/GetTimeZoneCodeByLocalizedName(LocalizedStandardName=@p1,LocaleId=@p2)?@p1='Pacific Standard Time'&@p2=1033  
```  
  
 <span data-ttu-id="76b9c-121">Parameter aliases also allow you to re-use parameter values to reduce the total length of the URL when the parameter value is used multiple times.</span><span class="sxs-lookup"><span data-stu-id="76b9c-121">Parameter aliases also allow you to re-use parameter values to reduce the total length of the URL when the parameter value is used multiple times.</span></span>  
  
<a name="bkmk_passCrmEntityReference"></a>

## <a name="pass-reference-to-an-entity-to-a-function"></a><span data-ttu-id="76b9c-122">Pass reference to an entity to a function</span><span class="sxs-lookup"><span data-stu-id="76b9c-122">Pass reference to an entity to a function</span></span>

 <span data-ttu-id="76b9c-123">Certain functions will require passing a reference to an existing entity.</span><span class="sxs-lookup"><span data-stu-id="76b9c-123">Certain functions will require passing a reference to an existing entity.</span></span> <span data-ttu-id="76b9c-124">For example, the following functions have a parameter that requires a <xref href="Microsoft.Dynamics.CRM.crmbaseentity?text=crmbaseentity EntityType" />:</span><span class="sxs-lookup"><span data-stu-id="76b9c-124">For example, the following functions have a parameter that requires a <xref href="Microsoft.Dynamics.CRM.crmbaseentity?text=crmbaseentity EntityType" />:</span></span>  
  
||||  
|-|-|-|  
|<xref href="Microsoft.Dynamics.CRM.CalculateRollupField?text=CalculateRollupField Function" />|<xref href="Microsoft.Dynamics.CRM.IncrementKnowledgeArticleViewCount?text=IncrementKnowledgeArticleViewCount Function" />|<xref href="Microsoft.Dynamics.CRM.InitializeFrom?text=InitializeFrom Function" />|  
|<xref href="Microsoft.Dynamics.CRM.IsValidStateTransition?text=IsValidStateTransition Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveDuplicates?text=RetrieveDuplicates Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveLocLabels?text=RetrieveLocLabels Function" />|  
|<xref href="Microsoft.Dynamics.CRM.RetrievePrincipalAccess?text=RetrievePrincipalAccess Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveRecordWall?text=RetrieveRecordWall Function" />|<xref href="Microsoft.Dynamics.CRM.ValidateRecurrenceRule?text=ValidateRecurrenceRule Function" />|  
  
 <span data-ttu-id="76b9c-125">When you pass a reference to an existing entity, use the `@odata.id` annotation to the Uri for the entity.</span><span class="sxs-lookup"><span data-stu-id="76b9c-125">When you pass a reference to an existing entity, use the `@odata.id` annotation to the Uri for the entity.</span></span> <span data-ttu-id="76b9c-126">For example if you are using the <xref href="Microsoft.Dynamics.CRM.RetrievePrincipalAccess?text=RetrievePrincipalAccess Function" /> you can use the following Uri to specify retrieving access to a specific contact:</span><span class="sxs-lookup"><span data-stu-id="76b9c-126">For example if you are using the <xref href="Microsoft.Dynamics.CRM.RetrievePrincipalAccess?text=RetrievePrincipalAccess Function" /> you can use the following Uri to specify retrieving access to a specific contact:</span></span>  
  
```http
GET [Organization URI]/api/data/v9.0/systemusers(af9b3cf6-f654-4cd9-97a6-cf9526662797)/Microsoft.Dynamics.CRM.RetrievePrincipalAccess(Target=@tid)?@tid={'@odata.id':'contacts(9f3162f6-804a-e611-80d1-00155d4333fa)'}
```  
  
 <span data-ttu-id="76b9c-127">The `@odata.id` annotation can be the full Uri, but a relative Uri works too.</span><span class="sxs-lookup"><span data-stu-id="76b9c-127">The `@odata.id` annotation can be the full Uri, but a relative Uri works too.</span></span>  
  
<a name="bkmk_boundAndUnboundFunctions"></a>
 
## <a name="bound-and-unbound-functions"></a><span data-ttu-id="76b9c-128">Bound and unbound functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-128">Bound and unbound functions</span></span>

 <span data-ttu-id="76b9c-129">Only those functions found in <xref:Microsoft.Dynamics.CRM.FunctionIndex> may be bound.</span><span class="sxs-lookup"><span data-stu-id="76b9c-129">Only those functions found in <xref:Microsoft.Dynamics.CRM.FunctionIndex> may be bound.</span></span> <span data-ttu-id="76b9c-130">Query functions are never bound.</span><span class="sxs-lookup"><span data-stu-id="76b9c-130">Query functions are never bound.</span></span>  
  
<a name="bkmk_boundFunctions"></a>

### <a name="bound-functions"></a><span data-ttu-id="76b9c-131">Bound functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-131">Bound functions</span></span>

 <span data-ttu-id="76b9c-132">In the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl), when a `Function` element represents a bound function, it has an `IsBound` attribute with the value `true`.</span><span class="sxs-lookup"><span data-stu-id="76b9c-132">In the [CSDL metadata document](web-api-types-operations.md#bkmk_csdl), when a `Function` element represents a bound function, it has an `IsBound` attribute with the value `true`.</span></span> <span data-ttu-id="76b9c-133">The first `Parameter` element defined in the function represents the entity that the function is bound to.</span><span class="sxs-lookup"><span data-stu-id="76b9c-133">The first `Parameter` element defined in the function represents the entity that the function is bound to.</span></span> <span data-ttu-id="76b9c-134">When the `Type` attribute of the parameter is a collection, the function is bound to an entity collection.</span><span class="sxs-lookup"><span data-stu-id="76b9c-134">When the `Type` attribute of the parameter is a collection, the function is bound to an entity collection.</span></span> <span data-ttu-id="76b9c-135">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncident?text=CalculateTotalTimeIncident Function" /> and <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse?text=CalculateTotalTimeIncidentResponse ComplexType" /> in the CSDL.</span><span class="sxs-lookup"><span data-stu-id="76b9c-135">As an example, the following is the definition of the <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncident?text=CalculateTotalTimeIncident Function" /> and <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse?text=CalculateTotalTimeIncidentResponse ComplexType" /> in the CSDL.</span></span>  
  
```xml
<ComplexType Name="CalculateTotalTimeIncidentResponse">  
  <Property Name="TotalTime" Type="Edm.Int64" Nullable="false" />  
</ComplexType>  
<Function Name="CalculateTotalTimeIncident" IsBound="true">  
  <Parameter Name="entity" Type="mscrm.incident" Nullable="false" />  
  <ReturnType Type="mscrm.CalculateTotalTimeIncidentResponse" Nullable="false" />  
</Function>  
```  
  
 <span data-ttu-id="76b9c-136">This bound function is equivalent to the <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest> used by the organization service.</span><span class="sxs-lookup"><span data-stu-id="76b9c-136">This bound function is equivalent to the <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest> used by the organization service.</span></span> <span data-ttu-id="76b9c-137">In the Web API this function is bound to the <xref href="Microsoft.Dynamics.CRM.incident?text=incident EntityType" /> that represents the <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest>.<xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest.IncidentId></span><span class="sxs-lookup"><span data-stu-id="76b9c-137">In the Web API this function is bound to the <xref href="Microsoft.Dynamics.CRM.incident?text=incident EntityType" /> that represents the <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest>.<xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentRequest.IncidentId></span></span> <span data-ttu-id="76b9c-138">property.</span><span class="sxs-lookup"><span data-stu-id="76b9c-138">property.</span></span> <span data-ttu-id="76b9c-139">Instead of returning a <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentResponse>, this function returns a <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse?text=CalculateTotalTimeIncidentResponse ComplexType" />.</span><span class="sxs-lookup"><span data-stu-id="76b9c-139">Instead of returning a <xref:Microsoft.Crm.Sdk.Messages.CalculateTotalTimeIncidentResponse>, this function returns a <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse?text=CalculateTotalTimeIncidentResponse ComplexType" />.</span></span> <span data-ttu-id="76b9c-140">When a function returns a complex type, its definition appears directly above the definition of the function in the CSDL.</span><span class="sxs-lookup"><span data-stu-id="76b9c-140">When a function returns a complex type, its definition appears directly above the definition of the function in the CSDL.</span></span>  
  
 <span data-ttu-id="76b9c-141">To invoke a bound function, append the full name of the function to the URL and include any named parameters within the parentheses following the function name.</span><span class="sxs-lookup"><span data-stu-id="76b9c-141">To invoke a bound function, append the full name of the function to the URL and include any named parameters within the parentheses following the function name.</span></span> <span data-ttu-id="76b9c-142">The full function name includes the namespace `Microsoft.Dynamics.CRM`.</span><span class="sxs-lookup"><span data-stu-id="76b9c-142">The full function name includes the namespace `Microsoft.Dynamics.CRM`.</span></span> <span data-ttu-id="76b9c-143">Functions that aren’t bound must not use the full name.</span><span class="sxs-lookup"><span data-stu-id="76b9c-143">Functions that aren’t bound must not use the full name.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="76b9c-144">A bound function must be invoked using a URI to set the first parameter value.</span><span class="sxs-lookup"><span data-stu-id="76b9c-144">A bound function must be invoked using a URI to set the first parameter value.</span></span> <span data-ttu-id="76b9c-145">You can’t set it as a named parameter value.</span><span class="sxs-lookup"><span data-stu-id="76b9c-145">You can’t set it as a named parameter value.</span></span>  
  
 <span data-ttu-id="76b9c-146">The following example shows an example using the <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncident?text=CalculateTotalTimeIncident Function" />, which is bound to the `incident` entity.</span><span class="sxs-lookup"><span data-stu-id="76b9c-146">The following example shows an example using the <xref href="Microsoft.Dynamics.CRM.CalculateTotalTimeIncident?text=CalculateTotalTimeIncident Function" />, which is bound to the `incident` entity.</span></span>  
  
 <span data-ttu-id="76b9c-147">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="76b9c-147">**Request**</span></span>

```http
GET [Organization URI]/api/data/v9.0/incidents(90427858-7a77-e511-80d4-00155d2a68d1)/Microsoft.Dynamics.CRM.CalculateTotalTimeIncident() HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 <span data-ttu-id="76b9c-148">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="76b9c-148">**Response**</span></span>
 
```http 
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
  
{  
  "@odata.context":"[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.CalculateTotalTimeIncidentResponse","TotalTime":30  
}  
```  
  
<a name="bkmk_unboundFunctions"></a>
 
### <a name="unbound-functions"></a><span data-ttu-id="76b9c-149">Unbound functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-149">Unbound functions</span></span>

 <span data-ttu-id="76b9c-150">The <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> isn’t bound to an entity.</span><span class="sxs-lookup"><span data-stu-id="76b9c-150">The <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" /> isn’t bound to an entity.</span></span> <span data-ttu-id="76b9c-151">It is defined in the CSDL without an `IsBound` attribute.</span><span class="sxs-lookup"><span data-stu-id="76b9c-151">It is defined in the CSDL without an `IsBound` attribute.</span></span>  
  
```xml
<ComplexType Name="WhoAmIResponse">  
  <Property Name="BusinessUnitId" Type="Edm.Guid" Nullable="false" />  
  <Property Name="UserId" Type="Edm.Guid" Nullable="false" />  
  <Property Name="OrganizationId" Type="Edm.Guid" Nullable="false" />  
</ComplexType>  
<Function Name="WhoAmI">  
  <ReturnType Type="mscrm.WhoAmIResponse" Nullable="false" />  
</Function>  
```  
  
 <span data-ttu-id="76b9c-152">This function corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> and returns a <xref href="Microsoft.Dynamics.CRM.WhoAmIResponse?text=WhoAmIResponse ComplexType" /> that corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIResponse> used by the organization service.</span><span class="sxs-lookup"><span data-stu-id="76b9c-152">This function corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIRequest> and returns a <xref href="Microsoft.Dynamics.CRM.WhoAmIResponse?text=WhoAmIResponse ComplexType" /> that corresponds to the <xref:Microsoft.Crm.Sdk.Messages.WhoAmIResponse> used by the organization service.</span></span> <span data-ttu-id="76b9c-153">This function doesn’t have any parameters.</span><span class="sxs-lookup"><span data-stu-id="76b9c-153">This function doesn’t have any parameters.</span></span>  
  
 <span data-ttu-id="76b9c-154">When invoking an unbound function, use just the function name as shown in the following example.</span><span class="sxs-lookup"><span data-stu-id="76b9c-154">When invoking an unbound function, use just the function name as shown in the following example.</span></span>  
  
 <span data-ttu-id="76b9c-155">**Yêu cầu**</span><span class="sxs-lookup"><span data-stu-id="76b9c-155">**Request**</span></span>

```http
GET [Organization URI]/api/data/v9.0/WhoAmI() HTTP/1.1  
Accept: application/json  
OData-MaxVersion: 4.0  
OData-Version: 4.0  
```  
  
 <span data-ttu-id="76b9c-156">**Phản hồi**</span><span class="sxs-lookup"><span data-stu-id="76b9c-156">**Response**</span></span>

```http
HTTP/1.1 200 OK  
Content-Type: application/json; odata.metadata=minimal  
OData-Version: 4.0  
{  
 "@odata.context": "[Organization URI]/api/data/v9.0/$metadata#Microsoft.Dynamics.CRM.WhoAmIResponse",  
 "BusinessUnitId": "ded5a64f-f06d-e511-80d0-00155db07cb1",  
 "UserId": "d96e9f55-f06d-e511-80d0-00155db07cb1",  
 "OrganizationId": "4faf1f34-f06d-e511-80d0-00155db07cb1"  
}  
```  
  
<a name="bkmk_composeQueryWithFunctions"></a>

## <a name="compose-a-query-with-functions"></a><span data-ttu-id="76b9c-157">Compose a query with functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-157">Compose a query with functions</span></span>

 <span data-ttu-id="76b9c-158">There are two ways that functions can be used to control data returned with queries.</span><span class="sxs-lookup"><span data-stu-id="76b9c-158">There are two ways that functions can be used to control data returned with queries.</span></span> <span data-ttu-id="76b9c-159">Certain functions allow for control over the columns or conditions that they return and you use query functions to evaluate conditions in a query.</span><span class="sxs-lookup"><span data-stu-id="76b9c-159">Certain functions allow for control over the columns or conditions that they return and you use query functions to evaluate conditions in a query.</span></span>  
  
<a name="bkmk_composableFunctions"></a>
  
### <a name="composable-functions"></a><span data-ttu-id="76b9c-160">Composable functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-160">Composable functions</span></span>

 <span data-ttu-id="76b9c-161">Some functions listed in <xref:Microsoft.Dynamics.CRM.FunctionIndex> will return a collection of entities.</span><span class="sxs-lookup"><span data-stu-id="76b9c-161">Some functions listed in <xref:Microsoft.Dynamics.CRM.FunctionIndex> will return a collection of entities.</span></span> <span data-ttu-id="76b9c-162">A subset of these functions are *composable*, which means that you can include an additional `$select` or `$filter` system query option to control which columns are returned in the results.</span><span class="sxs-lookup"><span data-stu-id="76b9c-162">A subset of these functions are *composable*, which means that you can include an additional `$select` or `$filter` system query option to control which columns are returned in the results.</span></span> <span data-ttu-id="76b9c-163">These functions have an `IsComposable` attribute in the CSDL.</span><span class="sxs-lookup"><span data-stu-id="76b9c-163">These functions have an `IsComposable` attribute in the CSDL.</span></span> <span data-ttu-id="76b9c-164">Each of these functions has a companion message in the organization service that accept either a <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> or <xref:Microsoft.Xrm.Sdk.Query.QueryBase> type parameter.</span><span class="sxs-lookup"><span data-stu-id="76b9c-164">Each of these functions has a companion message in the organization service that accept either a <xref:Microsoft.Xrm.Sdk.Query.ColumnSet> or <xref:Microsoft.Xrm.Sdk.Query.QueryBase> type parameter.</span></span> <span data-ttu-id="76b9c-165">The OData system query options provide the same functionality so these functions do not have the same parameters as their companion messages in the organization service.</span><span class="sxs-lookup"><span data-stu-id="76b9c-165">The OData system query options provide the same functionality so these functions do not have the same parameters as their companion messages in the organization service.</span></span> <span data-ttu-id="76b9c-166">The following table shows a list of those composable functions in this release.</span><span class="sxs-lookup"><span data-stu-id="76b9c-166">The following table shows a list of those composable functions in this release.</span></span>  
  
||||  
|-|-|-|  
|<xref href="Microsoft.Dynamics.CRM.GetDefaultPriceLevel?text=GetDefaultPriceLevel Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveAllChildUsersSystemUser?text=RetrieveAllChildUsersSystemUser Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveBusinessHierarchyBusinessUnit?text=RetrieveBusinessHierarchyBusinessUnit Function" />|  
|<xref href="Microsoft.Dynamics.CRM.RetrieveByGroupResource?text=RetrieveByGroupResource Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveByResourceResourceGroup?text=RetrieveByResourceResourceGroup Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveMembersBulkOperation?text=RetrieveMembersBulkOperation Function" />|  
|<xref href="Microsoft.Dynamics.CRM.RetrieveParentGroupsResourceGroup?text=RetrieveParentGroupsResourceGroup Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveSubGroupsResourceGroup?text=RetrieveSubGroupsResourceGroup Function" />|<xref href="Microsoft.Dynamics.CRM.RetrieveUnpublishedMultiple?text=RetrieveUnpublishedMultiple Function" />|  
|<xref href="Microsoft.Dynamics.CRM.SearchByBodyKbArticle?text=SearchByBodyKbArticle Function" />|<xref href="Microsoft.Dynamics.CRM.SearchByKeywordsKbArticle?text=SearchByKeywordsKbArticle Function" />|<xref href="Microsoft.Dynamics.CRM.SearchByTitleKbArticle?text=SearchByTitleKbArticle Function" />|  
  
<a name="bkmk_queryevaluationFunctions"></a>
  
### <a name="query-functions"></a><span data-ttu-id="76b9c-167">Query functions</span><span class="sxs-lookup"><span data-stu-id="76b9c-167">Query functions</span></span>

 <span data-ttu-id="76b9c-168">Functions listed in <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex> are intended to be used to compose a query.</span><span class="sxs-lookup"><span data-stu-id="76b9c-168">Functions listed in <xref:Microsoft.Dynamics.CRM.QueryFunctionIndex> are intended to be used to compose a query.</span></span> <span data-ttu-id="76b9c-169">These functions can be used in a manner similar to the [Built-in query functions](query-data-web-api.md#bkmk_buildInQueryFunctions), but there are some important differences.</span><span class="sxs-lookup"><span data-stu-id="76b9c-169">These functions can be used in a manner similar to the [Built-in query functions](query-data-web-api.md#bkmk_buildInQueryFunctions), but there are some important differences.</span></span>  
  
 <span data-ttu-id="76b9c-170">You must use the full name of the function and include the names of the parameters.</span><span class="sxs-lookup"><span data-stu-id="76b9c-170">You must use the full name of the function and include the names of the parameters.</span></span> <span data-ttu-id="76b9c-171">The following example shows how to use the <xref href="Microsoft.Dynamics.CRM.LastXHours?text=LastXHours Function" /> to return all account entities modified in the past 12 hours.</span><span class="sxs-lookup"><span data-stu-id="76b9c-171">The following example shows how to use the <xref href="Microsoft.Dynamics.CRM.LastXHours?text=LastXHours Function" /> to return all account entities modified in the past 12 hours.</span></span>  
  
```http
GET [Organization URI]/api/data/v9.0/accounts?$select=name,accountnumber&$filter=Microsoft.Dynamics.CRM.LastXHours(PropertyName=@p1,PropertyValue=@p2)&@p1='modifiedon'&@p2=12  
```  
  
### <a name="see-also"></a><span data-ttu-id="76b9c-172">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="76b9c-172">See also</span></span>

 <span data-ttu-id="76b9c-173">[Web API Functions and Actions Sample (C#)](web-api-functions-actions-sample-csharp.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-173">[Web API Functions and Actions Sample (C#)](web-api-functions-actions-sample-csharp.md) </span></span>  
 <span data-ttu-id="76b9c-174">[Web API Functions and Actions Sample (Client-side JavaScript)](web-api-functions-actions-sample-client-side-javascript.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-174">[Web API Functions and Actions Sample (Client-side JavaScript)](web-api-functions-actions-sample-client-side-javascript.md) </span></span>  
 <span data-ttu-id="76b9c-175">[Perform operations using the Web API](perform-operations-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-175">[Perform operations using the Web API](perform-operations-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-176">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-176">[Compose Http requests and handle errors](compose-http-requests-handle-errors.md) </span></span>  
 <span data-ttu-id="76b9c-177">[Query Data using the Web API](query-data-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-177">[Query Data using the Web API](query-data-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-178">[Create an entity using the Web API](create-entity-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-178">[Create an entity using the Web API](create-entity-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-179">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-179">[Retrieve an entity using the Web API](retrieve-entity-using-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-180">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-180">[Update and delete entities using the Web API](update-delete-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-181">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-181">[Associate and disassociate entities using the Web API](associate-disassociate-entities-using-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-182">[Use Web API actions](use-web-api-actions.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-182">[Use Web API actions](use-web-api-actions.md) </span></span>  
 <span data-ttu-id="76b9c-183">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-183">[Execute batch operations using the Web API](execute-batch-operations-using-web-api.md) </span></span>  
 <span data-ttu-id="76b9c-184">[Impersonate another user using the Web API](impersonate-another-user-web-api.md) </span><span class="sxs-lookup"><span data-stu-id="76b9c-184">[Impersonate another user using the Web API](impersonate-another-user-web-api.md) </span></span>  
 [<span data-ttu-id="76b9c-185">Perform conditional operations using the Web API</span><span class="sxs-lookup"><span data-stu-id="76b9c-185">Perform conditional operations using the Web API</span></span>](perform-conditional-operations-using-web-api.md)
