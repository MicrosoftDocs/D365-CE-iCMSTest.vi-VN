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
# <a name="sample-assign-a-user-owned-dashboard-to-another-user"></a><span data-ttu-id="3854d-104">Sample: Assign a user-owned dashboard to another user</span><span class="sxs-lookup"><span data-stu-id="3854d-104">Sample: Assign a user-owned dashboard to another user</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="3854d-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="3854d-105">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="3854d-106">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span><span class="sxs-lookup"><span data-stu-id="3854d-106">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3854d-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3854d-107">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="3854d-108">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="3854d-108">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="3854d-109">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="3854d-109">Demonstrates</span></span>  
 <span data-ttu-id="3854d-110">This sample shows how to assign a user-owned dashboard to another user by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span><span class="sxs-lookup"><span data-stu-id="3854d-110">This sample shows how to assign a user-owned dashboard to another user by using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span></span> <span data-ttu-id="3854d-111">Because you can’t delete a user-owned dashboard that is assigned to another user, this sample shows how to use impersonation to delete the user-owned dashboard.</span><span class="sxs-lookup"><span data-stu-id="3854d-111">Because you can’t delete a user-owned dashboard that is assigned to another user, this sample shows how to use impersonation to delete the user-owned dashboard.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3854d-112">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="3854d-112">Example</span></span>  
 [!code-csharp[VisualizationsAndDashboards#AssignDashboardToUser](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/assigndashboardtouser.cs#assigndashboardtouser)]  
  
### <a name="see-also"></a><span data-ttu-id="3854d-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3854d-113">See also</span></span>  
 <span data-ttu-id="3854d-114">[Actions on Dashboard](actions-dashboards.md) </span><span class="sxs-lookup"><span data-stu-id="3854d-114">[Actions on Dashboard](actions-dashboards.md) </span></span>  
 <span data-ttu-id="3854d-115">[Gán](../introduction-entities.md#Assign) </span><span class="sxs-lookup"><span data-stu-id="3854d-115">[Assign](../introduction-entities.md#Assign) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>
