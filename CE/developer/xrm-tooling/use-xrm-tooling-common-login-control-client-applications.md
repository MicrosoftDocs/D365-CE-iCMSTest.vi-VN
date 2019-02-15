---
title: Use the XRM tooling common login control in your client applications (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The Dynamics 365 for Customer Engagement apps SDK provides you with a template for Visual Studio that enables you to use the common login control in your client applications. The code for Dynamics 365 for Customer Engagement authentication, credential storage and retrieval, and diagnostic logging is built into the template so that you can quickly leverage these capabilities in your Windows client applications for Dynamics 365 for Customer Engagement
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: f77b2a20-0a30-4211-a1d9-74923d3eeae1
caps.latest.revision: 27
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: b876c3c7436d83913ff236d3a50e18e251b9a954
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386628"
---
# <a name="use-the-xrm-tooling-common-login-control-in-your-client-applications"></a><span data-ttu-id="4ecd7-104">Use the XRM tooling common login control in your client applications</span><span class="sxs-lookup"><span data-stu-id="4ecd7-104">Use the XRM tooling common login control in your client applications</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="4ecd7-105">There is a template for [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that enables you to use the common login control in your client applications.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-105">There is a template for [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] that enables you to use the common login control in your client applications.</span></span> <span data-ttu-id="4ecd7-106">The code for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] authentication, credential storage and retrieval, and diagnostic logging is built into the template so that you can quickly leverage these capabilities in your Windows client applications for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="4ecd7-106">The code for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] authentication, credential storage and retrieval, and diagnostic logging is built into the template so that you can quickly leverage these capabilities in your Windows client applications for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span> <span data-ttu-id="4ecd7-107">The common login control is an implementation of the <xref:Microsoft.Xrm.Tooling.CrmConnectControl>, and the control resembles the following image.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-107">The common login control is an implementation of the <xref:Microsoft.Xrm.Tooling.CrmConnectControl>, and the control resembles the following image.</span></span>  
  
 <span data-ttu-id="4ecd7-108">![XRM Tooling common login control](../media/crm-sdk-v6-commonlogincontrol.png "XRM Tooling common login control")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-108">![XRM Tooling common login control](../media/crm-sdk-v6-commonlogincontrol.png "XRM Tooling common login control")</span></span>  
  
<a name="Prereq"></a>

## <a name="prerequisites"></a><span data-ttu-id="4ecd7-109">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="4ecd7-109">Prerequisites</span></span>
  
- [!INCLUDE[pn_NET_Framework_452_short](../../includes/pn-net-framework-452-short.md)]  
  
- [!INCLUDE[pn_microsoft_visual_studio_2012](../../includes/pn-microsoft-visual-studio-2012.md)]<span data-ttu-id="4ecd7-110">, [!INCLUDE[pn_visual_studio_2013](../../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] 2015</span><span class="sxs-lookup"><span data-stu-id="4ecd7-110">, [!INCLUDE[pn_visual_studio_2013](../../includes/pn-visual-studio-2013.md)], or [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] 2015</span></span>  
  
- <span data-ttu-id="4ecd7-111">Nuget Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span><span class="sxs-lookup"><span data-stu-id="4ecd7-111">Nuget Package Manager for [Visual Studio 2012](http://visualstudiogallery.msdn.microsoft.com/27077b70-9dad-4c64-adcf-c7cf6bc9970c), [Visual Studio 2013](http://visualstudiogallery.msdn.microsoft.com/4ec1526c-4a8c-4a84-b702-b21a8f5293ca), or [Visual Studio 2015](https://visualstudiogallery.msdn.microsoft.com/5d345edc-2e2d-4a9c-b73b-d53956dc458d)</span></span>  
  
- <span data-ttu-id="4ecd7-112">Connected to Internet so that you can download/restore the required Nuget packages while using the project template.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-112">Connected to Internet so that you can download/restore the required Nuget packages while using the project template.</span></span>  
  
- <span data-ttu-id="4ecd7-113">CRM SDK template templates for [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] that contains the common login control template.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-113">CRM SDK template templates for [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] that contains the common login control template.</span></span> <span data-ttu-id="4ecd7-114">You can get it by downloading the [Microsoft Dynamics CRM SDK Templates](http://go.microsoft.com/fwlink/p/?LinkId=400925) from [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] gallery, and double-click the `CRMSDKTemplates.vsix` file to install the template in [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="4ecd7-114">You can get it by downloading the [Microsoft Dynamics CRM SDK Templates](http://go.microsoft.com/fwlink/p/?LinkId=400925) from [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)] gallery, and double-click the `CRMSDKTemplates.vsix` file to install the template in [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span></span>  
  
  
<a name="NewProjectUsingTemplate"></a>
   
## <a name="create-a-wpf-application-using-the-common-login-control-template"></a><span data-ttu-id="4ecd7-115">Create a WPF application using the common login control template</span><span class="sxs-lookup"><span data-stu-id="4ecd7-115">Create a WPF application using the common login control template</span></span>
  
 <span data-ttu-id="4ecd7-116">Here is a quick way to create a [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../../includes/pn-ms-windows-presentation-foundation.md)] application that leverages the common login control and the underlying code for authentication, credential storage and reuse, and default tracing or logging.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-116">Here is a quick way to create a [!INCLUDE[pn_ms_Windows_Presentation_Foundation](../../includes/pn-ms-windows-presentation-foundation.md)] application that leverages the common login control and the underlying code for authentication, credential storage and reuse, and default tracing or logging.</span></span>  
  
1. <span data-ttu-id="4ecd7-117">Bắt đầu [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)] và tạo một dự án mới.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-117">Start [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)], and create a new project.</span></span>  
  
2. <span data-ttu-id="4ecd7-118">In the **New Project** dialog box:</span><span class="sxs-lookup"><span data-stu-id="4ecd7-118">In the **New Project** dialog box:</span></span>  
  
   1. <span data-ttu-id="4ecd7-119">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-119">From the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span></span>  
  
   2. <span data-ttu-id="4ecd7-120">Ensure that **[!INCLUDE[pn_NET_Framework_452_short](../../includes/pn-net-framework-452-short.md)]** is selected.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-120">Ensure that **[!INCLUDE[pn_NET_Framework_452_short](../../includes/pn-net-framework-452-short.md)]** is selected.</span></span>  
  
   3. <span data-ttu-id="4ecd7-121">Select **WPF Application for Dynamics 365 for Customer Engagement apps**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-121">Select **WPF Application for Dynamics 365 for Customer Engagement apps**.</span></span>  
  
   4. <span data-ttu-id="4ecd7-122">Specify the name and location of the project, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-122">Specify the name and location of the project, and click **OK**.</span></span>  
  
   <span data-ttu-id="4ecd7-123">![WPF Application for Dynamics 365 for Customer Engagement template](../media/crm-sdk-v6-xrmtooling-newproject.png "WPF Application for Dynamics 365 for Customer Engagement template")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-123">![WPF Application for Dynamics 365 for Customer Engagement template](../media/crm-sdk-v6-xrmtooling-newproject.png "WPF Application for Dynamics 365 for Customer Engagement template")</span></span>  
  
3. <span data-ttu-id="4ecd7-124">To test the project:</span><span class="sxs-lookup"><span data-stu-id="4ecd7-124">To test the project:</span></span>  
  
   1. <span data-ttu-id="4ecd7-125">Save the project and press F5 or click **Debug** > **Start Debugging** to verify if the project compiles successfully.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-125">Save the project and press F5 or click **Debug** > **Start Debugging** to verify if the project compiles successfully.</span></span> <span data-ttu-id="4ecd7-126">On successful compilation, you’ll see a MainWindow with **Login to Dynamics 365 for Customer Engagement apps** button.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-126">On successful compilation, you’ll see a MainWindow with **Login to Dynamics 365 for Customer Engagement apps** button.</span></span> <span data-ttu-id="4ecd7-127">Click the button to display the common login control.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-127">Click the button to display the common login control.</span></span>  
  
   2. <span data-ttu-id="4ecd7-128">Test the authentication by providing your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and then click **Login**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-128">Test the authentication by providing your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and then click **Login**.</span></span> <span data-ttu-id="4ecd7-129">A message displays your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection status.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-129">A message displays your [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection status.</span></span>  
  
   <span data-ttu-id="4ecd7-130">For a sample that uses the common login control template to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] and perform various operations, see [Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md).</span><span class="sxs-lookup"><span data-stu-id="4ecd7-130">For a sample that uses the common login control template to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] and perform various operations, see [Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md).</span></span>  
  
