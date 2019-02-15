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
# <a name="sample-create-retrieve-update-and-delete-a-dashboard"></a><span data-ttu-id="2bee8-104">Sample: Create, retrieve, update, and delete a dashboard</span><span class="sxs-lookup"><span data-stu-id="2bee8-104">Sample: Create, retrieve, update, and delete a dashboard</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="2bee8-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="2bee8-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="2bee8-106">Download the sample: [Work visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span><span class="sxs-lookup"><span data-stu-id="2bee8-106">Download the sample: [Work visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2bee8-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2bee8-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="2bee8-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="2bee8-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="2bee8-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="2bee8-109">Demonstrates</span></span>  
 <span data-ttu-id="2bee8-110">This sample shows how to create, retrieve, update, and delete an organization-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="2bee8-110">This sample shows how to create, retrieve, update, and delete an organization-owned dashboard.</span></span> <span data-ttu-id="2bee8-111">As part of updating the dashboard, it’s set to be the default dashboard for the organization.</span><span class="sxs-lookup"><span data-stu-id="2bee8-111">As part of updating the dashboard, it’s set to be the default dashboard for the organization.</span></span> <span data-ttu-id="2bee8-112">This sample uses the following common methods:</span><span class="sxs-lookup"><span data-stu-id="2bee8-112">This sample uses the following common methods:</span></span>  
  
-   <span data-ttu-id="2bee8-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span><span class="sxs-lookup"><span data-stu-id="2bee8-113"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Create*></span></span>  
  
-   <span data-ttu-id="2bee8-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span><span class="sxs-lookup"><span data-stu-id="2bee8-114"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Retrieve*></span></span>  
  
-   <span data-ttu-id="2bee8-115"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span><span class="sxs-lookup"><span data-stu-id="2bee8-115"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Update*></span></span>  
  
-   <span data-ttu-id="2bee8-116"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span><span class="sxs-lookup"><span data-stu-id="2bee8-116"><xref:Microsoft.Xrm.Sdk.IOrganizationService>.<xref:Microsoft.Xrm.Sdk.IOrganizationService.Delete*></span></span>  
  
## <a name="example"></a><span data-ttu-id="2bee8-117">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="2bee8-117">Example</span></span>  
 [!code-csharp[VisualizationsAndDashboards#CRUDDashboards](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/cruddashboards.cs#cruddashboards)]  
  
### <a name="see-also"></a><span data-ttu-id="2bee8-118">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2bee8-118">See also</span></span>  
 <span data-ttu-id="2bee8-119">[Analyze Data with Dashboards](analyze-data-with-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="2bee8-119">[Analyze Data with Dashboards](analyze-data-with-dashboards.md) </span></span>  
 <span data-ttu-id="2bee8-120">[Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md) </span><span class="sxs-lookup"><span data-stu-id="2bee8-120">[Sample: Assign a User-Owned Dashboard to Another User](sample-assign-user-owned-dashboard-another-user.md) </span></span>  
 <span data-ttu-id="2bee8-121">[Actions on Dashboard](actions-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="2bee8-121">[Actions on Dashboard](actions-dashboards.md) </span></span>  
<xref:Microsoft.Xrm.Sdk.IOrganizationService>   
 [<span data-ttu-id="2bee8-122">Sample: CrmServiceHelper Class</span><span class="sxs-lookup"><span data-stu-id="2bee8-122">Sample: CrmServiceHelper Class</span></span>](../org-service/helper-code-serverconnection-class.md)
