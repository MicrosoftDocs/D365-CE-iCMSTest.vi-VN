---
title: Connect to Dynamics 365 for Customer Engagement web services using OAuth (Developer Guide for Dynamics 365 for Customer Engagement apps)| MicrosoftDocs
description: Learn how to connect to Dynamics 365 for Customer Engagement web services using OAuth and how the ADAL API manages OAuth 2.0 authentication with the Dynamics 365 for Customer Engagement web service identity provider
ms.custom: ''
ms.date: 03/13/2018
ms.reviewer: ''
ms.service: crm-online
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: get-started-article
applies_to:
- Dynamics 365 for Customer Engagement (online)
ms.assetid: 05696c45-2a01-4787-aad5-87e2afef2b7f
caps.latest.revision: 20
author: JimDaly
ms.author: jdaly
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: 31f9ac1ab7959707d5eefa3e3e49ef4114767b8d
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387758"
---
# <a name="connect-to-dynamics-365-for-customer-engagement-web-services-using-oauth"></a><span data-ttu-id="6537d-103">Connect to Dynamics 365 for Customer Engagement web services using OAuth</span><span class="sxs-lookup"><span data-stu-id="6537d-103">Connect to Dynamics 365 for Customer Engagement web services using OAuth</span></span>

[!INCLUDE[](../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="6537d-104">OAuth is the authentication method supported by the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Web API, and is one of two authentication methods for the Organization Service – the other being [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] authentication.</span><span class="sxs-lookup"><span data-stu-id="6537d-104">OAuth is the authentication method supported by the [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] apps Web API, and is one of two authentication methods for the Organization Service – the other being [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)] authentication.</span></span> <span data-ttu-id="6537d-105">One benefit of using OAuth is that your application can support multi-factor authentication.</span><span class="sxs-lookup"><span data-stu-id="6537d-105">One benefit of using OAuth is that your application can support multi-factor authentication.</span></span> <span data-ttu-id="6537d-106">You can use OAuth authentication when your application connects to either the Organization service or the Discovery service.</span><span class="sxs-lookup"><span data-stu-id="6537d-106">You can use OAuth authentication when your application connects to either the Organization service or the Discovery service.</span></span>  
  
 <span data-ttu-id="6537d-107">Method calls to the web services must be authorized with the identity provider for that service endpoint.</span><span class="sxs-lookup"><span data-stu-id="6537d-107">Method calls to the web services must be authorized with the identity provider for that service endpoint.</span></span> <span data-ttu-id="6537d-108">Authorization is approved when a valid              OAuth 2.0 (user) access token, issued by [!INCLUDE[pn_microsoft_azure_active_directory](../includes/pn-microsoft-azure-active-directory.md)], is provided in the headers of the message requests.</span><span class="sxs-lookup"><span data-stu-id="6537d-108">Authorization is approved when a valid              OAuth 2.0 (user) access token, issued by [!INCLUDE[pn_microsoft_azure_active_directory](../includes/pn-microsoft-azure-active-directory.md)], is provided in the headers of the message requests.</span></span>  
  
 <span data-ttu-id="6537d-109">The recommended authentication API for use with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] Web API is [Azure Active Directory Authentication Library (ADAL)](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-libraries/), which is available for a wide variety of platforms and programming languages.</span><span class="sxs-lookup"><span data-stu-id="6537d-109">The recommended authentication API for use with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] Web API is [Azure Active Directory Authentication Library (ADAL)](https://azure.microsoft.com/en-us/documentation/articles/active-directory-authentication-libraries/), which is available for a wide variety of platforms and programming languages.</span></span> <span data-ttu-id="6537d-110">The ADAL API manages OAuth 2.0 authentication with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web service identity provider.</span><span class="sxs-lookup"><span data-stu-id="6537d-110">The ADAL API manages OAuth 2.0 authentication with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web service identity provider.</span></span> <span data-ttu-id="6537d-111">For more details on the actual OAuth protocol used, see [Use OAuth to Authenticate with the CRM Service](http://blogs.msdn.com/b/crm/archive/2013/12/12/use-oauth-to-authenticate-with-the-crm-service.aspx).</span><span class="sxs-lookup"><span data-stu-id="6537d-111">For more details on the actual OAuth protocol used, see [Use OAuth to Authenticate with the CRM Service](http://blogs.msdn.com/b/crm/archive/2013/12/12/use-oauth-to-authenticate-with-the-crm-service.aspx).</span></span>  
 
> [!NOTE]
> <span data-ttu-id="6537d-112">You must use the ADAL 2.0 libraries.</span><span class="sxs-lookup"><span data-stu-id="6537d-112">You must use the ADAL 2.0 libraries.</span></span> <span data-ttu-id="6537d-113">All Dynamics 365 for Customer Engagement tools, assemblies, and utilities require the patterns supported by ADAL 2.0.</span><span class="sxs-lookup"><span data-stu-id="6537d-113">All Dynamics 365 for Customer Engagement tools, assemblies, and utilities require the patterns supported by ADAL 2.0.</span></span>
> <span data-ttu-id="6537d-114">The ADAL 3.0 libraries require a sign-in screen to capture user account information and do not provide for passing this account information in a headless fashion as required by Dynamics 365 for Customer Engagement apps.</span><span class="sxs-lookup"><span data-stu-id="6537d-114">The ADAL 3.0 libraries require a sign-in screen to capture user account information and do not provide for passing this account information in a headless fashion as required by Dynamics 365 for Customer Engagement apps.</span></span> 

<span data-ttu-id="6537d-115">Before you can use OAuth authentication to connect with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web services, your application must first be registered with [!INCLUDE[pn_microsoft_azure_active_directory](../includes/pn-microsoft-azure-active-directory.md)].</span><span class="sxs-lookup"><span data-stu-id="6537d-115">Before you can use OAuth authentication to connect with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web services, your application must first be registered with [!INCLUDE[pn_microsoft_azure_active_directory](../includes/pn-microsoft-azure-active-directory.md)].</span></span> [!INCLUDE[pn_azure_active_directory](../includes/pn-azure-active-directory.md)] <span data-ttu-id="6537d-116">is used to verify that your application is permitted access to the business data stored in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] tenant.</span><span class="sxs-lookup"><span data-stu-id="6537d-116">is used to verify that your application is permitted access to the business data stored in a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] tenant.</span></span>  
  
