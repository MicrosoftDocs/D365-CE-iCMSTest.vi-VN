---
title: 'Walkthrough: Create custom hosted control for Unified Service Desk | MicrosoftDocs'
description: Learn about how to create a custom hosted control for Unified Service Desk.
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
ms.assetid: 7d184ce7-ba95-46ea-9219-67fd6821eba5
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 42b01a41f2d57225af64779f844459c2952e6fc5
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385845"
---
# <a name="walkthrough-create-custom-hosted-control-for-unified-service-desk"></a><span data-ttu-id="c2bad-103">Walkthrough: Create custom hosted control for Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="c2bad-103">Walkthrough: Create custom hosted control for Unified Service Desk</span></span>
<span data-ttu-id="c2bad-104">Trong chủ đề này, bạn sẽ tìm hiểu cách tạo kiểm soát tổ chức tùy chỉnh được gọi là `My Custom Control` với hành động tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="c2bad-104">In this topic, you’ll learn how to create a custom hosted control called `My Custom Control` with a custom action.</span></span> <span data-ttu-id="c2bad-105">The custom hosted control has two [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] controls: a button that calls the Debugger hosted control and a text label that displays the user name when a custom action, `MyCustomAction`, is called.</span><span class="sxs-lookup"><span data-stu-id="c2bad-105">The custom hosted control has two [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../includes/pn-ms-windows-presentation-foundation.md)] controls: a button that calls the Debugger hosted control and a text label that displays the user name when a custom action, `MyCustomAction`, is called.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c2bad-106">In This Section</span><span class="sxs-lookup"><span data-stu-id="c2bad-106">In This Section</span></span>  
 [<span data-ttu-id="c2bad-107">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c2bad-107">Prerequisites</span></span>](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#Prereq)  
  
 [<span data-ttu-id="c2bad-108">Tạo kiểm soát tổ chức tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="c2bad-108">Create a custom hosted control</span></span>](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#HowTo)  
  
 [<span data-ttu-id="c2bad-109">Kiểm tra kiểm soát tổ chức tùy chỉnh của bạn</span><span class="sxs-lookup"><span data-stu-id="c2bad-109">Test your custom hosted control</span></span>](../unified-service-desk/walkthrough-create-custom-hosted-control-for-unified-service-desk.md#Test)  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="c2bad-110">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="c2bad-110">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="c2bad-111">4.5.2</span><span class="sxs-lookup"><span data-stu-id="c2bad-111">4.5.2</span></span>  
  
- <span data-ttu-id="c2bad-112">Ứng dụng khách [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]; ứng dụng khách là bắt buộc để thử nghiệm kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="c2bad-112">[!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application; the client application is required for testing the hosted control</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="c2bad-113">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], hoặc [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="c2bad-113">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  
  
- [!INCLUDE[tn_nuget](../includes/tn-nuget.md)] <span data-ttu-id="c2bad-114">Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="c2bad-114">Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="c2bad-115">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the custom hosted control project template.</span><span class="sxs-lookup"><span data-stu-id="c2bad-115">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the custom hosted control project template.</span></span> <span data-ttu-id="c2bad-116">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="c2bad-116">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>
  
<a name="HowTo"></a>   
## <a name="create-a-custom-hosted-control"></a><span data-ttu-id="c2bad-117">Tạo kiểm soát tổ chức tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="c2bad-117">Create a custom hosted control</span></span>  
  
<a name="Step1"></a>   
1. <span data-ttu-id="c2bad-118">Bắt đầu [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] và tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="c2bad-118">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="c2bad-119">Trong hộp thoại **Dự án mới**:</span><span class="sxs-lookup"><span data-stu-id="c2bad-119">In the **New Project** dialog box:</span></span>  
  
   1. <span data-ttu-id="c2bad-120">From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD Custom Hosted Control**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-120">From the list of installed templates, expand **Visual C#**, and select **CRM SDK Templates** > **Unified Service Desk** > **USD Custom Hosted Control**.</span></span>  
  
   2. <span data-ttu-id="c2bad-121">Đảm bảo rằng **[!INCLUDE[pn_NET_Framework](../includes/pn-net-framework.md)] 4.5.2** được chọn.</span><span class="sxs-lookup"><span data-stu-id="c2bad-121">Ensure that **[!INCLUDE[pn_NET_Framework](../includes/pn-net-framework.md)] 4.5.2** is selected.</span></span>  
  
   3. <span data-ttu-id="c2bad-122">Chỉ định tên và vị trí của dự án, và bấm vào **OK** để tạo ra một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="c2bad-122">Specify the name and location of the project, and click **OK** to create a new project.</span></span>  
  
   <span data-ttu-id="c2bad-123">![Template for creating a custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol01.png "Template for creating a custom hosted control")</span><span class="sxs-lookup"><span data-stu-id="c2bad-123">![Template for creating a custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol01.png "Template for creating a custom hosted control")</span></span>  
  
3. <span data-ttu-id="c2bad-124">In **Solution Explorer**, double-click the USDControl.xaml file to bring up the XAML designer.</span><span class="sxs-lookup"><span data-stu-id="c2bad-124">In **Solution Explorer**, double-click the USDControl.xaml file to bring up the XAML designer.</span></span>  
  
4. <span data-ttu-id="c2bad-125">Trong trình thiết kế, thêm kiểm soát sau từ **Hộp công cụ**:</span><span class="sxs-lookup"><span data-stu-id="c2bad-125">In the designer, add the following controls from the **Toolbox**:</span></span>  
  
   - <span data-ttu-id="c2bad-126">**Label**: In the **Properties** pane, set the name of the control to “myLabel.”</span><span class="sxs-lookup"><span data-stu-id="c2bad-126">**Label**: In the **Properties** pane, set the name of the control to “myLabel.”</span></span>  
  
   - <span data-ttu-id="c2bad-127">**Button**: In the **Properties** pane, set the name of the control to “myButton,” and the content to “**Start Debugger**.”</span><span class="sxs-lookup"><span data-stu-id="c2bad-127">**Button**: In the **Properties** pane, set the name of the control to “myButton,” and the content to “**Start Debugger**.”</span></span>  
  
     <span data-ttu-id="c2bad-128">This is how the controls look in the XAML designer.</span><span class="sxs-lookup"><span data-stu-id="c2bad-128">This is how the controls look in the XAML designer.</span></span>  
  
   <span data-ttu-id="c2bad-129">![XAML designer with custom controls](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol02.png "XAML designer with custom controls")</span><span class="sxs-lookup"><span data-stu-id="c2bad-129">![XAML designer with custom controls](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol02.png "XAML designer with custom controls")</span></span>  
  
5. <span data-ttu-id="c2bad-130">Bấm đúp vào nút này để thêm mã sau XAML.</span><span class="sxs-lookup"><span data-stu-id="c2bad-130">Double-click the button to add code behind the XAML.</span></span> <span data-ttu-id="c2bad-131">Điều này sẽ đưa bạn đến định nghĩa sự kiện nhấp chuột của Nút của tôi trong tệp USDControl.xaml.cs.</span><span class="sxs-lookup"><span data-stu-id="c2bad-131">This will take you to the click event definition of myButton in the USDControl.xaml.cs file.</span></span> <span data-ttu-id="c2bad-132">Thêm lệnh sau.</span><span class="sxs-lookup"><span data-stu-id="c2bad-132">Add the following command.</span></span>  
  
   ```csharp  
   private void myButton_Click(object sender, RoutedEventArgs e)  
   {  
       if (!this.desktopAccess.AppExistsInUI("Debugger"))  
       {  
           this.desktopAccess.CreateDynamicApplication("Debugger");  
       }  
       this.FireRequestAction(new Microsoft.Uii.Csr.RequestActionEventArgs("Debugger", "default", null));  
   }  
   ```  
  
6. <span data-ttu-id="c2bad-133">Xác định hành động tùy chỉnh cho kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="c2bad-133">Define a custom action for the hosted control.</span></span> <span data-ttu-id="c2bad-134">In the USDControl.xaml.cs file, browse to the override definition of `DoAction`.</span><span class="sxs-lookup"><span data-stu-id="c2bad-134">In the USDControl.xaml.cs file, browse to the override definition of `DoAction`.</span></span>  
  
   ```csharp  
   protected override void DoAction(Microsoft.Uii.Csr.RequestActionEventArgs args)  
   ```  
  
7. <span data-ttu-id="c2bad-135">Thêm mã sau bên trong định nghĩa thay thế của `DoAction` để xác định hành động tùy chỉnh gọi là `MyCustomAction`, chấp nhận tham số có tên `username`.</span><span class="sxs-lookup"><span data-stu-id="c2bad-135">Add the following code within the override definition of `DoAction` to define a custom action called `MyCustomAction`, which accepts a parameter called `username`.</span></span>  
  
   ```csharp  
   if (args.Action.Equals("MyCustomAction", StringComparison.OrdinalIgnoreCase))  
   {  
       List<KeyValuePair<string, string>> actionDataList = Utility.SplitLines(args.Data, CurrentContext, localSession);  
       string valueIwant = Utility.GetAndRemoveParameter(actionDataList, "username"); // assume there is a myKey=<value> in the data.  
  
       if (!string.IsNullOrEmpty(valueIwant))  
       {  
           this.Dispatcher.Invoke(() => { this.myLabel.Content = valueIwant; });  
       }  
   }  
   ```  
  
   > [!TIP]
   >  <span data-ttu-id="c2bad-136">Mẫu này cung cấp hầu hết các mã như nhận xét bên trong định nghĩa thay thế của `DoAction` để giúp bạn nhanh chóng bắt đầu phát triển.</span><span class="sxs-lookup"><span data-stu-id="c2bad-136">The template provides most of the code as comment within the override definition of `DoAction` to help you quickly get started with the development.</span></span> <span data-ttu-id="c2bad-137">Bạn cần phải bỏ ghi chú dòng mã yêu cầu và thay thế giá trị trình giữ chỗ bằng giá trị của mình.</span><span class="sxs-lookup"><span data-stu-id="c2bad-137">You need to uncomment the required line of code, and replace the placeholder values with your values.</span></span>  
  
8. <span data-ttu-id="c2bad-138">Save your project, and build it (**Build** > **Build Solution**) to verify that it builds successfully.</span><span class="sxs-lookup"><span data-stu-id="c2bad-138">Save your project, and build it (**Build** > **Build Solution**) to verify that it builds successfully.</span></span>  
  
<a name="Test"></a>   
## <a name="test-your-custom-hosted-control"></a><span data-ttu-id="c2bad-139">Kiểm tra kiểm soát tổ chức tùy chỉnh của bạn</span><span class="sxs-lookup"><span data-stu-id="c2bad-139">Test your custom hosted control</span></span>  
 <span data-ttu-id="c2bad-140">Sau khi dự án của bạn được tạo dựng thành công, hãy kiểm tra kiểm soát tổ chức tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="c2bad-140">After your project builds successfully, test the custom hosted control.</span></span> <span data-ttu-id="c2bad-141">Thử nghiệm bao gồm hai phần: xác định kiểm soát tổ chức tùy chỉnh trên máy chủ rồi sau đó kết nối với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] trên máy chủ bằng cách sử dụng ứng dụng khách của bạn.</span><span class="sxs-lookup"><span data-stu-id="c2bad-141">Testing consists of two parts: defining the custom hosted control on the server and then connecting to [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] on the server using your client application.</span></span>  
  
### <a name="define-the-custom-hosted-control-and-action-on-the-dynamics-365-for-customer-engagement-server"></a><span data-ttu-id="c2bad-142">Define the custom hosted control and action on the Dynamics 365 for Customer Engagement server</span><span class="sxs-lookup"><span data-stu-id="c2bad-142">Define the custom hosted control and action on the Dynamics 365 for Customer Engagement server</span></span>  
  
1. <span data-ttu-id="c2bad-143">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="c2bad-143">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="c2bad-144">Trên thanh điều hướng, chọn **Microsoft Dynamics 365 for Customer Engagement** và chọn **Thiết đặt**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-144">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement**, and select **Settings**.</span></span>  
  
3. <span data-ttu-id="c2bad-145">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-145">Choose **Settings** > **Unified Service Desk** > **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="c2bad-146">Chọn **MỚI** rồi chỉ định các giá trị trong màn hình **Kiểm soát Tổ chức Mới** như được hiển thị tại đây.</span><span class="sxs-lookup"><span data-stu-id="c2bad-146">Choose **NEW**, and then specify values in the **New Hosted Control** screen as shown here.</span></span>  
  
   <span data-ttu-id="c2bad-147">![New custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol03.png "New custom hosted control")</span><span class="sxs-lookup"><span data-stu-id="c2bad-147">![New custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol03.png "New custom hosted control")</span></span>  
  
   > [!NOTE]
   > <span data-ttu-id="c2bad-148">**URI Cụm** là tên của cụm của bạn và **Loại cụm** là tên của cụm (dll) theo sau là một dấu chấm (.) và sau đó tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="c2bad-148">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly (dll) followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="c2bad-149">Trong ví dụ này, tên của cụm là **Kiểm soát tùy chỉnh của tôi** và tên của các lớp là **Kiểm soát USD**, chính là tên lớp mặc định khi bạn tạo kiểm soát tổ chức tùy chỉnh.</span><span class="sxs-lookup"><span data-stu-id="c2bad-149">In this example, the name of the assembly is **MyCustomControl** and name of the class is **USDControl**, which is the default class name when you create a custom hosted control.</span></span>  
  
5. <span data-ttu-id="c2bad-150">Chọn **Lưu** để tạo kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="c2bad-150">Choose **Save** to create the hosted control.</span></span>  
  
6. <span data-ttu-id="c2bad-151">Create the action for the hosted control that you defined in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="c2bad-151">Create the action for the hosted control that you defined in Visual Studio.</span></span> <span data-ttu-id="c2bad-152">Trên thanh điều hướng, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức của bạn và chọn **Hành động UII**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-152">On the nav bar, choose the down arrow next to your hosted control name, and select **UII Actions**.</span></span>  
  
7. <span data-ttu-id="c2bad-153">Chọn **Thêm Hành động UII Mới**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-153">Choose **Add New UII Action**.</span></span>  
  
8. <span data-ttu-id="c2bad-154">Nhập **MyCustomAction** vào trường **tên** và chọn **Lưu**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-154">Type **MyCustomAction** in the **Name** field, and choose **Save**.</span></span>  
  
   <span data-ttu-id="c2bad-155">You have now configured your custom hosted control and custom action on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="c2bad-155">You have now configured your custom hosted control and custom action on your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span>  
  
<a name="Run"></a>   
### <a name="run-the-unified-service-desk-client-to-work-with-custom-hosted-control"></a><span data-ttu-id="c2bad-156">Chạy ứng dụng Unified Service Desk để hoạt động với kiểm soát tổ chức tùy chỉnh</span><span class="sxs-lookup"><span data-stu-id="c2bad-156">Run the Unified Service Desk client to work with custom hosted control</span></span>  
  
1. <span data-ttu-id="c2bad-157">Copy the assembly that contains your custom hosted control definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<*ProjectFolder*>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span><span class="sxs-lookup"><span data-stu-id="c2bad-157">Copy the assembly that contains your custom hosted control definition from your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project output folder (\<*ProjectFolder*>\bin\debug) to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] application directory.</span></span> <span data-ttu-id="c2bad-158">In this case, you’ll copy the MyCustomControl.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span><span class="sxs-lookup"><span data-stu-id="c2bad-158">In this case, you’ll copy the MyCustomControl.dll file to the c:\Program Files\Microsoft Dynamics CRM USD\USD directory.</span></span>  
  
2. <span data-ttu-id="c2bad-159">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="c2bad-159">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span>  
  
3. <span data-ttu-id="c2bad-160">Khi đăng nhập thành công, bạn sẽ thấy kiểm soát tổ chức tùy chỉnh, **Kiểm soát tổ chức tùy chỉnh của tôi**, trong máy tính của bạn.</span><span class="sxs-lookup"><span data-stu-id="c2bad-160">On successful sign in, you’ll see the custom hosted control, **My Custom Hosted Control**, on your desktop.</span></span>  
  
   <span data-ttu-id="c2bad-161">![Custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol04.png "Custom hosted control")</span><span class="sxs-lookup"><span data-stu-id="c2bad-161">![Custom hosted control](../unified-service-desk/media/crm-itpro-usd-customhostedcontrol04.png "Custom hosted control")</span></span>  
  
4. <span data-ttu-id="c2bad-162">Bấm vào **bắt đầu trình gỡ lỗi** để khởi động kiểm soát tổ chức trình gỡ lỗi.</span><span class="sxs-lookup"><span data-stu-id="c2bad-162">Click **Start Debugger** to launch the Debugger hosted control.</span></span>  
  
5. <span data-ttu-id="c2bad-163">Để kiểm tra hành động tùy chỉnh, chọn tab **Trình gỡ lỗi** rồi bấm vào mũi tên xuống phía trên tab **Cuộc gọi Hành động** để hiển thị khu vực nơi bạn có thể kiểm tra cuộc gọi hành động và hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].</span><span class="sxs-lookup"><span data-stu-id="c2bad-163">To test the custom action, choose the **Debugger** tab, and then click the down arrow above the **Action Calls** tab to display the area where you can test action calls and [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions.</span></span>  
  
   <span data-ttu-id="c2bad-164">![Expanded testing area in debugger](../unified-service-desk/media/crm-itpro-usd-customhostedcontroldebugger.png "Expanded testing area in debugger")</span><span class="sxs-lookup"><span data-stu-id="c2bad-164">![Expanded testing area in debugger](../unified-service-desk/media/crm-itpro-usd-customhostedcontroldebugger.png "Expanded testing area in debugger")</span></span>  
  
6. <span data-ttu-id="c2bad-165">Chọn tab **Hành động Trực tiếp**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-165">Choose the **Direct Action** tab.</span></span>  
  
7. <span data-ttu-id="c2bad-166">Từ danh sách **Kiểm soát tổ chức**, chọn **Kiểm soát tổ chức tùy chỉnh của tôi**, và từ danh sách **hành động**, chọn **Hành động tùy chỉnh của tôi**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-166">From the **Hosted Control** list, select **My Custom Hosted Control**, and from the **Action** list, select **MyCustomAction**.</span></span>  
  
8. <span data-ttu-id="c2bad-167">Theo định nghĩa hành động tùy chỉnh, cuộc gọi hành động này giả sử tham số có tên `username`, do đó hãy thêm giá trị sau vào trường **Dữ liệu**: **username=Tracie Hamilton**.</span><span class="sxs-lookup"><span data-stu-id="c2bad-167">As per the custom action definition, this action call expects a parameter called `username`, so add the following value in the **Data** field: **username=Tracie Hamilton**.</span></span>  
  
   <span data-ttu-id="c2bad-168">![Test your custom hosted control](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol01.png "Test your custom hosted control")</span><span class="sxs-lookup"><span data-stu-id="c2bad-168">![Test your custom hosted control](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol01.png "Test your custom hosted control")</span></span>  
  
9. <span data-ttu-id="c2bad-169">Click the **Run Direct Action** icon (![Unified Service Desk debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "Unified Service Desk debugger Run Action Call button")), and then click the **My Custom Hosted Control** tab. The specified user name is displayed in the label field.</span><span class="sxs-lookup"><span data-stu-id="c2bad-169">Click the **Run Direct Action** icon (![Unified Service Desk debugger Run Action Call button](../unified-service-desk/media/usd-run-action-call-icon.png "Unified Service Desk debugger Run Action Call button")), and then click the **My Custom Hosted Control** tab. The specified user name is displayed in the label field.</span></span>  
  
   <span data-ttu-id="c2bad-170">![My Custom Host Control tab shows username](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol02.png "My Custom Host Control tab shows username")</span><span class="sxs-lookup"><span data-stu-id="c2bad-170">![My Custom Host Control tab shows username](../unified-service-desk/media/crm-itpro-usd-custhostedcontrol02.png "My Custom Host Control tab shows username")</span></span>
  
### <a name="see-also"></a><span data-ttu-id="c2bad-171">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="c2bad-171">See also</span></span>  
 [<span data-ttu-id="c2bad-172">Kiểm soát tổ chức USD (Kiểm soát tổ chức)</span><span class="sxs-lookup"><span data-stu-id="c2bad-172">USD Hosted Control (Hosted Control)</span></span>](../unified-service-desk/usd-hosted-control-hosted-control.md)  
 <span data-ttu-id="c2bad-173">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span><span class="sxs-lookup"><span data-stu-id="c2bad-173">[Hosted control types and action/event reference](../unified-service-desk/hosted-control-types-action-event-reference.md) </span></span>  
 <span data-ttu-id="c2bad-174">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span><span class="sxs-lookup"><span data-stu-id="c2bad-174">[Unified Service Desk Configuration Walkthroughs](../unified-service-desk/unified-service-desk-configuration-walkthroughs.md) </span></span>  
 [<span data-ttu-id="c2bad-175">Use custom hosted control in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="c2bad-175">Use custom hosted control in Unified Service Desk</span></span>](../unified-service-desk/use-custom-hosted-control-unified-service-desk.md)
