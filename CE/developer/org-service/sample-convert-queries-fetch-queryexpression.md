---
title: 'Sample: Convert queries between Fetch and QueryExpression (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to convert queries between FetchXML and Query Expression
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for converting queries between fetch and query expressions
- converting queries between fetch and query expressions sample
- FetchXML queries, samples
- building queries with FetchXML, samples
ms.assetid: fa08b0e7-11e1-4ac5-b809-91660a4fb147
caps.latest.revision: 15
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a5386c5135aa437b79a62d6a11297406cda964f9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387769"
---
# <a name="sample-convert-queries-between-fetch-and-queryexpression"></a>Sample: Convert queries between Fetch and QueryExpression

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code   is for [!INCLUDE[pn_crm_2016_and_online_full](../../includes/pn-crm-2016-and-online-full.md)]. Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to convert queries between FetchXML and  Query Expression.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Query#FetchXmlAndQueryExpressionQueryConversion](../../snippets/csharp/CRMV8/query/cs/fetchxmlandqueryexpressionqueryconversion.cs#fetchxmlandqueryexpressionqueryconversion)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 [Build Queries with FetchXML](build-queries-fetchxml.md)   
 [Sample: Validate and Execute a Saved Query](sample-validate-execute-saved-query.md)   
 [Build Queries with QueryExpression](build-queries-with-queryexpression.md)   
 <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>
