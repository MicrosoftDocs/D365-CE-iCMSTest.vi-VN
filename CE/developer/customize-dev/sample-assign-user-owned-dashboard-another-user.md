---
title: 'Sample: Assign a user-owned dashboard to another user (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to assign a user-owned dashboard to another user by using the AssignRequest message. Because you can’t delete a user-owned dashboard that is assigned to another user, this sample shows how to use impersonation to delete the user-owned dashboard. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 3c88b87d-e178-41ac-bd44-f7aa790677b9
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 22
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c73bc290a3c4000a782414d18da03a55771d75e7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388606"
---
# <a name="sample-assign-a-user-owned-dashboard-to-another-user"></a>Sample: Assign a user-owned dashboard to another user

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to assign a user-owned dashboard to another user by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message. Because you can’t delete a user-owned dashboard that is assigned to another user, this sample shows how to use impersonation to delete the user-owned dashboard.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[VisualizationsAndDashboards#AssignDashboardToUser](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/assigndashboardtouser.cs#assigndashboardtouser)]  
  
### <a name="see-also"></a>Xem thêm  
 [Actions on Dashboard](actions-dashboards.md)   
 [Gán](../introduction-entities.md#Assign)   
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>
