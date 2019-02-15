---
title: 'Sample: Send an email (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to send an email SendEmailRequest message
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
helpviewer_keywords:
- sample for sending email messages, activity entities
- activity entities samples, sending email messages
ms.assetid: c95bec08-bdd2-420a-93aa-ee7c0f20fa16
caps.latest.revision: 18
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 46697a16c5f8b9798191a297f1c900223320a8d7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388342"
---
# <a name="sample-send-an-email"></a>Sample: Send an email

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
    
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to send an email <xref:Microsoft.Crm.Sdk.Messages.SendEmailRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Activities#SendEmail](../snippets/csharp/CRMV8/activities/cs/sendemail.cs#sendemail)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Activity](sample-code-activity-entities.md)   
 [Sample: Create an Email Using a Template](sample-create-email-template.md)   
 [E-mail Activity Entities](email-activity-entities.md)   
 [Email Entity](entities/email.md)   
 [Sample: CrmServiceHelper Class](org-service/helper-code-serverconnection-class.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SendEmailRequest>
