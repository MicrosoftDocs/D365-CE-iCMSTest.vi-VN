---
title: 'Sample: Execute multiple requests in transaction (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to execute multiple organization message requests in a single database transaction by using a single web service method call, passing ExecuteTransactionRequest as a parameter
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 1ba7b824-6cbf-41f8-87a3-901d42ab5aa1
author: JimDaly
ms.author: jdaly
manager: sakudes
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 8
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ea5531275132610fcc7607764dc11ad1bc9d2cf0
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388424"
---
# <a name="sample-execute-multiple-requests-in-transaction"></a><span data-ttu-id="d3c45-103">Sample: Execute multiple requests in transaction</span><span class="sxs-lookup"><span data-stu-id="d3c45-103">Sample: Execute multiple requests in transaction</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] <span data-ttu-id="d3c45-104">apps supports batching of requests into a single web service method call.</span><span class="sxs-lookup"><span data-stu-id="d3c45-104">apps supports batching of requests into a single web service method call.</span></span> <span data-ttu-id="d3c45-105">Each request in the batch is executed as part of a single database transaction.</span><span class="sxs-lookup"><span data-stu-id="d3c45-105">Each request in the batch is executed as part of a single database transaction.</span></span> <span data-ttu-id="d3c45-106">Failure of any request to complete successfully causes a rollback of any completed requests and no further processing is performed on requests not yet executed.</span><span class="sxs-lookup"><span data-stu-id="d3c45-106">Failure of any request to complete successfully causes a rollback of any completed requests and no further processing is performed on requests not yet executed.</span></span>

<span data-ttu-id="d3c45-107">Download the sample: [Work with multiple requests in transaction](https://code.msdn.microsoft.com/Work-with-execute-4388dac6).</span><span class="sxs-lookup"><span data-stu-id="d3c45-107">Download the sample: [Work with multiple requests in transaction](https://code.msdn.microsoft.com/Work-with-execute-4388dac6).</span></span>
  
 <span data-ttu-id="d3c45-108">This code sample applies to [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="d3c45-108">This code sample applies to [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="d3c45-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="d3c45-109">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="d3c45-110">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="d3c45-110">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="d3c45-111">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="d3c45-111">Demonstrates</span></span>  
 <span data-ttu-id="d3c45-112">This sample shows how to execute multiple organization message requests in a single database transaction by using a single web service method call, passing <xref:Microsoft.Xrm.Sdk.Messages.ExecuteTransactionRequest> as a parameter.</span><span class="sxs-lookup"><span data-stu-id="d3c45-112">This sample shows how to execute multiple organization message requests in a single database transaction by using a single web service method call, passing <xref:Microsoft.Xrm.Sdk.Messages.ExecuteTransactionRequest> as a parameter.</span></span> <span data-ttu-id="d3c45-113">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-execute-multiple-requests.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="d3c45-113">A snippet showing just the key sections of the sample is shown first, followed by the [complete sample code](sample-execute-multiple-requests.md#complete_sample).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d3c45-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="d3c45-114">Example</span></span>  
 <span data-ttu-id="d3c45-115">This sample uses a single web method call to execute all message requests in a collection as part of a single database transaction.</span><span class="sxs-lookup"><span data-stu-id="d3c45-115">This sample uses a single web method call to execute all message requests in a collection as part of a single database transaction.</span></span> <span data-ttu-id="d3c45-116">Settings to alter the execution behavior are also shown.</span><span class="sxs-lookup"><span data-stu-id="d3c45-116">Settings to alter the execution behavior are also shown.</span></span>  
  
 [!code-csharp[ExecuteTransaction#ExecuteTransaction1](../../snippets/csharp/CRMV8/executetransaction/cs/executetransaction1.cs#executetransaction1)]  
  
<a name="complete_sample"></a>   
## <a name="complete-sample-code"></a><span data-ttu-id="d3c45-117">Complete sample code</span><span class="sxs-lookup"><span data-stu-id="d3c45-117">Complete sample code</span></span>  
 [!code-csharp[ExecuteTransaction#ExecuteTransaction](../../snippets/csharp/CRMV8/executetransaction/cs/executetransaction.cs#executetransaction)]  
  
### <a name="see-also"></a><span data-ttu-id="d3c45-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d3c45-118">See also</span></span>  
 <span data-ttu-id="d3c45-119">[Execute messages in a single database transaction](use-messages-request-response-classes-execute-method.md#bkmk_transaction) </span><span class="sxs-lookup"><span data-stu-id="d3c45-119">[Execute messages in a single database transaction](use-messages-request-response-classes-execute-method.md#bkmk_transaction) </span></span>  
 [<span data-ttu-id="d3c45-120">Use the IOrganizationService Web Service to Read and Write Data or Metadata</span><span class="sxs-lookup"><span data-stu-id="d3c45-120">Use the IOrganizationService Web Service to Read and Write Data or Metadata</span></span>](use-organization-service-read-write-data-metadata.md)
