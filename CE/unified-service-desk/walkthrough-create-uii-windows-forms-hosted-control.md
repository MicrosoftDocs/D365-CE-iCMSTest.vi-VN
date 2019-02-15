---
title: 'Walkthrough: Create a UII Windows Forms Hosted Control | MicrosoftDocs'
description: Demonstrates how you can build a Windows Forms UII hosted control that interacts with Unified Service Desk and standalone or web external applications.
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
ms.assetid: a9fd1d9e-b04e-4ea0-b9c2-fda7bac4b7f9
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
ms.openlocfilehash: d2145bccc14b57e04c6d96512c03fd356dfbb9e2
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387538"
---
# <a name="walkthrough-create-a-uii-windows-forms-hosted-control-in-unified-service-desk"></a><span data-ttu-id="3cc97-103">Walkthrough: Create a UII Windows Forms Hosted Control in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="3cc97-103">Walkthrough: Create a UII Windows Forms Hosted Control in Unified Service Desk</span></span>
<span data-ttu-id="3cc97-104">Cách này trình bày cách bạn có thể xây dựng kiểm soát tổ chức [Biểu mẫu Windows](https://msdn.microsoft.com/library/ms229601\(v=vs.110\).aspx) [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và ứng dụng web hoặc bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="3cc97-104">This walkthrough demonstrates how you can build a [Windows Forms](https://msdn.microsoft.com/library/ms229601\(v=vs.110\).aspx) [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted control that interacts with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and standalone or web external applications.</span></span>  
  
 <span data-ttu-id="3cc97-105">Trong cách này, bạn sẽ:</span><span class="sxs-lookup"><span data-stu-id="3cc97-105">In this walkthrough, you’ll:</span></span>  
  
- <span data-ttu-id="3cc97-106">Tạo [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] kiểm soát tổ chức Biểu mẫu Windows, **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, sẽ hiển thị tên, họ, địa chỉ đường phố và ID của người liên hệ khi bạn tìm kiếm liên hệ và bấm vào tên người liên hệ để mở trong một phiên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-106">Create a [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] Windows Forms hosted control, **Sample UII Windows Forms Hosted Control**, which will display first name, last name, street address, and ID of a contact when you search for contacts, and click a contact name to open it in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="3cc97-107">Các giá trị này được hiển thị từ ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-107">These values are displayed from the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context.</span></span>  
  
- <span data-ttu-id="3cc97-108">Thay đổi các giá trị tên, họ hoặc địa chỉ đường phố trong ứng dụng bên ngoài và web được lưu trữ trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] từ kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] mà chúng ta đã tạo.</span><span class="sxs-lookup"><span data-stu-id="3cc97-108">Change first name, last name, or street address values in an external application and web application hosted in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Windows Forms hosted control that we create.</span></span> <span data-ttu-id="3cc97-109">The external and web applications were created in earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="3cc97-109">The external and web applications were created in earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span></span>  
  
