---
title: 'Sample: Create, retrieve, update, and delete a chart (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: 'The sample shows how to create, retrieve, update, and delete an organization-owned visualization. '
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 51d4ecad-3c50-4f81-bfff-aa321d62cb2c
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 27
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: c4c4c94e09ac69b0466937b1e25478e4ac8e64d2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387730"
---
# <a name="sample-create-retrieve-update-and-delete-a-chart"></a>Sample: Create, retrieve, update, and delete a chart

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create, retrieve, update, and delete an organization-owned visualization. This sample uses the following common methods:  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[VisualizationsAndDashboards#CRUDVisualization](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/crudvisualization.cs#crudvisualization)]  
  
### <a name="see-also"></a>Xem thêm  
 [Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md)   
 [Actions on Chart](actions-visualizations-charts.md)   
 [Create a Chart](create-visualization-chart.md)   
 [Sample Code for Visualization](sample-code-charts-visualizations.md)   
 [Sample: Retrieve all Charts Attached to an Entity](sample-retrieve-all-charts-attached-entity.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>   
 <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest>
