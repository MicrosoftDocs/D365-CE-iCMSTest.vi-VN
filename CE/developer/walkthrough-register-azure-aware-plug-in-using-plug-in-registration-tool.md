---
title: 'Walkthrough: Register an Azure-aware plug-in using the Plug-in Registration Tool (Developer Guide for Dynamics 365 for Customer Engagement apps) | MicrosoftDocs'
description: 'The walkthrough demonstrates how to register a service endpoint step using the Plug-in Registration Tool. '
ms.custom: ''
ms.date: 10/31/2017
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: adc9af13-8505-4701-ab74-064df1f346a0
caps.latest.revision: 64
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 3af0f3433f4439d8cb5df79161a4176413f5f36a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385839"
---
# <a name="walkthrough-register-an-azure-aware-plug-in-using-the-plug-in-registration-tool"></a><span data-ttu-id="05c51-103">Walkthrough: Register an Azure-aware plug-in using the Plug-in Registration Tool</span><span class="sxs-lookup"><span data-stu-id="05c51-103">Walkthrough: Register an Azure-aware plug-in using the Plug-in Registration Tool</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="05c51-104">This walkthrough demonstrates how to register a service endpoint step using the Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="05c51-104">This walkthrough demonstrates how to register a service endpoint step using the Plug-in Registration Tool.</span></span> <span data-ttu-id="05c51-105">Once configured, [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement can post the execution context of the current operation to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution endpoint.</span><span class="sxs-lookup"><span data-stu-id="05c51-105">Once configured, [!INCLUDE[pn_dynamics_crm_online](../includes/pn-dynamics-crm-online.md)] Customer Engagement can post the execution context of the current operation to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] solution endpoint.</span></span> <span data-ttu-id="05c51-106">For this walkthrough, the step is registered to post the execution context of the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message for an `Account` entity to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="05c51-106">For this walkthrough, the step is registered to post the execution context of the <xref:Microsoft.Xrm.Sdk.Messages.CreateRequest> message for an `Account` entity to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span>  

 <span data-ttu-id="05c51-107">The following prerequisites must be completed before you start this walkthrough:</span><span class="sxs-lookup"><span data-stu-id="05c51-107">The following prerequisites must be completed before you start this walkthrough:</span></span>  

- <span data-ttu-id="05c51-108">Access to the Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="05c51-108">Access to the Plug-in Registration Tool.</span></span> [!INCLUDE[proc-download-plugin-registration-tool](../includes/proc-download-plugin-registration-tool.md)] 

- <span data-ttu-id="05c51-109">Your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] system user account must have the System Customizer or System Administrator role.</span><span class="sxs-lookup"><span data-stu-id="05c51-109">Your [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] system user account must have the System Customizer or System Administrator role.</span></span> <span data-ttu-id="05c51-110">For more information, see [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement](security-dev/how-role-based-security-control-access-entities.md).</span><span class="sxs-lookup"><span data-stu-id="05c51-110">For more information, see [How Role-Based Security Can Be Used to Control Access to Entities In Dynamics 365 for Customer Engagement](security-dev/how-role-based-security-control-access-entities.md).</span></span>  

