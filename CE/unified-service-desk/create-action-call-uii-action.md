---
title: Create an action call for a UII action | MicrosoftDocs
description: Learn about creating an action call for a UII action.
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
ms.assetid: 5b8bac46-075e-4ad7-864f-a3a08ca8c743
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
ms.openlocfilehash: 9ac7b9915c9036b223f2347621b04b0875ced08c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385789"
---
# <a name="create-an-action-call-for-a-uii-action-in-unified-service-desk"></a><span data-ttu-id="91e0f-103">Create an action call for a UII action in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="91e0f-103">Create an action call for a UII action in Unified Service Desk</span></span>
<span data-ttu-id="91e0f-104">Có hai cách mà bạn có thể tạo cuộc gọi hành động cho một hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)]:</span><span class="sxs-lookup"><span data-stu-id="91e0f-104">There are two ways in which you can create an action call for a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] action:</span></span>  

-   <span data-ttu-id="91e0f-105">Tạo một cuộc gọi hành động và sau đó đính kèm nó vào kiểm soát tổ chức và hành động UII tương ứng.</span><span class="sxs-lookup"><span data-stu-id="91e0f-105">Create an action call and then attach it to the hosted control and the respective UII action.</span></span>  

-   <span data-ttu-id="91e0f-106">Bắt đầu từ kiểm soát tổ chức chứa hành động UII mà bạn muốn tạo cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-106">Start from a hosted control that contains the UII action that you want to create the action call for.</span></span>  

<a name="StartActionCall"></a>   
## <a name="start-from-the-action-call"></a><span data-ttu-id="91e0f-107">Bắt đầu từ cuộc gọi hành động</span><span class="sxs-lookup"><span data-stu-id="91e0f-107">Start from the action call</span></span>  

1. <span data-ttu-id="91e0f-108">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="91e0f-108">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="91e0f-109">Click **Action Calls**.</span><span class="sxs-lookup"><span data-stu-id="91e0f-109">Click **Action Calls**.</span></span>  

4. <span data-ttu-id="91e0f-110">Trên trang danh sách cuộc gọi hành động, chọn **Thêm Cuộc gọi Hành động Mới** trên thanh lệnh.</span><span class="sxs-lookup"><span data-stu-id="91e0f-110">On the action call list page, choose **Add New Action Call** on the command bar.</span></span>  

