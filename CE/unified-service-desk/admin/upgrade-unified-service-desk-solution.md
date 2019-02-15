---
title: Upgrade a Unified Service Desk for Dynamics 365 for Customer Engagement apps solution | MicrosoftDocs
description: Learn how to upgrade Unified Service Desk for Dynamics 365 for Customer Engagement apps.
ms.custom:
- dyn365-USD, dyn365-admin
ms.date: 02/06/2018
ms.reviewer: ''
ms.service: dynamics-365-customerservice
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 46250912-52bc-45dc-914b-a77b32fc27c4
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: c17eb81b5c74b421af55db689f79e8227b412540
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382598"
---
# <a name="upgrading-the-solution"></a><span data-ttu-id="ec735-103">Upgrading the solution</span><span class="sxs-lookup"><span data-stu-id="ec735-103">Upgrading the solution</span></span>
<span data-ttu-id="ec735-104">You can upgrade a Unified Service Desk 1.x or [!INCLUDE[pn_unified_service_desk_20](../../includes/pn-unified-service-desk-20.md)] sample application package to [!INCLUDE[pn_unified_service_desk_3_2](../../includes/pn-unified-service-desk-3-2.md)] by importing the Upgrade sample application package.</span><span class="sxs-lookup"><span data-stu-id="ec735-104">You can upgrade a Unified Service Desk 1.x or [!INCLUDE[pn_unified_service_desk_20](../../includes/pn-unified-service-desk-20.md)] sample application package to [!INCLUDE[pn_unified_service_desk_3_2](../../includes/pn-unified-service-desk-3-2.md)] by importing the Upgrade sample application package.</span></span> <span data-ttu-id="ec735-105">The upgrade will not affect the configuration data associated with the existing solution.</span><span class="sxs-lookup"><span data-stu-id="ec735-105">The upgrade will not affect the configuration data associated with the existing solution.</span></span>  
  
