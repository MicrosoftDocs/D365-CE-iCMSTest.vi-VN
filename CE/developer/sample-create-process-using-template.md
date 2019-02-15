---
title: 'Sample: Create a process using a template (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: This sample demonstrates how to create a workflow process using a template using the CreateWorkflowFromTemplateRequest
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 5c7f045f-7b57-4e44-a99c-becefe533035
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 027ca4d171594ec7f329a6367e04b5e249a5c96b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387165"
---
# <a name="sample-create-a-process-using-a-template"></a><span data-ttu-id="7b9e2-103">Sample: Create a process using a template</span><span class="sxs-lookup"><span data-stu-id="7b9e2-103">Sample: Create a process using a template</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="7b9e2-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps.</span></span> <span data-ttu-id="7b9e2-105">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span><span class="sxs-lookup"><span data-stu-id="7b9e2-105">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7b9e2-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="7b9e2-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="7b9e2-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="7b9e2-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="7b9e2-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="7b9e2-108">Demonstrates</span></span>  
 <span data-ttu-id="7b9e2-109">The following code example demonstrates how to create a workflow process using a template using the <xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest>.</span><span class="sxs-lookup"><span data-stu-id="7b9e2-109">The following code example demonstrates how to create a workflow process using a template using the <xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7b9e2-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="7b9e2-110">Example</span></span>  
 [!code-csharp[Workflows#CreateProcessFromTemplate](../snippets/csharp/CRMV8/workflows/cs/createprocessfromtemplate.cs#createprocessfromtemplate)]  
  
### <a name="see-also"></a><span data-ttu-id="7b9e2-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="7b9e2-111">See also</span></span>  
 <span data-ttu-id="7b9e2-112">[Sample Code for Processes](sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="7b9e2-112">[Sample Code for Processes](sample-code-processes.md) </span></span>  
 <span data-ttu-id="7b9e2-113">[Sample: Execute a Workflow](sample-run-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="7b9e2-113">[Sample: Execute a Workflow](sample-run-workflow.md) </span></span>  
 <span data-ttu-id="7b9e2-114">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="7b9e2-114">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest>
