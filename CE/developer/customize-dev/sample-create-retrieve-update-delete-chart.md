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
# <a name="sample-create-retrieve-update-and-delete-a-chart"></a><span data-ttu-id="4f20c-103">Sample: Create, retrieve, update, and delete a chart</span><span class="sxs-lookup"><span data-stu-id="4f20c-103">Sample: Create, retrieve, update, and delete a chart</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4f20c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="4f20c-104">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="4f20c-105">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span><span class="sxs-lookup"><span data-stu-id="4f20c-105">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4f20c-106">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="4f20c-106">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="4f20c-107">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="4f20c-107">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="4f20c-108">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="4f20c-108">Demonstrates</span></span>  
 <span data-ttu-id="4f20c-109">This sample shows how to create, retrieve, update, and delete an organization-owned visualization.</span><span class="sxs-lookup"><span data-stu-id="4f20c-109">This sample shows how to create, retrieve, update, and delete an organization-owned visualization.</span></span> <span data-ttu-id="4f20c-110">This sample uses the following common methods:</span><span class="sxs-lookup"><span data-stu-id="4f20c-110">This sample uses the following common methods:</span></span>  
  
-   <span data-ttu-id="4f20c-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="4f20c-111"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span>  
  
-   <span data-ttu-id="4f20c-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="4f20c-112"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span>  
  
-   <span data-ttu-id="4f20c-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="4f20c-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span>  
  
-   <span data-ttu-id="4f20c-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="4f20c-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span>  
  
## <a name="example"></a><span data-ttu-id="4f20c-115">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="4f20c-115">Example</span></span>  
 [!code-csharp[VisualizationsAndDashboards#CRUDVisualization](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/crudvisualization.cs#crudvisualization)]  
  
### <a name="see-also"></a><span data-ttu-id="4f20c-116">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4f20c-116">See also</span></span>  
 <span data-ttu-id="4f20c-117">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="4f20c-117">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="4f20c-118">[Actions on Chart](actions-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="4f20c-118">[Actions on Chart](actions-visualizations-charts.md) </span></span>  
 <span data-ttu-id="4f20c-119">[Create a Chart](create-visualization-chart.md) </span><span class="sxs-lookup"><span data-stu-id="4f20c-119">[Create a Chart](create-visualization-chart.md) </span></span>  
 <span data-ttu-id="4f20c-120">[Sample Code for Visualization](sample-code-charts-visualizations.md) </span><span class="sxs-lookup"><span data-stu-id="4f20c-120">[Sample Code for Visualization](sample-code-charts-visualizations.md) </span></span>  
 <span data-ttu-id="4f20c-121">[Sample: Retrieve all Charts Attached to an Entity](sample-retrieve-all-charts-attached-entity.md) </span><span class="sxs-lookup"><span data-stu-id="4f20c-121">[Sample: Retrieve all Charts Attached to an Entity](sample-retrieve-all-charts-attached-entity.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*>   
 <xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*>   
 <xref:Microsoft.Crm.Sdk.Messages.PublishAllXmlRequest>
