---
title: Setup a Postman environment(Developer Guide for Dynamics 365 for Customer Engagement)| MicrosoftDocs
description: Learn how to setup and configure a Postman environment that connects with Dynamics 365 for Customer Engagement online and on-premise environments.
ms.custom: ''
ms.date: 10/17/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 955BA444-A53D-4843-9429-833B1636E2B4
caps.latest.revision: 7
author: SushantSikka
ms.author: susikka
manager: shujoshi
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 651a2a3001c31408326394219e8431c5834c5afd
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "385940"
---
# <a name="setup-a-postman-environment"></a><span data-ttu-id="1846c-103">Setup a Postman environment</span><span class="sxs-lookup"><span data-stu-id="1846c-103">Setup a Postman environment</span></span>

<span data-ttu-id="1846c-104">You can use Postman to connect to your [!INCLUDE[](../../includes/pn-dyn-365.md)] for Customer Engagement apps instance, compose Web API requests, send them, and view responses.</span><span class="sxs-lookup"><span data-stu-id="1846c-104">You can use Postman to connect to your [!INCLUDE[](../../includes/pn-dyn-365.md)] for Customer Engagement apps instance, compose Web API requests, send them, and view responses.</span></span> <span data-ttu-id="1846c-105">Managing authentication is part that challenges many people.</span><span class="sxs-lookup"><span data-stu-id="1846c-105">Managing authentication is part that challenges many people.</span></span> <span data-ttu-id="1846c-106">Use this information configure a Postman environment to work for both Online and On-premise environments.</span><span class="sxs-lookup"><span data-stu-id="1846c-106">Use this information configure a Postman environment to work for both Online and On-premise environments.</span></span>

