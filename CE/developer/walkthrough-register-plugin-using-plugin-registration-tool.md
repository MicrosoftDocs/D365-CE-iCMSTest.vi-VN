---
title: 'Walkthrough: Register a plug-in using the plug-in registration tool (Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs'
description: This article tells how to register a plug-in by using the Plug-in Registration tool that is provided in the SDK.
ms.custom: ''
ms.date: 05/01/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: c0adf742-e0b7-4699-8972-afe0638af4e4
caps.latest.revision: 48
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 2771fe323ebc1192c21f3cf37847e2893a91aa34
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387166"
---
# <a name="walkthrough-register-a-plug-in-using-the-plug-in-registration-tool"></a><span data-ttu-id="55384-103">Walkthrough: Register a plug-in using the plug-in registration tool</span><span class="sxs-lookup"><span data-stu-id="55384-103">Walkthrough: Register a plug-in using the plug-in registration tool</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="55384-104">This walkthrough demonstrates how to register a plug-in by using the Plug-in Registration tool that is provided in the SDK.</span><span class="sxs-lookup"><span data-stu-id="55384-104">This walkthrough demonstrates how to register a plug-in by using the Plug-in Registration tool that is provided in the SDK.</span></span> <span data-ttu-id="55384-105">The plug-in to register is the FollowupPlugin from the [Sample: Basic Plug-in](sample-create-basic-plugin.md) topic.</span><span class="sxs-lookup"><span data-stu-id="55384-105">The plug-in to register is the FollowupPlugin from the [Sample: Basic Plug-in](sample-create-basic-plugin.md) topic.</span></span>  

 <span data-ttu-id="55384-106">The plug-in is to be registered on the `account` entity, <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message, on a post-event, and in the sandbox.</span><span class="sxs-lookup"><span data-stu-id="55384-106">The plug-in is to be registered on the `account` entity, <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message, on a post-event, and in the sandbox.</span></span> <span data-ttu-id="55384-107">The plug-in can be registered on any [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement deployment where your user account has the System Customizer or System Administrator role.</span><span class="sxs-lookup"><span data-stu-id="55384-107">The plug-in can be registered on any [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement deployment where your user account has the System Customizer or System Administrator role.</span></span>  

 <span data-ttu-id="55384-108">The following prerequisites must be completed before starting this walkthrough:</span><span class="sxs-lookup"><span data-stu-id="55384-108">The following prerequisites must be completed before starting this walkthrough:</span></span>  

- <span data-ttu-id="55384-109">Get the PluginRegistration.exe tool.</span><span class="sxs-lookup"><span data-stu-id="55384-109">Get the PluginRegistration.exe tool.</span></span> [!INCLUDE[proc-download-plugin-registration-tool](../includes/proc-download-plugin-registration-tool.md)] 

- <span data-ttu-id="55384-110">Obtain a system user account on a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span><span class="sxs-lookup"><span data-stu-id="55384-110">Obtain a system user account on a [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server.</span></span>  

- <span data-ttu-id="55384-111">Your user account must have the System Customizer or System Administrator role.</span><span class="sxs-lookup"><span data-stu-id="55384-111">Your user account must have the System Customizer or System Administrator role.</span></span> <span data-ttu-id="55384-112">See [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement](security-dev/how-role-based-security-control-access-entities.md).</span><span class="sxs-lookup"><span data-stu-id="55384-112">See [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement](security-dev/how-role-based-security-control-access-entities.md).</span></span>  

[!INCLUDE [cc_register-plug-in-premium-entities-note](../includes/cc_register-plug-in-premium-entities-note.md)]

### <a name="connect-to-the-includepndynamicscrmincludespn-dynamics-crmmd-server"></a><span data-ttu-id="55384-113">Connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Server</span><span class="sxs-lookup"><span data-stu-id="55384-113">Connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] Server</span></span>  

1. <span data-ttu-id="55384-114">Run the Plug-in Registration tool.</span><span class="sxs-lookup"><span data-stu-id="55384-114">Run the Plug-in Registration tool.</span></span>  

2. <span data-ttu-id="55384-115">Click **CREATE NEW CONNECTION**.</span><span class="sxs-lookup"><span data-stu-id="55384-115">Click **CREATE NEW CONNECTION**.</span></span>  

3. <span data-ttu-id="55384-116">In the **Login** dialog, select the deployment type radio button corresponding to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server you intend to register plug-ins with.</span><span class="sxs-lookup"><span data-stu-id="55384-116">In the **Login** dialog, select the deployment type radio button corresponding to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server you intend to register plug-ins with.</span></span> <span data-ttu-id="55384-117">The **On-premises** radio button includes an IFD deployment, the **Online** button is for the [!INCLUDE[pn_Windows_Live](../includes/pn-windows-live.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)], and the **Office 365** button is for the [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="55384-117">The **On-premises** radio button includes an IFD deployment, the **Online** button is for the [!INCLUDE[pn_Windows_Live](../includes/pn-windows-live.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)], and the **Office 365** button is for the [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span>  


   |                                                                                                                                                                |                                                                                                                                                                                   |
   |----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <span data-ttu-id="55384-118">![Login dialog for an online deployment](media/crm-v6s-pr-login-online.PNG "Login dialog for an online deployment")</span><span class="sxs-lookup"><span data-stu-id="55384-118">![Login dialog for an online deployment](media/crm-v6s-pr-login-online.PNG "Login dialog for an online deployment")</span></span><br /><span data-ttu-id="55384-119">Login window for an online deployment</span><span class="sxs-lookup"><span data-stu-id="55384-119">Login window for an online deployment</span></span> | <span data-ttu-id="55384-120">![Login window for an on-premises deployment](media/crm-v6s-pr-login-onprem.png "Login window for an on-premises deployment")</span><span class="sxs-lookup"><span data-stu-id="55384-120">![Login window for an on-premises deployment](media/crm-v6s-pr-login-onprem.png "Login window for an on-premises deployment")</span></span><br /><span data-ttu-id="55384-121">Login window for an on-premises deployment</span><span class="sxs-lookup"><span data-stu-id="55384-121">Login window for an on-premises deployment</span></span> |


4. <span data-ttu-id="55384-122">If you check **Always display list of available orgs**, you are presented with a list of organizations that you belong to after you click **Login**.</span><span class="sxs-lookup"><span data-stu-id="55384-122">If you check **Always display list of available orgs**, you are presented with a list of organizations that you belong to after you click **Login**.</span></span> <span data-ttu-id="55384-123">This enables you to choose the organization that you want to register the plug-in with.</span><span class="sxs-lookup"><span data-stu-id="55384-123">This enables you to choose the organization that you want to register the plug-in with.</span></span> <span data-ttu-id="55384-124">Otherwise, your default organization is used.</span><span class="sxs-lookup"><span data-stu-id="55384-124">Otherwise, your default organization is used.</span></span>  

5. <span data-ttu-id="55384-125">Enter the indicated information about the server and login account, and then click **Login**.</span><span class="sxs-lookup"><span data-stu-id="55384-125">Enter the indicated information about the server and login account, and then click **Login**.</span></span>  

   <span data-ttu-id="55384-126">You should see a collapsed list of registered plug-in or custom workflow activity assemblies and service endpoints.</span><span class="sxs-lookup"><span data-stu-id="55384-126">You should see a collapsed list of registered plug-in or custom workflow activity assemblies and service endpoints.</span></span> <span data-ttu-id="55384-127">The activity feeds and Microsoft.Crm.ObjectModel assemblies are required for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to function properly so the tool prevents you from altering them.</span><span class="sxs-lookup"><span data-stu-id="55384-127">The activity feeds and Microsoft.Crm.ObjectModel assemblies are required for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to function properly so the tool prevents you from altering them.</span></span> <span data-ttu-id="55384-128">Selecting an item in the list results in the **Properties** and **Details** tab panes displaying information about that list item.</span><span class="sxs-lookup"><span data-stu-id="55384-128">Selecting an item in the list results in the **Properties** and **Details** tab panes displaying information about that list item.</span></span>  

   <span data-ttu-id="55384-129">![The application's main window](media/crm-v6s-pr-main-window.PNG "The application's main window")</span><span class="sxs-lookup"><span data-stu-id="55384-129">![The application's main window](media/crm-v6s-pr-main-window.PNG "The application's main window")</span></span>  
   <span data-ttu-id="55384-130">The application’s main window</span><span class="sxs-lookup"><span data-stu-id="55384-130">The application’s main window</span></span>  

### <a name="register-a-plug-in-assembly"></a><span data-ttu-id="55384-131">Register a plug-in assembly</span><span class="sxs-lookup"><span data-stu-id="55384-131">Register a plug-in assembly</span></span>  

1. <span data-ttu-id="55384-132">Select an organization tab to make it active.</span><span class="sxs-lookup"><span data-stu-id="55384-132">Select an organization tab to make it active.</span></span>  

2. <span data-ttu-id="55384-133">In the toolbar of the tab, click **Register** and then **Register New Assembly**.</span><span class="sxs-lookup"><span data-stu-id="55384-133">In the toolbar of the tab, click **Register** and then **Register New Assembly**.</span></span>  

3. <span data-ttu-id="55384-134">In the **Register New Assembly** dialog box, click the ellipses [**…**] button to the right of the **Step#1** field.</span><span class="sxs-lookup"><span data-stu-id="55384-134">In the **Register New Assembly** dialog box, click the ellipses [**…**] button to the right of the **Step#1** field.</span></span>  

4. <span data-ttu-id="55384-135">In the **Open** dialog box, navigate to the location of the compiled SamplePlugin.dll assembly.</span><span class="sxs-lookup"><span data-stu-id="55384-135">In the **Open** dialog box, navigate to the location of the compiled SamplePlugin.dll assembly.</span></span> <span data-ttu-id="55384-136">You will find this assembly in the [Sample directory]/bin/Debug folder once you have run the sample [Work with Plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade). Select the assembly, and then click **Open**.</span><span class="sxs-lookup"><span data-stu-id="55384-136">You will find this assembly in the [Sample directory]/bin/Debug folder once you have run the sample [Work with Plug-ins](https://code.msdn.microsoft.com/Sample-Create-a-basic-plug-64d86ade). Select the assembly, and then click **Open**.</span></span>  

5. <span data-ttu-id="55384-137">In the **Step#2** section, expand the **SamplePlugins** assembly to view all plug-ins in that assembly.</span><span class="sxs-lookup"><span data-stu-id="55384-137">In the **Step#2** section, expand the **SamplePlugins** assembly to view all plug-ins in that assembly.</span></span> <span data-ttu-id="55384-138">Select (check) only the **Microsoft.Crm.Sdk.Samples.FollowupPlugin** plug-in.</span><span class="sxs-lookup"><span data-stu-id="55384-138">Select (check) only the **Microsoft.Crm.Sdk.Samples.FollowupPlugin** plug-in.</span></span>  

6. <span data-ttu-id="55384-139">In the **Step#3** section, select the **Sandbox** option.</span><span class="sxs-lookup"><span data-stu-id="55384-139">In the **Step#3** section, select the **Sandbox** option.</span></span>  

7. <span data-ttu-id="55384-140">In the **Step#4** section, select the **Database** option.</span><span class="sxs-lookup"><span data-stu-id="55384-140">In the **Step#4** section, select the **Database** option.</span></span>  

   <span data-ttu-id="55384-141">![Dialog to register an assembly](media/crm-v6s-pr-assembly-registration.png "Dialog to register an assembly")</span><span class="sxs-lookup"><span data-stu-id="55384-141">![Dialog to register an assembly](media/crm-v6s-pr-assembly-registration.png "Dialog to register an assembly")</span></span>  
   <span data-ttu-id="55384-142">Dialog to register an assembly</span><span class="sxs-lookup"><span data-stu-id="55384-142">Dialog to register an assembly</span></span>  

8. <span data-ttu-id="55384-143">Click **Register Selected Plugins**.</span><span class="sxs-lookup"><span data-stu-id="55384-143">Click **Register Selected Plugins**.</span></span> <span data-ttu-id="55384-144">You can close any open dialog boxes.</span><span class="sxs-lookup"><span data-stu-id="55384-144">You can close any open dialog boxes.</span></span>  

   <span data-ttu-id="55384-145">![A registered plug-in shown in the tree view](media/crm-v6s-pr-registered-plugin.PNG "A registered plug-in shown in the tree view")</span><span class="sxs-lookup"><span data-stu-id="55384-145">![A registered plug-in shown in the tree view](media/crm-v6s-pr-registered-plugin.PNG "A registered plug-in shown in the tree view")</span></span>  
   <span data-ttu-id="55384-146">A registered plug-in shown in the tree view</span><span class="sxs-lookup"><span data-stu-id="55384-146">A registered plug-in shown in the tree view</span></span>  

   > [!TIP]
   >  <span data-ttu-id="55384-147">Do you see an error in the **Log** area and the log contains the following message?</span><span class="sxs-lookup"><span data-stu-id="55384-147">Do you see an error in the **Log** area and the log contains the following message?</span></span>  
   >   
   >  `<Message>Action failed for assembly 'SamplePlugins, Version=0.0.0.0, Culture=neutral, PublicKeyToken=829f574d80e89132': Deployment/Scalegroup does not allow running external code.</Message>`  
   >   
   >  <span data-ttu-id="55384-148">If so, you must enable custom code on the server and try again.</span><span class="sxs-lookup"><span data-stu-id="55384-148">If so, you must enable custom code on the server and try again.</span></span> <span data-ttu-id="55384-149">For more information see [Enable or Disable Custom Code Execution](register-deploy-plugins.md#bkmk_enablecode).</span><span class="sxs-lookup"><span data-stu-id="55384-149">For more information see [Enable or Disable Custom Code Execution](register-deploy-plugins.md#bkmk_enablecode).</span></span>  

   <span data-ttu-id="55384-150">The SamplePlugins.dll assembly and FollowupPlugin plug-in are now registered and deployed to the server.</span><span class="sxs-lookup"><span data-stu-id="55384-150">The SamplePlugins.dll assembly and FollowupPlugin plug-in are now registered and deployed to the server.</span></span> <span data-ttu-id="55384-151">If you used the tool to register a custom workflow activity assembly, the next section on registering a step does not apply.</span><span class="sxs-lookup"><span data-stu-id="55384-151">If you used the tool to register a custom workflow activity assembly, the next section on registering a step does not apply.</span></span>  

### <a name="register-a-plug-in-step-for-an-event"></a><span data-ttu-id="55384-152">Register a plug-in step for an event</span><span class="sxs-lookup"><span data-stu-id="55384-152">Register a plug-in step for an event</span></span>  

1. <span data-ttu-id="55384-153">In the **Registered Plug-ins & Custom Workflow Activities** tree view, expand the **(Assembly) SamplePlugins** node and select a registered plug-in.</span><span class="sxs-lookup"><span data-stu-id="55384-153">In the **Registered Plug-ins & Custom Workflow Activities** tree view, expand the **(Assembly) SamplePlugins** node and select a registered plug-in.</span></span>  

2. <span data-ttu-id="55384-154">Navigate to the **Register** menu in the toolbar, and then click **Register New Step**.</span><span class="sxs-lookup"><span data-stu-id="55384-154">Navigate to the **Register** menu in the toolbar, and then click **Register New Step**.</span></span>  

   > [!NOTE]
   >  <span data-ttu-id="55384-155">Plug-ins are registered to execute when an event is processed in the event execution pipeline.</span><span class="sxs-lookup"><span data-stu-id="55384-155">Plug-ins are registered to execute when an event is processed in the event execution pipeline.</span></span> <span data-ttu-id="55384-156">Each event has a stage name and number to indicate its location in the pipeline either before or after the core platform operation.</span><span class="sxs-lookup"><span data-stu-id="55384-156">Each event has a stage name and number to indicate its location in the pipeline either before or after the core platform operation.</span></span> <span data-ttu-id="55384-157">A *step* refers to the SDK message processing step entity that is used to configure when and how the plug-in is to be executed.</span><span class="sxs-lookup"><span data-stu-id="55384-157">A *step* refers to the SDK message processing step entity that is used to configure when and how the plug-in is to be executed.</span></span>  

3. <span data-ttu-id="55384-158">Complete the **Register New Step** dialog box as shown in the following figure.</span><span class="sxs-lookup"><span data-stu-id="55384-158">Complete the **Register New Step** dialog box as shown in the following figure.</span></span>  

   <span data-ttu-id="55384-159">![Dialog to register a new step](media/crm-v6s-pr-register-step.png "Dialog to register a new step")</span><span class="sxs-lookup"><span data-stu-id="55384-159">![Dialog to register a new step](media/crm-v6s-pr-register-step.png "Dialog to register a new step")</span></span>  
   <span data-ttu-id="55384-160">Dialog to register a new step</span><span class="sxs-lookup"><span data-stu-id="55384-160">Dialog to register a new step</span></span>  

4. <span data-ttu-id="55384-161">Click **Register New Step**.</span><span class="sxs-lookup"><span data-stu-id="55384-161">Click **Register New Step**.</span></span>  

5. <span data-ttu-id="55384-162">Expand the **(Assembly) SamplePlugins** node and sub-nodes to see the plug-in and step nodes you created.</span><span class="sxs-lookup"><span data-stu-id="55384-162">Expand the **(Assembly) SamplePlugins** node and sub-nodes to see the plug-in and step nodes you created.</span></span> <span data-ttu-id="55384-163">You can now close the tool, but you may want to keep it open until after you test the plug-in and unregister the assembly.</span><span class="sxs-lookup"><span data-stu-id="55384-163">You can now close the tool, but you may want to keep it open until after you test the plug-in and unregister the assembly.</span></span>  

   > [!NOTE]
   >  <span data-ttu-id="55384-164">To unregister the step, plug-in, or assembly, select its node in the tree, and then click **Unregister** in the tool bar.</span><span class="sxs-lookup"><span data-stu-id="55384-164">To unregister the step, plug-in, or assembly, select its node in the tree, and then click **Unregister** in the tool bar.</span></span>  <span data-ttu-id="55384-165">To modify an assembly or step registration, double-click the assembly or step node in the tree view.</span><span class="sxs-lookup"><span data-stu-id="55384-165">To modify an assembly or step registration, double-click the assembly or step node in the tree view.</span></span> <span data-ttu-id="55384-166">Alternately, you can select the node and click **Update** in the tool bar.</span><span class="sxs-lookup"><span data-stu-id="55384-166">Alternately, you can select the node and click **Update** in the tool bar.</span></span>  

   <span data-ttu-id="55384-167">The plug-in is now registered to execute in the sandbox, for an account create event, and after the core operation executes.</span><span class="sxs-lookup"><span data-stu-id="55384-167">The plug-in is now registered to execute in the sandbox, for an account create event, and after the core operation executes.</span></span> <span data-ttu-id="55384-168">You registered the plug-in to run asynchronously since the creation of the follow-up task activity is not time critical.</span><span class="sxs-lookup"><span data-stu-id="55384-168">You registered the plug-in to run asynchronously since the creation of the follow-up task activity is not time critical.</span></span> <span data-ttu-id="55384-169">After an account is created, the plug-in will execute the next time the asynchronous service processes its queue.</span><span class="sxs-lookup"><span data-stu-id="55384-169">After an account is created, the plug-in will execute the next time the asynchronous service processes its queue.</span></span>  

## <a name="test-the-plug-in"></a><span data-ttu-id="55384-170">Test the plug-in</span><span class="sxs-lookup"><span data-stu-id="55384-170">Test the plug-in</span></span>  
 <span data-ttu-id="55384-171">After you register the plug-in you can optionally test its execution by using the following procedure.</span><span class="sxs-lookup"><span data-stu-id="55384-171">After you register the plug-in you can optionally test its execution by using the following procedure.</span></span>  

1. <span data-ttu-id="55384-172">Open the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application for the same organization that you registered the plug-in assembly under.</span><span class="sxs-lookup"><span data-stu-id="55384-172">Open the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application for the same organization that you registered the plug-in assembly under.</span></span>  

2. <span data-ttu-id="55384-173">Move to the workplace, select **Accounts**, and then click **New**.</span><span class="sxs-lookup"><span data-stu-id="55384-173">Move to the workplace, select **Accounts**, and then click **New**.</span></span>  

3. <span data-ttu-id="55384-174">In the **Account Name** box, type an account name, for example, `Adventure Works Cycle`, and then click **Save & Close**.</span><span class="sxs-lookup"><span data-stu-id="55384-174">In the **Account Name** box, type an account name, for example, `Adventure Works Cycle`, and then click **Save & Close**.</span></span>  

4. <span data-ttu-id="55384-175">Double-click the form name in the **Accounts** grid to open the form.</span><span class="sxs-lookup"><span data-stu-id="55384-175">Double-click the form name in the **Accounts** grid to open the form.</span></span>  

5. <span data-ttu-id="55384-176">Click **Activities** to display a list of related activities for the account.</span><span class="sxs-lookup"><span data-stu-id="55384-176">Click **Activities** to display a list of related activities for the account.</span></span> <span data-ttu-id="55384-177">You should see the activity named “Send email to the new customer“ that the plug-in created.</span><span class="sxs-lookup"><span data-stu-id="55384-177">You should see the activity named “Send email to the new customer“ that the plug-in created.</span></span>  

6. <span data-ttu-id="55384-178">If you registered the plug-in to run asynchronously, and did not select the **Delete AsyncOperation if StatusCode = Successful** option on the **Register New Step** form, there will be a new system job named “FollowupPlugin: Create of account”.</span><span class="sxs-lookup"><span data-stu-id="55384-178">If you registered the plug-in to run asynchronously, and did not select the **Delete AsyncOperation if StatusCode = Successful** option on the **Register New Step** form, there will be a new system job named “FollowupPlugin: Create of account”.</span></span> <span data-ttu-id="55384-179">To view the related system job, click **Settings**, and then click **System Jobs**.</span><span class="sxs-lookup"><span data-stu-id="55384-179">To view the related system job, click **Settings**, and then click **System Jobs**.</span></span> <span data-ttu-id="55384-180">Double-click the system job previously mentioned.</span><span class="sxs-lookup"><span data-stu-id="55384-180">Double-click the system job previously mentioned.</span></span>  

   <span data-ttu-id="55384-181">You can now unregister the step, plug-in, and assembly if you want.</span><span class="sxs-lookup"><span data-stu-id="55384-181">You can now unregister the step, plug-in, and assembly if you want.</span></span> <span data-ttu-id="55384-182">You may also want to delete the system job and account that you created.</span><span class="sxs-lookup"><span data-stu-id="55384-182">You may also want to delete the system job and account that you created.</span></span>  

### <a name="see-also"></a><span data-ttu-id="55384-183">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="55384-183">See also</span></span>  
 <span data-ttu-id="55384-184">[Plug-in Development](plugin-development.md) </span><span class="sxs-lookup"><span data-stu-id="55384-184">[Plug-in Development](plugin-development.md) </span></span>  
 <span data-ttu-id="55384-185">[Walkthrough: Configure Assembly Security for an Offline Plug-in](walkthrough-configure-assembly-security-offline-plugin.md) </span><span class="sxs-lookup"><span data-stu-id="55384-185">[Walkthrough: Configure Assembly Security for an Offline Plug-in](walkthrough-configure-assembly-security-offline-plugin.md) </span></span>  
 <span data-ttu-id="55384-186">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span><span class="sxs-lookup"><span data-stu-id="55384-186">[Register and Deploy Plug-ins](register-deploy-plugins.md) </span></span>  
 <span data-ttu-id="55384-187">[Event Execution Pipeline](event-execution-pipeline.md) </span><span class="sxs-lookup"><span data-stu-id="55384-187">[Event Execution Pipeline](event-execution-pipeline.md) </span></span>  
 <span data-ttu-id="55384-188">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span><span class="sxs-lookup"><span data-stu-id="55384-188">[Plug-in Isolation, Trust, and Statistics](plugin-isolation-trusts-statistics.md) </span></span>  
 [<span data-ttu-id="55384-189">Supported Messages and Entities for Plug-ins</span><span class="sxs-lookup"><span data-stu-id="55384-189">Supported Messages and Entities for Plug-ins</span></span>](supported-messages-entities-plugin.md)
