---
title: Create a custom workflow activity (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: The topic describes how to create a custom workflow activity and register it for use in Dynamics 365 for Customer Engagement (online) Customer Engagement.
ms.custom: ''
ms.date: 09/12/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: ab72830b-e6a6-4f49-a6a8-1d69c4a1d308
caps.latest.revision: 56
author: JimDaly
ms.author: kvivek
manager: kvivek
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 86a04714298e66cbd65e7e7a9e8a9aa41030c6e9
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "386903"
---
# <a name="create-a-custom-workflow-activity"></a><span data-ttu-id="b7ced-103">Create a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="b7ced-103">Create a custom workflow activity</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="b7ced-104">This topic describes how to create a custom workflow activity and register it for use in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="b7ced-104">This topic describes how to create a custom workflow activity and register it for use in [!INCLUDE[pn_dynamics_crm_online](../../includes/pn-dynamics-crm-online.md)] Customer Engagement.</span></span> <span data-ttu-id="b7ced-105">For [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], custom workflow activities can only be registered to execute in the sandbox (partial trust).</span><span class="sxs-lookup"><span data-stu-id="b7ced-105">For [!INCLUDE[pn_CRM_Online](../../includes/pn-crm-online.md)], custom workflow activities can only be registered to execute in the sandbox (partial trust).</span></span> <span data-ttu-id="b7ced-106">For more information about the sandbox and partial trust, see [Plug-in isolation, trusts, and statistics](../plugin-isolation-trusts-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-106">For more information about the sandbox and partial trust, see [Plug-in isolation, trusts, and statistics](../plugin-isolation-trusts-statistics.md).</span></span>  
  
<a name="Requirements"></a>

## <a name="required-software-and-assemblies"></a><span data-ttu-id="b7ced-107">Required software and assemblies</span><span class="sxs-lookup"><span data-stu-id="b7ced-107">Required software and assemblies</span></span>

 <span data-ttu-id="b7ced-108">To develop [!INCLUDE[pn_Windows_Workflow_Foundation](../../includes/pn-windows-workflow-foundation.md)] 4 custom activities for Dynamics 365 for Customer Engagement, you must develop them on [!INCLUDE[pn_NET_Framework_452_long](../../includes/pn-net-framework-452-long.md)].</span><span class="sxs-lookup"><span data-stu-id="b7ced-108">To develop [!INCLUDE[pn_Windows_Workflow_Foundation](../../includes/pn-windows-workflow-foundation.md)] 4 custom activities for Dynamics 365 for Customer Engagement, you must develop them on [!INCLUDE[pn_NET_Framework_452_long](../../includes/pn-net-framework-452-long.md)].</span></span> <span data-ttu-id="b7ced-109">The assembilies are available as Nuget packages and you can download from the NuGet profile [crmsdk](https://www.nuget.org/profiles/crmsdk).</span><span class="sxs-lookup"><span data-stu-id="b7ced-109">The assembilies are available as Nuget packages and you can download from the NuGet profile [crmsdk](https://www.nuget.org/profiles/crmsdk).</span></span>
  
<a name="UseCodeActivity"></a>

## <a name="use-the-codeactivity-workflow-base-class"></a><span data-ttu-id="b7ced-110">Use the CodeActivity workflow base class</span><span class="sxs-lookup"><span data-stu-id="b7ced-110">Use the CodeActivity workflow base class</span></span>

 <span data-ttu-id="b7ced-111">To create a custom workflow activity, create a class that inherits from the <xref:System.Activities.CodeActivity> workflow base class.</span><span class="sxs-lookup"><span data-stu-id="b7ced-111">To create a custom workflow activity, create a class that inherits from the <xref:System.Activities.CodeActivity> workflow base class.</span></span> <span data-ttu-id="b7ced-112">This class is available in the <xref:System.Activities> namespace.</span><span class="sxs-lookup"><span data-stu-id="b7ced-112">This class is available in the <xref:System.Activities> namespace.</span></span> <span data-ttu-id="b7ced-113">Activities that inherit from the `CodeActivity` class can override the `Execute` method to produce custom functionality.</span><span class="sxs-lookup"><span data-stu-id="b7ced-113">Activities that inherit from the `CodeActivity` class can override the `Execute` method to produce custom functionality.</span></span>  
  
1. <span data-ttu-id="b7ced-114">Bắt đầu [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span><span class="sxs-lookup"><span data-stu-id="b7ced-114">Start [!INCLUDE[pn_Visual_Studio](../../includes/pn-visual-studio.md)].</span></span>  
  
2. <span data-ttu-id="b7ced-115">On the **File** menu, click **New**, and then click **Project**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-115">On the **File** menu, click **New**, and then click **Project**.</span></span>  
  
3. <span data-ttu-id="b7ced-116">In the **New Project** dialog box, select **Workflow** under **Visual C#** in the **Installed Templates** pane, and then select **Activity Library**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-116">In the **New Project** dialog box, select **Workflow** under **Visual C#** in the **Installed Templates** pane, and then select **Activity Library**.</span></span>  
  
4. <span data-ttu-id="b7ced-117">Specify a name and location for the solution, and then click **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-117">Specify a name and location for the solution, and then click **OK**.</span></span>  
  
5. <span data-ttu-id="b7ced-118">Navigate to the **Project** menu and select **Properties**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-118">Navigate to the **Project** menu and select **Properties**.</span></span> <span data-ttu-id="b7ced-119">On the **Application** tab, specify **.NET Framework 4.5.2** as the target framework.</span><span class="sxs-lookup"><span data-stu-id="b7ced-119">On the **Application** tab, specify **.NET Framework 4.5.2** as the target framework.</span></span>  
  
6. <span data-ttu-id="b7ced-120">Add references to the `Microsoft.Xrm.Sdk.dll` and `Microsoft.Xrm.Workflow.dll` assemblies.</span><span class="sxs-lookup"><span data-stu-id="b7ced-120">Add references to the `Microsoft.Xrm.Sdk.dll` and `Microsoft.Xrm.Workflow.dll` assemblies.</span></span>  
  
7. <span data-ttu-id="b7ced-121">Delete the Activity1.xaml file in the project.</span><span class="sxs-lookup"><span data-stu-id="b7ced-121">Delete the Activity1.xaml file in the project.</span></span>  
  
8. <span data-ttu-id="b7ced-122">Add a class file (.cs) to the project.</span><span class="sxs-lookup"><span data-stu-id="b7ced-122">Add a class file (.cs) to the project.</span></span> <span data-ttu-id="b7ced-123">In Solution Explorer, right-click the project, select **Add**, and then click **Class**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-123">In Solution Explorer, right-click the project, select **Add**, and then click **Class**.</span></span> <span data-ttu-id="b7ced-124">In the **Add New Item** dialog box, type a name for the class, and then click **Add**.</span><span class="sxs-lookup"><span data-stu-id="b7ced-124">In the **Add New Item** dialog box, type a name for the class, and then click **Add**.</span></span>  
  
9. <span data-ttu-id="b7ced-125">Open the class file, and add the following using directives:</span><span class="sxs-lookup"><span data-stu-id="b7ced-125">Open the class file, and add the following using directives:</span></span>  
  
    ```csharp  
    using System.Activities;
    using Microsoft.Xrm.Sdk;
    using Microsoft.Xrm.Sdk.Workflow;  
    ```  
  
10. <span data-ttu-id="b7ced-126">Make the class inherit from the `CodeActivity` class and give it a public access modifier as shown here:</span><span class="sxs-lookup"><span data-stu-id="b7ced-126">Make the class inherit from the `CodeActivity` class and give it a public access modifier as shown here:</span></span>  
  
    ```csharp  
    public class SampleCustomActivity : CodeActivity  
    ```  
  
11. <span data-ttu-id="b7ced-127">Add functionality to the class by adding an [Execute](https://msdn.microsoft.com/library/system.activities.codeactivity.execute.aspx) method:</span><span class="sxs-lookup"><span data-stu-id="b7ced-127">Add functionality to the class by adding an [Execute](https://msdn.microsoft.com/library/system.activities.codeactivity.execute.aspx) method:</span></span>  
  
    ```csharp  
    protected override void Execute(CodeActivityContext context)
    {
      //Activity code
    }  
    ```  
  
     <span data-ttu-id="b7ced-128">For more information, see [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-128">For more information, see [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md).</span></span>  
  
12. <span data-ttu-id="b7ced-129">Specify input and output parameters.</span><span class="sxs-lookup"><span data-stu-id="b7ced-129">Specify input and output parameters.</span></span> <span data-ttu-id="b7ced-130">For more information, see [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-130">For more information, see [Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md).</span></span>  
  
13. <span data-ttu-id="b7ced-131">In the project properties, under the **Signing** tab, select **Sign the assembly** and provide a key file name.</span><span class="sxs-lookup"><span data-stu-id="b7ced-131">In the project properties, under the **Signing** tab, select **Sign the assembly** and provide a key file name.</span></span> <span data-ttu-id="b7ced-132">Custom workflow activity (and plug-in) assemblies must be signed.</span><span class="sxs-lookup"><span data-stu-id="b7ced-132">Custom workflow activity (and plug-in) assemblies must be signed.</span></span>  
  
14. <span data-ttu-id="b7ced-133">Compile the project to create an assembly (.dll).</span><span class="sxs-lookup"><span data-stu-id="b7ced-133">Compile the project to create an assembly (.dll).</span></span>  
  
    <span data-ttu-id="b7ced-134">To view a code sample that demonstrates how to create a custom workflow activity, see [Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-134">To view a code sample that demonstrates how to create a custom workflow activity, see [Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="b7ced-135">For improved performance, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] caches custom workflow activity instances.</span><span class="sxs-lookup"><span data-stu-id="b7ced-135">For improved performance, [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] caches custom workflow activity instances.</span></span> <span data-ttu-id="b7ced-136">The custom workflow activity’s [Execute](https://msdn.microsoft.com/library/system.activities.codeactivity.execute.aspx) method should be written to be stateless because the constructor is not called for every invocation of the custom workflow activity.</span><span class="sxs-lookup"><span data-stu-id="b7ced-136">The custom workflow activity’s [Execute](https://msdn.microsoft.com/library/system.activities.codeactivity.execute.aspx) method should be written to be stateless because the constructor is not called for every invocation of the custom workflow activity.</span></span> <span data-ttu-id="b7ced-137">Also, multiple system threads could execute the custom workflow activity at the same time.</span><span class="sxs-lookup"><span data-stu-id="b7ced-137">Also, multiple system threads could execute the custom workflow activity at the same time.</span></span> <span data-ttu-id="b7ced-138">All per invocation state information is stored in the context, so it is not recommended to use global variables or member variables to pass data from one invocation to the next.</span><span class="sxs-lookup"><span data-stu-id="b7ced-138">All per invocation state information is stored in the context, so it is not recommended to use global variables or member variables to pass data from one invocation to the next.</span></span>  
  
<a name="NameandGroupName"></a>

## <a name="specify-the-name-and-group-name-for-a-custom-workflow-activity"></a><span data-ttu-id="b7ced-139">Specify the name and group name for a custom workflow activity</span><span class="sxs-lookup"><span data-stu-id="b7ced-139">Specify the name and group name for a custom workflow activity</span></span>

 <span data-ttu-id="b7ced-140">When you register a custom workflow activity assembly, specify the name and group name.</span><span class="sxs-lookup"><span data-stu-id="b7ced-140">When you register a custom workflow activity assembly, specify the name and group name.</span></span> <span data-ttu-id="b7ced-141">The name property specifies the name of the workflow activity.</span><span class="sxs-lookup"><span data-stu-id="b7ced-141">The name property specifies the name of the workflow activity.</span></span> <span data-ttu-id="b7ced-142">The group name property specifies the name of the submenu added to the main menu in the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer.</span><span class="sxs-lookup"><span data-stu-id="b7ced-142">The group name property specifies the name of the submenu added to the main menu in the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer.</span></span> <span data-ttu-id="b7ced-143">These properties link the custom workflow activity with the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer, so that the custom activity name will appear in the user interface.</span><span class="sxs-lookup"><span data-stu-id="b7ced-143">These properties link the custom workflow activity with the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer, so that the custom activity name will appear in the user interface.</span></span>  
  
 <span data-ttu-id="b7ced-144">To specify the name and group name for a custom workflow activity, use the `PluginType.Name` and `PluginType.WorkflowActivityGroupName` attributes when you register the custom workflow activity assembly.</span><span class="sxs-lookup"><span data-stu-id="b7ced-144">To specify the name and group name for a custom workflow activity, use the `PluginType.Name` and `PluginType.WorkflowActivityGroupName` attributes when you register the custom workflow activity assembly.</span></span> <span data-ttu-id="b7ced-145">For more information about registering custom workflow activities, see [Registering the Workflow Assembly](register-use-custom-workflow-activity-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-145">For more information about registering custom workflow activities, see [Registering the Workflow Assembly](register-use-custom-workflow-activity-assembly.md).</span></span> <span data-ttu-id="b7ced-146">If the `PluginType.Name` and `PluginType.WorkflowActivityGroupName` attributes are set to **null**, the custom activity is hidden from the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] workflow designer and is only accessible from XAML workflows.</span><span class="sxs-lookup"><span data-stu-id="b7ced-146">If the `PluginType.Name` and `PluginType.WorkflowActivityGroupName` attributes are set to **null**, the custom activity is hidden from the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] workflow designer and is only accessible from XAML workflows.</span></span>  
  
 <span data-ttu-id="b7ced-147">If you are using the Plug-in Registration tool to register the custom workflow activity assembly, you can specify appropriate values in the **Name** and **WorkflowActivityGroupName** boxes, under the **Editable** region.</span><span class="sxs-lookup"><span data-stu-id="b7ced-147">If you are using the Plug-in Registration tool to register the custom workflow activity assembly, you can specify appropriate values in the **Name** and **WorkflowActivityGroupName** boxes, under the **Editable** region.</span></span> <span data-ttu-id="b7ced-148">For more information about using the Plug-in Registration tool, see [Walkthrough: Register a plug-in using the plug-in registration tool](../walkthrough-register-plugin-using-plugin-registration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-148">For more information about using the Plug-in Registration tool, see [Walkthrough: Register a plug-in using the plug-in registration tool](../walkthrough-register-plugin-using-plugin-registration-tool.md).</span></span>  
  
 <span data-ttu-id="b7ced-149">![Specify the Group Name and Name while registering](../media/process-name-workflow-activity.png "Specify the Group Name and Name while registering")</span><span class="sxs-lookup"><span data-stu-id="b7ced-149">![Specify the Group Name and Name while registering](../media/process-name-workflow-activity.png "Specify the Group Name and Name while registering")</span></span>  
  
 <span data-ttu-id="b7ced-150">After this custom workflow activity is registered, you can use it from the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer for workflows or dialogs.</span><span class="sxs-lookup"><span data-stu-id="b7ced-150">After this custom workflow activity is registered, you can use it from the [!INCLUDE[pn_dynamics_crm](../../includes/pn-dynamics-crm.md)] process designer for workflows or dialogs.</span></span> <span data-ttu-id="b7ced-151">For more information, see [Register and Use a Custom Workflow Activity Assembly](register-use-custom-workflow-activity-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="b7ced-151">For more information, see [Register and Use a Custom Workflow Activity Assembly](register-use-custom-workflow-activity-assembly.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b7ced-152">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="b7ced-152">See also</span></span>

 <span data-ttu-id="b7ced-153">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span><span class="sxs-lookup"><span data-stu-id="b7ced-153">[Custom workflow activities (workflow assemblies)](../custom-workflow-activities-workflow-assemblies.md) </span></span>  
 <span data-ttu-id="b7ced-154">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b7ced-154">[Adding Metadata to the Custom Workflow Activity](add-metadata-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="b7ced-155">[Using the IOrganization Web Service within a Custom Workflow Activity](use-iorganization-web-service-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b7ced-155">[Using the IOrganization Web Service within a Custom Workflow Activity](use-iorganization-web-service-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="b7ced-156">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b7ced-156">[Sample: Create a Custom Workflow Activity](sample-create-custom-workflow-activity.md) </span></span>  
 <span data-ttu-id="b7ced-157">[Sample: Azure aware custom workflow activity](../sample-azure-aware-custom-workflow-activity.md) </span><span class="sxs-lookup"><span data-stu-id="b7ced-157">[Sample: Azure aware custom workflow activity](../sample-azure-aware-custom-workflow-activity.md) </span></span>  
 [<span data-ttu-id="b7ced-158">Windows Workflow Foundation 4 Base Activity Classes</span><span class="sxs-lookup"><span data-stu-id="b7ced-158">Windows Workflow Foundation 4 Base Activity Classes</span></span>](https://msdn.microsoft.com/library/ee264170.aspx)
