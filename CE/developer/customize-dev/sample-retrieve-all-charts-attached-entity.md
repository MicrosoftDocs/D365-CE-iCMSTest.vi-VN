---
title: 'Sample: Retrieve all charts attached to an entity (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to retrieve all the organization-owned visualizations attached to an entity by using the IOrganizationService.QueryBase) method. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 4ee28c9c-4d78-47b1-911b-782527bcda45
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 28
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 49763c2befe2a8105013c9c173214fbd8aa20cba
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388637"
---
# <a name="sample-retrieve-all-charts-attached-to-an-entity"></a>Sample: Retrieve all charts attached to an entity

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to retrieve all the organization-owned visualizations attached to an entity by using the <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*> method.  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[VisualizationsAndDashboards#RetrieveVisualizationsAttachedToAnEntity](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/retrievevisualizationsattachedtoanentity.cs#retrievevisualizationsattachedtoanentity)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md)   
 [Working with Visualizations](view-data-with-visualizations-charts.md)   
 [Sample Code for Visualization](sample-code-charts-visualizations.md)   
 [Sample: Assign a Chart to Another User](sample-assign-chart-another-user.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.RetrieveMultiple*>