- <span data-ttu-id="3cc97-110">Thông báo các thay đổi đối với ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] để cập nhật các giá trị tại đó.</span><span class="sxs-lookup"><span data-stu-id="3cc97-110">Notify changes to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context to update the values there.</span></span>  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="3cc97-111">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="3cc97-111">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="3cc97-112">4.5.2</span><span class="sxs-lookup"><span data-stu-id="3cc97-112">4.5.2</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] <span data-ttu-id="3cc97-113">client application; required for testing the hosted control.</span><span class="sxs-lookup"><span data-stu-id="3cc97-113">client application; required for testing the hosted control.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="3cc97-114">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="3cc97-114">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] <span data-ttu-id="3cc97-115">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="3cc97-115">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="3cc97-116">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII Windows Forms hosted control project template.</span><span class="sxs-lookup"><span data-stu-id="3cc97-116">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contains the UII Windows Forms hosted control project template.</span></span> <span data-ttu-id="3cc97-117">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-117">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
- <span data-ttu-id="3cc97-118">You should have completed [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external application and web application set up with the respective adapters to facilitate interaction with those applications.</span><span class="sxs-lookup"><span data-stu-id="3cc97-118">You should have completed [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external application and web application set up with the respective adapters to facilitate interaction with those applications.</span></span>  
  
<a name="step1"></a>   
## <a name="step-1-create-a-uii-windows-forms-hosted-control-using-visual-studio"></a><span data-ttu-id="3cc97-119">Step 1: Create a UII Windows Forms hosted control using Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3cc97-119">Step 1: Create a UII Windows Forms hosted control using Visual Studio</span></span>  
  
<a name="Step1"></a>   
1. <span data-ttu-id="3cc97-120">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span><span class="sxs-lookup"><span data-stu-id="3cc97-120">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="3cc97-121">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="3cc97-121">In the **New Project** dialog box:</span></span>  
  
   1.  <span data-ttu-id="3cc97-122">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Windows Forms Hosted Control**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-122">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII Windows Forms Hosted Control**.</span></span>  
  
   2.  <span data-ttu-id="3cc97-123">Specify the name and location of the project, and click **OK** to create a new project.</span><span class="sxs-lookup"><span data-stu-id="3cc97-123">Specify the name and location of the project, and click **OK** to create a new project.</span></span>  
  
   <span data-ttu-id="3cc97-124">![Create a UII Windows Form hosted control](../unified-service-desk/media/usd-create-uii-windows-form-hosted-control-1.png "Create a UII Windows Form hosted control")</span><span class="sxs-lookup"><span data-stu-id="3cc97-124">![Create a UII Windows Form hosted control](../unified-service-desk/media/usd-create-uii-windows-form-hosted-control-1.png "Create a UII Windows Form hosted control")</span></span>  
  
3. <span data-ttu-id="3cc97-125">Trong ngăn **Trình khám phá Giải pháp**, bấm chuột phải vào tệp **UiiWinformControl.cs** và chọn **Mở** để hiển thị trình thiết kế Biểu mẫu Windows.</span><span class="sxs-lookup"><span data-stu-id="3cc97-125">In **Solution Explorer** pane, right-click the **UiiWinformControl.cs** file, and select **Open** to display the Windows Forms designer.</span></span>  
  
4. <span data-ttu-id="3cc97-126">In the designer, add the following controls from the **Toolbox**:</span><span class="sxs-lookup"><span data-stu-id="3cc97-126">In the designer, add the following controls from the **Toolbox**:</span></span>  
  
   |<span data-ttu-id="3cc97-127">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="3cc97-127">Control type</span></span>|<span data-ttu-id="3cc97-128">Tên</span><span class="sxs-lookup"><span data-stu-id="3cc97-128">Name</span></span>|<span data-ttu-id="3cc97-129">Text</span><span class="sxs-lookup"><span data-stu-id="3cc97-129">Text</span></span>|  
   |------------------|----------|----------|  
   |<span data-ttu-id="3cc97-130">Nhãn</span><span class="sxs-lookup"><span data-stu-id="3cc97-130">Label</span></span>|<span data-ttu-id="3cc97-131">lblFirstName</span><span class="sxs-lookup"><span data-stu-id="3cc97-131">lblFirstName</span></span>|<span data-ttu-id="3cc97-132">Tên</span><span class="sxs-lookup"><span data-stu-id="3cc97-132">First Name</span></span>|  
   |<span data-ttu-id="3cc97-133">Nhãn</span><span class="sxs-lookup"><span data-stu-id="3cc97-133">Label</span></span>|<span data-ttu-id="3cc97-134">lblLastName</span><span class="sxs-lookup"><span data-stu-id="3cc97-134">lblLastName</span></span>|<span data-ttu-id="3cc97-135">Họ</span><span class="sxs-lookup"><span data-stu-id="3cc97-135">Last Name</span></span>|  
   |<span data-ttu-id="3cc97-136">Nhãn</span><span class="sxs-lookup"><span data-stu-id="3cc97-136">Label</span></span>|<span data-ttu-id="3cc97-137">lblAddress</span><span class="sxs-lookup"><span data-stu-id="3cc97-137">lblAddress</span></span>|<span data-ttu-id="3cc97-138">Địa chỉ Đường phố</span><span class="sxs-lookup"><span data-stu-id="3cc97-138">Street Address</span></span>|  
   |<span data-ttu-id="3cc97-139">Nhãn</span><span class="sxs-lookup"><span data-stu-id="3cc97-139">Label</span></span>|<span data-ttu-id="3cc97-140">lblID</span><span class="sxs-lookup"><span data-stu-id="3cc97-140">lblID</span></span>|<span data-ttu-id="3cc97-141">ID</span><span class="sxs-lookup"><span data-stu-id="3cc97-141">ID</span></span>|  
   |<span data-ttu-id="3cc97-142">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="3cc97-142">TextBox</span></span>|<span data-ttu-id="3cc97-143">txtFirstName</span><span class="sxs-lookup"><span data-stu-id="3cc97-143">txtFirstName</span></span>||  
   |<span data-ttu-id="3cc97-144">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="3cc97-144">TextBox</span></span>|<span data-ttu-id="3cc97-145">txtLastName</span><span class="sxs-lookup"><span data-stu-id="3cc97-145">txtLastName</span></span>||  
   |<span data-ttu-id="3cc97-146">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="3cc97-146">TextBox</span></span>|<span data-ttu-id="3cc97-147">txtAddress</span><span class="sxs-lookup"><span data-stu-id="3cc97-147">txtAddress</span></span>||  
   |<span data-ttu-id="3cc97-148">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="3cc97-148">TextBox</span></span>|<span data-ttu-id="3cc97-149">txtID</span><span class="sxs-lookup"><span data-stu-id="3cc97-149">txtID</span></span>||  
   |<span data-ttu-id="3cc97-150">Nút</span><span class="sxs-lookup"><span data-stu-id="3cc97-150">Button</span></span>|<span data-ttu-id="3cc97-151">btnUpdate</span><span class="sxs-lookup"><span data-stu-id="3cc97-151">btnUpdate</span></span>|<span data-ttu-id="3cc97-152">Cập nhật các giá trị trong ứng dụng được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="3cc97-152">Update values in hosted apps</span></span>|  
   |<span data-ttu-id="3cc97-153">Nút</span><span class="sxs-lookup"><span data-stu-id="3cc97-153">Button</span></span>|<span data-ttu-id="3cc97-154">btnUpdateContext</span><span class="sxs-lookup"><span data-stu-id="3cc97-154">btnUpdateContext</span></span>|<span data-ttu-id="3cc97-155">Cập nhật ngữ cảnh</span><span class="sxs-lookup"><span data-stu-id="3cc97-155">Update context</span></span>|  
  
    <span data-ttu-id="3cc97-156">Đây là cách các kiểm soát nên được đặt trong trình thiết kế.</span><span class="sxs-lookup"><span data-stu-id="3cc97-156">This is how the controls should be laid out in the designer.</span></span>  
  
   <span data-ttu-id="3cc97-157">![Layout of the controls in your UII hosted control](../unified-service-desk/media/usd-ui-iwindows-form-hosted-control-design.png "Layout of the controls in your UII hosted control")</span><span class="sxs-lookup"><span data-stu-id="3cc97-157">![Layout of the controls in your UII hosted control](../unified-service-desk/media/usd-ui-iwindows-form-hosted-control-design.png "Layout of the controls in your UII hosted control")</span></span>  
  
5. <span data-ttu-id="3cc97-158">Bấm đúp vào nút **Cập nhật các giá trị trong ứng dụng được lưu trữ** (`btnUpdate`) để thêm mã cho sự kiện `click` cho nút này và thêm mã sau.</span><span class="sxs-lookup"><span data-stu-id="3cc97-158">Double-click the **Update values in hosted apps** button (`btnUpdate`) to add the code for the `click` event for this button, and add the following code.</span></span>  
  
   ```csharp  
   private void btnUpdate_Click(object sender, EventArgs e)  
   {  
      // This is how you fire an action to other hosted applications.   
      // The DoAction() code in the other application or application adapter   
      // will be called.  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateFirstName", txtFirstName.Text)); // For the external application  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateLastName", txtLastName.Text)); // For the external application  
      FireRequestAction(new RequestActionEventArgs("QsExternalApp", "UpdateAddress", txtAddress.Text)); // For the external application  
  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateFirstName", txtFirstName.Text)); // For the external web application  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateLastName", txtLastName.Text)); // For the external web application  
      FireRequestAction(new RequestActionEventArgs("QsWebApplication", "UpdateAddress", txtAddress.Text)); // For the external web application  
   }  
   ```  
  
6. <span data-ttu-id="3cc97-159">Đi đến chế độ xem thiết kế, bấm đúp vào nút **Cập nhật ngữ cảnh** (`btnUpdateContext`) để thêm mã cho sự kiện bấm chuột cho nút này.</span><span class="sxs-lookup"><span data-stu-id="3cc97-159">Go to the design view, double-click the **Update context** button (`btnUpdateContext`) to add the code for the click event for this button.</span></span> <span data-ttu-id="3cc97-160">Thêm mã sau.</span><span class="sxs-lookup"><span data-stu-id="3cc97-160">Add the following code.</span></span>  
  
   ```csharp  
   private void btnUpdateContext_Click(object sender, EventArgs e)  
   {  
      // Get the current context and create a new context object from it.  
      string temp = Context.GetContext();  
      Context updatedContext = new Context(temp);  
  
      // Update the new context with the changed information.  
      updatedContext["firstname"] = txtFirstName.Text;  
      updatedContext["lastname"] = txtLastName.Text;  
      updatedContext["address1_line1"] = txtAddress.Text;  
  
      // Notify Unified Service Desk of this new context information  
      FireChangeContext(new ContextEventArgs(updatedContext));  
  
      // Notify this UII hosted control about the change  
      NotifyContextChange(updatedContext);  
   }  
   ```  
  
7. <span data-ttu-id="3cc97-161">In the same file (UiiWinformControl.cs), update the override definition of the `NotifyContextChange` method to the following:</span><span class="sxs-lookup"><span data-stu-id="3cc97-161">In the same file (UiiWinformControl.cs), update the override definition of the `NotifyContextChange` method to the following:</span></span>  
  
   ```csharp  
   public override void NotifyContextChange(Context context)  
   {  
      // Populating text fields from context information.  
      txtFirstName.Text = context["firstname"];  
      txtLastName.Text = context["lastname"];  
      txtAddress.Text = context["address1_line1"];  
      txtID.Text = context["CustomerID"];  
  
      base.NotifyContextChange(context);  
   }  
   ```  
  
8. <span data-ttu-id="3cc97-162">Save your project, and build it (**Build** > **Build Solution**).</span><span class="sxs-lookup"><span data-stu-id="3cc97-162">Save your project, and build it (**Build** > **Build Solution**).</span></span> <span data-ttu-id="3cc97-163">After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWindowsFormHostedConrol1.dll) in the /bin/debug folder of your project.</span><span class="sxs-lookup"><span data-stu-id="3cc97-163">After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWindowsFormHostedConrol1.dll) in the /bin/debug folder of your project.</span></span>  
  
