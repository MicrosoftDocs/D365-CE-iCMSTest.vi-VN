---
title: Configure session information | MicrosoftDocs
description: Learn about configuring session information.
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
ms.assetid: 574034ed-82c1-4db4-ac64-786591397e74
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
ms.openlocfilehash: c2d953516beb9e70331ca47bf7b83339ca72c037
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385493"
---
# <a name="configure-session-information"></a><span data-ttu-id="5b23f-103">Configure session information</span><span class="sxs-lookup"><span data-stu-id="5b23f-103">Configure session information</span></span>
<span data-ttu-id="5b23f-104">Thông tin phiên sẽ được hiển thị dưới tab trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] theo hai vùng: tên tab phiên và tổng quan về phiên.</span><span class="sxs-lookup"><span data-stu-id="5b23f-104">The session information is displayed under tabs in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] under two areas: session tab name and session overview.</span></span> <span data-ttu-id="5b23f-105">For an overview about this, see [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="5b23f-105">For an overview about this, see [Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md).</span></span> <span data-ttu-id="5b23f-106">Bạn có thể đặt cấu hình định dạng thông tin hiển thị như tên tab phiên và tổng quan bằng cách tạo nguyên tắc dòng phiên phù hợp.</span><span class="sxs-lookup"><span data-stu-id="5b23f-106">You can configure the format of the information that displays as the session tab name and overview by creating appropriate session line rules.</span></span>  
  
<a name="SessionName"></a>   
## <a name="configure-the-session-tab-name-format"></a><span data-ttu-id="5b23f-107">Đặt cấu hình định dạng tên tab phiên</span><span class="sxs-lookup"><span data-stu-id="5b23f-107">Configure the session tab name format</span></span>  
  
1. <span data-ttu-id="5b23f-108">Đăng nhập vào ứng dụng [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)].</span><span class="sxs-lookup"><span data-stu-id="5b23f-108">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="5b23f-109">Click **Session Lines**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-109">Click **Session Lines**.</span></span>  
  
4. <span data-ttu-id="5b23f-110">Trên trang **Thông tin phiên mới**:</span><span class="sxs-lookup"><span data-stu-id="5b23f-110">On new **New Session Information** page:</span></span>  
  
   1.  <span data-ttu-id="5b23f-111">Nhập giá trị số nguyên (nói 100) trong trường **Thứ tự** để bảo rằng quy tắc của bạn thực hiện theo thứ tự đúng.</span><span class="sxs-lookup"><span data-stu-id="5b23f-111">Type an integer value (say 100) in the **Order** field to ensure that your rule executes in the proper order.</span></span>  
  
   2.  <span data-ttu-id="5b23f-112">Nhập tên có nghĩa trong trường **Tên**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-112">Type a meaningful name in the **Name** field.</span></span>  
  
   3.  <span data-ttu-id="5b23f-113">Trong trường **Thực thể được chọn**, nhập tên thực thể mà tab phiên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5b23f-113">In the **Selected Entity** field, type the name of the entity for which the session tab will be displayed.</span></span>  
  
   4.  <span data-ttu-id="5b23f-114">Từ danh sách thả xuống **Loại**, chọn **Tên phiên**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-114">From the **Type** drop-down list, select **Session Name**.</span></span>  
  
   5.  <span data-ttu-id="5b23f-115">In the **Display** field, type the display format for the tab. In this case, we want to display the name of the account followed by a dash, and then the primary contact name for the account.</span><span class="sxs-lookup"><span data-stu-id="5b23f-115">In the **Display** field, type the display format for the tab. In this case, we want to display the name of the account followed by a dash, and then the primary contact name for the account.</span></span> <span data-ttu-id="5b23f-116">Nhập giá trị sau: [[account.name]]-[[account.address1_primarycontactname]].</span><span class="sxs-lookup"><span data-stu-id="5b23f-116">Type the following value: [[account.name]]-[[account.address1_primarycontactname]].</span></span>  
  
   <span data-ttu-id="5b23f-117">![Configure session tab name](../unified-service-desk/media/usd-configure-session-name.png "Configure session tab name")</span><span class="sxs-lookup"><span data-stu-id="5b23f-117">![Configure session tab name](../unified-service-desk/media/usd-configure-session-name.png "Configure session tab name")</span></span>  
  
        Alternatively, you can use replacement parameters as well to pick up values at runtime, and dynamically display the tab name. For example, to display the name of the account followed by a dash and ending with the name of the activity that started the session (such as chat, or phonecall). Type the following value: [[account.name]]-[[$Context.InitialEntity]].  
  
       > [!NOTE]
       >  If all replacement values have matching values in it’s dataset, the rule will be used and the system will stop looking for subsequent rules. If one or more replacement values can’t be replaced, because the data doesn’t exist, the rule will fail and the system will try the next rule ordering to the Order field (checked in order of lowest to highest).  
  
        In the preceding example, [[account.name]] will be looking for the name field from an account entity that has been loaded somewhere within the current session. Because we used the lowercased version of “account” that matches to the entity name in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, it means that it is looking for the last account page loaded no matter which tab it happens to be loaded within. Because of this, if you load a subaccount and your rules have it loading in a subaccount tab (thus displaying your primary account in the Account tab, and your subaccount in your Sub Account tab), the account name that will be used will be that of the sub account. This is because the subaccount is loaded after the Account tab. If you instead wish to always use the account name of the account that is displayed in the Account tab, you would use the following: **[[Account.name]]**.  
  
        The [[$Context.InitialEntity]] value is replaced at runtime with the InitialEntity context variable. This is a special context variable populated by the system with the entity name that is used to start the session.  
  
