---
title: 'Walkthrough: Create a UII Application Adapter in Unified Service Desk fopr Dynamics 365 for Customer Engagement| MicrosoftDocs'
description: Demonstrates how to host and interact with an external application in Unified Service Desk.
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
ms.assetid: f280285b-2284-40a8-a01d-ea24a65926c9
caps.latest.revision: 9
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: bd9292ad1011decbb1d808138ffd6498ca086aa6
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "388237"
---
# <a name="walkthrough-create-a-uii-application-adapter"></a><span data-ttu-id="2d283-103">Walkthrough: Create a UII Application Adapter</span><span class="sxs-lookup"><span data-stu-id="2d283-103">Walkthrough: Create a UII Application Adapter</span></span>
<span data-ttu-id="2d283-104">You can create an application adapter if you want to integrate an external application with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-104">You can create an application adapter if you want to integrate an external application with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="2d283-105">apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating an application adapter.</span><span class="sxs-lookup"><span data-stu-id="2d283-105">apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating an application adapter.</span></span> <span data-ttu-id="2d283-106">Mẫu này cung cấp mã cơ bản như nhận xét để giúp bạn bắt đầu với việc tạo bộ chuyển đổi ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="2d283-106">The template provides basic code as comments to help you get started with creating the application adapter.</span></span>  
  
 <span data-ttu-id="2d283-107">Trong cách này, bạn sẽ xây dựng một ứng dụng bên ngoài `QsExternalApp` và lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-107">In this walkthrough, you’ll build an external application `QsExternalApp` and host it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="2d283-108">Sau đó, bạn sẽ tạo và cấu hình bộ chuyển đổi ứng dụng được gọi là `ExternalApplicationAdapter` cho ứng dụng bên ngoài để tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-108">You’ll then create and configure an application adapter `ExternalApplicationAdapter` for the external application to interact with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="2d283-109">Ứng dụng bên ngoài có bốn nhãn: mỗi nhãn cho tên, họ, địa chỉ và ID của khách hàng và bốn hộp văn bản tương ứng để hiển thị các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-109">The external application has four labels: one each for the customer’s first name, last name, address and ID and four corresponding text boxes to display the values from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="2d283-110">In This Section</span><span class="sxs-lookup"><span data-stu-id="2d283-110">In This Section</span></span>  
 [<span data-ttu-id="2d283-111">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2d283-111">Prerequisites</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#Prereq)  
  
 [<span data-ttu-id="2d283-112">Bước 1: Xây dựng ứng dụng bên ngoài mẫu</span><span class="sxs-lookup"><span data-stu-id="2d283-112">Step 1: Build a sample external application</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#CreateExternalApp)  
  
 [<span data-ttu-id="2d283-113">Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="2d283-113">Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#ConfigureExApp)  
  
 [<span data-ttu-id="2d283-114">Bước 3: Kiểm tra ứng dụng bên ngoài</span><span class="sxs-lookup"><span data-stu-id="2d283-114">Step 3: Test the external application</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#TestExApp)  
  
 [<span data-ttu-id="2d283-115">Bước 4: Tạo bộ chuyển đổi ứng dụng</span><span class="sxs-lookup"><span data-stu-id="2d283-115">Step 4: Create the application adapter</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#CreateAppAdapter)  
  
 [<span data-ttu-id="2d283-116">Step 5: Configure the application adapter in Microsoft Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="2d283-116">Step 5: Configure the application adapter in Microsoft Dynamics 365 for Customer Engagement apps</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#ConfigureAppAdapter)  
  
 [<span data-ttu-id="2d283-117">Bước 6: Thử nghiệm bộ chuyển đổi ứng dụng</span><span class="sxs-lookup"><span data-stu-id="2d283-117">Step 6: Test the application adapter</span></span>](../unified-service-desk/walkthrough-create-uii-application-adapter.md#TestAppAdapter)  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="2d283-118">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="2d283-118">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="2d283-119">4.5.2</span><span class="sxs-lookup"><span data-stu-id="2d283-119">4.5.2</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="2d283-120">client application; required for testing the hosted control.</span><span class="sxs-lookup"><span data-stu-id="2d283-120">client application; required for testing the hosted control.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="2d283-121">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="2d283-121">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] <span data-ttu-id="2d283-122">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="2d283-122">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="2d283-123">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template.</span><span class="sxs-lookup"><span data-stu-id="2d283-123">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template.</span></span> <span data-ttu-id="2d283-124">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-124">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
<a name="CreateExternalApp"></a>   
## <a name="step-1-build-a-sample-external-application"></a><span data-ttu-id="2d283-125">Bước 1: Xây dựng ứng dụng bên ngoài mẫu</span><span class="sxs-lookup"><span data-stu-id="2d283-125">Step 1: Build a sample external application</span></span>  
  
1. <span data-ttu-id="2d283-126">[Tải xuống gói UII SDK](http://go.microsoft.com/fwlink/p/?LinkId=519179).</span><span class="sxs-lookup"><span data-stu-id="2d283-126">[Download the UII SDK package](http://go.microsoft.com/fwlink/p/?LinkId=519179).</span></span>  
  
2. <span data-ttu-id="2d283-127">Double-click the package file to extract the contents.</span><span class="sxs-lookup"><span data-stu-id="2d283-127">Double-click the package file to extract the contents.</span></span>  
  
3. <span data-ttu-id="2d283-128">Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsExternalApp folder, and open the Microsoft.Uii.QuickStarts.QsExternalApp.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-128">Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsExternalApp folder, and open the Microsoft.Uii.QuickStarts.QsExternalApp.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
4. <span data-ttu-id="2d283-129">Press F5 or choose **Debug** > **Start Debugging** to create a sample external application.</span><span class="sxs-lookup"><span data-stu-id="2d283-129">Press F5 or choose **Debug** > **Start Debugging** to create a sample external application.</span></span> <span data-ttu-id="2d283-130">The application (Microsoft.Uii.QuickStarts.QsExternalApp.exe) is created in the /bin/debug folder of the project.</span><span class="sxs-lookup"><span data-stu-id="2d283-130">The application (Microsoft.Uii.QuickStarts.QsExternalApp.exe) is created in the /bin/debug folder of the project.</span></span>  
  
   <span data-ttu-id="2d283-131">![Sample external app](../unified-service-desk/media/usd-sample-external-app.PNG "Sample external app")</span><span class="sxs-lookup"><span data-stu-id="2d283-131">![Sample external app](../unified-service-desk/media/usd-sample-external-app.PNG "Sample external app")</span></span>  
  
<a name="ConfigureExApp"></a>   
## <a name="step-2-configure-the-external-application-in-microsoft-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="2d283-132">Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="2d283-132">Step 2: Configure the external application in Microsoft Dynamics 365 for Customer Engagement apps.</span></span>  
 <span data-ttu-id="2d283-133">Trong bước này, bạn sẽ tạo kiểm soát tổ chức của loại **Ứng dụng Được lưu trữ Bên ngoài** để hiển thị ứng dụng biểu mẫu [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-133">In this step, you will create a hosted control of **External Hosted Application** type to display the [!INCLUDE[pn_ms_Windows_short](../includes/pn-ms-windows-short.md)] forms application.</span></span>  
  
1. <span data-ttu-id="2d283-134">Đăng nhập vào **Microsoft Dynamics 365 for Customer Engagement**.</span><span class="sxs-lookup"><span data-stu-id="2d283-134">Sign in to **Microsoft Dynamics 365 for Customer Engagement**.</span></span>  
  
2. <span data-ttu-id="2d283-135">Trên thanh điều hướng, bấm hoặc chạm vào **Microsoft Dynamics 365 for Customer Engagement**, rồi chọn **Thiết đặt**.</span><span class="sxs-lookup"><span data-stu-id="2d283-135">On the navigation bar, click or tap **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="2d283-136">Click or tap **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="2d283-136">Click or tap **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="2d283-137">Bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="2d283-137">Click **New**.</span></span>  
  
5. <span data-ttu-id="2d283-138">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="2d283-138">On the **New Hosted Control** page, specify the following values:</span></span>  
  
   |<span data-ttu-id="2d283-139">Trường</span><span class="sxs-lookup"><span data-stu-id="2d283-139">Field</span></span>|<span data-ttu-id="2d283-140">Value</span><span class="sxs-lookup"><span data-stu-id="2d283-140">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="2d283-141">Tên</span><span class="sxs-lookup"><span data-stu-id="2d283-141">Name</span></span>|<span data-ttu-id="2d283-142">QsExternalApp</span><span class="sxs-lookup"><span data-stu-id="2d283-142">QsExternalApp</span></span>|  
   |<span data-ttu-id="2d283-143">Thành phần USD</span><span class="sxs-lookup"><span data-stu-id="2d283-143">USD Component</span></span>|<span data-ttu-id="2d283-144">CCA Hosted Application</span><span class="sxs-lookup"><span data-stu-id="2d283-144">CCA Hosted Application</span></span>|  
   |<span data-ttu-id="2d283-145">Ứng dụng được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="2d283-145">Hosted Application</span></span>|<span data-ttu-id="2d283-146">Ứng dụng được lưu trữ bên ngoài</span><span class="sxs-lookup"><span data-stu-id="2d283-146">External Hosted Application</span></span>|  
   |<span data-ttu-id="2d283-147">Application is Global</span><span class="sxs-lookup"><span data-stu-id="2d283-147">Application is Global</span></span>|<span data-ttu-id="2d283-148">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="2d283-148">Checked</span></span>|  
   |<span data-ttu-id="2d283-149">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="2d283-149">Display Group</span></span>|<span data-ttu-id="2d283-150">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="2d283-150">MainPanel</span></span>|  
   |<span data-ttu-id="2d283-151">Bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="2d283-151">Adapter</span></span>|<span data-ttu-id="2d283-152">Use No Adapter</span><span class="sxs-lookup"><span data-stu-id="2d283-152">Use No Adapter</span></span>|  
   |<span data-ttu-id="2d283-153">Application is Dynamic</span><span class="sxs-lookup"><span data-stu-id="2d283-153">Application is Dynamic</span></span>|<span data-ttu-id="2d283-154">Không</span><span class="sxs-lookup"><span data-stu-id="2d283-154">No</span></span>|  
   |<span data-ttu-id="2d283-155">URI ứng dụng bên ngoài</span><span class="sxs-lookup"><span data-stu-id="2d283-155">External App URI</span></span>|<span data-ttu-id="2d283-156">Microsoft.Uii.QuickStarts.QsExternalApp.exe</span><span class="sxs-lookup"><span data-stu-id="2d283-156">Microsoft.Uii.QuickStarts.QsExternalApp.exe</span></span>|  
  
   <span data-ttu-id="2d283-157">![Application adapter configuration screen](../unified-service-desk/media/usd-external-app-config-1.PNG "Application adapter configuration screen")</span><span class="sxs-lookup"><span data-stu-id="2d283-157">![Application adapter configuration screen](../unified-service-desk/media/usd-external-app-config-1.PNG "Application adapter configuration screen")</span></span>  
  
   <span data-ttu-id="2d283-158">![Unified Service Desk external app hosting settings](../unified-service-desk/media/usd-externa-app-config-2.PNG "Unified Service Desk external app hosting settings")</span><span class="sxs-lookup"><span data-stu-id="2d283-158">![Unified Service Desk external app hosting settings](../unified-service-desk/media/usd-externa-app-config-2.PNG "Unified Service Desk external app hosting settings")</span></span>  
  
6. <span data-ttu-id="2d283-159">Bấm vào **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="2d283-159">Click **Save**.</span></span>  
  
<a name="TestExApp"></a>   
## <a name="step-3-test-the-external-application"></a><span data-ttu-id="2d283-160">Bước 3: Kiểm tra ứng dụng bên ngoài</span><span class="sxs-lookup"><span data-stu-id="2d283-160">Step 3: Test the external application</span></span>  
  
1. <span data-ttu-id="2d283-161">Copy the application from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span><span class="sxs-lookup"><span data-stu-id="2d283-161">Copy the application from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span></span> <span data-ttu-id="2d283-162">In this case, we will copy the Microsoft.Uii.QuickStarts.QsExternalApp.exefile to the C:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span><span class="sxs-lookup"><span data-stu-id="2d283-162">In this case, we will copy the Microsoft.Uii.QuickStarts.QsExternalApp.exefile to the C:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span></span>  
  
2. <span data-ttu-id="2d283-163">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="2d283-163">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span></span>  
  
3. <span data-ttu-id="2d283-164">Trên lần đăng nhập thành công, bạn sẽ thấy nút **Ứng dụng Bên ngoài Mẫu** trên màn hình nền.</span><span class="sxs-lookup"><span data-stu-id="2d283-164">On successful sign in, you’ll see the **Sample External Application** button on your desktop.</span></span>  
  
4. <span data-ttu-id="2d283-165">Chọn **Ứng dụng Bên ngoài Mẫu** để xem ứng dụng bên ngoài được lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-165">Choose **Sample External Application** to see your external application hosted within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   <span data-ttu-id="2d283-166">![Sample external app in Unified Service Desk](../unified-service-desk/media/usd-sample-external-app-1.PNG "Sample external app in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="2d283-166">![Sample external app in Unified Service Desk](../unified-service-desk/media/usd-sample-external-app-1.PNG "Sample external app in Unified Service Desk")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2d283-167">Tại thời điểm này, các trường trống vì bạn chỉ lưu trữ ứng dụng trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-167">At this point the fields are empty as you’re only hosting the application in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="2d283-168">Để điền các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải tạo bộ chuyển đổi ứng dụng như được mô tả trong bước tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="2d283-168">To populate them with values from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you’ll have to create an application adapter as described in the next step.</span></span>  
  
<a name="CreateAppAdapter"></a>   
## <a name="step-4-create-the-application-adapter"></a><span data-ttu-id="2d283-169">Bước 4: Tạo bộ chuyển đổi ứng dụng</span><span class="sxs-lookup"><span data-stu-id="2d283-169">Step 4: Create the application adapter</span></span>  
  
1. <span data-ttu-id="2d283-170">Bắt đầu [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] và tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="2d283-170">Start [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="2d283-171">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="2d283-171">In the **New Project** dialog box:</span></span>  
  
   1. <span data-ttu-id="2d283-172">From the list of installed templates, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select Dynamics 365 for Customer Engagement apps SDK Templates > **Unified Service Desk** > [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Application Adapter</span><span class="sxs-lookup"><span data-stu-id="2d283-172">From the list of installed templates, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select Dynamics 365 for Customer Engagement apps SDK Templates > **Unified Service Desk** > [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Application Adapter</span></span>  
  
   2. <span data-ttu-id="2d283-173">Specify the name and location of the project, and click **OK** to create a new project.</span><span class="sxs-lookup"><span data-stu-id="2d283-173">Specify the name and location of the project, and click **OK** to create a new project.</span></span>  
  
   <span data-ttu-id="2d283-174">![External application adapter in Visual Studio](../unified-service-desk/media/usd-external-app-adapter-vs.PNG "External application adapter in Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="2d283-174">![External application adapter in Visual Studio](../unified-service-desk/media/usd-external-app-adapter-vs.PNG "External application adapter in Visual Studio")</span></span>  
  
3. <span data-ttu-id="2d283-175">Trong Trình khám phá Giải pháp, mở rộng phần Tham khảo để đảm bảo tất cả tham khảo cụm tổ hợp giải quyết chính xác.</span><span class="sxs-lookup"><span data-stu-id="2d283-175">In Solution Explorer, expand the References section to ensure all the assembly references resolve correctly.</span></span>  
  
4. <span data-ttu-id="2d283-176">Open the AppAdapter.cs file and add the following lines of code to set the locations for each component on the page in the class definition.</span><span class="sxs-lookup"><span data-stu-id="2d283-176">Open the AppAdapter.cs file and add the following lines of code to set the locations for each component on the page in the class definition.</span></span>  
  
   ```csharp  
   // Set up your locations for each component on the page.  
           // If you wish, you could use Spy++ to get the actual names as well.  
           // First Name text box  
           int intFirstNameCoordX = 47;  
           int intFirstNameCoordY = 32;  
           // Last Name text box  
           int intLastNameCoordX = 223;  
           int intLastNameCoordY = 32;  
           // Address Text box  
           int intAddressCoordX = 47;  
           int intAddressCoordY = 81;  
           // Customer ID text box  
           int intIDCoordX = 47;  
           int intIDCoordY = 126;  
   ```  
  
5. <span data-ttu-id="2d283-177">Thêm mã sau đây vào định nghĩa `NotifyContextChange` để thông báo cho ứng dụng rằng ngữ cảnh đã thay đổi.</span><span class="sxs-lookup"><span data-stu-id="2d283-177">Add the following code to the definition of `NotifyContextChange` to notify the application that the context has changed.</span></span> <span data-ttu-id="2d283-178">For more information, see [Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))</span><span class="sxs-lookup"><span data-stu-id="2d283-178">For more information, see [Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))</span></span>  
  
   ```csharp  
   public override bool NotifyContextChange(Context context)  
           {  
               IntPtr ptr = MainWindowHandle;  
               // Find the control (first name) by position  
               IntPtr childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intFirstNameCoordX, intFirstNameCoordY));  
               // Fill data out  
               Win32API.SetWindowTextAny(childHwnd, context["firstname"]);  
               // Find the control (last name) by position  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intLastNameCoordX, intLastNameCoordY));  
               // Fill out the data  
               Win32API.SetWindowTextAny(childHwnd, context["lastname"]);  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intAddressCoordX, intAddressCoordY));  
               Win32API.SetWindowTextAny(childHwnd, context["address1_line1"]);  
               childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intIDCoordX, intIDCoordY));  
               Win32API.SetWindowTextAny(childHwnd, context["CustomerID"]);  
               // Hands control back over to the base class to notify next app of context change.  
               return base.NotifyContextChange(context);  
  
           }  
   ```  
  
6. <span data-ttu-id="2d283-179">Thêm mã sau vào định nghĩa thay thế của `DoAction` để cập nhật các trường biểu mẫu với các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="2d283-179">Add the following code to the override definition of `DoAction` to update the form fields with values from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   ```csharp  
   public override bool DoAction(Microsoft.Uii.Csr.Action action, RequestActionEventArgs args)  
           {  
               IntPtr ptr;  
               IntPtr childHwnd;  
               switch (args.Action)  
               {  
                   case "UpdateFirstName":  
                       // Get locations of what you want to update and handles  
                       ptr = MainWindowHandle;  
                       childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intFirstNameCoordX, intFirstNameCoordY));  
                       // Populate data into fields  
                       Win32API.SetWindowTextAny(childHwnd, args.Data);  
                       break;  
                   case "UpdateLastName":  
                       // Get locations of what you want to update and handles  
                       ptr = MainWindowHandle;  
                       childHwnd = Win32API.FindWindowByPosition(ptr, new Point(intLastNameCoordX, intLastNameCoordY));  
                       // Populate data into fields  
                       Win32API.SetWindowTextAny(childHwnd, args.Data);  
                       break;  
               }  
               return base.DoAction(action, args);  
           }  
   ```  
  
7. <span data-ttu-id="2d283-180">Save your project, and build it (**Build** > **Build Solution**).</span><span class="sxs-lookup"><span data-stu-id="2d283-180">Save your project, and build it (**Build** > **Build Solution**).</span></span> <span data-ttu-id="2d283-181">After the project builds successfully, an assembly (ExternalApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder.</span><span class="sxs-lookup"><span data-stu-id="2d283-181">After the project builds successfully, an assembly (ExternalApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder.</span></span> <span data-ttu-id="2d283-182">Bạn sẽ cần cụm tổ hợp này sau để kiểm tra và sử dụng bộ chuyển đổi ứng dụng của mình.</span><span class="sxs-lookup"><span data-stu-id="2d283-182">You’ll need this assembly later for testing and using your application adapter.</span></span>  
  
<a name="ConfigureAppAdapter"></a>   
## <a name="step-4-configure-the-application-adapter-in-dynamics-365-for-customer-engagement"></a><span data-ttu-id="2d283-183">Step 4: Configure the application adapter in Dynamics 365 for Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="2d283-183">Step 4: Configure the application adapter in Dynamics 365 for Customer Engagement</span></span>  
  
1. <span data-ttu-id="2d283-184">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="2d283-184">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="2d283-185">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="2d283-185">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span></span>  
  
3. <span data-ttu-id="2d283-186">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="2d283-186">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="2d283-187">Từ danh sách kiểm soát tổ chức, chọn kiểm soát tổ chức `QsExternalApp`.</span><span class="sxs-lookup"><span data-stu-id="2d283-187">From the list of hosted controls, select the `QsExternalApp` hosted control.</span></span>  
  
   <span data-ttu-id="2d283-188">![Hosted control in Unified Service Desk](../unified-service-desk/media/usd-external-app-hosted-control.PNG "Hosted control in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="2d283-188">![Hosted control in Unified Service Desk](../unified-service-desk/media/usd-external-app-hosted-control.PNG "Hosted control in Unified Service Desk")</span></span>  
  
5. <span data-ttu-id="2d283-189">Trong phần Cấu hình Bộ chuyển đổi, chỉ định các giá trị sau:</span><span class="sxs-lookup"><span data-stu-id="2d283-189">In the Adapter Configuration section, specify the following values:</span></span>  
  
   |||  
   |-|-|  
   |<span data-ttu-id="2d283-190">Trường</span><span class="sxs-lookup"><span data-stu-id="2d283-190">Field</span></span>|<span data-ttu-id="2d283-191">Value</span><span class="sxs-lookup"><span data-stu-id="2d283-191">Value</span></span>|  
   |<span data-ttu-id="2d283-192">Bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="2d283-192">Adapter</span></span>|<span data-ttu-id="2d283-193">Sử dụng bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="2d283-193">Use Adapter</span></span>|  
   |<span data-ttu-id="2d283-194">URI</span><span class="sxs-lookup"><span data-stu-id="2d283-194">URI</span></span>|`ExternalApplicationAdapter`|  
   |<span data-ttu-id="2d283-195">Loại</span><span class="sxs-lookup"><span data-stu-id="2d283-195">Type</span></span>|`ExternalApplicationAdapter.AppAdapter`|  
  
   <span data-ttu-id="2d283-196">![External adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-external-adapter-config.PNG "External adapter configuration in Dynamics 365 for Customer Engagement")</span><span class="sxs-lookup"><span data-stu-id="2d283-196">![External adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-external-adapter-config.PNG "External adapter configuration in Dynamics 365 for Customer Engagement")</span></span>  
  
   > [!NOTE]
   >  <span data-ttu-id="2d283-197">URI là tên của cụm tổ hợp của bạn và Loại là tên của cụm tổ hợp theo sau bởi dấu chấm (.) sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="2d283-197">URI is the name of your assembly and the Type is the name of your assembly (dll) followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="2d283-198">Trong ví dụ này, tên của cụm tổ hợp là `ExternalApplicationAdapter` và tên của lớp là `AppAdapter`, chính là tên lớp mặc định khi bạn tạo bộ chuyển đổi ứng dụng.</span><span class="sxs-lookup"><span data-stu-id="2d283-198">In this example, the name of the assembly is `ExternalApplicationAdapter` and name of the class is `AppAdapter`, which is the default class name when you create an application adapter.</span></span>  
  
6. <span data-ttu-id="2d283-199">Bấm vào **Lưu** để lưu thay đổi của bạn.</span><span class="sxs-lookup"><span data-stu-id="2d283-199">Click **Save** to save the changes.</span></span>  
  
<a name="TestAppAdapter"></a>   
## <a name="step-5-test-the-application-adapter"></a><span data-ttu-id="2d283-200">Bước 5: Thử nghiệm bộ chuyển đổi ứng dụng</span><span class="sxs-lookup"><span data-stu-id="2d283-200">Step 5: Test the application adapter</span></span>  
  
1. <span data-ttu-id="2d283-201">Copy the assembly that contains your application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span><span class="sxs-lookup"><span data-stu-id="2d283-201">Copy the assembly that contains your application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span></span> <span data-ttu-id="2d283-202">In this case, we will copy the ExternalApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span><span class="sxs-lookup"><span data-stu-id="2d283-202">In this case, we will copy the ExternalApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span></span>  
  
2. <span data-ttu-id="2d283-203">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="2d283-203">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span></span>  
  
3. <span data-ttu-id="2d283-204">Trên lần đăng nhập thành công, bạn sẽ nhìn thấy ứng dụng bên ngoài mẫu trên màn hình của mình.</span><span class="sxs-lookup"><span data-stu-id="2d283-204">On successful sign in, you’ll see the sample external application on your desktop.</span></span>  
  
4. <span data-ttu-id="2d283-205">Choose **Search** and then choose **Contacts** and select a contact.</span><span class="sxs-lookup"><span data-stu-id="2d283-205">Choose **Search** and then choose **Contacts** and select a contact.</span></span> <span data-ttu-id="2d283-206">Trong trường hợp này, chúng tôi sẽ chọn `Patrick Sands`.</span><span class="sxs-lookup"><span data-stu-id="2d283-206">In this case, we’ll select `Patrick Sands`.</span></span>  
  
   <span data-ttu-id="2d283-207">![Contacts list in Unified Service Desk](../unified-service-desk/media/usd-external-app-contacts-list.PNG "Contacts list in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="2d283-207">![Contacts list in Unified Service Desk](../unified-service-desk/media/usd-external-app-contacts-list.PNG "Contacts list in Unified Service Desk")</span></span>  
  
5. <span data-ttu-id="2d283-208">Bấm vào **Ứng dụng Bên ngoài Mẫu** và bạn sẽ nhìn thấy tên, họ, địa chỉ và ID của khách hàng được điền vào.</span><span class="sxs-lookup"><span data-stu-id="2d283-208">Click **Sample External Application** and you’ll see the customer’s first name, last name, address, and ID populated.</span></span>  
  
   <span data-ttu-id="2d283-209">![Customer info in external application](../unified-service-desk/media/usd-external-app-customer-info.PNG "Customer info in external application")</span><span class="sxs-lookup"><span data-stu-id="2d283-209">![Customer info in external application](../unified-service-desk/media/usd-external-app-customer-info.PNG "Customer info in external application")</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="2d283-210">Cách này cho bạn thấy cách hiển thị hoặc đọc dữ liệu từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="2d283-210">This walkthrough demonstrates how to display or read data from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] in the external application.</span></span> <span data-ttu-id="2d283-211">To understand how to update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external application, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="2d283-211">To understand how to update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external application, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2d283-212">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="2d283-212">See also</span></span>  
 [<span data-ttu-id="2d283-213">Use UII adapters to interact with external and web applications</span><span class="sxs-lookup"><span data-stu-id="2d283-213">Use UII adapters to interact with external and web applications</span></span>](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md)
