---
title: 'Sample: Create, retrieve, update, and delete a dialog (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: The sample shows how to create, retrieve, update, and delete a dialog process using the methods IOrganizationService.Entity, IOrganizationService.ColumnSet, and IOrganizationService. Guid.
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 6bebfba9-833f-4e46-88e4-d1b5fa6b5962
caps.latest.revision: 25
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c68880016f2e8221fde04aa4eaddf1d52913ba8e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386044"
---
# <a name="sample-create-retrieve-update-and-delete-a-dialog"></a>Sample: Create, retrieve, update, and delete a dialog

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] for Customer Engagement apps. See the complete sample here [Sample: Create, retrieve, update, and delete a dialog](https://msdn.microsoft.com/en-us/library/gg334435.aspx)

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create, retrieve, update, and delete a dialog process using these methods:  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>  
  
-  <xref:Microsoft.Xrm.Sdk.IOrganizationService>. <xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[Dialogs#CRUDDialog](../snippets/csharp/CRMV8/dialogs/cs/cruddialog.cs#cruddialog)]  
  
### <a name="see-also"></a>Xem thêm  
 [Use Dialogs in Dynamics 365 for Customer Engagement apps](use-dialogs-guided-processes.md)   
 [Sample: Create a Workflow in Code](sample-create-workflow-code.md)   
 [Sample Code for Processes](sample-code-processes.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Crm.Sdk.Messages.SetStateRequest>
