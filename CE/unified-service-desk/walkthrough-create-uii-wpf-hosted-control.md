---
title: 'Walkthrough: Create a UII WPF Hosted Control | MicrosoftDocs'
description: Demonstrates how you can build a WPF-based User Interface Integration (UII) hosted control that interacts with Unified Service Desk and external applications (standalone and web).
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
ms.assetid: 4a6e9113-3956-448c-9953-ec7ee6f22d9e
author: kabala123
ms.author: kabala
manager: shujoshi
search.audienceType:
- customizer
- developer
search.app:
- D365CE
- D365USD
ms.openlocfilehash: 7f65042a084c1c5caedb6345f5d659705e5dab9c
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387850"
---
# <a name="walkthrough-create-a-uii-wpf-hosted-control-in-unified-service-desk"></a><span data-ttu-id="74c9d-103">Walkthrough: Create a UII WPF Hosted Control in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="74c9d-103">Walkthrough: Create a UII WPF Hosted Control in Unified Service Desk</span></span>
<span data-ttu-id="74c9d-104">Cách này trình bày cách bạn có thể xây dựng kiểm soát tổ chức dựa trên [Windows Presentation Foundation (WPF)](https://msdn.microsoft.com/library/ms754130\(v=vs.110\).aspx) [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] tương tác với [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] và các ứng dụng bên ngoài (độc lập và web).</span><span class="sxs-lookup"><span data-stu-id="74c9d-104">This walkthrough demonstrates how you can build a [Windows Presentation Foundation (WPF)](https://msdn.microsoft.com/library/ms754130\(v=vs.110\).aspx)-based [!INCLUDE[pn_user_inteface_integration_uii](../includes/pn-user-interface-integration-uii.md)] hosted control that interacts with [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] and external applications (standalone and web).</span></span>  
  
 <span data-ttu-id="74c9d-105">Trong cách này, bạn sẽ:</span><span class="sxs-lookup"><span data-stu-id="74c9d-105">In this walkthrough, you’ll:</span></span>  
  
- <span data-ttu-id="74c9d-106">Create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, **Sample UII WPF Hosted Control**, which will display first name, last name, street address and ID of a contact when you search for contacts, and click a contact name to open it in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-106">Create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, **Sample UII WPF Hosted Control**, which will display first name, last name, street address and ID of a contact when you search for contacts, and click a contact name to open it in a session in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span> <span data-ttu-id="74c9d-107">Các giá trị này được hiển thị từ ngữ cảnh [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-107">These values are displayed from the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context.</span></span>  
  
- <span data-ttu-id="74c9d-108">Change first name, last name, or street address values in an external application and web application hosted in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control that we create.</span><span class="sxs-lookup"><span data-stu-id="74c9d-108">Change first name, last name, or street address values in an external application and web application hosted in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] from the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control that we create.</span></span> <span data-ttu-id="74c9d-109">The external and web applications were created in the following earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span><span class="sxs-lookup"><span data-stu-id="74c9d-109">The external and web applications were created in the following earlier walkthroughs: [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md).</span></span>  
  
- <span data-ttu-id="74c9d-110">Notify changes to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context to update the values there.</span><span class="sxs-lookup"><span data-stu-id="74c9d-110">Notify changes to the [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] context to update the values there.</span></span>  
  
<a name="Prereq"></a>   
## <a name="prerequisites"></a><span data-ttu-id="74c9d-111">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="74c9d-111">Prerequisites</span></span>  
  
- [!INCLUDE[pn_Microsoft_.Net_Framework](../includes/pn-microsoft-net-framework.md)] <span data-ttu-id="74c9d-112">4.5.2</span><span class="sxs-lookup"><span data-stu-id="74c9d-112">4.5.2</span></span>  
  
- [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]<span data-ttu-id="74c9d-113">ứng dụng khách.</span><span class="sxs-lookup"><span data-stu-id="74c9d-113">client application.</span></span> <span data-ttu-id="74c9d-114">Điều này là cần thiết để thử nghiệm kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="74c9d-114">This is required for testing the hosted control.</span></span>  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="74c9d-115">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span><span class="sxs-lookup"><span data-stu-id="74c9d-115">, [!INCLUDE[pn_visual_studio_2013](../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_visual_studio_2015](../includes/pn-visual-studio-2015.md)]</span></span>  
  
