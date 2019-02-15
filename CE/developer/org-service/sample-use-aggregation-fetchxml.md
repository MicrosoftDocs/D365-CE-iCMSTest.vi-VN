---
title: 'Sample: Use aggregation in FetchXML (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to retrieve aggregate record data using FetchXML
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
- retrieving aggregate record data by using FetchXML sample
- using aggregation in FetchXML sample
- FetchXML queries, samples
- sample for retrieving aggregate record data by using FetchXML
- building queries with FetchXML, samples
- sample for using aggregation in FetchXML
ms.assetid: 283151dc-212c-445d-8181-9baec0dcba75
caps.latest.revision: 28
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 0768065ccb796869ac2c7fb6dbc0de828cdb0065
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386144"
---
# <a name="sample-use-aggregation-in-fetchxml"></a><span data-ttu-id="83430-103">Sample: Use aggregation in FetchXML</span><span class="sxs-lookup"><span data-stu-id="83430-103">Sample: Use aggregation in FetchXML</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="83430-104">This sample code is for [!INCLUDE[pn_crm_2016_and_online_full](../../includes/pn-crm-2016-and-online-full.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="83430-104">This sample code is for [!INCLUDE[pn_crm_2016_and_online_full](../../includes/pn-crm-2016-and-online-full.md)] apps.</span></span> <span data-ttu-id="83430-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span><span class="sxs-lookup"><span data-stu-id="83430-105">Download the complete sample from [Sample: Work with Queries](https://code.msdn.microsoft.com/Sample-Work-with-Queries-8265a78e).</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="83430-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="83430-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="83430-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="83430-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="83430-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="83430-108">Demonstrates</span></span>  
 <span data-ttu-id="83430-109">This sample shows how to retrieve aggregate record data using FetchXML.</span><span class="sxs-lookup"><span data-stu-id="83430-109">This sample shows how to retrieve aggregate record data using FetchXML.</span></span>  
  
## <a name="example"></a><span data-ttu-id="83430-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="83430-110">Example</span></span>  
 [!code-csharp[Query#FetchAggregationAndGroupBy](../../snippets/csharp/CRMV8/query/cs/fetchaggregationandgroupby.cs#fetchaggregationandgroupby)]  
  
### <a name="see-also"></a><span data-ttu-id="83430-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="83430-111">See also</span></span>  
 <span data-ttu-id="83430-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="83430-112">[Sample: CrmServiceHelper Class](helper-code-serverconnection-class.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>   
 <span data-ttu-id="83430-113">[Using FetchXML Aggregration](use-fetchxml-aggregation.md) </span><span class="sxs-lookup"><span data-stu-id="83430-113">[Using FetchXML Aggregration](use-fetchxml-aggregation.md) </span></span>  
 <span data-ttu-id="83430-114">[Build Queries with FetchXML](build-queries-fetchxml.md) </span><span class="sxs-lookup"><span data-stu-id="83430-114">[Build Queries with FetchXML](build-queries-fetchxml.md) </span></span>  
 <span data-ttu-id="83430-115">[Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md) </span><span class="sxs-lookup"><span data-stu-id="83430-115">[Sample: Use FetchXML with a Paging Cookie](sample-use-fetchxml-paging-cookie.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Query.FetchExpression>
