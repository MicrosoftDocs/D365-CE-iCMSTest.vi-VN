---
title: Sample code for softphone integration using Channel Integration Framework (CIF) | Microsoft Docs
description: Learn about sample code for softphone integration using Channel Integration Framework (CIF) with Microsoft Dynamics 365 Unified Interface App.
keywords: ''
ms.date: 12/17/2018
ms.service:
- dynamics-365-cross-app
ms.custom:
- dyn365-a11y
- dyn365-developer
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
- Dynamics 365 for Customer Engagement Version 9.x
ms.assetid: 30E520EC-1791-48DD-BD70-1D29D78E89AB
author: kabala123
ms.author: kabala
manager: shujoshi
ms.openlocfilehash: 78f46bdb998963ddea3148e1aa11714016a44f7a
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387679"
---
# <a name="sample-softphone-integration-using-channel-integration-framework"></a><span data-ttu-id="26342-103">Sample softphone integration using Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="26342-103">Sample softphone integration using Channel Integration Framework</span></span>

<span data-ttu-id="26342-104">[Download](https://go.microsoft.com/fwlink/p/?linkid=2025867) the sample to integrate a softphone with Dynamics 365 for Customer Engagement apps using Channel Integration Framework.</span><span class="sxs-lookup"><span data-stu-id="26342-104">[Download](https://go.microsoft.com/fwlink/p/?linkid=2025867) the sample to integrate a softphone with Dynamics 365 for Customer Engagement apps using Channel Integration Framework.</span></span>

> [!NOTE]
> <span data-ttu-id="26342-105">The sample code does not support Internet Explorer and on browsers that do not have webRTC support.</span><span class="sxs-lookup"><span data-stu-id="26342-105">The sample code does not support Internet Explorer and on browsers that do not have webRTC support.</span></span> <span data-ttu-id="26342-106">More information [WebRTC](https://webrtc.org/)</span><span class="sxs-lookup"><span data-stu-id="26342-106">More information [WebRTC](https://webrtc.org/)</span></span>

> [!Important]
> - <span data-ttu-id="26342-107">This sample code currently has limited availability.</span><span class="sxs-lookup"><span data-stu-id="26342-107">This sample code currently has limited availability.</span></span>
> - <span data-ttu-id="26342-108">The sample code for softphone integration with Dynamics 365 using Channel Integration Framework is made available so customers can get early access and provide feedback.</span><span class="sxs-lookup"><span data-stu-id="26342-108">The sample code for softphone integration with Dynamics 365 using Channel Integration Framework is made available so customers can get early access and provide feedback.</span></span> <span data-ttu-id="26342-109">The sample code is not meant for production use and may have limited or restricted functionality.</span><span class="sxs-lookup"><span data-stu-id="26342-109">The sample code is not meant for production use and may have limited or restricted functionality.</span></span>
> - <span data-ttu-id="26342-110">Microsoft doesn't provide support for this sample code for production use and Microsoft Dynamics 365 Technical Support won’t be able to help you with issues or questions.</span><span class="sxs-lookup"><span data-stu-id="26342-110">Microsoft doesn't provide support for this sample code for production use and Microsoft Dynamics 365 Technical Support won’t be able to help you with issues or questions.</span></span> <span data-ttu-id="26342-111">This is subject to [supplemental terms of use](http://go.microsoft.com/fwlink/p/?LinkId=511446)</span><span class="sxs-lookup"><span data-stu-id="26342-111">This is subject to [supplemental terms of use](http://go.microsoft.com/fwlink/p/?LinkId=511446)</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="26342-112">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="26342-112">Pre-requisites</span></span>

- <span data-ttu-id="26342-113">A valid Azure subscription is required to publish the sample app to Azure.</span><span class="sxs-lookup"><span data-stu-id="26342-113">A valid Azure subscription is required to publish the sample app to Azure.</span></span>
> [!Note]
> <span data-ttu-id="26342-114">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/).</span><span class="sxs-lookup"><span data-stu-id="26342-114">If you don't have an Azure subscription, create a [free account](https://azure.microsoft.com/free/).</span></span>


## <a name="publish-sample-app-to-azure"></a><span data-ttu-id="26342-115">Publish sample app to Azure</span><span class="sxs-lookup"><span data-stu-id="26342-115">Publish sample app to Azure</span></span>

1. <span data-ttu-id="26342-116">Open the solution **SampleInteg.sln** using Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="26342-116">Open the solution **SampleInteg.sln** using Visual Studio 2017.</span></span>
2. <span data-ttu-id="26342-117">In **Solution Explorer**, right-click on the solution and build the complete solution.</span><span class="sxs-lookup"><span data-stu-id="26342-117">In **Solution Explorer**, right-click on the solution and build the complete solution.</span></span>
3. <span data-ttu-id="26342-118">In **Solution Explorer**, right-click on the project **SampleInteg**  and select **Publish**</span><span class="sxs-lookup"><span data-stu-id="26342-118">In **Solution Explorer**, right-click on the project **SampleInteg**  and select **Publish**</span></span>
4. <span data-ttu-id="26342-119">Select **Start** to launch the **Publish** wizard.</span><span class="sxs-lookup"><span data-stu-id="26342-119">Select **Start** to launch the **Publish** wizard.</span></span>
5. <span data-ttu-id="26342-120">Choose **App Service** as the publish target.</span><span class="sxs-lookup"><span data-stu-id="26342-120">Choose **App Service** as the publish target.</span></span>
6. <span data-ttu-id="26342-121">Select **Create New** and select on **Publish**.</span><span class="sxs-lookup"><span data-stu-id="26342-121">Select **Create New** and select on **Publish**.</span></span>
7. <span data-ttu-id="26342-122">Provide an app name.</span><span class="sxs-lookup"><span data-stu-id="26342-122">Provide an app name.</span></span><br> <span data-ttu-id="26342-123">For example, **SampleInteg**.</span><span class="sxs-lookup"><span data-stu-id="26342-123">For example, **SampleInteg**.</span></span>
8. <span data-ttu-id="26342-124">Provide valid subscription, resource group, and hosting plan details.</span><span class="sxs-lookup"><span data-stu-id="26342-124">Provide valid subscription, resource group, and hosting plan details.</span></span>
9. <span data-ttu-id="26342-125">Select *Create* to create the azure app service, and save the app service URL for future use.</span><span class="sxs-lookup"><span data-stu-id="26342-125">Select *Create* to create the azure app service, and save the app service URL for future use.</span></span><br><span data-ttu-id="26342-126">Ví dụ, `https://sampleinteg.azurewebsites.net`.</span><span class="sxs-lookup"><span data-stu-id="26342-126">For example, `https://sampleinteg.azurewebsites.net`.</span></span>

## <a name="create-function-to-use-with-the-app-service"></a><span data-ttu-id="26342-127">Create function to use with the app service</span><span class="sxs-lookup"><span data-stu-id="26342-127">Create function to use with the app service</span></span>

1. <span data-ttu-id="26342-128">Create sample code for the **client-voice** function.</span><span class="sxs-lookup"><span data-stu-id="26342-128">Create sample code for the **client-voice** function.</span></span><br> <span data-ttu-id="26342-129">Refer to function from the readme file packaged with the sample softphone integration in the [Dynamics 365 Insider Portal](https://go.microsoft.com/fwlink/p/?linkid=2025867).</span><span class="sxs-lookup"><span data-stu-id="26342-129">Refer to function from the readme file packaged with the sample softphone integration in the [Dynamics 365 Insider Portal](https://go.microsoft.com/fwlink/p/?linkid=2025867).</span></span>

2. <span data-ttu-id="26342-130">Use the sample code for the **capability-token** function.</span><span class="sxs-lookup"><span data-stu-id="26342-130">Use the sample code for the **capability-token** function.</span></span><br> <span data-ttu-id="26342-131">Refer to function from the readme file packaged with the sample softphone integration in the [Dynamics 365 Insider Portal](https://go.microsoft.com/fwlink/p/?linkid=2025867).</span><span class="sxs-lookup"><span data-stu-id="26342-131">Refer to function from the readme file packaged with the sample softphone integration in the [Dynamics 365 Insider Portal](https://go.microsoft.com/fwlink/p/?linkid=2025867).</span></span>

> [!Note] 
> <span data-ttu-id="26342-132">Save the URL for the **capability-token** function you obtain from the above sample code.</span><span class="sxs-lookup"><span data-stu-id="26342-132">Save the URL for the **capability-token** function you obtain from the above sample code.</span></span> <span data-ttu-id="26342-133">For example, URL is `https://sampleinteg.sample/capability-token`.</span><span class="sxs-lookup"><span data-stu-id="26342-133">For example, URL is `https://sampleinteg.sample/capability-token`.</span></span>

## <a name="configure-sample-app-in-dynamics-365"></a><span data-ttu-id="26342-134">Configure sample app in Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="26342-134">Configure sample app in Dynamics 365</span></span>

1. <span data-ttu-id="26342-135">Note the base URL of the CRM org from where all webresources are served.</span><span class="sxs-lookup"><span data-stu-id="26342-135">Note the base URL of the CRM org from where all webresources are served.</span></span> <span data-ttu-id="26342-136">For an online org, this should be of the form `https://<orgname>.crmXX.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="26342-136">For an online org, this should be of the form `https://<orgname>.crmXX.dynamics.com`.</span></span> <span data-ttu-id="26342-137">Ví dụ: `https://sampleorg.crm10.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="26342-137">For example, `https://sampleorg.crm10.dynamics.com`</span></span>

1. <span data-ttu-id="26342-138">Get the **Dynamics 365 Channel Integration Framework** solution.</span><span class="sxs-lookup"><span data-stu-id="26342-138">Get the **Dynamics 365 Channel Integration Framework** solution.</span></span> <span data-ttu-id="26342-139">For more information, see [Get Dynamics 365 Channel Integration Framework](get-channel-integration-framework.md).</span><span class="sxs-lookup"><span data-stu-id="26342-139">For more information, see [Get Dynamics 365 Channel Integration Framework](get-channel-integration-framework.md).</span></span>

2. <span data-ttu-id="26342-140">Configure the channel provider by providing the detail as show in the matrix.</span><span class="sxs-lookup"><span data-stu-id="26342-140">Configure the channel provider by providing the detail as show in the matrix.</span></span> <span data-ttu-id="26342-141">For more information, see [Configure the channel provider](configure-channel-provider-channel-integration-framework.md)</span><span class="sxs-lookup"><span data-stu-id="26342-141">For more information, see [Configure the channel provider](configure-channel-provider-channel-integration-framework.md)</span></span>

  | <span data-ttu-id="26342-142">Trường</span><span class="sxs-lookup"><span data-stu-id="26342-142">Field</span></span> | <span data-ttu-id="26342-143">Mô tả</span><span class="sxs-lookup"><span data-stu-id="26342-143">Description</span></span> |
  |-------|-------|
  |<span data-ttu-id="26342-144">Tên</span><span class="sxs-lookup"><span data-stu-id="26342-144">Name</span></span>|<span data-ttu-id="26342-145">Name of the channel provider.</span><span class="sxs-lookup"><span data-stu-id="26342-145">Name of the channel provider.</span></span><br><br> <span data-ttu-id="26342-146">Example: Contoso</span><span class="sxs-lookup"><span data-stu-id="26342-146">Example: Contoso</span></span>|
  |<span data-ttu-id="26342-147">Nhãn</span><span class="sxs-lookup"><span data-stu-id="26342-147">Label</span></span>|<span data-ttu-id="26342-148">The label is displayed as the title on the widget.</span><span class="sxs-lookup"><span data-stu-id="26342-148">The label is displayed as the title on the widget.</span></span><br><br> <span data-ttu-id="26342-149">Example: Contoso</span><span class="sxs-lookup"><span data-stu-id="26342-149">Example: Contoso</span></span>|
  |<span data-ttu-id="26342-150">Channel URL</span><span class="sxs-lookup"><span data-stu-id="26342-150">Channel URL</span></span>| <span data-ttu-id="26342-151">The channel URL is in the format: `<azure_app_service_url>?base=<crm_base_url>&twa=<capability_token_url>`</span><span class="sxs-lookup"><span data-stu-id="26342-151">The channel URL is in the format: `<azure_app_service_url>?base=<crm_base_url>&twa=<capability_token_url>`</span></span><br><br><span data-ttu-id="26342-152">**Note:** In this sample, the URL is `https://sampleinteg.azurewebsites.net?base=https://sampleorg.crm10.dynamics.com&twa=https://sampleinteg.sample/capability-token`.</span><span class="sxs-lookup"><span data-stu-id="26342-152">**Note:** In this sample, the URL is `https://sampleinteg.azurewebsites.net?base=https://sampleorg.crm10.dynamics.com&twa=https://sampleinteg.sample/capability-token`.</span></span> |
  |<span data-ttu-id="26342-153">Enable Outbound Communication</span><span class="sxs-lookup"><span data-stu-id="26342-153">Enable Outbound Communication</span></span>| <span data-ttu-id="26342-154">Có</span><span class="sxs-lookup"><span data-stu-id="26342-154">Yes</span></span> |
  |<span data-ttu-id="26342-155">Channel Order</span><span class="sxs-lookup"><span data-stu-id="26342-155">Channel Order</span></span>| <span data-ttu-id="26342-156">0</span><span class="sxs-lookup"><span data-stu-id="26342-156">0</span></span> |
  |<span data-ttu-id="26342-157">API Version</span><span class="sxs-lookup"><span data-stu-id="26342-157">API Version</span></span>| <span data-ttu-id="26342-158">1.0</span><span class="sxs-lookup"><span data-stu-id="26342-158">1.0</span></span> |
  |<span data-ttu-id="26342-159">Trusted Domains</span><span class="sxs-lookup"><span data-stu-id="26342-159">Trusted Domains</span></span>|<span data-ttu-id="26342-160">The domain (URL) that can access the Channel Integration Framework APIs.</span><span class="sxs-lookup"><span data-stu-id="26342-160">The domain (URL) that can access the Channel Integration Framework APIs.</span></span>|
  |<span data-ttu-id="26342-161">Select the Unified Interface Apps for the Channel</span><span class="sxs-lookup"><span data-stu-id="26342-161">Select the Unified Interface Apps for the Channel</span></span>| <span data-ttu-id="26342-162">The list of Unified Interface Apps where the channel is displayed for the agents.</span><span class="sxs-lookup"><span data-stu-id="26342-162">The list of Unified Interface Apps where the channel is displayed for the agents.</span></span> |
  |<span data-ttu-id="26342-163">Select Roles for the Channel</span><span class="sxs-lookup"><span data-stu-id="26342-163">Select Roles for the Channel</span></span>|<span data-ttu-id="26342-164">The security roles that are present in Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="26342-164">The security roles that are present in Dynamics 365.</span></span><br><span data-ttu-id="26342-165">**Note:** If you do not assign any role, the channel provider is shown to all users assigned for the Dynamics 365 Unified Interface App.</span><span class="sxs-lookup"><span data-stu-id="26342-165">**Note:** If you do not assign any role, the channel provider is shown to all users assigned for the Dynamics 365 Unified Interface App.</span></span>|

3. <span data-ttu-id="26342-166">Launch the Unified Interface App to see the communication widget on the right side.</span><span class="sxs-lookup"><span data-stu-id="26342-166">Launch the Unified Interface App to see the communication widget on the right side.</span></span><br><br>
<span data-ttu-id="26342-167">**The communication widget in the minimized mode**</span><span class="sxs-lookup"><span data-stu-id="26342-167">**The communication widget in the minimized mode**</span></span><br><br>
<span data-ttu-id="26342-168">![communication widget in the minimized mode](media/widget-minimized-mode.PNG "communication widget in the minimized mode")</span><span class="sxs-lookup"><span data-stu-id="26342-168">![communication widget in the minimized mode](media/widget-minimized-mode.PNG "communication widget in the minimized mode")</span></span>
<br><br>
<span data-ttu-id="26342-169">**The communication widget in the expanded mode**</span><span class="sxs-lookup"><span data-stu-id="26342-169">**The communication widget in the expanded mode**</span></span><br><br>
<span data-ttu-id="26342-170">![communication widget in the expanded mode](media/widget-expanded-mode.PNG "communication widget in the expanded mode")</span><span class="sxs-lookup"><span data-stu-id="26342-170">![communication widget in the expanded mode](media/widget-expanded-mode.PNG "communication widget in the expanded mode")</span></span>

> [!Important]
> - <span data-ttu-id="26342-171">All URLs must be https.</span><span class="sxs-lookup"><span data-stu-id="26342-171">All URLs must be https.</span></span>
> - <span data-ttu-id="26342-172">If you use a self-signed certificate for the Azure app or the Dynamics 365 org, certain browsers may reject the connection and fail to load the sample phone.</span><span class="sxs-lookup"><span data-stu-id="26342-172">If you use a self-signed certificate for the Azure app or the Dynamics 365 org, certain browsers may reject the connection and fail to load the sample phone.</span></span> <span data-ttu-id="26342-173">As a workaround, open the Azure app in a separate tab and accept the certificate once.</span><span class="sxs-lookup"><span data-stu-id="26342-173">As a workaround, open the Azure app in a separate tab and accept the certificate once.</span></span>
> - <span data-ttu-id="26342-174">Ensure microphone and speaker access is not blocked by browser policy.</span><span class="sxs-lookup"><span data-stu-id="26342-174">Ensure microphone and speaker access is not blocked by browser policy.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26342-175">Chủ đề liên quan</span><span class="sxs-lookup"><span data-stu-id="26342-175">Related topics</span></span>

- [<span data-ttu-id="26342-176">Get Dynamics 365 Channel Integration Framework</span><span class="sxs-lookup"><span data-stu-id="26342-176">Get Dynamics 365 Channel Integration Framework</span></span>](get-channel-integration-framework.md)

- [<span data-ttu-id="26342-177">Configure the channel provider</span><span class="sxs-lookup"><span data-stu-id="26342-177">Configure the channel provider</span></span>](configure-channel-provider-channel-integration-framework.md)

- [<span data-ttu-id="26342-178">Microsoft.CIFramework</span><span class="sxs-lookup"><span data-stu-id="26342-178">Microsoft.CIFramework</span></span>](reference/microsoft-ciframework.md)

- [<span data-ttu-id="26342-179">Client-side events</span><span class="sxs-lookup"><span data-stu-id="26342-179">Client-side events</span></span>](reference/client-side-events.md)

- [<span data-ttu-id="26342-180">Tham chiếu thực thể</span><span class="sxs-lookup"><span data-stu-id="26342-180">Entity reference</span></span>](reference/entities-attributes/msdyn-ciprovider.md)