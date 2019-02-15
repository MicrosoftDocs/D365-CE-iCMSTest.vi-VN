---
title: Manage access in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs
description: Learn how to control user access to Unified Service Desk for Dynamics 365 for Customer Engagement apps by using configuration and security roles.
ms.custom:
- dyn365-USD, dyn365-admin
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
ms.assetid: 6246a780-eb72-4c37-b84a-9a78904ed631
caps.latest.revision: 5
author: kabala123
ms.author: kabala
manager: shujoshi
tags:
- MigrationHO
search.audienceType:
- admin
search.app:
- D365CE
- D365USD
ms.openlocfilehash: b1c592430deb42463c532e5e4a575c9a763e2bb3
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382555"
---
# <a name="about-access-control"></a><span data-ttu-id="aa3ac-103">About access control</span><span class="sxs-lookup"><span data-stu-id="aa3ac-103">About access control</span></span>
[!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] <span data-ttu-id="aa3ac-104">configuration entities and the underlying [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] entities are stored in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and you can use the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security model to govern access to both of these entities.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-104">configuration entities and the underlying [!INCLUDE[pn_user_inteface_integration_uii](../../includes/pn-user-interface-integration-uii.md)] entities are stored in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps, and you can use the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security model to govern access to both of these entities.</span></span> [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] <span data-ttu-id="aa3ac-105">has a robust security model that combines role-based, record-level, and field-level security to define the overall security rights that users have.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-105">has a robust security model that combines role-based, record-level, and field-level security to define the overall security rights that users have.</span></span> [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="aa3ac-106">[Security concepts for Microsoft Dynamics CRM](/dynamics365/customer-engagement/admin/security-concepts)</span><span class="sxs-lookup"><span data-stu-id="aa3ac-106">[Security concepts for Microsoft Dynamics CRM](/dynamics365/customer-engagement/admin/security-concepts)</span></span>  
  
 [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)]<span data-ttu-id="aa3ac-107">người dùng có thể được phân loại rộng rãi thành hai loại:</span><span class="sxs-lookup"><span data-stu-id="aa3ac-107">users can be broadly classified into two categories:</span></span>  
  
- <span data-ttu-id="aa3ac-108">**Quản trị viên**: những người đặt cấu hình các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và thực thể UII để xác định một ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-108">**Administrators**: People who configure the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and UII entities to define an agent application.</span></span>  
  
