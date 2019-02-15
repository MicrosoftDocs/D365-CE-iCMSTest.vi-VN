---
title: 'Sample: Create a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample demonstrates how to write a custom workflow activity that can create an account and a task for the account. This sample uses early binding.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6d498e86-8702-43ed-bf76-96d1b4246dfd
caps.latest.revision: 26
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 447b9b12c72981d347437977ea669e9abce7b9dc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386239"
---
# <a name="sample-create-a-custom-workflow-activity"></a>Sample: Create a custom workflow activity

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the complete sample here [Custom workflow activities sample](https://code.msdn.microsoft.com/Custom-Workflow-Activities-eee57285). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to write a custom workflow activity that can create an account and a task for the account. This sample uses early binding.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[customworkflowactivities#simplesdkactivity](../../snippets/csharp/CRMV8/customworkflowactivities/cs/simplesdkactivity.cs#simplesdkactivity)]  
  
### <a name="see-also"></a>Xem thêm  
 [Custom Workflow Activities (Workflow Assemblies)](../custom-workflow-activities-workflow-assemblies.md)   
 [Sample: Update Next Birthday Using a Custom Workflow Activity](sample-update-next-birthday-using-custom-workflow-activity.md)   
 [Sample Code for Processes](../sample-code-processes.md)   
 [Creating a Custom Workflow Activity](create-custom-workflow-activity.md)   
 [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md)   
 [Using the IOrganization Web Service within a Custom Workflow Activity](use-iorganization-web-service-custom-workflow-activity.md)