- [!INCLUDE[tn_nuget_package_manager](../includes/tn-nuget-package-manager.md)] <span data-ttu-id="74c9d-116">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="74c9d-116">for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="74c9d-117">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contain the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control project template.</span><span class="sxs-lookup"><span data-stu-id="74c9d-117">**CRM SDK Templates** for [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] that contain the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control project template.</span></span> <span data-ttu-id="74c9d-118">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-118">[Download](http://go.microsoft.com/fwlink/p/?LinkId=400925) the **CRM SDK Templates** from the Visual Studio gallery, and double-click the CRMSDKTemplates.vsix file to install the template in [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)].</span></span>  
  
- <span data-ttu-id="74c9d-119">You should have completed the [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external and web applications set up with the adapters to facilitate interaction with those applications.</span><span class="sxs-lookup"><span data-stu-id="74c9d-119">You should have completed the [Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md) to ensure that you have the external and web applications set up with the adapters to facilitate interaction with those applications.</span></span>  
  
<a name="step1"></a>   
## <a name="step-1-create-a-uii-wpf-hosted-control-using-visual-studio"></a><span data-ttu-id="74c9d-120">Step 1: Create a UII WPF hosted control using Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74c9d-120">Step 1: Create a UII WPF hosted control using Visual Studio</span></span>  
  
<a name="Step1"></a>   
1. <span data-ttu-id="74c9d-121">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span><span class="sxs-lookup"><span data-stu-id="74c9d-121">Start [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="74c9d-122">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="74c9d-122">In the **New Project** dialog box:</span></span>  
  
   1.  <span data-ttu-id="74c9d-123">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII WPF Hosted Control**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-123">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates** > **Unified Service Desk** > **UII WPF Hosted Control**.</span></span>  
  
   2.  <span data-ttu-id="74c9d-124">Chỉ định tên và vị trí của dự án và chọn **OK** để tạo dự án mới.</span><span class="sxs-lookup"><span data-stu-id="74c9d-124">Specify the name and location of the project, and choose **OK** to create a new project.</span></span>  
  
   <span data-ttu-id="74c9d-125">![Create a UII WPF hosted control](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-1.png "Create a UII WPF hosted control")</span><span class="sxs-lookup"><span data-stu-id="74c9d-125">![Create a UII WPF hosted control](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-1.png "Create a UII WPF hosted control")</span></span>  
  
3. <span data-ttu-id="74c9d-126">In **Solution Explorer**, right-click the **UiiWpfControl.xaml** file, and select **Open** to display the XAML designer.</span><span class="sxs-lookup"><span data-stu-id="74c9d-126">In **Solution Explorer**, right-click the **UiiWpfControl.xaml** file, and select **Open** to display the XAML designer.</span></span>  
  
4. <span data-ttu-id="74c9d-127">In the designer, add the following controls from the **Toolbox**:</span><span class="sxs-lookup"><span data-stu-id="74c9d-127">In the designer, add the following controls from the **Toolbox**:</span></span>  
  
   |<span data-ttu-id="74c9d-128">Loại kiểm soát</span><span class="sxs-lookup"><span data-stu-id="74c9d-128">Control type</span></span>|<span data-ttu-id="74c9d-129">Tên</span><span class="sxs-lookup"><span data-stu-id="74c9d-129">Name</span></span>|<span data-ttu-id="74c9d-130">Text</span><span class="sxs-lookup"><span data-stu-id="74c9d-130">Text</span></span>|  
   |------------------|----------|----------|  
   |<span data-ttu-id="74c9d-131">Nhãn</span><span class="sxs-lookup"><span data-stu-id="74c9d-131">Label</span></span>|<span data-ttu-id="74c9d-132">lblFirstName</span><span class="sxs-lookup"><span data-stu-id="74c9d-132">lblFirstName</span></span>|<span data-ttu-id="74c9d-133">Tên</span><span class="sxs-lookup"><span data-stu-id="74c9d-133">First Name</span></span>|  
   |<span data-ttu-id="74c9d-134">Nhãn</span><span class="sxs-lookup"><span data-stu-id="74c9d-134">Label</span></span>|<span data-ttu-id="74c9d-135">lblLastName</span><span class="sxs-lookup"><span data-stu-id="74c9d-135">lblLastName</span></span>|<span data-ttu-id="74c9d-136">Họ</span><span class="sxs-lookup"><span data-stu-id="74c9d-136">Last Name</span></span>|  
   |<span data-ttu-id="74c9d-137">Nhãn</span><span class="sxs-lookup"><span data-stu-id="74c9d-137">Label</span></span>|<span data-ttu-id="74c9d-138">lblAddress</span><span class="sxs-lookup"><span data-stu-id="74c9d-138">lblAddress</span></span>|<span data-ttu-id="74c9d-139">Địa chỉ Đường phố</span><span class="sxs-lookup"><span data-stu-id="74c9d-139">Street Address</span></span>|  
   |<span data-ttu-id="74c9d-140">Nhãn</span><span class="sxs-lookup"><span data-stu-id="74c9d-140">Label</span></span>|<span data-ttu-id="74c9d-141">lblID</span><span class="sxs-lookup"><span data-stu-id="74c9d-141">lblID</span></span>|<span data-ttu-id="74c9d-142">ID</span><span class="sxs-lookup"><span data-stu-id="74c9d-142">ID</span></span>|  
   |<span data-ttu-id="74c9d-143">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="74c9d-143">TextBox</span></span>|<span data-ttu-id="74c9d-144">txtFirstName</span><span class="sxs-lookup"><span data-stu-id="74c9d-144">txtFirstName</span></span>||  
   |<span data-ttu-id="74c9d-145">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="74c9d-145">TextBox</span></span>|<span data-ttu-id="74c9d-146">txtLastName</span><span class="sxs-lookup"><span data-stu-id="74c9d-146">txtLastName</span></span>||  
   |<span data-ttu-id="74c9d-147">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="74c9d-147">TextBox</span></span>|<span data-ttu-id="74c9d-148">txtAddress</span><span class="sxs-lookup"><span data-stu-id="74c9d-148">txtAddress</span></span>||  
   |<span data-ttu-id="74c9d-149">Hộp văn bản</span><span class="sxs-lookup"><span data-stu-id="74c9d-149">TextBox</span></span>|<span data-ttu-id="74c9d-150">txtID</span><span class="sxs-lookup"><span data-stu-id="74c9d-150">txtID</span></span>||  
   |<span data-ttu-id="74c9d-151">Nút</span><span class="sxs-lookup"><span data-stu-id="74c9d-151">Button</span></span>|<span data-ttu-id="74c9d-152">btnUpdate</span><span class="sxs-lookup"><span data-stu-id="74c9d-152">btnUpdate</span></span>|<span data-ttu-id="74c9d-153">Update values in hosted apps</span><span class="sxs-lookup"><span data-stu-id="74c9d-153">Update values in hosted apps</span></span>|  
   |<span data-ttu-id="74c9d-154">Nút</span><span class="sxs-lookup"><span data-stu-id="74c9d-154">Button</span></span>|<span data-ttu-id="74c9d-155">btnUpdateContext</span><span class="sxs-lookup"><span data-stu-id="74c9d-155">btnUpdateContext</span></span>|<span data-ttu-id="74c9d-156">Cập nhật ngữ cảnh</span><span class="sxs-lookup"><span data-stu-id="74c9d-156">Update context</span></span>|  
  
    <span data-ttu-id="74c9d-157">This is how the controls should be laid out in the XAML designer.</span><span class="sxs-lookup"><span data-stu-id="74c9d-157">This is how the controls should be laid out in the XAML designer.</span></span>  
  
   <span data-ttu-id="74c9d-158">![Controls layout in the XAML designer](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-2.png "Controls layout in the XAML designer")</span><span class="sxs-lookup"><span data-stu-id="74c9d-158">![Controls layout in the XAML designer](../unified-service-desk/media/usd-create-uii-wpf-hosted-control-2.png "Controls layout in the XAML designer")</span></span>  
  
5. <span data-ttu-id="74c9d-159">Double-click the **Update values in hosted apps** button (btnUpdate) to add the code for the `click` event for this button, and add the following code.</span><span class="sxs-lookup"><span data-stu-id="74c9d-159">Double-click the **Update values in hosted apps** button (btnUpdate) to add the code for the `click` event for this button, and add the following code.</span></span>  
  
   ```csharp  
   private void btnUpdate_Click(object sender, System.Windows.RoutedEventArgs e)  
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
  
6. <span data-ttu-id="74c9d-160">Go to the XAML designer, and double-click the **Update context** button (btnUpdateContext) to add the code for the `click` event for this button.</span><span class="sxs-lookup"><span data-stu-id="74c9d-160">Go to the XAML designer, and double-click the **Update context** button (btnUpdateContext) to add the code for the `click` event for this button.</span></span> <span data-ttu-id="74c9d-161">Add the following code.</span><span class="sxs-lookup"><span data-stu-id="74c9d-161">Add the following code.</span></span>  
  
   ```csharp  
   private void btnContextChange_Click(object sender, System.Windows.RoutedEventArgs e)  
   {  
      // Get the current context and create a new context object from it.  
      string temp = Context.GetContext();  
      Context updatedContext = new Context(temp);  
  
      // Update the new context with the changed information.  
      updatedContext["firstname"] = txtFirstName.Text;  
      updatedContext["lastname"] = txtLastName.Text;  
      updatedContext["address1_line1"] = txtAddress.Text;  
  
      // Notify Unified Service Desk of this new context information.  
      FireChangeContext(new ContextEventArgs(updatedContext));  
  
      // Notify this UII hosted control about the change.  
      NotifyContextChange(updatedContext);  
   }  
   ```  
  
7. <span data-ttu-id="74c9d-162">In the same file (UiiWpfControl.xaml.cs), update the override definition of the `NotifyContextChange` method to the following.</span><span class="sxs-lookup"><span data-stu-id="74c9d-162">In the same file (UiiWpfControl.xaml.cs), update the override definition of the `NotifyContextChange` method to the following.</span></span>  
  
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
  
8. <span data-ttu-id="74c9d-163">Save your project, and build it (**Build** > **Build Solution**).</span><span class="sxs-lookup"><span data-stu-id="74c9d-163">Save your project, and build it (**Build** > **Build Solution**).</span></span> <span data-ttu-id="74c9d-164">After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWPFHostedControl1.dll) in the /bin/debug folder of your project.</span><span class="sxs-lookup"><span data-stu-id="74c9d-164">After the project builds successfully, an assembly (.dll file) is generated with the same name as your project name (in this case, UIIWPFHostedControl1.dll) in the /bin/debug folder of your project.</span></span>  
  
9. <span data-ttu-id="74c9d-165">Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD).</span><span class="sxs-lookup"><span data-stu-id="74c9d-165">Copy this file to your [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client application installation directory (typically C:\Program Files\Microsoft Dynamics CRM USD\USD).</span></span> <span data-ttu-id="74c9d-166">This file is required for testing, and eventually using this control from your client application.</span><span class="sxs-lookup"><span data-stu-id="74c9d-166">This file is required for testing, and eventually using this control from your client application.</span></span>  
  
   > [!TIP]
   >  <span data-ttu-id="74c9d-167">Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWpfControl.xaml.cs file.</span><span class="sxs-lookup"><span data-stu-id="74c9d-167">Note the name of the class that is used to build your [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] hosted control in the UiiWpfControl.xaml.cs file.</span></span> <span data-ttu-id="74c9d-168">Trong trường hợp này, đó là `UiiWpfControl`.</span><span class="sxs-lookup"><span data-stu-id="74c9d-168">In this case, it’s `UiiWpfControl`.</span></span> <span data-ttu-id="74c9d-169">You’ll need this information in the next step.</span><span class="sxs-lookup"><span data-stu-id="74c9d-169">You’ll need this information in the next step.</span></span>  
  
<a name="step2"></a>   
## <a name="step-2-define-the-hosted-control-in-unified-service-desk"></a><span data-ttu-id="74c9d-170">Bước 2: Xác định kiểm soát tổ chức trong Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="74c9d-170">Step 2: Define the hosted control in Unified Service Desk</span></span>  
 <span data-ttu-id="74c9d-171">Để lưu trữ [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] kiểm soát tổ chức WPF trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], bạn sẽ phải xác định và đặt cấu hình kiểm soát đó.</span><span class="sxs-lookup"><span data-stu-id="74c9d-171">To host the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] WPF hosted control in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)], you’ll have to define and configure it.</span></span>  
  
1. <span data-ttu-id="74c9d-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="74c9d-172">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="74c9d-173">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-173">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="74c9d-174">On the **Unified Service Desk** page, choose **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-174">On the **Unified Service Desk** page, choose **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="74c9d-175">Trên trang **Kiểm soát Tổ chức**, chọn **Mới**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-175">On the **Hosted Controls** page, choose **New**.</span></span>  
  
5. <span data-ttu-id="74c9d-176">On the **New Hosted Control** page, specify the following values.</span><span class="sxs-lookup"><span data-stu-id="74c9d-176">On the **New Hosted Control** page, specify the following values.</span></span>  
  
   |<span data-ttu-id="74c9d-177">Trường</span><span class="sxs-lookup"><span data-stu-id="74c9d-177">Field</span></span>|<span data-ttu-id="74c9d-178">Value</span><span class="sxs-lookup"><span data-stu-id="74c9d-178">Value</span></span>|  
   |-----------|-----------|  
   |<span data-ttu-id="74c9d-179">Tên</span><span class="sxs-lookup"><span data-stu-id="74c9d-179">Name</span></span>|<span data-ttu-id="74c9d-180">UIIWPFHostedControl</span><span class="sxs-lookup"><span data-stu-id="74c9d-180">UIIWPFHostedControl</span></span>|  
   |<span data-ttu-id="74c9d-181">Tên Hiển thị</span><span class="sxs-lookup"><span data-stu-id="74c9d-181">Display Name</span></span>|<span data-ttu-id="74c9d-182">Sample UII WPF Hosted Control</span><span class="sxs-lookup"><span data-stu-id="74c9d-182">Sample UII WPF Hosted Control</span></span>|  
   |<span data-ttu-id="74c9d-183">USD Component Type</span><span class="sxs-lookup"><span data-stu-id="74c9d-183">USD Component Type</span></span>|<span data-ttu-id="74c9d-184">CCA Hosted Application</span><span class="sxs-lookup"><span data-stu-id="74c9d-184">CCA Hosted Application</span></span>|  
   |<span data-ttu-id="74c9d-185">Ứng dụng được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="74c9d-185">Hosted Application</span></span>|<span data-ttu-id="74c9d-186">Kiểm soát được lưu trữ</span><span class="sxs-lookup"><span data-stu-id="74c9d-186">Hosted Control</span></span>|  
   |<span data-ttu-id="74c9d-187">Ứng dụng toàn cầu</span><span class="sxs-lookup"><span data-stu-id="74c9d-187">Application is Global</span></span>|<span data-ttu-id="74c9d-188">Được chọn</span><span class="sxs-lookup"><span data-stu-id="74c9d-188">Selected</span></span>|  
   |<span data-ttu-id="74c9d-189">Nhóm hiển thị</span><span class="sxs-lookup"><span data-stu-id="74c9d-189">Display Group</span></span>|<span data-ttu-id="74c9d-190">Bảng điều khiển chính</span><span class="sxs-lookup"><span data-stu-id="74c9d-190">MainPanel</span></span>|  
   |<span data-ttu-id="74c9d-191">Bộ điều hợp</span><span class="sxs-lookup"><span data-stu-id="74c9d-191">Adapter</span></span>|<span data-ttu-id="74c9d-192">Use No Adapter</span><span class="sxs-lookup"><span data-stu-id="74c9d-192">Use No Adapter</span></span>|  
   |<span data-ttu-id="74c9d-193">URI cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="74c9d-193">Assembly URI</span></span>|<span data-ttu-id="74c9d-194">UIIWPFHostedControl1</span><span class="sxs-lookup"><span data-stu-id="74c9d-194">UIIWPFHostedControl1</span></span>|  
   |<span data-ttu-id="74c9d-195">Loại cụm tổ hợp</span><span class="sxs-lookup"><span data-stu-id="74c9d-195">Assembly Type</span></span>|<span data-ttu-id="74c9d-196">UIIWPFHostedControl1.UiiWpfControl</span><span class="sxs-lookup"><span data-stu-id="74c9d-196">UIIWPFHostedControl1.UiiWpfControl</span></span>|  
  
   > [!NOTE]
   > <span data-ttu-id="74c9d-197">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span><span class="sxs-lookup"><span data-stu-id="74c9d-197">**Assembly URI** is the name of your assembly and the **Assembly Type** is the name of your assembly followed by a dot (.) and then the class name in your [!INCLUDE[pn_Visual_Studio_short](../includes/pn-visual-studio-short.md)] project.</span></span> <span data-ttu-id="74c9d-198">Trong ví dụ này, tên của cụm tổ hợp là `UIIWPFHostedControl1` và tên của lớp là `UiiWpfControl`, tên lớp mặc định khi bạn tạo kiểm soát tổ chức WPF [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-198">In this example, the name of the assembly is `UIIWPFHostedControl1` and name of the class is `UiiWpfControl`, which is the default class name when you create a [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] WPF hosted control.</span></span>  
  
   <span data-ttu-id="74c9d-199">![Define a new hosted control](../unified-service-desk/media/usd-new-hosted-control-uii-wpf.png "Define a new hosted control")</span><span class="sxs-lookup"><span data-stu-id="74c9d-199">![Define a new hosted control](../unified-service-desk/media/usd-new-hosted-control-uii-wpf.png "Define a new hosted control")</span></span>  
  
6. <span data-ttu-id="74c9d-200">Choose **Save** to create the hosted control.</span><span class="sxs-lookup"><span data-stu-id="74c9d-200">Choose **Save** to create the hosted control.</span></span>  
  
<a name="step3"></a>   
## <a name="step-3-define-uii-actions-for-the-external-application-and-web-application-hosted-controls-in-unified-service-desk"></a><span data-ttu-id="74c9d-201">Step 3: Define UII actions for the external application and web application hosted controls in Unified Service Desk</span><span class="sxs-lookup"><span data-stu-id="74c9d-201">Step 3: Define UII actions for the external application and web application hosted controls in Unified Service Desk</span></span>  
 <span data-ttu-id="74c9d-202">Bộ chuyển đổi cho các ứng dụng độc lập và web hiển thị ba hành động sau: `UpdateFirstName`, `UpdateLastName` và `UpdateAddress`.</span><span class="sxs-lookup"><span data-stu-id="74c9d-202">The adapters for the external standalone and web applications expose the following three actions: `UpdateFirstName`, `UpdateLastName`, and `UpdateAddress`.</span></span> <span data-ttu-id="74c9d-203">These adapters and the hosted controls for the external standalone and web applications were created in the earlier walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).</span><span class="sxs-lookup"><span data-stu-id="74c9d-203">These adapters and the hosted controls for the external standalone and web applications were created in the earlier walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)).</span></span>  
  
 <span data-ttu-id="74c9d-204">To update information in the external applications from within the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] WPF hosted control, you’ll have to define three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same name as defined earlier in the adapters for each of the external applications.</span><span class="sxs-lookup"><span data-stu-id="74c9d-204">To update information in the external applications from within the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] WPF hosted control, you’ll have to define three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same name as defined earlier in the adapters for each of the external applications.</span></span> <span data-ttu-id="74c9d-205">In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application  Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), we defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  `QsExternalApp` and `QsExternalWebApplication`.</span><span class="sxs-lookup"><span data-stu-id="74c9d-205">In the earlier adapter walkthroughs ([Walkthrough: Create a UII Application Adapter](../unified-service-desk/walkthrough-create-uii-application-adapter.md) and [Walkthrough: Create a UII Web Application  Adapter](../unified-service-desk/walkthrough-create-uii-web-application-adapter.md)), we defined the following two hosted controls in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] to display the external applications within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)]:  `QsExternalApp` and `QsExternalWebApplication`.</span></span> <span data-ttu-id="74c9d-206">Trong bước này, chúng ta sẽ thêm ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] cho mỗi kiểm soát tổ chức.</span><span class="sxs-lookup"><span data-stu-id="74c9d-206">In this step, we will add three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions for each hosted control.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="74c9d-207">If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md), you don’t have to perform this step again.</span><span class="sxs-lookup"><span data-stu-id="74c9d-207">If you have already added the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions as part of step 3 in [Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md), you don’t have to perform this step again.</span></span> <span data-ttu-id="74c9d-208">You can proceed to the next section for testing your hosted control.</span><span class="sxs-lookup"><span data-stu-id="74c9d-208">You can proceed to the next section for testing your hosted control.</span></span>  
  
1. <span data-ttu-id="74c9d-209">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span><span class="sxs-lookup"><span data-stu-id="74c9d-209">Sign in to [!INCLUDE[pn_microsoftcrm](../includes/pn-microsoftcrm.md)] apps.</span></span>  
  
2. <span data-ttu-id="74c9d-210">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-210">On the nav bar, choose **Microsoft Dynamics 365 for Customer Engagement** > **Settings** > **Unified Service Desk**.</span></span>  
  
3. <span data-ttu-id="74c9d-211">On the **Unified Service Desk** page, choose **Hosted Controls**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-211">On the **Unified Service Desk** page, choose **Hosted Controls**.</span></span>  
  
4. <span data-ttu-id="74c9d-212">Trên trang **Kiểm soát Tổ chức**, tìm kiếm `QSExternalApp` và mở để chỉnh sửa.</span><span class="sxs-lookup"><span data-stu-id="74c9d-212">On the **Hosted Controls** page, search for the `QSExternalApp`, and open it for editing.</span></span>  
  
5. <span data-ttu-id="74c9d-213">Trên trang `QSExternalApp`, chọn mũi tên xuống bên cạnh tên kiểm soát tổ chức rồi chọn **Hành động UII**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-213">On the `QSExternalApp` page, choose the down arrow next to the hosted control name, and then choose **UII Actions**.</span></span>  
  
6. <span data-ttu-id="74c9d-214">Trên trang tiếp theo, chọn **Thêm Hành động UII Mới**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-214">On the next page, choose **Add New UII Action**.</span></span>  
  
7. <span data-ttu-id="74c9d-215">Trên trang **Hành động UII Mới**, nhập tên dưới dạng `UpdateFirstName` và chọn **Lưu & Đóng**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-215">On the **New UII Action** page, type the name as `UpdateFirstName`, and choose **Save & Close**.</span></span> <span data-ttu-id="74c9d-216">Thao tác này thêm hành động vào trang trước.</span><span class="sxs-lookup"><span data-stu-id="74c9d-216">This adds the action in the previous page.</span></span>  
  
8. <span data-ttu-id="74c9d-217">Tương tự, thêm hai hành động sau:  `UpdateLastName` và `UpdateAddress`.</span><span class="sxs-lookup"><span data-stu-id="74c9d-217">Similarly, add the following two actions:  `UpdateLastName` and `UpdateAddress`.</span></span> <span data-ttu-id="74c9d-218">Tất cả ba hành động này sẽ có sẵn cho kiểm soát tổ chức `QSExternalApp`.</span><span class="sxs-lookup"><span data-stu-id="74c9d-218">All the three actions become available for the `QSExternalApp` hosted control.</span></span>  
  
   <span data-ttu-id="74c9d-219">![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")</span><span class="sxs-lookup"><span data-stu-id="74c9d-219">![Available UII actions for a hosted control](../unified-service-desk/media/usd-available-uii-actions-hosted-control.png "Available UII actions for a hosted control")</span></span>  
  
9. <span data-ttu-id="74c9d-220">Làm theo các bước 4 đến 8 để tạo ba hành động [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] với cùng tên cho **QSExternalWebApp**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-220">Follow steps 4 through 8 to create three [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)] actions with the same names for the **QSExternalWebApp**.</span></span>  
  
<a name="test"></a>   
## <a name="test-the-hosted-control"></a><span data-ttu-id="74c9d-221">Kiểm tra kiểm soát tổ chức</span><span class="sxs-lookup"><span data-stu-id="74c9d-221">Test the hosted control</span></span>  
 <span data-ttu-id="74c9d-222">Before you test the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, ensure that your sample web application is running so that it renders within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-222">Before you test the [!INCLUDE[pn_uii_acronym](../includes/pn-uii-acronym.md)][!INCLUDE[pn_wpf_acronym](../includes/pn-wpf-acronym.md)] hosted control, ensure that your sample web application is running so that it renders within [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
1. <span data-ttu-id="74c9d-223">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span><span class="sxs-lookup"><span data-stu-id="74c9d-223">Run [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)] client to connect to your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps server.</span></span>  
  
2. <span data-ttu-id="74c9d-224">Trên lần đăng nhập thành công, bạn sẽ nhìn thấy ba kiểm soát tổ chức: **Kiểm soát Tổ chức WPF UII Mẫu**, **Ứng dụng Web Bên ngoài Mẫu** và **Ứng dụng Bên ngoài Mẫu**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-224">On successful sign in, you’ll see three hosted controls: **Sample UII WPF Hosted Control**, **Sample External Web Application**, and **Sample External Application**.</span></span>  
  
   <span data-ttu-id="74c9d-225">![Sample UII WPF hosted control avaiilable](../unified-service-desk/media/usd-sample-hosted-controls-available-uii-wpf.png "Sample UII WPF hosted control avaiilable")</span><span class="sxs-lookup"><span data-stu-id="74c9d-225">![Sample UII WPF hosted control avaiilable](../unified-service-desk/media/usd-sample-hosted-controls-available-uii-wpf.png "Sample UII WPF hosted control avaiilable")</span></span>  
  
3. <span data-ttu-id="74c9d-226">Choose **Search**, and then choose **Contacts**.</span><span class="sxs-lookup"><span data-stu-id="74c9d-226">Choose **Search**, and then choose **Contacts**.</span></span> <span data-ttu-id="74c9d-227">Choose any of the contacts to display the contact details in a session.</span><span class="sxs-lookup"><span data-stu-id="74c9d-227">Choose any of the contacts to display the contact details in a session.</span></span> <span data-ttu-id="74c9d-228">Điều này cũng hiển thị tên, họ, địa chỉ đường phố và ID của hồ sơ liên hệ hiện được hiển thị trong tất cả ba kiểm soát mẫu:</span><span class="sxs-lookup"><span data-stu-id="74c9d-228">This also displays the first name, last name, street address, and ID of the currently displayed contact record in all the three sample controls:</span></span>  
  
   <span data-ttu-id="74c9d-229">![Data displayed from USD context in the 3 controls](../unified-service-desk/media/usd-sample-controls-uii-wpf.png "Data displayed from USD context in the 3 controls")</span><span class="sxs-lookup"><span data-stu-id="74c9d-229">![Data displayed from USD context in the 3 controls](../unified-service-desk/media/usd-sample-controls-uii-wpf.png "Data displayed from USD context in the 3 controls")</span></span>  
  
4. <span data-ttu-id="74c9d-230">Thay đổi các giá trị trong **Kiểm soát Tổ chức WPF UII Mẫu** và bấm **Cập nhật các giá trị trong ứng dụng được lưu trữ** để cập nhật các giá trị trong hai ứng dụng bên ngoài khác.</span><span class="sxs-lookup"><span data-stu-id="74c9d-230">Change the values in **Sample UII WPF Hosted Control**, and click **Update values in hosted apps** to update the values in the other two external applications.</span></span>  
  
   <span data-ttu-id="74c9d-231">![Updated values in external apps](../unified-service-desk/media/usd-sample-controls-updated-values-uii-wpf.png "Updated values in external apps")</span><span class="sxs-lookup"><span data-stu-id="74c9d-231">![Updated values in external apps](../unified-service-desk/media/usd-sample-controls-updated-values-uii-wpf.png "Updated values in external apps")</span></span>  
  
5. <span data-ttu-id="74c9d-232">Trong **Kiểm soát Tổ chức WPF UII Mẫu**, chọn **Cập nhật ngữ cảnh** để cập nhật thông tin ngữ cảnh trong [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span><span class="sxs-lookup"><span data-stu-id="74c9d-232">In **Sample UII WPF Hosted Control**, choose **Update context** to update the context information in [!INCLUDE[pn_unified_service_desk](../includes/pn-unified-service-desk.md)].</span></span>  
  
   <span data-ttu-id="74c9d-233">![Values updated in USD context](../unified-service-desk/media/usd-uii-wpf-values-updated-context.png "Values updated in USD context")</span><span class="sxs-lookup"><span data-stu-id="74c9d-233">![Values updated in USD context](../unified-service-desk/media/usd-uii-wpf-values-updated-context.png "Values updated in USD context")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="74c9d-234">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="74c9d-234">See also</span></span>  
 <span data-ttu-id="74c9d-235">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span><span class="sxs-lookup"><span data-stu-id="74c9d-235">[Integrate with external applications and web applications](../unified-service-desk/integrate-external-applications-web-applications.md) </span></span>  
 <span data-ttu-id="74c9d-236">[Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span><span class="sxs-lookup"><span data-stu-id="74c9d-236">[Work with UII Hosted Controls](../unified-service-desk/use-uii-hosted-controls-unified-service-desk.md) </span></span>  
 <span data-ttu-id="74c9d-237">[Cách: Tạo một Kiểm soát Tổ chức Biểu mẫu Windows UII](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md) </span><span class="sxs-lookup"><span data-stu-id="74c9d-237">[Walkthrough: Create a UII Windows Forms Hosted Control](../unified-service-desk/walkthrough-create-uii-windows-forms-hosted-control.md) </span></span>  
 [<span data-ttu-id="74c9d-238">Hành động UII</span><span class="sxs-lookup"><span data-stu-id="74c9d-238">UII actions</span></span>](../unified-service-desk/uii-actions.md)
