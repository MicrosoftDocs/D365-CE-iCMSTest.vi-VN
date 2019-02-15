---
title: 'Sample: Create, retrieve, update, and delete a dashboard (Developer Guide for Dynamics 365 for Customer Engagement) | MicrosoftDocs'
description: The sample shows how to create, retrieve, update, and delete an organization-owned dashboard. As part of updating the dashboard, it’s set to be the default dashboard for the organization.
keywords: ''
ms.date: 10/31/2017
ms.service: crm-online
ms.custom: ''
ms.topic: samples
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: eac23f38-e682-40b8-aa6a-b8145ebf7764
author: JimDaly
ms.author: jdaly
manager: jdaly
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
caps.latest.revision: 25
topic-status: Drafting
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 7ddf85ee8ed5f32c19c7b3c52525c92427d67a67
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387705"
---
# <a name="sample-create-retrieve-update-and-delete-a-dashboard"></a>Sample: Create, retrieve, update, and delete a dashboard

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement. Download the sample: [Work visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).

## <a name="prerequisites"></a>Điều kiện tiên quyết
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a>Yêu cầu  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a>Chứng tỏ  
 This sample shows how to create, retrieve, update, and delete an organization-owned dashboard. As part of updating the dashboard, it’s set to be the default dashboard for the organization. This sample uses the following common methods:  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>  
  
-   <xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*>  
  
## <a name="example"></a>Ví dụ  
 [!code-csharp[VisualizationsAndDashboards#CRUDDashboards](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/cruddashboards.cs#cruddashboards)]  
  
### <a name="see-also"></a>Xem thêm  
 [Analyze Data with Dashboards](analyze-data-with-dashboards.md)   
 [Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md)   
 [Actions on Dashboard](actions-dashboards.md)   
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md)
