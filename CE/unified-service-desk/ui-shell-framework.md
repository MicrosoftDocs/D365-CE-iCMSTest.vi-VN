---
title: UI Shell Framework in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about the UI shell framework that enables developers to build a desktop for hosting integrated applications.
ms.custom:
- dyn365-USD
ms.date: 08/23/2017
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
ms.assetid: f48c6efd-a067-406a-b271-24dc6462081a
caps.latest.revision: 6
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f979a0e5642082dcbc7cc3253239b011d2d85173
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387601"
---
# <a name="ui-shell-framework-in-unified-service-desk"></a><span data-ttu-id="c8de7-103">UI Shell Framework in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="c8de7-103">UI Shell Framework in Unified Service Desk</span></span>
<span data-ttu-id="c8de7-104">The UI Shell Framework is the part of [UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) that enables developers to build a desktop for hosting integrated applications.</span><span class="sxs-lookup"><span data-stu-id="c8de7-104">The UI Shell Framework is the part of [UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) that enables developers to build a desktop for hosting integrated applications.</span></span> <span data-ttu-id="c8de7-105">The UI Shell Framework has the following components:</span><span class="sxs-lookup"><span data-stu-id="c8de7-105">The UI Shell Framework has the following components:</span></span>  
  
- <span data-ttu-id="c8de7-106">**Desktop Core**: Contains core interfaces and classes that implement interfaces, exposed as APIs, which allow you to create a new [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] shell.</span><span class="sxs-lookup"><span data-stu-id="c8de7-106">**Desktop Core**: Contains core interfaces and classes that implement interfaces, exposed as APIs, which allow you to create a new [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] shell.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="c8de7-107">[Core](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core)</span><span class="sxs-lookup"><span data-stu-id="c8de7-107">[Core](https://docs.microsoft.com/dotnet/api/microsoft.uii.desktop.core)</span></span>  
  
- <span data-ttu-id="c8de7-108">**Session Manager**:  These classes are derived from Application Integration Framework sessions and [Sessions](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.sessions) classes.</span><span class="sxs-lookup"><span data-stu-id="c8de7-108">**Session Manager**:  These classes are derived from Application Integration Framework sessions and [Sessions](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.sessions) classes.</span></span>  
  
- <span data-ttu-id="c8de7-109">**UI Controls**: The UI Shell Framework contains controls such as the WPF panel, windows panel, and floating panel that allow you to create new shells quickly.</span><span class="sxs-lookup"><span data-stu-id="c8de7-109">**UI Controls**: The UI Shell Framework contains controls such as the WPF panel, windows panel, and floating panel that allow you to create new shells quickly.</span></span>  
  
- <span data-ttu-id="c8de7-110">**UI Core**: The Core class is the anchor class for all core functions.</span><span class="sxs-lookup"><span data-stu-id="c8de7-110">**UI Core**: The Core class is the anchor class for all core functions.</span></span> <span data-ttu-id="c8de7-111">It provides APIs for adding and removing sessions; managing notifications, the current view of applications, default operational behaviors for workflow management in relationship to current application views, access to service utility functions and methods; and loading and logging on to a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span><span class="sxs-lookup"><span data-stu-id="c8de7-111">It provides APIs for adding and removing sessions; managing notifications, the current view of applications, default operational behaviors for workflow management in relationship to current application views, access to service utility functions and methods; and loading and logging on to a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span></span> <span data-ttu-id="c8de7-112">This class provides override hooks to allow the developer to intercept, take action, and modify desktop behavior.</span><span class="sxs-lookup"><span data-stu-id="c8de7-112">This class provides override hooks to allow the developer to intercept, take action, and modify desktop behavior.</span></span>  
  
- <span data-ttu-id="c8de7-113">**CTI**: [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] computer telephony integration (CTI) framework contains core interfaces and classes that allow you to integrate CTI into a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span><span class="sxs-lookup"><span data-stu-id="c8de7-113">**CTI**: [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] computer telephony integration (CTI) framework contains core interfaces and classes that allow you to integrate CTI into a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Desktop (such as [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c8de7-114">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c8de7-114">See also</span></span>  
 <span data-ttu-id="c8de7-115">[UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) </span><span class="sxs-lookup"><span data-stu-id="c8de7-115">[UII Application Integration Framework](../unified-service-desk/uii-application-integration-framework.md) </span></span>  
 [<span data-ttu-id="c8de7-116">UII Computer Telephony Integration (CTI) framework</span><span class="sxs-lookup"><span data-stu-id="c8de7-116">UII Computer Telephony Integration (CTI) framework</span></span>](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