## <a name="upgrade-procedure"></a><span data-ttu-id="ec735-106">Upgrade procedure</span><span class="sxs-lookup"><span data-stu-id="ec735-106">Upgrade procedure</span></span>  
 <span data-ttu-id="ec735-107">To upgrade a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution, follow these steps.</span><span class="sxs-lookup"><span data-stu-id="ec735-107">To upgrade a [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution, follow these steps.</span></span>  
  
1. <span data-ttu-id="ec735-108">[Download](http://go.microsoft.com/fwlink/p/?LinkID=867343) the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application packages and [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)] tool.</span><span class="sxs-lookup"><span data-stu-id="ec735-108">[Download](http://go.microsoft.com/fwlink/p/?LinkID=867343) the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] sample application packages and [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)] tool.</span></span>  
  
2. <span data-ttu-id="ec735-109">Start [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)], that will be used  to import the Upgrade sample application package.</span><span class="sxs-lookup"><span data-stu-id="ec735-109">Start [!INCLUDE[pn_package_deployer_long](../../includes/pn-package-deployer-long.md)], that will be used  to import the Upgrade sample application package.</span></span> <span data-ttu-id="ec735-110">Alternatively, you can use [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] commands.</span><span class="sxs-lookup"><span data-stu-id="ec735-110">Alternatively, you can use [!INCLUDE[pn_PowerShell](../../includes/pn-powershell.md)] commands.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="ec735-111">[Import-CrmPackage](https://technet.microsoft.com/library/dn756301.aspx)</span><span class="sxs-lookup"><span data-stu-id="ec735-111">[Import-CrmPackage](https://technet.microsoft.com/library/dn756301.aspx)</span></span>  
  
3. <span data-ttu-id="ec735-112">In the Package Deployer window, click **Continue**.</span><span class="sxs-lookup"><span data-stu-id="ec735-112">In the Package Deployer window, click **Continue**.</span></span>  
  
4. <span data-ttu-id="ec735-113">On the Connect to Microsoft Dynamics 365 for Customer Engagement apps page, connect to the organization that you want to upgrade the current [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution.</span><span class="sxs-lookup"><span data-stu-id="ec735-113">On the Connect to Microsoft Dynamics 365 for Customer Engagement apps page, connect to the organization that you want to upgrade the current [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] solution.</span></span>  
  
5. <span data-ttu-id="ec735-114">Under Select the import package to use, click **Unified Service Desk – Upgrade**, and then click **Next**.</span><span class="sxs-lookup"><span data-stu-id="ec735-114">Under Select the import package to use, click **Unified Service Desk – Upgrade**, and then click **Next**.</span></span>  
  
   <span data-ttu-id="ec735-115">![Select the import package](../../unified-service-desk/media/usd-select-package.png "Select the import package")</span><span class="sxs-lookup"><span data-stu-id="ec735-115">![Select the import package](../../unified-service-desk/media/usd-select-package.png "Select the import package")</span></span>  
  
6. <span data-ttu-id="ec735-116">The Welcome to the Unified Service Desk – Upgrade Setup Tool page appears.</span><span class="sxs-lookup"><span data-stu-id="ec735-116">The Welcome to the Unified Service Desk – Upgrade Setup Tool page appears.</span></span> <span data-ttu-id="ec735-117">Review the information about the components that will be upgraded, and then click **Next**.</span><span class="sxs-lookup"><span data-stu-id="ec735-117">Review the information about the components that will be upgraded, and then click **Next**.</span></span>  
  
   <span data-ttu-id="ec735-118">![Unified Service Desk upgrade details](../../unified-service-desk/media/usd-upgrade-details.png "Unified Service Desk upgrade details")</span><span class="sxs-lookup"><span data-stu-id="ec735-118">![Unified Service Desk upgrade details](../../unified-service-desk/media/usd-upgrade-details.png "Unified Service Desk upgrade details")</span></span>  
  
7. <span data-ttu-id="ec735-119">On the Ready to Install page, click **Next** to verify the components to upgrade.</span><span class="sxs-lookup"><span data-stu-id="ec735-119">On the Ready to Install page, click **Next** to verify the components to upgrade.</span></span>  
  
8. <span data-ttu-id="ec735-120">On the Reading Unified Service Desk – Upgrade Installer Configuration page, information about what will be upgraded is listed.</span><span class="sxs-lookup"><span data-stu-id="ec735-120">On the Reading Unified Service Desk – Upgrade Installer Configuration page, information about what will be upgraded is listed.</span></span> <span data-ttu-id="ec735-121">Click **Next** to begin the upgrade.</span><span class="sxs-lookup"><span data-stu-id="ec735-121">Click **Next** to begin the upgrade.</span></span>  
  
   <span data-ttu-id="ec735-122">![Upgrade in progress](../../unified-service-desk/media/usd-upgrade-progress.png "Upgrade in progress")</span><span class="sxs-lookup"><span data-stu-id="ec735-122">![Upgrade in progress](../../unified-service-desk/media/usd-upgrade-progress.png "Upgrade in progress")</span></span>  
  
9. <span data-ttu-id="ec735-123">The Executing Install Actions page appears.</span><span class="sxs-lookup"><span data-stu-id="ec735-123">The Executing Install Actions page appears.</span></span> <span data-ttu-id="ec735-124">Updating one or more solutions can take several minutes.</span><span class="sxs-lookup"><span data-stu-id="ec735-124">Updating one or more solutions can take several minutes.</span></span>  
  
10. <span data-ttu-id="ec735-125">The upgrade complete page appears.</span><span class="sxs-lookup"><span data-stu-id="ec735-125">The upgrade complete page appears.</span></span> <span data-ttu-id="ec735-126">Click **Finish** to complete the upgrade.</span><span class="sxs-lookup"><span data-stu-id="ec735-126">Click **Finish** to complete the upgrade.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec735-127">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="ec735-127">See also</span></span>  
 [<span data-ttu-id="ec735-128">Install, upgrade, and deploy Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ec735-128">Install, upgrade, and deploy Unified Service Desk</span></span>](../../unified-service-desk/admin/install-upgrade-deploy-unified-service-desk.md)
