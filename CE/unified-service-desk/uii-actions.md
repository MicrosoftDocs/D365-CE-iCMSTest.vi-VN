---
title: UII actions in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Learn about UII actions in Unified Service Desk that define a specific operation that can be performed when called.
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
ms.assetid: 145b3e99-2423-441e-88ac-ec99b1364ed6
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
ms.openlocfilehash: 0c024104ad0552e323eae41e0576f5e40cf059e1
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388151"
---
# <a name="uii-actions-in-unified-service-desk"></a><span data-ttu-id="96c49-103">UII actions in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="96c49-103">UII actions in Unified Service Desk</span></span>
<span data-ttu-id="96c49-104">Hành động UII là một khái niệm kế thừa từ [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] (UII).</span><span class="sxs-lookup"><span data-stu-id="96c49-104">UII action is a concept inherited from [!INCLUDE[pn_user_interface_integration](../includes/pn-user-interface-integration.md)] (UII).</span></span> <span data-ttu-id="96c49-105">Hành động UII là cốt lõi của kiểm soát tổ chức và xác định một hoạt động cụ thể mà có thể được thực hiện khi được gọi.</span><span class="sxs-lookup"><span data-stu-id="96c49-105">UII actions are the core of a hosted control, and define a specific operation that can be performed when called.</span></span> <span data-ttu-id="96c49-106">Hành động UII có thể được dùng như các phương pháp chung mà có thể được gọi từ thành phần bên ngoài và là chủ đề của cuộc gọi hành động trong [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span><span class="sxs-lookup"><span data-stu-id="96c49-106">UII action can be thought of as the public methods that can be called from external components, and are the subject of action calls in [!INCLUDE[pn_unified_service_desk_for_crm](../includes/pn-unified-service-desk-for-crm.md)].</span></span> <span data-ttu-id="96c49-107">Kiểm soát tổ chức không thể tương tác với phần còn lại của các ứng dụng nếu không có hành động UII được xác định hoặc có sẵn cho kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="96c49-107">A hosted control cannot interact with the rest of the application if no UII action is defined or available for the hosted control.</span></span>  
  
 <span data-ttu-id="96c49-108">Với mỗi loại kiểm soát tổ chức được xác định trước trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], một tập hợp các hoạt động UII có sẵn.</span><span class="sxs-lookup"><span data-stu-id="96c49-108">For each predefined hosted control type in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], a set of predefined UII actions are available.</span></span> <span data-ttu-id="96c49-109">For information about predefined UII actions available for each hosted control type, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md).</span><span class="sxs-lookup"><span data-stu-id="96c49-109">For information about predefined UII actions available for each hosted control type, see [Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md).</span></span> <span data-ttu-id="96c49-110">If you are developing a custom hosted control, it is not enough to just override the `DoAction` method in the code to handle a specific action for the hosted control.</span><span class="sxs-lookup"><span data-stu-id="96c49-110">If you are developing a custom hosted control, it is not enough to just override the `DoAction` method in the code to handle a specific action for the hosted control.</span></span> <span data-ttu-id="96c49-111">You must explicitly define the action in the **UII Actions** list for the custom hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, thereby enabling the user to call it using action calls.</span><span class="sxs-lookup"><span data-stu-id="96c49-111">You must explicitly define the action in the **UII Actions** list for the custom hosted control in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps, thereby enabling the user to call it using action calls.</span></span> <span data-ttu-id="96c49-112">For more information about explicitly defining a UII action for a custom hosted control, see [Create custom Unified Service Desk hosted control](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="96c49-112">For more information about explicitly defining a UII action for a custom hosted control, see [Create custom Unified Service Desk hosted control](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="96c49-113">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="96c49-113">See also</span></span>  
 <span data-ttu-id="96c49-114">[Thêm một hành động UII vào một điều khiển tổ chức](../unified-service-desk/add-uii-action-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="96c49-114">[Add a UII action to a hosted control](../unified-service-desk/add-uii-action-hosted-control.md) </span></span>  
 <span data-ttu-id="96c49-115">[Cuộc gọi hành động](../unified-service-desk/action-calls.md) </span><span class="sxs-lookup"><span data-stu-id="96c49-115">[Action calls](../unified-service-desk/action-calls.md) </span></span>  
 <span data-ttu-id="96c49-116">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span><span class="sxs-lookup"><span data-stu-id="96c49-116">[Create an action call for a UII action](../unified-service-desk/create-action-call-uii-action.md) </span></span>  
 [<span data-ttu-id="96c49-117">Core concepts for configuring Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="96c49-117">Core concepts for configuring Unified Service Desk</span></span>](../unified-service-desk/core-concepts-for-configuring-unified-service-desk.md)