- <span data-ttu-id="aa3ac-109">**Tổng đài viên**: những người sử dụng các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] ứng dụng khách để đọc cấu hình trong [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và thực thể UII để thực hiện công việc hàng ngày của họ trong một trung tâm cuộc gọi.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-109">**Agents**: People who use the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] client application to read the configuration in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and UII entities to perform their day-to-day work in a call center.</span></span>  
  
## <a name="using-unified-service-desk-security-roles"></a><span data-ttu-id="aa3ac-110">Sử dụng vai trò bảo mật mới cho Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="aa3ac-110">Using Unified Service Desk security roles</span></span>  
 <span data-ttu-id="aa3ac-111">Khi bạn triển khai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cho phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], bốn vai trò bảo mật được tạo ra:</span><span class="sxs-lookup"><span data-stu-id="aa3ac-111">When you deploy [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] to a [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance, four security roles are created:</span></span>  
  
- <span data-ttu-id="aa3ac-112">Vai trò **UIIAdministrator** và **UIIAgent** xác định quyền truy cập vào UII và yêu cầu thực thể [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="aa3ac-112">**UIIAdministrator** and **UIIAgent** roles define access to the UII and required [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] entities.</span></span>  
  
- <span data-ttu-id="aa3ac-113">Vai trò **Quản trị viên USD** và **USD đại lý** xác định quyền truy cập vào các [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] tổ chức, các thực thể UII tiềm ẩn, và yêu cầu [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] thực thể.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-113">**USD Administrator** and **USD Agent** roles define access to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] entities, the underlying UII entities, and required [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] entities.</span></span> <span data-ttu-id="aa3ac-114">Bạn phải gán một trong hai vai trò cho người dùng trong tổ chức của bạn tùy thuộc vào vai trò công việc của họ (người quản trị hoặc đại lý).</span><span class="sxs-lookup"><span data-stu-id="aa3ac-114">You must assign one of these two roles to users in your organization depending on their job role (administrator or agent).</span></span>  
  
  [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="aa3ac-115">[Implement security using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)</span><span class="sxs-lookup"><span data-stu-id="aa3ac-115">[Implement security using custom security roles](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)</span></span>  
  
## <a name="using-unified-service-desk-configuration"></a><span data-ttu-id="aa3ac-116">Sử dụng cấu hình ứng dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="aa3ac-116">Using Unified Service Desk configuration</span></span>  
 <span data-ttu-id="aa3ac-117">Một cách tiếp cận khác để lọc truy cập vào dữ liệu [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] là thông qua sử dụng cấu hình.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-117">Another approach to filtering access to [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] data is through the use of configurations.</span></span> <span data-ttu-id="aa3ac-118">Cấu hình là nhóm hợp lý của các thành phần khác nhau trong ứng dụng đại lý [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] chẳng hạn như cuộc gọi hành động, mã lệnh tổng đài viên, tìm kiếm thực thể, sự kiện, và kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-118">A configuration is the logical grouping of various components in the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] agent application such as action calls, agent scripts, entity searches, events, and hosted controls.</span></span> <span data-ttu-id="aa3ac-119">Cấu hình có thể được gán cho người dùng để khi người dùng bắt đầu ứng dụng tổng đài viên [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)], chỉ có các thành phần bao gồm trong cấu hình được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-119">The configuration can be assigned to a user so that when the user starts the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] agent application, only the components included in the configuration are displayed.</span></span> <span data-ttu-id="aa3ac-120">Đây là một cách tuyệt vời để lọc điều mà bạn muốn được hiển thị cho các tổng đài viên của bạn mà không cần phải quản lý vai trò bảo mật của họ.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-120">This is a great way to filter things that you want to be displayed to your agents without having to manage their security roles.</span></span> <span data-ttu-id="aa3ac-121">Tuy nhiên, xin vui lòng lưu ý những điều sau đây:</span><span class="sxs-lookup"><span data-stu-id="aa3ac-121">However, please keep the following things in mind:</span></span>  
  
- <span data-ttu-id="aa3ac-122">A configuration can only be assigned to a user, and not to a team in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-122">A configuration can only be assigned to a user, and not to a team in [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
- <span data-ttu-id="aa3ac-123">Một cấu hình chỉ lọc các thành phần khi bạn truy cập vào thông tin [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] thông qua ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-123">A configuration only filters the components when you access [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] information through the client application.</span></span> <span data-ttu-id="aa3ac-124">If you access [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)] directly, you can access data as per your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security role.</span><span class="sxs-lookup"><span data-stu-id="aa3ac-124">If you access [!INCLUDE[pn_microsoftcrm](../../includes/pn-microsoftcrm.md)] apps or [!INCLUDE[pn_microsoft_dynamics_crm_for_outlook](../../includes/pn-microsoft-dynamics-crm-for-outlook.md)] directly, you can access data as per your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security role.</span></span>  
  
  [!INCLUDE[proc_more_information](../../includes/proc-more-information.md)] <span data-ttu-id="aa3ac-125">[Manage access using Unified Service Desk configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="aa3ac-125">[Manage access using Unified Service Desk configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
  
## <a name="see-also"></a><span data-ttu-id="aa3ac-126">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="aa3ac-126">See also</span></span>  
 [<span data-ttu-id="aa3ac-127">Quản lý quyền truy cập bằng cách sử dụng vai trò bảo mật của Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="aa3ac-127">Manage access using Unified Service Desk security roles</span></span>](../../unified-service-desk/admin/manage-access-using-unified-service-desk-security-roles.md)  
  
 [<span data-ttu-id="aa3ac-128">Quản lý quyền truy cập bằng cách sử dụng cấu hình của Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="aa3ac-128">Manage access using Unified Service Desk configuration</span></span>](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)  
