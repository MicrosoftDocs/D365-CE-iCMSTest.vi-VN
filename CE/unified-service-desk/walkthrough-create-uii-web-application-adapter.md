---
title: 'Walkthrough: Create a UII Web Application Adapter in Unified Service Desk for Dynamics 365 for Customer Engagement apps | MicrosoftDocs'
description: Demonstrates how to host and interact with an external web application in Unified Service Desk.
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
ms.assetid: 0b4f5456-deef-41e9-ac58-13a2a0ce5de2
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 872fd24a73e15fd089a60c96aa836ee59525b061
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387614"
---
# <a name="walkthrough-create-a-uii-web-application-adapter"></a><span data-ttu-id="18c39-103">Walkthrough: Create a UII Web Application Adapter</span><span class="sxs-lookup"><span data-stu-id="18c39-103">Walkthrough: Create a UII Web Application Adapter</span></span>
<span data-ttu-id="18c39-104">You can create a web application adapter if you want to enhance and modify web applications for which you don’t have access to the source code or don’t have permissions to change by using managed code.</span><span class="sxs-lookup"><span data-stu-id="18c39-104">You can create a web application adapter if you want to enhance and modify web applications for which you don’t have access to the source code or don’t have permissions to change by using managed code.</span></span> [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] <span data-ttu-id="18c39-105">apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating a web application adapter.</span><span class="sxs-lookup"><span data-stu-id="18c39-105">apps provides a [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] template for creating a web application adapter.</span></span> <span data-ttu-id="18c39-106">Mẫu này cung cấp mã cơ bản như nhận xét để giúp bạn bắt đầu với việc tạo bộ chuyển đổi ứng dụng web.</span><span class="sxs-lookup"><span data-stu-id="18c39-106">The template provides basic code as comments to help you get started with creating the web application adapter.</span></span>  

 <span data-ttu-id="18c39-107">Trong cách này, bạn sẽ xây dựng một ứng dụng web bên ngoài được gọi là `QsWebApplication` và lưu trữ nó trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="18c39-107">In this walkthrough, you’ll build an external web application called `QsWebApplication` and host it in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="18c39-108">Sau đó, bạn sẽ tạo và cấu hình bộ chuyển đổi ứng dụng web được gọi là `MyWebApplicationAdapter` cho ứng dụng web bên ngoài để tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="18c39-108">You’ll then create and configure a web application adapter called `MyWebApplicationAdapter` for the external web application to interact with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="18c39-109">Ứng dụng web có bốn nhãn, mỗi nhãn cho tên, họ, địa chỉ và ID của khách hàng và bốn hộp văn bản tương ứng để hiển thị các giá trị [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="18c39-109">The web application has four labels, one each for the customer’s first name, last name, address, and ID and four corresponding text boxes to display the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] values.</span></span>  

<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="18c39-110">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="18c39-110">Prerequisites</span></span>  

- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="18c39-111">4.5.2</span><span class="sxs-lookup"><span data-stu-id="18c39-111">4.5.2</span></span>  

- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="18c39-112">client application; required for testing the hosted control.</span><span class="sxs-lookup"><span data-stu-id="18c39-112">client application; required for testing the hosted control.</span></span>  

- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="18c39-113">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="18c39-113">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  

- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] <span data-ttu-id="18c39-114">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="18c39-114">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  

- <span data-ttu-id="18c39-115">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template.</span><span class="sxs-lookup"><span data-stu-id="18c39-115">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII hosted control project template.</span></span> <span data-ttu-id="18c39-116">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="18c39-116">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  

<a name="Build"></a>   
## <a name="step-1-build-a-sample-web-application"></a><span data-ttu-id="18c39-117">Bước 1: Xây dựng một ứng dụng web mẫu</span><span class="sxs-lookup"><span data-stu-id="18c39-117">Step 1: Build a sample web application</span></span>  