5. <span data-ttu-id="5b23f-118">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-118">Click **Save**.</span></span>  
  
<a name="SessionOverview"></a>   
## <a name="define-session-overview-information"></a><span data-ttu-id="5b23f-119">Define session overview information</span><span class="sxs-lookup"><span data-stu-id="5b23f-119">Define session overview information</span></span>  
  
1. <span data-ttu-id="5b23f-120">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="5b23f-120">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="5b23f-121">Click **Session Lines**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-121">Click **Session Lines**.</span></span>  
  
4. <span data-ttu-id="5b23f-122">Trên trang **Thông tin phiên mới**,</span><span class="sxs-lookup"><span data-stu-id="5b23f-122">On **New Session Information** page,</span></span>  
  
   1. <span data-ttu-id="5b23f-123">Type an integer value (say 100) in the **Order** field to ensure that your rule executes in the proper order.</span><span class="sxs-lookup"><span data-stu-id="5b23f-123">Type an integer value (say 100) in the **Order** field to ensure that your rule executes in the proper order.</span></span>  
  
   2. <span data-ttu-id="5b23f-124">Nhập tên có nghĩa trong trường **Tên**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-124">Type a meaningful name in the **Name** field.</span></span>  
  
   3. <span data-ttu-id="5b23f-125">Trong trường **Thực thể được chọn**, nhập tên thực thể mà thông tin tổng quan phiên sẽ được hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5b23f-125">In the **Selected Entity** field, type the name of the entity for which the session overview information.</span></span>  
  
   4. <span data-ttu-id="5b23f-126">Từ danh sách thả xuống **Loại**, chọn **Dòng tổng quan về phiên**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-126">From the **Type** drop-down list, select **Session Overview Line**.</span></span>  
  
   5. <span data-ttu-id="5b23f-127">In the **Display** field, specify XAML script that defines the layout and content of the overview area.</span><span class="sxs-lookup"><span data-stu-id="5b23f-127">In the **Display** field, specify XAML script that defines the layout and content of the overview area.</span></span> <span data-ttu-id="5b23f-128">You can use designer tools such as [!INCLUDE[pn_blend_for_visual_studio](../includes/pn-blend-for-visual-studio.md)] to create and design the XAML script, and then copy it in this field.</span><span class="sxs-lookup"><span data-stu-id="5b23f-128">You can use designer tools such as [!INCLUDE[pn_blend_for_visual_studio](../includes/pn-blend-for-visual-studio.md)] to create and design the XAML script, and then copy it in this field.</span></span> <span data-ttu-id="5b23f-129">The XAML script must be properly formatted for it to display correctly in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="5b23f-129">The XAML script must be properly formatted for it to display correctly in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   <span data-ttu-id="5b23f-130">![Configure session overview](../unified-service-desk/media/usd-configure-session-overview.png "Configure session overview")</span><span class="sxs-lookup"><span data-stu-id="5b23f-130">![Configure session overview](../unified-service-desk/media/usd-configure-session-overview.png "Configure session overview")</span></span>  
  
5. <span data-ttu-id="5b23f-131">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="5b23f-131">Click **Save**.</span></span>  
  
