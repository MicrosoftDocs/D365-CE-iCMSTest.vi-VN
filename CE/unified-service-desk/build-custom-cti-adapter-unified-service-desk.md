---
title: Build a custom CTI adapter for Unified Service Desk | MicrosoftDocs
description: Learn about building a custom computer telephony integration (CTI) adapter to connect to a CTI system that provides access to events and CTI actions via web services or APIs.
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
ms.assetid: 19cd4af7-2465-4c61-ba7e-56b89720c69a
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 3f6e5d196f83a8c23a107c759cc8bba7ba54c684
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386317"
---
# <a name="build-a-custom-cti-adapter-for-unified-service-desk"></a><span data-ttu-id="1d391-103">Build a custom CTI adapter for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="1d391-103">Build a custom CTI adapter for Unified Service Desk</span></span>
<span data-ttu-id="1d391-104">You can build a custom [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] adapter to connect to a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system that provides access to events and [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] actions via web services or APIs.</span><span class="sxs-lookup"><span data-stu-id="1d391-104">You can build a custom [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] adapter to connect to a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system that provides access to events and [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] actions via web services or APIs.</span></span>  
  
 <span data-ttu-id="1d391-105">The [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] infrastructure supports connecting to both models (web services or APIs).</span><span class="sxs-lookup"><span data-stu-id="1d391-105">The [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] infrastructure supports connecting to both models (web services or APIs).</span></span> <span data-ttu-id="1d391-106">Building a custom adapter involves:</span><span class="sxs-lookup"><span data-stu-id="1d391-106">Building a custom adapter involves:</span></span>  
  
1. <span data-ttu-id="1d391-107">Creating the connection bridge to the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system.</span><span class="sxs-lookup"><span data-stu-id="1d391-107">Creating the connection bridge to the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system.</span></span> [<span data-ttu-id="1d391-108">Tạo trình kết nối CTI</span><span class="sxs-lookup"><span data-stu-id="1d391-108">Create a CTI Connector</span></span>](../unified-service-desk/create-cti-connector.md)  
  
2. <span data-ttu-id="1d391-109">Creating a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] manager that communicates between the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] connection layer and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to manage calls and the agent state.</span><span class="sxs-lookup"><span data-stu-id="1d391-109">Creating a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] manager that communicates between the [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] connection layer and [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to manage calls and the agent state.</span></span> [<span data-ttu-id="1d391-110">Create a CTI Desktop Manager</span><span class="sxs-lookup"><span data-stu-id="1d391-110">Create a CTI Desktop Manager</span></span>](../unified-service-desk/create-cti-desktop-manager.md)  
  
3. <span data-ttu-id="1d391-111">Define the user interface or the controls on the agent desktop that helps in call management and displays the agent state.</span><span class="sxs-lookup"><span data-stu-id="1d391-111">Define the user interface or the controls on the agent desktop that helps in call management and displays the agent state.</span></span> [<span data-ttu-id="1d391-112">Create a CTI Control</span><span class="sxs-lookup"><span data-stu-id="1d391-112">Create a CTI Control</span></span>](../unified-service-desk/create-cti-control.md)  
  
### <a name="see-also"></a><span data-ttu-id="1d391-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1d391-113">See also</span></span>  
 <span data-ttu-id="1d391-114">[Considerations for creating a CTI adapter for Unified Service Desk](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="1d391-114">[Considerations for creating a CTI adapter for Unified Service Desk](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="1d391-115">Integrate with CTI systems using CTI adapters</span><span class="sxs-lookup"><span data-stu-id="1d391-115">Integrate with CTI systems using CTI adapters</span></span>](../unified-service-desk/integrate-cti-systems-cti-adapters.md)
