---
title: 'Walkthrough 5: Display enhanced session information by displaying session name and overview data | MicrosoftDocs'
description: Demonstrates how to dynamically display session name and session overview information in Unified Service Desk to enhance the customer-interaction experience for your agents.
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
ms.assetid: 01e6b62c-2add-46ca-9d90-0c45c60f83f9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 4f955058d2e39eef2a32925521f5ea70d5e80490
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387675"
---
# <a name="walkthrough-5-display-enhanced-session-information-by-displaying-session-name-and-overview-data"></a><span data-ttu-id="8babb-103">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span><span class="sxs-lookup"><span data-stu-id="8babb-103">Walkthrough 5: Display enhanced session information by displaying session name and overview data</span></span>
<span data-ttu-id="8babb-104">In the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md), you learned how to display your customer record stored in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="8babb-104">In the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md), you learned how to display your customer record stored in [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="8babb-105">Tuy nhiên, trải nghiệm sẽ tốt hơn nếu bạn có thể xác định mỗi phiên làm việc với một tên duy nhất cùng với một số thông tin quan trọng tổng quan về hồ sơ trong một phiên.</span><span class="sxs-lookup"><span data-stu-id="8babb-105">However, the experience would be better if you can identify each session with a unique name along with some key overview information about the record in a session.</span></span>  
  
 <span data-ttu-id="8babb-106">Cách này trình cách cách hiển thị tên phiên và thông tin tổng quan về phiên động để nâng cao trải nghiệm tương tác khách hàng cho các tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="8babb-106">This walkthrough demonstrates how to dynamically display session name and session overview information to enhance the customer-interaction experience for your agents.</span></span> <span data-ttu-id="8babb-107">This walkthrough is built on top of the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="8babb-107">This walkthrough is built on top of the previous walkthrough, [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="8babb-108">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="8babb-108">Prerequisites</span></span>  
  
- <span data-ttu-id="8babb-109">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="8babb-109">You must have completed [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md) and [Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md).</span></span> <span data-ttu-id="8babb-110">The configurations that you completed in those walkthroughs are required in this walkthrough.</span><span class="sxs-lookup"><span data-stu-id="8babb-110">The configurations that you completed in those walkthroughs are required in this walkthrough.</span></span>  
  
- <span data-ttu-id="8babb-111">Cách này giả định rằng bạn sẽ đang sử dụng cùng một thông tin đăng nhập người dùng bạn đã dùng trong cách 1 để đăng nhập vào ứng dụng tổng đài viên ở cuối cách này để kiểm tra ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="8babb-111">This walkthrough assumes that you’ll be using the same user credential that you used in walkthrough 1 to sign in to the agent application at the end of the walkthrough to test the application.</span></span> <span data-ttu-id="8babb-112">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8babb-112">If a different user will be testing the application, you must assign the user to **Contoso Configuration**.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8babb-113">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span><span class="sxs-lookup"><span data-stu-id="8babb-113">[Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)</span></span>  
  
- <span data-ttu-id="8babb-114">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span><span class="sxs-lookup"><span data-stu-id="8babb-114">You must know about the following in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:</span></span>  
  
  - <span data-ttu-id="8babb-115">**Session Lines** and **Session Tabs** type of hosted control.</span><span class="sxs-lookup"><span data-stu-id="8babb-115">**Session Lines** and **Session Tabs** type of hosted control.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8babb-116">[Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md) and [Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="8babb-116">[Session Lines (Hosted Control)](../unified-service-desk/session-lines-hosted-control.md) and [Session Tabs (Hosted Control)](../unified-service-desk/session-tabs-hosted-control.md)</span></span>  
  
  - <span data-ttu-id="8babb-117">Đặt cấu hình tên phiên và thông tin tổng quan về phiên.</span><span class="sxs-lookup"><span data-stu-id="8babb-117">Configure session name and session overview information.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8babb-118">[Configure session information](../unified-service-desk/configure-session-information.md)</span><span class="sxs-lookup"><span data-stu-id="8babb-118">[Configure session information](../unified-service-desk/configure-session-information.md)</span></span>  
  
  - <span data-ttu-id="8babb-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span><span class="sxs-lookup"><span data-stu-id="8babb-119">Filter access using [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] configuration.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="8babb-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="8babb-120">[Manage access using Unified Service Desk configuration](../unified-service-desk/admin/manage-access-using-unified-service-desk-configuration.md)</span></span>  
  
## <a name="in-this-walkthrough"></a><span data-ttu-id="8babb-121">In This Walkthrough</span><span class="sxs-lookup"><span data-stu-id="8babb-121">In This Walkthrough</span></span>  
 [<span data-ttu-id="8babb-122">Bước 1: Tạo loại dòng phiên của kiểm soát tổ chức để hiển thị thông tin tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-122">Step 1: Create a Session Lines type of hosted control to display session overview information</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Step1)  
  
 [<span data-ttu-id="8babb-123">Bước 2: Xác định thông tin tên phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-123">Step 2: Define session name information</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Step2)  
  
 [<span data-ttu-id="8babb-124">Bước 3: Xác định thông tin tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-124">Step 3: Define session overview information</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Step3)  
  
 [<span data-ttu-id="8babb-125">Bước 4: Thêm kiểm soát vào cấu hình</span><span class="sxs-lookup"><span data-stu-id="8babb-125">Step 4: Add the controls to the configuration</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Step4)  
  
 [<span data-ttu-id="8babb-126">Bước 5: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="8babb-126">Step 5: Test the application</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Step5)  
  
 [<span data-ttu-id="8babb-127">Kết luận</span><span class="sxs-lookup"><span data-stu-id="8babb-127">Conclusion</span></span>](../unified-service-desk/walkthrough-5-display-enhanced-session-information-displaying-session-name-overview-data.md#Conclusion)  
  
<a name="Step1"></a>   
## <a name="step-1-create-a-session-lines-type-of-hosted-control-to-display-session-overview-information"></a><span data-ttu-id="8babb-128">Bước 1: Tạo loại dòng phiên của kiểm soát tổ chức để hiển thị thông tin tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-128">Step 1: Create a Session Lines type of hosted control to display session overview information</span></span>  
 <span data-ttu-id="8babb-129">Để hiển thị thông tin tổng quan về phiên trong ứng dụng tổng đài viên của bạn, tạo một phiên bản loại **Dòng phiên** của kiểm soát tổ chức trong ứng dụng tổng đài viên của bạn.</span><span class="sxs-lookup"><span data-stu-id="8babb-129">To display session overview information in your agent application, create an instance of a **Session Lines** type of hosted control in your agent application.</span></span>  
  
1. <span data-ttu-id="8babb-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8babb-130">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="8babb-131">Click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="8babb-131">Click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="8babb-132">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="8babb-132">Click **New**.</span></span>  
  
5. <span data-ttu-id="8babb-133">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="8babb-133">On the **New Hosted Control** page, specify the following values:</span></span>  
  
   |<span data-ttu-id="8babb-134">Trường</span><span class="sxs-lookup"><span data-stu-id="8babb-134">Field</span></span>|<span data-ttu-id="8babb-135">Giá trị</span><span class="sxs-lookup"><span data-stu-id="8babb-135">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="8babb-136">Tên</span><span class="sxs-lookup"><span data-stu-id="8babb-136">Name</span></span>|<span data-ttu-id="8babb-137">Tổng quan về phiên contoso</span><span class="sxs-lookup"><span data-stu-id="8babb-137">Contoso Session Overview</span></span>|  
   |<span data-ttu-id="8babb-138">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="8babb-138">USD Component Type</span></span>|<span data-ttu-id="8babb-139">Dòng Phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-139">Session Lines</span></span>|  
   |<span data-ttu-id="8babb-140">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="8babb-140">Display Group</span></span>|<span data-ttu-id="8babb-141">Bảng điều khiển Trình khám phá phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-141">SessionExplorerPanel</span></span>|  
  
   <span data-ttu-id="8babb-142">![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-wt05-01.png "Create a Session Lines hosted control")</span><span class="sxs-lookup"><span data-stu-id="8babb-142">![Create a Session Lines hosted control](../unified-service-desk/media/crm-itpro-usd-wt05-01.png "Create a Session Lines hosted control")</span></span>  
  
6. <span data-ttu-id="8babb-143">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8babb-143">Click **Save**.</span></span>  
  
<a name="Step2"></a>   
## <a name="step-2-define-session-name-information"></a><span data-ttu-id="8babb-144">Bước 2: Xác định thông tin tên phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-144">Step 2: Define session name information</span></span>  
 <span data-ttu-id="8babb-145">Để hiển thị tên tab phiên động, bạn sẽ đặt cấu hình quy tắc dòng phiên bằng cách sử dụng các tham số thay thế.</span><span class="sxs-lookup"><span data-stu-id="8babb-145">To dynamically display the session tab name, you’ll configure a session lines rule using the replacement parameters.</span></span>  
  
1. <span data-ttu-id="8babb-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8babb-146">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="8babb-147">Click **Session Lines**.</span><span class="sxs-lookup"><span data-stu-id="8babb-147">Click **Session Lines**.</span></span>  
  
4. <span data-ttu-id="8babb-148">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="8babb-148">Click **New**.</span></span>  
  
5. <span data-ttu-id="8babb-149">Trên trang **Thông tin phiên mới**, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="8babb-149">On the **New Session Information** page, specify the following values:</span></span>  
  
   |<span data-ttu-id="8babb-150">Trường</span><span class="sxs-lookup"><span data-stu-id="8babb-150">Field</span></span>|<span data-ttu-id="8babb-151">Giá trị</span><span class="sxs-lookup"><span data-stu-id="8babb-151">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="8babb-152">Đơn hàng</span><span class="sxs-lookup"><span data-stu-id="8babb-152">Order</span></span>|<span data-ttu-id="8babb-153">Bất kỳ giá trị ngẫu nhiên; nói 5</span><span class="sxs-lookup"><span data-stu-id="8babb-153">Any random value; say 5</span></span>|  
   |<span data-ttu-id="8babb-154">Tên</span><span class="sxs-lookup"><span data-stu-id="8babb-154">Name</span></span>|<span data-ttu-id="8babb-155">Tên phiên Contoso</span><span class="sxs-lookup"><span data-stu-id="8babb-155">Contoso Session Name</span></span>|  
   |<span data-ttu-id="8babb-156">Thực thể được chọn</span><span class="sxs-lookup"><span data-stu-id="8babb-156">Selected Entity</span></span>|<span data-ttu-id="8babb-157">tài khoản</span><span class="sxs-lookup"><span data-stu-id="8babb-157">account</span></span>|  
   |<span data-ttu-id="8babb-158">Loại</span><span class="sxs-lookup"><span data-stu-id="8babb-158">Type</span></span>|<span data-ttu-id="8babb-159">Tên Phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-159">Session Name</span></span>|  
   |<span data-ttu-id="8babb-160">Hiển thị</span><span class="sxs-lookup"><span data-stu-id="8babb-160">Display</span></span>|<span data-ttu-id="8babb-161">Phiên: [[account.name]]</span><span class="sxs-lookup"><span data-stu-id="8babb-161">Session: [[account.name]]</span></span><br /><br /> <span data-ttu-id="8babb-162">Chúng tôi đang sử dụng các tham số thay thế để xác định định dạng tên tab phiên.</span><span class="sxs-lookup"><span data-stu-id="8babb-162">We are using the replacement parameters to define the session tab name format.</span></span> <span data-ttu-id="8babb-163">Trong trường hợp này tên phiên sẽ là **phiên:** theo sau là tên của hồ sơ tài khoản được hiển thị trong phiên.</span><span class="sxs-lookup"><span data-stu-id="8babb-163">In this case the session name will be **Session:** followed by the name of the account record that is displayed in the session.</span></span>|  
  
   <span data-ttu-id="8babb-164">![Define session tab name text and format](../unified-service-desk/media/crm-itpro-usd-wt05-02.png "Define session tab name text and format")</span><span class="sxs-lookup"><span data-stu-id="8babb-164">![Define session tab name text and format](../unified-service-desk/media/crm-itpro-usd-wt05-02.png "Define session tab name text and format")</span></span>  
  
6. <span data-ttu-id="8babb-165">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8babb-165">Click **Save**.</span></span>  
  
<a name="Step3"></a>   
## <a name="step-3-define-session-overview-information"></a><span data-ttu-id="8babb-166">Bước 3: Xác định thông tin tổng quan về phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-166">Step 3: Define session overview information</span></span>  
 <span data-ttu-id="8babb-167">Xác định thông tin tổng quan phiên để hiển thị trong loại **Dòng phiên** của kiểm soát điều khiển mà bạn đã đặt cấu hình trong bước 1.</span><span class="sxs-lookup"><span data-stu-id="8babb-167">Define the session overview information to display in the **Session Lines** type of hosted control that you configured in step 1.</span></span>  
  
1. <span data-ttu-id="8babb-168">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8babb-168">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="8babb-169">Click **Session Lines**.</span><span class="sxs-lookup"><span data-stu-id="8babb-169">Click **Session Lines**.</span></span>  
  
4. <span data-ttu-id="8babb-170">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="8babb-170">Click **New**.</span></span>  
  
5. <span data-ttu-id="8babb-171">Trên trang **Thông tin phiên mới**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="8babb-171">On the **New Session Information** page, specify the following values.</span></span>  
  
   - <span data-ttu-id="8babb-172">**Order**: Any random value; say 6.</span><span class="sxs-lookup"><span data-stu-id="8babb-172">**Order**: Any random value; say 6.</span></span>  
  
   - <span data-ttu-id="8babb-173">**Name**: Contoso Session Overview Info</span><span class="sxs-lookup"><span data-stu-id="8babb-173">**Name**: Contoso Session Overview Info</span></span>  
  
   - <span data-ttu-id="8babb-174">**Selected Entity**: account</span><span class="sxs-lookup"><span data-stu-id="8babb-174">**Selected Entity**: account</span></span>  
  
   - <span data-ttu-id="8babb-175">**Type**: Session Overview</span><span class="sxs-lookup"><span data-stu-id="8babb-175">**Type**: Session Overview</span></span>  
  
   - <span data-ttu-id="8babb-176">**Display**:</span><span class="sxs-lookup"><span data-stu-id="8babb-176">**Display**:</span></span>  
  
       ```xaml  
       <Grid Margin="0"      xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"      xmlns:CCA="clr-namespace:Microsoft.Crm.UnifiedServiceDesk.Dynamics;assembly=Microsoft.Crm.UnifiedServiceDesk.Dynamics">  
         <Grid.RowDefinitions>  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
           <RowDefinition Height="auto" />  
         </Grid.RowDefinitions>  
         <Grid.ColumnDefinitions>  
           <ColumnDefinition Width="80"/>  
           <ColumnDefinition Width="*" />  
           <ColumnDefinition Width="auto" />  
         </Grid.ColumnDefinitions>  
         <TextBlock Margin="5,0,0,0" Grid.Row="0" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="Primary Contact: [[account.primarycontactid.name]x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="1" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Text="[[account.address1_line1]x]"/>  
         <TextBlock Margin="5,0,0,0" Grid.Row="2" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_line2]+x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="3" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_line3]+x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="4" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="[[account.address1_city]x], [[account.address1_stateorprovince]x] [[account.address1_postalcode]x]" />  
         <TextBlock Margin="5,0,0,0" Grid.Row="5" TextWrapping="Wrap" Padding="3,0,0,3" Grid.ColumnSpan="3" FontFamily="Tohoma" FontSize="14" Style="{DynamicResource AutoCollapse}" Text="Phone: [[account.telephone1]x]" />  
       </Grid>  
       ```  
  
       > [!NOTE]
       >  <span data-ttu-id="8babb-177">Mẫu này sử dụng tham số XAML và thay thế để xác định thông tin tổng quan phiên mà hiển thị số điện thoại, địa chỉ và liên hệ chính của tài khoản hiện tại trong vùng tổng quan về phiên.</span><span class="sxs-lookup"><span data-stu-id="8babb-177">This sample uses XAML and replacement parameters to define the session overview information that displays the current account’s primary contact, address, and phone number in the session overview area.</span></span>  
  
   <span data-ttu-id="8babb-178">![Define session overview information](../unified-service-desk/media/crm-itpro-usd-wt05-03.png "Define session overview information")</span><span class="sxs-lookup"><span data-stu-id="8babb-178">![Define session overview information](../unified-service-desk/media/crm-itpro-usd-wt05-03.png "Define session overview information")</span></span>  
  
6. <span data-ttu-id="8babb-179">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8babb-179">Click **Save**.</span></span>  
  
<a name="Step4"></a>   
## <a name="step-4-add-the-controls-to-the-configuration"></a><span data-ttu-id="8babb-180">Step 4: Add the controls to the configuration</span><span class="sxs-lookup"><span data-stu-id="8babb-180">Step 4: Add the controls to the configuration</span></span>  
 <span data-ttu-id="8babb-181">Trong bước này, bạn sẽ thêm kiểm soát tổ chức và nguyên tắc dòng phiên đã cấu hình trong cách này vào **Cấu hình Contoso** để hiển thị các kiểm soát này cho người dùng được chỉ định cho cấu hình này.</span><span class="sxs-lookup"><span data-stu-id="8babb-181">In this step, you’ll add the hosted control and session line rules that were configured in this walkthrough to **Contoso Configuration** to display these controls to the user who is assigned to the configuration.</span></span> <span data-ttu-id="8babb-182">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="8babb-182">**Contoso Configuration** was created in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span>  
  
 <span data-ttu-id="8babb-183">Add the following to **Contoso Configuration**.</span><span class="sxs-lookup"><span data-stu-id="8babb-183">Add the following to **Contoso Configuration**.</span></span>  
  
|<span data-ttu-id="8babb-184">Tên kiểm soát</span><span class="sxs-lookup"><span data-stu-id="8babb-184">Control name</span></span>|<span data-ttu-id="8babb-185">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="8babb-185">Control type</span></span>|  
|------------------|------------------|  
|<span data-ttu-id="8babb-186">Tổng quan về phiên contoso</span><span class="sxs-lookup"><span data-stu-id="8babb-186">Contoso Session Overview</span></span>|<span data-ttu-id="8babb-187">Kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="8babb-187">Hosted Control</span></span>|  
|<span data-ttu-id="8babb-188">Tên phiên Contoso</span><span class="sxs-lookup"><span data-stu-id="8babb-188">Contoso Session Name</span></span>|<span data-ttu-id="8babb-189">Dòng Phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-189">Session Line</span></span>|  
|<span data-ttu-id="8babb-190">Thông tin Tổng quan về phiên contoso</span><span class="sxs-lookup"><span data-stu-id="8babb-190">Contoso Session Overview Info</span></span>|<span data-ttu-id="8babb-191">Dòng Phiên</span><span class="sxs-lookup"><span data-stu-id="8babb-191">Session Line</span></span>|  
  
 <span data-ttu-id="8babb-192">To add a control to the configuration:</span><span class="sxs-lookup"><span data-stu-id="8babb-192">To add a control to the configuration:</span></span>  
  
1. <span data-ttu-id="8babb-193">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="8babb-193">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  
  
3. <span data-ttu-id="8babb-194">Bấm **Cấu hình**.</span><span class="sxs-lookup"><span data-stu-id="8babb-194">Click **Configuration**.</span></span>  
  
4. <span data-ttu-id="8babb-195">Click **Contoso Configuration** to open the definition.</span><span class="sxs-lookup"><span data-stu-id="8babb-195">Click **Contoso Configuration** to open the definition.</span></span>  
  
5. <span data-ttu-id="8babb-196">Trên thanh điều hướng, nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso** và chọn **Kiểm soát tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="8babb-196">On the nav bar, click the down arrow next to **Contoso Configuration**, and select **Hosted Controls**.</span></span>  
  
6. <span data-ttu-id="8babb-197">Trên trang tiếp theo, bấm vào **Thêm Kiểm soát Tổ chức Hiện có**, nhập “`Contoso Session Overview`” vào thanh tìm kiếm, rồi nhấn ENTER hoặc bấm vào biểu tượng tìm kiếm.</span><span class="sxs-lookup"><span data-stu-id="8babb-197">On the next page, click **Add Existing Hosted Control**, type “`Contoso Session Overview`” in the search bar, and then press ENTER or click the search icon.</span></span>  
  
7. <span data-ttu-id="8babb-198">Trong hộp kết quả tìm kiếm, hãy nhấp vào kiểm soát tổ chức để thêm vào **Cấu hình Contoso**.</span><span class="sxs-lookup"><span data-stu-id="8babb-198">In the search result box, click the hosted control to add it to **Contoso Configuration**.</span></span>  
  
8. <span data-ttu-id="8babb-199">Tương tự, thêm kiểm soát dòng phiên bằng cách nhấp vào mũi tên xuống bên cạnh **Cấu hình Contoso**, và nhấp vào **Dòng phiên**.</span><span class="sxs-lookup"><span data-stu-id="8babb-199">Similarly, add the session line controls by clicking the down arrow next to **Contoso Configuration**, and clicking **Session Lines**.</span></span>  
  
9. <span data-ttu-id="8babb-200">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="8babb-200">Click **Save**.</span></span>  
  
<a name="Step5"></a>   
## <a name="step-5-test-the-application"></a><span data-ttu-id="8babb-201">Bước 5: Kiểm tra ứng dụng</span><span class="sxs-lookup"><span data-stu-id="8babb-201">Step 5: Test the application</span></span>  
  
1. <span data-ttu-id="8babb-202">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span><span class="sxs-lookup"><span data-stu-id="8babb-202">Start the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, and sign in to the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance where you configured [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] by using the same user credentials that is assigned to Contoso Configuration in [Walkthrough 1: Build a simple agent application](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md).</span></span> <span data-ttu-id="8babb-203">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span><span class="sxs-lookup"><span data-stu-id="8babb-203">For information about connecting to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance using the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application, see [Connect to a Dynamics 365 for Customer Engagement apps instance using the Unified Service Desk client](../unified-service-desk/admin/connect-dynamics-365-instance-using-unified-service-desk-client.md)</span></span>  
  
2. <span data-ttu-id="8babb-204">Click the down arrow next to the **Search** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span><span class="sxs-lookup"><span data-stu-id="8babb-204">Click the down arrow next to the **Search** button in the toolbar, and then click **Account** to display the account records from your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance.</span></span>  
  
3. <span data-ttu-id="8babb-205">Click the expander to display the left pane (SessionExplorerPanel).</span><span class="sxs-lookup"><span data-stu-id="8babb-205">Click the expander to display the left pane (SessionExplorerPanel).</span></span>  
  
   <span data-ttu-id="8babb-206">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="8babb-206">![Choose the expander in Unified Service Desk](../unified-service-desk/media/usd-choose-expander.png "Choose the expander in Unified Service Desk")</span></span>  
  
4. <span data-ttu-id="8babb-207">Nhấp vào bất kỳ hồ sơ tài khoản nào để hiện thị thông tin tài khoản tương ứng trong phiên trong ứng dụng tổng đài viên.</span><span class="sxs-lookup"><span data-stu-id="8babb-207">Click any of the account records to display the respective account information in a session in the agent application.</span></span> <span data-ttu-id="8babb-208">Lưu ý rằng tên của tab phiên hiển thị từ **phiên:** theo sau là tên tài khoản hiện tại.</span><span class="sxs-lookup"><span data-stu-id="8babb-208">Note that the name of the session tab automatically displays the word **Session:** followed by the current account name.</span></span> <span data-ttu-id="8babb-209">Ngăn trái hiển thị các thông tin tổng quan về phiên đã được xác định trước đó.</span><span class="sxs-lookup"><span data-stu-id="8babb-209">The left pane displays the session overview information that was defined earlier.</span></span>  
  
   <span data-ttu-id="8babb-210">![Session name and overview information](../unified-service-desk/media/crm-itpro-usd-wt05-05.png "Session name and overview information")</span><span class="sxs-lookup"><span data-stu-id="8babb-210">![Session name and overview information](../unified-service-desk/media/crm-itpro-usd-wt05-05.png "Session name and overview information")</span></span>  
  
5. <span data-ttu-id="8babb-211">If you open another account record, it will be displayed in another session in your client application.</span><span class="sxs-lookup"><span data-stu-id="8babb-211">If you open another account record, it will be displayed in another session in your client application.</span></span> <span data-ttu-id="8babb-212">To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.</span><span class="sxs-lookup"><span data-stu-id="8babb-212">To open another account, click the down arrow next to the **Search** button, click **Account**, and then click an account name to display the account information in another session.</span></span>  
  
   <span data-ttu-id="8babb-213">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt05-06.png "Multiple sessions in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="8babb-213">![Multiple sessions in Unified Service Desk](../unified-service-desk/media/crm-itpro-usd-wt05-06.png "Multiple sessions in Unified Service Desk")</span></span>  
  
<a name="Conclusion"></a>   
## <a name="conclusion"></a><span data-ttu-id="8babb-214">Kết luận</span><span class="sxs-lookup"><span data-stu-id="8babb-214">Conclusion</span></span>  
 <span data-ttu-id="8babb-215">Trong cách này, bạn biết cách sử dụng nguyên tắc cấu hình dòng phiên để hiển thị tên tab phiên và thông tin tổng quan tính theo ngữ cảnh về hồ sơ trong phiên trong ứng dụng tổng đài viên của mình.</span><span class="sxs-lookup"><span data-stu-id="8babb-215">In this walkthrough, you saw how to use the session lines configuration rules to contextually display the session tab name and key overview information about the record in a session in your agent application.</span></span> <span data-ttu-id="8babb-216">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span><span class="sxs-lookup"><span data-stu-id="8babb-216">You also learned how to filter access to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] controls using configuration.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="8babb-217">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="8babb-217">See also</span></span>  
 [<span data-ttu-id="8babb-218">Walkthrough 1: Build a simple agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-218">Walkthrough 1: Build a simple agent application</span></span>](../unified-service-desk/walkthrough-1-build-a-simple-agent-application.md)   
 
 [<span data-ttu-id="8babb-219">Walkthrough 2: Display an external webpage in your agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-219">Walkthrough 2: Display an external webpage in your agent application</span></span>](../unified-service-desk/walkthrough-2-display-an-external-webpage-in-your-agent-application.md)   
 
 [<span data-ttu-id="8babb-220">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-220">Walkthrough 3: Display Microsoft Dynamics 365 for Customer Engagement apps records in your agent application</span></span>](../unified-service-desk/walkthrough-3-display-microsoft-dynamics-365-records-in-your-agent-application.md)   
 
 [<span data-ttu-id="8babb-221">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-221">Walkthrough 4: Display a Microsoft Dynamics 365 for Customer Engagement apps record in a session in your agent application</span></span>](../unified-service-desk/walkthrough-display-dynamics-365-record-session-agent-application.md)   
 
 [<span data-ttu-id="8babb-222">Walkthrough 6: Configure the Debugger hosted control in your agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-222">Walkthrough 6: Configure the Debugger hosted control in your agent application</span></span>](../unified-service-desk/walkthrough-configure-debugger-hosted-control-agent-application.md)   
 
 [<span data-ttu-id="8babb-223">Walkthrough 7: Configure agent scripting in your agent application</span><span class="sxs-lookup"><span data-stu-id="8babb-223">Walkthrough 7: Configure agent scripting in your agent application</span></span>](../unified-service-desk/walkthrough-configure-agent-scripting-agent-application.md)   
 
 [<span data-ttu-id="8babb-224">Unified Service Desk Configuration Walkthroughs</span><span class="sxs-lookup"><span data-stu-id="8babb-224">Unified Service Desk Configuration Walkthroughs</span></span>](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md)
