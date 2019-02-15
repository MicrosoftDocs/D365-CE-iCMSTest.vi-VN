---
title: 'Walkthrough: Use the generic listener adapter for CTI event routing | MicrosoftDocs'
description: Learn about using the CTI Desktop Manager and generic listener in to expose the CTI events as screen pops in Unified Service Desk.
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
ms.assetid: d6013727-b00e-4671-97c6-f0c0600da980
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 23cc3e9743188e5ddfd014e639524c7481a1bdc7
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386189"
---
# <a name="walkthrough-use-the-generic-listener-adapter-for-cti-event-routing"></a><span data-ttu-id="0879d-103">Walkthrough: Use the generic listener adapter for CTI event routing</span><span class="sxs-lookup"><span data-stu-id="0879d-103">Walkthrough: Use the generic listener adapter for CTI event routing</span></span>
<span data-ttu-id="0879d-104">Cách này trình bày cách bạn có thể sử dụng Trình quản lý Màn hình nền CTI và trình nghe chung trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để hiển thị các sự kiện CTI dưới dạng mục bật lên trên màn hình trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0879d-104">This walkthrough demonstrates how you can use the CTI Desktop Manager and generic listener in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to expose the CTI events as screen pops in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="0879d-105">Đối với cách này, chúng ta sẽ sử dụng ứng dụng Trình mô phỏng CTI mẫu gửi yêu cầu CTI tới [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0879d-105">For this walkthrough, we will use a sample CTI Simulator application that sends CTI requests to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
 <span data-ttu-id="0879d-106">In this walkthrough, you’ll:</span><span class="sxs-lookup"><span data-stu-id="0879d-106">In this walkthrough, you’ll:</span></span>  
  
- <span data-ttu-id="0879d-107">Search for a contact record in the sample [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps data based on an email address specified in the sample CTI Call Tester application.</span><span class="sxs-lookup"><span data-stu-id="0879d-107">Search for a contact record in the sample [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps data based on an email address specified in the sample CTI Call Tester application.</span></span>  
  
- <span data-ttu-id="0879d-108">Tạo quy tắc điều hướng cửa sổ để hiển thị bản ghi phù hợp trong phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0879d-108">Create a window navigation rule to display the matching record in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="0879d-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="0879d-109">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="0879d-110">4.5.2</span><span class="sxs-lookup"><span data-stu-id="0879d-110">4.5.2</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="0879d-111">ứng dụng khách, được yêu cầu để thử nghiệm kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="0879d-111">client application; required for testing the hosted control.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)] <span data-ttu-id="0879d-112">hoặc [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)]</span><span class="sxs-lookup"><span data-stu-id="0879d-112">or [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)]</span></span>  
  