9. <span data-ttu-id="3cc97-164">Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD).</span><span class="sxs-lookup"><span data-stu-id="3cc97-164">Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD).</span></span> <span data-ttu-id="3cc97-165">Cần có tệp này để thử nghiệm và cuối cùng là sử dụng kiểm soát này từ ứng dụng khách của bạn.</span><span class="sxs-lookup"><span data-stu-id="3cc97-165">This file is required for testing, and eventually using this control from your client application.</span></span>  
  
   > [!TIP]
   >  <span data-ttu-id="3cc97-166">Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWinformControl.cs file.</span><span class="sxs-lookup"><span data-stu-id="3cc97-166">Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWinformControl.cs file.</span></span> <span data-ttu-id="3cc97-167">Trong trường hợp này, đó là UiiWinformControl.</span><span class="sxs-lookup"><span data-stu-id="3cc97-167">In this case, it’s UiiWinformControl.</span></span> <span data-ttu-id="3cc97-168">Bạn sẽ cần thông tin này trong bước tiếp theo.</span><span class="sxs-lookup"><span data-stu-id="3cc97-168">You’ll need this information in the next step.</span></span>  
  
<a name="step2"></a>   
## <a name="step-2-define-the-hosted-control-in-unified-service-desk"></a><span data-ttu-id="3cc97-169">Bước 2: Xác định kiểm soát tổ chức trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="3cc97-169">Step 2: Define the hosted control in Unified Service Desk</span></span>  
 <span data-ttu-id="3cc97-170">Để lưu trữ kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải xác định và đặt cấu hình chúng.</span><span class="sxs-lookup"><span data-stu-id="3cc97-170">To host the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Windows Forms hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you’ll have to define and configure it.</span></span>  
  
