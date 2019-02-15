---
title: Fiscal date and older than datetime query operators in FetchXML (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how to use FetchXML fiscal data conditional operators and &quot;older than&quot; clauses for date and time values
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ab6e60c-161e-468f-b89c-cc3bd243b3df
caps.latest.revision: 33
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 21687962cad55009749dc01f2bbdc79993244056
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386521"
---
# <a name="fiscal-date-and-older-than-datetime-query-operators-in-fetchxml"></a><span data-ttu-id="fdccb-103">Fiscal date and older than datetime query operators in FetchXML</span><span class="sxs-lookup"><span data-stu-id="fdccb-103">Fiscal date and older than datetime query operators in FetchXML</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="fdccb-104">A FetchXML query in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps can use special fiscal date values and *older than* clauses for date and time values in queries.</span><span class="sxs-lookup"><span data-stu-id="fdccb-104">A FetchXML query in [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps can use special fiscal date values and *older than* clauses for date and time values in queries.</span></span> <span data-ttu-id="fdccb-105">For example, a FetchXML query can find all orders fulfilled in the last fiscal month or urgent cases with high severity that are older than 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="fdccb-105">For example, a FetchXML query can find all orders fulfilled in the last fiscal month or urgent cases with high severity that are older than 15 minutes.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="fdccb-106">For all fiscal date queries, the FetchXML query uses the organization’s fiscal year settings.</span><span class="sxs-lookup"><span data-stu-id="fdccb-106">For all fiscal date queries, the FetchXML query uses the organization’s fiscal year settings.</span></span>  
  
<a name="FiscalDate"></a>   
## <a name="using-fetchxml-fiscal-date-conditional-operators"></a><span data-ttu-id="fdccb-107">Using FetchXML fiscal date conditional operators</span><span class="sxs-lookup"><span data-stu-id="fdccb-107">Using FetchXML fiscal date conditional operators</span></span>  
 <span data-ttu-id="fdccb-108">The following example shows a FetchXML expression that finds all orders fulfilled in the last fiscal period, according to the organization’s fiscal year settings.</span><span class="sxs-lookup"><span data-stu-id="fdccb-108">The following example shows a FetchXML expression that finds all orders fulfilled in the last fiscal period, according to the organization’s fiscal year settings.</span></span> <span data-ttu-id="fdccb-109">For example, if the organization uses fiscal months, the query returns orders fulfilled in the last fiscal month.</span><span class="sxs-lookup"><span data-stu-id="fdccb-109">For example, if the organization uses fiscal months, the query returns orders fulfilled in the last fiscal month.</span></span> <span data-ttu-id="fdccb-110">If the organization uses fiscal quarters, the query returns orders fulfilled in the last fiscal quarter.</span><span class="sxs-lookup"><span data-stu-id="fdccb-110">If the organization uses fiscal quarters, the query returns orders fulfilled in the last fiscal quarter.</span></span> <span data-ttu-id="fdccb-111">If the organization uses fiscal semesters, orders fulfilled in the last fiscal semester are returned.</span><span class="sxs-lookup"><span data-stu-id="fdccb-111">If the organization uses fiscal semesters, orders fulfilled in the last fiscal semester are returned.</span></span>  
  
```xml  
<fetch>  
 <entity name="order">  
  <attribute name="name"/>  
  <filter type="and">  
   <condition attribute="datefulfilled" operator="last-fiscal-period"/>  
  </filter>  
 </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-112">The following example shows a FetchXML expression that finds all accounts created in fiscal year 2013.</span><span class="sxs-lookup"><span data-stu-id="fdccb-112">The following example shows a FetchXML expression that finds all accounts created in fiscal year 2013.</span></span>  
  
```xml  
<fetch>  
 <entity name="account">  
  <attribute name="name"/>  
  <filter type="and">  
   <condition attribute="createdon" operator="in-fiscal-year" value="2013"/>  
  </filter>  
 </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-113">The following example shows a FetchXML expression that finds all opportunities with an estimated close date in the next three fiscal years, based on the organization’s fiscal year settings.</span><span class="sxs-lookup"><span data-stu-id="fdccb-113">The following example shows a FetchXML expression that finds all opportunities with an estimated close date in the next three fiscal years, based on the organization’s fiscal year settings.</span></span> <span data-ttu-id="fdccb-114">The value for `x` is specified in the value attribute of the condition tag.</span><span class="sxs-lookup"><span data-stu-id="fdccb-114">The value for `x` is specified in the value attribute of the condition tag.</span></span>  
  
```xml  
<fetch>  
 <entity name="opportunity">  
  <attribute name="name"/>  
  <filter type="and">  
   <condition attribute="estimatedclosedate" operator="next-x-fiscal-years" value="3"/>  
  </filter>  
 </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-115">The following example shows a FetchXML expression that finds all orders fulfilled in period three of any fiscal year, according to the organization’s fiscal year settings.</span><span class="sxs-lookup"><span data-stu-id="fdccb-115">The following example shows a FetchXML expression that finds all orders fulfilled in period three of any fiscal year, according to the organization’s fiscal year settings.</span></span> <span data-ttu-id="fdccb-116">The fiscal period value is specified in the value attribute of the condition tag.</span><span class="sxs-lookup"><span data-stu-id="fdccb-116">The fiscal period value is specified in the value attribute of the condition tag.</span></span> <span data-ttu-id="fdccb-117">If the organization uses fiscal months, the query returns results from month three.</span><span class="sxs-lookup"><span data-stu-id="fdccb-117">If the organization uses fiscal months, the query returns results from month three.</span></span> <span data-ttu-id="fdccb-118">If the organization uses fiscal quarters, the query returns results from quarter three.</span><span class="sxs-lookup"><span data-stu-id="fdccb-118">If the organization uses fiscal quarters, the query returns results from quarter three.</span></span> <span data-ttu-id="fdccb-119">If the organization uses fiscal semesters, no results are returned; there are only two semesters, and the value supplied is therefore out-of-range.</span><span class="sxs-lookup"><span data-stu-id="fdccb-119">If the organization uses fiscal semesters, no results are returned; there are only two semesters, and the value supplied is therefore out-of-range.</span></span>  
  
```xml  
<fetch>  
 <entity name="order">  
  <attribute name="name"/>  
  <filter type="and">  
   <condition attribute="datefulfilled" operator="in-fiscal-period" value="3"/>  
  </filter>  
 </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-120">The following example shows a FetchXML expression that finds all orders fulfilled in period three of fiscal year 2013, according to the organization’s fiscal year settings.</span><span class="sxs-lookup"><span data-stu-id="fdccb-120">The following example shows a FetchXML expression that finds all orders fulfilled in period three of fiscal year 2013, according to the organization’s fiscal year settings.</span></span> <span data-ttu-id="fdccb-121">If the organization uses fiscal months, the query returns results from month three.</span><span class="sxs-lookup"><span data-stu-id="fdccb-121">If the organization uses fiscal months, the query returns results from month three.</span></span> <span data-ttu-id="fdccb-122">If the organization uses fiscal quarters, the query returns results from quarter three.</span><span class="sxs-lookup"><span data-stu-id="fdccb-122">If the organization uses fiscal quarters, the query returns results from quarter three.</span></span> <span data-ttu-id="fdccb-123">If the organization uses fiscal semesters, no results are returned; there are only two semesters, and the value supplied is therefore out-of-range.</span><span class="sxs-lookup"><span data-stu-id="fdccb-123">If the organization uses fiscal semesters, no results are returned; there are only two semesters, and the value supplied is therefore out-of-range.</span></span>  
  
```xml  
<fetch>  
 <entity name="order">  
  <attribute name="name"/>  
  <filter type="and">  
   <condition attribute="datefulfilled" operator="in-fiscal-period-and-year">  
    <value>3</value>  
    <value>2013</value>  
   </condition>  
  </filter>  
 </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-124">The following example shows a FetchXML aggregation expression that sums the total amount of orders fulfilled and groups the result by fiscal semester and fiscal year.</span><span class="sxs-lookup"><span data-stu-id="fdccb-124">The following example shows a FetchXML aggregation expression that sums the total amount of orders fulfilled and groups the result by fiscal semester and fiscal year.</span></span>  
  
```xml  
<fetch aggregate="true">  
 <entity name="order">  
  <attribute name="totalamount" aggregate="sum" alias="total"/>  
  <attribute name="datefulfilled" groupby="true" dategrouping="fiscal-period"/>  
 </entity>  
</fetch>  
```  
  
<a name="OlderThan"></a>   
## <a name="using-older-than-clauses-for-date-and-time-values"></a><span data-ttu-id="fdccb-125">Using “older than” clauses for date and time values</span><span class="sxs-lookup"><span data-stu-id="fdccb-125">Using “older than” clauses for date and time values</span></span>  
 <span data-ttu-id="fdccb-126">The following example shows a FetchXML that finds incidents that are older than 30 minutes.</span><span class="sxs-lookup"><span data-stu-id="fdccb-126">The following example shows a FetchXML that finds incidents that are older than 30 minutes.</span></span>  
  
```  
<fetch>  
  <entity name="incident">  
    <attribute name="title" />  
    <attribute name="ticketnumber" />  
    <attribute name="createdon" />  
    <attribute name="incidentid" />  
    <filter type="and">  
      <condition attribute="createdon" operator="olderthan-x-minutes" value="30" />  
    </filter>  
  </entity>  
</fetch>  
```  
  
 <span data-ttu-id="fdccb-127">Use the following syntax to specify variious *older than* clauses in a FetchXML expression.</span><span class="sxs-lookup"><span data-stu-id="fdccb-127">Use the following syntax to specify variious *older than* clauses in a FetchXML expression.</span></span>  
  
 <span data-ttu-id="fdccb-128">Older than X minutes</span><span class="sxs-lookup"><span data-stu-id="fdccb-128">Older than X minutes</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-minutes" value="<VALUE>" />  
```  
  
> [!NOTE]
>  <span data-ttu-id="fdccb-129">This clause is not supported for date and time attributes with `DateOnly` behavior.</span><span class="sxs-lookup"><span data-stu-id="fdccb-129">This clause is not supported for date and time attributes with `DateOnly` behavior.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="fdccb-130">[Date and time query operators not supported for DateOnly behavior](../behavior-format-date-time-attribute.md#date-and-time-query-operators-not-supported-for-dateonly-behavior)</span><span class="sxs-lookup"><span data-stu-id="fdccb-130">[Date and time query operators not supported for DateOnly behavior](../behavior-format-date-time-attribute.md#date-and-time-query-operators-not-supported-for-dateonly-behavior)</span></span>
  
 <span data-ttu-id="fdccb-131">Older than X hours</span><span class="sxs-lookup"><span data-stu-id="fdccb-131">Older than X hours</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-hours" value="<VALUE>" />  
```  
  
> [!NOTE]
>  <span data-ttu-id="fdccb-132">This clause is not supported for date and time attributes with `DateOnly` behavior.</span><span class="sxs-lookup"><span data-stu-id="fdccb-132">This clause is not supported for date and time attributes with `DateOnly` behavior.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="fdccb-133">[Date and time query operators not supported for DateOnly behavior](../behavior-format-date-time-attribute.md#date-and-time-query-operators-not-supported-for-dateonly-behavior)</span><span class="sxs-lookup"><span data-stu-id="fdccb-133">[Date and time query operators not supported for DateOnly behavior](../behavior-format-date-time-attribute.md#date-and-time-query-operators-not-supported-for-dateonly-behavior)</span></span>  
  
 <span data-ttu-id="fdccb-134">Older than X days</span><span class="sxs-lookup"><span data-stu-id="fdccb-134">Older than X days</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-days" value="<VALUE>" />  
```  
  
 <span data-ttu-id="fdccb-135">Older than X weeks</span><span class="sxs-lookup"><span data-stu-id="fdccb-135">Older than X weeks</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-weeks" value="<VALUE>" />  
```  
  
 <span data-ttu-id="fdccb-136">Older than X months</span><span class="sxs-lookup"><span data-stu-id="fdccb-136">Older than X months</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-months" value="<VALUE>" />  
```  
  
 <span data-ttu-id="fdccb-137">Older than X years</span><span class="sxs-lookup"><span data-stu-id="fdccb-137">Older than X years</span></span>  
 ```xml  
<condition attribute="<AttributeName>" operator="olderthan-x-years" value="<VALUE>" />  
```  
  
> [!NOTE]
>  <span data-ttu-id="fdccb-138">Except for the **Older than X months** clause, all the other *older than* clauses are available only if you’re using versions later than [!INCLUDE[pn_crm_online_2015_update_1_shortest](../../includes/pn-crm-online-2015-update-1-shortest.md)] or [!INCLUDE[pn_crm_2015_service_pack_1_op_short](../../includes/pn-crm-2015-service-pack-1-op-short.md)].</span><span class="sxs-lookup"><span data-stu-id="fdccb-138">Except for the **Older than X months** clause, all the other *older than* clauses are available only if you’re using versions later than [!INCLUDE[pn_crm_online_2015_update_1_shortest](../../includes/pn-crm-online-2015-update-1-shortest.md)] or [!INCLUDE[pn_crm_2015_service_pack_1_op_short](../../includes/pn-crm-2015-service-pack-1-op-short.md)].</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fdccb-139">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="fdccb-139">See also</span></span>  
 <span data-ttu-id="fdccb-140">[Create Queries to Retrieve Data](retrieve-data-queries-sdk-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="fdccb-140">[Create Queries to Retrieve Data](retrieve-data-queries-sdk-assemblies.md) </span></span>  
 <span data-ttu-id="fdccb-141">[Building Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="fdccb-141">[Building Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 [<span data-ttu-id="fdccb-142">Use a left outer join in FetchXML to query for records "not in"</span><span class="sxs-lookup"><span data-stu-id="fdccb-142">Use a left outer join in FetchXML to query for records "not in"</span></span>](use-left-outer-join-fetchxml-query-records-not-in.md)