## <a name="authenticate-using-adal"></a><span data-ttu-id="6537d-117">Authenticate using ADAL</span><span class="sxs-lookup"><span data-stu-id="6537d-117">Authenticate using ADAL</span></span>  
 <span data-ttu-id="6537d-118">Basic OAuth web service authentication using ADAL is done using just a few lines of code.</span><span class="sxs-lookup"><span data-stu-id="6537d-118">Basic OAuth web service authentication using ADAL is done using just a few lines of code.</span></span>  
  
```csharp  
// TODO Substitute your correct CRM root service address,   
string resource = "https://mydomain.crm.dynamics.com";  
  
// TODO Substitute your app registration values that can be obtained after you  
// register the app in Active Directory on the Microsoft Azure portal.  
string clientId = "e5cf0024-a66a-4f16-85ce-99ba97a24bb2";  
string redirectUrl = "http://localhost/SdkSample";  
  
// Authenticate the registered application with Azure Active Directory.  
AuthenticationContext authContext =   
    new AuthenticationContext("https://login.windows.net/common", false);  
AuthenticationResult result = authContext.AcquireToken(resource, clientId, new Uri(redirectUrl));  
```  
  
 <span data-ttu-id="6537d-119">The authentication context is returned using a well-known authority provider.</span><span class="sxs-lookup"><span data-stu-id="6537d-119">The authentication context is returned using a well-known authority provider.</span></span> <span data-ttu-id="6537d-120">When you don’t know the [!INCLUDE[pn_azure_active_directory](../includes/pn-azure-active-directory.md)] tenant associated with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance you’re calling, you can use a constant string of `https://login.microsoftonline.com`, which is the authority URL for a multiple tenant scenario.</span><span class="sxs-lookup"><span data-stu-id="6537d-120">When you don’t know the [!INCLUDE[pn_azure_active_directory](../includes/pn-azure-active-directory.md)] tenant associated with the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] apps instance you’re calling, you can use a constant string of `https://login.microsoftonline.com`, which is the authority URL for a multiple tenant scenario.</span></span> <span data-ttu-id="6537d-121">An alternate method to dynamically discover the authority at run time is described later in this topic.</span><span class="sxs-lookup"><span data-stu-id="6537d-121">An alternate method to dynamically discover the authority at run time is described later in this topic.</span></span>  
  
 <span data-ttu-id="6537d-122">The next line of code gets the authentication result that contains the access token you’re looking for.</span><span class="sxs-lookup"><span data-stu-id="6537d-122">The next line of code gets the authentication result that contains the access token you’re looking for.</span></span> <span data-ttu-id="6537d-123">You can send message requests to the web service with this token.</span><span class="sxs-lookup"><span data-stu-id="6537d-123">You can send message requests to the web service with this token.</span></span>  
  
 <span data-ttu-id="6537d-124">A few more items of interest in this code are the string values used.</span><span class="sxs-lookup"><span data-stu-id="6537d-124">A few more items of interest in this code are the string values used.</span></span> <span data-ttu-id="6537d-125">The `resource` variable contains the Transport Layer Security (TLS) or Secure Sockets Layer (SSL) root address, including the domain (organization), of your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server.</span><span class="sxs-lookup"><span data-stu-id="6537d-125">The `resource` variable contains the Transport Layer Security (TLS) or Secure Sockets Layer (SSL) root address, including the domain (organization), of your [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] server.</span></span> <span data-ttu-id="6537d-126">The `clientId` and `redirectUrl` variables contain the app registration information that is the result of registering the app with [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)].</span><span class="sxs-lookup"><span data-stu-id="6537d-126">The `clientId` and `redirectUrl` variables contain the app registration information that is the result of registering the app with [!INCLUDE[pn_Active_Directory](../includes/pn-active-directory.md)].</span></span> <span data-ttu-id="6537d-127">For more information on app registration, see [Walkthrough: Register a Dynamics 365 for Customer Engagement apps with Azure Active Directory](walkthrough-register-dynamics-365-app-azure-active-directory.md).</span><span class="sxs-lookup"><span data-stu-id="6537d-127">For more information on app registration, see [Walkthrough: Register a Dynamics 365 for Customer Engagement apps with Azure Active Directory](walkthrough-register-dynamics-365-app-azure-active-directory.md).</span></span>  
  