<a name="Add"></a>

## <a name="add-the-common-login-control-template-to-your-existing-wpf-application"></a><span data-ttu-id="4ecd7-131">Add the common login control template to your existing WPF application</span><span class="sxs-lookup"><span data-stu-id="4ecd7-131">Add the common login control template to your existing WPF application</span></span>

 <span data-ttu-id="4ecd7-132">If you already have a WPF client application, you can easily add the common login control template to it to leverage the uniform sign-in experience and the underlying code for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] authentication, credential storage and reuse, and default tracing or logging.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-132">If you already have a WPF client application, you can easily add the common login control template to it to leverage the uniform sign-in experience and the underlying code for [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] authentication, credential storage and reuse, and default tracing or logging.</span></span> <span data-ttu-id="4ecd7-133">In this case, you must create a control in the user interface of your existing client application to call the common login control, instantiate an instance of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection object, and then use the connection object to perform various operations in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span><span class="sxs-lookup"><span data-stu-id="4ecd7-133">In this case, you must create a control in the user interface of your existing client application to call the common login control, instantiate an instance of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection object, and then use the connection object to perform various operations in [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)].</span></span>  
  
1. <span data-ttu-id="4ecd7-134">Open an existing WPF application project in [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span><span class="sxs-lookup"><span data-stu-id="4ecd7-134">Open an existing WPF application project in [!INCLUDE[pn_Visual_Studio_short](../../includes/pn-visual-studio-short.md)].</span></span> <span data-ttu-id="4ecd7-135">For this example, let’s assume that the name of your WPF application project is SampleWPFApp.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-135">For this example, let’s assume that the name of your WPF application project is SampleWPFApp.</span></span>  
  
2. <span data-ttu-id="4ecd7-136">Add the common login control template to your project.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-136">Add the common login control template to your project.</span></span>  
  
   1.  <span data-ttu-id="4ecd7-137">In the **Solution Explorer** pane, right-click the project name, and click **Add** > **New Item**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-137">In the **Solution Explorer** pane, right-click the project name, and click **Add** > **New Item**.</span></span>  
  
<span data-ttu-id="4ecd7-138"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="4ecd7-138"><<<<<<< HEAD</span></span>
   2.  <span data-ttu-id="4ecd7-139">In the **Add New Item** dialog box, from the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-139">In the **Add New Item** dialog box, from the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span></span> <span data-ttu-id="4ecd7-140">Click **Dynamics 365 for Customer Engagement apps Login Form for WPF Applications**, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-140">Click **Dynamics 365 for Customer Engagement apps Login Form for WPF Applications**, and click **OK**.</span></span>  
=======
   2.  <span data-ttu-id="4ecd7-141">In the **Add New Item** dialog box, from the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-141">In the **Add New Item** dialog box, from the list of installed templates, expand **Visual C#**, and select **Dynamics 365 for Customer Engagement apps SDK Templates**.</span></span> <span data-ttu-id="4ecd7-142">Click **Dynamics 365 for Customer Engagement Login Form for WPF Applications**, and click **OK**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-142">Click **Dynamics 365 for Customer Engagement Login Form for WPF Applications**, and click **OK**.</span></span>  
>>>>>>> <span data-ttu-id="4ecd7-143">58afe5531139485f76d29dc85b1ea680128b55c8</span><span class="sxs-lookup"><span data-stu-id="4ecd7-143">58afe5531139485f76d29dc85b1ea680128b55c8</span></span>
  
   <span data-ttu-id="4ecd7-144">![Add the common login control template](../media/crm-sdk-v6-xrmtooling-addtemplate01.png "Add the common login control template")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-144">![Add the common login control template](../media/crm-sdk-v6-xrmtooling-addtemplate01.png "Add the common login control template")</span></span>  
  
3. <span data-ttu-id="4ecd7-145">The newly added `CrmLoginForm1.xaml` login control is displayed in the XAML designer area.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-145">The newly added `CrmLoginForm1.xaml` login control is displayed in the XAML designer area.</span></span> <span data-ttu-id="4ecd7-146">If it isn’t displayed, double-click the `CrmLoginForm1.xaml` file in the **Solution Explorer** pane.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-146">If it isn’t displayed, double-click the `CrmLoginForm1.xaml` file in the **Solution Explorer** pane.</span></span>  
  
   <span data-ttu-id="4ecd7-147">![Verify that the login control renders properly](../media/crm-sdk-v6-xrmtooling-addtemplate03.png "Verify that the login control renders properly")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-147">![Verify that the login control renders properly](../media/crm-sdk-v6-xrmtooling-addtemplate03.png "Verify that the login control renders properly")</span></span>  
  
4. <span data-ttu-id="4ecd7-148">You must now call the newly added login control from your application.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-148">You must now call the newly added login control from your application.</span></span> <span data-ttu-id="4ecd7-149">To do this, add a **Button** control on your MainWindow.xaml file, and set the name and content to **btnSignIn** and **Sign in to Dynamics 365 for Customer Engagement apps** respectively.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-149">To do this, add a **Button** control on your MainWindow.xaml file, and set the name and content to **btnSignIn** and **Sign in to Dynamics 365 for Customer Engagement apps** respectively.</span></span>  
  
   <span data-ttu-id="4ecd7-150">![Add a control to call the login form](../media/crm-sdk-v6-xrmtooling-addtemplate02.png "Add a control to call the login form")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-150">![Add a control to call the login form](../media/crm-sdk-v6-xrmtooling-addtemplate02.png "Add a control to call the login form")</span></span>  
  
5. <span data-ttu-id="4ecd7-151">Double-click the button to add code for the click event of the **btnSignIn** button in the MainWindow.xaml.cs file.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-151">Double-click the button to add code for the click event of the **btnSignIn** button in the MainWindow.xaml.cs file.</span></span>  
  
6. <span data-ttu-id="4ecd7-152">Add the following sample code in the click event of the **btnSignIn** button to call the CrmLoginForm1 control, and create an instance of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection object.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-152">Add the following sample code in the click event of the **btnSignIn** button to call the CrmLoginForm1 control, and create an instance of the [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)] connection object.</span></span>  
  
   ```csharp
   // Establish the Login control.  
   CRMLoginForm1 ctrl = new CRMLoginForm1();  
  
   // Wire event to login response.   
   ctrl.ConnectionToCrmCompleted += ctrl_ConnectionToCrmCompleted;  
  
   // Show the login control.   
   ctrl.ShowDialog();  
  
   // Handle the returned CRM connection object.  
   // On successful connection, display the CRM version and connected org name   
   if (ctrl.CrmConnectionMgr != null && ctrl.CrmConnectionMgr.CrmSvc != null && ctrl.CrmConnectionMgr.CrmSvc.IsReady)  
   {  
       MessageBox.Show("Connected to CRM! Version: " + ctrl.CrmConnectionMgr.CrmSvc.ConnectedOrgVersion.ToString() +   
       " Org: " + ctrl.CrmConnectionMgr.CrmSvc.ConnectedOrgUniqueName, "Connection Status");  
  
       // Perform your actions here  
   }  
   else  
   {  
       MessageBox.Show("Cannot connect; try again!", "Connection Status");  
   }  
   ```  
  
7. <span data-ttu-id="4ecd7-153">Add the definition of the `ctrl_ConnectionToCrmCompleted` event below the click event of the button:</span><span class="sxs-lookup"><span data-stu-id="4ecd7-153">Add the definition of the `ctrl_ConnectionToCrmCompleted` event below the click event of the button:</span></span>  
  
   ```csharp  
   private void ctrl_ConnectionToCrmCompleted(object sender, EventArgs e)  
   {  
       if (sender is CRMLoginForm1)  
       {  
           this.Dispatcher.Invoke(() =>  
           {  
               ((CRMLoginForm1)sender).Close();  
           });  
       }  
   }  
   ```  
  
8. <span data-ttu-id="4ecd7-154">This is how your MainWindow.xaml.cs file appears after adding code from the previous two steps:</span><span class="sxs-lookup"><span data-stu-id="4ecd7-154">This is how your MainWindow.xaml.cs file appears after adding code from the previous two steps:</span></span>  
  
   <span data-ttu-id="4ecd7-155">![Sample code](../media/crm-sdk-v6-xrmtooling-addtemplate04.png "Sample code")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-155">![Sample code](../media/crm-sdk-v6-xrmtooling-addtemplate04.png "Sample code")</span></span>  
  
9. <span data-ttu-id="4ecd7-156">To test the project:</span><span class="sxs-lookup"><span data-stu-id="4ecd7-156">To test the project:</span></span>  
  
   1. <span data-ttu-id="4ecd7-157">Save the project and press F5 or click **Debug** > **Start Debugging** to verify if the project compiles successfully.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-157">Save the project and press F5 or click **Debug** > **Start Debugging** to verify if the project compiles successfully.</span></span> <span data-ttu-id="4ecd7-158">On successful compilation, you will see a MainWindow with the new **Sign In to Dynamics 365 for Customer Engagement apps** button.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-158">On successful compilation, you will see a MainWindow with the new **Sign In to Dynamics 365 for Customer Engagement apps** button.</span></span> <span data-ttu-id="4ecd7-159">Click it to display the common login control.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-159">Click it to display the common login control.</span></span>  
  
   2. <span data-ttu-id="4ecd7-160">Test the authentication by providing your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and then click **Login**.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-160">Test the authentication by providing your credentials to connect to [!INCLUDE[pn_crm_shortest](../../includes/pn-crm-shortest.md)], and then click **Login**.</span></span> <span data-ttu-id="4ecd7-161">If successful, a message appears stating the version and the organization name that you are connected to.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-161">If successful, a message appears stating the version and the organization name that you are connected to.</span></span> <span data-ttu-id="4ecd7-162">Click **OK** to close the message.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-162">Click **OK** to close the message.</span></span>  
  
   <span data-ttu-id="4ecd7-163">![Project test results](../media/crm-sdk-v6-xrmtooling-addtemplate05.png "Project test results")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-163">![Project test results](../media/crm-sdk-v6-xrmtooling-addtemplate05.png "Project test results")</span></span>  
  
    3.  <span data-ttu-id="4ecd7-164">If you click **Sign In to Dynamics 365 for Customer Engagement apps** again, the application prompts you to either choose the saved credentials from the last sign-in activity, or to re-enter the new credentials.</span><span class="sxs-lookup"><span data-stu-id="4ecd7-164">If you click **Sign In to Dynamics 365 for Customer Engagement apps** again, the application prompts you to either choose the saved credentials from the last sign-in activity, or to re-enter the new credentials.</span></span>  
  
   <span data-ttu-id="4ecd7-165">![Stored credentials](../media/crm-sdk-v6-xrmtooling-addtemplate06.png "Stored credentials")</span><span class="sxs-lookup"><span data-stu-id="4ecd7-165">![Stored credentials](../media/crm-sdk-v6-xrmtooling-addtemplate06.png "Stored credentials")</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4ecd7-166">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="4ecd7-166">See also</span></span>  
 <span data-ttu-id="4ecd7-167">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span><span class="sxs-lookup"><span data-stu-id="4ecd7-167">[Sample: Quick start for XRM Tooling API](sample-quick-start-xrm-tooling-api.md) </span></span>  
 [<span data-ttu-id="4ecd7-168">Build windows client applications using the XRM tools</span><span class="sxs-lookup"><span data-stu-id="4ecd7-168">Build windows client applications using the XRM tools</span></span>](../build-windows-client-applications-xrm-tools.md)
