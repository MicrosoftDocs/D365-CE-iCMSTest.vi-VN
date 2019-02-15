---
title: 'Sample: Convert a fax to a task (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs'
description: This sample shows how to create a task for a fax by using the IOrganizationService.Entity) method
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f82fe3eb-1867-4edb-869d-58081f38d653
caps.latest.revision: 23
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 647961b1c8d8ed9664d72768a5266759451870d8
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388635"
---
# <a name="sample-convert-a-fax-to-a-task"></a>Sample: Convert a fax to a task

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504). 
  
## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]

## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create a task for a fax by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*> method.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Activities#ConvertFaxToTask](../snippets/csharp/CRMV8/activities/cs/convertfaxtotask.cs#convertfaxtotask)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Activity](sample-code-activity-entities.md)   
 [Fax Entity](entities/fax.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [Sample: Promote an Email Message to Dynamics 365 for Customer Engagement apps](sample-promote-email-message.md)
