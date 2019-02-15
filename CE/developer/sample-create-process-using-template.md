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
# <a name="sample-create-a-process-using-a-template"></a>Sample: Create a process using a template

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps. Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 The following code example demonstrates how to create a workflow process using a template using the <xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest>.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Workflows#CreateProcessFromTemplate](../snippets/csharp/CRMV8/workflows/cs/createprocessfromtemplate.cs#createprocessfromtemplate)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Processes](sample-code-processes.md)   
 [Sample: Execute a Workflow](sample-run-workflow.md)   
 [Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md)   
 <xref:Microsoft.Crm.Sdk.Messages.CreateWorkflowFromTemplateRequest>
