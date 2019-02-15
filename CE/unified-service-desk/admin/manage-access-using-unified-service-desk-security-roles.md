---
title: Manage access using Unified Service Desk for Dynamics 365 for Customer Engagement security roles | MicrosoftDocs
description: Learn to control how agents use Unified Service Desk for Dynamics 365 for Customer Engagement by using security roles.
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
ms.assetid: 1d1e06fc-188d-4f3e-91b1-a6c371c28eb4
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
ms.openlocfilehash: aeba7dd4031567e2a60116762508d0db71af15fc
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "382421"
---
# <a name="use-security-roles-to-manage-access"></a><span data-ttu-id="01439-103">Use security roles to manage access</span><span class="sxs-lookup"><span data-stu-id="01439-103">Use security roles to manage access</span></span> 
<span data-ttu-id="01439-104">Bạn phải chỉ định hai [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] vai trò bảo mật cho người dùng hoặc nhóm thích hợp.</span><span class="sxs-lookup"><span data-stu-id="01439-104">You must assign the two [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] security roles to appropriate users or teams.</span></span> <span data-ttu-id="01439-105">Vai trò **Quản trị viên USD** phải được chỉ định cho những người dùng sẽ định cấu hình ứng dụng sử dụng [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] để xác định ứng dụng tác nhân.</span><span class="sxs-lookup"><span data-stu-id="01439-105">The **USD Administrator** role must be assigned to the users who will be configuring the application using [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] to define an agent application.</span></span> <span data-ttu-id="01439-106">Vai trò **Tác nhân USD** phải được gán cho người dùng cuối (tác nhân) người sẽ sử dụng các ứng dụng hàng để kết nối với phiên bản [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] bằng thực thể [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] đã được cấu hình.</span><span class="sxs-lookup"><span data-stu-id="01439-106">The **USD Agent** role must be assigned to the end users (agents) who will be using the client application to connect to the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] instance with the configured [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] entities.</span></span>  
  
 <span data-ttu-id="01439-107">Bạn cũng phải chỉ định vai trò bảo mật [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] thích hợp cho các quản trị viên và tác nhân của [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] cùng với vai trò bảo mật [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] để tạo thuận lợi cho truy nhập phù hợp trên các thực thể [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] cùng với [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] và thực thể UII tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="01439-107">You must also assign the appropriate [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] security role to the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] administrators and agents along with the [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] security role to facilitate appropriate access on the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] entities along with the custom [!INCLUDE[pn_unified_service_desk](../../includes/pn-unified-service-desk.md)] and UII entities.</span></span> <span data-ttu-id="01439-108">Ví dụ: bạn nên gán vai trò **Đại diện dịch vụ khách hàng** cùng với vai trò **Tác nhân USD** cho các tác nhân.</span><span class="sxs-lookup"><span data-stu-id="01439-108">For example, you should assign the **Customer Service Representative** role along with the **USD Agent** role to the agents.</span></span>  
  
 <span data-ttu-id="01439-109">For information about assigning a security role to a user or team in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], see [Security roles and privileges](/dynamics365/customer-engagement/admin/security-roles-privileges) or [Manage teams](/dynamics365/customer-engagement/admin/manage-teams).</span><span class="sxs-lookup"><span data-stu-id="01439-109">For information about assigning a security role to a user or team in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], see [Security roles and privileges](/dynamics365/customer-engagement/admin/security-roles-privileges) or [Manage teams](/dynamics365/customer-engagement/admin/manage-teams).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01439-110">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="01439-110">See also</span></span>  
 <span data-ttu-id="01439-111">[Create Unified Service Desk Configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="01439-111">[Create Unified Service Desk Configuration](../../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md) </span></span>  
 <span data-ttu-id="01439-112">[Access management in Unified Service Desk](../../unified-service-desk/admin/security-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="01439-112">[Access management in Unified Service Desk](../../unified-service-desk/admin/security-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="01439-113">Privilege and role entities</span><span class="sxs-lookup"><span data-stu-id="01439-113">Privilege and role entities</span></span>](https://msdn.microsoft.com/library/gg328230.aspx)
