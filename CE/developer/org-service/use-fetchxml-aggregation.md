---
title: Use FetchXML aggregation (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read about the grouping and aggregation features of FetchXML that let you calculate sum, average min, max and count
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- FetchXML queries
- using FetchXML aggregation (grouping), code examples
- using FetchXML aggregation (grouping), null value limitations when computing averages (avgaggregate attribute)
- using FetchXML aggregation (grouping), difference between aggregate queries and standard queries
- using FetchXML aggregation (grouping), aggregation functions supported
- FetchXML queries, grouping and aggregation features
- FetchXML queries, using FetchXML to construct queries
- building queries with FetchXML, using FetchXML aggregation (grouping)
- using FetchXML aggregation (grouping), effects of null values when minimum or maximum data is computed
ms.assetid: be0fb5cf-4ba8-487f-b517-ae1c24045478
caps.latest.revision: 31
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 15ea09f8aa182d94ce9c8c259b9c04317a3f98ef
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387228"
---
# <a name="use-fetchxml-aggregation"></a><span data-ttu-id="505be-103">Use FetchXML aggregation</span><span class="sxs-lookup"><span data-stu-id="505be-103">Use FetchXML aggregation</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="505be-104">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, `FetchXML` includes grouping and aggregation features that let you calculate sum, average min, max and count.</span><span class="sxs-lookup"><span data-stu-id="505be-104">In [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps, `FetchXML` includes grouping and aggregation features that let you calculate sum, average min, max and count.</span></span>  
  
 <span data-ttu-id="505be-105">The following aggregate functions are supported:</span><span class="sxs-lookup"><span data-stu-id="505be-105">The following aggregate functions are supported:</span></span>  
  
-   <span data-ttu-id="505be-106">sum</span><span class="sxs-lookup"><span data-stu-id="505be-106">sum</span></span>  
  
-   <span data-ttu-id="505be-107">avg</span><span class="sxs-lookup"><span data-stu-id="505be-107">avg</span></span>  
  
-   <span data-ttu-id="505be-108">min</span><span class="sxs-lookup"><span data-stu-id="505be-108">min</span></span>  
  
-   <span data-ttu-id="505be-109">max</span><span class="sxs-lookup"><span data-stu-id="505be-109">max</span></span>  
  
-   <span data-ttu-id="505be-110">count(\*)</span><span class="sxs-lookup"><span data-stu-id="505be-110">count(\*)</span></span>  
  
-   <span data-ttu-id="505be-111">count(*attribute name*)</span><span class="sxs-lookup"><span data-stu-id="505be-111">count(*attribute name*)</span></span>  
  
<a name="Aggregation"></a>

## <a name="about-aggregation"></a><span data-ttu-id="505be-112">About aggregation</span><span class="sxs-lookup"><span data-stu-id="505be-112">About aggregation</span></span>
 
 <span data-ttu-id="505be-113">To create an aggregate attribute, set the keyword `aggregate` to `true`, then specify a valid *entity name*, *attribute name*, and *alias* (variable name).</span><span class="sxs-lookup"><span data-stu-id="505be-113">To create an aggregate attribute, set the keyword `aggregate` to `true`, then specify a valid *entity name*, *attribute name*, and *alias* (variable name).</span></span> <span data-ttu-id="505be-114">You must also specify the type of aggregation you want to perform.</span><span class="sxs-lookup"><span data-stu-id="505be-114">You must also specify the type of aggregation you want to perform.</span></span>  
  
 <span data-ttu-id="505be-115">The following example shows a simple aggregate attribute in `FetchXML`.</span><span class="sxs-lookup"><span data-stu-id="505be-115">The following example shows a simple aggregate attribute in `FetchXML`.</span></span>  
  
```xml  
<fetch distinct='false' mapping='logical' aggregate='true'>   
   <entity name='entity name'>   
      <attribute name='attribute name' aggregate='count' alias='alias name'/>   
   </entity>   
</fetch>
```  
  
 <span data-ttu-id="505be-116">The result of a query with an aggregate attribute is different from the results of a standard query.</span><span class="sxs-lookup"><span data-stu-id="505be-116">The result of a query with an aggregate attribute is different from the results of a standard query.</span></span> <span data-ttu-id="505be-117">The alias value is used as the tag identifier for the aggregate result.</span><span class="sxs-lookup"><span data-stu-id="505be-117">The alias value is used as the tag identifier for the aggregate result.</span></span>  
  
 <span data-ttu-id="505be-118">The following example shows the format of the result of an aggregate query.</span><span class="sxs-lookup"><span data-stu-id="505be-118">The following example shows the format of the result of an aggregate query.</span></span>  
  
```xml
<resultset morerecords="0"'>   
   <result>  
      <alias>aggregate value</alias>  
   </result>  
</resultset>
```  
  
 <span data-ttu-id="505be-119">The following example shows the results of a query when the alias variable is set to `account_count`.</span><span class="sxs-lookup"><span data-stu-id="505be-119">The following example shows the results of a query when the alias variable is set to `account_count`.</span></span>  
  
```xml
<resultset morerecords="0"'>   
   <result>  
      <account_count>20</account_count>  
   </result>  
</resultset>
```  
  
<a name="AVG"></a>

## <a name="avg"></a><span data-ttu-id="505be-120">Avg</span><span class="sxs-lookup"><span data-stu-id="505be-120">Avg</span></span>

 <span data-ttu-id="505be-121">The following example shows how to use the `avg``aggregate` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-121">The following example shows how to use the `avg``aggregate` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy1](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby1.cs#fetchaggregationandgroupby1)]  
  
### <a name="limitation-with-null-values-while-computing-average"></a><span data-ttu-id="505be-122">Limitation with null values while computing average</span><span class="sxs-lookup"><span data-stu-id="505be-122">Limitation with null values while computing average</span></span>  
 <span data-ttu-id="505be-123">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the average of data.</span><span class="sxs-lookup"><span data-stu-id="505be-123">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the average of data.</span></span> <span data-ttu-id="505be-124">However, zero (0) is used.</span><span class="sxs-lookup"><span data-stu-id="505be-124">However, zero (0) is used.</span></span>  
  
 <span data-ttu-id="505be-125">In the following example, with the following data, the average for Account 1 (two entries) is shown as 250 whereas the average for Account 2 (two entries) is shown as 125.</span><span class="sxs-lookup"><span data-stu-id="505be-125">In the following example, with the following data, the average for Account 1 (two entries) is shown as 250 whereas the average for Account 2 (two entries) is shown as 125.</span></span>  
  
|<span data-ttu-id="505be-126">Chủ đề</span><span class="sxs-lookup"><span data-stu-id="505be-126">Topic</span></span>|<span data-ttu-id="505be-127">Khách hàng Tiềm năng</span><span class="sxs-lookup"><span data-stu-id="505be-127">Potential Customer</span></span>|<span data-ttu-id="505be-128">Estimated value</span><span class="sxs-lookup"><span data-stu-id="505be-128">Estimated value</span></span>|  
|-----|------------------|---------------|  
|<span data-ttu-id="505be-129">Cơ hội 1</span><span class="sxs-lookup"><span data-stu-id="505be-129">Opportunity 1</span></span>|<span data-ttu-id="505be-130">Tài khoản 1</span><span class="sxs-lookup"><span data-stu-id="505be-130">Account 1</span></span>|<span data-ttu-id="505be-131">rỗng</span><span class="sxs-lookup"><span data-stu-id="505be-131">null</span></span>|  
|<span data-ttu-id="505be-132">Cơ hội 2</span><span class="sxs-lookup"><span data-stu-id="505be-132">Opportunity 2</span></span>|<span data-ttu-id="505be-133">Tài khoản 1</span><span class="sxs-lookup"><span data-stu-id="505be-133">Account 1</span></span>|<span data-ttu-id="505be-134">250</span><span class="sxs-lookup"><span data-stu-id="505be-134">250</span></span>|  
|<span data-ttu-id="505be-135">Cơ hội 3</span><span class="sxs-lookup"><span data-stu-id="505be-135">Opportunity 3</span></span>|<span data-ttu-id="505be-136">Tài khoản 2</span><span class="sxs-lookup"><span data-stu-id="505be-136">Account 2</span></span>|<span data-ttu-id="505be-137">0</span><span class="sxs-lookup"><span data-stu-id="505be-137">0</span></span>|  
|<span data-ttu-id="505be-138">Cơ hội 4</span><span class="sxs-lookup"><span data-stu-id="505be-138">Opportunity 4</span></span>|<span data-ttu-id="505be-139">Tài khoản 2</span><span class="sxs-lookup"><span data-stu-id="505be-139">Account 2</span></span>|<span data-ttu-id="505be-140">250</span><span class="sxs-lookup"><span data-stu-id="505be-140">250</span></span>|  
  
<a name="count"></a>

## <a name="count"></a><span data-ttu-id="505be-141">Count</span><span class="sxs-lookup"><span data-stu-id="505be-141">Count</span></span>

 <span data-ttu-id="505be-142">The following example shows how to use the `count``aggregate` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-142">The following example shows how to use the `count``aggregate` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy2](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby2.cs#fetchaggregationandgroupby2)]  
  
<a name="count_column"></a>

### <a name="countcolumn"></a><span data-ttu-id="505be-143">CountColumn</span><span class="sxs-lookup"><span data-stu-id="505be-143">CountColumn</span></span>

 <span data-ttu-id="505be-144">The following example shows how to use the `countcolumn``aggregate` attribute to count columns.</span><span class="sxs-lookup"><span data-stu-id="505be-144">The following example shows how to use the `countcolumn``aggregate` attribute to count columns.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy3](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby3.cs#fetchaggregationandgroupby3)]  
  
<a name="count_distinct"></a>
 
### <a name="count-distinct-columns"></a><span data-ttu-id="505be-145">Count distinct columns</span><span class="sxs-lookup"><span data-stu-id="505be-145">Count distinct columns</span></span>

 <span data-ttu-id="505be-146">The following example shows how to use the `countcolumn``aggregate` attribute with the `distinct` attribute to count distinct columns.</span><span class="sxs-lookup"><span data-stu-id="505be-146">The following example shows how to use the `countcolumn``aggregate` attribute with the `distinct` attribute to count distinct columns.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy4](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby4.cs#fetchaggregationandgroupby4)]  
  
<a name="max"></a>

## <a name="max"></a><span data-ttu-id="505be-147">Max</span><span class="sxs-lookup"><span data-stu-id="505be-147">Max</span></span>

 <span data-ttu-id="505be-148">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the maximum of data.</span><span class="sxs-lookup"><span data-stu-id="505be-148">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the maximum of data.</span></span> <span data-ttu-id="505be-149">However, zero (0) is used.</span><span class="sxs-lookup"><span data-stu-id="505be-149">However, zero (0) is used.</span></span>  
  
 <span data-ttu-id="505be-150">The following example shows how to use the `max``aggregate` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-150">The following example shows how to use the `max``aggregate` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy5](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby5.cs#fetchaggregationandgroupby5)]  
  
<a name="min"></a>
 
## <a name="min"></a><span data-ttu-id="505be-151">Min</span><span class="sxs-lookup"><span data-stu-id="505be-151">Min</span></span>

 <span data-ttu-id="505be-152">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the minimum of data.</span><span class="sxs-lookup"><span data-stu-id="505be-152">**Null** values are not considered when [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] apps computes the minimum of data.</span></span> <span data-ttu-id="505be-153">However, zero (0) is used.</span><span class="sxs-lookup"><span data-stu-id="505be-153">However, zero (0) is used.</span></span>  
  
 <span data-ttu-id="505be-154">The following example shows how to use the `min``aggregate` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-154">The following example shows how to use the `min``aggregate` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy6](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby6.cs#fetchaggregationandgroupby6)]  
  
<a name="sum"></a>

## <a name="sum"></a><span data-ttu-id="505be-155">Sum</span><span class="sxs-lookup"><span data-stu-id="505be-155">Sum</span></span>

 <span data-ttu-id="505be-156">The following example shows how to use the `sum``aggregate` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-156">The following example shows how to use the `sum``aggregate` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy7](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby7.cs#fetchaggregationandgroupby7)]  
  
<a name="mult_agg"></a>
 
## <a name="multiple-aggregates"></a><span data-ttu-id="505be-157">Multiple aggregates</span><span class="sxs-lookup"><span data-stu-id="505be-157">Multiple aggregates</span></span>

 <span data-ttu-id="505be-158">The following example shows how to use multiple `aggregate` attributes to set a minimum and maximum.</span><span class="sxs-lookup"><span data-stu-id="505be-158">The following example shows how to use multiple `aggregate` attributes to set a minimum and maximum.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy8](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby8.cs#fetchaggregationandgroupby8)]  
  
<a name="groupby"></a>
 
## <a name="group-by"></a><span data-ttu-id="505be-159">Group by</span><span class="sxs-lookup"><span data-stu-id="505be-159">Group by</span></span>

 <span data-ttu-id="505be-160">The following example shows how to use multiple `aggregate` attributes and a linked `groupby` attribute.</span><span class="sxs-lookup"><span data-stu-id="505be-160">The following example shows how to use multiple `aggregate` attributes and a linked `groupby` attribute.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy9](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby9.cs#fetchaggregationandgroupby9)]  
  
 <span data-ttu-id="505be-161">The samples below show the following group by examples:</span><span class="sxs-lookup"><span data-stu-id="505be-161">The samples below show the following group by examples:</span></span>  
  
 [<span data-ttu-id="505be-162">Group by with linked entity</span><span class="sxs-lookup"><span data-stu-id="505be-162">Group by with linked entity</span></span>](use-fetchxml-aggregation.md#groupby_linked)  
  
 [<span data-ttu-id="505be-163">Group by year</span><span class="sxs-lookup"><span data-stu-id="505be-163">Group by year</span></span>](use-fetchxml-aggregation.md#groupby_year)  
  
 [<span data-ttu-id="505be-164">Group by quarter</span><span class="sxs-lookup"><span data-stu-id="505be-164">Group by quarter</span></span>](use-fetchxml-aggregation.md#groupby_quarter)  
  
 [<span data-ttu-id="505be-165">Group by month</span><span class="sxs-lookup"><span data-stu-id="505be-165">Group by month</span></span>](use-fetchxml-aggregation.md#groupby_month)  
  
 [<span data-ttu-id="505be-166">Group by week</span><span class="sxs-lookup"><span data-stu-id="505be-166">Group by week</span></span>](use-fetchxml-aggregation.md#groupby_week)  
  
 [<span data-ttu-id="505be-167">Group by day</span><span class="sxs-lookup"><span data-stu-id="505be-167">Group by day</span></span>](use-fetchxml-aggregation.md#groupby_day)  
  
 [<span data-ttu-id="505be-168">Multiple group by</span><span class="sxs-lookup"><span data-stu-id="505be-168">Multiple group by</span></span>](use-fetchxml-aggregation.md#Multiple_GroupBy)  
  
<a name="groupby_linked"></a>

### <a name="group-by-with-linked-entity"></a><span data-ttu-id="505be-169">Group by with linked entity</span><span class="sxs-lookup"><span data-stu-id="505be-169">Group by with linked entity</span></span>

 <span data-ttu-id="505be-170">The following example shows how to use the `sum``aggregate` attribute to sum linked entity values.</span><span class="sxs-lookup"><span data-stu-id="505be-170">The following example shows how to use the `sum``aggregate` attribute to sum linked entity values.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy10](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby10.cs#fetchaggregationandgroupby10)]  
  
<a name="groupby_year"></a>

### <a name="group-by-year"></a><span data-ttu-id="505be-171">Group by year</span><span class="sxs-lookup"><span data-stu-id="505be-171">Group by year</span></span>

 <span data-ttu-id="505be-172">Group By for dates uses the day, week, month, quarter, or year value.</span><span class="sxs-lookup"><span data-stu-id="505be-172">Group By for dates uses the day, week, month, quarter, or year value.</span></span> <span data-ttu-id="505be-173">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by year.</span><span class="sxs-lookup"><span data-stu-id="505be-173">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by year.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy11](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby11.cs#fetchaggregationandgroupby11)]  
  
<a name="groupby_quarter"></a>
 
### <a name="group-by-quarter"></a><span data-ttu-id="505be-174">Group by quarter</span><span class="sxs-lookup"><span data-stu-id="505be-174">Group by quarter</span></span>

 <span data-ttu-id="505be-175">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by quarter.</span><span class="sxs-lookup"><span data-stu-id="505be-175">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by quarter.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy12](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby12.cs#fetchaggregationandgroupby12)]  
  
<a name="groupby_month"></a>

### <a name="group-by-month"></a><span data-ttu-id="505be-176">Group by month</span><span class="sxs-lookup"><span data-stu-id="505be-176">Group by month</span></span>

 <span data-ttu-id="505be-177">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by month.</span><span class="sxs-lookup"><span data-stu-id="505be-177">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by month.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy13](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby13.cs#fetchaggregationandgroupby13)]  
  
<a name="groupby_week"></a>

### <a name="group-by-week"></a><span data-ttu-id="505be-178">Group by week</span><span class="sxs-lookup"><span data-stu-id="505be-178">Group by week</span></span>

 <span data-ttu-id="505be-179">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by week.</span><span class="sxs-lookup"><span data-stu-id="505be-179">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by week.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy14](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby14.cs#fetchaggregationandgroupby14)]  
  
<a name="groupby_day"></a>

### <a name="group-by-day"></a><span data-ttu-id="505be-180">Group by day</span><span class="sxs-lookup"><span data-stu-id="505be-180">Group by day</span></span>

 <span data-ttu-id="505be-181">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by day.</span><span class="sxs-lookup"><span data-stu-id="505be-181">The following example shows how to use the `aggregate` attribute and the `groupby` attribute to group the results by day.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy15](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby15.cs#fetchaggregationandgroupby15)]  
  
<a name="Multiple_GroupBy"></a>
 
### <a name="multiple-group-by"></a><span data-ttu-id="505be-182">Multiple group by</span><span class="sxs-lookup"><span data-stu-id="505be-182">Multiple group by</span></span>

 <span data-ttu-id="505be-183">The following example shows how to use the `aggregate` attribute and multiple `groupby` clauses.</span><span class="sxs-lookup"><span data-stu-id="505be-183">The following example shows how to use the `aggregate` attribute and multiple `groupby` clauses.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy16](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby16.cs#fetchaggregationandgroupby16)]  
  
<a name="orderby_aggregate"></a>

## <a name="order-by"></a><span data-ttu-id="505be-184">Order by</span><span class="sxs-lookup"><span data-stu-id="505be-184">Order by</span></span>

 <span data-ttu-id="505be-185">The following example shows how to use the `aggregate` attribute and multiple `orderby` clauses.</span><span class="sxs-lookup"><span data-stu-id="505be-185">The following example shows how to use the `aggregate` attribute and multiple `orderby` clauses.</span></span>  
  
 [!code-csharp[Query#FetchAggregationAndGroupBy17](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby17.cs#fetchaggregationandgroupby17)]  
  
### <a name="see-also"></a><span data-ttu-id="505be-186">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="505be-186">See also</span></span>  
 <span data-ttu-id="505be-187">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="505be-187">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="505be-188">[Page Large Result Sets with FetchXML](page-large-result-sets-with-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="505be-188">[Page Large Result Sets with FetchXML](page-large-result-sets-with-fetchxml.md) </span></span>  
 <span data-ttu-id="505be-189">[Fetch XML Schema](fetchxml-schema.md) </span><span class="sxs-lookup"><span data-stu-id="505be-189">[Fetch XML Schema](fetchxml-schema.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 <xref:Microsoft.Xrm.Sdk.Messages.RetrieveMultipleRequest>   
 <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>