1. <span data-ttu-id="3cc97-171">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3cc97-171">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="3cc97-172">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-172">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="3cc97-173">On the **Unified Service Desk** page, click **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-173">On the **Unified Service Desk** page, click **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="3cc97-174">Trên trang **Kiểm soát Tổ chức**, bấm vào **Mới**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-174">On the **Hosted Controls** page, click **New**.</span></span>  
  
5. <span data-ttu-id="3cc97-175">On the **New Hosted Control** page, specify the following values:</span><span class="sxs-lookup"><span data-stu-id="3cc97-175">On the **New Hosted Control** page, specify the following values:</span></span>  
  
   |<span data-ttu-id="3cc97-176">Trường</span><span class="sxs-lookup"><span data-stu-id="3cc97-176">Field</span></span>|<span data-ttu-id="3cc97-177">Value</span><span class="sxs-lookup"><span data-stu-id="3cc97-177">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="3cc97-178">Tên</span><span class="sxs-lookup"><span data-stu-id="3cc97-178">Name</span></span>|<span data-ttu-id="3cc97-179">UIIWindowsFormHostedControl</span><span class="sxs-lookup"><span data-stu-id="3cc97-179">UIIWindowsFormHostedControl</span></span>|  
   |<span data-ttu-id="3cc97-180">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="3cc97-180">Display Name</span></span>|<span data-ttu-id="3cc97-181">Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu</span><span class="sxs-lookup"><span data-stu-id="3cc97-181">Sample UII Windows Forms Hosted Control</span></span>|  
   |<span data-ttu-id="3cc97-182">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="3cc97-182">USD Component Type</span></span>|<span data-ttu-id="3cc97-183">Ứng dụng được lưu trữ CCA</span><span class="sxs-lookup"><span data-stu-id="3cc97-183">CCA Hosted Application</span></span>|  
   |<span data-ttu-id="3cc97-184">Ứng dụng được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="3cc97-184">Hosted Application</span></span>|<span data-ttu-id="3cc97-185">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="3cc97-185">Hosted Control</span></span>|  
   |<span data-ttu-id="3cc97-186">Ứng dụng toàn cầu</span><span class="sxs-lookup"><span data-stu-id="3cc97-186">Application is Global</span></span>|<span data-ttu-id="3cc97-187">Được chọn</span><span class="sxs-lookup"><span data-stu-id="3cc97-187">Selected</span></span>|  
   |<span data-ttu-id="3cc97-188">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="3cc97-188">Display Group</span></span>|<span data-ttu-id="3cc97-189">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="3cc97-189">MainPanel</span></span>|  
   |<span data-ttu-id="3cc97-190">Bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="3cc97-190">Adapter</span></span>|<span data-ttu-id="3cc97-191">Use No Adapter</span><span class="sxs-lookup"><span data-stu-id="3cc97-191">Use No Adapter</span></span>|  
   |<span data-ttu-id="3cc97-192">URI cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="3cc97-192">Assembly URI</span></span>|<span data-ttu-id="3cc97-193">UIIWindowsFormHostedControl1</span><span class="sxs-lookup"><span data-stu-id="3cc97-193">UIIWindowsFormHostedControl1</span></span>|  
   |<span data-ttu-id="3cc97-194">Loại cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="3cc97-194">Assembly Type</span></span>|<span data-ttu-id="3cc97-195">UIIWindowsFormHostedControl1.UiiWinformControl</span><span class="sxs-lookup"><span data-stu-id="3cc97-195">UIIWindowsFormHostedControl1.UiiWinformControl</span></span>|  
  
   > [!NOTE]
   > <span data-ttu-id="3cc97-196">**URI cụm tổ hợp** là tên của cụm tổ hợp của bạn và **Loại Cụm tổ hợp** là tên của cụm tổ hợp của bạn theo sau là dấu chấm (.) và sau đó là tên lớp trong dự án [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] của bạn.</span><span class="sxs-lookup"><span data-stu-id="3cc97-196">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="3cc97-197">Trong ví dụ này, tên của cụm tổ hợp là `UIIWindowsFormHostedControl1` và tên của lớp là `UiiWinformControl`, là tên lớp mặc định khi bạn tạo kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-197">In this example, the name of the assembly is `UIIWindowsFormHostedControl1` and name of the class is `UiiWinformControl`, which is the default class name when you create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Windows Forms hosted control.</span></span>  
  
   <span data-ttu-id="3cc97-198">![New hosted control in Unified Service Desk](../unified-service-desk/media/usd-new-hosted-control-uii-windows-form.png "New hosted control in Unified Service Desk")</span><span class="sxs-lookup"><span data-stu-id="3cc97-198">![New hosted control in Unified Service Desk](../unified-service-desk/media/usd-new-hosted-control-uii-windows-form.png "New hosted control in Unified Service Desk")</span></span>  
  
