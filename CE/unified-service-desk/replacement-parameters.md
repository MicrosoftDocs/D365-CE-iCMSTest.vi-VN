---
title: Replacement parameters in Unified Service Desk for Dynamics 365 for Customer Engagement apps| MicrosoftDocs
description: Replacement parameters can be used throughout the application to pull data from data elements (called data parameters) captured during the execution of the application that augment and include the Unified Service Desk context.
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
ms.assetid: fbef0bd3-e118-4a5b-8568-897538972066
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
ms.openlocfilehash: 5e77062ab91601d9d2a637c4b788ebe07d0fe702
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388292"
---
# <a name="replacement-parameters-in-unified-service-desk"></a><span data-ttu-id="d188c-103">Replacement parameters in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-103">Replacement parameters in Unified Service Desk</span></span>

<span data-ttu-id="d188c-104">Tham số thay thế có thể được sử dụng trong ứng dụng để kéo dữ liệu từ phần tử dữ liệu (được gọi là tham số dữ liệu) nắm bắt được trong quá trình thực hiện ứng dụng bổ sung và bao gồm ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="d188c-104">Replacement parameters can be used throughout the application to pull data from data elements (called data parameters) captured during the execution of the application that augment and include the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context.</span></span> <span data-ttu-id="d188c-105">Bối cảnh bao gồm cặp chuỗi tên/giá trị mà thay đổi thường xuyên như dữ liệu được khám phá từ nhiều cách khác nhau trong khi sử dụng ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="d188c-105">The context consists of name/value string pairs that change frequently as data is discovered from various ways while the application is used.</span></span> <span data-ttu-id="d188c-106">Tham số thay thế được sử dụng cho một loạt các nhiệm vụ như xác định chuỗi truy vấn URL, tạo đầu ra mã lệnh trong Scriptlet, chỉ định giá trị tìm kiếm cho tìm kiếm thực thể, Tích hợp điện thoại máy tính (CTI) và xác định đầu vào cho hành động được gọi trên kiểm soát tổ chức khác.</span><span class="sxs-lookup"><span data-stu-id="d188c-106">Replacement parameters are used for a variety of tasks such as specifying URL query strings, generating script output in scriptlets, specifying search values for entity searches, Computer Telephone Integration (CTI), and specifying input for actions being called on other hosted controls.</span></span> <span data-ttu-id="d188c-107">Tham số thay thế là những yếu tố chính mà cho phép một mức độ cao của cấu hình hoặc tuỳ chỉnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] mà không cần phải sử dụng mã.</span><span class="sxs-lookup"><span data-stu-id="d188c-107">Replacement parameters are the key elements that enable a high degree of configuration or customization in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] without having to use the code.</span></span>  
  
 <span data-ttu-id="d188c-108">For information on how you can use replacement parameters to configure your agent application, see [Use replacement parameters to configure Unified Service Desk](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md).</span><span class="sxs-lookup"><span data-stu-id="d188c-108">For information on how you can use replacement parameters to configure your agent application, see [Use replacement parameters to configure Unified Service Desk](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d188c-109">Đôi khi tham số thay thế được sử dụng thay thế cho nhau với dữ liệu tham số vì tham số thay thế về cơ bản là đại diện của một tham số dữ liệu.</span><span class="sxs-lookup"><span data-stu-id="d188c-109">Sometimes replacement parameter is used interchangeably with data parameter because replacement parameter essentially is the representation of a data parameter.</span></span>  
  
<a name="ViewReplacementParameters"></a>   
## <a name="view-the-replacement-parameters-in-unified-service-desk"></a><span data-ttu-id="d188c-110">Xem tham số thay thế trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-110">View the Replacement Parameters in Unified Service Desk</span></span>  
 <span data-ttu-id="d188c-111">Kiểm soát trình gỡ lỗi trong ứng dụng khách có thể được sử dụng để xem danh sách các tham số thay thế có sẵn tại bất kỳ thời gian nhất định.</span><span class="sxs-lookup"><span data-stu-id="d188c-111">The Debugger control in the client application can be used to view the list of available replacement parameters at any given time.</span></span>  
  
1. <span data-ttu-id="d188c-112">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and log on to Microsoft Dynamics 365 for Customer Engagement apps where you have installed the sample packages.</span><span class="sxs-lookup"><span data-stu-id="d188c-112">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and log on to Microsoft Dynamics 365 for Customer Engagement apps where you have installed the sample packages.</span></span>  
  
2. <span data-ttu-id="d188c-113">Trong màn hình chính của ứng dụng [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], nhấp vào mũi tên xuống bên cạnh các bánh răng ở góc trên bên phải, và chọn **gỡ lỗi**.</span><span class="sxs-lookup"><span data-stu-id="d188c-113">In the main screen of the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, click the down arrow next to the gear on the top-right corner, and select **Debug**.</span></span> <span data-ttu-id="d188c-114">Trình gỡ lỗi xuất hiện.</span><span class="sxs-lookup"><span data-stu-id="d188c-114">The Debugger appears.</span></span>  
  
   <span data-ttu-id="d188c-115">![Debug option to open Debugger](../unified-service-desk/media/usd-view-debugger.png "Debug option to open Debugger")</span><span class="sxs-lookup"><span data-stu-id="d188c-115">![Debug option to open Debugger](../unified-service-desk/media/usd-view-debugger.png "Debug option to open Debugger")</span></span>  
  
3. <span data-ttu-id="d188c-116">Trong trình gỡ lỗi, bấm vào **Tham số dữ liệu** để xem các thông số thay thế.</span><span class="sxs-lookup"><span data-stu-id="d188c-116">In the Debugger, click **Data Parameters** to view the replacement parameters.</span></span>  
  
   <span data-ttu-id="d188c-117">![Replacement parameters on Data Parameters tab](../unified-service-desk/media/usd-replacement-parameters.PNG "Replacement parameters on Data Parameters tab")</span><span class="sxs-lookup"><span data-stu-id="d188c-117">![Replacement parameters on Data Parameters tab](../unified-service-desk/media/usd-replacement-parameters.PNG "Replacement parameters on Data Parameters tab")</span></span>  
  
   <span data-ttu-id="d188c-118">Chế độ xem dạng cây được sử dụng để đại diện cho các biến có sẵn.</span><span class="sxs-lookup"><span data-stu-id="d188c-118">A tree view is used to represent the available variables.</span></span> <span data-ttu-id="d188c-119">Khi xác định các biến, chỉ định tên ở cấp độ gốc, theo sau là dấu chấm (.), và sau đó là tên trong danh sách.</span><span class="sxs-lookup"><span data-stu-id="d188c-119">When specifying the variable, specify the name at the root level, followed by a period (.), and then the name in the list.</span></span> <span data-ttu-id="d188c-120">Dưới đây là một số ví dụ:</span><span class="sxs-lookup"><span data-stu-id="d188c-120">Here are some examples:</span></span>  
  
- `[[$Session.IsGlobal]]`  
  
- `[[$User.fullname]]`  
  
  <span data-ttu-id="d188c-121">These values will change as the user interacts in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="d188c-121">These values will change as the user interacts in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="d188c-122">Cuộc gọi hành động sẽ chọn giá trị hiện tại và sử dụng trong danh sách tham số của nó, hoặc bất cứ nơi nào khác nó có thể được sử dụng.</span><span class="sxs-lookup"><span data-stu-id="d188c-122">Action calls will pick up the current value and use in its parameter list, or wherever else it may be used.</span></span> <span data-ttu-id="d188c-123">Bất cứ lúc nào các biến được cập Nhật, sự kiện **NotifyContextChange** sẽ được hiển thị trong kiểm soát cơ sở ngay cả khi ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] không không thay đổi chính nó.</span><span class="sxs-lookup"><span data-stu-id="d188c-123">Any time the variables are updated, a **NotifyContextChange** event is fired in the base controls even if the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context didn’t change itself.</span></span> <span data-ttu-id="d188c-124">Điều này cho phép các tính năng giống như dòng phiên kiểm tra lại các giá trị của tham số thay thế để xem nếu nó cần phải cập nhật màn hình của nó không.</span><span class="sxs-lookup"><span data-stu-id="d188c-124">This allows features like the Session Lines to recheck the values of the replacement parameters to see if it needs to update its display.</span></span>  
  
