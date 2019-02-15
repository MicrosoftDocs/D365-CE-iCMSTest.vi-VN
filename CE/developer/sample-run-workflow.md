---
title: 'Sample: Run a workflow (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: This sample demonstrates how to programmatically execute a workflow by using the ExecuteWorkflowRequest
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c32a634c-3e01-42cd-b3ed-d1a89586b1cc
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 89d3a0610f2213860cf4f82ebe7dc03d92b2961d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385627"
---
# <a name="sample-run-a-workflow"></a><span data-ttu-id="3982c-103">Sample: Run a workflow</span><span class="sxs-lookup"><span data-stu-id="3982c-103">Sample: Run a workflow</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3982c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3982c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="3982c-105">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span><span class="sxs-lookup"><span data-stu-id="3982c-105">Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3982c-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3982c-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="3982c-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3982c-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="3982c-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3982c-108">Demonstrates</span></span>  
 <span data-ttu-id="3982c-109">The following sample demonstrates how to programmatically execute a workflow by using the <xref:Microsoft.Crm.Sdk.Messages.ExecuteWorkflowRequest>.</span><span class="sxs-lookup"><span data-stu-id="3982c-109">The following sample demonstrates how to programmatically execute a workflow by using the <xref:Microsoft.Crm.Sdk.Messages.ExecuteWorkflowRequest>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3982c-110">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3982c-110">Example</span></span>  
 [!code-csharp[Workflows#ExecuteWorkflow](../snippets/csharp/CRMV8/workflows/cs/executeworkflow.cs#executeworkflow)]  
  
### <a name="see-also"></a><span data-ttu-id="3982c-111">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3982c-111">See also</span></span>  
 <span data-ttu-id="3982c-112">[Sample code for workflows](sample-code-processes.md) </span><span class="sxs-lookup"><span data-stu-id="3982c-112">[Sample code for workflows](sample-code-processes.md) </span></span>  
 <span data-ttu-id="3982c-113">[Sample: Create, Retrieve, Update, and Delete a Dialog](sample-create-retrieve-update-delete-dialog.md) </span><span class="sxs-lookup"><span data-stu-id="3982c-113">[Sample: Create, Retrieve, Update, and Delete a Dialog](sample-create-retrieve-update-delete-dialog.md) </span></span>  
 <span data-ttu-id="3982c-114">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span><span class="sxs-lookup"><span data-stu-id="3982c-114">[Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.ExecuteWorkflowRequest>   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