6. <span data-ttu-id="3cc97-199">Click **Save** to create the hosted control.</span><span class="sxs-lookup"><span data-stu-id="3cc97-199">Click **Save** to create the hosted control.</span></span>  
  
<a name="step3"></a>   
## <a name="step-3-define-uii-actions-for-the-external-application-and-web-application-hosted-controls-in-unified-service-desk"></a><span data-ttu-id="3cc97-200">Bước 3: Xác định hành động UII cho kiểm soát tổ chức ứng dụng bên ngoài và ứng dụng web trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="3cc97-200">Step 3: Define UII actions for the external application and web application hosted controls in Unified Service Desk</span></span>  
 <span data-ttu-id="3cc97-201">Bộ chuyển đổi cho các ứng dụng độc lập và web hiển thị ba hành động sau: `UpdateFirstName`, `UpdateLastName` và `UpdateAddress`.</span><span class="sxs-lookup"><span data-stu-id="3cc97-201">The adapters for the external standalone and web applications expose the following three actions: `UpdateFirstName`, `UpdateLastName`, and `UpdateAddress`.</span></span> <span data-ttu-id="3cc97-202">These adapters and the hosted controls for the external standalone and web applications were created in the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).</span><span class="sxs-lookup"><span data-stu-id="3cc97-202">These adapters and the hosted controls for the external standalone and web applications were created in the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).</span></span>  
  
 <span data-ttu-id="3cc97-203">Để cập nhật thông tin trong các ứng dụng bên ngoài từ trong [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] kiểm soát tổ chức Biểu mẫu Windows, bạn sẽ phải xác định ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên như được định nghĩa trước trong các bộ chuyển đổi cho mỗi ứng dụng bên ngoài.</span><span class="sxs-lookup"><span data-stu-id="3cc97-203">To update information in the external applications from within the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Windows Forms hosted control, you’ll have to define three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same name as defined earlier in the adapters for each of the external applications.</span></span> <span data-ttu-id="3cc97-204">In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), you defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: `QsExternalApp` and `QsExternalWebApplication`.</span><span class="sxs-lookup"><span data-stu-id="3cc97-204">In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), you defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]: `QsExternalApp` and `QsExternalWebApplication`.</span></span> <span data-ttu-id="3cc97-205">Trong bước này, bạn sẽ thêm ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho mỗi kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="3cc97-205">In this step, you’ll add three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions for each hosted control.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="3cc97-206">If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII WPF Hosted Control](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md), you don’t have to perform this step again.</span><span class="sxs-lookup"><span data-stu-id="3cc97-206">If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII WPF Hosted Control](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md), you don’t have to perform this step again.</span></span> <span data-ttu-id="3cc97-207">Bạn có thể tiến hành phần tiếp theo để kiểm tra kiểm soát tổ chức của mình.</span><span class="sxs-lookup"><span data-stu-id="3cc97-207">You can proceed to the next section for testing your hosted control.</span></span>  
  