<a name="SystemReplacementParameters"></a>   
## <a name="system-replacement-parameters"></a><span data-ttu-id="d188c-125">Thông số thay thế hệ thống</span><span class="sxs-lookup"><span data-stu-id="d188c-125">System Replacement Parameters</span></span>  
 <span data-ttu-id="d188c-126">Thông số thay thế hệ thống là các tham số thay thế được xác định và lưu trữ tại hệ thống, và tên bắt đầu với $ để giữ cho chúng riêng biệt với các tham số thay thế do người dùng xác định.</span><span class="sxs-lookup"><span data-stu-id="d188c-126">System replacement parameters are the replacement parameters that are defined and populated by the system, and the names start with $ to keep them separate from the user-defined replacement parameters.</span></span> <span data-ttu-id="d188c-127">Ví dụ, `$Global`.</span><span class="sxs-lookup"><span data-stu-id="d188c-127">For example, `$Global`.</span></span> [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="d188c-128">has following replacement parameters:</span><span class="sxs-lookup"><span data-stu-id="d188c-128">has following replacement parameters:</span></span>  
  
-   [<span data-ttu-id="d188c-129">$Context</span><span class="sxs-lookup"><span data-stu-id="d188c-129">$Context</span></span>](../unified-service-desk/replacement-parameters.md#Context)  
  
-   [<span data-ttu-id="d188c-130">$Debug</span><span class="sxs-lookup"><span data-stu-id="d188c-130">$Debug</span></span>](../unified-service-desk/replacement-parameters.md#Debug)  
  
-   [<span data-ttu-id="d188c-131">$Global</span><span class="sxs-lookup"><span data-stu-id="d188c-131">$Global</span></span>](../unified-service-desk/replacement-parameters.md#Global)  
  
-   [<span data-ttu-id="d188c-132">$Panel</span><span class="sxs-lookup"><span data-stu-id="d188c-132">$Panel</span></span>](../unified-service-desk/replacement-parameters.md#Panel)  
  
-   [<span data-ttu-id="d188c-133">$Resources</span><span class="sxs-lookup"><span data-stu-id="d188c-133">$Resources</span></span>](../unified-service-desk/replacement-parameters.md#Resources)  
  
-   [<span data-ttu-id="d188c-134">$Return</span><span class="sxs-lookup"><span data-stu-id="d188c-134">$Return</span></span>](../unified-service-desk/replacement-parameters.md#Return)  
  
-   [<span data-ttu-id="d188c-135">$Session</span><span class="sxs-lookup"><span data-stu-id="d188c-135">$Session</span></span>](../unified-service-desk/replacement-parameters.md#Session)  
  
-   [<span data-ttu-id="d188c-136">$Settings</span><span class="sxs-lookup"><span data-stu-id="d188c-136">$Settings</span></span>](../unified-service-desk/replacement-parameters.md#Settings)  
  
-   [<span data-ttu-id="d188c-137">$Subject</span><span class="sxs-lookup"><span data-stu-id="d188c-137">$Subject</span></span>](../unified-service-desk/replacement-parameters.md#Subject)  
  
-   [<span data-ttu-id="d188c-138">$SystemParameters</span><span class="sxs-lookup"><span data-stu-id="d188c-138">$SystemParameters</span></span>](#SystemParameters)  
  
-   [<span data-ttu-id="d188c-139">$User</span><span class="sxs-lookup"><span data-stu-id="d188c-139">$User</span></span>](../unified-service-desk/replacement-parameters.md#User)  
  
<a name="Context"></a>   
### <a name="context"></a><span data-ttu-id="d188c-140">$Context</span><span class="sxs-lookup"><span data-stu-id="d188c-140">$Context</span></span>  
 <span data-ttu-id="d188c-141">This section contains the contents of the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] session context, and provides a convenient way to use [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] session context variables throughout the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]application.</span><span class="sxs-lookup"><span data-stu-id="d188c-141">This section contains the contents of the [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] session context, and provides a convenient way to use [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] session context variables throughout the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d188c-142">The Global Manager hosted control provides an action that allows you to copy values from other replacement parameters into the context.</span><span class="sxs-lookup"><span data-stu-id="d188c-142">The Global Manager hosted control provides an action that allows you to copy values from other replacement parameters into the context.</span></span> <span data-ttu-id="d188c-143">Điều này có thể là hữu ích khi chuyển cuộc gọi hoặc lưu phiên cho quá trình phục hồi sau đó.</span><span class="sxs-lookup"><span data-stu-id="d188c-143">This can be useful when transferring calls or saving the session for rehydration later.</span></span> <span data-ttu-id="d188c-144">Bối cảnh có thể được lưu vào máy chủ trong các phiên bản này sử dụng cơ cấu UII tiêu chuẩn.</span><span class="sxs-lookup"><span data-stu-id="d188c-144">The context can be saved to the server in these instances using standard UII mechanisms.</span></span>  
  
<a name="Debug"></a>   
### <a name="debug"></a><span data-ttu-id="d188c-145">$Debug</span><span class="sxs-lookup"><span data-stu-id="d188c-145">$Debug</span></span>  
 <span data-ttu-id="d188c-146">Đây là một giá trị thay thế đặc biệt chỉ được sử dụng trong Scriptlet để xác định xem nó có được gọi bởi cửa sổ gỡ lỗi không.</span><span class="sxs-lookup"><span data-stu-id="d188c-146">This is a special replacement value used only within a Scriptlet to determine if it is being called by the debug window.</span></span> <span data-ttu-id="d188c-147">Đặc biệt là khi Scriptlet đang làm cho hành động được thực hiện trên hệ thống, chúng tôi kiểm tra tham số này để xác định xem chúng ta có nên bỏ qua việc chặn mã để tránh tác dụng phụ khi gỡ lỗi.</span><span class="sxs-lookup"><span data-stu-id="d188c-147">Particularly when scriptlets are causing actions to be performed on the system, we test this parameter to determine if we should skip the block of code to avoid side effects when debugging.</span></span> <span data-ttu-id="d188c-148">Scriptlet sau đây sẽ khởi động kiểm soát tổ chức tài khoản và hiển thị tab khi cửa sổ gỡ lỗi được mở ra.</span><span class="sxs-lookup"><span data-stu-id="d188c-148">The following scriptlet would launch the Account hosted control and display the tab when the debug window is opened.</span></span>  
  
```  
CRMGlobalManager.GetApp(“Account”);  
```  
  
 <span data-ttu-id="d188c-149">This is because the scripts are run in the current context to determine their values in the current state of the system.</span><span class="sxs-lookup"><span data-stu-id="d188c-149">This is because the scripts are run in the current context to determine their values in the current state of the system.</span></span> <span data-ttu-id="d188c-150">To avoid this side effect from occurring, do the following.</span><span class="sxs-lookup"><span data-stu-id="d188c-150">To avoid this side effect from occurring, do the following.</span></span>  
  
```  
If ([[$Debug]]!= true) CRMGlobalManager.GetApp(“Account”);  
```  
  
 <span data-ttu-id="d188c-151">Điều này sẽ tránh các tác dụng phụ và tiếp tục cung cấp thông tin hữu ích cho trình gỡ lỗi.</span><span class="sxs-lookup"><span data-stu-id="d188c-151">This will avoid the side effect and still provide useful information to the debugger.</span></span>  
  
<a name="Global"></a>   
### <a name="global"></a><span data-ttu-id="d188c-152">$Global</span><span class="sxs-lookup"><span data-stu-id="d188c-152">$Global</span></span>  
 <span data-ttu-id="d188c-153">This section is automatically added to show all options configured in Dynamics 365 for Customer Engagement apps Options and their values.</span><span class="sxs-lookup"><span data-stu-id="d188c-153">This section is automatically added to show all options configured in Dynamics 365 for Customer Engagement apps Options and their values.</span></span> <span data-ttu-id="d188c-154">Điều này làm cho tùy chọn có thể được truy cập dễ dàng vì chúng có thể được sử dụng để kiểm soát thực hiện hoặc để kiểm soát hành vi đã được tạo trong quy trình công việc hoặc cuộc gọi hành động.</span><span class="sxs-lookup"><span data-stu-id="d188c-154">This makes Options easily accessible as they can be used to control execution or to control behaviors that were created in workflows or Action Calls.</span></span> <span data-ttu-id="d188c-155">Tất cả cờ kiểm tra tự động hiển thị từ phần này.</span><span class="sxs-lookup"><span data-stu-id="d188c-155">All the audit flags are automatically visible from this section.</span></span>  
  
<a name="Panel"></a>   
### <a name="panel"></a><span data-ttu-id="d188c-156">$Panel</span><span class="sxs-lookup"><span data-stu-id="d188c-156">$Panel</span></span>  
 <span data-ttu-id="d188c-157">The `$Panel` replacement parameter contains all the hosted controls and their current panel names as key-value pairs that have moved to another panel after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="d188c-157">The `$Panel` replacement parameter contains all the hosted controls and their current panel names as key-value pairs that have moved to another panel after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="d188c-158">The replacement parameter becomes available only if at least one hosted control has changed panels after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span><span class="sxs-lookup"><span data-stu-id="d188c-158">The replacement parameter becomes available only if at least one hosted control has changed panels after you last started the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client.</span></span> <span data-ttu-id="d188c-159">All other hosted controls and their existing panels currently loaded in the agent desktop aren’t available in this replacement parameter.</span><span class="sxs-lookup"><span data-stu-id="d188c-159">All other hosted controls and their existing panels currently loaded in the agent desktop aren’t available in this replacement parameter.</span></span>  
  
<a name="Resources"></a>   
### <a name="resources"></a><span data-ttu-id="d188c-160">$Resources</span><span class="sxs-lookup"><span data-stu-id="d188c-160">$Resources</span></span>  
 <span data-ttu-id="d188c-161">Bộ sưu tập các thông số thay thế được Trình quản lý chung xác định với bộ định danh ngôn ngữ.</span><span class="sxs-lookup"><span data-stu-id="d188c-161">This collection of replacement parameters is populated by the Global Manager with language identifiers.</span></span> <span data-ttu-id="d188c-162">In the configuration of the Global Manager hosted control, you can specify various language resources.</span><span class="sxs-lookup"><span data-stu-id="d188c-162">In the configuration of the Global Manager hosted control, you can specify various language resources.</span></span> <span data-ttu-id="d188c-163">These resources take the form of .resx files but are uploaded into web resources as XML files.</span><span class="sxs-lookup"><span data-stu-id="d188c-163">These resources take the form of .resx files but are uploaded into web resources as XML files.</span></span> <span data-ttu-id="d188c-164">Upon loading of the application, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will read the current language setting from Dynamics 365 for Customer Engagement apps and then look for this language in the Global Manager language list.</span><span class="sxs-lookup"><span data-stu-id="d188c-164">Upon loading of the application, [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] will read the current language setting from Dynamics 365 for Customer Engagement apps and then look for this language in the Global Manager language list.</span></span> <span data-ttu-id="d188c-165">Nếu mục được liệt kê, các nguồn của bộ định danh ngôn ngữ sẽ được tải vào bộ sưu tập $Resources này.</span><span class="sxs-lookup"><span data-stu-id="d188c-165">If the item is listed, the resource of language identifiers will be loaded into this $Resources collection.</span></span>  
  
 <span data-ttu-id="d188c-166">Wherever you intended to provide language neutral text on the output, you can instead use the replacement parameters from the `$Resources` collection.</span><span class="sxs-lookup"><span data-stu-id="d188c-166">Wherever you intended to provide language neutral text on the output, you can instead use the replacement parameters from the `$Resources` collection.</span></span> <span data-ttu-id="d188c-167">Ví dụ, bạn có thể sử dụng sau đây cho các văn bản nút.</span><span class="sxs-lookup"><span data-stu-id="d188c-167">For example, you may use the following for button text.</span></span>  
  
```  
[[$Resources.MyButtonName]+]  
```  
  
 <span data-ttu-id="d188c-168">Depending on the selected language for the user, appropriate localized text will be used.</span><span class="sxs-lookup"><span data-stu-id="d188c-168">Depending on the selected language for the user, appropriate localized text will be used.</span></span>  
  
 <span data-ttu-id="d188c-169">It is also important to note here that these replacement parameters, and therefore the .resx files that are loaded, may contain replacement parameter syntax itself.</span><span class="sxs-lookup"><span data-stu-id="d188c-169">It is also important to note here that these replacement parameters, and therefore the .resx files that are loaded, may contain replacement parameter syntax itself.</span></span> <span data-ttu-id="d188c-170">After `$Resources` values are replaced, they are rechecked for additional replacement parameters.</span><span class="sxs-lookup"><span data-stu-id="d188c-170">After `$Resources` values are replaced, they are rechecked for additional replacement parameters.</span></span> <span data-ttu-id="d188c-171">Bằng cách này, ngay cả khi bạn đang cung cấp chuỗi dành riêng ngôn ngữ, bạn cũng có thể thay thế các dữ liệu từ phần còn lại của các ứng dụng vào chuỗi này.</span><span class="sxs-lookup"><span data-stu-id="d188c-171">In this way, even though you are providing language specific strings, you may substitute data from the rest of the application into this string as well.</span></span>  
  
 <span data-ttu-id="d188c-172">For information about adding localized resources to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Add multilanguage support for your agent applications](../unified-service-desk/add-multilanguage-support-agent-applications.md).</span><span class="sxs-lookup"><span data-stu-id="d188c-172">For information about adding localized resources to configure [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], see [Add multilanguage support for your agent applications](../unified-service-desk/add-multilanguage-support-agent-applications.md).</span></span>  
  
<a name="Return"></a>   
### <a name="return"></a><span data-ttu-id="d188c-173">$Return</span><span class="sxs-lookup"><span data-stu-id="d188c-173">$Return</span></span>  
 <span data-ttu-id="d188c-174">Một số hành động trả về một giá trị chuỗi.</span><span class="sxs-lookup"><span data-stu-id="d188c-174">Some actions return a string value.</span></span> <span data-ttu-id="d188c-175">This string value is placed into the $Return replacement parameter using the name of the action call.</span><span class="sxs-lookup"><span data-stu-id="d188c-175">This string value is placed into the $Return replacement parameter using the name of the action call.</span></span> <span data-ttu-id="d188c-176">Nó sẽ tuân theo mô hình này:</span><span class="sxs-lookup"><span data-stu-id="d188c-176">It will follow this pattern:</span></span>  
  
```  
[[$Return.ActionCallName]]  
```  
  
 <span data-ttu-id="d188c-177">Một ví dụ về điều này sẽ gọi CreateEntity trên trình quản lý chung.</span><span class="sxs-lookup"><span data-stu-id="d188c-177">An example of this would be calling CreateEntity on Global Manager.</span></span> <span data-ttu-id="d188c-178">This will create a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and return the GUID of the new record.</span><span class="sxs-lookup"><span data-stu-id="d188c-178">This will create a record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps, and return the GUID of the new record.</span></span> <span data-ttu-id="d188c-179">This new GUID will be in the `$Return` replacement parameter list and can be used as input to the next action.</span><span class="sxs-lookup"><span data-stu-id="d188c-179">This new GUID will be in the `$Return` replacement parameter list and can be used as input to the next action.</span></span>  
  
<a name="Session"></a>   
### <a name="session"></a><span data-ttu-id="d188c-180">$Session</span><span class="sxs-lookup"><span data-stu-id="d188c-180">$Session</span></span>  
 <span data-ttu-id="d188c-181">The `$Session` section exposes useful variables needed by action calls such as the session count, whether the active session is global, currently active session ID.</span><span class="sxs-lookup"><span data-stu-id="d188c-181">The `$Session` section exposes useful variables needed by action calls such as the session count, whether the active session is global, currently active session ID.</span></span> <span data-ttu-id="d188c-182">The `StartTime` value can be used for writing the start time to an activity.</span><span class="sxs-lookup"><span data-stu-id="d188c-182">The `StartTime` value can be used for writing the start time to an activity.</span></span> <span data-ttu-id="d188c-183">This section is populated automatically.</span><span class="sxs-lookup"><span data-stu-id="d188c-183">This section is populated automatically.</span></span>  
  
<a name="Settings"></a>   
### <a name="settings"></a><span data-ttu-id="d188c-184">$Settings</span><span class="sxs-lookup"><span data-stu-id="d188c-184">$Settings</span></span>  
 <span data-ttu-id="d188c-185">This section provides user settings that only apply to the current user.</span><span class="sxs-lookup"><span data-stu-id="d188c-185">This section provides user settings that only apply to the current user.</span></span> <span data-ttu-id="d188c-186">These settings are automatically loaded at startup, and may be read using an action call at runtime.</span><span class="sxs-lookup"><span data-stu-id="d188c-186">These settings are automatically loaded at startup, and may be read using an action call at runtime.</span></span> <span data-ttu-id="d188c-187">These often include settings for the theme selection of the user but may provide access to any user specific settings that the configurator wants to make available.</span><span class="sxs-lookup"><span data-stu-id="d188c-187">These often include settings for the theme selection of the user but may provide access to any user specific settings that the configurator wants to make available.</span></span>  
  
 <span data-ttu-id="d188c-188">These user settings are defined in the **User Settings** area (**Settings** > **User Settings**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps while configuring [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="d188c-188">These user settings are defined in the **User Settings** area (**Settings** > **User Settings**) in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps while configuring [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
 <span data-ttu-id="d188c-189">Các thiết đặt này có thể được sử dụng như bất kỳ tham số thay thế khác trong hệ thống.</span><span class="sxs-lookup"><span data-stu-id="d188c-189">These settings can be used like any other replacement parameter in the system.</span></span> <span data-ttu-id="d188c-190">The Global Manager hosted control provides an action, [SaveSetting](../unified-service-desk/global-manager-hosted-control.md#SaveSetting), which will write user settings to the server, assuming the user has write access.</span><span class="sxs-lookup"><span data-stu-id="d188c-190">The Global Manager hosted control provides an action, [SaveSetting](../unified-service-desk/global-manager-hosted-control.md#SaveSetting), which will write user settings to the server, assuming the user has write access.</span></span> <span data-ttu-id="d188c-191">This can be used to store user specific preferences such as theme selection and layouts.</span><span class="sxs-lookup"><span data-stu-id="d188c-191">This can be used to store user specific preferences such as theme selection and layouts.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d188c-192">The user settings can be saved to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server if the user has write access.</span><span class="sxs-lookup"><span data-stu-id="d188c-192">The user settings can be saved to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server if the user has write access.</span></span>  
  
<a name="Subject"></a>   
### <a name="subject"></a><span data-ttu-id="d188c-193">$Subject</span><span class="sxs-lookup"><span data-stu-id="d188c-193">$Subject</span></span>  
 <span data-ttu-id="d188c-194">Một khả năng hữu ích trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] là để tự động xác định cây chủ đề trong trường hợp mới mà được tạo trên danh nghĩa của người sử dụng.</span><span class="sxs-lookup"><span data-stu-id="d188c-194">A useful capability in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] is to auto-populate the subject tree in a new case that is created on behalf of the user.</span></span> <span data-ttu-id="d188c-195">Đôi khi bạn sẽ muốn tự động xác định trường chủ đề nhưng bạn cần phải biết các giá trị chính xác để sử dụng, mà có thể thay đổi từ hệ thống đến hệ thống.</span><span class="sxs-lookup"><span data-stu-id="d188c-195">Sometimes you’ll want to auto-populate the subject field but you need to know the correct values to use, which can change from system to system.</span></span>  
  
 <span data-ttu-id="d188c-196">Với mục nhập này, bạn có thể tham chiếu đến chủ đề cụ thể khi bạn đang tạo trường hợp, bằng cách sử dụng các tham số thay thế sau đây.</span><span class="sxs-lookup"><span data-stu-id="d188c-196">With this entry, you can refer to a specific subject when you are creating the case, by using the following replacement parameter.</span></span>  
  
```  
[[$Subject.Default Subject.Id]][[$Subject.Default Subject.LogicalName]]  
```  
  
<a name="SystemParameters"></a>   
### <a name="systemparameters"></a><span data-ttu-id="d188c-197">$SystemParameters</span><span class="sxs-lookup"><span data-stu-id="d188c-197">$SystemParameters</span></span>  
 <span data-ttu-id="d188c-198">This section contains a variable called `HighContrast` that displays whether high-contrast mode in Windows is enabled or not (true/false).</span><span class="sxs-lookup"><span data-stu-id="d188c-198">This section contains a variable called `HighContrast` that displays whether high-contrast mode in Windows is enabled or not (true/false).</span></span> <span data-ttu-id="d188c-199">You could use this variable to decide whether to enable normal custom colors or system colors (compliant with high-contrast setting) when you customize your theme in the client.</span><span class="sxs-lookup"><span data-stu-id="d188c-199">You could use this variable to decide whether to enable normal custom colors or system colors (compliant with high-contrast setting) when you customize your theme in the client.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="d188c-200">[Customize themes in Unified Service Desk](../unified-service-desk/customize-themes-in-unified-service-desk.md )</span><span class="sxs-lookup"><span data-stu-id="d188c-200">[Customize themes in Unified Service Desk](../unified-service-desk/customize-themes-in-unified-service-desk.md )</span></span>  
  
<a name="User"></a>   
### <a name="user"></a><span data-ttu-id="d188c-201">$User</span><span class="sxs-lookup"><span data-stu-id="d188c-201">$User</span></span>  
 <span data-ttu-id="d188c-202">This replacement parameter group is automatically populated with the contents of the current user’s record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="d188c-202">This replacement parameter group is automatically populated with the contents of the current user’s record in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps.</span></span> <span data-ttu-id="d188c-203">For example, if the administrator extends the system user entity in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to include an agent id, the agent id will appear in this list.</span><span class="sxs-lookup"><span data-stu-id="d188c-203">For example, if the administrator extends the system user entity in [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps to include an agent id, the agent id will appear in this list.</span></span> <span data-ttu-id="d188c-204">This can be used to configure special user settings.</span><span class="sxs-lookup"><span data-stu-id="d188c-204">This can be used to configure special user settings.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d188c-205">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="d188c-205">See also</span></span>  
 [<span data-ttu-id="d188c-206">Use replacement parameters to configure Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-206">Use replacement parameters to configure Unified Service Desk</span></span>](../unified-service-desk/use-replacement-parameters-configure-unified-service-desk.md)   
 
 [<span data-ttu-id="d188c-207">Execute scripts using scriptlets in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-207">Execute scripts using scriptlets in Unified Service Desk</span></span>](../unified-service-desk/execute-scripts-using-scriptlets-unified-service-desk.md)   
 
 [<span data-ttu-id="d188c-208">Search data using entity searches in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-208">Search data using entity searches in Unified Service Desk</span></span>](../unified-service-desk/search-data-entity-searches.md) 
 
 [<span data-ttu-id="d188c-209">Learn to use Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="d188c-209">Learn to use Unified Service Desk</span></span>](../unified-service-desk/learn-to-use-unified-service-desk.md)   
 
 [<span data-ttu-id="d188c-210">Global Manager (Hosted Control)</span><span class="sxs-lookup"><span data-stu-id="d188c-210">Global Manager (Hosted Control)</span></span>](../unified-service-desk/global-manager-hosted-control.md)
