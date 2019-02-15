---
title: CCA Hosted Application (Hosted Control) | MicrosoftDocs
description: The topic explains Customer Care Accelerator (CCA) hosted application (Hosted Control) that enables you to host an external application or web application in Unified Service Desk and interact with it by using the UII adapters.
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
ms.assetid: 321a95f9-fd0a-45fc-a624-13bf1aa928bd
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
ms.openlocfilehash: 65ee9b00987f0b2dea1dd9cff2d32cad4d68d34b
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385854"
---
# <a name="cca-hosted-application-hosted-control"></a><span data-ttu-id="b68b9-103">CCA Hosted Application (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="b68b9-103">CCA Hosted Application (Hosted Control)</span></span>
<span data-ttu-id="b68b9-104">A Customer Care Accelerator (CCA) hosted application hosted control enables you to host an external application or web application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and interact with it by using the [UII adapters](../unified-service-desk/uii-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="b68b9-104">A Customer Care Accelerator (CCA) hosted application hosted control enables you to host an external application or web application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and interact with it by using the [UII adapters](../unified-service-desk/uii-adapters.md).</span></span> <span data-ttu-id="b68b9-105">Nó cũng được sử dụng để lưu trữ kiểm soát kết nối với hệ thống [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with a [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)].</span><span class="sxs-lookup"><span data-stu-id="b68b9-105">It is also used for hosting the control that connects [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] with a [!INCLUDE[pn_computer_telephony_integration_cti](../includes/pn-computer-telephony-integration-cti.md)] system.</span></span>  
  
 <span data-ttu-id="b68b9-106">Loại tổ chức kiểm soát này cũng cung cấp liên kết tới các ứng dụng CCA được lưu trữ truyền thống.</span><span class="sxs-lookup"><span data-stu-id="b68b9-106">This type of hosted control also provides the link to traditional CCA hosted applications.</span></span> <span data-ttu-id="b68b9-107">For more information about building a CCA hosted application, see the see the **CCA Deployment Guide** in the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] SDK [download package](http://go.microsoft.com/fwlink/p/?LinkId=519179).</span><span class="sxs-lookup"><span data-stu-id="b68b9-107">For more information about building a CCA hosted application, see the see the **CCA Deployment Guide** in the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] SDK [download package](http://go.microsoft.com/fwlink/p/?LinkId=519179).</span></span>  
  
<a name="Create"></a>   
## <a name="create-a-cca-hosted-application-hosted-control"></a><span data-ttu-id="b68b9-108">Tạo kiểm soát tổ chức ứng dụng tổ chức CCA</span><span class="sxs-lookup"><span data-stu-id="b68b9-108">Create a CCA Hosted Application hosted control</span></span>  
 <span data-ttu-id="b68b9-109">Bạn tạo một loại kiểm soát lưu trữ của **Ứng dụng CCA Được lưu trữ** để lưu trữ một ứng dụng [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] được lưu trữ.</span><span class="sxs-lookup"><span data-stu-id="b68b9-109">You create a hosted control type of **CCA Hosted Application** to host a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application.</span></span> <span data-ttu-id="b68b9-110">Ứng dụng được lưu trữ [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] là một kiểm soát người dùng có thể được sử dụng để lưu trữ các ứng dụng bên ngoài, web, từ xa và tùy chỉnh bên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="b68b9-110">A [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application is a user control that can be used to host external, web, remote and custom applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="b68b9-111">For information about using [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted applications, see [Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b68b9-111">For information about using [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted applications, see [Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md).</span></span>  
  
 <span data-ttu-id="b68b9-112">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="b68b9-112">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="b68b9-113">For detailed information about the information that you need to specify for each field for creating a **CCA Hosted Application** type of hosted control, see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span><span class="sxs-lookup"><span data-stu-id="b68b9-113">For detailed information about the information that you need to specify for each field for creating a **CCA Hosted Application** type of hosted control, see [Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b68b9-114">Loại kiểm soát tổ chức **Ứng dụng tổ chức CCA** có một số lượng giới hạn vì nó liên quan đến chức năng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="b68b9-114">The **CCA Hosted Application** hosted control type has a number of limitations as it relates to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] functionality.</span></span> <span data-ttu-id="b68b9-115">Đặc biệt, những kiểm soát tổ chức này không bắt đầu sự kiện.</span><span class="sxs-lookup"><span data-stu-id="b68b9-115">In particular, these hosted controls don’t fire events.</span></span> <span data-ttu-id="b68b9-116">Trong khi các kiểm soát này có thể bắt đầu sự kiện vào [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], kiểm soát đó không tự động như các kiểm soát tổ chức [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] khác.</span><span class="sxs-lookup"><span data-stu-id="b68b9-116">While it’s possible for these controls to fire events into [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], it isn’t automatic like it would be for other [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] hosted controls.</span></span>  
  
<a name="actions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="b68b9-117">Thao tác UII được xác định trước</span><span class="sxs-lookup"><span data-stu-id="b68b9-117">Predefined UII actions</span></span>  
 <span data-ttu-id="b68b9-118">Nhà phát triển của ứng dụng được lưu trữ [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] xác định hành động nào nên được thêm vào kiểm soát.</span><span class="sxs-lookup"><span data-stu-id="b68b9-118">The developer of the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application decides which actions should be added to the control.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b68b9-119">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b68b9-119">See also</span></span>  
 <span data-ttu-id="b68b9-120">[Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md) </span><span class="sxs-lookup"><span data-stu-id="b68b9-120">[Create and manage UII hosted applications](../unified-service-desk/create-manage-uii-hosted-applications.md) </span></span>  
 <span data-ttu-id="b68b9-121">[Use UII adapters to interact with external and web applications](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="b68b9-121">[Use UII adapters to interact with external and web applications](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md) </span></span>  
 <span data-ttu-id="b68b9-122">[Use UII automation adapters to interact with external and web applications](../unified-service-desk/use-uii-automation-adapter-interact-external-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="b68b9-122">[Use UII automation adapters to interact with external and web applications](../unified-service-desk/use-uii-automation-adapter-interact-external-web-applications.md) </span></span>  
 <span data-ttu-id="b68b9-123">[Use UII hosted controls with Unified Service Desk](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="b68b9-123">[Use UII hosted controls with Unified Service Desk](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="b68b9-124">Integrate with CTI systems using CTI adapters</span><span class="sxs-lookup"><span data-stu-id="b68b9-124">Integrate with CTI systems using CTI adapters</span></span>](../unified-service-desk/integrate-cti-systems-cti-adapters.md)