1. <span data-ttu-id="3cc97-208">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="3cc97-208">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="3cc97-209">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-209">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="3cc97-210">On the **Unified Service Desk** page, choose **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-210">On the **Unified Service Desk** page, choose **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="3cc97-211">Trên trang **Kiểm soát Tổ chức**, tìm kiếm `QsExternalApp` và mở để chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="3cc97-211">On the **Hosted Controls** page, search for the `QsExternalApp`, and open it for editing.</span></span>  
  
5. <span data-ttu-id="3cc97-212">Trên trang **QsExternalApp**, bấm vào mũi tên xuống bên cạnh tên kiểm soát tổ chức, rồi bấm vào **Hành động UII**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-212">On the **QsExternalApp** page, click the down arrow next to the hosted control name, and then click **UII Actions**.</span></span>  
  
6. <span data-ttu-id="3cc97-213">Trên trang tiếp theo, bấm vào **thêm hành động UII mới**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-213">On the next page, click **Add New UII Action**.</span></span>  
  
7. <span data-ttu-id="3cc97-214">Nhập tên là **UpdateFirstName** và bấm vào **Lưu & Đóng**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-214">Type the name as **UpdateFirstName**, and click **Save & Close**.</span></span> <span data-ttu-id="3cc97-215">Thao tác này sẽ thêm hành động vào trang trước.</span><span class="sxs-lookup"><span data-stu-id="3cc97-215">This will add the action in the previous page.</span></span>  
  
