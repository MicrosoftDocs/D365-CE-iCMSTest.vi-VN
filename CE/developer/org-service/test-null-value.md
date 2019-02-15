---
title: Test for a null value (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: This sample shows how to test for a null value by using the FilterExpression and QueryByAttribute classes
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
- testing for null values, about and code examples
- testing for equality or inequality of
- testing for null values
- null values, testing for
- testing for null values, by using the FilterExpression and QueryByAttribute classes
ms.assetid: f0998642-40e2-4283-a306-b61d48abec98
caps.latest.revision: 11
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 8955019007c17dfa0b15f1c74740a9c85772082a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388028"
---
# <a name="test-for-a-null-value"></a>Test for a null value

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

The following code example shows how to test for a null value by using the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> and <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> classes.  
  
## <a name="example"></a>Ví dụ  
 Use this code to test for equality by using the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class.  
  
```csharp  
FilterExpression null_filter = new FilterExpression(LogicalOperator.And);   
null_filter.FilterOperator = LogicalOperator.And;   
null_filter.AddCondition("leadid", ConditionOperator.Null);  
  
```  
  
## <a name="example"></a>Ví dụ  
 Use this code to test for inequality by using the <xref:Microsoft.Xrm.Sdk.Query.FilterExpression> class.  
  
```csharp  
  
FilterExpression filter = new FilterExpression(LogicalOperator.And);   
filter.FilterOperator = LogicalOperator.And;   
filter.AddCondition("leadid", ConditionOperator.NotNull);  
```  
  
## <a name="example"></a>Ví dụ  
 Use this code to test for equality by using the <xref:Microsoft.Xrm.Sdk.Query.QueryByAttribute> class.  
  
```csharp  
  
QueryByAttribute qba = new QueryByAttribute("account");   
qba.ColumnSet = new ColumnSet("name","address1_stateorprovince");   
qba.AddAttributeValue("donotfax", null);  
```  
  
### <a name="see-also"></a>Xem thêm  
 [Building Queries with QueryExpression](build-queries-with-queryexpression.md)   
 [Page large result sets with QueryExpression](page-large-result-sets-with-queryexpression.md)
