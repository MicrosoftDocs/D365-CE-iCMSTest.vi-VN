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
# <a name="sample-assign-a-chart-to-another-user"></a><span data-ttu-id="cbf4c-102">Sample: Assign a chart to another user</span><span class="sxs-lookup"><span data-stu-id="cbf4c-102">Sample: Assign a chart to another user</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="cbf4c-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="cbf4c-103">This sample code is for [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="cbf4c-104">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span><span class="sxs-lookup"><span data-stu-id="cbf4c-104">Download the sample: [Work with visualizations and dashboards](https://code.msdn.microsoft.com/Samples-of-visualizations-027f7480).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cbf4c-105">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="cbf4c-105">Prerequisites</span></span>
[!INCLUDE[sdk-prerequisite](../../includes/sdk-prerequisite.md)]
  
## <a name="requirements"></a><span data-ttu-id="cbf4c-106">Yêu cầu</span><span class="sxs-lookup"><span data-stu-id="cbf4c-106">Requirements</span></span>  
[!INCLUDE[sdk_SeeConnectionHelper](../../includes/sdk-seeconnectionhelper.md)]
  
## <a name="demonstrates"></a><span data-ttu-id="cbf4c-107">Chứng tỏ</span><span class="sxs-lookup"><span data-stu-id="cbf4c-107">Demonstrates</span></span>  
 <span data-ttu-id="cbf4c-108">This sample shows how to assign a user-owned visualization to another user using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span><span class="sxs-lookup"><span data-stu-id="cbf4c-108">This sample shows how to assign a user-owned visualization to another user using the <xref:Microsoft.Crm.Sdk.Messages.AssignRequest> message.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cbf4c-109">Ví dụ</span><span class="sxs-lookup"><span data-stu-id="cbf4c-109">Example</span></span>  
 [!code-csharp[VisualizationsAndDashboards#AssignVisualizationToUser](../../snippets/csharp/CRMV8/visualizationsanddashboards/cs/assignvisualizationtouser.cs#assignvisualizationtouser)]  
  
### <a name="see-also"></a><span data-ttu-id="cbf4c-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cbf4c-110">See also</span></span>  
 <span data-ttu-id="cbf4c-111">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span><span class="sxs-lookup"><span data-stu-id="cbf4c-111">[Sample: CrmServiceHelper Class](../org-service/helper-code-serverconnection-class.md) </span></span>  
 <span data-ttu-id="cbf4c-112">[Working with Visualizations](view-data-with-visualizations-charts.md) </span><span class="sxs-lookup"><span data-stu-id="cbf4c-112">[Working with Visualizations](view-data-with-visualizations-charts.md) </span></span>  
 <span data-ttu-id="cbf4c-113">[Sample Code for Visualization](sample-code-charts-visualizations.md) </span><span class="sxs-lookup"><span data-stu-id="cbf4c-113">[Sample Code for Visualization](sample-code-charts-visualizations.md) </span></span>  
 <xref:Microsoft.Crm.Sdk.Messages.AssignRequest>