1. [<span data-ttu-id="18c39-118">Tải xuống gói UII SDK (.exe)</span><span class="sxs-lookup"><span data-stu-id="18c39-118">Download the UII SDK package (.exe)</span></span>](http://go.microsoft.com/fwlink/p/?LinkId=519179)  

2. <span data-ttu-id="18c39-119">Bấm đúp vào tệp gói để giải nén nội dung.</span><span class="sxs-lookup"><span data-stu-id="18c39-119">Double-click the package file to extract the contents.</span></span>  

3. <span data-ttu-id="18c39-120">Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsWebApplication folder, and open the Microsoft.Uii.QuickStarts.QsWebApplication.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="18c39-120">Navigate to the \<ExtractedFolder>\UII\SampleCode\UII\AIF\QsWebApplication folder, and open the Microsoft.Uii.QuickStarts.QsWebApplication.csproj file in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  

4. <span data-ttu-id="18c39-121">Press F5 or choose **Debug** > **Start Debugging** to host the sample web application locally on your computer.</span><span class="sxs-lookup"><span data-stu-id="18c39-121">Press F5 or choose **Debug** > **Start Debugging** to host the sample web application locally on your computer.</span></span> <span data-ttu-id="18c39-122">The application will be hosted at http://localhost:2627/.</span><span class="sxs-lookup"><span data-stu-id="18c39-122">The application will be hosted at http://localhost:2627/.</span></span>  

   <span data-ttu-id="18c39-123">![Web app in Visual Studio](../unified-service-desk/media/usd-web-app-local-host.png "Web app in Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="18c39-123">![Web app in Visual Studio](../unified-service-desk/media/usd-web-app-local-host.png "Web app in Visual Studio")</span></span>  

<a name="ConfigureExApp"></a>   
## <a name="step-2-configure-the-web-application-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="18c39-124">Step 2: Configure the web application in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="18c39-124">Step 2: Configure the web application in Dynamics 365 for Customer Engagement apps</span></span>

1. <span data-ttu-id="18c39-125">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="18c39-125">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. [!INCLUDE[proc_settings_usd](../includes/proc-settings-usd.md)]  

3. <span data-ttu-id="18c39-126">Chọn **Kiểm soát Tổ chức**.</span><span class="sxs-lookup"><span data-stu-id="18c39-126">Choose **Hosted Controls**.</span></span>  

4. <span data-ttu-id="18c39-127">Chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="18c39-127">Choose **New**.</span></span>  

5. <span data-ttu-id="18c39-128">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="18c39-128">On the **New Hosted Control** page, specify the following values.</span></span>  


   |           <span data-ttu-id="18c39-129">Trường</span><span class="sxs-lookup"><span data-stu-id="18c39-129">Field</span></span>            |                                                 <span data-ttu-id="18c39-130">Value</span><span class="sxs-lookup"><span data-stu-id="18c39-130">Value</span></span>                                                 |
   |----------------------------|-------------------------------------------------------------------------------------------------------|
   |          <span data-ttu-id="18c39-131">**Tên**</span><span class="sxs-lookup"><span data-stu-id="18c39-131">**Name**</span></span>          |                                           <span data-ttu-id="18c39-132">QsWebApplication</span><span class="sxs-lookup"><span data-stu-id="18c39-132">QsWebApplication</span></span>                                            |
   |   <span data-ttu-id="18c39-133">**Loại thành phần USD**</span><span class="sxs-lookup"><span data-stu-id="18c39-133">**USD Component Type**</span></span>   |                                        <span data-ttu-id="18c39-134">CCA Hosted Application</span><span class="sxs-lookup"><span data-stu-id="18c39-134">CCA Hosted Application</span></span>                                         |
   |   <span data-ttu-id="18c39-135">**Ứng dụng được lưu trữ**</span><span class="sxs-lookup"><span data-stu-id="18c39-135">**Hosted Application**</span></span>   |                                        <span data-ttu-id="18c39-136">Ứng dụng web được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="18c39-136">Web Hosted Application</span></span>                                         |
   | <span data-ttu-id="18c39-137">**Ứng dụng toàn cầu**</span><span class="sxs-lookup"><span data-stu-id="18c39-137">**Application is Global**</span></span>  |                                                <span data-ttu-id="18c39-138">Đã kiểm tra</span><span class="sxs-lookup"><span data-stu-id="18c39-138">Checked</span></span>                                                |
   |     <span data-ttu-id="18c39-139">**Nhóm hiển thị**</span><span class="sxs-lookup"><span data-stu-id="18c39-139">**Display Group**</span></span>      |                                               <span data-ttu-id="18c39-140">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="18c39-140">MainPanel</span></span>                                               |
   |        <span data-ttu-id="18c39-141">**Bộ điều hợp**</span><span class="sxs-lookup"><span data-stu-id="18c39-141">**Adapter**</span></span>         |                                            <span data-ttu-id="18c39-142">Không sử dụng bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="18c39-142">Use No Adapter</span></span>                                             |
   | <span data-ttu-id="18c39-143">**Ứng dụng động**</span><span class="sxs-lookup"><span data-stu-id="18c39-143">**Application is Dynamic**</span></span> |                                                  <span data-ttu-id="18c39-144">No</span><span class="sxs-lookup"><span data-stu-id="18c39-144">No</span></span>                                                   |
   |  <span data-ttu-id="18c39-145">**Lưu trữ ứng dụng**</span><span class="sxs-lookup"><span data-stu-id="18c39-145">**Application Hosting**</span></span>   |                                             <span data-ttu-id="18c39-146">Sử dụng SetParent</span><span class="sxs-lookup"><span data-stu-id="18c39-146">Use SetParent</span></span>                                             |
   |          <span data-ttu-id="18c39-147">**URL**</span><span class="sxs-lookup"><span data-stu-id="18c39-147">**URL**</span></span>           | <span data-ttu-id="18c39-148">Xác định vị trí nơi ứng dụng web của bạn được tổ chức.</span><span class="sxs-lookup"><span data-stu-id="18c39-148">Specify the location where your web application is hosted.</span></span> <span data-ttu-id="18c39-149">Trong trường hợp này, đây là http://localhost:2627/</span><span class="sxs-lookup"><span data-stu-id="18c39-149">In this case, it is http://localhost:2627/</span></span> |

   <span data-ttu-id="18c39-150">![Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-crm-config.png "Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps")</span><span class="sxs-lookup"><span data-stu-id="18c39-150">![Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-crm-config.png "Screenshot of Web App Config in Dynamics 365 for Customer Engagement apps")</span></span>  

6. <span data-ttu-id="18c39-151">Chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="18c39-151">Choose **Save**.</span></span>  

<a name="TestExApp"></a>   
## <a name="step-3-test-the-web-application"></a><span data-ttu-id="18c39-152">Bước 3: Kiểm tra ứng dụng web</span><span class="sxs-lookup"><span data-stu-id="18c39-152">Step 3: Test the web application</span></span>  

1. <span data-ttu-id="18c39-153">Đảm bảo rằng ứng dụng web mẫu bạn xây dựng trong bước 1 vẫn đang chạy.</span><span class="sxs-lookup"><span data-stu-id="18c39-153">Make sure that the sample web application that you built in step 1 is still running.</span></span>  

2. <span data-ttu-id="18c39-154">Chạy ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để kết nối với máy chủ **Microsoft Dynamics 365 for Customer Engagement** của bạn.</span><span class="sxs-lookup"><span data-stu-id="18c39-154">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your **Microsoft Dynamics 365 for Customer Engagement** server.</span></span>  

3. <span data-ttu-id="18c39-155">Trên lần đăng nhập thành công, bạn sẽ nhìn thấy **Ứng dụng Web Bên ngoài Mẫu** trên máy tính để bàn của mình.</span><span class="sxs-lookup"><span data-stu-id="18c39-155">On successful sign in, you’ll see the **Sample External Web Application** on your desktop.</span></span>  

4. <span data-ttu-id="18c39-156">Bấm vào tab \*\*Ứng dụng Web Bên ngoài Mẫu \*\*để xem ứng dụng web của bạn có được tổ chức trong **Unified Service Desk** hay không.</span><span class="sxs-lookup"><span data-stu-id="18c39-156">Click the **Sample External Web Application** tab to see your web application hosted within **Unified Service Desk**.</span></span>  

   <span data-ttu-id="18c39-157">![Hosting web app in Unified Service Desk](../unified-service-desk/media/usd-web-app-hosting.PNG "Hosting web app in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="18c39-157">![Hosting web app in Unified Service Desk](../unified-service-desk/media/usd-web-app-hosting.PNG "Hosting web app in Unified Service Desk")</span></span>  

> [!NOTE]
>  <span data-ttu-id="18c39-158">Tại thời điểm này, các trường này trống vì bạn chỉ đang lưu trữ ứng dụng web bên ngoài trong **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="18c39-158">At this point the fields are empty because you’re only hosting the external web application in **Unified Service Desk**.</span></span> <span data-ttu-id="18c39-159">Để đưa vào các giá trị từ **Unified Service Desk**, chúng ta phải tạo ra một bộ chuyển đổi ứng dụng web như minh họa trong bước tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="18c39-159">To populate them with values from **Unified Service Desk**, we have to create a web application adapter as illustrated in the next step.</span></span>  

<a name="createappadapter"></a>   
## <a name="step-4-create-the-web-application-adapter"></a><span data-ttu-id="18c39-160">Bước 4: Tạo các bộ chuyển đổi ứng dụng web</span><span class="sxs-lookup"><span data-stu-id="18c39-160">Step 4: Create the web application adapter</span></span>  

1. <span data-ttu-id="18c39-161">Bắt đầu [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)] và tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="18c39-161">Start [!INCLUDE[pn_Visual_Studio](../includes/pn-visual-studio.md)], and create a new project.</span></span>  

2. <span data-ttu-id="18c39-162">Trong hộp thoại **Dự án mới**:</span><span class="sxs-lookup"><span data-stu-id="18c39-162">In the **New Project** dialog box:</span></span>  

   1. <span data-ttu-id="18c39-163">From the list of installed templates on the left, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Web Application Adapter**.</span><span class="sxs-lookup"><span data-stu-id="18c39-163">From the list of installed templates on the left, expand [!INCLUDE[pn_Visual_C#](../includes/pn-visual-csharp.md)], and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Web Application Adapter**.</span></span>  

   2. <span data-ttu-id="18c39-164">Specify the name and location of the project, and click **OK** to create a new project.</span><span class="sxs-lookup"><span data-stu-id="18c39-164">Specify the name and location of the project, and click **OK** to create a new project.</span></span>  

   <span data-ttu-id="18c39-165">![Screenshot of Web Adapter in Visual Studio](../unified-service-desk/media/usd-web-app-adapter-vs.PNG "Screenshot of Web Adapter in Visual Studio")</span><span class="sxs-lookup"><span data-stu-id="18c39-165">![Screenshot of Web Adapter in Visual Studio](../unified-service-desk/media/usd-web-app-adapter-vs.PNG "Screenshot of Web Adapter in Visual Studio")</span></span>  

   3. <span data-ttu-id="18c39-166">Choose WebAppAdapter.cs and update the definition of **NotifyContextChange** with the following code to populate the text fields from the context information.</span><span class="sxs-lookup"><span data-stu-id="18c39-166">Choose WebAppAdapter.cs and update the definition of **NotifyContextChange** with the following code to populate the text fields from the context information.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="18c39-167">[Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))</span><span class="sxs-lookup"><span data-stu-id="18c39-167">[Context)](https://docs.microsoft.com/dotnet/api/microsoft.uii.csr.hostedapplicationadapter.notifycontextchange\(microsoft.uii.csr.context\))</span></span>  

      ```csharp  
      public override bool NotifyContextChange(Context context)  
              {  
                  // Populating text fields from context information.  

                  HTMLDocument htmlDoc = Browser.Document as HTMLDocument;  
                  if (htmlDoc != null)  
                  {  
                      IHTMLElementCollection htmlElementCollection = htmlDoc.all;  
                      IHTMLElement htmlFirstName = htmlElementCollection.item("txtFirstName", 0) as IHTMLElement;  
                      htmlFirstName.setAttribute("value", context["firstname"], 0);  
                      IHTMLElement htmlLastName = htmlElementCollection.item("txtLastName", 0) as IHTMLElement;  
                      htmlLastName.setAttribute("value", context["lastname"], 0);  
                      IHTMLElement htmlAddress = htmlElementCollection.item("txtAddress", 0) as IHTMLElement;  
                      htmlAddress.setAttribute("value", context["address1_line1"], 0);  
                      IHTMLElement htmlID = htmlElementCollection.item("txtID", 0) as IHTMLElement;  
                      htmlID.setAttribute("value", context["CustomerID"], 0);  
                  }  
                  return base.NotifyContextChange(context);  
              }  

      ```  

   4. <span data-ttu-id="18c39-168">Thêm mã sau vào định nghĩa ghi đè của **DoAction** để cập nhật ứng dụng với các giá trị từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span><span class="sxs-lookup"><span data-stu-id="18c39-168">Add the following code to the override definition of **DoAction** to update the application with values from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]</span></span>  

      ```csharp  
      public override bool DoAction(HostedWebApplication.WebAction action, ref string data)  
              {  
                  Trace.WriteLine(string.Format("{0}>>>>> RECEIVED (WebAction) Action : {1} ", this.Name, action.Name));  

                  // Check to see if the browser is working on something before allowing the system to do 'normal' behavior.  
                  if (Browser.WebBrowser.ReadyState != tagREADYSTATE.READYSTATE_COMPLETE)  
                  {  
                      // Browser is not in a state to process this request,  Queue it for when the browser is ready to handle it.   
                      Trace.WriteLine(string.Format("{0}>>>>> Browser Busy,({2}) Queuing Action : {1} ", this.Name, action.Name, Browser.WebBrowser.ReadyState.ToString()));  
                      qReqActionList.Enqueue(new BrowserActionData(action, data));  
                      return false;  
                  }  
                Trace.WriteLine(string.Format("{0}>>>>>>>>>>> Action:Name={1} Action:Url={2} Action:Query={3} Action:Init={4}", this.Name, action.Name, action.Url, action.QueryString, action.Initialization));  

                  // Get browser DOM and element collection.  
                  // Create an XML Document to load the passed in data to.  
                  HTMLDocument htmlDoc = Browser.Document as HTMLDocument;  
                  IHTMLElementCollection htmlElementCollection = htmlDoc.all;  

                  // Check action name for something we know how to process.  
                  switch (action.Name)  
                  {  
                      case "UpdateFirstName":  
                          IHTMLElement htmlFirstName = htmlElementCollection.item("txtFirstName", 0) as IHTMLElement;  
                          htmlFirstName.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateLastName":  
                          IHTMLElement htmlLastName = htmlElementCollection.item("txtLastName", 0) as IHTMLElement;  
                          htmlLastName.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateAddress":  
                          IHTMLElement htmlAddress = htmlElementCollection.item("txtAddress", 0) as IHTMLElement;  
                          htmlAddress.setAttribute("value", data, 0);  
                          break;  
                      case "UpdateID":  
                          IHTMLElement htmlID = htmlElementCollection.item("txtID", 0) as IHTMLElement;  
                          htmlID.setAttribute("value", data, 0);  
                          break;  
                  }  
                  return false;  
              }  

      ```  

   5. <span data-ttu-id="18c39-169">Save your project, and build it (**Build** > **Build Solution**).</span><span class="sxs-lookup"><span data-stu-id="18c39-169">Save your project, and build it (**Build** > **Build Solution**).</span></span> <span data-ttu-id="18c39-170">After the project builds successfully, an assembly (MyWebApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder.</span><span class="sxs-lookup"><span data-stu-id="18c39-170">After the project builds successfully, an assembly (MyWebApplicationAdapter.dll) is generated in the \bin\debug folder of your project folder.</span></span> <span data-ttu-id="18c39-171">Bạn sẽ cần lắp ráp cụm tổ hợp này sau để thử nghiệm và sử dụng bộ chuyển đổi ứng dụng web của bạn.</span><span class="sxs-lookup"><span data-stu-id="18c39-171">You’ll need this assembly later for testing and using your web application adapter.</span></span>  

<a name="ConfigureWebAdapter"></a>   
## <a name="step-5-configure-the-web-application-adapter-in-dynamics-365-for-customer-engagement-apps"></a><span data-ttu-id="18c39-172">Step 5: Configure the web application adapter in Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="18c39-172">Step 5: Configure the web application adapter in Dynamics 365 for Customer Engagement apps</span></span>  

1. <span data-ttu-id="18c39-173">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="18c39-173">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  

2. <span data-ttu-id="18c39-174">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span><span class="sxs-lookup"><span data-stu-id="18c39-174">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and then select **Settings**.</span></span>  

3. <span data-ttu-id="18c39-175">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="18c39-175">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  

4. <span data-ttu-id="18c39-176">Từ danh sách kiểm soát tổ chức, chọn kiểm soát được tổ chức **QsWebApplication**.</span><span class="sxs-lookup"><span data-stu-id="18c39-176">From the list of hosted controls, select **QsWebApplication** hosted control.</span></span>  

   <span data-ttu-id="18c39-177">![Hosted controls list in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-hosted-controls-list.PNG "Hosted controls list in Dynamics 365 for Customer Engagement apps")</span><span class="sxs-lookup"><span data-stu-id="18c39-177">![Hosted controls list in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-hosted-controls-list.PNG "Hosted controls list in Dynamics 365 for Customer Engagement apps")</span></span>  

5. <span data-ttu-id="18c39-178">Trong phần **Cấu hình Bộ chuyển đổi**, chỉ định các giá trị sau.</span><span class="sxs-lookup"><span data-stu-id="18c39-178">In the **Adapter Configuration** section, specify the following values.</span></span>  

   |<span data-ttu-id="18c39-179">**Trường**</span><span class="sxs-lookup"><span data-stu-id="18c39-179">**Field**</span></span>|<span data-ttu-id="18c39-180">Value</span><span class="sxs-lookup"><span data-stu-id="18c39-180">Value</span></span>|  
   |---------------|-----------|  
   |<span data-ttu-id="18c39-181">**Bộ điều hợp**</span><span class="sxs-lookup"><span data-stu-id="18c39-181">**Adapter**</span></span>|<span data-ttu-id="18c39-182">Sử dụng bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="18c39-182">Use Adapter</span></span>|  
   |<span data-ttu-id="18c39-183">**URI**</span><span class="sxs-lookup"><span data-stu-id="18c39-183">**URI**</span></span>|<span data-ttu-id="18c39-184">MyWebApplicationAdapter</span><span class="sxs-lookup"><span data-stu-id="18c39-184">MyWebApplicationAdapter</span></span>|  
   |<span data-ttu-id="18c39-185">Loại</span><span class="sxs-lookup"><span data-stu-id="18c39-185">Type</span></span>|<span data-ttu-id="18c39-186">MyWebApplicationAdapter.WebAppAdapter</span><span class="sxs-lookup"><span data-stu-id="18c39-186">MyWebApplicationAdapter.WebAppAdapter</span></span>|  

   <span data-ttu-id="18c39-187">![Web adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-adapter-config.PNG "Web adapter configuration in Dynamics 365 for Customer Engagement apps")</span><span class="sxs-lookup"><span data-stu-id="18c39-187">![Web adapter configuration in Dynamics 365 for Customer Engagement apps](../unified-service-desk/media/usd-web-app-adapter-config.PNG "Web adapter configuration in Dynamics 365 for Customer Engagement apps")</span></span>  

   > [!NOTE]
   > <span data-ttu-id="18c39-188">**URI** là tên của cụm tổ hợp của bạn và **Loại** là tên của cụm tổ hợp của bạn (dll) theo sau bởi dấu chấm (.) sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="18c39-188">**URI** is the name of your assembly and the **Type** is the name of your assembly (dll) followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="18c39-189">In this example, the name of the assembly is MyWebApplicationAdapter and name of the class is WebAdapter, which is the default class name when you create a web application adapter.</span><span class="sxs-lookup"><span data-stu-id="18c39-189">In this example, the name of the assembly is MyWebApplicationAdapter and name of the class is WebAdapter, which is the default class name when you create a web application adapter.</span></span>  

6. <span data-ttu-id="18c39-190">Chọn **Lưu** để lưu các thay đổi.</span><span class="sxs-lookup"><span data-stu-id="18c39-190">Choose **Save** to save the changes.</span></span>  

<a name="TestAppAdapter"></a>   
## <a name="step-6-test-the-web-application-adapter"></a><span data-ttu-id="18c39-191">Bước 6: Thử nghiệm bộ chuyển đổi ứng dụng web</span><span class="sxs-lookup"><span data-stu-id="18c39-191">Step 6: Test the web application adapter</span></span>  

1. <span data-ttu-id="18c39-192">Copy the assembly that contains your web application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the Unified Service Desk application directory.</span><span class="sxs-lookup"><span data-stu-id="18c39-192">Copy the assembly that contains your web application adapter definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<ProjectFolder>\bin\debug) to the Unified Service Desk application directory.</span></span> <span data-ttu-id="18c39-193">In this case, you’ll copy the MyWebApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span><span class="sxs-lookup"><span data-stu-id="18c39-193">In this case, you’ll copy the MyWebApplicationAdapter.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span></span>  

2. <span data-ttu-id="18c39-194">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="18c39-194">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps server.</span></span>  

3. <span data-ttu-id="18c39-195">Trên lần đăng nhập thành công, bạn sẽ nhìn thấy nút ứng dụng web bên ngoài mẫu trên máy tính để bàn của mình.</span><span class="sxs-lookup"><span data-stu-id="18c39-195">On successful sign in, you will see the sample external web application button on your desktop.</span></span>  

4. <span data-ttu-id="18c39-196">Chọn **Tìm kiếm** rồi sau đó chọn **Người liên hệ** và chọn một người liên hệ.</span><span class="sxs-lookup"><span data-stu-id="18c39-196">Choose **Search** and then choose **Contacts** and select a contact.</span></span> <span data-ttu-id="18c39-197">Trong trường hợp này, chọn **Patrick Sands**.</span><span class="sxs-lookup"><span data-stu-id="18c39-197">In this case, select **Patrick Sands**.</span></span>  

   <span data-ttu-id="18c39-198">![Screenshot of contact list](../unified-service-desk/media/usd-web-app-adapter-contacts-list.PNG "Screenshot of contact list")</span><span class="sxs-lookup"><span data-stu-id="18c39-198">![Screenshot of contact list](../unified-service-desk/media/usd-web-app-adapter-contacts-list.PNG "Screenshot of contact list")</span></span>  

5. <span data-ttu-id="18c39-199">Bấm vào **Ứng dụng Web Bên Ngoài Mẫu** và bạn sẽ nhìn thấy tên, họ, địa chỉ và ID của khách hàng được điền vào.</span><span class="sxs-lookup"><span data-stu-id="18c39-199">Click **Sample External Web Application** and you’ll see the customer’s first name, last name, address, and ID populated.</span></span>  

   <span data-ttu-id="18c39-200">![Testing WebApp Adapter screenshot](../unified-service-desk/media/usd-web-app-adapter-test.PNG "Testing WebApp Adapter screenshot")</span><span class="sxs-lookup"><span data-stu-id="18c39-200">![Testing WebApp Adapter screenshot](../unified-service-desk/media/usd-web-app-adapter-test.PNG "Testing WebApp Adapter screenshot")</span></span>  

> [!NOTE]
>  <span data-ttu-id="18c39-201">Cách này cho bạn thấy cách đọc hoặc hiển thị dữ liệu từ [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trong ứng dụng web bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="18c39-201">This walkthrough showed you how to read or display data from [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] in the external web application.</span></span> <span data-ttu-id="18c39-202">To update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external web application, and vice versa, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)</span><span class="sxs-lookup"><span data-stu-id="18c39-202">To update the data in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the external web application, and vice versa, see [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md)</span></span>  

### <a name="see-also"></a><span data-ttu-id="18c39-203">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="18c39-203">See also</span></span>  
 [<span data-ttu-id="18c39-204">Use UII adapters to interact with external and web applications</span><span class="sxs-lookup"><span data-stu-id="18c39-204">Use UII adapters to interact with external and web applications</span></span>](../unified-service-desk/use-uii-adapters-interact-external-web-applications.md)
