---
title: Authenticate to use the Online Management API for Dynamics 365 for Customer Engagement| MicrosoftDocs
description: Provides information about authenticating to the Online Management API to perform instance-related operations.
ms.date: 11/27/2017
ms.service: crm-online
ms.topic: conceptual
applies_to: Dynamics 365 for Customer Engagement (online)
ms.assetid: c292c148-01f0-41f6-a2fe-7ed05a01a733
author: KumarVivek
ms.author: kvivek
manager: amyla
search.audienceType:
- developer
search.app:
- D365CE
ms.openlocfilehash: f2ccd0dbb88ad8e4ff4f81bd3aaa77b4f3d56f08
ms.sourcegitcommit: 9f0efd59de16a6d9902fa372cb25fc0baf1c2838
ms.translationtype: HT
ms.contentlocale: vi-VN
ms.lasthandoff: 01/08/2019
ms.locfileid: "387032"
---
# <a name="authenticate-to-use-the-online-management-api"></a><span data-ttu-id="92b37-103">Authenticate to use the Online Management API</span><span class="sxs-lookup"><span data-stu-id="92b37-103">Authenticate to use the Online Management API</span></span>

[!INCLUDE[](../../includes/cc_applies_to_update_9_0_0.md)]

<span data-ttu-id="92b37-104">Online Management API supports OAuth 2.0 protocol for authentication.</span><span class="sxs-lookup"><span data-stu-id="92b37-104">Online Management API supports OAuth 2.0 protocol for authentication.</span></span> <span data-ttu-id="92b37-105">Use [Azure Active Directory (AAD)](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis) to authenticate by obtaining a valid OAuth 2.0 access token, and pass it using the **Authorization** header in your requests to the Online Management API.</span><span class="sxs-lookup"><span data-stu-id="92b37-105">Use [Azure Active Directory (AAD)](https://docs.microsoft.com/en-us/azure/active-directory/active-directory-whatis) to authenticate by obtaining a valid OAuth 2.0 access token, and pass it using the **Authorization** header in your requests to the Online Management API.</span></span>

<span data-ttu-id="92b37-106">The recommended authentication API to use with the Online Management API is [Azure Active Directory Authentication Library (ADAL)](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries), which is available for a wide variety of platforms and programming languages.</span><span class="sxs-lookup"><span data-stu-id="92b37-106">The recommended authentication API to use with the Online Management API is [Azure Active Directory Authentication Library (ADAL)](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries), which is available for a wide variety of platforms and programming languages.</span></span> 

## <a name="how-to-authenticate"></a><span data-ttu-id="92b37-107">How to authenticate?</span><span class="sxs-lookup"><span data-stu-id="92b37-107">How to authenticate?</span></span>

<span data-ttu-id="92b37-108">These are the broad steps to authenticate to the Online Management API service.</span><span class="sxs-lookup"><span data-stu-id="92b37-108">These are the broad steps to authenticate to the Online Management API service.</span></span> 

1. <span data-ttu-id="92b37-109">Register an app with Azure Active Directory to obtain *clientId* and *redirectUrl* values for your app.</span><span class="sxs-lookup"><span data-stu-id="92b37-109">Register an app with Azure Active Directory to obtain *clientId* and *redirectUrl* values for your app.</span></span> <span data-ttu-id="92b37-110">For information about this, see the "App registration for OAuth authentication" section in [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](https://msdn.microsoft.com/library/mt622431.aspx)</span><span class="sxs-lookup"><span data-stu-id="92b37-110">For information about this, see the "App registration for OAuth authentication" section in [Walkthrough: Register a Dynamics 365 for Customer Engagement app with Azure Active Directory](https://msdn.microsoft.com/library/mt622431.aspx)</span></span>

1. <span data-ttu-id="92b37-111">Specify the values obtained from step# 1 in the authentication [helper code](sample-authentication-helper.md):</span><span class="sxs-lookup"><span data-stu-id="92b37-111">Specify the values obtained from step# 1 in the authentication [helper code](sample-authentication-helper.md):</span></span>

    ```csharp
    // TODO: Substitute your app registration values here.
    // These values are obtained on registering your application with the 
    // Azure Active Directory.
    private static string _clientId = "<GUID>";    //e.g. "e5cf0024-a66a-4f16-85ce-99ba97a24bb2"
    private static string _redirectUrl = "<Url>";  //e.g. "app://s7cf7712-b773-4f16-92b3-34cs97a25cc7"
    ```

1. <span data-ttu-id="92b37-112">Discover authority information for Online Management API based on the service URL.</span><span class="sxs-lookup"><span data-stu-id="92b37-112">Discover authority information for Online Management API based on the service URL.</span></span> <span data-ttu-id="92b37-113">For North America region, the service URL is: **https://admin.services.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="92b37-113">For North America region, the service URL is: **https://admin.services.crm.dynamics.com**.</span></span> <span data-ttu-id="92b37-114">For region-specific service URL, see [Service URL](get-started-online-management-api.md#service-url)</span><span class="sxs-lookup"><span data-stu-id="92b37-114">For region-specific service URL, see [Service URL](get-started-online-management-api.md#service-url)</span></span><br /> <span data-ttu-id="92b37-115">Use Azure Active Directory challenge format to determine the authority information based on the service URL of the API.</span><span class="sxs-lookup"><span data-stu-id="92b37-115">Use Azure Active Directory challenge format to determine the authority information based on the service URL of the API.</span></span><br /><span data-ttu-id="92b37-116">We are also determining the resource for the Online Management API (different from the service URL), which will be used in the next step to acquire access token.</span><span class="sxs-lookup"><span data-stu-id="92b37-116">We are also determining the resource for the Online Management API (different from the service URL), which will be used in the next step to acquire access token.</span></span>

    ```csharp
    public static async Task<string> DiscoverAuthority(string _serviceUrl)
    {
        try
        {
            AuthenticationParameters ap = await AuthenticationParameters.CreateFromResourceUrlAsync(
                    new Uri(_serviceUrl + "/api/aad/challenge"));
            _resource = ap.Resource;
            return ap.Authority;
        }
        catch (HttpRequestException e)
        {
            throw new Exception("An HTTP request exception occurred during authority discovery.", e);
        }
        catch (Exception e)
        {
            throw e;
        }
    }
    ```
1. <span data-ttu-id="92b37-117">Use the resource you discoverd in the previous step along with the client ID and redirect URL values of your client app to acquire an access token.</span><span class="sxs-lookup"><span data-stu-id="92b37-117">Use the resource you discoverd in the previous step along with the client ID and redirect URL values of your client app to acquire an access token.</span></span> <span data-ttu-id="92b37-118">Note that you must use the resource, and not service URL to acquire or refresh access token.</span><span class="sxs-lookup"><span data-stu-id="92b37-118">Note that you must use the resource, and not service URL to acquire or refresh access token.</span></span>

    ```csharp
    public AuthenticationResult AcquireToken()
    {
        return _authContext.AcquireToken(_resource, _clientId, new Uri(_redirectUrl),
                PromptBehavior.Always);
    }        
    ```

1. <span data-ttu-id="92b37-119">Once you have the access token, you must set the **Authorization** header of the message request to the access token value, and specify the token type as **Bearer**.</span><span class="sxs-lookup"><span data-stu-id="92b37-119">Once you have the access token, you must set the **Authorization** header of the message request to the access token value, and specify the token type as **Bearer**.</span></span> <span data-ttu-id="92b37-120">Also, set the **Accept-Language** header to specify the preferred language for the response.</span><span class="sxs-lookup"><span data-stu-id="92b37-120">Also, set the **Accept-Language** header to specify the preferred language for the response.</span></span> <span data-ttu-id="92b37-121">The `SendAsync` method in the authentication sets these header values for all the message requests:</span><span class="sxs-lookup"><span data-stu-id="92b37-121">The `SendAsync` method in the authentication sets these header values for all the message requests:</span></span>

    ```csharp
    protected override Task<HttpResponseMessage> SendAsync(
                HttpRequestMessage request, System.Threading.CancellationToken cancellationToken)
    {
        // It is a best practice to refresh the access token before every message request is sent. Doing so
        // avoids having to check the expiration date/time of the token. This operation is quick.
        request.Headers.Authorization = new AuthenticationHeaderValue("Bearer", _auth.AcquireToken().AccessToken);
        
        // Set the "Accept-Language" header
        request.Headers.Add("Accept-Language", "en-US");

        return base.SendAsync(request, cancellationToken);
    }
    ```

<span data-ttu-id="92b37-122">You are all set to execute messages against the Online Management API.</span><span class="sxs-lookup"><span data-stu-id="92b37-122">You are all set to execute messages against the Online Management API.</span></span> <span data-ttu-id="92b37-123">For a sample code that demonstrates how to retrieve all Customer Engagement instances in your Office 365 tenant, see [Quick Start Sample: Retrieve instances in your tenant](sample-quick-start.md)</span><span class="sxs-lookup"><span data-stu-id="92b37-123">For a sample code that demonstrates how to retrieve all Customer Engagement instances in your Office 365 tenant, see [Quick Start Sample: Retrieve instances in your tenant](sample-quick-start.md)</span></span>


### <a name="related-topics"></a><span data-ttu-id="92b37-124">Related Topics</span><span class="sxs-lookup"><span data-stu-id="92b37-124">Related Topics</span></span>  

[<span data-ttu-id="92b37-125">Sample: Authentication helper for the Online Management API</span><span class="sxs-lookup"><span data-stu-id="92b37-125">Sample: Authentication helper for the Online Management API</span></span>](sample-authentication-helper.md)

[<span data-ttu-id="92b37-126">Get started with Online Management API</span><span class="sxs-lookup"><span data-stu-id="92b37-126">Get started with Online Management API</span></span>](get-started-online-management-api.md)

[<span data-ttu-id="92b37-127">Online Management API Reference</span><span class="sxs-lookup"><span data-stu-id="92b37-127">Online Management API Reference</span></span>](/rest/api/admin.services.crm.dynamics.com)