- <span data-ttu-id="0879d-113">[Download the sample CTI Simulator Application Visual Studio project to your computer](http://go.microsoft.com/fwlink/p/?LinkId=519007).</span><span class="sxs-lookup"><span data-stu-id="0879d-113">[Download the sample CTI Simulator Application Visual Studio project to your computer](http://go.microsoft.com/fwlink/p/?LinkId=519007).</span></span> <span data-ttu-id="0879d-114">Build the project, and run the application (.exe file) from the bin\debug folder of the sample application project.</span><span class="sxs-lookup"><span data-stu-id="0879d-114">Build the project, and run the application (.exe file) from the bin\debug folder of the sample application project.</span></span> <span data-ttu-id="0879d-115">Bạn phải chạy ứng dụng Trình mô phỏng USD CTI trên cùng một máy tính nơi ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] đang chạy để kiểm tra các ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="0879d-115">You must run the USD CTI Simulator application on the same computer where [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client is running to test the application.</span></span>  
  
<a name="step1"></a>   
## <a name="step-1-configure-a-cti-desktop-manager-hosted-control-in-unified-service-desk"></a><span data-ttu-id="0879d-116">Bước 1: Đặt cấu hình kiểm soát tổ chức Trình quản lý Màn hình nền CTI trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="0879d-116">Step 1: Configure a CTI Desktop Manager hosted control in Unified Service Desk</span></span>  
  
1. <span data-ttu-id="0879d-117">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0879d-117">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="0879d-118">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="0879d-118">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="0879d-119">On the **Unified Service Desk** page, choose **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="0879d-119">On the **Unified Service Desk** page, choose **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="0879d-120">Trên trang **Kiểm soát Tổ chức**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="0879d-120">On the **Hosted Controls** page, choose **New**.</span></span>  
  
5. <span data-ttu-id="0879d-121">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="0879d-121">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="0879d-122">Trường</span><span class="sxs-lookup"><span data-stu-id="0879d-122">Field</span></span>|<span data-ttu-id="0879d-123">Value</span><span class="sxs-lookup"><span data-stu-id="0879d-123">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="0879d-124">Tên</span><span class="sxs-lookup"><span data-stu-id="0879d-124">Name</span></span>|<span data-ttu-id="0879d-125">CTITest</span><span class="sxs-lookup"><span data-stu-id="0879d-125">CTITest</span></span>|  
   |<span data-ttu-id="0879d-126">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="0879d-126">USD Component Type</span></span>|<span data-ttu-id="0879d-127">Trình quản lý Màn hình nền CTI</span><span class="sxs-lookup"><span data-stu-id="0879d-127">CTI Desktop Manager</span></span>|  
   |<span data-ttu-id="0879d-128">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="0879d-128">Display Group</span></span>|<span data-ttu-id="0879d-129">Bảng điều khiển bị ẩn</span><span class="sxs-lookup"><span data-stu-id="0879d-129">HiddenPanel</span></span>|  
   |<span data-ttu-id="0879d-130">URI cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="0879d-130">Assembly URI</span></span>|<span data-ttu-id="0879d-131">Microsoft.Crm.UnifiedServiceDesk.GenericListener</span><span class="sxs-lookup"><span data-stu-id="0879d-131">Microsoft.Crm.UnifiedServiceDesk.GenericListener</span></span>|  
   |<span data-ttu-id="0879d-132">Loại cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="0879d-132">Assembly Type</span></span>|<span data-ttu-id="0879d-133">Microsoft.Crm.UnifiedServiceDesk.GenericListener.DesktopManager</span><span class="sxs-lookup"><span data-stu-id="0879d-133">Microsoft.Crm.UnifiedServiceDesk.GenericListener.DesktopManager</span></span>|  
  
   > [!NOTE]
   >  <span data-ttu-id="0879d-134">Các giá trị được chỉ định trong các trường **URI Cụm tổ hợp** và **Loại Cụm tổ hợp** là các giá trị trình nghe chung cho loại kiểm soát tổ chức **Trình quản lý Màn hình nền CTI**.</span><span class="sxs-lookup"><span data-stu-id="0879d-134">The values specified in the **Assembly URI** and **Assembly Type** fields are the generic listener values for the **CTI Desktop Manager** hosted control type.</span></span>  
  
   <span data-ttu-id="0879d-135">![Configure CTI Dekstop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager.png "Configure CTI Dekstop Manager hosted control")</span><span class="sxs-lookup"><span data-stu-id="0879d-135">![Configure CTI Dekstop Manager hosted control](../unified-service-desk/media/usd-cti-desktop-manager.png "Configure CTI Dekstop Manager hosted control")</span></span>  
  
6. <span data-ttu-id="0879d-136">Bấm vào **Lưu** để tạo kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="0879d-136">Click **Save** to create the hosted control.</span></span>  
  
<a name="step2"></a>   
## <a name="step-2-test-if-the-cti-events-are-raised-in-unified-service-desk"></a><span data-ttu-id="0879d-137">Bước 2: Kiểm tra xem các sự kiện CTI có được nêu trong Unified Service Desk không</span><span class="sxs-lookup"><span data-stu-id="0879d-137">Step 2: Test if the CTI events are raised in Unified Service Desk</span></span>  
  
1. <span data-ttu-id="0879d-138">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="0879d-138">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> <span data-ttu-id="0879d-139">After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.</span><span class="sxs-lookup"><span data-stu-id="0879d-139">After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.</span></span>  
  
   <span data-ttu-id="0879d-140">![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")</span><span class="sxs-lookup"><span data-stu-id="0879d-140">![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")</span></span>  
  
2. <span data-ttu-id="0879d-141">Bắt đầu ứng dụng Trình mô phỏng USD CTI, nhập **Email** vào cột **Phím** và chỉ định một giá trị ngẫu nhiên trong cột **Giá trị**.</span><span class="sxs-lookup"><span data-stu-id="0879d-141">Start the USD CTI Simulator application, type **Email** in the **Key** column and specify a random value in the **Value** column.</span></span> <span data-ttu-id="0879d-142">Bấm **Gửi tới USD**.</span><span class="sxs-lookup"><span data-stu-id="0879d-142">Click **Send to USD**.</span></span>  
  
   <span data-ttu-id="0879d-143">![Unified Service Desk CTI Simulator](../unified-service-desk/media/usd-ctistimulator.png "Unified Service Desk CTI Simulator")</span><span class="sxs-lookup"><span data-stu-id="0879d-143">![Unified Service Desk CTI Simulator](../unified-service-desk/media/usd-ctistimulator.png "Unified Service Desk CTI Simulator")</span></span>  
  
3. <span data-ttu-id="0879d-144">Màn hình cửa sổ bật lên xuất hiện trong ứng dụng khách để hiển thị sự kiện CTI.</span><span class="sxs-lookup"><span data-stu-id="0879d-144">A screen pop-up occurs in the client application to expose the CTI event.</span></span> <span data-ttu-id="0879d-145">Trong trường hợp này, `CTILookUpRequest` được khởi tạo với giá trị được chỉ định trong ứng dụng Trình mô phỏng USD CTI.</span><span class="sxs-lookup"><span data-stu-id="0879d-145">In this case, a `CTILookUpRequest` is initiated with the value that was specified in the USD CTI Simulator application.</span></span> <span data-ttu-id="0879d-146">Bởi vì bạn chưa ghép với một quy tắc điều hướng cửa sổ, sẽ không có gì khác xảy ra.</span><span class="sxs-lookup"><span data-stu-id="0879d-146">Because you haven’t wired it yet with a window navigation rule, nothing further happens.</span></span>  
  
   <span data-ttu-id="0879d-147">![Screen pop in for the CTI event](../unified-service-desk/media/usd-usdclientwithctievent.png "Screen pop in for the CTI event")</span><span class="sxs-lookup"><span data-stu-id="0879d-147">![Screen pop in for the CTI event](../unified-service-desk/media/usd-usdclientwithctievent.png "Screen pop in for the CTI event")</span></span>  
  
<a name="step3"></a>   
## <a name="step-3-define-a-window-navigation-rule-to-route-the-ctilookuprequest"></a><span data-ttu-id="0879d-148">Bước 3: Xác định một quy tắc điều hướng cửa sổ để định tuyến CtiLookUpRequest</span><span class="sxs-lookup"><span data-stu-id="0879d-148">Step 3: Define a window navigation rule to route the CtiLookUpRequest</span></span>  
 <span data-ttu-id="0879d-149">Tạo một quy tắc điều hướng cửa sổ để tạo phiên nếu tìm thấy giá trị phù hợp, sau đó hiển thị bản ghi liên hệ phù hợp trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="0879d-149">Create a window navigation rule to create a session if a match is found, and then display the matching contact record in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span></span>  
  
1. <span data-ttu-id="0879d-150">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="0879d-150">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="0879d-151">Navigate to the advanced find for contacts, and create a query where you search for active contacts where the email, email address 2, or email address 3 field equals a certain value, for example, someone_c@example.com.</span><span class="sxs-lookup"><span data-stu-id="0879d-151">Navigate to the advanced find for contacts, and create a query where you search for active contacts where the email, email address 2, or email address 3 field equals a certain value, for example, someone_c@example.com.</span></span>  
  
   <span data-ttu-id="0879d-152">![Query for contacts based on email address](../unified-service-desk/media/usd-contactsadvancedfind.png "Query for contacts based on email address")</span><span class="sxs-lookup"><span data-stu-id="0879d-152">![Query for contacts based on email address](../unified-service-desk/media/usd-contactsadvancedfind.png "Query for contacts based on email address")</span></span>  
  
3. <span data-ttu-id="0879d-153">Bấm **Tải xuống Fetch XML** để lưu truy vấn làm `FetchXML`.</span><span class="sxs-lookup"><span data-stu-id="0879d-153">Click **Download Fetch XML** to save the query as `FetchXML`.</span></span>  
  
4. <span data-ttu-id="0879d-154">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk** > **Window Navigation Rules**.</span><span class="sxs-lookup"><span data-stu-id="0879d-154">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk** > **Window Navigation Rules**.</span></span>  
  
5. <span data-ttu-id="0879d-155">Bấm **Mới** và trên cửa sổ **Quy tắc Điều hướng Cửa sổ Mới**, hãy chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="0879d-155">Click **New**, and on the **New Window Navigation Rule** window, specify the following values.</span></span>  
  
   |<span data-ttu-id="0879d-156">Trường</span><span class="sxs-lookup"><span data-stu-id="0879d-156">Field</span></span>|<span data-ttu-id="0879d-157">Value</span><span class="sxs-lookup"><span data-stu-id="0879d-157">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="0879d-158">Tên</span><span class="sxs-lookup"><span data-stu-id="0879d-158">Name</span></span>|<span data-ttu-id="0879d-159">CTITestRoute</span><span class="sxs-lookup"><span data-stu-id="0879d-159">CTITestRoute</span></span>|  
   |<span data-ttu-id="0879d-160">Thứ tự</span><span class="sxs-lookup"><span data-stu-id="0879d-160">Order</span></span>|<span data-ttu-id="0879d-161">50</span><span class="sxs-lookup"><span data-stu-id="0879d-161">50</span></span>|  
   |<span data-ttu-id="0879d-162">Từ</span><span class="sxs-lookup"><span data-stu-id="0879d-162">From</span></span>|<span data-ttu-id="0879d-163">CTITest</span><span class="sxs-lookup"><span data-stu-id="0879d-163">CTITest</span></span><br /><br /> <span data-ttu-id="0879d-164">Đây là tên của kiểm soát tổ chức Trình quản lý Màn hình nền CTI.</span><span class="sxs-lookup"><span data-stu-id="0879d-164">This is the name of your CTI Desktop Manager hosted control.</span></span>|  
   |<span data-ttu-id="0879d-165">Hướng</span><span class="sxs-lookup"><span data-stu-id="0879d-165">Direction</span></span>|<span data-ttu-id="0879d-166">Cả hai</span><span class="sxs-lookup"><span data-stu-id="0879d-166">Both</span></span>|  
  
   <span data-ttu-id="0879d-167">![New window navigation rule for routing CTI event](../unified-service-desk/media/usd-cti-route-rule.png "New window navigation rule for routing CTI event")</span><span class="sxs-lookup"><span data-stu-id="0879d-167">![New window navigation rule for routing CTI event](../unified-service-desk/media/usd-cti-route-rule.png "New window navigation rule for routing CTI event")</span></span>  
  
6. <span data-ttu-id="0879d-168">Lưu quy tắc.</span><span class="sxs-lookup"><span data-stu-id="0879d-168">Save the rule.</span></span> <span data-ttu-id="0879d-169">Điều này cho phép phần còn lại trên trang này.</span><span class="sxs-lookup"><span data-stu-id="0879d-169">This enables the rest of the controls on the page.</span></span>  
  
7. <span data-ttu-id="0879d-170">Bây giờ, thêm truy vấn `FetchXML` đã được lưu trước đây vào quy tắc này.</span><span class="sxs-lookup"><span data-stu-id="0879d-170">Now, add the `FetchXML` query that was saved earlier to this rule.</span></span> <span data-ttu-id="0879d-171">Under the **CTI Searches** area, choose Add ![Add a record button](../unified-service-desk/media/crm-ua-add-record.gif "Add a record button").</span><span class="sxs-lookup"><span data-stu-id="0879d-171">Under the **CTI Searches** area, choose Add ![Add a record button](../unified-service-desk/media/crm-ua-add-record.gif "Add a record button").</span></span>  
  
8. <span data-ttu-id="0879d-172">In the **New CTI Search** window, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="0879d-172">In the **New CTI Search** window, specify the following values:</span></span>  
  
   - <span data-ttu-id="0879d-173">**Name**: CTIContactSearch</span><span class="sxs-lookup"><span data-stu-id="0879d-173">**Name**: CTIContactSearch</span></span>  
  
   - <span data-ttu-id="0879d-174">**Order**: 1</span><span class="sxs-lookup"><span data-stu-id="0879d-174">**Order**: 1</span></span>  
  
   - <span data-ttu-id="0879d-175">**FetchXML**:</span><span class="sxs-lookup"><span data-stu-id="0879d-175">**FetchXML**:</span></span>  
  
       ```xml  
  
       <fetch version="1.0" output-format="xml-platform" mapping="logical" distinct="false">  
         <entity name="contact">  
           <attribute name="fullname" />  
           <attribute name="parentcustomerid" />  
           <attribute name="telephone1" />  
           <attribute name="emailaddress1" />  
           <attribute name="contactid" />  
           <order attribute="fullname" descending="false" />  
           <filter type="and">  
             <condition attribute="statecode" operator="eq" value="0" />  
             <filter type="or">  
               <condition attribute="emailaddress1" operator="eq" value="[[cti.Email]]" />  
               <condition attribute="emailaddress2" operator="eq" value="[[cti.Email]]" />  
               <condition attribute="emailaddress3" operator="eq" value="[[cti.Email]]" />  
             </filter>  
           </filter>  
         </entity>  
       </fetch>  
       ```  
  
     > [!NOTE]
     >  <span data-ttu-id="0879d-176">The address someone_c@example.com was replaced with `[[cti.Email]]` so that the search is run based on the value specified for the **Email** key in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] CTI Simulator application.</span><span class="sxs-lookup"><span data-stu-id="0879d-176">The address someone_c@example.com was replaced with `[[cti.Email]]` so that the search is run based on the value specified for the **Email** key in the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] CTI Simulator application.</span></span>  
  
   <span data-ttu-id="0879d-177">![Define a CTI search for contacts](../unified-service-desk/media/usd-contactctisearch.png "Define a CTI search for contacts")</span><span class="sxs-lookup"><span data-stu-id="0879d-177">![Define a CTI search for contacts](../unified-service-desk/media/usd-contactctisearch.png "Define a CTI search for contacts")</span></span>  
  
