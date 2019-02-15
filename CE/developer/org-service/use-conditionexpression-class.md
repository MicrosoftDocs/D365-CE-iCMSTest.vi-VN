---
title: Use the ConditionExpression class (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Read how you can use the ConditionExpression class to compare an attribute to a value or set of values by using an operator, such as “equal to” or “greater than”
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
- using the ConditionExpression class
- comparing attributes to a value or set of values by using operators, ConditionExpression class
- ConditionExpression class, about; properties for; and code examples
- using operators to compare attributes to a value or set of values, ConditionExpression class
- ConditionExpression class, comparing attributes to a value or set of values by using operators
- ConditionExpression class, passing condition expressions to other classes
ms.assetid: 68a072f6-e3d9-48f6-9e55-11df3dbd1bf5
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ba34a140788c136499d07b4c8fd83e2508cdb48f
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388020"
---
# <a name="use-the-conditionexpression-class"></a><span data-ttu-id="4a5aa-103">Use the ConditionExpression class</span><span class="sxs-lookup"><span data-stu-id="4a5aa-103">Use the ConditionExpression class</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4a5aa-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression> class to compare an attribute to a value or set of values by using an operator, such as “equal to” or “greater than”.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-104">In [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement, you can use the <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression> class to compare an attribute to a value or set of values by using an operator, such as “equal to” or “greater than”.</span></span> <span data-ttu-id="4a5aa-105">The `ConditionExpression` class lets you pass condition expressions as parameters to other classes, such as <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-105">The `ConditionExpression` class lets you pass condition expressions as parameters to other classes, such as <xref:Microsoft.Xrm.Sdk.Query.QueryExpression> and <xref:Microsoft.Xrm.Sdk.Query.FilterExpression>.</span></span>  
  
 <span data-ttu-id="4a5aa-106">The following table lists the properties you can set to create a condition using the `ConditionExpression` class.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-106">The following table lists the properties you can set to create a condition using the `ConditionExpression` class.</span></span>  
  
|<span data-ttu-id="4a5aa-107">Thuộc tính</span><span class="sxs-lookup"><span data-stu-id="4a5aa-107">Property</span></span>|<span data-ttu-id="4a5aa-108">Mô tả</span><span class="sxs-lookup"><span data-stu-id="4a5aa-108">Description</span></span>|  
|--------------|-----------------|  
|<xref:Microsoft.Xrm.Sdk.Query.ConditionExpression.AttributeName>|<span data-ttu-id="4a5aa-109">Specifies the logical name of the attribute in the condition expression.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-109">Specifies the logical name of the attribute in the condition expression.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.ConditionExpression.Operator>|<span data-ttu-id="4a5aa-110">Specifies the condition operator.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-110">Specifies the condition operator.</span></span> <span data-ttu-id="4a5aa-111">This is set by using the <xref:Microsoft.Xrm.Sdk.Query.ConditionOperator> enumeration.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-111">This is set by using the <xref:Microsoft.Xrm.Sdk.Query.ConditionOperator> enumeration.</span></span>|  
|<xref:Microsoft.Xrm.Sdk.Query.ConditionExpression.Values>|<span data-ttu-id="4a5aa-112">Specifies the values of the attribute.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-112">Specifies the values of the attribute.</span></span>|  
  
 <span data-ttu-id="4a5aa-113">When using the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.AddCondition(Microsoft.Xrm.Sdk.Query.ConditionExpression)> method (or the constructor for <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>), it’s important to understand whether the array is being added as multiple values or as an array.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-113">When using the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression.AddCondition(Microsoft.Xrm.Sdk.Query.ConditionExpression)> method (or the constructor for <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>), it’s important to understand whether the array is being added as multiple values or as an array.</span></span>  
  
 <span data-ttu-id="4a5aa-114">The following code example shows two different outcomes depending on how the array is used.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-114">The following code example shows two different outcomes depending on how the array is used.</span></span>  
  
```csharp  
string[] values = new string[] { "Value1", "Value2" };  
ConditionExpression c = new ConditionExpression("name", ConditionOperator.In, values);  
Console.WriteLine(c.Values.Count); //This will output 2   
string[] values = new string[] { "Value1", "Value2" }object value = values;  
ConditionExpression c = new ConditionExpression("name", ConditionOperator.In, value);  
Console.WriteLine(c.Values.Count); //This will output 1  
  
```  
  
 <span data-ttu-id="4a5aa-115">In some cases, it is necessary to cast to either `object[]` or `object`, depending on the desired behavior.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-115">In some cases, it is necessary to cast to either `object[]` or `object`, depending on the desired behavior.</span></span>  
  
 <span data-ttu-id="4a5aa-116">When you create a condition that compares an attribute value to an enumeration, such as a state code, you must use the `ToString` method to convert the value to a string.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-116">When you create a condition that compares an attribute value to an enumeration, such as a state code, you must use the `ToString` method to convert the value to a string.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4a5aa-117">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4a5aa-117">Example</span></span>  
 <span data-ttu-id="4a5aa-118">The following code example shows how to use the `ConditionExpression` class.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-118">The following code example shows how to use the `ConditionExpression` class.</span></span>  
  
```csharp  
  
//  Query using ConditionExpression    
ConditionExpression condition1 = new ConditionExpression();  
condition1.AttributeName = "lastname";    
condition1.Operator = ConditionOperator.Equal;    
condition1.Values.Add("Brown");                    
FilterExpression filter1 = new FilterExpression();    
filter1.Conditions.Add(condition1);    
QueryExpression query = new QueryExpression("contact");    
query.ColumnSet.AddColumns("firstname", "lastname");    
query.Criteria.AddFilter(filter1);    
EntityCollection result1 = _serviceProxy.RetrieveMultiple(query);    
Console.WriteLine();    
Console.WriteLine("Query using Query Expression with ConditionExpression and FilterExpression");    
Console.WriteLine("---------------------------------------");    
foreach (var a in result1.Entities)    
{  
      Console.WriteLine("Name: " + a.Attributes["firstname"] + " " + a.Attributes["lastname"]);    
}    
Console.WriteLine("---------------------------------------");  
```  
  
## <a name="example"></a><span data-ttu-id="4a5aa-119">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4a5aa-119">Example</span></span>  
 <span data-ttu-id="4a5aa-120">The following code example shows how to use the `ConditionExpression` class to test for the inactive state.</span><span class="sxs-lookup"><span data-stu-id="4a5aa-120">The following code example shows how to use the `ConditionExpression` class to test for the inactive state.</span></span>  
  
```csharp  
  
ConditionExpression condition3 = new ConditionExpression();  
condition3.AttributeName = "statecode";  
condition3.Operator = ConditionOperator.Equal;  
condition3.Values.Add(AccountState.Active);  
  
```  
  
### <a name="see-also"></a><span data-ttu-id="4a5aa-121">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4a5aa-121">See also</span></span>  
 <span data-ttu-id="4a5aa-122">[Building Queries](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="4a5aa-122">[Building Queries](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="4a5aa-123">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="4a5aa-123">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <span data-ttu-id="4a5aa-124">[Use the FilterExpression Class](use-filterexpression-class.md) </span><span class="sxs-lookup"><span data-stu-id="4a5aa-124">[Use the FilterExpression Class](use-filterexpression-class.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.ConditionExpression>
