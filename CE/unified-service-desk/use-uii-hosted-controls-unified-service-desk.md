---
title: Use UII hosted controls with Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn how to use UII hosted controls in Unified Service Desk.
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
ms.assetid: 7e889489-bf8c-48d0-9a44-2b8504dac8f1
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
ms.openlocfilehash: 88f79f1f244e8bae79e13a50b2f648366e6470bd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386269"
---
# <a name="use-uii-hosted-controls-with-unified-service-desk"></a><span data-ttu-id="cec65-103">Use UII hosted controls with Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="cec65-103">Use UII hosted controls with Unified Service Desk</span></span>
[!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] <span data-ttu-id="cec65-104">hosted controls are user controls that are derived from the [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol) class, and  implements the [IHostedApplication4](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.ihostedapplication4) interface, which provides most of the implementation code for a hosted control.</span><span class="sxs-lookup"><span data-stu-id="cec65-104">hosted controls are user controls that are derived from the [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol) class, and  implements the [IHostedApplication4](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.ihostedapplication4) interface, which provides most of the implementation code for a hosted control.</span></span> <span data-ttu-id="cec65-105">You can override the functions in the [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol) class, as required.</span><span class="sxs-lookup"><span data-stu-id="cec65-105">You can override the functions in the [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol) class, as required.</span></span>  
  
 [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] <span data-ttu-id="cec65-106">hosted controls can be used to create new or advanced user interface elements with complex business logic to interact with external applications from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="cec65-106">hosted controls can be used to create new or advanced user interface elements with complex business logic to interact with external applications from within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="cec65-107">You can either create a Windows Forms-based or a WPF-based [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, and host it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="cec65-107">You can either create a Windows Forms-based or a WPF-based [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, and host it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
 <span data-ttu-id="cec65-108">For more information about the properties, functions, and events available for a UII hosted control, see [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol).</span><span class="sxs-lookup"><span data-stu-id="cec65-108">For more information about the properties, functions, and events available for a UII hosted control, see [HostedControl](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedcontrol).</span></span>  
  
 <span data-ttu-id="cec65-109">The following walkthroughs demonstrate how to create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, and use it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="cec65-109">The following walkthroughs demonstrate how to create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control, and use it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
-   [<span data-ttu-id="cec65-110">Walkthrough: Create a UII Windows Forms Hosted Control</span><span class="sxs-lookup"><span data-stu-id="cec65-110">Walkthrough: Create a UII Windows Forms Hosted Control</span></span>](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)  
  
-   [<span data-ttu-id="cec65-111">Walkthrough: Create a UII WPF Hosted Control</span><span class="sxs-lookup"><span data-stu-id="cec65-111">Walkthrough: Create a UII WPF Hosted Control</span></span>](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md)  
  
### <a name="see-also"></a><span data-ttu-id="cec65-112">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="cec65-112">See also</span></span>  
 <span data-ttu-id="cec65-113">[UII Hosted Applications](../unified-service-desk/uii-hosted-applications.md) </span><span class="sxs-lookup"><span data-stu-id="cec65-113">[UII Hosted Applications](../unified-service-desk/uii-hosted-applications.md) </span></span>  
 [<span data-ttu-id="cec65-114">Create and manage UII hosted applications</span><span class="sxs-lookup"><span data-stu-id="cec65-114">Create and manage UII hosted applications</span></span>](../unified-service-desk/create-manage-uii-hosted-applications.md)
