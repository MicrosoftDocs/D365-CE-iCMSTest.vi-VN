---
title: 'Sample: Create, retrieve, update, and delete an email attachment (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This sample shows how to create, retrieve, update, and delete email attachments using methods such as IOrganizationService.Entity, IOrganizationService.ColumnSet, IOrganizationService.Entity, IOrganizationService.Guid
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
- sample for creating; retrieving; updating; and deleting email attachments, activity entities
- activity entities samples, creating; retrieving; updating; and deleting email attachments
ms.assetid: 918c0b7e-2850-40c5-8333-5dad6d83b850
caps.latest.revision: 22
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: ec1b862cafb6d003b875ae5774f68369e08b631e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386735"
---
# <a name="sample-create-retrieve-update-and-delete-an-email-attachment"></a>Sample: Create, retrieve, update, and delete an email attachment

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)]. Download the complete sample from [Sample: Work with Activity entities](https://code.msdn.microsoft.com/Activities-Samples-61bf7504).   

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create, retrieve, update, and delete email attachments using the following methods:  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Activities#CRUDEmailAttachments](../snippets/csharp/CRMV8/activities/cs/crudemailattachments.cs#crudemailattachments)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample Code for Activity Entities](sample-code-activity-entities.md)   
 [EMail Activity Entities](email-activity-entities.md)   
 [Sample: Retrieve Email Attachments for an Email Template](sample-retrieve-email-attachments-email-template.md)   
 [ActivityMimeAttachment Entity](entities/activitymimeattachment.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>
