---
title: Stop and start the asynchronous service (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs
description: Learn about stopping and starting the asynchronous service by using the Services administrative tool. The service should be stopped before a plug-in assembly that contains asynchronous plug-ins is deleted.
ms.custom: ''
ms.date: 10/31/2017
ms.prod: crm-2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (on-premises)
ms.assetid: f3492a19-2a93-4477-853f-ee6bd3ea750d
caps.latest.revision: 15
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: e5619d25aa78c64e584398107e67435507954e67
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386876"
---
# <a name="stop-and-start-the-asynchronous-service"></a><span data-ttu-id="e45fe-104">Stop and start the asynchronous service</span><span class="sxs-lookup"><span data-stu-id="e45fe-104">Stop and start the asynchronous service</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

[!INCLUDE[cc_sdk_onpremises_note](../includes/cc-sdk-onpremises-note.md)] 

<span data-ttu-id="e45fe-105">For [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement on-premises (including IFD) deployments, the asynchronous service can be stopped and restarted by using the Services administrative tool.</span><span class="sxs-lookup"><span data-stu-id="e45fe-105">For [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Customer Engagement on-premises (including IFD) deployments, the asynchronous service can be stopped and restarted by using the Services administrative tool.</span></span> <span data-ttu-id="e45fe-106">The service should be stopped before a plug-in assembly that contains asynchronous plug-ins is deleted.</span><span class="sxs-lookup"><span data-stu-id="e45fe-106">The service should be stopped before a plug-in assembly that contains asynchronous plug-ins is deleted.</span></span>  
  
### <a name="stop-and-restart-the-service"></a><span data-ttu-id="e45fe-107">Stop and restart the service</span><span class="sxs-lookup"><span data-stu-id="e45fe-107">Stop and restart the service</span></span>  
  
1. <span data-ttu-id="e45fe-108">Navigate to **Start**, select **Administrative Tools**, then click **Services**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-108">Navigate to **Start**, select **Administrative Tools**, then click **Services**.</span></span>  
  
2. <span data-ttu-id="e45fe-109">Right-click **Dynamics 365 for Customer Engagement Asynchronous Processing Service** in the **Name** column of the service listing.</span><span class="sxs-lookup"><span data-stu-id="e45fe-109">Right-click **Dynamics 365 for Customer Engagement Asynchronous Processing Service** in the **Name** column of the service listing.</span></span>  
  
3. <span data-ttu-id="e45fe-110">Click **Start** or **Stop**.</span><span class="sxs-lookup"><span data-stu-id="e45fe-110">Click **Start** or **Stop**.</span></span> <span data-ttu-id="e45fe-111">Or, you can click **Properties** in the shortcut menu and then click **Start** or **Stop** in the dialog box.</span><span class="sxs-lookup"><span data-stu-id="e45fe-111">Or, you can click **Properties** in the shortcut menu and then click **Start** or **Stop** in the dialog box.</span></span>  
  
   <span data-ttu-id="e45fe-112">You must have System Administrator privileges to stop or start the service.</span><span class="sxs-lookup"><span data-stu-id="e45fe-112">You must have System Administrator privileges to stop or start the service.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e45fe-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="e45fe-113">See also</span></span>  
 [<span data-ttu-id="e45fe-114">Asynchronous Service in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="e45fe-114">Asynchronous Service in Dynamics 365 for Customer Engagement apps</span></span>](asynchronous-service.md)
