---
title: Hosted control types, action, and event reference in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: The section provides information about the various types of hosted controls in Unified Service Desk, and the predefined User Interface Integration (UII) actions and events available for each hosted control type.
keywords: ''
ms.date: 08/17/2018
ms.service:
- dynamics-365-customerservice
ms.custom:
- dyn365-USD
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement apps
- Dynamics 365 for Customer Engagement (on-premises) apps
- Dynamics CRM 2013
- Dynamics CRM 2015
- Dynamics CRM 2016
ms.assetid: 4b891311-28d7-4776-8414-c6d83bfe43bf
author: kabala123
ms.author: kabala
manager: shujoshi
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 97cab8f13f4ddfa3a11311cbd86f89f65bbd7934
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388480"
---
# <a name="hosted-control-types-action-and-event-reference-in-unified-service-desk"></a><span data-ttu-id="2c5b4-103">Hosted control types, action, and event reference in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2c5b4-103">Hosted control types, action, and event reference in Unified Service Desk</span></span>
<span data-ttu-id="2c5b4-104">This section provides information about the various types of hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and the predefined [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] actions and events available for each hosted control type.</span><span class="sxs-lookup"><span data-stu-id="2c5b4-104">This section provides information about the various types of hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and the predefined [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] actions and events available for each hosted control type.</span></span> <span data-ttu-id="2c5b4-105">You can also view information about the predefined [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions and events for hosted controls in the embedded help in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2c5b4-105">You can also view information about the predefined [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions and events for hosted controls in the embedded help in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2c5b4-106">[View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-106">[View embedded help for actions and events](../unified-service-desk/view-embedded-help-for-actions-and-events.md)</span></span>  
  
 <span data-ttu-id="2c5b4-107">Apart from the predefined hosted control types, this section also provides information about a custom hosted control, `Session Timer`, that becomes available when you deploy one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="2c5b4-107">Apart from the predefined hosted control types, this section also provides information about a custom hosted control, `Session Timer`, that becomes available when you deploy one of the sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] applications on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2c5b4-108">[Session Timer (Custom Hosted Control)](../unified-service-desk/session-timer-custom-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-108">[Session Timer (Custom Hosted Control)](../unified-service-desk/session-timer-custom-hosted-control.md)</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2c5b4-109">Most of the predefined hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] have a predefined action called **default**, which calls an action on the hosted control that’s marked as the default.</span><span class="sxs-lookup"><span data-stu-id="2c5b4-109">Most of the predefined hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] have a predefined action called **default**, which calls an action on the hosted control that’s marked as the default.</span></span> <span data-ttu-id="2c5b4-110">Because none of the predefined actions for any of the predefined hosted controls are marked as default, calling the **default** action on any predefined hosted control just loads the respective hosted control.</span><span class="sxs-lookup"><span data-stu-id="2c5b4-110">Because none of the predefined actions for any of the predefined hosted controls are marked as default, calling the **default** action on any predefined hosted control just loads the respective hosted control.</span></span> <span data-ttu-id="2c5b4-111">However, for a custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control, you can define an action and set it as default so that the action is called when the **default** action is called on the custom hosted control.</span><span class="sxs-lookup"><span data-stu-id="2c5b4-111">However, for a custom [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted control, you can define an action and set it as default so that the action is called when the **default** action is called on the custom hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="2c5b4-112">[USD Hosted Control (Hosted Control)](../unified-service-desk/usd-hosted-control-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-112">[USD Hosted Control (Hosted Control)](../unified-service-desk/usd-hosted-control-hosted-control.md)</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2c5b4-113">In this section</span><span class="sxs-lookup"><span data-stu-id="2c5b4-113">In this section</span></span>  
 [<span data-ttu-id="2c5b4-114">Trình quản lý kết nối (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-114">Connection Manager (Hosted Control)</span></span>](../unified-service-desk/connection-manager-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-115">Global Manager (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-115">Global Manager (Hosted Control)</span></span>](../unified-service-desk/global-manager-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-116">Mã lệnh tổng đài viên (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-116">Agent Scripting (Hosted Control)</span></span>](../unified-service-desk/agent-scripting-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-117">Hộp thoại CRM (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-117">CRM Dialog (Hosted Control)</span></span>](../unified-service-desk/crm-dialog-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-118">CRM Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-118">CRM Page (Hosted Control)</span></span>](../unified-service-desk/crm-page-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-119">Trình quản lý máy tính để bàn CTI (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-119">CTI Desktop Manager (Hosted Control)</span></span>](../unified-service-desk/cti-desktop-manager-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-120">Trình gỡ lỗi (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-120">Debugger (Hosted Control)</span></span>](../unified-service-desk/debugger-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-121">Interactive Service Hub Page (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-121">Interactive Service Hub Page (Hosted Control)</span></span>](../unified-service-desk/interactive-service-hub-page-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-122">Unified Interface KM Control (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-122">Unified Interface KM Control (Hosted Control)</span></span>](../unified-service-desk/unified-interface-km-control-hosted-control.md)  

 [<span data-ttu-id="2c5b4-123">KM Control (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-123">KM Control (Hosted Control)</span></span>](../unified-service-desk/km-control-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-124">Listener Hosted Control (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-124">Listener Hosted Control (Hosted Control)</span></span>](../unified-service-desk/listener-hosted-control-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-125">Bố cục bảng điều khiển (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-125">Panel Layout (Hosted Control)</span></span>](../unified-service-desk/panel-layout-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-126">Popup Notification (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-126">Popup Notification (Hosted Control)</span></span>](../unified-service-desk/popup-notification-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-127">Dòng phiên (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-127">Session Lines (Hosted Control)</span></span>](../unified-service-desk/session-lines-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-128">Tab Phiên (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-128">Session Tabs (Hosted Control)</span></span>](../unified-service-desk/session-tabs-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-129">Ứng dụng Web tiêu chuẩn (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-129">Standard Web Application (Hosted Control)</span></span>](../unified-service-desk/standard-web-application-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-130">Bộ chứa Thanh công cụ (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-130">Toolbar Container (Hosted Control)</span></span>](../unified-service-desk/toolbar-container-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-131">Ghi chú của người dùng (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-131">User Notes (Hosted Control)</span></span>](../unified-service-desk/user-notes-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-132">USD Hosted Control (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-132">USD Hosted Control (Hosted Control)</span></span>](../unified-service-desk/usd-hosted-control-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-133">Ứng dụng Được tổ chức CCA (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-133">CCA Hosted Application (Hosted Control)</span></span>](../unified-service-desk/cca-hosted-application-hosted-control.md)  
  
 [<span data-ttu-id="2c5b4-134">Session Timer (Custom Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="2c5b4-134">Session Timer (Custom Hosted Control)</span></span>](../unified-service-desk/session-timer-custom-hosted-control.md)  
  
  
## <a name="related-topics"></a><span data-ttu-id="2c5b4-135">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="2c5b4-135">Related topics</span></span>  
 [<span data-ttu-id="2c5b4-136">Learn to configure Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2c5b4-136">Learn to configure Unified Service Desk</span></span>](../unified-service-desk/learn-to-use-unified-service-desk.md)  
  
 [<span data-ttu-id="2c5b4-137">Get started with configuring your agent application</span><span class="sxs-lookup"><span data-stu-id="2c5b4-137">Get started with configuring your agent application</span></span>](../unified-service-desk/get-started-configuring-agent-application.md)  
  
 [<span data-ttu-id="2c5b4-138">Cách thức của Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2c5b4-138">Unified Service Desk walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)  
  
 [<span data-ttu-id="2c5b4-139">Extend Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2c5b4-139">Extend Unified Service Desk</span></span>](../unified-service-desk/extend-unified-service-desk.md)  
  
 [<span data-ttu-id="2c5b4-140">Tổng quan cho Nhà phát triển Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="2c5b4-140">Unified Service Desk Developer Overview</span></span>](../unified-service-desk/admin/overview-unified-service-desk.md)