<span data-ttu-id="1846c-107">You can use a Postman environment to save a set of variables that you will use to connect.</span><span class="sxs-lookup"><span data-stu-id="1846c-107">You can use a Postman environment to save a set of variables that you will use to connect.</span></span> <span data-ttu-id="1846c-108">These values can be accessed within postman using this syntax: `{{name}}`.</span><span class="sxs-lookup"><span data-stu-id="1846c-108">These values can be accessed within postman using this syntax: `{{name}}`.</span></span> [!INCLUDE[](../../includes/sdk-for-more-info-about.md)] <span data-ttu-id="1846c-109">Postman variables, see [Postman Documentation > Variables](https://www.getpostman.com/docs/v6/postman/environments_and_globals/variables).</span><span class="sxs-lookup"><span data-stu-id="1846c-109">Postman variables, see [Postman Documentation > Variables](https://www.getpostman.com/docs/v6/postman/environments_and_globals/variables).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1846c-110">Điều kiện tiên quyết</span><span class="sxs-lookup"><span data-stu-id="1846c-110">Prerequisites</span></span>

* <span data-ttu-id="1846c-111">An Online or On-premise environment you can connect to.</span><span class="sxs-lookup"><span data-stu-id="1846c-111">An Online or On-premise environment you can connect to.</span></span> 
* <span data-ttu-id="1846c-112">Download and install the [Postman desktop application](https://www.getpostman.com/apps).</span><span class="sxs-lookup"><span data-stu-id="1846c-112">Download and install the [Postman desktop application](https://www.getpostman.com/apps).</span></span>

<span data-ttu-id="1846c-113">Select the connection option that works for your environment:</span><span class="sxs-lookup"><span data-stu-id="1846c-113">Select the connection option that works for your environment:</span></span> 

* [<span data-ttu-id="1846c-114">Connect with an Online environment</span><span class="sxs-lookup"><span data-stu-id="1846c-114">Connect with an Online environment</span></span>](#bkmk_connectonline)
* [<span data-ttu-id="1846c-115">Connect with an On-premise environment</span><span class="sxs-lookup"><span data-stu-id="1846c-115">Connect with an On-premise environment</span></span>](#bkmk_connectonpremise)

<a name="bkmk_connectonline"></a> 

## <a name="connect-with-an-online-environment"></a><span data-ttu-id="1846c-116">Connect with an Online environment</span><span class="sxs-lookup"><span data-stu-id="1846c-116">Connect with an Online environment</span></span>

> [!NOTE]
> <span data-ttu-id="1846c-117">This environment uses a Client ID for an application that is registered for all Dynamics 365 for Customer Engagement apps online environments.</span><span class="sxs-lookup"><span data-stu-id="1846c-117">This environment uses a Client ID for an application that is registered for all Dynamics 365 for Customer Engagement apps online environments.</span></span> <span data-ttu-id="1846c-118">For your own applications you must register you’re an application using the steps described in [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="1846c-118">For your own applications you must register you’re an application using the steps described in [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](../walkthrough-register-dynamics-365-app-azure-active-directory.md).</span></span>



<span data-ttu-id="1846c-119">Use these steps to create a Postman environment that you can use to connect with your Dynamics 365 for Customer Engagement apps (online) instance.</span><span class="sxs-lookup"><span data-stu-id="1846c-119">Use these steps to create a Postman environment that you can use to connect with your Dynamics 365 for Customer Engagement apps (online) instance.</span></span>

1. <span data-ttu-id="1846c-120">Launch the Postman desktop application.</span><span class="sxs-lookup"><span data-stu-id="1846c-120">Launch the Postman desktop application.</span></span>
1. <span data-ttu-id="1846c-121">Click on the **Environment Options** gear icon in top-right corner.</span><span class="sxs-lookup"><span data-stu-id="1846c-121">Click on the **Environment Options** gear icon in top-right corner.</span></span> 
1. <span data-ttu-id="1846c-122">In the **Manage Environments** dialog box that opens up, click on **Add** button to add a new environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-122">In the **Manage Environments** dialog box that opens up, click on **Add** button to add a new environment.</span></span>
<br>
<span data-ttu-id="1846c-123">![Click on Add button to add a new Postman environment](../media/postman-manage-env.png "Click on Add button to add a new Postman environment")</span><span class="sxs-lookup"><span data-stu-id="1846c-123">![Click on Add button to add a new Postman environment](../media/postman-manage-env.png "Click on Add button to add a new Postman environment")</span></span><br>
1. <span data-ttu-id="1846c-124">In the dialog box that opens, add a name for the environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-124">In the dialog box that opens, add a name for the environment.</span></span> <span data-ttu-id="1846c-125">Then add the following key-value pairs into the editing space.</span><span class="sxs-lookup"><span data-stu-id="1846c-125">Then add the following key-value pairs into the editing space.</span></span>

|||
|----|---|
|<span data-ttu-id="1846c-126">url</span><span class="sxs-lookup"><span data-stu-id="1846c-126">url</span></span>|`https://<add your environment name, like ‘myorg.crm’>.dynamics.com`|
|<span data-ttu-id="1846c-127">clientid</span><span class="sxs-lookup"><span data-stu-id="1846c-127">clientid</span></span>|`51f81489-12ee-4a9e-aaae-a2591f45987d`|
|<span data-ttu-id="1846c-128">phiên bản</span><span class="sxs-lookup"><span data-stu-id="1846c-128">version</span></span>|`9.0`|
|<span data-ttu-id="1846c-129">webapiurl</span><span class="sxs-lookup"><span data-stu-id="1846c-129">webapiurl</span></span>|`{{url}}/api/data/v{{version}}/`|
|<span data-ttu-id="1846c-130">callback</span><span class="sxs-lookup"><span data-stu-id="1846c-130">callback</span></span>|`https://callbackurl`|
|<span data-ttu-id="1846c-131">authurl</span><span class="sxs-lookup"><span data-stu-id="1846c-131">authurl</span></span>|`https://login.microsoftonline.com/common/oauth2/authorize?resource={{url}}`|

<span data-ttu-id="1846c-132">![Create a new Postman environment to connect with Online instance](../media/postman-add-online-env.png "Create a new Postman environment to connect with Online instance")</span><span class="sxs-lookup"><span data-stu-id="1846c-132">![Create a new Postman environment to connect with Online instance](../media/postman-add-online-env.png "Create a new Postman environment to connect with Online instance")</span></span>

1. <span data-ttu-id="1846c-133">Replace the instance URL placeholder value with the URL of your Dynamics 365 for Customer Engagement apps instance and click **Add** to save the environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-133">Replace the instance URL placeholder value with the URL of your Dynamics 365 for Customer Engagement apps instance and click **Add** to save the environment.</span></span>

1. <span data-ttu-id="1846c-134">Close the **Manage environments** dialog.</span><span class="sxs-lookup"><span data-stu-id="1846c-134">Close the **Manage environments** dialog.</span></span>  

### <a name="generate-an-access-token-to-use-with-your-environment"></a><span data-ttu-id="1846c-135">Generate an Access Token to use with your environment</span><span class="sxs-lookup"><span data-stu-id="1846c-135">Generate an Access Token to use with your environment</span></span>

<span data-ttu-id="1846c-136">To connect using **OAuth 2.0**, you must have an access token.</span><span class="sxs-lookup"><span data-stu-id="1846c-136">To connect using **OAuth 2.0**, you must have an access token.</span></span> <span data-ttu-id="1846c-137">Use the following steps to get a new access token.</span><span class="sxs-lookup"><span data-stu-id="1846c-137">Use the following steps to get a new access token.</span></span>

1. <span data-ttu-id="1846c-138">Make sure the new environment you created is selected in the environments.</span><span class="sxs-lookup"><span data-stu-id="1846c-138">Make sure the new environment you created is selected in the environments.</span></span>
1. <span data-ttu-id="1846c-139">Select the **Authorization** tab.</span><span class="sxs-lookup"><span data-stu-id="1846c-139">Select the **Authorization** tab.</span></span>
1. <span data-ttu-id="1846c-140">Set the **Type** to **OAuth 2.0**.</span><span class="sxs-lookup"><span data-stu-id="1846c-140">Set the **Type** to **OAuth 2.0**.</span></span>
1. <span data-ttu-id="1846c-141">Verify that you have selected the environment that you created.</span><span class="sxs-lookup"><span data-stu-id="1846c-141">Verify that you have selected the environment that you created.</span></span>
1. <span data-ttu-id="1846c-142">Click on **Get New Access Token**.</span><span class="sxs-lookup"><span data-stu-id="1846c-142">Click on **Get New Access Token**.</span></span><br>
    <span data-ttu-id="1846c-143">![In Authorization tab, set Type to OAuth 2.0](../media/postman-set-type.png)</span><span class="sxs-lookup"><span data-stu-id="1846c-143">![In Authorization tab, set Type to OAuth 2.0](../media/postman-set-type.png)</span></span><br>
1. <span data-ttu-id="1846c-144">Set the following values in the dialog.</span><span class="sxs-lookup"><span data-stu-id="1846c-144">Set the following values in the dialog.</span></span> <span data-ttu-id="1846c-145">Select `Implicit` from the **Grant Type** dropdown menu.</span><span class="sxs-lookup"><span data-stu-id="1846c-145">Select `Implicit` from the **Grant Type** dropdown menu.</span></span> <span data-ttu-id="1846c-146">You can set the **Token Name** to whatever you like and leave other keys to the default values.</span><span class="sxs-lookup"><span data-stu-id="1846c-146">You can set the **Token Name** to whatever you like and leave other keys to the default values.</span></span><br>

    <span data-ttu-id="1846c-147">![Get new Access Token](../media/postman-access-token.png "Get new Access Token")</span><span class="sxs-lookup"><span data-stu-id="1846c-147">![Get new Access Token](../media/postman-access-token.png "Get new Access Token")</span></span><br>

> [!NOTE]
> <span data-ttu-id="1846c-148">If you are configuring environments in Postman for multiple Dynamics 365 for Customer Engagement apps instances using different user credentials, you may need to delete the cookies cached by Postman.</span><span class="sxs-lookup"><span data-stu-id="1846c-148">If you are configuring environments in Postman for multiple Dynamics 365 for Customer Engagement apps instances using different user credentials, you may need to delete the cookies cached by Postman.</span></span> <span data-ttu-id="1846c-149">Click on **Cookies** link, that can be found under the **Send** button and remove the saved cookies from the **Manage Cookies** dialog box.</span><span class="sxs-lookup"><span data-stu-id="1846c-149">Click on **Cookies** link, that can be found under the **Send** button and remove the saved cookies from the **Manage Cookies** dialog box.</span></span><br><span data-ttu-id="1846c-150">![Remove Cookies](../media/postman-cookies.png "Remove Cookies")</span><span class="sxs-lookup"><span data-stu-id="1846c-150">![Remove Cookies](../media/postman-cookies.png "Remove Cookies")</span></span><br>
> <span data-ttu-id="1846c-151">Some of these cookies are very persistent.</span><span class="sxs-lookup"><span data-stu-id="1846c-151">Some of these cookies are very persistent.</span></span> <span data-ttu-id="1846c-152">You can delete some of them in groups, but others may have to be deleted individually.</span><span class="sxs-lookup"><span data-stu-id="1846c-152">You can delete some of them in groups, but others may have to be deleted individually.</span></span> <span data-ttu-id="1846c-153">You may need to do this twice to ensure that no cookies remain.</span><span class="sxs-lookup"><span data-stu-id="1846c-153">You may need to do this twice to ensure that no cookies remain.</span></span>

1. <span data-ttu-id="1846c-154">Click **Request Token**.</span><span class="sxs-lookup"><span data-stu-id="1846c-154">Click **Request Token**.</span></span> <span data-ttu-id="1846c-155">When you do this an Azure Active Directory login page will appear.</span><span class="sxs-lookup"><span data-stu-id="1846c-155">When you do this an Azure Active Directory login page will appear.</span></span> <span data-ttu-id="1846c-156">Enter your username and password.</span><span class="sxs-lookup"><span data-stu-id="1846c-156">Enter your username and password.</span></span>
1. <span data-ttu-id="1846c-157">After the token is generated, scroll to the bottom and click **Use Token**.</span><span class="sxs-lookup"><span data-stu-id="1846c-157">After the token is generated, scroll to the bottom and click **Use Token**.</span></span> <span data-ttu-id="1846c-158">This will close the **Manage Access Tokens** dialog.</span><span class="sxs-lookup"><span data-stu-id="1846c-158">This will close the **Manage Access Tokens** dialog.</span></span> 
1. <span data-ttu-id="1846c-159">After you have added a token, you can select which token to apply to requests.</span><span class="sxs-lookup"><span data-stu-id="1846c-159">After you have added a token, you can select which token to apply to requests.</span></span> <span data-ttu-id="1846c-160">Click on the **Available Tokens** drop-down and select the token you have just created.</span><span class="sxs-lookup"><span data-stu-id="1846c-160">Click on the **Available Tokens** drop-down and select the token you have just created.</span></span> <span data-ttu-id="1846c-161">The Authorization header gets added to the Web API request.</span><span class="sxs-lookup"><span data-stu-id="1846c-161">The Authorization header gets added to the Web API request.</span></span>


<span data-ttu-id="1846c-162">See [Test your connection](#test-your-connection) for steps to verify your connection.</span><span class="sxs-lookup"><span data-stu-id="1846c-162">See [Test your connection](#test-your-connection) for steps to verify your connection.</span></span>

<a name="bkmk_connectonpremise"></a>

## <a name="connect-with-an-on-premise-environment"></a><span data-ttu-id="1846c-163">Connect with an On-premise environment</span><span class="sxs-lookup"><span data-stu-id="1846c-163">Connect with an On-premise environment</span></span>

1. <span data-ttu-id="1846c-164">Launch the Postman desktop application.</span><span class="sxs-lookup"><span data-stu-id="1846c-164">Launch the Postman desktop application.</span></span>
2. <span data-ttu-id="1846c-165">Click on the **Environment Options** gear icon in top-right corner.</span><span class="sxs-lookup"><span data-stu-id="1846c-165">Click on the **Environment Options** gear icon in top-right corner.</span></span> 
3. <span data-ttu-id="1846c-166">In the **Manage Environments** dialog box that opens up, click on **Add** button to add a new environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-166">In the **Manage Environments** dialog box that opens up, click on **Add** button to add a new environment.</span></span>
4. <span data-ttu-id="1846c-167">In the dialog box that opens, add a name for the environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-167">In the dialog box that opens, add a name for the environment.</span></span> <span data-ttu-id="1846c-168">Then copy the following key-value pairs into the editing space.</span><span class="sxs-lookup"><span data-stu-id="1846c-168">Then copy the following key-value pairs into the editing space.</span></span>

|||
|----|---|
|<span data-ttu-id="1846c-169">url</span><span class="sxs-lookup"><span data-stu-id="1846c-169">url</span></span>|`http://yourservername/yourorgname`|
|<span data-ttu-id="1846c-170">phiên bản</span><span class="sxs-lookup"><span data-stu-id="1846c-170">version</span></span>|`8.2`|
|<span data-ttu-id="1846c-171">webapiurl</span><span class="sxs-lookup"><span data-stu-id="1846c-171">webapiurl</span></span>|`{{url}}/api/data/v{{version}}/`|

<span data-ttu-id="1846c-172">![Create a new Postman environment to connect with On-premise instance](../media/postman-add-onprem-env.png "Create a new Postman environment to connect with On-premise instance")</span><span class="sxs-lookup"><span data-stu-id="1846c-172">![Create a new Postman environment to connect with On-premise instance](../media/postman-add-onprem-env.png "Create a new Postman environment to connect with On-premise instance")</span></span>

5. <span data-ttu-id="1846c-173">Replace the instance URL placeholder value with your Dynamics 365 for Customer Engagement apps instance URL and click **Add** to save the environment.</span><span class="sxs-lookup"><span data-stu-id="1846c-173">Replace the instance URL placeholder value with your Dynamics 365 for Customer Engagement apps instance URL and click **Add** to save the environment.</span></span>
6. <span data-ttu-id="1846c-174">Close the **Manage environments** dialog.</span><span class="sxs-lookup"><span data-stu-id="1846c-174">Close the **Manage environments** dialog.</span></span>

### <a name="set-credentials"></a><span data-ttu-id="1846c-175">Set Credentials</span><span class="sxs-lookup"><span data-stu-id="1846c-175">Set Credentials</span></span>

1. <span data-ttu-id="1846c-176">On the Authorization tab select **NTLM Authentication [Beta]**.</span><span class="sxs-lookup"><span data-stu-id="1846c-176">On the Authorization tab select **NTLM Authentication [Beta]**.</span></span>
1. <span data-ttu-id="1846c-177">Set the following values in the form:</span><span class="sxs-lookup"><span data-stu-id="1846c-177">Set the following values in the form:</span></span><br>
<span data-ttu-id="1846c-178">•   **Username**:  Just the alias, do not include the domain.</span><span class="sxs-lookup"><span data-stu-id="1846c-178">•   **Username**:  Just the alias, do not include the domain.</span></span><br>
<span data-ttu-id="1846c-179">•   **Password**: You have the option to show the password.</span><span class="sxs-lookup"><span data-stu-id="1846c-179">•   **Password**: You have the option to show the password.</span></span><br>
<span data-ttu-id="1846c-180">•   **Domain**: This must be set if you are accessing the account from a different domain, although you can set it to ~ so that the default domain of the server will be used.</span><span class="sxs-lookup"><span data-stu-id="1846c-180">•   **Domain**: This must be set if you are accessing the account from a different domain, although you can set it to ~ so that the default domain of the server will be used.</span></span><br>

<span data-ttu-id="1846c-181">Your authentication may look like this if you are logging in as administrator.</span><span class="sxs-lookup"><span data-stu-id="1846c-181">Your authentication may look like this if you are logging in as administrator.</span></span><br>

<span data-ttu-id="1846c-182">![Click on Authorization tab, and select NTLM Authentication](../media/postman-ntlm-auth.png "Click on Authorization tab, and select NTLM Authentication")</span><span class="sxs-lookup"><span data-stu-id="1846c-182">![Click on Authorization tab, and select NTLM Authentication](../media/postman-ntlm-auth.png "Click on Authorization tab, and select NTLM Authentication")</span></span>



<span data-ttu-id="1846c-183">See the steps below to test your connection.</span><span class="sxs-lookup"><span data-stu-id="1846c-183">See the steps below to test your connection.</span></span>

## <a name="test-your-connection"></a><span data-ttu-id="1846c-184">Test your connection</span><span class="sxs-lookup"><span data-stu-id="1846c-184">Test your connection</span></span>

<span data-ttu-id="1846c-185">Follow the given steps to create a new Web API request to test connection with your Dynamics 365 for Customer Engagement apps instance with a simple request using <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI function" />.</span><span class="sxs-lookup"><span data-stu-id="1846c-185">Follow the given steps to create a new Web API request to test connection with your Dynamics 365 for Customer Engagement apps instance with a simple request using <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI function" />.</span></span>
1. <span data-ttu-id="1846c-186">Select `GET` as the HTTP method and add `{{webapiurl}}WhoAmI` in the editing space.</span><span class="sxs-lookup"><span data-stu-id="1846c-186">Select `GET` as the HTTP method and add `{{webapiurl}}WhoAmI` in the editing space.</span></span>
<span data-ttu-id="1846c-187">![WhoAmI function request](../media/postman-whoami-request.png "WhoAmI function request")</span><span class="sxs-lookup"><span data-stu-id="1846c-187">![WhoAmI function request](../media/postman-whoami-request.png "WhoAmI function request")</span></span>
2. <span data-ttu-id="1846c-188">Click on **Send** to send this request.</span><span class="sxs-lookup"><span data-stu-id="1846c-188">Click on **Send** to send this request.</span></span>
3. <span data-ttu-id="1846c-189">If your request is successful, you should see the data from the <xref href="Microsoft.Dynamics.CRM.WhoAmIResponse?text=WhoAmIResponse ComplexType" /> that is returned by the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span><span class="sxs-lookup"><span data-stu-id="1846c-189">If your request is successful, you should see the data from the <xref href="Microsoft.Dynamics.CRM.WhoAmIResponse?text=WhoAmIResponse ComplexType" /> that is returned by the <xref href="Microsoft.Dynamics.CRM.WhoAmI?text=WhoAmI Function" />.</span></span>

## <a name="see-also"></a><span data-ttu-id="1846c-190">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="1846c-190">See Also</span></span>

[<span data-ttu-id="1846c-191">Use Postman to perform operations</span><span class="sxs-lookup"><span data-stu-id="1846c-191">Use Postman to perform operations</span></span>](use-postman-perform-operations.md)<br>
[<span data-ttu-id="1846c-192">Use the Dynamics 365 for Customer Engagement Web API</span><span class="sxs-lookup"><span data-stu-id="1846c-192">Use the Dynamics 365 for Customer Engagement Web API</span></span>](../use-microsoft-dynamics-365-web-api.md)<br>
[<span data-ttu-id="1846c-193">Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1846c-193">Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory</span></span>](../walkthrough-register-dynamics-365-app-azure-active-directory.md)