8. <span data-ttu-id="3cc97-216">Tương tự, thêm hai hành động sau: **UpdateLastName** và **UpdateAddress**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-216">Similarly, add the following two actions: **UpdateLastName** and **UpdateAddress**.</span></span> <span data-ttu-id="3cc97-217">Tất cả ba hành động này sẽ có sẵn cho kiểm soát tổ chức `QsExternalApp`.</span><span class="sxs-lookup"><span data-stu-id="3cc97-217">All the three actions become available for the `QsExternalApp` hosted control.</span></span>  
  
   <span data-ttu-id="3cc97-218">![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="3cc97-218">![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")</span></span>  
  
9. <span data-ttu-id="3cc97-219">Làm theo các bước 4 đến 8 để tạo ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên cho kiểm soát tổ chức `QsExternalWebApp`.</span><span class="sxs-lookup"><span data-stu-id="3cc97-219">Follow steps 4 through 8 to create three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same names for the `QsExternalWebApp` hosted control.</span></span>  
  
<a name="test"></a>   
## <a name="test-the-hosted-control"></a><span data-ttu-id="3cc97-220">Kiểm tra kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="3cc97-220">Test the hosted control</span></span>  
 <span data-ttu-id="3cc97-221">Trước khi bạn kiểm tra kiểm soát tổ chức Biểu mẫu Windows [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)], đảm bảo rằng ứng dụng web mẫu của bạn đang chạy sao cho ứng dụng hiển thị bên trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-221">Before you test the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] Windows Forms hosted control, ensure that your sample web application is running so that it renders within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
1. <span data-ttu-id="3cc97-222">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="3cc97-222">Run the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span>  
  
2. <span data-ttu-id="3cc97-223">Trên lần đăng nhập an toàn, bạn sẽ nhìn thấy ba kiểm soát tổ chức: **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, **Ứng dụng Web Bên ngoài Mẫu** và **Ứng dụng Bên ngoài Mẫu**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-223">On successful sign in, you’ll see three hosted controls: **Sample UII Windows Forms Hosted Control**, **Sample External Web Application**, and **Sample External Application**.</span></span>  
  
   <span data-ttu-id="3cc97-224">![Sample hosted controls available](../unified-service-desk/media/usd-sample-hosted-controls-available.png "Sample hosted controls available")</span><span class="sxs-lookup"><span data-stu-id="3cc97-224">![Sample hosted controls available](../unified-service-desk/media/usd-sample-hosted-controls-available.png "Sample hosted controls available")</span></span>  
  
3. <span data-ttu-id="3cc97-225">Chọn **Tìm kiếm** rồi chọn **Người liên hệ**.</span><span class="sxs-lookup"><span data-stu-id="3cc97-225">Choose **Search**, and then choose **Contacts**.</span></span> <span data-ttu-id="3cc97-226">Chọn bất kỳ người liên hệ nào để hiển thị chi tiết liên hệ trong một phiên.</span><span class="sxs-lookup"><span data-stu-id="3cc97-226">Choose any of the contacts to display the contact details in a session.</span></span> <span data-ttu-id="3cc97-227">Điều này cũng hiển thị tên, họ, địa chỉ đường phố và ID của hồ sơ liên hệ hiện được hiển thị trong tất cả ba kiểm soát mẫu như được trình bày trong hình minh họa sau.</span><span class="sxs-lookup"><span data-stu-id="3cc97-227">This also displays the first name, last name, street address, and ID of the currently displayed contact record in all the three sample controls as shown in the following illustration.</span></span>  
  
   <span data-ttu-id="3cc97-228">![Sample controls in USD with contact information](../unified-service-desk/media/usd-3-samplecontrols-1.png "Sample controls in USD with contact information")</span><span class="sxs-lookup"><span data-stu-id="3cc97-228">![Sample controls in USD with contact information](../unified-service-desk/media/usd-3-samplecontrols-1.png "Sample controls in USD with contact information")</span></span>  
  
4. <span data-ttu-id="3cc97-229">Thay đổi các giá trị trong **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu** và bấm vào **Cập nhật giá trị trong ứng dụng được lưu trữ** để cập nhật các giá trị trong hai ứng dụng bên ngoài khác.</span><span class="sxs-lookup"><span data-stu-id="3cc97-229">Change the values in **Sample UII Windows Forms Hosted Control**, and click **Update values in hosted apps** to update the values in the other two external applications.</span></span>  
  
   <span data-ttu-id="3cc97-230">![Sample controls with updated values](../unified-service-desk/media/usd-3-sample-controls-updated-values.png "Sample controls with updated values")</span><span class="sxs-lookup"><span data-stu-id="3cc97-230">![Sample controls with updated values](../unified-service-desk/media/usd-3-sample-controls-updated-values.png "Sample controls with updated values")</span></span>  
  
5. <span data-ttu-id="3cc97-231">Trong **Kiểm soát Tổ chức Biểu mẫu Windows UII Mẫu**, bấm vào **Cập nhật ngữ cảnh** để cập nhật thông tin ngữ cảnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="3cc97-231">In **Sample UII Windows Forms Hosted Control**, click **Update context** to update the context information in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   <span data-ttu-id="3cc97-232">![Values updated in the USD context](../unified-service-desk/media/usd-values-updated-context.png "Values updated in the USD context")</span><span class="sxs-lookup"><span data-stu-id="3cc97-232">![Values updated in the USD context](../unified-service-desk/media/usd-values-updated-context.png "Values updated in the USD context")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="3cc97-233">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="3cc97-233">See also</span></span>  
 <span data-ttu-id="3cc97-234">[Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="3cc97-234">[Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span></span>  
 [<span data-ttu-id="3cc97-235">Cách: Tạo Kiểm soát Tổ chức UII WPF</span><span class="sxs-lookup"><span data-stu-id="3cc97-235">Walkthrough: Create a WPF UII Hosted Control</span></span>](../unified-service-desk/walkthrough-create-uii-wpf-hosted-control.md)