<a name="scriptlet"></a>   
## <a name="define-session-overview-information-using-scriptlets"></a><span data-ttu-id="5b23f-132">Xác định thông tin tổng quan phiên sử dụng Scriptlet</span><span class="sxs-lookup"><span data-stu-id="5b23f-132">Define session overview information using scriptlets</span></span>  
 <span data-ttu-id="5b23f-133">Với những nhà phát triển đã quen với [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], bạn có thể sử dụng Scriptlet để hiển thị thông tin tổng quan phiên.</span><span class="sxs-lookup"><span data-stu-id="5b23f-133">For developers who are familiar with [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], you can use scriptlets to display session overview information.</span></span> <span data-ttu-id="5b23f-134">Ví dụ:.</span><span class="sxs-lookup"><span data-stu-id="5b23f-134">For example:</span></span>  
  
1. <span data-ttu-id="5b23f-135">Bạn có thể tạo scriptlet, cho biết **Đầu ra địa chỉ**, mà chấp nhận tất cả các giá trị địa chỉ.</span><span class="sxs-lookup"><span data-stu-id="5b23f-135">You could create a scriptlet, say **Address Output**, which accepts all the address values.</span></span>  
  
2. <span data-ttu-id="5b23f-136">Bằng cách sử dụng [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], bạn có thể sử dụng các chức năng chuỗi để thực hiện nối chuỗi để tạo đầu ra mong muốn.</span><span class="sxs-lookup"><span data-stu-id="5b23f-136">Using [!INCLUDE[pn_JavaScript](../includes/pn-javascript.md)], you could use the string functions to perform the string concatenation to produce the desired output.</span></span>  
  
3. <span data-ttu-id="5b23f-137">In your XAML for the session overview information definition, use the following replacement parameter:</span><span class="sxs-lookup"><span data-stu-id="5b23f-137">In your XAML for the session overview information definition, use the following replacement parameter:</span></span>  
  
   ```  
   [[script.Address Output]]  
   ```  
  
   <span data-ttu-id="5b23f-138">Tại thời gian chạy, điều này khởi động việc thực hiện scriptlet mà định dạng đầu ra địa chỉ như bạn đã chỉ định.</span><span class="sxs-lookup"><span data-stu-id="5b23f-138">At runtime, this triggers the execution of the scriptlet that formats the address output as you specified.</span></span> <span data-ttu-id="5b23f-139">Nếu scriptlet của bạn là một ngoại lệ, các quy tắc sẽ được bỏ qua.</span><span class="sxs-lookup"><span data-stu-id="5b23f-139">If your scriptlet throws an exception, the rule will be ignored.</span></span> <span data-ttu-id="5b23f-140">Phương pháp này thường là phương pháp ưa thích khi kiểu `AutoCollapse` là chưa đủ để ẩn các đánh dấu liên quan trong đầu ra theo yêu cầu.</span><span class="sxs-lookup"><span data-stu-id="5b23f-140">This method is often the preferred method when the `AutoCollapse` style isn’t sufficient to hide related markup in the output as required.</span></span> <span data-ttu-id="5b23f-141">The replacement parameter may output XAML as well, which will be substituted before the XAML processor interprets the final result.</span><span class="sxs-lookup"><span data-stu-id="5b23f-141">The replacement parameter may output XAML as well, which will be substituted before the XAML processor interprets the final result.</span></span>  
  