9. <span data-ttu-id="0879d-178">Lưu quy tắc tìm kiếm CTI và trả lại quy tắc điều hướng cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="0879d-178">Save the CTI search rule, and return to the window navigation rule.</span></span>  
  
10. <span data-ttu-id="0879d-179">Trong **Một Kết quả phù hợp**, trong trường **Quyết định**, chọn **Tạo Phiên, Tải Kết quả phù hợp rồi Hành động**.</span><span class="sxs-lookup"><span data-stu-id="0879d-179">Under **Single Match**, in the **Decision** field, select **Create Session, Load Match then Do Action**.</span></span>  
  
11. <span data-ttu-id="0879d-180">Trong **Một Kết quả phù hợp**, trong trường **Hành động**, bấm vào biểu tượng tìm kiếm để chọn một giá trị rồi bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="0879d-180">Under **Single Match**, in the **Action** field, click the search icon to select a value, and then click **New**.</span></span>  
  
12. <span data-ttu-id="0879d-181">Trên trang **Cuộc gọi Hành động Mới**, tạo cuộc gọi hành động để mở bản ghi liên hệ bằng cách chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="0879d-181">On the **New Action Call** page, create an action call to open the contact record by specifying the following values.</span></span>  
  
    |<span data-ttu-id="0879d-182">Trường</span><span class="sxs-lookup"><span data-stu-id="0879d-182">Field</span></span>|<span data-ttu-id="0879d-183">Value</span><span class="sxs-lookup"><span data-stu-id="0879d-183">Value</span></span>|  
    |-----------|-----------|  
    |<span data-ttu-id="0879d-184">Tên</span><span class="sxs-lookup"><span data-stu-id="0879d-184">Name</span></span>|<span data-ttu-id="0879d-185">CTIOpenContact</span><span class="sxs-lookup"><span data-stu-id="0879d-185">CTIOpenContact</span></span>|  
    |<span data-ttu-id="0879d-186">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="0879d-186">Hosted Control</span></span>|<span data-ttu-id="0879d-187">Dynamics 365 for Customer Engagement apps Global Manager</span><span class="sxs-lookup"><span data-stu-id="0879d-187">Dynamics 365 for Customer Engagement apps Global Manager</span></span>|  
    |<span data-ttu-id="0879d-188">Hành động</span><span class="sxs-lookup"><span data-stu-id="0879d-188">Action</span></span>|<span data-ttu-id="0879d-189">Open_CRM_Page</span><span class="sxs-lookup"><span data-stu-id="0879d-189">Open_CRM_Page</span></span>|  
    |<span data-ttu-id="0879d-190">Dữ liệu</span><span class="sxs-lookup"><span data-stu-id="0879d-190">Data</span></span>|<span data-ttu-id="0879d-191">Id=[[$Context.Id]]</span><span class="sxs-lookup"><span data-stu-id="0879d-191">Id=[[$Context.Id]]</span></span><br /><span data-ttu-id="0879d-192">LogicalName=[[$Context.LogicalName]]</span><span class="sxs-lookup"><span data-stu-id="0879d-192">LogicalName=[[$Context.LogicalName]]</span></span>|  
  
    <span data-ttu-id="0879d-193">![Configure an action to display contact](../unified-service-desk/media/usd-ctiopencontact.png "Configure an action to display contact")</span><span class="sxs-lookup"><span data-stu-id="0879d-193">![Configure an action to display contact](../unified-service-desk/media/usd-ctiopencontact.png "Configure an action to display contact")</span></span>  
  
