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
# <a name="sample-convert-queries-between-fetch-and-queryexpression"></a><span data-ttu-id="6ce0e-103">Sample: Convert queries between Fetch and QueryExpression</span><span class="sxs-lookup"><span data-stu-id="6ce0e-103">Sample: Convert queries between Fetch and QueryExpression</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6ce0e-104">This sample code   is for [!INCLUDE[pn_crm_2016_and_online_full](../../includes/pn-crm-2016-and-online-full.md)].</span><span class="sxs-lookup"><span data-stu-id="6ce0e-104">This sample code   is for [!INCLUDE[pn_crm_2016_and_online_full](../../includes/pn-crm-2016-and-online-full.md)].</span></span> <span data-ttu-id="6ce0e-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="6ce0e-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="6ce0e-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="6ce0e-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="6ce0e-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="6ce0e-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="6ce0e-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="6ce0e-108">Demonstrates</span></span>  
 <span data-ttu-id="6ce0e-109">This sample shows how to convert queries between FetchXML and  Query Expression.</span><span class="sxs-lookup"><span data-stu-id="6ce0e-109">This sample shows how to convert queries between FetchXML and  Query Expression.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6ce0e-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="6ce0e-110">Example</span></span>  
 [!code-csharp[Query#FetchXmlAndQueryExpressionQueryConversion](../../snippets/csharp/CRMV8/query/cs/fetchxmlandqueryexpressionqueryconversion.cs#fetchxmlandqueryexpressionqueryconversion)]  
  
### <a name="see-also"></a><span data-ttu-id="6ce0e-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6ce0e-111">See also</span></span>  
 <span data-ttu-id="6ce0e-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="6ce0e-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 <span data-ttu-id="6ce0e-113">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="6ce0e-113">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="6ce0e-114">[Sample: Validate and Execute a Saved Query](sample-validate-execute-saved-query.md) </span><span class="sxs-lookup"><span data-stu-id="6ce0e-114">[Sample: Validate and Execute a Saved Query](sample-validate-execute-saved-query.md) </span></span>  
 <span data-ttu-id="6ce0e-115">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span><span class="sxs-lookup"><span data-stu-id="6ce0e-115">[Build Queries with QueryExpression](build-queries-with-queryexpression.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>
