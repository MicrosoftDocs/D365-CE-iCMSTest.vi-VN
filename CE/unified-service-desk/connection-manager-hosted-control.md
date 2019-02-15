---
title: Connection Manager (Hosted Control) | MicrosoftDocs
description: The Connection Manager hosted control type manages connections to the Dynamics 365 for Customer Engagement server, and makes it available to the rest of the agent application.
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
ms.assetid: c1a9b9ef-6243-4d1c-b0fe-726def04b417
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 79be0986f6f5b692ec38b39350a43fff36e666ff
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387568"
---
# <a name="connection-manager-hosted-control"></a><span data-ttu-id="47b92-103">Connection Manager (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="47b92-103">Connection Manager (Hosted Control)</span></span>
<span data-ttu-id="47b92-104">The **Connection Manager** hosted control type manages connections to the Dynamics 365 for Customer Engagement server, and makes it available to the rest of the agent application.</span><span class="sxs-lookup"><span data-stu-id="47b92-104">The **Connection Manager** hosted control type manages connections to the Dynamics 365 for Customer Engagement server, and makes it available to the rest of the agent application.</span></span> <span data-ttu-id="47b92-105">Một phiên bản của kiểm soát tổ chức này được yêu cầu bởi [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], và chỉ một phiên bản loại kiểm soát tổ chức đơn này mới tồn tại trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="47b92-105">An instance of this hosted control is required by [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], and only a single instance of this hosted control type must exist in your agent application.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="47b92-106">The three sample application packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], `New Environment`, `CRM Web Client`, and `Interactive Service Hub`, come preconfigured with an instance each of the **Connection Manager** hosted control type.</span><span class="sxs-lookup"><span data-stu-id="47b92-106">The three sample application packages for [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], `New Environment`, `CRM Web Client`, and `Interactive Service Hub`, come preconfigured with an instance each of the **Connection Manager** hosted control type.</span></span> <span data-ttu-id="47b92-107">For information about the sample applications, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).</span><span class="sxs-lookup"><span data-stu-id="47b92-107">For information about the sample applications, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="47b92-108">In This Section</span><span class="sxs-lookup"><span data-stu-id="47b92-108">In This Section</span></span>  
 [<span data-ttu-id="47b92-109">Tạo kiểm soát tổ chức Trình quản lý kết nối</span><span class="sxs-lookup"><span data-stu-id="47b92-109">Create a Connection Manager hosted control</span></span>](../unified-service-desk/connection-manager-hosted-control.md#create)  
  
 [<span data-ttu-id="47b92-110">Thao tác UII được xác định trước</span><span class="sxs-lookup"><span data-stu-id="47b92-110">Predefined UII actions</span></span>](../unified-service-desk/connection-manager-hosted-control.md#UIIactions)  
  
 [<span data-ttu-id="47b92-111">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="47b92-111">Predefined UII actions</span></span>](../unified-service-desk/connection-manager-hosted-control.md#UIIactions)  
  
<a name="create"></a>   
## <a name="create-a-connection-manager-hosted-control"></a><span data-ttu-id="47b92-112">Tạo kiểm soát tổ chức Trình quản lý kết nối</span><span class="sxs-lookup"><span data-stu-id="47b92-112">Create a Connection Manager hosted control</span></span>  
 <span data-ttu-id="47b92-113">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span><span class="sxs-lookup"><span data-stu-id="47b92-113">While creating a new hosted control, the fields in the **New Hosted Control** screen vary based on the type of hosted control you want to create.</span></span> <span data-ttu-id="47b92-114">Phần này cung cấp thông tin về các trường cụ thể mà là duy nhất cho loại kiểm soát tổ chức **Trình quản lý kết nối**.</span><span class="sxs-lookup"><span data-stu-id="47b92-114">This section provides information about the specific fields that are unique to the **Connection Manager** hosted control type.</span></span> <span data-ttu-id="47b92-115">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="47b92-115">For detailed information about creating a hosted control, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
 <span data-ttu-id="47b92-116">![Connection manager hosted control](../unified-service-desk/media/crm-itpro-usd-connectionmanagerhostedcontrol.PNG "Connection manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="47b92-116">![Connection manager hosted control](../unified-service-desk/media/crm-itpro-usd-connectionmanagerhostedcontrol.PNG "Connection manager hosted control")</span></span>  
  
 <span data-ttu-id="47b92-117">Trong màn hình **Kiểm soát tổ chức mới**, dưới khu vực **Unified Service Desk**, chọn **trình quản lý kết nối** từ danh sách thả xuống **Loại Thành phần USD**.</span><span class="sxs-lookup"><span data-stu-id="47b92-117">In the **New Hosted Control** screen, under the **Unified Service Desk** area, select **Connection Manager** from the **USD Component Type** drop-down list.</span></span> <span data-ttu-id="47b92-118">Ngoài ra, đảm bảo rằng bạn đặt giá trị **thứ tự sắp xếp** của kiểm soát tổ chức thành **1** để đảm bảo đây là kiểm soát tổ chức đầu tiên được trích xuất và hiển thị bằng ứng dụng tổng đài viên của bạn khi ứng dụng tổng đài viên được khởi chạy.</span><span class="sxs-lookup"><span data-stu-id="47b92-118">Also, ensure that you set the **Sort Order** value of this hosted control to **1** to ensure this is the first hosted control to be retrieved and displayed by your agent application when the agent application is launched.</span></span> <span data-ttu-id="47b92-119">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="47b92-119">For information about other **General** fields, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  
  
<a name="UIIactions"></a>   
## <a name="predefined-uii-actions"></a><span data-ttu-id="47b92-120">Predefined UII actions</span><span class="sxs-lookup"><span data-stu-id="47b92-120">Predefined UII actions</span></span>  
 <span data-ttu-id="47b92-121">Loại kiểm soát tổ chức này không có bất kỳ hoạt động UII được xác định trước nào.</span><span class="sxs-lookup"><span data-stu-id="47b92-121">This hosted control type does not have any predefined UII actions.</span></span>  
  
<a name="events"></a>   
## <a name="predefined-events"></a><span data-ttu-id="47b92-122">Sự kiện được xác định trước</span><span class="sxs-lookup"><span data-stu-id="47b92-122">Predefined events</span></span>  
 <span data-ttu-id="47b92-123">Loại kiểm soát tổ chức này không có bất kỳ sự kiện được xác định trước nào.</span><span class="sxs-lookup"><span data-stu-id="47b92-123">This hosted control type does not have any predefined events.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="47b92-124">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="47b92-124">See also</span></span>  
 <span data-ttu-id="47b92-125">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="47b92-125">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 <span data-ttu-id="47b92-126">[Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="47b92-126">[Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md) </span></span>  
 <span data-ttu-id="47b92-127">[Unified Service Desk Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md) </span><span class="sxs-lookup"><span data-stu-id="47b92-127">[Unified Service Desk Hosted Controls](../unified-service-desk/unified-service-desk-hosted-controls.md) </span></span>  
 [<span data-ttu-id="47b92-128">Walkthrough 1: Build a simple agent application</span><span class="sxs-lookup"><span data-stu-id="47b92-128">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)