13. <span data-ttu-id="0879d-194">Lưu cuộc gọi hành động, rồi sau đó đóng trang cuộc gọi hành động để trở về trang định nghĩa quy tắc điều hướng cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="0879d-194">Save the action call, and then close the action call page to return to the window navigation rule definition page.</span></span>  
  
14. <span data-ttu-id="0879d-195">Trong khu vực **Kết quả**:</span><span class="sxs-lookup"><span data-stu-id="0879d-195">Under the **Result** area:</span></span>  
  
    1. <span data-ttu-id="0879d-196">Trong trường **Đích**, chọn **Tab** để hiển thị bản ghi liên hệ phù hợp trong tab.</span><span class="sxs-lookup"><span data-stu-id="0879d-196">In the **Destination** field, choose **Tab** to display the matching contact record in a tab.</span></span>  
  
    2. <span data-ttu-id="0879d-197">Trong trường **Tab Đích**, chọn kiểm soát tổ chức **Liên hệ**.</span><span class="sxs-lookup"><span data-stu-id="0879d-197">In the **Target Tab** field, choose the **Contact** hosted control.</span></span> <span data-ttu-id="0879d-198">The **Contact** hosted control was created when you deployed a sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server using the [!INCLUDE[pn_package_deployer_tool](../includes/pn-package-deployer-tool.md)].</span><span class="sxs-lookup"><span data-stu-id="0879d-198">The **Contact** hosted control was created when you deployed a sample [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server using the [!INCLUDE[pn_package_deployer_tool](../includes/pn-package-deployer-tool.md)].</span></span> <span data-ttu-id="0879d-199">For more information, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).</span><span class="sxs-lookup"><span data-stu-id="0879d-199">For more information, see [Deploy sample Unified Service Desk applications to CRM server using Package Deployer](admin/deploy-sample-unified-service-desk-applications-using-package-deployer.md).</span></span>  
  
    3. <span data-ttu-id="0879d-200">Trong trường **Hiển thị Tab**, chọn kiểm soát tổ chức **Liên hệ**</span><span class="sxs-lookup"><span data-stu-id="0879d-200">In the **Show Tab** field, choose the **Contact** hosted control</span></span>  
  
    <span data-ttu-id="0879d-201">![Specify appropriate values for the rule definition](../unified-service-desk/media/usd-windownavruledefinition.png "Specify appropriate values for the rule definition")</span><span class="sxs-lookup"><span data-stu-id="0879d-201">![Specify appropriate values for the rule definition](../unified-service-desk/media/usd-windownavruledefinition.png "Specify appropriate values for the rule definition")</span></span>  
  
