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
# <a name="sample-run-a-workflow"></a>Sample: Run a workflow

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with workflows](https://code.msdn.microsoft.com/Work-with-workflows-edf8f3bf).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 The following sample demonstrates how to programmatically execute a workflow by using the <xref:Microsoft.Crm.Sdk.Messages.ExecuteWorkflowRequest>.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Workflows#ExecuteWorkflow](../snippets/csharp/CRMV8/workflows/cs/executeworkflow.cs#executeworkflow)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample code for workflows](sample-code-processes.md)   
 [Sample: Create, Retrieve, Update, and Delete a Dialog](sample-create-retrieve-update-delete-dialog.md)   
 [Processes in Dynamics 365 for Customer Engagement apps(formerly Workflows)](automate-business-processes-customer-engagement.md)   
 <xref:Microsoft.Crm.Sdk.Messages.ExecuteWorkflowRequest>   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
