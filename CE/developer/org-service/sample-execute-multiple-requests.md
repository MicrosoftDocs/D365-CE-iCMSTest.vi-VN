---
title: 'Sample: Execute multiple requests (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample uses a single web method call to execute multiple message requests
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 39f237ea-8805-4a45-925e-2663ff635611
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 9cded6f1297971f0e2269f36753976ed6b21f349
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387879"
---
# <a name="sample-execute-multiple-requests"></a><span data-ttu-id="8858c-103">Sample: Execute multiple requests</span><span class="sxs-lookup"><span data-stu-id="8858c-103">Sample: Execute multiple requests</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="8858c-104">Sending a large number of individual organization message requests over a network, as you would do in a bulk data import operation, is affected by network performance.</span><span class="sxs-lookup"><span data-stu-id="8858c-104">Sending a large number of individual organization message requests over a network, as you would do in a bulk data import operation, is affected by network performance.</span></span> <span data-ttu-id="8858c-105">For improved performance, [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps supports batching of requests into a single web service method call.</span><span class="sxs-lookup"><span data-stu-id="8858c-105">For improved performance, [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] apps supports batching of requests into a single web service method call.</span></span>  
  
 <span data-ttu-id="8858c-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="8858c-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)].</span></span> <span data-ttu-id="8858c-107">Download the sample: [Work with multiple requests](https://code.msdn.microsoft.com/Sample-Execute-multiple-ec698fa3).</span><span class="sxs-lookup"><span data-stu-id="8858c-107">Download the sample: [Work with multiple requests](https://code.msdn.microsoft.com/Sample-Execute-multiple-ec698fa3).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="8858c-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="8858c-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="8858c-109">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="8858c-109">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="8858c-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="8858c-110">Demonstrates</span></span>  
 <span data-ttu-id="8858c-111">This sample shows how to execute multiple organization message requests by using a single web service method call, passing <xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest> as a parameter.</span><span class="sxs-lookup"><span data-stu-id="8858c-111">This sample shows how to execute multiple organization message requests by using a single web service method call, passing <xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest> as a parameter.</span></span> <span data-ttu-id="8858c-112">Reducing the number of message requests that must be transmitted over the network results in increased message processing performance.</span><span class="sxs-lookup"><span data-stu-id="8858c-112">Reducing the number of message requests that must be transmitted over the network results in increased message processing performance.</span></span> <span data-ttu-id="8858c-113">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-execute-multiple-requests.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="8858c-113">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-execute-multiple-requests.md#complete_sample).</span></span>  
  
## <a name="example"></a><span data-ttu-id="8858c-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="8858c-114">Example</span></span>  
 <span data-ttu-id="8858c-115">This sample uses a single web method call to execute all message requests in a collection.</span><span class="sxs-lookup"><span data-stu-id="8858c-115">This sample uses a single web method call to execute all message requests in a collection.</span></span> <span data-ttu-id="8858c-116">Settings to alter the execution behavior are also shown.</span><span class="sxs-lookup"><span data-stu-id="8858c-116">Settings to alter the execution behavior are also shown.</span></span>  
  
 [!code-csharp[ExecuteMultiple#ExecuteMultiple1](../../snippets/csharp/CRMV8/executemultiple/cs/executemultiple1.cs#executemultiple1)]  
  
<a name="complete_sample"></a>   
## <a name="complete-sample-code"></a><span data-ttu-id="8858c-117">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="8858c-117">Complete sample code</span></span>  
 [!code-csharp[ExecuteMultiple#ExecuteMultiple](../../snippets/csharp/CRMV8/executemultiple/cs/executemultiple.cs#executemultiple)]  
  
### <a name="see-also"></a><span data-ttu-id="8858c-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8858c-118">See also</span></span>  
 <span data-ttu-id="8858c-119">[Use the IOrganizationService Web Service to Read and Write Data or Metadata](../org-service/use-organization-service-read-write-data-metadata.md) </span><span class="sxs-lookup"><span data-stu-id="8858c-119">[Use the IOrganizationService Web Service to Read and Write Data or Metadata](../org-service/use-organization-service-read-write-data-metadata.md) </span></span>  
 <xref:Microsoft.Xrm.Sdk.Messages.ExecuteMultipleRequest>   
 <xref:Microsoft.Xrm.Sdk.ExecuteMultipleSettings>   
 [<span data-ttu-id="8858c-120">Use Execute Multiple to Improve Performance for Bulk Data Load</span><span class="sxs-lookup"><span data-stu-id="8858c-120">Use Execute Multiple to Improve Performance for Bulk Data Load</span></span>](use-executemultiple-improve-performance-bulk-data-load.md)