## <a name="use-the-access-token-in-message-requests"></a><span data-ttu-id="6537d-128">Use the access token in message requests</span><span class="sxs-lookup"><span data-stu-id="6537d-128">Use the access token in message requests</span></span>  
 <span data-ttu-id="6537d-129">Depending on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] API you’re using, there are two different methods to send a message request to the web services.</span><span class="sxs-lookup"><span data-stu-id="6537d-129">Depending on the [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] API you’re using, there are two different methods to send a message request to the web services.</span></span> <span data-ttu-id="6537d-130">For the Web API, you would typically send an HTTP message request.</span><span class="sxs-lookup"><span data-stu-id="6537d-130">For the Web API, you would typically send an HTTP message request.</span></span> <span data-ttu-id="6537d-131">For the Organization Service, you would send a message request using the web client proxy.</span><span class="sxs-lookup"><span data-stu-id="6537d-131">For the Organization Service, you would send a message request using the web client proxy.</span></span>  
  
### <a name="http-message-request"></a><span data-ttu-id="6537d-132">HTTP message request</span><span class="sxs-lookup"><span data-stu-id="6537d-132">HTTP message request</span></span>  
 <span data-ttu-id="6537d-133">Once you have the access token, you must set the Authorization header of the message request that you are sending to the web service to the access token value and specify the token type of `Bearer`.</span><span class="sxs-lookup"><span data-stu-id="6537d-133">Once you have the access token, you must set the Authorization header of the message request that you are sending to the web service to the access token value and specify the token type of `Bearer`.</span></span> <span data-ttu-id="6537d-134">For more information on the Authorization header, see section 14.8 of the [HTTP/1.1 protocol](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html).</span><span class="sxs-lookup"><span data-stu-id="6537d-134">For more information on the Authorization header, see section 14.8 of the [HTTP/1.1 protocol](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html).</span></span> <span data-ttu-id="6537d-135">The following code demonstrates how this is done using the                          `System.Net.Http.HttpClient` class.</span><span class="sxs-lookup"><span data-stu-id="6537d-135">The following code demonstrates how this is done using the                          `System.Net.Http.HttpClient` class.</span></span>  
  
```csharp  
using (HttpClient httpClient = new HttpClient())  
{  
    httpClient.Timeout = new TimeSpan(0, 2, 0);  // 2 minutes  
    httpClient.DefaultRequestHeaders.Authorization =   
        new AuthenticationHeaderValue("Bearer", result.AccessToken);  
```  
  
### <a name="web-client-requests"></a><span data-ttu-id="6537d-136">Web client requests</span><span class="sxs-lookup"><span data-stu-id="6537d-136">Web client requests</span></span>

<span data-ttu-id="6537d-137">Simply set the <xref:Microsoft.Xrm.Sdk.WebServiceClient.WebProxyClient`1.HeaderToken> property value to the access token when using <xref:Microsoft.Xrm.Sdk.WebServiceClient.OrganizationWebProxyClient> or <xref:Microsoft.Xrm.Sdk.WebServiceClient.DiscoveryWebProxyClient> of the Organization Service.</span><span class="sxs-lookup"><span data-stu-id="6537d-137">Simply set the <xref:Microsoft.Xrm.Sdk.WebServiceClient.WebProxyClient`1.HeaderToken> property value to the access token when using <xref:Microsoft.Xrm.Sdk.WebServiceClient.OrganizationWebProxyClient> or <xref:Microsoft.Xrm.Sdk.WebServiceClient.DiscoveryWebProxyClient> of the Organization Service.</span></span>  
  
