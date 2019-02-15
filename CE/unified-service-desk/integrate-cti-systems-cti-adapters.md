---
title: Integrate with CTI systems using CTI adapters| MicrosoftDocs
description: Learn about the integration with CTI systems using CTI adapters.
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
ms.assetid: 88430e53-36e8-47ee-9e12-34b4d2e98362
caps.latest.revision: 7
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: f2262b997884a60d2b54db7a262b0c80d1871b1e
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385474"
---
# <a name="integrate-unified-service-desk-with-cti-systems-using-cti-adapters"></a><span data-ttu-id="ac4ff-103">Integrate Unified Service Desk with CTI systems using CTI adapters</span><span class="sxs-lookup"><span data-stu-id="ac4ff-103">Integrate Unified Service Desk with CTI systems using CTI adapters</span></span>
<span data-ttu-id="ac4ff-104">To integrate [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with your [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] system, use a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter.</span><span class="sxs-lookup"><span data-stu-id="ac4ff-104">To integrate [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with your [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] system, use a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter.</span></span> <span data-ttu-id="ac4ff-105">The [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] framework has components that you can use to build a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter.</span><span class="sxs-lookup"><span data-stu-id="ac4ff-105">The [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)][!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] framework has components that you can use to build a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ac4ff-106">[UII CTI Framework Components](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md#Architecture).</span><span class="sxs-lookup"><span data-stu-id="ac4ff-106">[UII CTI Framework Components](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md#Architecture).</span></span>  
  
 <span data-ttu-id="ac4ff-107">You can create two types of [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapters for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="ac4ff-107">You can create two types of [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapters for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
- <span data-ttu-id="ac4ff-108">The first type involves defining a *CTI Desktop Manager* component with the required telephony actions for call and agent state management that can communicate with your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system.</span><span class="sxs-lookup"><span data-stu-id="ac4ff-108">The first type involves defining a *CTI Desktop Manager* component with the required telephony actions for call and agent state management that can communicate with your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system.</span></span> <span data-ttu-id="ac4ff-109">Next, you configure it as a **CTI Desktop Manager** type of hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], which enables you to handle the interpretation of requests from a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system, and then route it within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="ac4ff-109">Next, you configure it as a **CTI Desktop Manager** type of hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], which enables you to handle the interpretation of requests from a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system, and then route it within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
  [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="ac4ff-110">provides a generic listener adapter that you can use to test your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system by sending [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] requests on a port with standard parameters that [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] can evaluate as a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event.</span><span class="sxs-lookup"><span data-stu-id="ac4ff-110">provides a generic listener adapter that you can use to test your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system by sending [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] requests on a port with standard parameters that [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] can evaluate as a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] event.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ac4ff-111">[Using the generic listener adapter in Unified Service Desk](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="ac4ff-111">[Using the generic listener adapter in Unified Service Desk](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md)</span></span>  
  
- <span data-ttu-id="ac4ff-112">The second type of adapter involves building all the components of a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter from scratch where you define how to connect to your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system (*CTI Connector*), how the calls and agent states will be managed (*CTI Desktop Manager*), and the look and feel of your softphone (*CTI Controls*).</span><span class="sxs-lookup"><span data-stu-id="ac4ff-112">The second type of adapter involves building all the components of a [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] adapter from scratch where you define how to connect to your [!INCLUDE[pn_cti_acronym](../includes/pn-cti-acronym.md)] system (*CTI Connector*), how the calls and agent states will be managed (*CTI Desktop Manager*), and the look and feel of your softphone (*CTI Controls*).</span></span> <span data-ttu-id="ac4ff-113">This type of adapter is used if your CTI system uses a service-based polling system or uses a callback/event notification system.</span><span class="sxs-lookup"><span data-stu-id="ac4ff-113">This type of adapter is used if your CTI system uses a service-based polling system or uses a callback/event notification system.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="ac4ff-114">[Build a custom CTI adapter for Unified Service Desk](../unified-service-desk/build-custom-cti-adapter-unified-service-desk.md)</span><span class="sxs-lookup"><span data-stu-id="ac4ff-114">[Build a custom CTI adapter for Unified Service Desk](../unified-service-desk/build-custom-cti-adapter-unified-service-desk.md)</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ac4ff-115">Trong Phần này</span><span class="sxs-lookup"><span data-stu-id="ac4ff-115">In This Section</span></span>  
 [<span data-ttu-id="ac4ff-116">Use the generic listener adapter in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ac4ff-116">Use the generic listener adapter in Unified Service Desk</span></span>](../unified-service-desk/use-generic-listener-adapter-unified-service-desk.md)  
  
 [<span data-ttu-id="ac4ff-117">Build a custom CTI adapter for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ac4ff-117">Build a custom CTI adapter for Unified Service Desk</span></span>](../unified-service-desk/build-custom-cti-adapter-unified-service-desk.md)  
  
 [<span data-ttu-id="ac4ff-118">Considerations for creating a CTI adapter for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="ac4ff-118">Considerations for creating a CTI adapter for Unified Service Desk</span></span>](../unified-service-desk/consideration-creating-cti-adapter-unified-service-desk.md)  
  
 [<span data-ttu-id="ac4ff-119">Walkthrough: Use generic listener adapter for CTI events</span><span class="sxs-lookup"><span data-stu-id="ac4ff-119">Walkthrough: Use generic listener adapter for CTI events</span></span>](../unified-service-desk/walkthrough-use-the-generic-listener-adapter-for-cti-event-routing.md)  
  
## <a name="related-sections"></a><span data-ttu-id="ac4ff-120">Các phần liên quan</span><span class="sxs-lookup"><span data-stu-id="ac4ff-120">Related Sections</span></span>  
 [<span data-ttu-id="ac4ff-121">UII Computer Telephony Integration (CTI) framework</span><span class="sxs-lookup"><span data-stu-id="ac4ff-121">UII Computer Telephony Integration (CTI) framework</span></span>](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)  
  
 [<span data-ttu-id="ac4ff-122">Tham chiếu chương trình</span><span class="sxs-lookup"><span data-stu-id="ac4ff-122">Programming reference</span></span>](../unified-service-desk/programming-reference.md)