<a name="Alerts"></a>   
## <a name="displaying-alerts-in-the-session-overview-information"></a><span data-ttu-id="5b23f-142">Hiển thị cảnh báo trong thông tin tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="5b23f-142">Displaying alerts in the session overview information</span></span>  
 <span data-ttu-id="5b23f-143">Cảnh báo là thông báo cho người dùng về thông tin quan trọng liên quan đến khách hàng.</span><span class="sxs-lookup"><span data-stu-id="5b23f-143">Alerts are notifications to the user about important information related to the customer.</span></span> <span data-ttu-id="5b23f-144">Một hệ thống cảnh báo cơ bản được tích hợp vào cơ chế thông tin phiên.</span><span class="sxs-lookup"><span data-stu-id="5b23f-144">A basic alerting system is built into the session information mechanism.</span></span> <span data-ttu-id="5b23f-145">Dòng phiên được đánh giá và hiển thị khi tất cả các tham số thay thế đã được thay thế và không có ngoại lệ từ Scriptlet.</span><span class="sxs-lookup"><span data-stu-id="5b23f-145">Session lines are evaluated and displayed when the replacement parameters are all replaced and no exceptions are thrown from scriptlets.</span></span> <span data-ttu-id="5b23f-146">Sử dụng thông tin này, bạn có thể hiển thị dòng đầu ra tùy chọn trong vùng thông tin tổng quan về phiên của màn hình dựa trên sự tồn tại hoặc lựa chọn thực thể hoặc giá trị tìm kiếm thực thể.</span><span class="sxs-lookup"><span data-stu-id="5b23f-146">Using this information, you can display optional lines of output in the session overview area of the screen based upon the existence or selections on entities or entity search values.</span></span> <span data-ttu-id="5b23f-147">Sau đó sử dụng Scriptlet để kiểm tra giá trị cụ thể, và trả về một giá trị nếu bạn muốn hiển thị cảnh báo hoặc thêm ngoại lệ nếu bạn không muốn hiển thị.</span><span class="sxs-lookup"><span data-stu-id="5b23f-147">Then use scriptlets to test for specific values, and return a value if you want the alert to display, or throw an exception if you do not.</span></span>  
  
 <span data-ttu-id="5b23f-148">Đây là một scriptlet ví dụ kiểm tra để xem nếu tài khoản đã tải có được tin cậy không.</span><span class="sxs-lookup"><span data-stu-id="5b23f-148">Here is an example scriptlet that checks to see if the loaded account has its credit on hold.</span></span>  
  
 <span data-ttu-id="5b23f-149">![Example scriptlet in Unified Service Desk](../unified-service-desk/media/usd-sample-scriptlet.png "Example scriptlet in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="5b23f-149">![Example scriptlet in Unified Service Desk](../unified-service-desk/media/usd-sample-scriptlet.png "Example scriptlet in Unified Service Desk")</span></span>  
  
 <span data-ttu-id="5b23f-150">Nhận thấy rằng thuộc tính `creditonhold` đã được chọn cho tài khoản.</span><span class="sxs-lookup"><span data-stu-id="5b23f-150">Notice that the `creditonhold` property is checked for the account.</span></span> <span data-ttu-id="5b23f-151">Nếu giá trị là `true`, giá trị sẽ trả về `true`, nếu không hãy đưa ra ngoại lệ.</span><span class="sxs-lookup"><span data-stu-id="5b23f-151">If the value is `true`, it returns `true`, otherwise it throws an exception.</span></span> <span data-ttu-id="5b23f-152">Tiếp theo dưới đây là dòng tổng quan về phiên mà hiển thị hộp văn bản và nút (thông báo của tôi) nếu giá trị là `true`.</span><span class="sxs-lookup"><span data-stu-id="5b23f-152">Next here is a session overview line that displays a textbox and button (my alert) if the value is `true`.</span></span>  
  
 <span data-ttu-id="5b23f-153">![Display alerts in Unified Service Desk](../unified-service-desk/media/usd-sample-session-information.png "Display alerts in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="5b23f-153">![Display alerts in Unified Service Desk](../unified-service-desk/media/usd-sample-session-information.png "Display alerts in Unified Service Desk")</span></span>  
  
 <span data-ttu-id="5b23f-154">Chú ý lệnh được đánh dấu.</span><span class="sxs-lookup"><span data-stu-id="5b23f-154">Notice the highlighted command.</span></span> <span data-ttu-id="5b23f-155">Lệnh này trên cột mà không hiển thị cho người dùng.</span><span class="sxs-lookup"><span data-stu-id="5b23f-155">This is on a column that isn’t visible to the user.</span></span> <span data-ttu-id="5b23f-156">Thay vào đó tham số thay thế ở đây sẽ làm hiển thị hoặc bỏ qua dòng tổng quan phiên này.</span><span class="sxs-lookup"><span data-stu-id="5b23f-156">Instead the replacement parameter here will either cause this session overview line to display or cause it to be skipped.</span></span> <span data-ttu-id="5b23f-157">Nếu scriptlet Đúng về khả năng tin cậy là ngoại lệ, Hệ thống sẽ không hiển thị bất kỳ nguyên tố thông tin phiên nào.</span><span class="sxs-lookup"><span data-stu-id="5b23f-157">If the Credit On Hold True Check scriptlet throws the exception, the system won’t display any of this Session Information element.</span></span> <span data-ttu-id="5b23f-158">Bây giờ chúng tôi có điều kiện quyết định thời điểm cảnh báo, hãy xem nút và một số tính năng thú vị ở đây.</span><span class="sxs-lookup"><span data-stu-id="5b23f-158">Now that we have the condition that decides when to show the alert, let’s look at the button and some interesting features here.</span></span>  
  
 <span data-ttu-id="5b23f-159">Since there is no code behind for this XAML, we take advantage of another XAML feature, Commands.</span><span class="sxs-lookup"><span data-stu-id="5b23f-159">Since there is no code behind for this XAML, we take advantage of another XAML feature, Commands.</span></span> <span data-ttu-id="5b23f-160">There is a special command defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], “USD:ActionCommands.DoActionCommand”.</span><span class="sxs-lookup"><span data-stu-id="5b23f-160">There is a special command defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], “USD:ActionCommands.DoActionCommand”.</span></span> <span data-ttu-id="5b23f-161">Lệnh này được thiết kế để gọi hành động [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] trên bất kỳ ứng dụng trong phiên đang chạy tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="5b23f-161">This command is designed to call a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] action on any application within the agents currently running session.</span></span> <span data-ttu-id="5b23f-162">The CommandParameter is a URL encoded action call, with the following format.</span><span class="sxs-lookup"><span data-stu-id="5b23f-162">The CommandParameter is a URL encoded action call, with the following format.</span></span>  
  
