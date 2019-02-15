---
title: 'Sample: Assign a chart to another user | MicrosoftDocs'
description: ''
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 0225d979-0e34-44b5-814c-a5dcb14d6fd9
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 24
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: fc7f8fc7937d8c718fcebe14c51161b420c12bce
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386441"
---
# <a name="sample-assign-a-chart-to-another-user"></a>Sample: Assign a chart to another user

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480). 

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to assign a user-owned visualization to another user using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[VisualizationsAndDashboards#AssignVisualizationToUser](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/assignvisualizationtouser.cs#assignvisualizationtouser)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md)   
 [Working with Visualizations](view-data-with-visualizations-charts.md)   
 [Sample Code for Visualization](sample-code-charts-visualizations.md)   
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>
