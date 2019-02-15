---
title: 'Sample: Create an email using a template (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to instantiate an email record by using the InstantiateTemplateRequest message
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4a17a1b0-c111-4575-ae70-802b79a2c6ae
caps.latest.revision: 17
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: a5aaff7f540ce8b3e0bea8934d2e3d9a907eb9a5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388253"
---
# <a name="sample-create-an-email-using-a-template"></a>Sample: Create an email using a template

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Templates](https://code.msdn.microsoft.com/Templates-Samples-1759ff39).  
  
## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to instantiate an email record by using the <xref:Microsoft.Crm.Sdk.Messages.InstantiateTemplateRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Templates#CreateEmailUsingTemplate](../snippets/csharp/CRMV8/templates/cs/createemailusingtemplate.cs#createemailusingtemplate)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Activity](sample-code-activity-entities.md)   
 [EMail Activity Entities](email-activity-entities.md)   
 [Email Entity](entities/email.md)   
 [Template Entity](entities/template.md)   
 [Sample: Work with Activity Party Records](sample-work-activity-party-records.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.InstantiateTemplateRequest>
