---
title: 'Sample: Set the state of a workflow (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The sample shows how to change the state of a workflow, through activating and deactivating it, by using the SetStateRequest message. In addition, the sample shows how to create a custom XAML workflow. A snippet showing just the key sections of the sample is shown first, followed by the Complete Sample Code. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 68a5e1da-7432-4520-a9df-72372ddb8a20
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 21
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ff5b43d52543001e0ebb49864cece4ea37df69f9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388248"
---
# <a name="sample-set-the-state-of-a-workflow"></a><span data-ttu-id="2c378-105">Sample: Set the state of a workflow</span><span class="sxs-lookup"><span data-stu-id="2c378-105">Sample: Set the state of a workflow</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2c378-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="2c378-106">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="2c378-107">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span><span class="sxs-lookup"><span data-stu-id="2c378-107">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c378-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2c378-108">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="2c378-109">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="2c378-109">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="2c378-110">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="2c378-110">Demonstrates</span></span>  
 <span data-ttu-id="2c378-111">This sample shows how to change the state of a workflow, through activating and deactivating it, by using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span><span class="sxs-lookup"><span data-stu-id="2c378-111">This sample shows how to change the state of a workflow, through activating and deactivating it, by using the <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest> message.</span></span> <span data-ttu-id="2c378-112">In addition, the sample shows how to create a custom XAML workflow.</span><span class="sxs-lookup"><span data-stu-id="2c378-112">In addition, the sample shows how to create a custom XAML workflow.</span></span> <span data-ttu-id="2c378-113">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-set-state-workflow.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="2c378-113">A snippet showing just the key sections of the sample is shown first, followed by the [Complete Sample Code](sample-set-state-workflow.md#complete_sample).</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c378-114">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2c378-114">Example</span></span>  
 <span data-ttu-id="2c378-115">Code snippet that shows how to activate and deactivate a workflow.</span><span class="sxs-lookup"><span data-stu-id="2c378-115">Code snippet that shows how to activate and deactivate a workflow.</span></span>  
  
 [!code-csharp[Workflows#SetStateWorkflow1](../snippets/csharp/CRMV8/workflows/cs/setstateworkflow1.cs#setstateworkflow1)]  
[!code-csharp[Workflows#SetStateWorkflow2](../snippets/csharp/CRMV8/workflows/cs/setstateworkflow2.cs#setstateworkflow2)]  
  
## <a name="example"></a><span data-ttu-id="2c378-116">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2c378-116">Example</span></span>  
 <span data-ttu-id="2c378-117">Code snippet that shows how to create a XAML workflow.</span><span class="sxs-lookup"><span data-stu-id="2c378-117">Code snippet that shows how to create a XAML workflow.</span></span>  
  
 [!code-csharp[Workflows#SetStateWorkflow3](../snippets/csharp/CRMV8/workflows/cs/setstateworkflow3.cs#setstateworkflow3)]  
  
 <span data-ttu-id="2c378-118">For the XAML code that defines the workflow, see the [Complete Sample Code](sample-set-state-workflow.md#complete_sample).</span><span class="sxs-lookup"><span data-stu-id="2c378-118">For the XAML code that defines the workflow, see the [Complete Sample Code](sample-set-state-workflow.md#complete_sample).</span></span>  
  
<a name="complete_sample"></a>   
## <a name="complete-sample-code"></a><span data-ttu-id="2c378-119">Complete Sample Code</span><span class="sxs-lookup"><span data-stu-id="2c378-119">Complete Sample Code</span></span>  
 [!code-csharp[Workflows#SetStateWorkflow](../snippets/csharp/CRMV8/workflows/cs/setstateworkflow.cs#setstateworkflow)]  
  
### <a name="see-also"></a><span data-ttu-id="2c378-120">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2c378-120">See also</span></span>  
 <span data-ttu-id="2c378-121">[Sample code for workflows](sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="2c378-121">[Sample code for workflows](sample-code-processes.md) </span></span>  
 <span data-ttu-id="2c378-122">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md)    </span><span class="sxs-lookup"><span data-stu-id="2c378-122">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md)    </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