15. <span data-ttu-id="0879d-202">Lưu quy tắc điều hướng cửa sổ.</span><span class="sxs-lookup"><span data-stu-id="0879d-202">Save the window navigation rule.</span></span>  
  
<a name="test"></a>   
## <a name="test-your-cti-adapter"></a><span data-ttu-id="0879d-203">Kiểm tra bộ chuyển đổi CTI của bạn</span><span class="sxs-lookup"><span data-stu-id="0879d-203">Test your CTI adapter</span></span>  
  
1. <span data-ttu-id="0879d-204">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="0879d-204">Start [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client, and connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span> <span data-ttu-id="0879d-205">After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.</span><span class="sxs-lookup"><span data-stu-id="0879d-205">After the client is up, choose **Settings**![Gear button](../unified-service-desk/media/crm-ua-selection-rule-gear.gif "Gear button") in the top-right corner to display the debugger control, and then choose **Clear Debug Output**![Delete button](../unified-service-desk/media/crm-ua-delete.gif "Delete button") to clear the desktop.</span></span>  
  
   <span data-ttu-id="0879d-206">![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")</span><span class="sxs-lookup"><span data-stu-id="0879d-206">![Unified Service Desk client](../unified-service-desk/media/usd-usdclientwithdebugger.png "Unified Service Desk client")</span></span>  
  
2. <span data-ttu-id="0879d-207">Khởi động ứng dụng Trình mô phỏng USD CTI, nhập **Email** vào cột **Phím** và chỉ định ID email hợp lệ từ liên hệ mà bạn muốn tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="0879d-207">Start the USD CTI Simulator application, type **Email** in the **Key** column and specify a valid email ID for the contact that you want to search.</span></span> <span data-ttu-id="0879d-208">In this case, type someone_d@example.com in the **Value** column.</span><span class="sxs-lookup"><span data-stu-id="0879d-208">In this case, type someone_d@example.com in the **Value** column.</span></span> <span data-ttu-id="0879d-209">Bấm **Gửi tới USD**.</span><span class="sxs-lookup"><span data-stu-id="0879d-209">Click **Send To USD**.</span></span>  
  
   <span data-ttu-id="0879d-210">![Specify the email to search for a contact](../unified-service-desk/media/usd-testctiadapter01.png "Specify the email to search for a contact")</span><span class="sxs-lookup"><span data-stu-id="0879d-210">![Specify the email to search for a contact](../unified-service-desk/media/usd-testctiadapter01.png "Specify the email to search for a contact")</span></span>  
  
3. <span data-ttu-id="0879d-211">Bản ghi liên hệ phù hợp được hiển thị trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="0879d-211">The matching contact record is displayed in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   <span data-ttu-id="0879d-212">![Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session](../unified-service-desk/media/usd-testctiadapter02.png "Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session")</span><span class="sxs-lookup"><span data-stu-id="0879d-212">![Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session](../unified-service-desk/media/usd-testctiadapter02.png "Matching Dynamics 365 for Customer Engagement apps contact record displayed in a session")</span></span>  
  
4. <span data-ttu-id="0879d-213">Kiểm tra kiểm soát tổ chức Trình gỡ lỗi để xem các sự kiện đã được nêu là kết quả của tìm kiếm CTI.</span><span class="sxs-lookup"><span data-stu-id="0879d-213">Check the Debugger hosted control to view the events that got raised as a result of the CTI search.</span></span> <span data-ttu-id="0879d-214">Ngoài ra, kiểm tra tab **Tham số Dữ liệu** để xem thông tin ngữ cảnh trong biến `$Context` và thông tin CTI trong biến `CTI`.</span><span class="sxs-lookup"><span data-stu-id="0879d-214">Also check out the **Data Parameters** tab to view the context information in the `$Context` variable and CTI information under the `CTI` variable.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0879d-215">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="0879d-215">See also</span></span>  
 <span data-ttu-id="0879d-216">[Integrate with CTI systems](../unified-service-desk/integrate-cti-systems-cti-adapters.md) </span><span class="sxs-lookup"><span data-stu-id="0879d-216">[Integrate with CTI systems](../unified-service-desk/integrate-cti-systems-cti-adapters.md) </span></span>  
 [<span data-ttu-id="0879d-217">UII Computer Telephony Integration (CTI) framework</span><span class="sxs-lookup"><span data-stu-id="0879d-217">UII Computer Telephony Integration (CTI) framework</span></span>](../unified-service-desk/uii-computer-telephony-integration-cti-framework.md)