- <span data-ttu-id="05c51-111">Have access to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] platform service namespace that is configured for SAS authorization, to which [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will post a message.</span><span class="sxs-lookup"><span data-stu-id="05c51-111">Have access to a [!INCLUDE[pn_Windows_Azure](../includes/pn-windows-azure.md)] platform service namespace that is configured for SAS authorization, to which [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] will post a message.</span></span>  


- <span data-ttu-id="05c51-112">If you plan to use any other [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging entity other than a queue, for example a relay, there must be a listener application actively listening to the specified solution endpoint for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to successfully post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span><span class="sxs-lookup"><span data-stu-id="05c51-112">If you plan to use any other [!INCLUDE[pn_azure_shortest](../includes/pn-azure-shortest.md)] messaging entity other than a queue, for example a relay, there must be a listener application actively listening to the specified solution endpoint for [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to successfully post to the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)].</span></span> <span data-ttu-id="05c51-113">For more information, see [Write a Listener for an Azure Solution](write-listener-application-azure-solution.md).</span><span class="sxs-lookup"><span data-stu-id="05c51-113">For more information, see [Write a Listener for an Azure Solution](write-listener-application-azure-solution.md).</span></span>  

- <span data-ttu-id="05c51-114">A configured service endpoint with SAS authorization is available in the target organization.</span><span class="sxs-lookup"><span data-stu-id="05c51-114">A configured service endpoint with SAS authorization is available in the target organization.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="05c51-115">[Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement](walkthrough-configure-azure-sas-integration.md).</span><span class="sxs-lookup"><span data-stu-id="05c51-115">[Walkthrough: Configure Microsoft Azure (SAS) for integration with Dynamics 365 for Customer Engagement](walkthrough-configure-azure-sas-integration.md).</span></span>  

## <a name="steps"></a><span data-ttu-id="05c51-116">Bước</span><span class="sxs-lookup"><span data-stu-id="05c51-116">Steps</span></span>  
 <span data-ttu-id="05c51-117">This walkthrough contains the following steps:</span><span class="sxs-lookup"><span data-stu-id="05c51-117">This walkthrough contains the following steps:</span></span>  

1.  [<span data-ttu-id="05c51-118">Connect to the Dynamics 365 for Customer Engagement server</span><span class="sxs-lookup"><span data-stu-id="05c51-118">Connect to the Dynamics 365 for Customer Engagement server</span></span>](#BKMK_Connect)  

2.  [<span data-ttu-id="05c51-119">Register a service endpoint step for an event</span><span class="sxs-lookup"><span data-stu-id="05c51-119">Register a service endpoint step for an event</span></span>](#BKMK_Register)  

3.  [<span data-ttu-id="05c51-120">Test the endpoint registration</span><span class="sxs-lookup"><span data-stu-id="05c51-120">Test the endpoint registration</span></span>](#BKMK_Test)  

<a name="BKMK_Connect"></a>   
## <a name="connect-to-the-includepndynamicscrmincludespn-dynamics-crmmd-server"></a><span data-ttu-id="05c51-121">Connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server</span><span class="sxs-lookup"><span data-stu-id="05c51-121">Connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server</span></span>  
 <span data-ttu-id="05c51-122">Follow the steps below to connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server using the Plug-in Registration tool.</span><span class="sxs-lookup"><span data-stu-id="05c51-122">Follow the steps below to connect to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server using the Plug-in Registration tool.</span></span>  

1. <span data-ttu-id="05c51-123">Run the Plug-in Registration tool.</span><span class="sxs-lookup"><span data-stu-id="05c51-123">Run the Plug-in Registration tool.</span></span>  

2. <span data-ttu-id="05c51-124">Click **Create New Connection**.</span><span class="sxs-lookup"><span data-stu-id="05c51-124">Click **Create New Connection**.</span></span>  

3. <span data-ttu-id="05c51-125">In the **Login** dialog box, select the deployment type radio button corresponding to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server you intend to register a service endpoint with.</span><span class="sxs-lookup"><span data-stu-id="05c51-125">In the **Login** dialog box, select the deployment type radio button corresponding to the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] server you intend to register a service endpoint with.</span></span> <span data-ttu-id="05c51-126">The **On-premises** radio button includes an IFD deployment and the **Office 365** button is for the [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span><span class="sxs-lookup"><span data-stu-id="05c51-126">The **On-premises** radio button includes an IFD deployment and the **Office 365** button is for the [!INCLUDE[pn_MS_Online_Services](../includes/pn-ms-online-services.md)] provider of [!INCLUDE[pn_CRM_Online](../includes/pn-crm-online.md)].</span></span>  


   |                                                                                                                                             |                                                                                                                                                                                 |
   |---------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   | <span data-ttu-id="05c51-127">![Login form for an online deployment](media/crm-v6s-pr.png "Login form for an online deployment")</span><span class="sxs-lookup"><span data-stu-id="05c51-127">![Login form for an online deployment](media/crm-v6s-pr.png "Login form for an online deployment")</span></span><br /><span data-ttu-id="05c51-128">Login form for an online deployment</span><span class="sxs-lookup"><span data-stu-id="05c51-128">Login form for an online deployment</span></span> | <span data-ttu-id="05c51-129">![Login window for an on-premises deployment](media/crm-v6s-pr-login-onprem.png "Login window for an on-premises deployment")</span><span class="sxs-lookup"><span data-stu-id="05c51-129">![Login window for an on-premises deployment](media/crm-v6s-pr-login-onprem.png "Login window for an on-premises deployment")</span></span><br /><span data-ttu-id="05c51-130">Login form for an on-premises deployment</span><span class="sxs-lookup"><span data-stu-id="05c51-130">Login form for an on-premises deployment</span></span> |


4. <span data-ttu-id="05c51-131">If you check **Display list of available organizations**, you are presented with a list of organizations that you belong to after you click **Login**.</span><span class="sxs-lookup"><span data-stu-id="05c51-131">If you check **Display list of available organizations**, you are presented with a list of organizations that you belong to after you click **Login**.</span></span> <span data-ttu-id="05c51-132">This enables you to choose the organization that you want to register the service endpoint with.</span><span class="sxs-lookup"><span data-stu-id="05c51-132">This enables you to choose the organization that you want to register the service endpoint with.</span></span> <span data-ttu-id="05c51-133">Otherwise, your default organization is used.</span><span class="sxs-lookup"><span data-stu-id="05c51-133">Otherwise, your default organization is used.</span></span>  

5. <span data-ttu-id="05c51-134">Enter the indicated information about the server and login account, and then click **Login**.</span><span class="sxs-lookup"><span data-stu-id="05c51-134">Enter the indicated information about the server and login account, and then click **Login**.</span></span>  

<a name="BKMK_Register"></a>   
## <a name="register-a-service-endpoint-step-for-an-event"></a><span data-ttu-id="05c51-135">Register a service endpoint step for an event</span><span class="sxs-lookup"><span data-stu-id="05c51-135">Register a service endpoint step for an event</span></span>  
 <span data-ttu-id="05c51-136">Follow the steps below to register a step for an event on the service endpoint.</span><span class="sxs-lookup"><span data-stu-id="05c51-136">Follow the steps below to register a step for an event on the service endpoint.</span></span>  

1. <span data-ttu-id="05c51-137">Select an existing service endpoint in the tab of the tab of the target organization.</span><span class="sxs-lookup"><span data-stu-id="05c51-137">Select an existing service endpoint in the tab of the tab of the target organization.</span></span>  

2. <span data-ttu-id="05c51-138">Navigate to the **Register** menu and click **Register New Step**.</span><span class="sxs-lookup"><span data-stu-id="05c51-138">Navigate to the **Register** menu and click **Register New Step**.</span></span>  

3. <span data-ttu-id="05c51-139">Fill out the **Register New Step** dialog box for an account create event as shown in the following figure.</span><span class="sxs-lookup"><span data-stu-id="05c51-139">Fill out the **Register New Step** dialog box for an account create event as shown in the following figure.</span></span>  

   <span data-ttu-id="05c51-140">![Creating a service endpoint step](media/crm-v6s-pr-service-endpoint-step.png "Creating a service endpoint step")</span><span class="sxs-lookup"><span data-stu-id="05c51-140">![Creating a service endpoint step](media/crm-v6s-pr-service-endpoint-step.png "Creating a service endpoint step")</span></span>  

4. <span data-ttu-id="05c51-141">Click **Register New Step**.</span><span class="sxs-lookup"><span data-stu-id="05c51-141">Click **Register New Step**.</span></span>  

   [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="05c51-142">will now post the current message containing the execution context to the service bus whenever an account is created.</span><span class="sxs-lookup"><span data-stu-id="05c51-142">will now post the current message containing the execution context to the service bus whenever an account is created.</span></span> <span data-ttu-id="05c51-143">The post is performed asynchronously and is not executed immediately.</span><span class="sxs-lookup"><span data-stu-id="05c51-143">The post is performed asynchronously and is not executed immediately.</span></span>  

<a name="BKMK_Test"></a>   
## <a name="test-the-endpoint-registration"></a><span data-ttu-id="05c51-144">Test the endpoint registration</span><span class="sxs-lookup"><span data-stu-id="05c51-144">Test the endpoint registration</span></span>  
 <span data-ttu-id="05c51-145">After you register the endpoint you can test it.</span><span class="sxs-lookup"><span data-stu-id="05c51-145">After you register the endpoint you can test it.</span></span> <span data-ttu-id="05c51-146">A listener must be running or a queue available on the target endpoint for the service bus post from the plug-in to happen.</span><span class="sxs-lookup"><span data-stu-id="05c51-146">A listener must be running or a queue available on the target endpoint for the service bus post from the plug-in to happen.</span></span>  

1. <span data-ttu-id="05c51-147">Open the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application for the same organization that you registered the service endpoint under.</span><span class="sxs-lookup"><span data-stu-id="05c51-147">Open the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] web application for the same organization that you registered the service endpoint under.</span></span>  

2. <span data-ttu-id="05c51-148">Click the **Create** button ![Create button](media/crm-v6s-wa-create-icon.PNG "Create button"), and then click **Account**.</span><span class="sxs-lookup"><span data-stu-id="05c51-148">Click the **Create** button ![Create button](media/crm-v6s-wa-create-icon.PNG "Create button"), and then click **Account**.</span></span>  

3. <span data-ttu-id="05c51-149">Enter an account name, for example `Adventure Works Cycle`, into the **Account Name** field, and then click **Save**.</span><span class="sxs-lookup"><span data-stu-id="05c51-149">Enter an account name, for example `Adventure Works Cycle`, into the **Account Name** field, and then click **Save**.</span></span>  

4. <span data-ttu-id="05c51-150">Wait about 10 minutes for the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] post to occur.</span><span class="sxs-lookup"><span data-stu-id="05c51-150">Wait about 10 minutes for the [!INCLUDE[windows_azure_service_bus](../includes/windows-azure-service-bus.md)] post to occur.</span></span>  

5. <span data-ttu-id="05c51-151">Click **Settings > System Jobs**.</span><span class="sxs-lookup"><span data-stu-id="05c51-151">Click **Settings > System Jobs**.</span></span>  

6. <span data-ttu-id="05c51-152">Open the system job that has the same name that you specified for your service endpoint.</span><span class="sxs-lookup"><span data-stu-id="05c51-152">Open the system job that has the same name that you specified for your service endpoint.</span></span> <span data-ttu-id="05c51-153">Check the status to see if the post was successful, is waiting, or failed.</span><span class="sxs-lookup"><span data-stu-id="05c51-153">Check the status to see if the post was successful, is waiting, or failed.</span></span>  

   <span data-ttu-id="05c51-154">You can now unregister the endpoint, if so desired, by selecting it in the tool’s tree view and click **Unregister**.</span><span class="sxs-lookup"><span data-stu-id="05c51-154">You can now unregister the endpoint, if so desired, by selecting it in the tool’s tree view and click **Unregister**.</span></span>  

### <a name="see-also"></a><span data-ttu-id="05c51-155">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="05c51-155">See also</span></span>  
 <span data-ttu-id="05c51-156">[Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span><span class="sxs-lookup"><span data-stu-id="05c51-156">[Azure Extensions for Dynamics 365 for Customer Engagement apps](azure-extensions.md) </span></span>  
 [<span data-ttu-id="05c51-157">Introduction to Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps</span><span class="sxs-lookup"><span data-stu-id="05c51-157">Introduction to Microsoft Azure Integration with Dynamics 365 for Customer Engagement apps</span></span>](azure-integration.md)