```  
http://uii/[UII Hosted Application]/[Action]?[Parameter]  
```  
  
 <span data-ttu-id="5b23f-163">Hành động phải được cấu hình như hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho ứng dụng tổ chức[!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] được chỉ định.</span><span class="sxs-lookup"><span data-stu-id="5b23f-163">The action must be configured as a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] action for the specified [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted application.</span></span> <span data-ttu-id="5b23f-164">This button calls the GotoTask action on the AgentScripting application and passes “Welcome” as the parameter.</span><span class="sxs-lookup"><span data-stu-id="5b23f-164">This button calls the GotoTask action on the AgentScripting application and passes “Welcome” as the parameter.</span></span> <span data-ttu-id="5b23f-165">For the AgentScripting application, this call locates the task with the name, “Welcome” and jumps to that task, thus displaying a new agent script.</span><span class="sxs-lookup"><span data-stu-id="5b23f-165">For the AgentScripting application, this call locates the task with the name, “Welcome” and jumps to that task, thus displaying a new agent script.</span></span>  
  
 <span data-ttu-id="5b23f-166">The image source uses a special image loader defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] called CRMImageLoader and must be defined in the Grid resources.</span><span class="sxs-lookup"><span data-stu-id="5b23f-166">The image source uses a special image loader defined in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] called CRMImageLoader and must be defined in the Grid resources.</span></span>  
  
 <span data-ttu-id="5b23f-167">Bây giờ khi bạn chỉ định một biểu thức ràng buộc, bạn có thể chỉ định nguồn như là tên nguồn tài nguyên ảnh.</span><span class="sxs-lookup"><span data-stu-id="5b23f-167">Now when you specify a binding expression, you can specify the source as an image resource name.</span></span> <span data-ttu-id="5b23f-168">This causes [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to load the image from the web resources in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps and show in the button.</span><span class="sxs-lookup"><span data-stu-id="5b23f-168">This causes [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to load the image from the web resources in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps and show in the button.</span></span> <span data-ttu-id="5b23f-169">Using this method, you can refer to resources from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps in your [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] (WPF) that is in your session overview.</span><span class="sxs-lookup"><span data-stu-id="5b23f-169">Using this method, you can refer to resources from [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps in your [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] (WPF) that is in your session overview.</span></span> <span data-ttu-id="5b23f-170">You may also specify an insecure URL for the image source.</span><span class="sxs-lookup"><span data-stu-id="5b23f-170">You may also specify an insecure URL for the image source.</span></span> <span data-ttu-id="5b23f-171">Specifying the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps image via the URL doesn’t work because authentication with the server is required to access it.</span><span class="sxs-lookup"><span data-stu-id="5b23f-171">Specifying the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps image via the URL doesn’t work because authentication with the server is required to access it.</span></span> <span data-ttu-id="5b23f-172">WPF components do not authenticate against the URL when it attempts to load components.</span><span class="sxs-lookup"><span data-stu-id="5b23f-172">WPF components do not authenticate against the URL when it attempts to load components.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="5b23f-173">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="5b23f-173">See also</span></span>  
 <span data-ttu-id="5b23f-174">[Quản lý phiên trong Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="5b23f-174">[Session management in Unified Service Desk](../unified-service-desk/session-management-unified-service-desk.md) </span></span>  
 <span data-ttu-id="5b23f-175">[Thực hiện mã lệnh sử dụng Scriptlet trong Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="5b23f-175">[Execute scripts using scriptlets in Unified Service Desk](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md) </span></span>  
 <span data-ttu-id="5b23f-176">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="5b23f-176">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 [<span data-ttu-id="5b23f-177">Cấu hình ứng dụng tổng đài viên của bạn bằng cách sử dụng Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="5b23f-177">Configure your agent application using Unified Service Desk</span></span>](../unified-service-desk/configure-agent-application-unified-service-desk.md)