## <a name="refresh-the-access-token"></a><span data-ttu-id="6537d-138">Refresh the access token</span><span class="sxs-lookup"><span data-stu-id="6537d-138">Refresh the access token</span></span>

<span data-ttu-id="6537d-139">It’s a recommended best practice to refresh the access token before each call to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web service method.</span><span class="sxs-lookup"><span data-stu-id="6537d-139">It’s a recommended best practice to refresh the access token before each call to a [!INCLUDE[pn_crm_shortest](../includes/pn-crm-shortest.md)] web service method.</span></span> <span data-ttu-id="6537d-140">To refresh the access token, which is cached by ADAL, you simply call the `AcquireToken` method again using the same context.</span><span class="sxs-lookup"><span data-stu-id="6537d-140">To refresh the access token, which is cached by ADAL, you simply call the `AcquireToken` method again using the same context.</span></span>  
  
```csharp    
AuthenticationResult result = authContext.AcquireToken(resource, clientId, new Uri(redirectUrl));  
```  
  
<span data-ttu-id="6537d-141">Afterwards, you once again set the Authorization header with `result.AccessToken` when using the Web API, or the <xref:Microsoft.Xrm.Sdk.WebServiceClient.WebProxyClient`1.HeaderToken> when using the Organization Service.</span><span class="sxs-lookup"><span data-stu-id="6537d-141">Afterwards, you once again set the Authorization header with `result.AccessToken` when using the Web API, or the <xref:Microsoft.Xrm.Sdk.WebServiceClient.WebProxyClient`1.HeaderToken> when using the Organization Service.</span></span>  
  
```csharp    
httpClient.DefaultRequestHeaders.Authorization =   
    new AuthenticationHeaderValue("Bearer", result.AccessToken);  
```  
  
## <a name="discover-the-authority-at-run-time"></a><span data-ttu-id="6537d-142">Discover the authority at run time</span><span class="sxs-lookup"><span data-stu-id="6537d-142">Discover the authority at run time</span></span>

<span data-ttu-id="6537d-143">The authentication authority URL, and the resource URL, can be determined dynamically at run time using the following ADAL code.</span><span class="sxs-lookup"><span data-stu-id="6537d-143">The authentication authority URL, and the resource URL, can be determined dynamically at run time using the following ADAL code.</span></span> <span data-ttu-id="6537d-144">This is the recommended method to use as compared to the well-known authority URL shown previously in a code snippet.</span><span class="sxs-lookup"><span data-stu-id="6537d-144">This is the recommended method to use as compared to the well-known authority URL shown previously in a code snippet.</span></span>  
  
```csharp    
AuthenticationParameters ap = AuthenticationParameters.CreateFromResourceUrlAsync(  
                        new Uri("https://mydomain.crm.dynamics.com/api/data/")).Result;  
  
String authorityUrl = ap.Authority;  
String resourceUrl  = ap.Resource;  
```  
  
<span data-ttu-id="6537d-145">For the Web API, another way to obtain the authority URL is to send any message request to the web service specifying no access token.</span><span class="sxs-lookup"><span data-stu-id="6537d-145">For the Web API, another way to obtain the authority URL is to send any message request to the web service specifying no access token.</span></span> <span data-ttu-id="6537d-146">This is known as a         *bearer challenge*.</span><span class="sxs-lookup"><span data-stu-id="6537d-146">This is known as a         *bearer challenge*.</span></span> <span data-ttu-id="6537d-147">The response can be parsed to obtain the authority URL.</span><span class="sxs-lookup"><span data-stu-id="6537d-147">The response can be parsed to obtain the authority URL.</span></span>  
  
```csharp  
httpClient.DefaultRequestHeaders.Authorization = new AuthenticationHeaderValue("Bearer", "");  
```  
  
### <a name="see-also"></a><span data-ttu-id="6537d-148">Xem thêm</span><span class="sxs-lookup"><span data-stu-id="6537d-148">See also</span></span>  
 <span data-ttu-id="6537d-149">[Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](walkthrough-register-dynamics-365-app-azure-active-directory.md) </span><span class="sxs-lookup"><span data-stu-id="6537d-149">[Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](walkthrough-register-dynamics-365-app-azure-active-directory.md) </span></span>  
 <span data-ttu-id="6537d-150">[Multi-Factor Authentication documentation](https://azure.microsoft.com/en-us/documentation/services/multi-factor-authentication/) </span><span class="sxs-lookup"><span data-stu-id="6537d-150">[Multi-Factor Authentication documentation](https://azure.microsoft.com/en-us/documentation/services/multi-factor-authentication/) </span></span>  
 [<span data-ttu-id="6537d-151">OAuth 2.0</span><span class="sxs-lookup"><span data-stu-id="6537d-151">OAuth 2.0</span></span>](http://oauth.net/2/)