5. <span data-ttu-id="91e0f-111">Trên trang **Cuộc gọi Hành động Mới**, chỉ định thông tin cho các trường khác nhau theo bảng sau.</span><span class="sxs-lookup"><span data-stu-id="91e0f-111">On the **New Action Call** page, specify information for various fields as per the following table.</span></span>  

   <span data-ttu-id="91e0f-112">![New action call in Unified Service Desk](../unified-service-desk/media/usd-new-action-call.png "New action call in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="91e0f-112">![New action call in Unified Service Desk](../unified-service-desk/media/usd-new-action-call.png "New action call in Unified Service Desk")</span></span>  


   |     <span data-ttu-id="91e0f-113">Trường</span><span class="sxs-lookup"><span data-stu-id="91e0f-113">Field</span></span>      |                                                                                                                                                                                                                                                                         <span data-ttu-id="91e0f-114">Mô tả</span><span class="sxs-lookup"><span data-stu-id="91e0f-114">Description</span></span>                                                                                                                                                                                                                                                                         |
   |----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |      <span data-ttu-id="91e0f-115">Tên</span><span class="sxs-lookup"><span data-stu-id="91e0f-115">Name</span></span>      |                                                                                                                                                                                                                                                           <span data-ttu-id="91e0f-116">Tên mô tả của cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-116">A descriptive name of the action call.</span></span>                                                                                                                                                                                                                                                            |
   | <span data-ttu-id="91e0f-117">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="91e0f-117">Hosted Control</span></span> |                                                                                                                                                                                                                                                   <span data-ttu-id="91e0f-118">Kiểm soát tổ chức có hành động UII được gọi.</span><span class="sxs-lookup"><span data-stu-id="91e0f-118">The hosted control having the UII action to be called.</span></span>                                                                                                                                                                                                                                                    |
   |     <span data-ttu-id="91e0f-119">Hành động</span><span class="sxs-lookup"><span data-stu-id="91e0f-119">Action</span></span>     |                                                                                                                                                                                   <span data-ttu-id="91e0f-120">Tên hành động UII để gọi trên kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="91e0f-120">The UII action name to call on the hosted control.</span></span> <span data-ttu-id="91e0f-121">To call a UII action for a hosted control, the action must be added to the list of UII actions for a hosted control in Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="91e0f-121">To call a UII action for a hosted control, the action must be added to the list of UII actions for a hosted control in Dynamics 365 for Customer Engagement apps.</span></span>                                                                                                                                                                                   |
   |      <span data-ttu-id="91e0f-122">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="91e0f-122">Data</span></span>      |                                                                                                                                                                                   <span data-ttu-id="91e0f-123">Đây là dữ liệu được đăng (chuỗi dữ liệu) được thông qua dưới dạng tham số dữ liệu vào hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-123">This is the serialized data (string data) that is passed as the data parameter to the action.</span></span> <span data-ttu-id="91e0f-124">**Note:**  Some actions interpret multiline input specified here as separate parameters.</span><span class="sxs-lookup"><span data-stu-id="91e0f-124">**Note:**  Some actions interpret multiline input specified here as separate parameters.</span></span>                                                                                                                                                                                    |
   |   <span data-ttu-id="91e0f-125">Điều kiện</span><span class="sxs-lookup"><span data-stu-id="91e0f-125">Condition</span></span>    |              <span data-ttu-id="91e0f-126">Đây là một biểu thức [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] phải dẫn đến đúng hoặc sai.</span><span class="sxs-lookup"><span data-stu-id="91e0f-126">This is a [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)] expression that should result in true or false.</span></span> <span data-ttu-id="91e0f-127">Ví dụ, "[[account.name]]"=="Tài khoản của tôi"</span><span class="sxs-lookup"><span data-stu-id="91e0f-127">For example, “[[account.name]]”==”My Account”</span></span><br /><br /> <span data-ttu-id="91e0f-128">Nếu điều kiện dẫn đến sai hoặc đặt ra trường hợp ngoại lệ, các hành động sẽ không được thực hiện.</span><span class="sxs-lookup"><span data-stu-id="91e0f-128">If the condition results in false or throws an exception, the action won’t be performed.</span></span> <span data-ttu-id="91e0f-129">Nếu các hành động là trống hoặc kết quả là đúng, những hành động sẽ được thực hiện.</span><span class="sxs-lookup"><span data-stu-id="91e0f-129">If the action is blank or the result is true, the action will be performed.</span></span> <span data-ttu-id="91e0f-130">**Note:**  If the condition results in false or throws an exception, the action won’t be performed.</span><span class="sxs-lookup"><span data-stu-id="91e0f-130">**Note:**  If the condition results in false or throws an exception, the action won’t be performed.</span></span> <span data-ttu-id="91e0f-131">Nếu các hành động là trống hoặc kết quả là đúng, những hành động sẽ được thực hiện.</span><span class="sxs-lookup"><span data-stu-id="91e0f-131">If the action is blank or the result is true, the action will be performed.</span></span>               |
   |  <span data-ttu-id="91e0f-132">Phím tắt</span><span class="sxs-lookup"><span data-stu-id="91e0f-132">Shortcut Key</span></span>  | <span data-ttu-id="91e0f-133">Đây là một phím tắt có thể được sử dụng bởi một tổng đài viên để chạy hành động này trong ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="91e0f-133">This is a shortcut key that can be used by an agent to run this action while within the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="91e0f-134">Có thể sử dụng mọi mục hợp lệ cho chuỗi `KeyBinding.Gesture` tại đây.</span><span class="sxs-lookup"><span data-stu-id="91e0f-134">Anything valid for the `KeyBinding.Gesture` string can be used here.</span></span> <span data-ttu-id="91e0f-135">For more information see: [http://msdn.microsoft.com/en-us/library/system.windows.input.keybinding.gesture.aspx](https://msdn.microsoft.com/library/system.windows.input.keybinding.gesture.aspx).</span><span class="sxs-lookup"><span data-stu-id="91e0f-135">For more information see: [http://msdn.microsoft.com/en-us/library/system.windows.input.keybinding.gesture.aspx](https://msdn.microsoft.com/library/system.windows.input.keybinding.gesture.aspx).</span></span><br /><br /> <span data-ttu-id="91e0f-136">Ví dụ:</span><span class="sxs-lookup"><span data-stu-id="91e0f-136">Examples:</span></span><br /><br /> <span data-ttu-id="91e0f-137">-   CTRL+R</span><span class="sxs-lookup"><span data-stu-id="91e0f-137">-   CTRL+R</span></span><br /><span data-ttu-id="91e0f-138">-   CTRL+ALT+A</span><span class="sxs-lookup"><span data-stu-id="91e0f-138">-   CTRL+ALT+A</span></span><br /><span data-ttu-id="91e0f-139">-   SHIFT+ALT+A</span><span class="sxs-lookup"><span data-stu-id="91e0f-139">-   SHIFT+ALT+A</span></span><br /><span data-ttu-id="91e0f-140">-   CTRL-F12</span><span class="sxs-lookup"><span data-stu-id="91e0f-140">-   CTRL-F12</span></span> |

   > [!TIP]
   >  <span data-ttu-id="91e0f-141">Bạn có thể xem trợ giúp nhúng ở cuối trang **Cuộc gọi hành động mới** để biết mô tả và thông số áp dụng có thể được thông qua sử dụng cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-141">You can view the embedded help at the bottom of the **New Action Call** page to know the description and the applicable parameters that can be passed using the action call.</span></span>  

6. <span data-ttu-id="91e0f-142">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="91e0f-142">Choose **Save**.</span></span>  

<a name="StartHostedControl"></a>   
## <a name="start-from-the-hosted-control"></a><span data-ttu-id="91e0f-143">Bắt đầu từ kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="91e0f-143">Start from the hosted control</span></span>  

1. <span data-ttu-id="91e0f-144">Tạo hoặc chỉnh sửa kiểm soát tổ chức có hành động UII mà bạn muốn tạo cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-144">Create or edit the hosted control that contains the UII action that you want to create an action call for.</span></span> <span data-ttu-id="91e0f-145">For more information, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span><span class="sxs-lookup"><span data-stu-id="91e0f-145">For more information, see [Create or edit a hosted control](../unified-service-desk/create-edit-hosted-control.md).</span></span>  

2. <span data-ttu-id="91e0f-146">Trên trang kiểm soát tổ chức, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức trên thanh điều hướng, sau đó chọn Hành động UII.</span><span class="sxs-lookup"><span data-stu-id="91e0f-146">On the hosted control page, choose the down arrow next to the hosted control name on the nav bar, and then choose UII Actions.</span></span>  

   <span data-ttu-id="91e0f-147">![Navigation to UII Actions for a hosted control](../unified-service-desk/media/usd-uii-actions-hosted-control.png "Navigation to UII Actions for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="91e0f-147">![Navigation to UII Actions for a hosted control](../unified-service-desk/media/usd-uii-actions-hosted-control.png "Navigation to UII Actions for a hosted control")</span></span>  

3. <span data-ttu-id="91e0f-148">Từ danh sách hành động UII, chọn tên của hành động UII trong cột **Tên** mà bạn muốn thêm cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="91e0f-148">From the UII action list, choose the name of the UII action in the **Name** column for which you want to add the action call.</span></span> <span data-ttu-id="91e0f-149">Ngoài ra, chọn hồ sơ hành động UII theo yêu cầu, sau đó chọn **Chỉnh sửa** ở thanh lệnh.</span><span class="sxs-lookup"><span data-stu-id="91e0f-149">Alternatively, select the required UII action record, and then choose **Edit** in the command bar.</span></span> <span data-ttu-id="91e0f-150">Thao tác này sẽ mở hồ sơ hành động UII.</span><span class="sxs-lookup"><span data-stu-id="91e0f-150">This will open the UII action record.</span></span>  

4. <span data-ttu-id="91e0f-151">Trên trang hành động UII, chọn mũi tên xuống bên cạnh tên hành động UII trên thanh điều hướng, rồi chọn **Cuộc gọi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="91e0f-151">On the UII action page, choose the down arrow next to the UII action name on the nav bar, and then choose **Action Calls**.</span></span>  

   <span data-ttu-id="91e0f-152">![Menu navigation to create an action call](../unified-service-desk/media/usd-action-call-uii-action.png "Menu navigation to create an action call")</span><span class="sxs-lookup"><span data-stu-id="91e0f-152">![Menu navigation to create an action call](../unified-service-desk/media/usd-action-call-uii-action.png "Menu navigation to create an action call")</span></span>  

5. <span data-ttu-id="91e0f-153">On the action call list page, choose **Add New Action Call** on the command bar.</span><span class="sxs-lookup"><span data-stu-id="91e0f-153">On the action call list page, choose **Add New Action Call** on the command bar.</span></span>  

6. <span data-ttu-id="91e0f-154">Trên trang **Cuộc gọi hành động mới**, làm theo bước 5 và 6 trong phần trước.</span><span class="sxs-lookup"><span data-stu-id="91e0f-154">On the **New Action Call** page, follows steps 5 and 6 in the previous section.</span></span>  

### <a name="see-also"></a><span data-ttu-id="91e0f-155">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="91e0f-155">See also</span></span>  
 <span data-ttu-id="91e0f-156">[Quản lý kiểm soát tổ chức, hành động và sự kiện](../unified-service-desk/manage-hosted-controls-actions-events.md) </span><span class="sxs-lookup"><span data-stu-id="91e0f-156">[Manage hosted controls, actions, and events](../unified-service-desk/manage-hosted-controls-actions-events.md) </span></span>  
 [<span data-ttu-id="91e0f-157">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="91e0f-157">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)  

